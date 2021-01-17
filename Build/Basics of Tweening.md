Suppose, you need to move an object from point A to point B. You'll have to find the point between the two each frame of the transition, meaning you'll need to store the phase of the transition in a variable. Let's call it Tween. Tween will vary from 0 to 1, increasing each frame. Then Tween will be used in a simple vector Interpolation (for more information, [check this article](https://www.fancade.com/wiki/Blocks/LERP.md)). Let's take a look:

[[/uploads/photo_2021-01-17_10-49-05.jpg]]

Works fine, but if you'll take a closer look, you'll notice that the movement is rough. Notice that there's a variable called Int, and it's set to Tween, suggesting that the interpolation is linear.

[[/uploads/linear_int.jpg]]

Maybe we can apply some expressions to that variable to achieve a different kind of movement. Here are some simple ones, followed by their simple graphs (**made in Fancade!!**):

[[/uploads/sine_int.jpg]][[uploads/sine_int_graph.jpg]]
[[/uploads/square_int.jpg]][[/uploads/square_int_graph.jpg]]
[[/uploads/smoothstep.jpg]][[/uploads/smoothstep_graph.jpg]]

Take a look at the last one, it's the one we need to make the movement smooth on both sides! It's called Smoothstep and it's really useful in our situation. Put this script in the main one and you're good to go