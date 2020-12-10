The Late Update block will execute scripts _after_ physics.

Since physics will change the position of objects after scripts have run, which is sometimes unwanted, it can be useful to instead run the physics first. This ensures that your scripts are working with the updated positions of the objects.