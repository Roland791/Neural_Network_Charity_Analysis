# Neural_Network_Charity_Analysis

## Overview
The Charitable organization Alphabet Soup is trying to find a way to predict whether applicants for funding will be successful. By analyzing historical data for 34,000 organizations that have been funded by Alphabet Soup and running it through a Machine Learning Neural Network, we will attempt to create a model that can accurately make that prediction. 

## Results

### Data Preprocessing
    Model Target Variable: IS_SUCCESSFUL Column
    Model Feature Variables: All other columns excluding EIN and Name

### Compiling, Training and Evaluating the Model
The initial model that was ran contained 2 hidden layers running the “relu” activation function and containing 70 and 40 neurons respectively followed by an output layer running the “sigmoid” function. The model was ran for 30 Epochs and was not able to reach the target 75%. The final accuracy for the model was 67.7%.

### Optimizing Performance
Prior to attempting optimization models, an attempt was made to reduce the number of columns in the initial dataset by removing “Use_Case”, “Special Considerations” and “Income_Amt” Categories. 3 different model variants were then ran to see if the accuracy could be improved to the goal state of 75% 

    Attempt 1: A Third Layer was added (also running “relu” activation) and the neurons were set at 100, 50 and 10 respectively. Accuracy dropped to 51.4%.

    Attempt 2: The Third Layer and neurons from Attempt #1 were used, but activation for each layer were set to “tanh” for the hidden layers and “sigmoid” for the output. Accuracy was 51.8%

    Attempt 3: Settings from Attempt 1 were used, but attempted to increase the number of Epochs ran from 30 to 60. Accuracy was 52.2%

## Summary

The accuracy score for the model dropped by over 15% across the optimization attempts compared to the original model. This loss in accuracy can be explained from the fact that the model overfitted. Alternative options to optimize our neural network would be to look at removing more features or simply adding more data to the dataset to increase accuracy. Since our accuracy score was not particularly up to the standard with neural networks, Random Forest classifiers could be used instead. Random Forest is a robust and accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks and could have avoided the data from being overfitted.
