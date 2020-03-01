# Predicting Bikeshare

Predict the bikeshare usage for December given the data for last 60 days. 

The graph below shows the rider data for the first 10 days of December. 

![number of bikers](https://github.com/shahzina/Bikeshare/blob/master/images/num_bike_riders.png)

## Building our neural network in Python:

For this project I built my own neural network from scratch. I started by creating a Neural Network class where I started with the init function and set the number of input, hidden and output nodes. I also defined the activation function and learning rate in the init function. The values for hidden nodes, output nodes and the learning rate are set later and can be changed until we get desired accuracy. The init function is executed when a new instance is created and is used to set initial values for the attribute of the instance. <br>

Then I defined the train function which uses the forward pass function, backpropagation function, a function to update the weights after each iteration and a run function. All these functions are also defined in the class NeuralNetwork. <br>

In the jupyter notebook we start by cleaning and organizing the data, then dividing into training, test and validation datasets. Then an instance of class NeuralNetwork is created and the input values and hyperparameters are passed as arguments. The input values are passed as an array and the model goes through every input value one by one. Here, the training and validation losses are calculated and plotted. <br>

The validation loss, 0.173, is higher than the training loss at 0.877, which means that there is overfitting and the model tends to generalize on the test data. <br>

The training and validation loss was as follows:
![train_valid_loss](https://github.com/shahzina/Bikeshare/blob/master/images/train_valid_loss.png)

### What does this mean? <br>
Accuracy in neural networks is measured as a percentage but loss is the summation of errors made for each example in training or validation sets. We are using the mean squared error to calculate the loss for our network and we define a function for this in our jupyter notebook. Loss tells how well or bad the model behaves after each iteration of optimization. While training our model, the goal is to reduce the loss as much as possible. <br>

Our validation loss is higher than our training loss, as stated above, which is indicative of over-generalization or overfitting. It occurs when the model learns from the training set in a way that it expects the test set to be the same or similar and becomes ineffective for it. Regularization is done to correct or prevent overfitting and in our model we regularize by dividing the product of learning rate and delta weights by the total number of records. <br>

## Predictions by the model - <br>
![predictions](https://github.com/shahzina/Bikeshare/blob/master/images/predictions.png)
