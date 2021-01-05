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

Every frame, the block rotates 5% (0.05) of the way from its initial rotation (0°) towards its goal (90°). Note that it doesn't rotate on a constant speed, but it eases out/slows down until it comes to a stop at its goal, it's because by every frame, the From input changes itself to be the block's current rotation, which means the distance between From and To gets smaller, therefore 5% of the way towards its goal is smaller than what it was in the previous frames.

Currently, there is only a LERP for rotation values, but if you want make one for numbers or vectors:

[[/uploads/20210105_102823.jpg]]