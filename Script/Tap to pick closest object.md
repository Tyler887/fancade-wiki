So many games involve tapping very small objects on the screen. But phones are small, fingers are big, and people's patience is limited. So many games are *so much **fun*** if they're *kind* to the player. If they hastily tapped in the general vicinity, but missed by a pixel? Give them a break and pretend they hit perfectly!

Here's Martin's favorite way to turn that kindness into script:

[[/uploads/pick_closest.png]]

First, the three tappable wood blocks add themselves to a list named `$Bs`. (Short for BlockS.) Then our [[Touch Sensor]] feeds into [[Line vs Plane]] to compute the world coordinate the player tapped. Our [[loop]] then checks the distance between our finger and the position of *all* blocks in the list, and keeps track of the *best* pick. Finally, do whatever you want with the tapped object, e.g. [[Set Position]] moves it to the tap position.

In this example `Best` is initialized to `3`, so even if the tap misses by a large margin, it'll still count as a hit! And if multiple objects are within that distance, it'll still pick the *best* hit.