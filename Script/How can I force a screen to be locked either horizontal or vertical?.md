Fancade can be played in portrait or landscape mode, whichever you're most comfortable with. Games made with Fancade might work best in portrait or landscape, but should try to support both.

That said, creators have discovered ways of *forcing* the player to use one mode or the other. Here's how you can do that, even though you shouldn't.

There are several ways to achieve it. The first one is changing camera rotation depending on the screen orientation so the way a player flips a device doesn't have an effect on what is displayed on screen:

[[/uploads/IMG_20191013_100643.jpg]]

These scripts will set vertical orientation. If you want horizontal, just wire that [[Set Rotation|Set Variable]] to the "Else" plug instead of "True".

The second method is way straightforward, just place the [[Accelerometer]] script block anywhere on floor (don't forget to wire it to something) — it will literally lock the screen orientation to a state that was when a game was opened. It's useful when you don't necessarily need a specific orientation to be set but you want it to be unchangeable during gameplay.

[[/uploads/Screenshot_2019-10-12-23-59-57-807_com.martinmagni.fancade.png]]
