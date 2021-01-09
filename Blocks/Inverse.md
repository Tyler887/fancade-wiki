Outputs the inverse of the input [[rotation]].

[[/uploads/Inverse.png]]

Input :
- Rot : rotation value

Output :
- Rot Inverse : the inverse of the rotation

## Details
The inverse of a rotation is the rotation that, when [[combined|Combine]] with the original rotation, equals the identity rotation (0, 0, 0).

In math, the inverse of a value with respect to some operation is the value that "undoes" the operation.

For example, the additive inverse of `5` is `-5`, since `5 + -5 = 0`. If you add 5, then subtract 5, you get back the original value.

The multiplicative inverse of `5` is `1/5`, since `5 * 1/5 = 1`. If you multiply by 5, then divide by 5, you get back the original value.

The same applies to rotations. The inverse of a rotation can be used to "undo" that rotation. If you combine with a rotation, then combine that with the rotation's inverse, you get back the original rotation. 

Normally, the inverse of a rotation on it's own is not useful, and is usually combined with another rotation.

