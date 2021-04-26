Traces a line between two points and outputs [[True]] if the line hits anything, the position of intersection, and the object it hit. (Think of it as a laser, you stand in the starting position and shoot a laser to the end position.)

Note that Raycast detects when the line hits the outside surface of a block. If the line starts *inside* the block then it will not hit that block when going out. Also, it won't  detect an object that has been created in the same frame, you have to wait 1 frame after creating the object for Raycast to detect it.

It cannot detect [[Pass Through]]s and [[Script Block]]s. However, [[Script Block]]s are invisible in game.

This is useful for Raycast drawing using a [[Marker]].

[[/uploads/Raycast.png]]