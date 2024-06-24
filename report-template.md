# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Aribim Bristol

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I learned that removing the negative values from the predictions is required to submit the submission.

### What was the top ranked model that performed?
The WeightedEnsemble_L3 performed best.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
During EDA, additional features were added by splitting the datetime coloumn into year, month, day and hour.

### How much better did your model preform after adding additional features and why do you think that is?
The model performance improved from a score of 1.8213 before adding additional features to 0.45619 afterwards.
This might be because the models are able to select more relevant features and disregard the less relevant ones. In this case, seperating the datetime column into years, months, days and hours might have given the models more relevant information to work with. 

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
My model did not perform better after hyperparameter tuning. The score dropepd from 0.45619 to 0.48043. 

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend more time on hyperparameter tuning since my model did not improve.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|    | model        | hpo1                    | hpo2         | hpo3       |   score |
|---:|:-------------|:------------------------|:-------------|:-----------|--------:|
|  0 | initial      | root_mean_squared_error | best_quality | regression | 1.8213  |
|  1 | add_features | root_mean_squared_error | best_quality | regression | 0.45619 |
|  2 | hpo          | default                 | auto         | regression | 0.48043 |

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation
