Stores the input value into a variable. Think of a variable as a container with a nametag that can only store one value at a time. If you were to set another value to a variable, it will overwrite the previous value of that variable.

[[uploads/Set_Variable1.png | width=336px, alt=Set Variable]]

You can get/output the value from a variable with the same name using the [[Get Variable]] block.

[[uploads/Screenshot_2021_1022_011555_com.martinmagni.fancade.png]]

### Globals

Let's say you have a script inside a block that sets a variable to 1. And you have a script outside of the block to inspect that variable.

[[/uploads/20211022_012115.png]]

As you can see, we've set the variable to 1, but the Get Variable block outputs 0 as if we never set the variable in the first place.

This is because those two variables are local, meaning they can't transfer variable information from one place to another (inside a block to outside the block, or into another block and vice versa).

If we want a variable to share information to another variable in different places, then we would have to globalize them. You can simply press the Global button on the keyboard where you type the variable's name. Global variables gain a `$` at the start of their name.

Note that two variables with the same name with one being a global will not count as the same variables (e.g Number and $Number are not the same).

[[uploads/Screenshot_2021_1022_012758_com.martinmagni.fancade.png]]

### Saved variables

Saved variables were added in Fancade 1.6. Like global variables, you can make a saved variable by pressing the Local/Global/Saved button on the keyboard where you type the variable's name. Saved variables gain a `!` at the start of their name.

[[uploads/Screenshot_2021_1022_012641_com.martinmagni.fancade.png]]

As the name implies, saved variables persist their value from one game session to the next. This is true whether the user ends the game by winning, dying, or simply pausing and returning to the menu.

Additionally, saved variables are shared across all levels in the same game. This allows a player's actions in one level to affect their gameplay in other levels, and to keep track of purchases from the [Menu Item](https://www.fancade.com/wiki/Blocks/Menu%20Item.md) block.

Saved variables currently only work with number variables.

A game can have up to 64 saved num variables