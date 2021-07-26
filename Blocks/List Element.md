Gets a value stored in a list, with index starting from 0 (max 1,048,575). The output can also wired to [[Set Reference]] to store a value in a list. It's what you call an "Array" in other programming language.

[[/uploads/Listelement.png]]

Input:
- Variable: The variable for the list. It only accepts the output of a Get Variable, any output from a different block and the script won't plug.
- Index: Every value in a list is assigned an index (think of it as an ID number). We plug an index to get value from the list with the assigned index.

Output:
- Elements: Outputs the value from the list with the index. It can also be used with [[Set Reference]] to set the value for that index.

## Notes

- Every variable can be treated as a list or a scalar (non-list). When a variable is accessed as a scalar, it points to its value at index 0.
- A non-integer index number is rounded down to the next smallest integer.

## Example

Here is the script for when a player shoots a bullet.

[[/uploads/Screenshot_20210107-112017_Fancade.jpg]]

Let me explain the script:
- We create a bullet, store it in a variable, and set its position to the player's position.
- Assuming that the player faces (0, 0, 1) if its rotation is 0°, we rotate that vector (0, 0, 1) by the player's rotation, and that gets us the player's direction, which should also be the bullet's velocity.
- We add the bullet's position with the velocity and set that to be the bullet's new position, that makes the bullet move.

So far so good, until the player shoots again adding another bullet. The variable can only store one value at a time, so the first bullet and its velocity are replaced with the second, the second bullet moves like it should, but the first bullet stop because it's no longer affected by the script. How do we fix that?

[[/uploads/Screenshot_20210107-114652_Fancade.jpg]]

Lists are like variables, but they can store more values in one, so we just have to store the bullets and their velocities like so. We have to make sure to increment the index, otherwise the next bullet would be stored in the list with the same index giving us the same problem we had with the previous script.

[[/uploads/Screenshot_20210107-121128_Fancade.jpg]]

Next thing we have to do is run the script for every bullet with a [[loop]]. We plug the Counter output of the loop into the Index input of our lists, so that we could access each index and the values one by one. The script runs for every bullet and our problem is solved!