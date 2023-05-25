## Overview 
This project aims to develop a binary classifier using my knowledge of machine learning and neural networks. I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The overall objective is to optimize the model in order to attain an accuracy score surpassing 75%.

#### Data Preprocessing
The model aims to predict the success of applicants if they receive funding which is indicated by the `IS_SUCCESSFUL` column in the dataset which is also the target variable of the model. The feature variables are every column other than the target variable and the non-relevant variables (`EIN` and `names`). The features capture relevant information about the data and can be used in predicting the target variables, the non-relevant variables that are neither targets nor features will be drop from the dataset to avoid potential noise that might confuse the model.  
During preprocessing, I implemented binning/bucketing for rare occurrences in the `APPLICATION_TYPE` and `CLASSIFICATION` columns. Next, I transformed categorical data into numeric data. I split the data into separate sets for features and targets, as well as for training and testing. Lastly, I scaled the data to ensure uniformity in the data distribution. 

#### Compiling, Training, and Evaluating the Model
Initial Model: For my initial model, I decided to include 3 layers: an input layer with 50 neurons, a second layer with 25 neurons, and an output layer with 1 neuron. I made this choice because I believed it was a good starting point for the model. In this case, there were 43 input features remaining after removing 2 irrelevant ones. I selected the `relu` activation function for the first and second layers, and the `sigmoid` activation function for the output layer since the goal was binary classification. To start, I trained the model for 100 epochs and achieved an accuracy score of approximately  for the training data and  for the testing data.

**Optimization attempts**
1. I attempted to optimize the model’s performance by first making adjustments to the neurons. I modified the total number of neurons to 86 so it would be about two times the number of input features. In this case, there were 43 input features remaining after removing 2 irrelevant ones. After adjusting the amount of neurons I got an accuracy score of  for my training set and  for my testing set.

2.


3. 

 

## Summary
Given that I couldn't attain the target accuracy of 75%, I wouldn't suggest any of the models above. However, with additional time, I would explore alternative approaches like incorporating the Random Forest Classifier and experimenting with different preprocessing modifications. I believe that making changes to the dropout layers, trying out various activation functions, and adjusting the number of layers and neurons could also contribute to optimizing the model and achieving the desired goal of 75% accuracy. 
