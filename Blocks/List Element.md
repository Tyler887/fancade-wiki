Gets a value stored in a list, with index starting from 0 (max 1,048,575). The output can also wired to [[Set Reference]] to store a value in a list.

[[/uploads/Listelement.png]]
## Notes
The list basically is what you call in scripting language as "Array", But what really is this array. An array is single variable which can contain multiple values , in then which each is value defined as this varible[index] , normally index in real scripting is automatically generated depending on its order e.g. in JS language: 
`var list = new Array["Hello", "Hi" , "Bye"]`
`document.write(list[0])`

In which in outputs "Hello" as hello is defined as variable `list` and its index is `[0]`.

*auto-generated index in all text script language always start with index 0.

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

Next thing we have to do is run the script for every bullet with a [[loop]]. We plug the Counter output of the loop into the Index input of our lists, which helps us get access to the individual values stored in the list. The script runs for every bullet in the list.