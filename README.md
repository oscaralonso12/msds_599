# All-NBA 2023-2024 Team Predictions

This repository contains code for predicting the All-NBA teams for the 2023-2024 NBA season based on bootstrapped probit model.

## Dataset
The data used for this analysis was created by scraping box score, advanced stats, and historical All-NBA teams from Basketball Reference since the 1979 NBA season. The dataset includes various player statistics, including points, assists, rebounds, steals, blocks, player efficiency rating (PER), true shooting percentage (TS%), usage percentage (USG%), and win shares (WS). The analysis focuses on seasons starting from 1979 onwards, coinciding with the introduction of the NBA 3-point line.
![features_by_all_nba_historical](https://github.com/oscaralonso12/All-NBA-teams-prediction/assets/41983149/e216e31a-ec5d-4d1e-a8f5-c3b58dd1ab1c)

## Data Preparation
- The data undergoes normalization on a season-by-season basis, with numerical values adjusted to fall within the range of 0 to 10 for each individual season.
- The full dataset is split into training and test datasets.
- Training data excludes the 2023-2024 season.
- Test data includes only players who played at least 65 games in the 2023-2024 season.

## Model Building
- The data is bootstrapped, and 1000 probit model are fitted to predict All-NBA selection.
- The distribution of estimates is visualized using histograms.
- Probabilities for each model are predicted and combined using the median across models.
![estimates_dist](https://github.com/oscaralonso12/All-NBA-teams-prediction/assets/41983149/6f06e092-6a48-4ed0-b3d4-aafab62070c6)

## Results
Based on the calculated probabilities, the top 15 players are identified and classified into All-NBA teams.

## Table of All-NBA 2023-2024 Team Predictions
![all_nba_2023-2024_preds](https://github.com/oscaralonso12/All-NBA-teams-prediction/assets/41983149/e3cf4fd1-5e2e-4bdf-ac3b-ebaff1c566b8)

