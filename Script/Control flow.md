**Control flow** is a programming term that means the order that the steps of a computer program are executed, and the ways a programmer can control that order to do things like loops, if/then branches, or more advanced patterns like event handlers. This page describes how control flow works in Fancade scripting.

# Statements and expressions

For purposes of control flow, it's useful to think of script blocks as belonging to one of two categories:

## Statements

**Statements** are script blocks that make changes to the game's state (or as we sometimes say in programming, they have "side effects"). A statement might [[play a sound|Blocks/Play Sound]], [[write a value|Blocks/Set Variable]] to a variable, [[change the position|Blocks/Set Position]] of an object, [[cause another statement to run|Blocks/If]], etc.

Statements are easy to recognize &mdash; **they always have yellow "before" and "after" wires** at top and bottom.

Only statements are subject to control flow. Because they have side effects, their order of execution is important!

## Expressions

**Expressions** are script blocks that _do not_ make changes to the game's state. Instead, they provide data values which can be inputs to statements or other expressions. An expression might add two numbers together, [[read a value|Blocks/Get Variable]] from a variable, [[measure|Blocks/Get Position]] an object's position, etc.

Expressions are only evaluated when they're an input to the currently executing statement (or an input to an input, etc...). When that happens, they're evaluated against the game's _current state_. An expression can be an input to multiple statements, in which case it'll be evaluated again for each of them, against the current game state each time.

# The tick cycle

The basic unit of time in Fancade is the "tick". There are 60 ticks to a second, and the script blocks get a chance to run in every tick. The physics engine also updates the state of physics-enabled objects once per tick (and scripts can execute after the physics update, using the [[Late Update|Blocks/Late Update]] block.)

During the script execution phase of a tick, statements are executed synchronously, one at a time. Even though the wires may make it look like things are multi-threaded, they are not!

# Instruction sequencing

There are two basic ways to determine the sequence that statements get executed: **Execution order** wires, and script block **positioning** (See also: [[Execution Order]])

## 1. "Execution order" wires

The **<font color="ffe043">yellow</font>** "before" and "after" wires that all statements have, are called "execution order" wires.

* After a statement executes, it sends a run signal to its **"after"** wire.
* If a statement block has its **"before"** wire attached to another block, it will run each time a run signal is sent down that wire
    * (If its "before" wire isn't attached to anything, it'll run **once per tick** according to its position, as described in the next section.)

Some things to be aware of:

* These connections can be many-to-many &mdash; a statement can send its "run" signal to multiple recipients, or it can receive "run" signals from multiple senders
* A statement can run many times in a single tick, if it receives multiple "run" signals. This is usually caused by Control statements (see below), though it can also be from having multiple "before" connections.
* A statement will not run at all in a tick, if its "before" wire is connected but it receives no "run" signal. This can only happen due to Control statements.

## 2. Positioning

If a statement block does **not** have a wire attached to its "before" input, it will be executed **once on every tick\***. These disconnected statements are sequenced according to their position in the game field. Statements are executed top to bottom, left to right, like words on a page.

Specifically, they're ordered like so:

1. Z axis, descending
2. X axis, ascending
3. Y axis, descending

This same ordering also controls the order of execution when multiple statements have their "before" wires attached to the same "after" wire.

**\* Note:** As an exception to the rule, the [[Play Sound|Blocks/Play Sound]] and [[Stop Sound|Blocks/Stop Sound]] blocks will **not** run at all if their "before" wire isn't attached to anything. But all other statement blocks will execute once per tick if their "before" wire is unattached.

## Working together

With positioning and execution order wires together, the full ordering sequence is something like this:

1. The uppermost, leftmost statement with no "before" input gets executed first.
2. Any blocks connected to its "after" wire get executed next, followed by any blocks connected to _their_ "after" wire, and so on.
3. The next statement with no "before" input gets executed, followed by any blocks connected to its "after" wire.

# Control statements

Blocks in the "Control" category are the main way you can modify the control flow beyond simple before/after sequencing. Control statement blocks are colored yellow, the same as execution order wires, and they all have one or more additional execution order wires sticking out of their right side (along with the normal "before" and "after" wires).

When a control block executes, it may send a run signal down its "third wire" (or multiple run signals, for the [[Loop block|Blocks/Loop]]). The same as an "after" wire, the "third wire" can be attached to another statement's "before" wire, and it will cause that block to execute each time the control block sends a run signal.

Control blocks also have the same "before" and "after" wires as other statement blocks, and these work alongside the "third wire":

* If a control block's "before" wire is connected, the control block won't signal along its "after" wire or its "third wire" unless and until it receives a run signal.
    * And it can send a pulse down its "third wire" every time it receives a run signal
* When a control block executes, it sends any "third wire" run signals **before** it sends its "after" wire's run signal.
    * So all the blocks connected to the third wire will execute before any blocks connected to the "after" wire.
* After a control block executes, it sends a run signal down its "after" wire. This happens whether or not it sent a signal down its "third wire".

There are a few general types of control blocks:

## Branching and looping

These blocks give you basic control structures that you'd find in most programming languages.

* [[If|Blocks/If]] takes a boolean value as an input, and sends a run signal down its "True" wire or its "False" wire
* [[Loop|Blocks/Loop]] acts like a [https://en.wikipedia.org/wiki/For_loop for loop]. It takes a numeric "start" value and "end" value, and it sends a run signal down its third wire once for every number from "start" to "end".

## Event handling

These blocks act something like [event handlers](https://en.wikipedia.org/wiki/Event-driven_programming#Event_handlers). They send a run signal down their third wire in response to an event from an outside source (user input, or the physics engine).

* [[Touch Sensor]]
* [[Swipe Sensor]]
* [[Collision Sensor|Collision]]

Although they're somewhat like event handlers, they're still governed by the execution ordering rules. Basically, if their triggering event happened during this tick, then the block will send a run signal down its third wire when (or if) the block executes during this tick.

## Timing modifiers

* [[Play Sensor|Blocks/Play Sensor]] sends a run signal down its third wire only on the game's first tick. It's used for initial setup tasks that should only run once.
* [[Box Art Sensor|Blocks/Box Art Sensor]] sends a run signal down its third wire only when the game is being executed to take a picture for box art. It's used to customize a game's box art imagery.
* [[Late Update|Blocks/Late Update]] sends a run signal down its third wire in a special final phase of the tick, after the physics engine has run. It's used to provide same-tick response to physics changes.