Fancade 1.6 adds a new script block called [[Menu Item]] and a currency named [[Coins]]. This page is a guide on how to use them.

Currently the only way to access the shop is by winning or losing.

# Coins
To use the coins, just take a number variable and connect it to the `Coins` input in the score block. 

[[/uploads/Captura_de_pantalla_2021-06-02_143144.png]]

When you play-test the game you should see the coin counter at the corner of the screen. To get coins just increment the variable you used as the coin counter.

[[/uploads/Captura_1.png]]

*Note: When making a game, you can give yourself free coins to test your upgrade shop. They won't count as coins in the actual game though.*

# Menu items
To use the menu items, first take a block out of the inventory, and after placing it in the floor you will see two kinds of inputs: a Picture input and a Variable input.

[[/uploads/Captura_de_pantalla_2021-06-02_142338.png]]

The Picture input is the object that will be displayed for the corresponding item in the Shop.

The Variable input uses a variable to save the current state of the upgrade.
You will need to use a saved variable (!Var) for this or it'll be completely useless.

There's also other options when you select the block:

[[/uploads/Captura_2.png]]

Name: how the item will be named in the shop. 

[[/uploads/Captura_3.png]]

If there's no Variable connected to the Variable input then it'll show as a title on a new page.

[[/uploads/Captura_4.png]]

Buy Limit: this sets the amount of times that object can be upgraded. For example: let's say you set it on Max 2.

[[/uploads/Captura_5.png]]

The corresponding object in the shop system will have to be upgraded 2 times to be maxed out.

[[/uploads/Captura_6.png]]

If you leave it as On/Off, you'll be able to upgrade it once, and toggle it on and off, like an extra mode or a cheat code.
If the connected Variable is \-1, that means OFF. You can set it to \-1 or 1 to avoid the purchase. 

[[/uploads/Captura_7.png]]

But if you set it to No Limit then the upgrade will have no limit and you will be able to buy it how many times you want.
*Note: "No Limit" comes after Max 100 in that menu.*

[[/uploads/Screenshot_20210609-192759.png]]

Price Type:
This changes the price of the upgrade after you've bought it. 

"Fixed":
If left on "10 fixed", the price will stay on 10 coins every time you buy the upgrade. 

"Linear":
If it is on 10 Linear, then the price will increase by 10 coins each time you buy the upgrade. 

"Double":
If set to 10 Double, then the price doubles each time you buy the upgrade. 

And you even get a bigger price if you keep clicking after 10 Double! The existing prices are 100, 1k (1,000) and 10k (10,000) and all of them have the same options except for 10k, which only has the fixed option.

[[/uploads/Captura_8.png]]

# Variables

The [[menu item]] has the input called variable, this input can only accept number variable type inputs and not number value type inputs. Though this maybe the case you can somehow do sorcery with it by using the same variable before the menu item and giving that variable a value.

- For example you use the variable `!var` and given it a value of 2 before feeding it to a menu item (with a setting of `max 5`/`price 100`/`price double`) the upgrade will be then immediately upgraded to level 2 with a price of 400 for the next upgrade.

- Playing with it's variable is not as simple as it is though. setting the value of the variable before the menu item means overwriting the existing value of the variable, one work around to it tho is by using [[max]] math block which outputs the higher number, that means on start being the variable having value of 0 feeding it to max with the other input of it having value of 2 the max will output the 2 and will feed it back to variable, then if the variable has a value of 3 now with the same case with max the max will output 3 as it is higher than 2 and will feed 3 back to itelf preventing value overwrite. This method though is not absolute as it doesn't work with on/off type items, in this case if blocks and truth values will be the one to help. 

With this in mind you can try to get more complex and have your shop with items that can be bought/upgraded interestingly.

# How to use the bought upgrades

To use these, take the saved variable (!Var) you sticked into the Variable input and use it in whatever you want. Normally the variables are equal to the upgrade level of the certain upgrade. For example, if used a Max 5 upgrade then the variable can be equal to the values of 0 through 5. If used a On/Off upgrade, the variable can only equal \-1, 0 or 1. If used a No Limit upgrade, the variable can equal 0 through N (all natural numbers.)

# Limits.

- 6 Pages
- 100 Items (including Titles)

## Buggy effects of negative numbers
Negative values do work with other settings besides on/off, but they change the button to look like OFF. It still works, and the calculation that generates the price just uses the negative number.
For example, 10 \* 2^\-2 for 10 Double and other fractions are rounded down, here to 2.
Linear Prices will give you coins on \-2 and less
