---
quest: true
---
[[Minecade|https://play.fancade.com/5B7948C4AD85967E]] is a [[Minesweeper|https://en.wikipedia.org/wiki/Minesweeper_(video_game)]] clone by Mathias Elgaard,  where you uncover cells with numbers without uncovering a mine, and you can flag cells to help.
[[/uploads/minecademathiaselgaard.png | height=400px]]

## How to Play

Tap on a cell to uncover the cell. Hold on a cell for a long time to mark it as a flag. To win, uncover all cells without mines. You lose if you touch a mine. NOTE: All puzzles are randomized, so there isn't a predetermined solution to win.

A number determines how much mines are adjacent to the cell, even diagonally, an empty cell is a 0 clue.

## Helpful Tricks

Look for 1 clues which are in a neighbor with only 1 diagonal covered cell, you can flag them:

[[/uploads/minecade-a1.png | height=200px]]

[[/uploads/minecade-a2.png | height=200px]]

Any 1 clues that are adjacent to the flag, are 0 clues and now can be safe to uncover those cells adjacent to those 1s:

[[/uploads/minecade-a3.png | height=250px]]

Any other clues adjacent to the flag get "reduced" by 1.

To generalize, if there's a cell where the number of total white cells adjacent is equal to the number in the cell, all cells are mines:

[[/uploads/minecade-a4.png | height=250px]]

If the cell has equal amount of flags to the cell's number, all cells are safe: (Unless if you made a mistake)

[[/uploads/minecade-a5.png | height=250px]]

-------------------

Trickier strategies involve visualizing if a cell is a mine or not.

In a case like this:

[[/uploads/minecade-b.png | height=150px]]

The 1 has a mine on the top, but the 2 has a mine at the top as well. If there's not a mine in cell A, you cant satisfy both the clues at the same time because the neighboring cells in the 2 is forced, and 1 has too much mines into it, so the A cell is a mine and must be flagged.

-------------------

[[/uploads/minecade-c.png | height=150px]]

Same goes for this pattern, but inverted. If there's a mine in cell B, you can no longer satisfy both clues, since the 1 in the middle is forced to mark the remaining cells as safe, leaving no mines for the 1 on the right, so cell B is safe.

-------------------

In a beginner board, there are always exactly 10 mines in the board, in intermediate: 40, in expert: 99, so you can use this fact to reveal safe spots by counting the total mines in the squares with a non zero amount, and use this fact to disambiguate some unsolvable boards.

Some cases are unwinnable without guessing, so some luck is involved in solving puzzles.