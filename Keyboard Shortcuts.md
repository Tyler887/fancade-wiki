# Desktop controls

On macOS, CMD and CTRL are treated as the same button.

## Edit Mode

| Input | Description | Other |
| ----- |-------------| ----- |
| Mouse + RMB OR Arrow keys OR WASD keys OR Keypad | Pan | Shift pans slower. Pan is default in xz-plane only but using ALT unlocks free pan like in the app |
| Mouse scroll wheel OR Keypad +/- OR  ? and ´ keys (the two buttons at the right of 0) | Zoom | Shift and CTRL modifies speed |
| Mouse + MMB OR O key OR R key | Orbit | Shift orbits slower, CTRL snaps angle, ALT snaps angle to topdown view |
| LMB + CTRL | Toggle selection of mouse-hovered block | |
| LMB + CTRL + Mouse move | Rectangle select adds to current selection | |
| Backspace OR Delete | Remove block | Removes selected blocks first. If no blocks are selected, it removes the block that the mouse hovers over. Holding down Shift continuously removes all blocks that the mouse hovers over. |
| E key | Open / Close block | |
| T key | Open / Close block for painting | |
| I key | Open / Close inventory | |
| F key | Focus on selected / Auto-fit camera | Auto-fits camera if no blocks are selected |
| G key | Camera pitch snap | Same as tapping on the camera button |
| Shift + F key | Fill block with current paint | Only available in paint block mode |
| CTRL + C key | Copy blocks | |
| CTRL + V key | Paste blocks | |
| CTRL + X key | Cut blocks | |
| CTRL + S key | Save level | |
| CTRL + Z key | Undo | |
| CTRL + Shift + Z key | Redo | |
| Escape key | Go back or Close | |


## Play Mode

| Input | Description | Other |
| ----- |-------------| ----- |
| Arrow keys | Generate directional swipes with minor offset along seconary direction + Generating fake accelerometer inputs | Shift and CTRL modifies the distance. Special cases when detecting the Virtual Gamepad or Neo Joystick (does not support buttons or dual sticks mode yet) |
| WASD | Same as arrow keys but with opposite minor offset along secondary direction | Shift and CTRL modifies the distance |
| Keypad keys | Same as arrow keys but no secondary direction offsets | Shift and CTRL modifies the distance |
| TFGH | Fake accelerometer | Shift and CTRL modifies the angle amount, ALT adds white noise to the output |
| IJKL | Tap like it was an on-screen control in left-right-back-forward | |
| Space key OR Keypad 5 | Tap middle | |
| Z key | Tap left middle | |
| X key | Tap right middle | |
| Escape key | Tap top left | |
| Enter key | Tap top right | |
| P key | Pause / Resume | |
| Mouse + RMB | Pan with fake gesture | |
| Mouse scroll wheel OR ? and ´ keys OR Keypad +/- (the two buttons at the right of 0) | Zoom with fake gesture | Shift and CTRL modifies speed |
| Mouse + MMB | Orbit with fake gesture | |
| Mouse + MMB + CTRL | Pitch with fake gesture | |
| CTRL + R key | Restart | Also works in the pause menu |
| CTRL + P key | Enters "dev pause mode" where the game is paused without the pause UI showing | |
| SHIFT + P key | Steps a single frame forward in "dev pause mode" | Only works in edit mode |


## Menus

| Input | Description | Other  |
| ----- |-------------| ----- |
| Mouse scroll wheel OR Up and down arrow keys | Scroll up and down | |
| Left and right arrow keys | Switches tab in main menu | |
| Enter key | Tap the "focus" button | |
| Escape key | Close or back | |
| CTRL + Q | Eject / Exit game in pause menu | |

## Top Menu

| CTRL + S key | Save the selected game as a local file | Only works in "Projects" |
| Files dropped onto window | Create a new game in "Projects" for each file | Only works in the top menu |


## Misc

| Input | Description | Other  |
| ----- |-------------| ----- |
| F1 | Contextual help | Open a wiki help page in a new tab. Selecting or hovering over (in the inventory) a stock prefab opens up the wiki page for that prefab. |


## Parameters

| Parameter | Description | Other |
| --------- | ----------- | ----- |
| max_w | Maximum width of the canvas | Default value is 1024 |
| max_h | Maximum height of the canvas | Default value is 768 |
| ar_w | Aspect ratio width | In a 4/3 aspect ratio, this parameter should be 3. If any of the ar_w or ar_h is set, the aspect ratio is forced and limited by the max_w and max_h parameters |
| ar_h | Aspect ratio height | In a 4/3 aspect ratio, this parameter should be 4. If any of the ar_w or ar_h is set, the aspect ratio is forced and limited by the max_w and max_h parameters |
