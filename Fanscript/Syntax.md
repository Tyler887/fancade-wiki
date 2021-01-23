Ever wondered how Fanscript would look in text format? Well, you can see them all in the /Fanscript directory.

## Examples
Values consist of:

```
Number Age = 10
Vector Position = (10, 1.51, 5)
Rotation Angle = (0, 90, 0)
Truth Hit = True
Object Player = MyBlocks.Player
```

For the constraints, it'll be the same inside Fancade:

```
PlaySensor() {
    Constraint const = Physics.AddConstraint(base, part, pivot)
    Physics.AngularLimits(const, (0, 0, 1), (0, 0, 0))
    Physics.AngularMotor(const, (0, 0, 90), (0, 0, 100))
}
```
