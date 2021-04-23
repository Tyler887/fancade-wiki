This is a tutorial on how to create a perfect regular hexagon in Fancade. This exact method is used to create hexagons in games Hexoban and Hexals.

## Classic method

Hexagons are made out of 6 square pieces, properly placed, and rotated. First of all, we need to create a square piece. We're going to create a green hexagon with a darker boundary, so our piece looks like this: 

[[/uploads/Screenshot_20210423-140008~2.jpg | height=200px]]

This piece will be copied 5 times and the other pieces will be placed relative to the original one. To obtain the coordinates of the remaining pieces, we need to add the following vectors to the position of the original piece:
- (-0.317, 0, 0.183),
- (-0.317, 0, 0.549),
- (0, 0, 0.732),
- (0.317, 0, 0.183),
- (0.317, 0, 0.549).

These coordinates are not exact (the exact coordinates are irrational and they require a square root of three), but three decimal places is enough for our hexagon to look good. Let's put them in a list (starting from index 1 for convenience):

[[/uploads/Screenshot_20210423-140026~2.jpg | height=500px]]

Now our hexagon can be created with a simple loop. We create the remaining pieces and we set their positions using the list above. We also need to rotate them (by 60&deg;, 120&deg; etc) and for that, we're going to use the Make Rotation block. The loop looks like this:

[[/uploads/Screenshot_20210423-140054~2.jpg | height=450px]] 

Let's start the script now. See what happened to our original object!

[[/uploads/Screenshot_20210423-140112~2.jpg | height=250px]]

Here we go! A perfect regular hexagon!

## Advanced method

Instead of creating the list of positions, they can be calculated in Fancade using trigonometric functions. Using this method, we can also create regular polygons with a different number of sides!

We need three additional variables. Variable **N** is the number of sides of our polygon, while **X** and **Z** denotes the size of our original square object.

Now we need to calculate the vector from the origin of our polygon to the origin of our square object. We're going to call it **A**. Its X and Y coordinates are both equal to 0, while the Z coordinate can be computed using trigonometry:

 **A** = (0, 0, 0.5(**Z** - **X** &sdot; cot(180&deg;/**N**))).

This is how it looks in Fancade. Here we use the fact that the cotangent of an angle is equal to its cosine divided by its sine:

[[/uploads/Screenshot_20210423-180421~2.jpg | height = 180px]]

Now, to calculate the positions of the remaining pieces, we can subtract **A** from the position of the original object and then add **A** rotated by a certain angle. Here's how it looks:

[[/uploads/Screenshot_20210423-180438~2.jpg | height = 500px]]

For **N** = 6 and **X** = **Z** = 1, we obtain the exact same hexagon as in the classic method, without using any additional lists! After changing the value of **N**, we can obtain different polygons, for instance, a pentagon:

[[/uploads/Screenshot_20210423-183301~2.jpg | height = 200px]]

If **N** is bigger than 6, we obtain a polygon with a hole in the middle. To avoid that, we simply need to enlarge our original object and change the values of **X** and **Z**.

[[/uploads/Screenshot_20210423-183341~2.jpg | height = 200px]]