In Fancade we have a total of 7 datatypes. These datatypes are Number, Vector, Rotation, Truth, Object, Constraint, and List.

The `Number`type can be either a whole number or in decimals, in the programming world we call these "int" and "float/double".

Here are some examples:
```coffeescript
Number jumpSpeed = 0.2
Vector level = (1, 1, -10)
Rotation fan = {0.1, 0, 0}
Truth blocked = False
Object me = MyBlocks.Me
```

For the constraint, here is how you do it:
```coffeescript
PlaySensor() {
    Constraint const = Physics.AddConstraint(base, part, pivot)
    Physics.AngularLimits(const, (0, 0, 1), (0, 0, 0))
    Physics.AngularMotor(const, (0, 0, 90), (0, 0, 100))
}
```
To create variables simply type:
`Datatype variableName`

And to initialize:
`Datatype variableName = value`

For the lists here is an example:
```coffeescript
PlaySensor() {
    Object landmine = MyBlocks.LM
    List<Object>[Number $LM] $LM = landmine
    List<Vector>[Number $LM] $LM = Objects.GetPosition(landmine)
    Number $LM++
}
```

To access values inside a list:
```coffeescript
Loop(0, $landmines) {
Number I = this.currentIndex
Vector landminePositions = List<Vector>[Number I] $LM
}
```

