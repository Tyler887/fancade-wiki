Assuming you're making a top-down view game, zoom = 5 * block width. E.g. to fit 10 blocks wide, set zoom to 50:

[[/uploads/IMG_20190818_234332.png]]

What about height? Well, different users will have different screen sizes, so even with a fixed width the height is variable. But like the image shows, you can compute it by multiplying width by the screen's aspect ratio.

[[/uploads/IMG_20190818_234312.png]]****

Zoom automatically adapts to the smallest dimension, so in landscape mode the role of height and width are reversed.