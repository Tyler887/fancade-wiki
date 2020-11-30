Assuming you're making a top-down view game, zoom = 5 * block width. E.g. to fit 10 blocks wide, set zoom to 50:

[[https://cdn.discordapp.com/attachments/608689686134784000/612718494869487623/IMG_20190818_234332.png]]

What about height? Well, different users will have different screen sizes, so even with a fixed width the height is variable. But like the image shows, you can compute it by multiplying width by the screen's aspect ratio.

[[https://cdn.discordapp.com/attachments/608689686134784000/612718494856904846/IMG_20190818_234312.png]]

Zoom automatically adapts to the smallest dimension, so in landscape mode the role of height and width are reversed.