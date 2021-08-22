# Neural_Network_Charity_Analysis
## Overview:
We are working with a Charity Network to see if their money is being used efficiently. To accomplish this, we used a neural network specifically using the Tensorflow machine learning library from Python. We wanted to predict the likelihood of success for potential project by using a neural network.

## Results:
### Data Preprocessing:
  * Variables considered the targer: IS_SUCCESSFUL
  * Variables considered the features: EIN, NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
  * Variables that are neither targers nor features (removed from the input data): EIN, NAME
### Compiling, Training and Evaluating the Model
  * Initially the model included a single input feature and two hidden layers with the first hidden layer having 50 neurons and the second hidden layer having 25 neurons. Each of the hidden layers employed the "relu" activation method. The output layer employed the "sigmoid" activation.
  * I was not able to achieve my goal of 75%. The first model was 69.97% and the second below 50%.
  * Steps taken to increase model performance:
    * Optimization 1: Reduced the application_counts to less than 500 and the classification_counts to less than 800 while also increasing the neurons to 80 and 30.
    * Optimization 2: Dropped the feature SPECIAL_CONSIDERATIONS   because the prevalance of "N" for the value. It reutrned application_counts to less than 700 and classification_counts less than 1800. Changed hidden layers to original values and added a third hidden layer with 25 neurons.
    * Optimization 3: Dropped the third hidden layer and changed the activation method to "tanh"
## Summary:
Overall, I was not able to receive an accuracy score greater than 75%. I feel I could have achieved better results by using a supervised machine learning model like "Random Forest Classifier" to reduce overfitting and improve my accuracy score.
