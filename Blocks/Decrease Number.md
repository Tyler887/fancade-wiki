Decreases the input variable by 1.

[[/uploads/Decrease Number.png]]

Inputs:
- Variable: The number variable to decrease by 1

# Notes

Decrease will work with a [[List Element]] input as well!

# Examples

Here's how you might script a simple delay:

[[/uploads/delay.png]]

When the user taps the screen, Num is set to 60. Num is then decreased each frame, and since Fancade runs at 60 FPS it'll reach zero after exactly one second. This triggers the If (remeber that unwired number inputs default to zero) and plays a sound.