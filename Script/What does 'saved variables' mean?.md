A saved variable is a variable whose value persists (isn't reset) between play sessions. It was made for [[Menu Item]] to work. Saved variables were introduced in Fancade 1.6.

If a local variable is accessible on the same floor, and a global variable is accessible on the same level, then a saved variable is accessible everywhere inside the game, regardless of any limit! This is really useful if you want to create custom game settings, autosave, a shop system, or others 

Saved variables currently only work with number variables, and a saved variable can't be used as a list. A game can have up to 64 saved variables.

Saved variables are saved whenever the player wins, loses, or leaves a game, but not when Fancade is force-closed from the task menu. If the game is stored in the Edit section, opening the editor resets all saved variables, and they won't be saved when played from inside it. During box art generation (the game is run for a single frame every time a level is selected), saved variables can both be read from and written to; take note of that if you have any scripts writing to them in the first frame.