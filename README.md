# *Mobile Game A/B Testing with Cookie Cats*

<a href="https://www.facebook.com/cookiecatsgame">Cookie Cats</a> is a hugely popular mobile puzzle game developed by <a href="http://tactile.dk">Tactile Entertainment</a>. It's a classic "connect three"-style puzzle game where the player must connect tiles of the same color to clear the board and win the level. 

![github](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/1a8d4b13-78b8-4134-a47a-bf7eb1531bd5)

As players progress through the levels of the game, they will occasionally encounter gates that force them to wait a non-trivial amount of time or make an in-app purchase to progress. In addition to driving in-app purchases, these gates serve the important purpose of giving players an enforced break from playing the game, hopefully resulting in that the player's enjoyment of the game being increased and prolonged.

![Gate](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/12e645d0-9825-4019-a0d3-bd9b1cafbe01)

But where should the gates be placed? Initially the first gate was placed at level 30,  we're going to analyze an AB-test where we moved the first gate in Cookie Cats from level 30 to level 40. In particular, we will look at the impact on player retention.

## Business goals

Conduct an A/B test in Cookie Cats, evaluating the optimal placement of encounter gates (forcing wait times or in-app purchases) and their impact on player retention.

### Methods Used:
* Hypothesis Testing
* Bootstrap Analysis
* Statistical Analysis

# Dataset information:
The dataset has **90189 rows** and **5 columns**

![github](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/80d5e78b-e4c9-4f82-aeed-7c42e84d0f90)

![github](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/a76031fc-a6b5-42bd-9956-e5bb39891265)

Number of player for each gate option:

![github](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/28b12fda-f83d-4d49-90bf-a60e7ef19ae8)
## Statistical step:
### 1. The distribution of the number of game rounds players played during their first week playing the game.

![Untitled](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/26ffb09c-6f4c-4484-8743-5ad93eb83f25)

We can see that some players install the game but then never play it (0 game rounds), some players just play a couple of game rounds in their first week, and some get really hooked!

==> **1-day retention**: The percentage of players that comes back and plays the game one day after they have installed it. 

==> The higher 1-day retention is, the easier it is to retain players and build a large player base.

### 2. Calculate 1-day retention and its confidence
* Overall 1-day retention: **0.4452**
* ==> A little less than half of the players come back one day after installing the game.
* 1-day retention between two groups (gate_30) and (gate_40)

![Untitled](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/15ceb54a-e375-4ee8-b366-76d554a09932)

* It appears that there was a slight decrease in 1-day retention when the gate was moved to level 40 (44.2%) compared to the control when it was at level 30 (44.8%). It's a small change, but even small changes in retention can have a large impact.

* We will repeatedly re-sample our dataset (with replacement) and calculate 1-day retention for those samples. The variation in 1-day retention will give us an indication of how uncertain the retention numbers are.

![image](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/c75a9614-2388-4a35-9449-ddfc41347e8a)
* ==> We can see that the most likely % difference is around 1% - 2%, and that most of the distribution is above 0%, in favor of a gate at level 30
* **Probability** that the difference above 0% is: **0.964**

### 3. Calculate 7-day retention and its confidence
* 7-day retention between two groups (gate_30) and (gate_40)

![Untitled](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/a3e568aa-8d08-4927-9b9a-d67dd0bc90d2)

* Like with 1-day retention, we see that 7-day retention is slightly lower (18.2%) when the gate is at level 40 than when the gate is at level 30 (19.0%).
* This difference is also larger than for 1-day retention, presumably because more players have had time to hit the first gate.
* We also see that the overall 7-day retention is lower than the overall 1-day retention; fewer people play a game a week after installing than a day after installing.

![image](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/9f50e438-dac6-4dfc-9ef8-ab0cb0de3ea5)

* ==> there is strong evidence that 7-day retention is higher when the gate is at level 30 than when it is at level 40
* **Probability** that the difference above 0% is: **100**
  
# Conclusion:
* If we want to keep retention high — both 1-day and 7-day retention — we should not move the gate from level 30 to level 40.
