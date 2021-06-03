Ok, so you wanna learn how to use the shop system, don't you? Well, I'm gonna tell you everything I figured out while using the shop system.

_Note: The shop system is only accessible on the beta version of Fancade 1.6.4_

Currently the only way to access the shop is by losing or winning.
Also, you will need to use a saved variable (!Var) or it'll be completely useless.

# Coins
To use the coins, just take a number variable and stick it to the new coins input in the score block. 

![Score block](https://cdn.discordapp.com/attachments/788803873330298880/849717918266032158/Captura_de_pantalla_2021-06-02_143144.png)

When you test-play the game you should see the coin counter at the corner of the screen. To get coins just increment the variable you used as the coin counter.

![Coin counter](https://cdn.discordapp.com/attachments/788803873330298880/849718303794004058/unknown.png)

*Note: When making a game you can give yourself free coins to test your upgrade shop. They won't count as coins in the actual game though.*

# Menu items
To use the menu items, first take a block out of the inventory, then you gotta use two kinds of inputs: a picture input and a variable input.

![Menu item block](https://cdn.discordapp.com/attachments/788803873330298880/849715742093475851/Captura_de_pantalla_2021-06-02_142338.png)

The Picture input is the object that will appear when looking at the according "Upgrade it" references.

The Variable input uses a variable to save the current state of the upgrade.

There's also other options when you select the block:

![Menu item block options](https://cdn.discordapp.com/attachments/788803873330298880/849720257870037012/unknown.png)

Name: how the item will appear nicknamed in the shop. 

![Menu item name](https://media.discordapp.net/attachments/788803873330298880/849719245243940874/unknown.png?width=351&height=467)

If the block isn't connected to something else and/or neither there's no object connected to the Picture input nor a Variable then it'll show as title on a new page.

![Menu page title](https://cdn.discordapp.com/attachments/788803873330298880/849720693074952232/unknown.png)

On/Off: this sets the amount of times that object can be upgraded. For example: let's say you set it on Max 2.

![Max 2](https://cdn.discordapp.com/attachments/788803873330298880/849721190892830750/unknown.png)

The corresponding object in the shop system will have to be upgraded 2 times to be maxed out.

![Max 2 showcase](https://cdn.discordapp.com/attachments/788803873330298880/849721737809231972/unknown.png)

If you leave it as On/Off, you'll be able to upgrade it once, and toggle it on and off, like an extra mode or a cheat code.

![On/Off showcase](https://cdn.discordapp.com/attachments/788803873330298880/849722559334711296/unknown.png)

"Fixed": 
This changes the price of the upgrade after you've bought it. If left on "10 fixed", the price will stay on 10 coins every time you buy the upgrade. 

"Linear":
If it is on 10 Linear, then the price will increase by 10 coins each time you buy the upgrade. 

"Double":
If set to 10 Double, then the price doubles each time you buy the upgrade. 

And you even get a bigger price if you keep clicking after 10 Double! The existing prices are 100, 1k (1,000) and 10k (10,000) and all of them have the same options except for 10k, which only has the fixed option.

![10 Linear showcase](https://cdn.discordapp.com/attachments/788803873330298880/849724272485335070/unknown.png)

# Limits

6 Pages
92 Items (including Titles)

P.S. Due to bug 100 items will break fangold/gems menu, because it also occupy 8 items. Dont do that or your game may be unpublished.

***

And that's about it! If the page needs some extra information, or I wrote something wrong, please correct it. Let's keep updating this page so more people can learn how to use:
**_The shop system!_**