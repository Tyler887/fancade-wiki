Some blocks have wires sticking out of them. These are *script blocks* and you script by connecting their wires to other script blocks.

When you tap Play, script blocks *execute* and do their thing. E.g. [[Set Score]] sets the current score, so if we wire the [[Number]] 3 to it, the score is set to 3.

[[https://cdn.discordapp.com/attachments/465222839327260672/620193017290293263/ex01_set_score.png]]

Blocks execute top-to-bottom, left-to-right. But you can plug in the yellow *control wires* to change the execution order. This is especially useful when you want to execute a block only some of the time. E.g. here I've wired a [[Button|https://www.fancade.com/wiki/cant_find_buttons_motors_characters]] to [[If|https://www.fancade.com/wiki/if]] to [[Win|https://www.fancade.com/wiki/win]], so when the player moves onto the button, then the game is won:

[[https://cdn.discordapp.com/attachments/465222839327260672/620193021710827531/ex02_win_if_button.png]]

There are other wire colors as well:

* **<font color="00e5ff">Blue</font>** is a number
* **<font color="00ee85">Green</font>** is an `X,Y,Z` vector (such as a position)
* **<font color="ff8543">Orange</font>** is a rotation
* **<font color="ff4343">Red</font>** is either [[True]] or [[False]]
* **<font color="ff85c8">Pink</font>** is an object
* **<font color="a7b1d0">Gray</font>** is a constraint
* **<font color="ffe043">Yellow</font>** is for execution control

That's the basics! Now, you'll probably learn a lot more by looking at some example scripts that show how to do useful game stuff. So start the app and look on the Build tab to find a game called "Tutorial". It's fully editable, so you'll be able to see and play around with each example script.