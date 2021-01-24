Ever wondered how Fanscript would look in text format? Well, you can see all references in this directory!

Keep in mind that this is a Work-In-Progress project and that all codes you see will not work if you try to write it in say Unity's C#.

## Examples
Values consist of:

```coffeescript
Number Age = 10
Vector Position = (10, 1.51, 5)
Rotation Angle = {0, 90, 0}
Truth Hit = True
Object Player = MyBlocks.Player
```

For the constraints, it'll be the same inside Fancade:

```coffeescript
PlaySensor() {
    Constraint const = Physics.AddConstraint(base, part, pivot)
    Physics.AngularLimits(const, (0, 0, 1), (0, 0, 0))
    Physics.AngularMotor(const, (0, 0, 90), (0, 0, 100))
}
```

In total we have 7 datatypes that includes lists.

Talking about lists here is how you do them in text format:

```coffeescript
# set a list variable
List<Vector>[0] Positions = (32.1, 5.51, -23.72)

# to access a list
Number.Inspect(List<Number>[2])
```

Here is [[Martin Magni]]'s Shepherd game [[script | Shepherd]] turned into Fanscript.

# Links
- [[Fanscript/Syntax.md | Syntax]]
- [[Fanscript/Datatypes.md | Datatypes]]