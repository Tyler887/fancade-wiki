This page is collection of information regarding of Text Scripts/Scripting (Including : Fancade's Possible Inner Codes & How they work and Fancade's Text Format for a quick Information Sharing during discussions about scripting in Fancade).

[[_TOC_]]

# Fancade Coding Text Format

A Pseudo-Coding Language Format made in contribution of  (**@Isaglish** , **@JP16D** , **@Qma** and **@Vex Ave**) base from Fancade's Coding. 

(*Note: this is not a real or existent coding language as the word "Pseudo" declares this is just a code format that can be used in scripting discussions)


This Format will be a basis when sharing or suggesting some codes and code solutions during script discussions. Take this as an easier way to share or suggest a code program instead doing it in fancade and go back to fancade server #scripting channel. Well in case of people that couldn't understand this ... Sorry we can't do anything about it :P so just do the thing in fancade , screenshot it and share it to them.


### Introduction
This format is based on C# syntax. Most of things are simplified for the better understanding.

As you know , Fancade's script blocks are located in different folders. To make it easier to understand , what it means , use their names as in the example below. It's not necessary and takes such a time to write , but please pay attention to it when you're explaining script to the new user or there are namesake custom blocks.

Following the C# syntax , let's imagine that each folder is a separate class with its own fields and functions. So , to represent Get Frame block , you need to type `Game.Current_Frame`. Again , it's not necessary , just `Current_Frame` is fine too.

All the cases:
```
//If block has yellow wires, add () at the end of the name
Game.Win();
Sound.Play_Sound();

//If block has inputs, count them and their type in the brackets
Objects.Set_Position(obj object, vec position, rot rotation);

//If block has more than one output you will need to define them individually 
//Use '.outputname' after the function to define them
Objects.Get_Position(target_object).position;

//Math block counts like this, except the basic ones listed below
vec result = Math.Line_vs_Plane(L_from, L_to, P_normal, P_point);

//If block has only outputs, don't do anything
num frame = Game.Get_Frame;
```

**____________________________________**
### Basics
**______________**

#### Value Types 
```
num varName = 0;
tru varName = true/false;
vec varName(x , y , z);
rot varName(x , y , z);
obj varName = Object; 

//Any variable can be used as list. Format: varName[index]


//Define wire value
wire_wireName = value;
```
**______________**

#### Basic Math Operators

```
//Add Numbers
2 + 2

//Subtract Numbers
2 - 2

//Multiply Numbers
2 * 2

//Divide Numbers
2 / 2

//Power
2 ^ 2

//Modulo
2 % 2

//Increase
num++

//Decrease
num--
```
**______________**

#### Basic Boolean Operators
```
//Boolean logic (AND, OR, NOT)

tru smart = ((NOT dumb) AND (has_brain)) OR already_smart;

//Math (Greater, Less, Equal)

tru equal = a == b;

tru greater = a > b;

tru less = a < b;
```

**____________________________________**

### Game
```
Game.Win();

Game.Lose();

Game.Set_Score(num Score);

Game.Set_Camera(vec Position, rot Rotation, num Distance);

Game.Set_Light(vec Position, rot Rotation);

Game.Screen_Size.x
Game.Screen_Size.y

Game.Accelerometer

Game.Current_Frame
```

**____________________________________**

### Objects
```
Objects.Get_Position(obj).Position
Objects.Get_Position(obj).Rotation

Objects.Set_Position(obj Object, vec position, rot Rotation);

//alternative
//get
vec = obj.position;
//set
obj.position = vec;

Objects.Raycast(vec, vec).Hit?
Objects.Raycast(vec, vec).Hit_Pos
Objects.Raycast(vec, vec).Hit_Obj

Objects.Get_Size(obj Object).Min
Objects.Get_Size(obj Object).Max

//alternative
vec = obj.size.min;

Objects.Create_Object(obj Object);

Objects.Destroy_Object(obj Object);
```

**____________________________________**

### Sound
```
Sound.Play_Sound(num Volume, num Pitch);
Sound.Play_Sound.Channel

Sound.Stop_Channel(num Channel);

Sound.Volume_Pitch(num Channel, num Volume, num Pitch);
```

**____________________________________**

### Physics
```
//I regret doing this, sorry
```


**____________________________________**

### Control
```
//Basic if operator
If (condition) { 
    function_true;
} else { 
    function_false;
}

//Or ternary
condition ? true : false; 
//Note: Fancade doesn't have ternary operator at the moment of writing. This is just a shortcut for scripting discussions

Loop(num start = 0, num end = 0) {
    //Output
    self.Counter
}

Touch_Sensor() { 
    //Outputs
    self.Screen_X
    self.Screen_Y
}

Collision(obj Physical_Object) {
    //Outputs
    self.Second_Object
    self.Normal
    self.Impulse
}

Swipe_Sensor() {
    //Output
    self.Direction
}

BoxArt() {
}

PlaySensor() {
}

LateUpdate() {
}
```

**____________________________________**

### Math
```
Math.Negate(num Num)

Math.Inverse(rot Rot)

vec.Scale(num Num)

vec.Rotate(rot Rot)

rot.Combine(rot Rot2)

Math.Random(num Min = 0, num Max = 1)

Math.Random_Seed(num Seed);

Math.Min(num Num1, num Num2)

Math.Max(num Num1, num Num2)

Math.Sin(num Num)

Math.Cos(num Num)

Math.Round(num Num)

Math.Floor(num Num)

Math.Ceiling(num Num)

Math.Absolute(num Num)

Math.Logarithm(num Number, num Base)

num vec.x
num vec.y
num vec.z

vec.Normalize()

vec.Dot(vec Vector)

vec.Cross(vec Vector)

num rot.x
num rot.y
num rot.z

Math.Distance(vec Vec1, vec Vec2)

LERP(rot From, rot To, num Amount)

Math.Axis_Angle(vec Axis, num Angle)

Math.Screen_To_World(num Screen_X, num Screen_Y)

Math.World_To_Screen(vec World_Pos)

Math.Line_vs_Plane(vec Line_From, vec Line_To, vec Plane_Point, vec Plane_Normal)

Math.Look_Rotation(vec Direction, vec Up)
```

# Syntax

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

## Datatypes

In Fancade we have a total of 7 datatypes. These datatypes are Number, Vector, Rotation, Truth, Object, Constraint, and List.

The number type can be either a whole number or in decimals, in the programming world we call these "int" and "float/double".

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

### Example

Here is [[Martin Magni]]'s Shepherd game in text format.

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