# 2022 Kaggle March Machine Learning Mania Submission

## Overview
This is the notebook submitted to the [2022 Kaggle March Machine Learning Mania 2022 Compteition](https://www.kaggle.com/competitions/mens-march-mania-2022/overview). I had a blast learning new technologies like PyCaret and really enjoyed diving into the data sets Kaggle and the Kaggle community provided.

[Placed](https://www.kaggle.com/competitions/mens-march-mania-2022/leaderboard) 18/930 submissions with a Log Loss score = 0.58929. Earned a silver medal for placing in the top 50 submissions.

## Goals of the compteition:
* Create a model that predicts the probablility of a team winning a tournament game for all possible games in the Men's 2022 NCAA Basketball Tournament.
* Minimize log loss for each predicted game.
* Output the results into a submission file.
* Output the results in a user friendly way to interpret using [ncaa_simulator](https://www.kaggle.com/code/thomaskotopoulos/ncaa-simulator).

## Methedology Overview
* First, I calculated metrics (score, posessions, pts/posession, efg%, ft%, tov%, ast%, reb%) for each game since 2003.
* I then used that df to calculate season totals for each team for seasons > 2003.
* For each tournament game, I added the season totals for the winning team and losing team as well as their Ken Pom AdjO, AdjD, Tempo, Luck and SOS.
* Finally, I split the data into a train and test set and fed these two sets into the PyCaret model which produced the submission file. 

