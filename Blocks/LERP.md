Linearly interpolates between two rotations.

[[/uploads/Lerp.png]]

Here's a script to get you started.

![LERP_example](https://cdn.discordapp.com/attachments/520112989416718346/784828563726794812/Screenshot_20201205-2212052.png)

Explaination of the above script: Rot A is the rotation of the block. Use get position if you made the block to have other positions too (You have to get the rotation in a single frame, or else it will become a loop of the LERP script trying to set it back to Rot B.). Rot B is the rotation you want the block to go to. Set B to the rotation you want. "Speed" is the speed of changing the rotation A to rotation B. 
Now it will be easier to understand LERP, with which you can do smooth rotations.