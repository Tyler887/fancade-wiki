Sets the score and/or [[coins]].

* In Fancade 1.6, a second input is made available to set the amount of Coins the player can get playing a game.

There is a setting that determines which score to consider as better one.

* Most Points: the more points the better
* Fewest Points: the less points the better

You also can provide time score, just make sure that the input is a total amount of seconds and you selected one of these options:

* Fastest Time: the faster the better
* Longest Time: the longer the better

Setting a negative score removes the score.

[[/uploads/Set_Score.png | width=336px]]
## Example 

[[/uploads/IMG_20210108_143008.png]]

_Touching the screen gives you 30 points._

## Edge Case

When there are multiple Set Scores with different comparisons for which is better, the new score is compared to your Personal Best by the comparison in the block that set it (e.g. Least Points). 
If it is better, the old PB is completely discarded. 
Time is also compared to points in seconds. 