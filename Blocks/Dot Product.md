Dot product is algebraically defined as the sum of the product of the corresponding vector component.

If we were to find the dot product of Vector A (Ax, Ay, Az) and Vector B (Bx, By, Bz), we would use this formula:
* A•B = (Ax×Bx)+(Ay×By)+(Az×Bz)

A few things to know that might help:
- If the angle formed by the two input vectors is acute, the dot product is positive.
- If the angle is a right angle (both vectors perpendicular), then the dot product is zero.
- If the angle is obtuse, then the dot product is negative.

[[/uploads/Dot Product.png]]

## Example

If the two input vectors are unit vectors (vectors with length of 1), the dot product outputs the cosine of the angles formed by those two vectors. If the two input aren't unit vectors, we can still find the cosine of the angle with two methods:
- Normalize the two input vectors first before the dot product.
- Get the output of the dot product and divide it by the product of the two input vectors' length.

[[/uploads/20210106_122008.jpg]]

We don't have an inverse cosine block, but we can create the script to find the angle:

[[/uploads/Screenshot_20210106-121820_Fancade.jpg]]

Moving on to another example involving a stealth game, there is a guard facing a direction with a FOV of 90° (visually highlighted in green), and there is a ninja sneaking up on him. How can we check if the ninja is on the guard's sight?

[[/uploads/Screenshot_20210106-131627_Fancade.jpg]]

The first input for the dot product is the direction that the guard is facing, the second input is the vector from the guard's position to the ninja's position. Then we compare the cosine of the angle formed by those two vector with the cosine of half the FOV:

[[/uploads/Screenshot_20210106-135840_Fancade.jpg]]

Let me explain the script:
- First we subtract the ninja's position by the guard's position (if it's the other way round, we get the vector from the ninja's position to the guard's position, that's the opposite of what we want). Then we normalize the vector before the dot product.
- For the guard's direction, we get the guard's current rotation and rotate the vector (0, 0, 1) by that rotation. This is only correct if we're assuming that the guard faces in that direction (0, 0, 1) if his current rotation is 0°, otherwise we use a different vector value. We don't have to normalize because we rotated the vector (0, 0, 1) which already has a length of one.
- Finally after we get the dot product (which should be the cosine of the angle formed by those two vectors), we can check if its less than the cosine of half the FOV (half because the direction of the guard sits in the middle between the two edges of the FOV, we would use 90° if the FOV is 180°). If its true, then the ninja is in sight, otherwise the ninja is still safe.