There are several ways to achieve it. The first one is changing camera rotation depending on the screen orientation so the way a player flips a device doesn't have an effect on what is displayed on screen:

[[https://cdn.discordapp.com/attachments/544763659625168897/632806501001592872/IMG_20191013_100643.jpg]]

These scripts will set vertical orientation. If you want horizontal, just wire that [[Set Rotation|Set Variable]] to the "Else" plug instead of "True".

The second method is way straightforward, just place the [[Accelerometer]] script block anywhere on floor (don't forget to wire it to something with yellow plugs!) — it will literally lock the screen orientation to a state that was when a game was opened. It's useful when you don't necessarily need a specific orientation to be set but you want it to be unchangeable during gameplay.

[[https://cdn.discordapp.com/attachments/544763659625168897/632654164077576212/Screenshot_2019-10-12-23-59-57-807_com.martinmagni.fancade.png]]

Might be worth noting that all of these are a last resort for games that are not just inconvenient, but impossible, to play in the "other" orientation. Else just let the user play the way they prefer.