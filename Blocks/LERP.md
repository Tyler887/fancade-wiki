Linear Interpolation (LERP) returns a value between two others at a point of linear scale.

The formula for the LERP output is:
From + (To - From) × Amount

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

On every frame, the block rotates from it's initial rotation (From) closer to it's target rotation (To) by a scaled amount (Speed), 
