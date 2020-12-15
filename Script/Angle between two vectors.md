You can get an angle between two [[vector]]s using this method:

1. Calculate [[cross product]] of the vectors
2. Get [[look rotation]] of both vectors with Up equal to the cross product
3. [["Subtruct" these rotations|How to subtract rotations?]]
4. Get Y component of the resulting rotation (X and Z will equal to 0)

*Note:* when you calculate the cross product and "subtract" the rotations, the arguments should be passed in the same order. Otherwise, the angle will be a negative number.

Script example:

[[uploads/angle_between_vectors.jpg]]