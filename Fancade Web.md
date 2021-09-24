Fancade is also available as a web app! Go to [[play.fancade.com|https://play.fancade.com]] to play Fancade in a browser!

[[_TOC_]]

## Linking to Games

A link to a published game can be generated in the web app (and also in the regular app after version 1.7 is released) by clicking the 'Share' button for that game.

Links to games have the following format: [[https://play.fancade.com/5F084A0BCE06B710]]
where '5F084A0BCE06B710' is the game's unique identifier.

The web app will load the linked game and directly start the first level.

## Setting Start Level of Linked Games

The starting level of a linked game can be set by appending the level index to the end like this: [[https://play.fancade.com/5F084A0BCE06B710/8]]
The `/8` part (after the game's unique identifier) sets the start level to 8, in this case.


## Differences Compared to App

There are some differences between the web app and the regular app. Here is a summary:
* Highscores, like/play counters use a separate system (we plan to merge these later)
* All in-app purchases are disabled
* Payouts are disabled
* The 'New' category is disabled
* Need to log in to Fancade account to play challenges
* Linked games start directly
* Additional controls for mouse and keyboard (see below for a complete list)
* Auto-save in edit mode
* Dev pause mode with single-frame step
* Can download games in 'Projects' to local file system
* Can drag-and-drop files from local file system into web app. The game ends up in 'Projects'


## Performance and Compatibility

If the game seems to run slow, check if hardware acceleration is enabled in your browser.

If the game doesn't run at all, there are usually some helpful messages shown (hopefully on screen but also in the web developer console). Fancade web has been tested and confirmed to work in Chrome, Firefox, Safari and Edge, but there can be issues with video drivers etc. that'll prevent it from running. You can also try to disable hardware acceleration, but then the game will run much slower.

## Additional Controls

The web app has additonal controls for mouse and keyboard.

In the info below, CMD and CTRL on macOS are treated as the same button.

### Edit Mode

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
| Q key + LMB Drag | Paint with the current selection. Uses mouse normal to limit the paint plane. | Need to hold down Q while painting. CTRL limits to y-plane, Shift limits to z-plane, ALT limits to x-plane, ALT + Shift limits to the line the mouse normal points towards |
| CTRL + S key | Save game in the browser's local storage | This is not a normal file in the filesystem. Local storage can easily be cleared, so it is recommended to download the game as a local file regularly using CTRL + Shift + S |
| CTRL + Shift + S key | Save the game as a local file | Such local files can later be dragged and dropped over the browser window to restore a lost game file or for collaboration projects |
| CTRL + Z key | Undo | |
| CTRL + Shift + Z key | Redo | |
| Escape key | Go back or Close | |


### Play Mode

| Input | Description | Other |
| ----- |-------------| ----- |
| Arrow keys | Generate directional swipes with minor offset along secondary direction + Generating fake accelerometer inputs | Shift and Alt modifies the distance. Special cases when detecting the Virtual Gamepad or Neo Joystick |
| WASD | Same as arrow keys but with opposite minor offset along secondary direction | Shift and ALT modifies the distance |
| Keypad keys | Same as arrow keys but no secondary direction offsets | Shift and ALT modifies the distance |
| TFGH | Fake accelerometer | Shift and ALT modifies the angle amount, CTRL adds white noise to the output |
| IJKL | Tap like it was an on-screen control in left-right-back-forward | |
| Space key OR Keypad 5 | Tap middle | |
| Z key | Tap left middle | |
| X key | Tap right middle | |
| Escape key | Tap top left | |
| Enter key | Tap top right | |
| P key | Pause / Resume | |
| Mouse + RMB | Pan with fake gesture | |
| Mouse scroll wheel OR ? and ´ keys OR Keypad +/- (the two buttons at the right of 0) | Zoom with fake gesture | Shift and ALT modifies speed |
| Mouse + MMB | Orbit with fake gesture | |
| Mouse + MMB + CTRL | Pitch with fake gesture | |
| CTRL + R key | Restart | Also works in the pause menu |
| CTRL + P key | Enters "dev pause mode" where the game is paused without the pause UI showing | |
| Shift + P key | Steps a single frame forward in "dev pause mode" | Only works in edit mode |

### Menus

| Input | Description | Other  |
| ----- |-------------| ----- |
| Mouse scroll wheel OR Up and down arrow keys | Scroll up and down | |
| Left and right arrow keys | Switches tab in main menu | |
| Enter key | Tap the "focus" button | |
| Escape key | Close or back | |
| CTRL + Q | Eject / Exit game in pause menu | |

### Top Menu

| CTRL + S key | Save the selected game as a local file | Only works in "Projects" or if the current logged-in user is the author of the game |
| Files dropped onto window | Create a new game in "Projects" for each file | Only works in the top menu. Doesn't work if the file exists or if the current logged-in user is not the author of that game (and the game is not editable). This can be used for turn-based collaboration. |

### Misc

| Input | Description | Other  |
| ----- |-------------| ----- |
| F1 | Contextual help | Open a wiki help page in a new tab. Selecting or hovering over (in the inventory) a stock prefab opens up the wiki page for that prefab. |

## Collaboration with Export/Import

It is possible to collaborate on a project by using the following procedure:
* Press CTRL + S in the game's menu to download a game from 'Projects' to the computer's local filesystem
* Send the file to the person you collaborate with
* That person then drags and drops the file into the browser window running the Fancade web app (only works in the top menu)
* The game will end up in 'Projects' and can be further edited and then exported with CTRL + S and sent back

NOTE: When importing a game with drag-and-drop, that game must first be removed.

NOTE: The first user who publish the game is the only one who can later update it.

## Size Parameters

The size of the web app canvas can be controlled with parameters.

This is useful when checking if a game works well on different screen sizes and orientations.

| Parameter | Description | Other |
| --------- | ----------- | ----- |
| max_w | Maximum width of the canvas | Default value is 1024 |
| max_h | Maximum height of the canvas | Default value is 768 |
| ar_w | Aspect ratio width | In a 4/3 aspect ratio, this parameter should be 3. If any of the ar_w or ar_h is set, the aspect ratio is forced and limited by the max_w and max_h parameters |
| ar_h | Aspect ratio height | In a 4/3 aspect ratio, this parameter should be 4. If any of the ar_w or ar_h is set, the aspect ratio is forced and limited by the max_w and max_h parameters |

The size of the canvas is never greater than the browser window's inner size. 

If any of the aspect ratio parameters are set, the aspect ratio is enforced. 

The width and height of the canvas is always maximized given the constraints from max_w, max_h, ar_w and ar_h.

Some examples of how to use the parameters:

| Link | Description |
| ---- | ----------- |
| <https://play.fancade.com?ar_w=16&ar_h=9> | Forces aspect ratio to 16/9 and maximizes the size |
| <https://play.fancade.com?ar_w=9&ar_h=16&max_h=800> | Forces aspect ratio to 9/16 and restricts the height to max 800 |

