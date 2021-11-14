Sometimes in 2D games, we need to completely remove the shadows from the scene. Here is a simple way to do that.

1. Set the camera **angle** to          whatever is needed for the       game.

2. Set the light **angle** to the    **same** angle as the camera.

Example:

[[uploads/shadorem.png]]

That's all!

But there might still be **fuzzy shadow bleed**.


### For a perfect shadow removal

For a perfect shadow removal, we can *move* the camera very far from the scene. It is less convenient, but works perfectly.

For a top-down **2D** game, we can set the camera **Y** value to a **very high** value.

Here is an example using camera 0,100,0:

[[uploads/pershadorem.png]]

(You should use your appropriate camera X and Z values. Set the Y value to a very high value.)

For **3D** games, use the Rotate block to move the camera in the right direction:

[[uploads/firefox_UFxHjI1sMY.png]]

(Explanation for the vector value: If the camera's rotation is 0,0,0 ("no rotation"), the camera is looking in the positive Z direction, so moving it in the negative Z pushes it farther away. Rotating the camera from that default angle causes the back direction to rotate accordingly.)

Note that if the camera is too far away, some objects might not be visible. Decrease the value if that happens.