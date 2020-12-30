So you have a physics object, and a script that suddenly removes the floor it's resting on, yet it doesn't fall down? Likely your object fell asleep!

Wait, what? Yes, physics objects fall asleep quite frequently. Simulating physics requires a lot of CPU, so the physics engine puts objects that haven't moved in a few seconds to sleep. Sleeping objects use up very little CPU, and if something happens to them, they'll automatically wake up and react realistically.

But in some cases you might want to do something sudden and unrealistic, like instantly removing the floor, and this won't wake the object up. So you'll need to manually wake it up by doing *something* physical to it. E.g. Add Force with a 0,0,0 force will wake the object, yet not actually push it anywhere.

For *some* games it's best to keep all objects awake all the time. This can be done by subtly changing Set Gravity each frame, which will wake everything up. [[Gobble]] does this, because the hole moves without physics, yet all objects need to fall into it all the time. Use this method only when needed, as it'll make all objects consume physics-simulation CPU all the time.