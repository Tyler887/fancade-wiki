Makes the constraint springy, like a car's suspension.

[[/uploads/Linearspring.png]]

Inputs:

* Constraint: This script must use the output of an [[add constraint]] script. This can be done directly (connect the two by a wire), or the linear spring script can be connected to a constraint variable or list.
* Stiffness: A vector value. Determines the amount of force that that will be used to "spring" the objects towards their original positions.
* Damping: A vector value. Acts as a kind of "drag" so that objects will not spring continually.

## Notes
Before this script will function as expected, a "[[linear limits]]" constraint must be applied to the same two objects. The linear limits constraint is necessary because it stores the upper and lower limits between which the objects can move. Adding a linear spring script makes the objects "spring" between these upper and lower limits.

## Examples
To find the perfect "stiffness" and "damping" values for your game, try copying the ones below and then adjust them until you get the results you were looking for.

[[/uploads/Linearspringexample.jpg]]