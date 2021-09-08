The Menu Item block is a script block which is added in Fancade 1.6 beta. When executed at least once it activates the shop system adding a shop to the game which is only accessible when you lose or win the game. The main use of this script is to add items to the shop that **should** be only done once per item. To learn how to use it, see [here](https://www.fancade.com/wiki/How%20to%20use%20the%20shop%20system.md).

[[/uploads/Screenshot_20210605-101540.png]]

## Notes
Though this new script made a great new mechanic for Fancade it has some limitations:
* The base price are currently only fixed to 10, 100, 1k & 10k.
* Each menu item script **must** only be executed once per game, if it's left continuosly executing the shop will be filled with repeating set of items until it has too many items in it that will cause the `Too many menu items!` error.

## More info
Items can be either one type of upgrades or boosters just by playing with the buy limit settings and Variable input of the menu item script. You can choose between an on/off, Max 2-100 or unlimited buy limit.