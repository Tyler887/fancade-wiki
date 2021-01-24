A Pseudo-Coding Language Format Developed by (@Isaglish , me @JP16D , @Qma and @Vex Ave) base from Fancade's Coding. 

Here is what we have done so far ...

### Basics

 **Value Types** :
```
• Num varName = 0 ; //NaN ~ Integers ~ Inf
• Tru varName = 0 ; //boolean either 0 or 1 only
• Vec varName[x , y , z] ;
• Rot varName[x , y , z] ;
• Obj varName = Obj ; 
```

Basic Math Operators

- Add - (+)
- Subtract - (-)
- Divide - (/ or ÷)
- Multiply - (* or ×)
- Power - (^)
- Modulo - (%)






Control

***if***
```
• If (condition) { function } else { function } ;
```
 **or**
```
• condition ? function : function ; /* This a secondary method of conditional if in JS language Idk if there are other languages using this method of conditional if */
```






***Loop***
```
• Loop[ start , end ]( ) 
{ function ; return ( counter ) ; } ;
```
**or**
```
• Num start = 0 ;
  While (start < end) { start++ , function } ; 
  /*this is loop in a nutshell :D , joke this is the manual loop*/
```
Touch Sensor
• Touch[ mode , touch ]( ) 
{ function ; return ( x , y ) ; } ;

Collision
• Collide[ Obj ]( )
{ function ; return ( Impulse , Normal , Hit Obj ) ; } ;

Swipe
• Swipe( ) { function ; return ( x , y , z ) ; } ;

Box Art 
• BoxArt( ) { function } ;

Play Sensor
• PlaySensor( ) { function } ;

Late Update
• LateUpdate( ) { function } ;

Basic Boolean Operators
>
Greater Than
<
Less Than
==
Equal
&&
AND
||
OR
!
Not

Object

Set Position
• SetPos( Obj , Position[ ] , Rotation[ ] ) ;

Raycast
• Raycast( From[ ] , To[ ] )
 { return ( Hit , Hit Pos[ ] , Hit Obj ) ; } ;

Get Position
• GetPos( ) { return ( Position[ ] , Rotation[ ] ) ; } ;

Get Size
• GetSize( ) { return ( max size[ ] , min size[ ] ) ; } ;


Create Object
• Object.Create( Obj ) ;

Destroy Object
• Object.Destroy( Obj ) ;

Set Visible
• Object.Visible( Obj , Visible ) ;







Advanced

List Set Element
• Num varName[ index ] = 0 ;
• Vec varName[ index ] = [ x , y , z ] ;
List Get Element
• varName[ index ] 
• varName[ [ x , y , z [ index ] ]

Advanced Math Functions

Scale & Rotate
•  Vec[ ] * Num 
• Math.Rotate[ Vec[ ] * Rot[ ] ]


Break and Create Vec/Rot
• Math.Break[ Vec[ ] ]
or
• vec[ x ] , vec[ y ] , vec[ z ]
• Math.Create[ NumX , NumY , NumZ ]

Dot & Cross Product
• Vec[ ] ° Vec[ ] // Dot Product
• Vec[ ] • Vec[ ] // Cross Product

Min & Max
• Math.Min[ a , b ]
• Math.Max[ a , b ]



Round , Floor & Ceil
• Math.Round[ Num ]
• Math.Floor[ Num ]
• Math.Ceil[ Num ]

Sin & Cos
• Math.Sine[ Num ]
• Math.Cos[ Num ]

Distance
• Math.Distance[ VecA[ ] , VecN[ ] ]

LERP
• Math.LERP[ From , To , Amount ]
