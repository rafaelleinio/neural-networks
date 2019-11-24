# MLP Project
Author: Rafael Leiniö

Neural Networks Postgraduate class (2019) - National Institute of Space Research (INPE) - Prof. Dr. Marcos Gonçalves Quiles

# Introduction
Multilayer perceptron (MLP) is a neural network similar to simple perceptron networks, but has more than one layer of neurons in the hidden layers. Is use in problems that are not easily linearly separable. Learning in this type of network is usually done through the error propagation algorithm, but there are other algorithms for this purpose. Each network layer has a specific activation function. The output layer receives stimulation from the last hidden layer and builds the response.

![](https://elogeel.files.wordpress.com/2010/05/050510_1627_multilayerp1.png?w=700)

The objective of this project is to test MLP, building networks of different sizes and testing different hyper-parameters in 3 classification datasets. 

# Experiments
There is 3 notebooks in this folder with the implementation of the experiments, one for each dataset. The MLP specification parameters tested in the notebooks are the following:

- Fixed parameters (were the same for all tests):
    - **Input** Layer: specific of each dataset
    - **Output Layer**: specific of each dataset
    - **Activation Function**: ReLU in hidden layers and Softmax in output Layer
    - **Loss function**: Mean Square Error (as requested in the activity)
    - **Epochs**: 300
    - **Batch size**: 25

- Variable parameters (all the combinations were tested):
    - **Hidden Layers**: 2x4, 2x32 and 2x128
    - **Momentum Beta**: 0.8, 0.9 and 0.99
    - **L2 regularizer**: 0.1, 0.01 and 0.001

The models were built from all the combinations of the parameters. Each dataset was split into training and validation subsets by the proportion of 85% and 15% respectively. All the models were trained and then validated. For this experiment it was calculated a ranking order by the accuracy over the validation subset, showing the best models for each dataset.

Finally it was show the effect of different Momentum beta and L2 regularizer values in the training phase by analyzing the loss curve through the training epochs.

# Datasets
- [Iris Data Set](https://archive.ics.uci.edu/ml/datasets/Iris)
- [Breast Cancer Wisconsin (Diagnostic) Data Set](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- [Pima Indians Diabetes Database](https://www.kaggle.com/uciml/pima-indians-diabetes-database)


