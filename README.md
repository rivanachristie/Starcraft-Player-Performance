# Starcraft Player Performance
The Starcraft player dataset contains player performance data in ranked games. In this notebook, we will explore the player performance wrt their league, perform feature selection and finally, train different models to predict the league index for the user that played the given game. The following models are used to predict the league index:
1. Decision Tree
2. Random Forest
3. LightGBM
4. Feedforward Neural Network

## About the dataset
Import the dataset from the file 'starcraft_player_data.csv'. The dataset has 3395 records with 20 features each. The 'GameID' is a unique identifier for each game. The dataset has features like 'APM', 'ActionLatency', 'NumberOfPACs', etc that define the player performance.

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
The following models are trained as part of data modeling.

|Model	                    | Train Accuracy | Test Accuracy |
| ------------- | ------------- | ------------- |
|Decision Tree	            |    38.03%	| 36.67% |
|Random Forest	            |    48.16%	| 40.21% |
|LightGBM	                  | 49.15%	| 35.49% |
|Feedforward Neural Network	|   47.46%|	41.24% |

## Conclusion and Future Work
Based on the data exploration and modeling, here are some of the key findings:
1. Professional players tend to have a higher actions per minute resulting in lower action latency time. 
2. As the number of hours spent playing the game increase, the level of expertise of the player also increases. 
3. Action latency is the most important feature of all because it indicates how quickly a player is able to respond to Perception Action Cycles (PACs). 
4. Even though we tried 4 different models, we are unable to get high accuracy. This could mean that there are external factors not recorded in the dataset that might be influential in determining the league of a player.

In the future, I would like to explore some other models like Logistic Regression, Naive Bayes and XGBoost and I would also like to optimize the models by performing hyperparameter tuning. I would also like to experiment by training a model using features that do not have collinearity to see if they yield better results or not.
