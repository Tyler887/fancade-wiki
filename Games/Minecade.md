---
quest: true
---
[[Minecade|https://fancade.page.link/xfsd]] is a game by Mathias Elgaard where you uncover spaces with numbers without uncovering a mine, and you can flag spaces to help. Theres also a timer for if you want to speedrun a minesweeper map.

## How to play
Tap a space to uncover the space, the first uncovered space is never a mine. Hold a space for a long time to flag it, to win, uncover all spaces without mines, you "lose" (cant play anymore) if you touch a mine. NOTE: All puzzles are randomized, so there isnt a predetermined solution to win.

### Rules
A number determines how much mines are adjacent to the cell, even diagonaly, an empty cell is a 0 clue.

## Helpful tricks
If you start with only 1 number, its just luck of the draw if you really start or reset.

If you find a lot of numbers in a click, look for 1 clues which are in a neighbor with only 1 diagonal white cell, flag them.

Any 1 clues that are adjacent to the flag, are 0 clues and now can be safe to uncover those cells adjecent to those 1s.

Any other clues adjacent to the flag get "reduced" by 1

If theres a cell where the number of total white cells adjacent is equal to the number in the cell, all cells are mines.

If the cell has equal amount of flags to the cell's number, all cells are safe UNLESS you made a mistake

in a case like this

W 0 0 0

W 1 2 ?

W O O A

W O O O

The 1 has a mine on the bottom, but the 2 has a mine at the bottom as well, if theres not a mine in cell A, you cant satisfy both the clues at the same time, so the A cell is a mine and must be flagged.

W 0 0 0

W 1 1 ?

W O O B

W O O O

Same goes for this pattern, but inverted, if theres a mine in cell B, you can no longer satisfy both clues, so cell B is safe.

Some cases are unwinnable without guessing, so some luck is involved in solving puzzles.