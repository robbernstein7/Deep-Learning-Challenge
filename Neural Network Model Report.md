## Overview 
This project aims to develop a binary classifier using my knowledge of machine learning and neural networks. I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The overall objective is to optimize the model in order to attain an accuracy score surpassing 75%.

#### Data Preprocessing
The model aims to predict the success of applicants if they receive funding which is indicated by the `IS_SUCCESSFUL` column in the dataset which is also the target variable of the model. The feature variables are every column other than the target variable and the non-relevant variables (`EIN` and `names`). The features capture relevant information about the data and can be used in predicting the target variables, the non-relevant variables that are neither targets nor features will be drop from the dataset to avoid potential noise that might confuse the model.  
During preprocessing, I implemented binning/bucketing for rare occurrences in the `APPLICATION_TYPE` and `CLASSIFICATION` columns. Next, I transformed categorical data into numeric data. I split the data into separate sets for features and targets, as well as for training and testing. Lastly, I scaled the data to ensure uniformity in the data distribution. 

#### Compiling, Training, and Evaluating the Model
Initial Model: For my initial model, I decided to include 3 layers: an input layer with 50 neurons, a second layer with 25 neurons, and an output layer with 1 neuron. I made this choice because I believed it was a good starting point for the model. In this case, there were 43 input features remaining after removing 2 irrelevant ones. I selected the `relu` activation function for the first and second layers, and the `sigmoid` activation function for the output layer since the goal was binary classification. To start, I trained the model for 100 epochs and achieved an accuracy score of approximately 73.94% for the training data and 72.8% for the testing data.

![optimization 1](https://github.com/robbernstein7/Deep-Learning-Challenge/assets/119881903/cd7fcbd4-c5bb-4ef1-b3a4-878b370fe2c0)

**Optimization attempts**
1. I attempted to optimize the model’s performance by first making adjustments to the neurons. I modified the total number of neurons to 86 so it would be about two times the number of input features. In this case, there were 43 input features remaining after removing 2 irrelevant ones. After adjusting the amount of neurons I got an accuracy score of 74.02% for my training set and  72.93% for my testing set.


![optimization 2](https://github.com/robbernstein7/Deep-Learning-Challenge/assets/119881903/36e8c993-6f6e-453e-bf16-57e6f1fb002a)


2. For my next attempt I changed the model by adding 2 dropout layers with a rate of 0.5 to enhance generalization and changed the activation function to tanh in the input and hidden layer. With that I got an accuracy score of 74.11% for my training set and 73.02% for my testing set.


![optimization 3](https://github.com/robbernstein7/Deep-Learning-Challenge/assets/119881903/22c8cd1e-62db-49e5-86b9-eb2a5bc24003)


3. For my final optimization attempt, I used hyperparameter tuning. During this process, Keras identified the optimal hyperparameters, which include using the tanh activation function, setting 76 neurons for the first layer, and assigning 5, 20, and 3 units for the subsequent layers. As a result, the model achieved an accuracy score of 73.21%.

![optimization 4](https://github.com/robbernstein7/Deep-Learning-Challenge/assets/119881903/df253fb1-8098-423c-a798-7743ab232fc0)


## Summary
After the three attempts at optimization I couldn't attain the target accuracy of 75%, therefore  I wouldn't suggest using any of the models above. With more time I would explore alternative approaches like incorporating the Random Forest Classifier and experimenting with different preprocessing modifications. I believe that making changes to the dropout layers, trying out various activation functions, and adjusting the number of layers and neurons could also contribute to optimizing the model and achieving the desired goal of 75% accuracy. 
