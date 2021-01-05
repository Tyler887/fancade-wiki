Linear Interpolation (LERP) returns a value between two others at a point of linear scale.

The formula for the LERP output is:
From + (To - From) × Amount


Input:
- From: The value to transition from.
- To: The value to transition to.
- Amount: How far to transition.

Output:
- Rotation: 

[[/uploads/Lerp.png]]

## Example

[[/uploads/Screenshot_20201205-2212052.png|alt=LERP usage example]]

Explaination of the above script: Rot A is the rotation of the block. Use get position if you made the block to have other rotations too (You have to get the rotation in a single frame, or else it will become a loop of the LERP script trying to set it back to Rot B.). Rot B is the rotation you want the block to go to. Set B to the rotation you want. "Speed" is the speed of changing the rotation A to rotation B. 
Now it will be easier to understand LERP, with which you can do smooth rotations.
What LERP actually does, is giving a rotation between the first rotation input and the second one. The number input is how far between those roation the output should be. 0 will output the first rotation, 1 will output the second rotation, 0.5 will output a rotation exactly in the middle of the two inputs, etc.