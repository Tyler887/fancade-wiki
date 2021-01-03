Create a rotation pointing in a given direction, e.g. rotating a character to look that way.

[[/uploads/Look_Rotation.png]]

Inputs:
* Direction: The direction you want to look in
* Up: Which way is up for the looing character (defaults to 0,1,0 if unwired)

Outputs:
* Rotation: A rotation "looking" in the direction.

## Notes

* The Up input can often be ignored, but is needed if the default 0,1,0 is in the same plane as the Direction input.

## Examples

Passing e.g. 0,0,5 as Direction will result in a rotation looking forward along the Z axis.