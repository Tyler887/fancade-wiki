The Loop block is used to run a script multiple times in the same frame. Often used for processing every element in a list.

Inputs
- Start: The Loop blocks starts looping from the Start input.
- Stop: Then it stops looping once it reaches the Stop input.

Outputs
- Do: Plug this to the script that you want to run for every loop.
- Counter: Outputs the current loop number counting from the Start value. If the Start value is greater than the Stop value, it counts down instead of up.

[[/uploads/Loop.png]]

If you were to start the loop at 0 and stop it at 5, you would loop the script 5 times (Count) and the Counter outputs from 0 to 4 (End). Which shows that the Counter won't output the Stop value by the end of the loop, might want to keep that in mind.

[[/uploads/Screenshot_20210128-114243_Fancade.jpg]]

## Example

Beginners often just place the script in the block that they want to process, in which every blocks of the same type would have the same script. For cases where the script is small or there aren't too many of the same type of blocks in a level, it won't cause much of a problem. Otherwise, you may easily run into a script limit while you're placing those blocks in a level.

We could put those blocks in a list and loop the script for every block, so that we could process every block we need with only one script, instead of having to add duplicates of that script.

In the example below, we're moving the blocks by (0, 0, 0.1) every frame.

[[/uploads/Screenshot_20210128-171605_Fancade.jpg]]

I mentioned previously that the Counter won't output the Stop value by the end of the loop. It won't be a problem because after we add the last block to a list, it increments the $Length variable by one. So, if the last block is assigned to index 4, $Length would equal to 5 which is exactly what the Stop input should be to account for every blocks.