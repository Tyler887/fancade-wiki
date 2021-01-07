Gets a value stored in a list, with index starting from 0 (max 1,048,575). The output can also wired to [[Set Reference]] to store a value in a list.

[[/uploads/Listelement.png]]

## Example

Here is the script for when a player shoots a bullet.

[[/uploads/Screenshot_20210107-112017_Fancade.jpg]]

Let me explain the script:
- We create a bullet, store it in a variable, and set its position to the player's position.
- Assuming that the player faces (0, 0, 1) if its rotation is 0°, we rotate that vector (0, 0, 1) by the player's rotation, and that gets us the player's direction, which should also be the bullet's velocity.
- We add the bullet's position with the velocity and set that to be the bullet's new position, that makes the bullet move.

So far so good, until the player shoots again adding another bullet. The variable can only store one value at a time, so the first bullet and its velocity are replaced with the second, the second bullet moves like it should, but the first bullet stop because it's no longer affected by the script. How do we fix that?

[[/uploads/Screenshot_20210107-114652_Fancade.jpg]]