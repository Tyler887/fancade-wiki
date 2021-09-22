Script blocks are executed top-to-bottom, left-to-right, [by default](Execution order). When you need more control over the order, connect them with yellow wires. Here are some examples where it's easy to forget that the default order may not be what you want:

### Example 1
This one is common among newbies. In this case, the problem is easy to spot. The variable **A is defined AFTER the Set Position** that has A as an input. Since A is not yet defined when Set Position was run, it simply does nothing resulting in a buggy script.
[[/uploads/NZgn9C7.jpeg]]
A simple solution for this is to **define A before the Set Position**.
[[/uploads/4KJxQG5.jpeg]]

### Example 2
Create Object is one of those scripts that has **an output AND execute wires** attached to it. If a scripts has both, output and execute wires, it's usually a good idea to set those outputs into a variable using the After Wire. Else, you'll suffer from an **One Frame Delay**.
[[/uploads/7xNbBVB.jpeg]]
The script shown above will suffer from that One Frame delay, since each frame the object that gets created is set onto the variable A **after** the set position has run. A simple fix would be, is to set the variable via the After Wire.
[[/uploads/4iUV6ZV.jpeg]]