Finds the point at which a line intersects a plane.

[[/uploads/Line_VS_Plane.png]]

Inputs:
* Line From: Line's starting position
* Line To: Line's end position
* Plane Point: A position in the plane (defaults to 0,0,0 if unwired)
* Plane Normal: A vector perpendicular to the plane (i.e. the direction the plane is pointing at, or the angle of the plane)

Outputs:
* Intersection: The point where the line intersects the plane (or nan if there is no such point)

## Notes

* It's a line, not a line segment, so the intersection will be found even if it's not in-between the line's from/to positions.

## Example

A common use case for Line vs Plane is to find the world coordinate of the user's finger:

[[/uploads/line_vs_plane_example01.png]]

The finger touches a 2D screen, but there's a whole bunch 3D points along a line *into* the scene, which are all at that 2D coordinate. So the above script first uses [[Screen To World]] to get two points on that line, and then Line vs Plane to pick out the *one* position that lies on the floor plane (point 0,0,0 and normal 0,1,0). As a result, the Wood block will move to the finger!