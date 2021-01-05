Linear Interpolation (LERP) returns a value between two others at a point of linear scale.

Rotation = From + (To - From) × Amount

[[uploads/LERP.png]]

Input:
- From: The value to transition from.
- To: The value to transition to.
- Amount: How far to transition.

Output:
- Rotation: The value between the From and To input, at a linear scale (defined by Amount input).

## Example

The most common use case is to smoothly transition from one rotation to another.

[[/uploads/20210105_102823.jpg]]

Every frame, the block rotates 5% (0.05) of the way from its initial rotation to its destination.