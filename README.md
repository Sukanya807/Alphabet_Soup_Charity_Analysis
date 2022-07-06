# Neural_Network_Charity_Analysis

## Overview & Purpose

The purpose of this project is to use machine learning and neural networks and create a binary classifier that is capable of predicting if the applicants that will be funded by a Charitable Organization called 'Alphabet Soup' will be successful. The dataset used for this analysis contains various measures on 34,000 organizations that have been funded by Alphabet Soup. The project includes three steps -

- Preprocessing the data for the neural network
- Compile, Train and Evaluate the Model
- Optimizing the model

## Resources
- Neural Network and deep learning
- Python - Pandas, Tensorflow, ScikitLearn
- Jupyter Notebook

## Data Source
[Alphabet Soup Charity Dataset](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-online/module_19/charity_data.csv)

## Results

### Data Preprocessing

- Dropped Variables : **EIN** and **NAME**
- Target Variable: **IS_SUCCESSFUL**
- Feature Variables : All other columns except the three mentioned above (For the optimization attempts, additional features that could be noisy were dropped)

### Compiling, Training and Evaluationg the Model

- For my initial attempt, the number of inputs were **len(X_train[0])**.
- The deep learning model includes 2 hidden layers with 50 and 20 neurons respectively and one output layer.
- The activation functions used in the hidden layers are **RELU** which is ideal for looking at positive non-linear input data for classification or regression.
- The activation function used in the output layer is **SIGMOID** which is ideal for binary classification.

![]()

**Was the model able to achieve the traget performance?**

The model was not able to achieve the target accuracy of 75%. The accuracy of this model was only 72.6%.

![]()

**What steps were taken to increase model performance**

Three additional attempts were made to increase the accuracy of the model to 75% and above.

**** First Attempt

- Two additional variables, Organization and Status were dropped from the dataframe before training.
- The number of hidden layers were increased to 4.
- The number of neurons were changed to 100, 90, 70 and 50.
- The activation functions for the hidden layers were changed to relu, tanh, relu and relu respectively.
- The number of epochs were increased to 80.
- The model was unable to reach the target accuracy.

![]()

**** Second Attempt
- The columns EIN, NAME and STATUS were dropped from the dataframe.
- Three hidden layers were included in the model.
- The number of neurons in the hidden layers were 100, 90 and 70 respectively.
- The activation functions for the hidden layers were changed to sigmoid, tanh and tanh respectively.
- The number of epochs was changed to 100.
- The model was unable to reach the target accuracy.

![]()

**** Third Attempt
- The columns EIN,NAME and STATUS were dropped from the dataframe.
- The app type count was increased to 7000 and classification count increased to 3000 for binning.
- The number of hidden layers added to the model was 4 with activation functions of relu, tanh, relu and relu respectively.
- The number of neurons for each hidden layer were changed to 120, 100, 90 and 50 respectively.
- The number of epochs were 100.
- The model failed to achieve the desired accuracy.

![]()

## Summary

Despite the various changes made in the model in the three attempts, the model was unable to reach the target accuracy of 75%. The average accuracy of this model continued to be around 72%. We could try to optimize this model by removing more features or adding more datapoints. A Random Forest Classifier model can probably do a better job here instead of neural networks. This is because the random forest is a robust and accurate model that use a number of weak learner algorithms and combine their output to make a final classification. The model can also easily handle non-linear data and outliers.







