# Deep Learning Model Performance Report for Alphabet Soup

## Overview of the Analysis

The purpose of this analysis is to develop a deep learning model that can classify charity funding applications to help Alphabet Soup make more informed decisions about which organizations are most likely to succeed based on historical data. This involves building a neural network that can predict whether an organization will be successful given a set of features derived from the dataset provided by Alphabet Soup.

## Results

Data Preprocessing
Target Variable(s):

The target variable for the model is the "IS_SUCCESSFUL" column, which indicates whether a charity campaign was successful (1) or not (0).
Feature Variable(s):

The features used for training the model include all the other relevant variables, such as:
"APPLICATION_TYPE"
"AFFILIATION"
"CLASSIFICATION"
"USE_CASE"
"ORGANIZATION"
"STATUS"
"INCOME_AMT"
"SPECIAL_CONSIDERATIONS"
"ASK_AMT"
Removed Variables:

The "EIN" (Employer Identification Number) and "NAME" columns were removed because they are unique identifiers and do not provide predictive value for the success of a charity.

Compiling, Training, and Evaluating the Model
Neurons, Layers, and Activation Functions:

The model consisted of:
2 hidden layers with 6 neurons each.
Relu activation function was used for both hidden layers to introduce non-linearity and help the model learn complex patterns.
The output layer had a single neuron with a sigmoid activation function for binary classification (successful or unsuccessful).
This architecture was chosen to maintain a balance between model complexity and performance, without overfitting the data.
Target Model Performance:

The model achieved an accuracy of 73%, slightly below the target of 75%. Although this is a decent performance, further improvements are needed to meet the target.
Steps Taken to Improve Performance:

Tuning Hyperparameters: Various combinations of neurons, batch sizes, and epochs were tested.
Normalization of Input Data: All numerical features were normalized to ensure the neural network can train efficiently.
Model Optimization: The addition of more layers and increasing the number of neurons was explored but led to diminishing returns. Dropout layers were also tested to reduce overfitting. I removed the dropouts and didnt save due to the decrease being 10%-15%.
Re-evaluating Features: Certain low-variance features were removed to simplify the model's input data.

## Summary

The deep learning model developed for Alphabet Soup achieved a 73% accuracy rate. While the model performs reasonably well, there is still room for improvement to meet the target of 75%. Alternative models, such as Random Forest Classifiers or Gradient Boosting Machines (GBM), could be considered, as they can handle non-linear relationships and feature interactions better than simple feedforward neural networks in some cases. These models may provide more flexibility in handling the dataset’s structure, leading to better classification performance.
