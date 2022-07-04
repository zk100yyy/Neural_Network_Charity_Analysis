# Neural Network Charity Analysis

## Overview

To predict loan risk for Alphabet Soup, Machine Learning and Neural Networks are used to analyze a dataset of more than 34,000 organizations that have received funding from Alphabet Soup over the years. Classifiers based on neural network models have been developed and evaluated.

## Results

### Data Preprocessing

- The "IS_SUCCESSFUL" variable is considered the target of the model.
- The rest of the variables, as well as their encoded features, are considered the features of the model.
- The "EIN" and "NAME" variables are neither targets nor features, and should be removed from the input data.

### Compiling, Training, and Evaluating the Model

- Using kerastuner, a number of hyperparameters of the neural network model have been adjusted and the best model has the following hyperparameters:

    |Hyperparameters|Value|
    | :---: | :---: |
    |Number of hidden layers | 5|
    |Number of neurons on layer 1| 21|
    |Number of neurons on layer 2| 16|
    |Number of neurons on layer 3| 51|
    |Number of neurons on layer 4| 16|
    |Number of neurons on layer 5| 76|
    |Activation Function| Sigmoid|

    However, it is worth noting that the difference in models regarding performance is marginal. 

- Even the best model upon tuning the hyperparameters was unable to achieve the target model performance.
- Kerastuner was able to change the number of hidden layers, the number of neurons of each layer, and the activation function for the hidden layers. I also tried to remove seemingly irrelavent variables, such as "ASK_AMT". However, none was able to achieve the target performance, which is above 75% accuracy.

## Summary

Pre-processing of the input dataset was successfully carried out. The neural network model was successfully compiled and regressed. However, the model performance only achieved 72-73% accuracy even upon changing the hyperparameters, such as activation function, number of layers and 
