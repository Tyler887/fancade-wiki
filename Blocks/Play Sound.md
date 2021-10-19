Plays a sound effect with optional volume and pitch inputs and outputs the channel the sound is played on. Use the settings to change which sound effect is played.

[[/uploads/Play_Sound.png | width=336px]]

## Input/Output

Unlike most other blocks, a wire connected to Before is *required* for it do do anything, it does not run automatically.

| Wire       | Range | Note |
|----------- |:-----:|:-----|
| Volume     | 0 to 1  | 
| Pitch      | 0 to 4  | 
| *Channel*  | -1 to 9 | Only -1 when channels 0 to 9 are occupied or plays too many looped sounds. If so, the sound will fail to play.

## Settings

[[/uploads/Playsound_contextmenu.png]]

The rightmost setting displays which sound effect is played. Tap to change.

Checking Loop will make the sound repeat on the chosen channel until stopped with [[Stop Sound]]. A looping channel becomes occupied until it is stopped, meaning other Play Sound blocks will not choose that channel. 

