This is a tutorial how to create a perfect regular hexagon in Fancade. This exact method is used to create hexagons in games Hexoban and Hexals.

## Classic method

Hexagons are made out of 6 square pieces, properly placed and rotated. First of all, we need to create one such a square piece. We're going to create a green hexagon with a darker boundary, so our piece looks like this: 

[[/uploads/Screenshot_20210423-140008~2.jpg | height=200px]]

This piece will be copied 5 times and the other pieces will be placed relatively to the original one. To obtain the coordinates of the remaining pieces, we need to add the following vectors to the position of the original piece:
- (-0.317, 0, 0.183),
- (-0.317, 0, 0.549),
- (0, 0, 0.732),
- (0.317, 0, 0.183),
- (0.317, 0, 0.549).

These coordinates are not exact (the exact coordinates are irrational and they require a square root of three), but three decimal places is enough for our hexagon to look good. Let's put them in a list (starting from the index 1 for convenience):

[[/uploads/Screenshot_20210423-140026~2.jpg | height=500px]]

Now our hexagon can be created with a simple loop. We create the remaining pieces and we set their positions using the list above. We also need to rotate them (by 60&deg;, 120&deg; etc) and for that we're going to use Make Rotation block. The loop looks like this:

[[/uploads/Screenshot_20210423-140054~2.jpg | height=450px]] 

Let's start the script now. See what happened to our original object!

[[/uploads/Screenshot_20210423-140112~2.jpg | height=250px]]

Here we go! A perfect regular hexagon!

## Advanced method

Instead of creating the list of positions, they can be calculated in Fancade using trigonometric functions.

(TBA)