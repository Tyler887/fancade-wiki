Like [[Set Variable]], but with an additional input for the variable to store the value in. This enables you to store a variable in a [[List Element]], or make custom script blocks that modify variables.

[[/uploads/Setreference.png]]

## Example

You can find an example of making lists in the [[List Element]] page. So we'll focus on another use.

Let's say we want to recreate the [[Increase Number]] block.

[[/uploads/Screenshot_20210110-134113_Fancade.jpg]]

We have the increased number, now we have to set that value to the input variable, but how? Using a Set Variable is out of the picture.

Using a Set Reference is another way to set a variable. This time, you can use a Get Variable instead of a Set Variable. You won't often use it since using the Set Variable is more optimal, but it helps with custom script blocks that modify the input variable.

[[/uploads/Screenshot_20210110-135616_Fancade.jpg]]

Note that you have to plug the Set Reference block to input first before any other plug. Otherwise, the Set Reference block won't plug to input at the same spot with the other plug.

[[/uploads/Screenshot_20210110-135813_Fancade.jpg]]