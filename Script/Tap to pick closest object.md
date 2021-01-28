Lots of games involve tapping tiny objects on screen. But phones are small, fingers are fat, and people's patience is limited. So many games are *more fun* if they're *kind* to the player. If they hastily tapped in the general vicinity, but missed by a pixel? Give them a break and pretend they hit perfectly!

Here's my favorite way to turn that kindness into script:

[[/uploads/pick_closest.png]]

First, the three tappable Wood blocks add themselves to a list `$Bs`. (Short for BlockS!) Then the [[Touch Sensor]] feeds into [[Line vs Plane]] to compute the world coordinate the player tapped. The [[Loop]] then checks the distance to *all* blocks, and keeps track of the *best* pick. Finally, do whatever you wanted to do with the tapped object, e.g. [[Set Position]] moves it to the tap position.

In this example `Best` is initialized to `3`, so even if the tap misses by a large margin, it'll still count as a hit! And if multiple objects are within that distance, it'll still pick the *best* hit.