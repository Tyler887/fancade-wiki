The Late Update block will execute scripts _after_ physics.

Since physics will change the position of objects after scripts have run, which is sometimes unwanted, it can be useful to instead run the physics first. This ensures that your scripts are working with the updated positions of the objects.

[[/uploads/Late Update.png]]

## Notes 

Late Update isn't a delay block , most people mistake it as a delay block , but what really is the the use of this block if it seems to not do anything?

Late update runs *after physics* , what does it mean?? ..... In a level a set of function runs in this order :
- Scripts
- Physics
- Late Update 

And that is what it means ... Late Update will run after scripts and physics functions and is useful to control some unwanted things after physics have ran.