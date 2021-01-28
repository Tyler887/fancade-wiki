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