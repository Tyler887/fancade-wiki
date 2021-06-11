The menu item is a script block which is added in Fancade 1.6. When executed at least once with it's "item" input not having null value it activates the shop system adding a shop to the game which is only accessible (probably just for now) when you lose or win the game. The main use of this script is to add items to the shop that **should** be only done once per item. 

Though this new script made a great new mechanics for fancade it has some limitations :
- The base price are currently only fixed to 10 , 100 , 1k & 10k.
- Each menu item script **must** only be executed once per game , if it's left continuosly executing the shop will be filled with repeating set of items until it has too many items in it that will cause the `"too many menu items!"` error.

Items can be either some type of upgrades or boosters just by playing with it's buy limit setting of the menu item script. You can choose between an on/off , Max 2-100 or unlimited buy limit.

To learn how to use it, you can see [here](https://www.fancade.com/wiki/How%20to%20use%20the%20shop%20system.md).

[[/uploads/Screenshot_20210605-101540.png]]