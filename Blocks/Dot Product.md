Dot product is algebraically defined as the sum of the product of the corresponding vector component.

If we were to find the dot product of Vector A (Ax, Ay, Az) and Vector B (Bx, By, Bz), we would use this formula:\
A•B = (Ax×Bx)+(Ay×By)+(Az×Bz)

[[/uploads/Dot Product.png]]

## Example

If the two input vectors are unit vectors (vectors with length of 1), the dot product outputs the cosine of the angles formed by those two vectors. If the two input aren't unit vectors, we can still find the cosine of the angle with two methods:

- Normalize the two input vectors first before the dot product.

- Get the output of the dot product and divide it by the product of the two input vectors' length.

[[/uploads/20210106_122008.jpg]]

We don't have an inverse cosine block, but we can create one to find the angle:

[[/uploads/Screenshot_20210106-121820_Fancade.jpg]]

Moving on to another example involving a stealth game, there is a guard facing a direction with a FOV of 90° (visually highlighted in green), and there is a ninja sneaking up on him. How can we check if the ninja is on the guard's sight?

[[/uploads/Screenshot_20210106-131627_Fancade.jpg]]