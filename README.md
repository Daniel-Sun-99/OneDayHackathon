# OneDayHackathon Project 🚀

## General Overview
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The main purpose of this project was to use as a benchmark to gauge how far I've come in the past 2 months of learning at General Assembly's Data Science Immersive Bootcamp. This project was an 8 hour time restricted endeavor. From the start in the morning, we had to find a dataset, clean it, and perform what ever analysis or model fitting we saw necessary and present our findings in the afternoon. The dataset used in this project is a kaggle dataset of professional Counter Strike: Global Offensive (CS:GO) professional match statistics. Find the full dataset and data dictionary here: [kaggle dataset](https://www.kaggle.com/datasets/sadmadlad/csgo-pro-players-dataset).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Utilizing this dataset I decided to explore any trends among high performing cs:go professionals and how they impact their performance in games. Using that information I fitted a model to predict the impact a professional player may have based on past statistics with hopes of applying this model to determine if there were any up and coming rookies that may be valuable for an organization to pick up early.


----

## EDA and Cleaning 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The dataset had no missing inputs or NaN values so little imputing was necessary. A few columns, namely anything that affiliates a set of statistics with a specific player or organization like team, nickname, or hltv statistics page, were removed from the dataset. Strong players are likely to be picked up by strong teams, however, in the future I wish for this model to be applied to rookies who are not affiliated with any organization and so the model needs to be trained without the influence of brand names and be purely trained on in game statistics. 

----

## Results
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;After cleaning the data and preparing it to be passed through pipelines to train various models, the best model for predicting and accurate impace a player would have based on their ingame statistics was a voting regressor model combining an adaregressor, ridgeregressor, and svrregressor models. The final model was slightly overfit, however, had a test set accuracy of approximately 85%. Due to the time restraints, the weights were not able to be pulled from the pipeline and thus the importance of each feature is unknown. If more time were to be spent on the project, the feature importances would be properly acquired as this could be important in increasing the efficiency of finding new promising rookies as recruiters may only need to look at a few strong statistics instead of all of them.