Here is [[Martin Magni]]'s game in text format.

```coffeescript
# Init
Object $Herder = MyBlocks.Herder
Object Sheep = MyBlocks.Sheep

# Sheep script
TouchSensor("First").touching {
    Physics.AddForce(Sheep, Math.LineVsPlane(Math.ScreenToWorld(this.screenX, this.screenY), (0, 2, 0), (0, 2, 0)) - Objects.GetPosition(Sheep))
}

Number $Dist = Math.Max(Math.Distance(Objects.GetPosition(Sheep), Objects.GetPosition($Herder)), $Dist)

Collision(Sheep) {
    If (this.secondObject == None) {
        Game.Lose(False)
    }
}

# Herder script
If (Number $Dist < 2) {
    Game.Win(False)
}
Number $Dist = 0


```