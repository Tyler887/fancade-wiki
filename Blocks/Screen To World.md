Given a screen coordinate, outputs the start and end points of a line going through that point (2 and 400 units away from the camera, respectively). That might sound weird, but usually you'll just wire those points into a [[Raycast]] to find the object the user tapped!

(Due to a technical issue, still to be fixed, the output lags by one frame. I.e. if you [[Set Camera]] on frame N then this block's output will change on frame N+1.)

[[/uploads/Screen_To_World.png]]