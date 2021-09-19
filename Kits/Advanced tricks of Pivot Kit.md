This is a Tutorial about the advanced tricks of Pivot Kit. Don't know what that is? [[Check this out|https://fancade.page.link/Rntz]]
[[/uploads/6fPf0qF.png]]

At the start of the level we are moving the 7 voxels height block beneath the starting platform at very high speed (in one frame) to hide it from the player. The small value along negative Y-axis is used to prevent some clipping flashes (set that to 0 to see what ViChyavIn is talking about).

[[/uploads/UsqZ4Kk.png]]

After that, whenever the user presses a switch, the output of that is processed by **Switch to Move**.
As long as the ID section of **Add Movement** is connected with the proper ID, it'll know which blocks to move. It just gets activated by the **Switch to Move** Script.
[[/uploads/gym2BJo.png]]

These are some of the useful global variables in **Pivot**.

* **$You**  (Vector) contains the current position of BlueCube.
* **$KGot** (Number) contains the amount of keys that BlueCube has collected.
* **$T** (Number) contains the amount of [[frames|Current Frame]] passed from the start.

In the third part we are checking if BlueCube is in the proper position, and if it is we change the camera zoom and make a staircase.
This part shows that you are not always stuck to switches for doing something!
[[/uploads/mr7fD6G.png]]

At last we have connected the After wire of one set of a **Add Movement** block to another set's before part.
As I said before, as long as **Add Movement** gets the proper ID it can be activated by either the **Switch to Move** block or After wire of another **Add Movement** block.
Here it gets activated by another Script to have a good *Staircase Building* effect.
[[/uploads/Pe3UdWH.png]]