The Menu Item block is a script block which was added on Fancade 1.6 beta. When it is  executed at least once it activates the shop system adding a shop to the game which is only accessible when you win or lose the game. The main use of this script is to add items to a shop which should ONLY be done once per item. To learn how to use it, see [here](https://www.fancade.com/wiki/Script/How%20to%20use%20the%20shop%20system%3F.md).

[[/uploads/Screenshot_20210605-101540.png]]

## Notes
Though this new script made a great new mechanic for Fancade it has some limitations:
* The base prices are currently only fixed to 10, 100, 1k & 10k.
* Each menu item script **must** only be executed once per game, if it's left continuosly executing the shop will be filled with repeating set of items until it has too many items in it, which will cause the `Too many menu items!` error to appear.

## More info
Items can be either one type of upgrades or boosters just by playing with the buy limit settings and Variable input of the menu item script. You can choose between ON/OFF, Max 2-100 or no limit.

You also cannot use menu item to add buttons on the top of the screen or the pause menu. Remember the [[top of this page|#top]]?
## Example
You can make a clicker game with Menu Item. So, add a [[touch sensor]], a [[get variable]], a [[increase number]] and this script (Menu Item). Make it detect tap begins. Make it increase variables named `Coins` and `!Score`. (! means saved variable, tap `Local` then `Global` to get `Saved`.)

Now get a [[set score]], plug in `!Score` into the Score wire, and plug `Coins` into the Coins wire.

Add a shop with many items, starting with `More per tap`. This is like in fanclicker by Origedit. Replace the increase number with: set var (add nums, `!Score`, (whatever saved variable you are using for the more per tap item in the shop, ~~lol~~)). Do the same for the `Coins` variable.

Add a way to make the player claim the coins they got in game and submit their score. If you are using a button to do this then check the [[tap to pick closest object]] article, make a unglued object and repeat the scripting in the article image.