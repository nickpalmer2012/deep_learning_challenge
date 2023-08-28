# deep_learning_challenge
Module 21 Challenge - Neural Networks and Deep Learning Models

## Overview
Alphabet Soup foundation wants to develop a machine-learning model to help predict which ventures will succeed based on metadata provided from previous ventures that AS has funded.

## Results
### Data Preprocessing
* What variable(s) are the target(s) for your model?
  * The target for the model was weather or not the venture was successful. The "IS_SUCCESSFUL" column
     
* What variable(s) are the features for your model?
  * The features of the model are all of the columns in the original dataset with the exception of the EIN, NAME, and IS_SUCCESSFUL columns. This is because EIN and NAME columns are unique identifiers and the IS_SUCCESSFUL column is our target data.

* What variable(s) should be removed from the input data because they are neither targets nor features?
  * The EIN And NAME columns

### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * The initial reason for having two hidden layers for this model is because the jupyter notebook file indicated that we should add two hidden layers. After research, it appears that the determination for the number of neurons, number of hidden layers, and the type of activation function applied comes down to experimentation and evaluating the accuracy results. I noticed that the output shape showed 80 neurons for the first layer, 30 for the second, and 1 for the output layer, so I stuck with those numbers. Any time I adjusted those units, I saw a dramatic negative change in the model accuracy figure for the model. I looked at different solutions from the examples in class and I landed on Sigmoid for the first layer, because I learned that this type performs well with binary results. I used "relu" for the second layer since it seemed to make the accuracy score jump closer to our target accuracy. Finally, I used linear activation for the output layer as linear since the value we are predicting is continuous in nature. 
* Were you able to achieve the target model performance?
  * Not quite. I was able to get to about 72% accuacy with the tweaks I made to the model parameters.
* What steps did you take in your attempts to increase model performance?
  * I adjusted almost every parameter you can in order to get the model close to the target accuracy score. I adjusted tried adjusting the neurons, but anyting outside of the 80, 30, 1 ratio reduced the accuracy score. I tried adjusting the activation methods and that negatively impacted the accuracy score. It seemed like anything outside of 5 epochs resulted in a poor accuracy score, so I decided to leave it at 5.

## Summary
It seems like the best outcome for this model is 75% accuracy, which I think is pretty good considering how many features are being evaluated. I think if you brought this model to a decision maker and said that the model had a 75% accuracy score, they would use it to compare its predictions vs predictions made by the team using the method they used before this model was available. I suppose you could try a random forest classifier model to see if the accuracy performed better as it is supposed to be influenced less by outliers. 



