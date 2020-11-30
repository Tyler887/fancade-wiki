
This is a Tutorial about the advanced tricks of Pivot Kit. Don't know what that is? [[Check this out|https://fancade.page.link/Rntz]]
[[https://imgur.com/6fPf0qF.jpg]]

At the start of the level we are moving the 7 voxels height block beneath the starting platform at very high speed *(In one frame)* to hide it from the player.
The small value along negative Y-axis is used to prevent some clipping flashes *(set that to 0 to see what I'm talking about)*
[[https://imgur.com/UsqZ4Kk.jpg]]

After that, whenever the user presses a switch, the output of that is processed by **Switch to Move**.
As long as the ID section of **Add Movement** is connected with the proper ID, it'll know which blocks to move. It just gets activated by the **Switch to Move** Script.
[[https://imgur.com/gym2BJo.jpg]]

These are some of the useful global variables in **Pivot**.

* **$You**  (Vector) contains the current position of BlueCube.
* **$KGot** (Number) contains the amount of keys collected.
* **$T** (Number) contains the amount of frames passed from the start.

In the third part we are checking if BlueCube is in the proper position, and if it is we change the camera zoom and make a staircase.
This part shows that you are *not always stuck to switches for doing something!*
[[https://imgur.com/mr7fD6G.jpg]]

Code for nothing: E441297

At last we have connected the After wire of one set of **Add Movement** block to another set's before part.
As I said before, as long as **Add Movement** gets the proper ID it can be activated by either the **Switch to Move** block or After wire of another **Add Movement** block.
Here it gets activated by another Script to have a good *Staircase Building* effect.
[[https://imgur.com/Pe3UdWH.jpg]]