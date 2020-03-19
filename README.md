# Neural Network (Backpropagation)

This is an implementation of a backpropagation based neural network in Python. It is very rudimentary and moreso a proof of concept and an exercise in neural networks than anything fully fleshed out.

Neural networks are a type of supervised learning where a network structure will learn over each iteration, based on the inputs and number of outputs. It's biological in nature, roughly simulating neurons and neural synapses in the brain. Provided an input and a classification, the network goes through each layer imprinting an error over expected, adjusting itself by means of synapse weights, and repeating the process until the error is diminished. In this, the network is trained to recognize and classify novel data.

While made for the MNIST Digit data set, it can accept any data in a correct format. The network structure is initialized based on the input data, deciding autonomously how many input and output neurons in those layers. The hidden layer structure, however, is a user defined parameter.

# Dependencies

- pandas
- numpy
- Python (3.6+)
- GNU/Linux

`pandas` has subdependencies which this repository also uses. `python3 -m pip install pandas` should install everything this repository needs.

# Execution

You can clone these files to your computer with the below:

` $ git clone https://github.com/stratzilla/backprop-neural-network`

Execute the script as the below:

` $ ./backprop_nn.py <Type> <H> <LR> <MR> <E> <S>`

Where the arguments are as below:

```
 <Type> -- type of activation function:
        -- "LOG" - logistic sigmoid
        -- "TANH" - hyperbolic tanget
 <H> -- hidden layer structure
     -- eg. "15-10" means two layers of 15 and 10 neurons each
 <LR> -- learning rate [0.00..10.00]
 <MR> -- momentum rate [0.00..10.00]
 <E> -- the number of epochs
 <S> -- proportion of examples to use [0.00..1.00]
```

Using no arguments will remind the user of this. If the arguments are appropriate, the output to console will be the accuracy and mean squared error per epoch, alongside the network parameters.

# Data

The data included is the MNIST Digit set, consisting of 7,000 examples of training data and 4,000 examples of testing data, equally split between digits 0-9.

`train.csv` and `test.csv` have already been preprocessed to work with the program; any other data may need to be preprocessed. Data is in the form of continuous features (0.00-1.00) with a classification in the final column. The network can accept any data in this format and will adapt the input and output layers accordingly.
