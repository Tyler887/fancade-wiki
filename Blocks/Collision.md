**Collided:** Triggers when the input object collides with another object, including the floor.

**2nd Object:** Outputs the object that the input object collided with. It'll output "None" if collided with the floor.

**Impulse:** Outputs the impact force of the collision (how hard did they collide). Specifically, impulse is a change of momentum of an object.

**Normal:** Outputs the direction of the impact from the object that the input object collided with.

[[/uploads/Collision.png]]

## Examples

The script below causes you to win if the two physics boxes collide with each other.

[[/uploads/c1.png]]

Because the ground counts as "None", the script below causes you to lose if the sphere touches the ground.

[[/uploads/c2.png]]