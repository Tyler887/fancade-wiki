[Hexalink](https://play.fancade.com/60D8A2D86F631309) is a game by LukaszM. It is a hexagonal variant of [[Link]] by nmskr.

## How to Play

Tap on an edge to place a line, tap the edge again to remove it. Tap with 2 fingers to enable/disable numbers. Buildings (numbers) indicate how many lines surround the cell. You win if all conditions are met:

* The line makes a single loop
* The line never makes a 3 way branch
* There are no isolated lines in the level
* All buildings are satisfied

## Basic Logic

Some of these logic will be modified versions of original [Slitherlink](https://www.conceptispuzzles.com/index.aspx?uri=puzzle/slitherlink/techniques) logic, so check those out before looking at hexalink logic.

Note: images are edited such that visualizations of cross marks are added to make it easier to see.

When finding new logic, visualizing combinations and if an edge is empty or not. Here are a couple of patterns:

* If a line has only one path to take, extend that line with that 1 path:
  [[/uploads/hexalink-1.png]]
* If there is an explicit path that leads to a dead end if you take the path, that path has no lines:
  [[/uploads/hexalink-2.png]]
* A 0 (tree) always doesn't have lines surrounding it:
  [[/uploads/hexalink-tips-3a.png]]
  As a result, more cross marks can be visualized:
  [[/uploads/hexalink-tips-3b.png]]
* A 1 (pool) clue with its edges consecutively touching the border at least 2 times doesn't have a line on the borders, since if one is filled, the loop is forced to extend, breaking the 1 clue:
  [[/uploads/hexalink-tips-d1.png]]
  Same for 2 (factory) clue consecutively touching the border at least 3 times:
  [[/uploads/hexalink-tips-d2.png]]

* The inverse applies. A 5 (tower) clue touching the border at least 2 times in a row must have a line on the borders, since if one is empty, the other one is empty and it will break the 5 clue:
  [[/uploads/hexalink-tips-e1.png]]
  Same for the 4 (hotel) clue touching the border at least 3 times in a row:
  [[/uploads/hexalink-tips-e2.png]]
  
* Two 5 clues adjacent to each other only has two combinations. Only keeping the common lines gives this pattern:
  [[/uploads/hexalink-tips-f.png]]
* A 3 (hospital) clue touching the border exactly 3 times in a row has only 2 combinations:
  [[/uploads/hexalink-tips-g.png]]

Keep in mind that a 2 (factory), 3 (hospital), or 4 (hotel) clue can have lines separated from each other.