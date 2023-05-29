# Starcraft Player Performance
The Starcraft player dataset contains player performance data in ranked games. In this notebook, we will explore the player performance wrt their league, perform feature selection and finally, train different models to predict the league index for the user that played the given game. The following models are used to predict the league index:
1. Decision Tree
2. Random Forest
3. LightGBM
4. Feedforward Neural Network

## About the dataset
The dataset has 3395 records with 20 features each. The 'GameID' is a unique identifier for each game. The dataset has features like 'APM', 'ActionLatency', 'NumberOfPACs', etc that define the player performance.

## Exploratory Data Analysis (EDA)
1. Number of games played by league:
![image](https://github.com/rivanachristie/starcraft_player_performance/assets/98617715/e81c94f2-f112-4e1c-b75c-f4970f76b403)

2. Distribution of Actions per minute (APM) by league:
![image](https://github.com/rivanachristie/starcraft_player_performance/assets/98617715/747938ab-7134-4b3b-823c-468b6ac161c7)

3. Distribution of Action Latency by league:
![image](https://github.com/rivanachristie/starcraft_player_performance/assets/98617715/90af8a1d-7801-4d74-99e0-a960410916fc)

## Data Preprocessing
As part of data preprocessing, the following steps are performed:
1. Handling outliers
2. Imputing missing values
3. Dropping NaN values
4. Log Transformation
5. Scaling using StandardScaler()
6. Feature selection using SelectKBest()
7. Splitting into train and test sets

## Data Modeling




