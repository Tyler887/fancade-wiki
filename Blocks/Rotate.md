Rotates vector by a rotation.

[[/uploads/Rotate_Vector.png]]

## Example

You can move a block to the direction that it's facing.

Since the arrow is facing up by default, the velocity of the arrow should be upwards (0, 0, 0.1). To get the velocity of the block if it's not facing up, we can rotate the velocity (0, 0, 0.1) by the block's rotation. To move the block, we just add the block's position and the velocity and set that to the block's new position.

[[/uploads/Screenshot_20210206-121736_Fancade.jpg]]

With the Rotate block, we can also rotate a block around a pivot, instead of just the center of block itself.

To rotate the block around a pivot, we would rotate the vector from the pivot to the block's starting position (not the current position). Make sure you add the result with the pivot before setting it to the block's new position, otherwise it would end up rotating around (0, 0, 0). Setting the pivot's rotation to the block's rotation is to make it rotate around the pivot instead of circling around it without changing rotation.

[[/uploads/Screenshot_20210113-094731_Fancade.jpg]]