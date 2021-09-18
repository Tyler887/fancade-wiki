[Hexalink](https://fancade.page.link/RkHU) is a game by LukaszM where you have to make a single loop that satisfies all the buildings to win

## How to play
Tap an edge to place a line, tap the edge again to remove it, the buildings (or the number above it) indicates how many lines are boardering the cell, buildings can only be satisfied if the boardering lines matches the number of the building type. You win if all conditions are met:

* The line makes a single loop
* The line never makes a 3 way branch
* There is no isolated lines in the level
* All buildings are satisfied

## Basic Logic
Some of these logic will be modified versions of original [slitherlink](https://www.conceptispuzzles.com/index.aspx?uri=puzzle/slitherlink/techniques) logic, so check those out before looking at hexalink logic.

* If a line has only one path to take, extend that line with that 1 path.
* If theres an explicit path that leads to a dead end if you take the path, that path has no lines.
* A 0 always doesn't have a line.
* A 1 clue adjacent to at least 2 consecutive empties doesn't have a line on the edges boardering the 2 consecutive empties, since if one is filled, the loop cant end and has to extend, breaking the 1 clue, same for 2 clue adjacent to 3 consecutive empties.
* A 5 clue adjacent to at least 2 consecutive empties must have a line on the edges boardering the consecutive empties, since if one is empty, the other one is empty and it will break the 5 clue, same for the 4 clue adjacent to at least 3 consecutive empties.
* 2 5 clues at least adjacent to each other and has other non-0 clues in the grid must form the modified classic pattern because you need to place the line in the middle first because it makes a closed link if not, then if the 3 lines of the top and bottom are not given, then one of the 5 clues will fail.
* A line that is directly pointing to the 5 will tell that the edges adjacent to that 5 and not connect the line are all lines, because if its not met, there will be branching lines.
* A 2, 3, or 4 clue can have lines separated from each other, keep in mind.
* Anytime you see the 6 clue (office), its just a 1 cell loop surrounding the loop. (Assuming the puzzle isn't impossible)

## Solutions 
Each photo shows 10 solutions to the puzzle, click to zoom those puzzles

Levels 1-10

Levels 11-20

Levels 21-30

Levels 31-40