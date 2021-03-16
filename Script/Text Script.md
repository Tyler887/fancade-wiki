Fancade games are made with drag-n-drop of functional building blocks. A sort of visual programming suitable for touch screen devices, if you will.

This page, however, describes an inofficial pseudo code text format, inspired by Fancade's script blocks, and worked on by @Isaglish, @JP16D, @Qma, and @Vex Ave on Discord.

[[_TOC_]]

# Fancade Coding Text Format

This Format will be a basis when sharing or suggesting some codes and code solutions during script discussions. Take this as an easier way to share or suggest a code program instead doing it in fancade and go back to fancade server #scripting channel. Well in case of people that couldn't understand this ... Sorry we can't do anything about it :P so just do the thing in fancade , screenshot it and share it to them.


### Introduction
This format is based on C# syntax. Most of things are simplified for better understanding.

As you know , Fancade's script blocks are located in different folders. To make it easier to understand , what it means , use their names as in the example below. It's not necessary and takes such a time to write , but please pay attention to it when you're explaining script to the new user or there are namesake custom blocks.

Following the C# syntax , let's imagine that each folder is a separate class with its own fields and functions. So , to represent Get Frame block , you need to type `Game.Frame`. Again , it's not necessary , just `Frame` is fine too.

All the cases:
```coffeescript
# If block has yellow wires, add () at the end of the name
Game.Win();
Sound.PlaySound();

# If block has inputs, count them and their type in the brackets
Objects.SetPosition(obj object, vec position, rot rotation);

# If block has more than one output you will need to define them individually 
# Use '.outputname' after the function to define them
Objects.GetPosition(target_object).position;

# Math block counts like this, except the basic ones listed below
vec result = Math.LineVsPlane(from, to, normal, point);

# If block has only outputs, don't do anything
num frame = Game.Frame;
```

**____________________________________**
### Basics
**____________________________________**

#### Value Types 
```coffeescript
# Variables and Data Types
num varName = 0;
tru varName = true/false;
vec varName = (x , y , z);
rot varName = (x , y , z);
obj varName = MyBlocks.BlockName;

# To make global variables, simply add a $ sign as a prefix of a variable name
obj me = Myblocks.Me
vec $myPosition = Objects.GetPosition(me).position

# Any variable can be used as list by using the format: varName[index]

#To define wire input values use
wire_wireName = value
#This can be use In case of functions that uses another functions to their inputs
#so that it doesn't look very messy unlike when directly placing them 
#(can this thing be called the spaghetti wires in text scripting 0w0)

```
**____________________________________**

#### Basic Math Operators
**____________________________________**

```coffeescript
# Add Numbers
2 + 2

# Subtract Numbers
2 - 2

# Multiply Numbers
2 * 2

# Divide Numbers
2 / 2

# Power
2 ^ 2

# Modulo
2 % 2

# Increase
num++

# Decrease
num--
```
**____________________________________**

#### Basic Boolean Operators
**____________________________________**
```coffeescript
# Boolean logic (and, or, not)

tru fruit = ((not lettuce) and (orange)) or apple;

# Math (Greater, Less, Equal)

tru equal = a == b;

tru greater = a > b;

tru less = a < b;
```

**____________________________________**

### Game 
**____________________________________**
```coffeescript
Game.Win();

Game.Lose();

Game.SetScore(num Score);

Game.SetCamera(vec Position, rot Rotation, num Distance);

Game.SetLight(vec Position, rot Rotation);

Game.ScreenSize.x
Game.ScreenSize.y

Game.Accelerometer

Game.Frame
```

**____________________________________**

### Objects
**____________________________________**
```coffeescript
Objects.GetPosition(obj).position
Objects.GetPosition(obj).rotation

Objects.SetPosition(obj Object, vec position, rot Rotation);

# alternatives

# Set Position
obj.position = vec;
obj.rotation = rot;

# Get Position
vec = obj.position;
rot = obj.rotation;

Objects.Raycast(vec, vec).hit
Objects.Raycast(vec, vec).hitPos
Objects.Raycast(vec, vec).hitObj

Objects.GetSize(obj Object).min
Objects.GetSize(obj Object).max

Objects.CreateObject(obj Object);

Objects.DestroyObject(obj Object);
```

**____________________________________**

### Sound
**____________________________________**
```coffeescript
Sound.PlaySound(num Volume, num Pitch);
num sfx = Sound.PlaySound(num Volume, num Pitch).channel

Sound.StopSound(num Channel);

Sound.VolumePitch(num Channel, num Volume, num Pitch);
```

**____________________________________**

### Physics
**____________________________________**
```coffeescript
Physics.AddForce(obj Object, vec Force, vec applyAt, vec Torque);

vec playerVelocity = Physics.GetVelocity(obj Object).velocity;
vec playerVelocity = Physics.GetVelocity(obj Object).spin;

Physics.SetVelocity(obj Object, vec Force, vec Spin);

Physics.SetLocked(obj Object, vec Position, vec Rotation);

Physics.SetMass(obj Object, num Mass);

Physics.SetFriction(obj Object, num Friction);

Physics.SetBounciness(obj Object, num Bounciness);

Physics.SetGravity(vec Gravity);

const constraint = Physics.AddConstraint(obj Base, obj Part, vec Pivot).constraint;

Physics.LinearLimits(const Constraint, vec Lower, vec Upper);

Physics.AngularLimits(const Constraint, vec Lower, vec Upper);

Physics.LinearSpring(const Constraint, vec Stiffness, vec Damping);

Physics.AngularSpring(const Constraint, vec Stiffness, vec Damping);

Physics.LinearMotor(const Constraint, vec Speed, vec Force);

Physics.AngularMotor(const Constraint, vec Speed, vec Force);

```


**____________________________________**

### Control
**____________________________________**
```coffeescript
# Basic if operator
If (condition) { 
    function_true;
} else { 
    function_false;
}

# Loop
Loop(num start = 0, num end = 0) {
    //Output
    out.counter
}

# Sensors
TouchSensor('touching' , '1st') { 
    //Outputs
    out.screen.x
    out.screen.y
}

Collision(obj mainObject) {
    //Outputs
    out.secondObject
    out.impulse
    out.normal
}

BoxArt() {
}

PlaySensor() {
}

LateUpdate() {
}
```

**____________________________________**

### Math
**____________________________________**
```coffeescript
Math.Negate(num Num)

Math.Inverse(rot Rot)

vec.Scale(num Num)

vec.Rotate(rot Rot)

rot1.Combine(rot Rot2)

Math.Random(num Min, num Max)

Math.RandomSeed(num Seed);

Math.Min(num Num1, num Num2)

Math.Max(num Num1, num Num2)

Math.Sin(num Num)

Math.Cos(num Num)

Math.Round(num Num)

Math.Floor(num Num)

Math.Ceil(num Num)

Math.Absolute(num Num)

Math.Log(num Num, num Base)

# break vectors into number variables.
num = vec.x
num = vec.y
num = vec.z

vec.Normalize

vec.Dot(vec Vector)

vec.Cross(vec Vector)

# break a rotation into number variables.
num rot.x
num rot.y
num rot.z

Math.Distance(vec Vec1, vec Vec2)

Math.LERP(rot From, rot To, num Amount)

Math.AxisAngle(vec Axis, num Angle)

Math.ScreenToWorld(num ScreenX, num ScreenY)

Math.WorldToScreen(vec WorldPos).x
Math.WorldToScreen(vec WorldPos).y

Math.LineVsPlane(vec From, vec To, vec Point, vec Normal)

Math.LookRotation(vec Direction, vec Up)
```
### (Important!) Editing Notes
***To all contributors and people who edits the Fancade Pseudo-Coding Language*** , Pls don't put too much extensions to the things as much as possible , extensions such as `Math.` or `Objects.` , this thing is very unnecessary since it will only be used in scripting discussion , unless... one of us can implement it as a real coding language ;D

# Syntax

Ever wondered how Fanscript would look in text format? Well, you can see all references in this directory!

Keep in mind that this is a Work-In-Progress project and that all codes you see will not work if you try to write it in say Unity's C#.

## Examples
Datatypes consist of:

```coffeescript
num Age = 10
vec Position = (10, 1.51, 5)
rot Angle = (0, 90, 0)
tru Hit = True
obj Player = MyBlocks.Player
```

For the constraints, it'll be the same inside Fancade:

```coffeescript
PlaySensor() {
    const constraint = Physics.AddConstraint(base, part, pivot)
    Physics.AngularLimits(constraint, (0, 0, 1), (0, 0, 0))
    Physics.AngularMotor(constraint, (0, 0, 90), (0, 0, 100))
}
```

In total we have 7 datatypes that includes lists.

Talking about lists here is how you do them in text format:

```coffeescript
# set a list variable
vec Positions[0] = (32.1, 5.51, -23.72)

# to access a list
num.Inspect(num phoneNumbers[2])
```

## Datatypes

In Fancade we have a total of 7 datatypes. These datatypes are num, vec, rot, tru, obj, const, and list.

The number type can be either a whole number or in decimals, in the programming world we call these "int" and "float/double".

Here are some examples:
```coffeescript
num jumpSpeed = 0.2
vec level = (1, 1, -10)
rot fan = (0.1, 0, 0)
tru blocked = False
obj me = MyBlocks.Me
```

For the constraint, here is how you do it:
```coffeescript
PlaySensor() {
    const constraint = Physics.AddConstraint(base, part, pivot)
    Physics.AngularLimits(const, (0, 0, 1), (0, 0, 0))
    Physics.AngularMotor(const, (0, 0, 90), (0, 0, 100))
}
```
To create variables simply type:
`Datatype variableName`

And to initialize:
`Datatype variableName = value`

For the lists here is an example:
```coffeescript
PlaySensor() {
    obj landmine = MyBlocks.LM
    obj $LM[num $LM] = landmine
    vec $LM[num $LM] = Objects.GetPosition(landmine).position
    num $LM++
}
```

To access values inside a list:
```coffeescript
Loop(0, $landmines) {
    num i = self.currentIndex
    vec landminePositions = vec $LM[num i]
}
```

### Example

Here is [[Martin Magni]]'s Shepherd game in text format.

```coffeescript
# Init
obj $Herder = MyBlocks.Herder
obj Sheep = MyBlocks.Sheep

# Sheep script
TouchSensor("First").touching {
    Physics.AddForce(Sheep, Math.LineVsPlane(Math.ScreenToWorld(self.screen.x, self.screen.y), (0, 2, 0), (0, 2, 0)) - Objects.GetPosition(Sheep).position)
}

num $Dist = Math.Max(Math.Distance(Objects.GetPosition(Sheep).position, Objects.GetPosition($Herder).position), $Dist)

Collision(Sheep) {
    If (this.secondObject == None) {
        Game.Lose(False)
    }
}

# Herder script
If (num $Dist < 2) {
    Game.Win(False)
}
num $Dist = 0


```