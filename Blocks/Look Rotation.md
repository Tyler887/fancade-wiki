Create a rotation pointing in a given direction, e.g. rotating a character to look that way.

[[/uploads/Look_Rotation.png]]

Inputs:
* Direction: The direction you want to look in
* Up: Which way is up for the looking character (defaults to 0,1,0 if unwired)

Outputs:
* Rotation: A rotation "looking" in the direction.

## Notes

* When converting one direction (vector) into a rotation, there is actually an infinite number of solutions! You can visualise this by picking up an object, say a pencil, and point it in some direction. You'll notice that you can still spin the pencil (thus changing it's rotation) without changing the direction it's pointing. That's why we define a second "Up" vector. It helps define how the pencil should be oriented. (It can often be ignored, but is definitely needed if the default 0,1,0 is in the same plane as the Direction input.)

## Examples

Passing e.g. 0,0,5 as Direction will result in a rotation looking forward along the Z axis.