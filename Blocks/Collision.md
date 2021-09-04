Collision checks the collision properties of the input object.

Output:
- Collided: Triggers when the input object collides with another object, including the floor.
- 2nd Object: The object that the input object collided with. It outputs "None" if collided with the floor.
- Impulse: The impact force of the collision (how hard did they collide). Specifically, impulse is a change of momentum of an object.
- Normal: The direction of the impact from the 2nd object to the 1st object.

[[/uploads/Collision.png]]

## Notes

- If you're colliding with multiple objects it'll report the most forceful collision.
- If you're overriding physics to move objects (using [[Set Position]]) then no collisions will occur. (Is this a issue with Bullet Physics?)

## Examples

The script below causes you to win if the two physics boxes collide with each other.

[[/uploads/c1.png]]

Because the ground counts as "None", the script below causes you to lose if the sphere touches the ground.

[[/uploads/c2.png]]

Triggers a sound effect only if the impulse is big enough.

[[/uploads/20210103_135824.jpg]]