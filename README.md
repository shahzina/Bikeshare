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


## Predictions by the model - <br>
![predictions](https://github.com/shahzina/Bikeshare/blob/master/images/predictions.png)
