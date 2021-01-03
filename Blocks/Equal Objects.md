Outputs True if the two input objects are equal. Since object inputs default to None, just leave the second input empty to check if the first input is None.

[[/uploads/Equal_Object.png]]

## Notes

* This checks if the two inputs are the same *[[object]]*, not whether they're the same *[[block]] type*. E.g. two [[Box]] blocks, placed in the world, will create two different and independently moving objects, so they are not equal despite both being made from the same block type.