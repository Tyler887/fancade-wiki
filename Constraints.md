Constraints Explained:

Use this to create a physics constraint between 2 objects. The 'Base' will not have physics enable unless it is enabled in script somewhere else or it is a physics block. The part will have physics enabled on it when the constraint is created. The pivot point is the position where the constraint connects the two objects. By default, if you leave it blank, the pivot will be set to the position of the 'part' object. By default, physics constraints have linear and angular limits locked.

#Types
There are different types of constraints. There is angular motor, which makes the part rotate around the base. Linear motor makes the part move in the given direction. Angular spring is like angular motor, but it bounces if it hits something. Linear spring is like linear motor, but more bouncy.