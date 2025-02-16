# Board Games Rank Prediction

## Project description
The goal of this project is to predict **rank** of a board game. As a point of reference, data has been gathered from a website [BoardGameGeek](https://boardgamegeek.com/), which is:

>"...an online resource and community that aims to be the definitive source for board game and card game content. The site is updated on a real-time basis by its large and still growing user base — more than two million registered users! — making the Geek the largest and most up->to-date place to get gaming information! You can become a registered member of BGG for free, although we welcome your contributions to the site in the form of ratings, reviews, and thoughts on games to the existing database!"

Original dataset contains information about approx. 21k board games. Data has been gathered on Feb 2024.

## Dataset description
Dataset comes from [Kaggle](https://www.kaggle.com/datasets/joebeachcapital/board-games).
Dataset used in the project consists of two merged files: 
- File *details* containing basic information about board games available on the site,
    - primary - primary name of the board game
    - year_published - year of the game first release
    - min_players - minimum number of players required to play
    - max_players - maximum number of players allowed to play
    - playing_time - average playing time (in minutes)
    - min_playtime - minimal playing time (in minutes)
    - max_playtime - maximal playing time (in minutes)
    - min_age - recommenden minimal age of player

- File *ratings* containing games' ratings:
    - owned - number of users having the game in their collecion
    - trading - number of users willing to trade the game - game for sale
    - wanting - user would like to buy game for himself
    - wishing - user would like to receive game as a gift
    - rank - rank of the game
    - average - average rate
    - bayes_average - Bayes average rating*
    - users_rated - number of users, who rated the game

*In order to prevent a new or rare game with only a few high ratings from taking the top spots in the ranking, 30 average ratings (not sure if it 5.5 or simply the current average rating on the geek) are added to every rating to form the Bayesian average. As more ratings are received, the effect of these "damper ratings" is reduced to nil.

## Models used in the project:
- Linear Regression,
- Random Forest,
- Support Vector Machines.
