You can create a circle by placing multiple objects, like this:
[[/uploads/Screenshot_20210321-143029_Fancade.jpg]]
R is the radius of the circle, W is the lenght of the object used to create the circle and C us the lenght of the circle.

It's important to keep the object offseted to avoid artifacts, meaning that the object should not go past the center.
[[/uploads/Screenshot_20210321-143113_Fancade.jpg/]]
If you want to change the circle in any way after it was drawn, you'd want to store each object in a list, so you could reuse them. It's important for optimizing your game.

If you care less about the exact size of the circle and more about it not being jagged, try following the tutorial on [[polygons|/Build/How to make hexagons?]].