Adds force and/or torque to an object, changing its motion.

Input:
- Object: The object you want to apply force to.
- Force: The force to apply to that object.
- Apply At: Where on the object you want to apply the force, it's applied at the center of mass by default.
- Torque: The rotational equivalent of a linear force, changing the object's rotational motion.

[[/uploads/Addforce.png]]

## Notes

- A torque force applied on the first frame, or the same frame that an object is created, seems to have no effect. (A normal force works just fine, and torque forces work just fine after the first frame. The reason is still unknown, perhaps some peculiarity in Bullet Physics?)