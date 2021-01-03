Outputs True if the two input objects are equal. Since object inputs default to None, just leave the second input empty to check if the first input is None.

[[/uploads/Equal_Object.png]]

Note that it doesn't count as equal even if the two blocks are the same type. It's  because each block has a unique ID (can be checked with Inspect Object). Glued blocks will count as a single object (with one object ID).