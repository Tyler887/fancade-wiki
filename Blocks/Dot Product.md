The Dot Product calculates the dot product of the two input vectors, and outputs a [[number]].

The dot product is written using a central dot:

A · B

This means the dot product of the vectors A and B.

[[/uploads/Dot Product.png]]

## Details

The Dot Product is a way of multiplying two vectors together.

We can calculate the Dot Product of two vectors this way:

A · B = \|A\| × \|B\| × cos(θ)

Where \|A\| is the magnitude (length) of vector A, \|B\| is the magnitude (length) of vector B, and θ is the angle between A and B.

So we multiply the length of A times the length of B, then multiply by the [[cosine|Cos]] of the angle between A and B.

We can also calculate it algebraically this way:

A · B = Ax × Bx + Ay × By + Az × Bz

So we multiply the x's, multiply the y's, multiply the z's, and then sum them all together.

The result is a [[number]] (called a "scalar" so we know it's not a vector).

### Right Angles

When two vectors are at right angles to each other the dot product is zero. This can be a handy way of checking if two vectors are perpendicular.

If the angle formed by the two input vectors is acute, the dot product is positive.

If the angle is obtuse, then the dot product is negative.

## Example

The dot product of two [[unit vector|Normalize]]s outputs the cosine of the angle between those two vectors. If our two inputs aren't unit vectors, we can find the cosine with two methods:
- Normalize the two input vectors first.
- Get the output of the dot product and divide it by the product of the two input vectors' length.

[[/uploads/20210106_122008.jpg]]

To find the angle, we then use the inverse cosine function:

[[/uploads/Screenshot_20210106-121820_Fancade.jpg]]

Here is another example, there is a guard facing a direction with a FOV of 90° (highlighted in green) and a ninja sneaking up on him. How can we check if the ninja is on sight?

[[/uploads/Screenshot_20210106-131627_Fancade.jpg]]

The first input for the dot product is the direction that the guard is facing, the second input is the vector from the guard's position to the ninja's position. Then we compare the cosine of the angle formed by those two vector with the cosine of half the FOV:

[[/uploads/Screenshot_20210106-135840_Fancade.jpg]]

Let me explain the script:
- First we subtract the ninja's position by the guard's position. Then we normalize the vector before the dot product.
- For the guard's direction, rotate the vector (0, 0, 1) by the guard's current rotation (because assuming that the guard faces up (0, 0, 1) if his current rotation is 0°).
We don't have to normalize because the vector we rotated (0, 0, 1) already has a length of one.
- Finally after we get the dot product, check if its less than the cosine of half the FOV (half because the direction of the guard sits in the middle between the two edges of the FOV). If true, then the ninja is in sight, otherwise the ninja is still safe.