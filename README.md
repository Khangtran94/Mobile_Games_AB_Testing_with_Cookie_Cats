# *Mobile Game A/B Testing with Cookie Cats*

<a href="https://www.facebook.com/cookiecatsgame">Cookie Cats</a> is a hugely popular mobile puzzle game developed by <a href="http://tactile.dk">Tactile Entertainment</a>. It's a classic "connect three"-style puzzle game where the player must connect tiles of the same color to clear the board and win the level. 

![github](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/1a8d4b13-78b8-4134-a47a-bf7eb1531bd5)

As players progress through the levels of the game, they will occasionally encounter gates that force them to wait a non-trivial amount of time or make an in-app purchase to progress. In addition to driving in-app purchases, these gates serve the important purpose of giving players an enforced break from playing the game, hopefully resulting in that the player's enjoyment of the game being increased and prolonged.

![Gate](https://github.com/Khangtran94/Mobile_Games_AB_Testing_with_Cookie_Cats/assets/146164801/12e645d0-9825-4019-a0d3-bd9b1cafbe01)

But where should the gates be placed? Initially the first gate was placed at level 30,  we're going to analyze an AB-test where we moved the first gate in Cookie Cats from level 30 to level 40. In particular, we will look at the impact on player retention.

## Business goals

Conduct an A/B test in Cookie Cats to determine the optimal placement of gates and its impact on player retention.

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

## Data Validation:



## Exploratory data analysis (EDA):





# Recommendations for future action:
* We suggest to deploy the Logistic Regression model to the recent recipes. With approximately 78% in predict high-traffic recipes, this predictive model can assist the product manager reaches the business goals in generating more traffic to the websit and boost overall performances.
* Both models suggest that category is the main feature affecting the traffic. Therefore, we should try to increase the number of categories and create more meaningful features from existing variables.
* To improve the accuracy, we should collect more information, such as more details about time to cost, cost per servings, and also the combination of ingredients.
