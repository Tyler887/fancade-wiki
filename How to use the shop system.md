**Note: The shop system is only accessible on the beta version of Fancade 1.6.4 for now.**

Ok, so you wanna learn how to use the shop system, don't you? Well, I'm gonna tell you everything I figured out while using the shop system.

Currently the only way to access the shop is by losing or winning.
Also, you will need to use a saved variable (!Var) or it'll be completely useless.

# Coins
To use the coins, just take a number variable and stick it to the new coins input in the score block. 

[[/uploads/Captura_de_pantalla_2021-06-02_143144.png]]

When you test-play the game you should see the coin counter at the corner of the screen. To get coins just increment the variable you used as the coin counter.

[[/uploads/Captura_1.png]]

*Note: When making a game, you can give yourself free coins to test your upgrade shop. They won't count as coins in the actual game though.*

# Menu items
To use the menu items, first take a block out of the inventory, then you are going to use two kinds of inputs: a picture input and a variable input.

[[/uploads/Captura_de_pantalla_2021-06-02_142338.png]]

The Picture input is the object that will appear when looking at the according "Upgrade it" references.

The Variable input uses a variable to save the current state of the upgrade.

There's also other options when you select the block:

[[/uploads/Captura_2.png]]

Name: how the item will be named in the shop. 

[[/uploads/Captura_3.png]]

If the block isn't connected to something else and/or neither there's no object connected to the Picture input nor a Variable then it'll show as title on a new page.

[[/uploads/Captura_4.png]]

On/Off: this sets the amount of times that object can be upgraded. For example: let's say you set it on Max 2.

[[/uploads/Captura_5.png]]

The corresponding object in the shop system will have to be upgraded 2 times to be maxed out.

[[/uploads/Captura_6.png]]

If you leave it as On/Off, you'll be able to upgrade it once, and toggle it on and off, like an extra mode or a cheat code.

[[/uploads/Captura_7.png]]

"Fixed": 
This changes the price of the upgrade after you've bought it. If left on "10 fixed", the price will stay on 10 coins every time you buy the upgrade. 

"Linear":
If it is on 10 Linear, then the price will increase by 10 coins each time you buy the upgrade. 

"Double":
If set to 10 Double, then the price doubles each time you buy the upgrade. 

And you even get a bigger price if you keep clicking after 10 Double! The existing prices are 100, 1k (1,000) and 10k (10,000) and all of them have the same options except for 10k, which only has the fixed option.

[[/uploads/Captura_8.png]]

# Limits

- 6 Pages
- 92 Items (including Titles)

Note: Due to a bug, 100 items will break fangold/gems menu, because it also occupies 8 items. Don't do that or your game may be unpublished.

***

And that's about it! If the page needs some extra information, or I wrote something wrong, please correct it. Let's keep updating this page so more people can learn how to use:
**_The shop system!_**