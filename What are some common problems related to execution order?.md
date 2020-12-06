[[Execution order]] is a boon and a curse at the same time. While it helps determining what to execute, sometimes the default Execution Order doesn't actually do what you want. Thankfully, you can easily fix that using Execution Wires.

Here are two common problems related to execution order.

1. This one is common among newbies. In this case, the problem is easy to spot. The variable **A is defined AFTER the Set Position** that has A as an input. Since A is not yet defined when Set Position was run, it simply does nothing resulting in a buggy script.
[[https://imgur.com/NZgn9C7.jpg]]
A simple solution for this is to **define A before the Set Position**.
[[https://imgur.com/4KJxQG5.jpg]]

2. Create Object is one of those scripts that has **an output AND execute wires** attached to it. If a scripts has both, output and execute wires, it's usually a good idea to set those outputs into a variable using the After Wire. Else, you'll suffer from an **One Frame Delay**.
[[https://imgur.com/7xNbBVB.jpg]]
The script shown above will suffer from that One Frame delay, since each frame the object that gets created is set onto the variable A **after** the set position has run. A simple fix would be, is to set the variable via the After Wire.
[[https://imgur.com/4iUV6ZV.jpg]]