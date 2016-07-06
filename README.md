# The Game of Hog

### Introduction
In Hog, two players alternate turns trying to reach 100 points first. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes, unless any of the dice comes up a 1, in which case the score for the turn is only 1 point (the Pig out rule).

### Special rules
To spice up the game, we will play with some special rules:

  - __Free bacon.__ A player who chooses to roll zero dice scores one more than the largest digit in the opponent's score.
    * _Example 1:_ If Player 1 has 42 points, Player 0 gains 1 + max(4, 2) = 5 points by rolling zero dice.
    * _Example 2:_ If Player 1 has 48 points, Player 0 gains 1 + max(4, 8) = 9 points.
    * _Example 3:_ If Player 1 has 7 points, Player 0 gains 1 + max(0, 7) = 8 points by rolling zero dice.


  - __Hog wild.__ If the sum of both players' total scores is a multiple of seven (e.g., 14, 21, 35), then the current player rolls four-sided dice instead of the usual six-sided dice.


  - __Swine Swap.__ At the end of each turn, if the last two digits of Player 0's score are the reverse of the last two digits of Player 1's score, the players' score will be swapped.
    * _Example 1:_ Player 0 has a score of 19 and Player 1 has a score of 91 after Player 0 has rolled. Reversing the last two digits of Player 0's score (19) results in 91, which are the last two digits of Player 1's score. This is considered a swap and the player's scores are switched. Player 0 now has a score of 91, Player 1 now has a score of 19 and Player 0's turn is over.
    * _Example 2:_ Player 0 has a score of 80 and Player 1 has a score of 8 at the end of Player 1's turn. In this example, Player 1's score is viewed as 08, which is the reverse of 80. The player's scores are swapped, leaving, Player 0 with 8 and Player 1 with 80. Player 1's turn ends.
    * _Example 3:_ Player 0 begins their turn with a score of 90 while Player 1 has 70 points. Player 0 rolls 7 dice, giving them 17 points. They now have a score of 107 and Player 1 has a score of 70. Swapping the last two digits of 107 will give back 70, so the two scores are swapped. Player 0 ends their turn with a score of 70 while Player 1 now has a score of 107. Because the swap occurs before Player 0's turn is over, Player 1 wins the game.

### Files

Files in the project:

* `hog.py`: A starter implementation of Hog
* `dice.py`: Functions for rolling dice
* `hog_gui.py`: A graphical user interface for Hog
* `ucb.py`: Utility functions for CS 61A
* `hog_eval.py`: Utility for evaluating the Hog project
* `images`: A directory of images used by hog_gui.py

### Running (GUI) - Tkinter required

To play against Bot, run:
```sh
$ python3 hog_gui.py -f
```
To see win rate of final stragegy, run:
```sh
$ python3 hog_gui.py --final
```

### Improving the AI
To improve the AI, you can modyfy the function:
```python
def final_strategy(score, opponent_score):
```
in the bottom of the file `hog.py`

### Class Project Site
[here]

[here]: <http://61a-su15-website.github.io/proj/hog/>

