# GNG Project
> Author: Rafael Leiniö
> Neural Networks Postgraduate Class - National Institute of Space Research (INPE) - Prof. Dr. Marcos Gonçalves Quiles

# Introduction
Growing Neural Gas (GNG) is an artificial neural network, inspired by the self-organizing map and introduced in 1991 by Thomas Martinetz and Klaus Schulten. GNG is a competitive model that is designed to learn and represent topology. Different from SOM this model does not require any initial definition of the complete architecture, as the name suggest is an iterative algorithm that will "grow" adding more neurons and connections overtime filling the topology of the data.

![](https://demogng.de/JavaPaper/img304.gif)

The objective of this project is to test GNG. Several models were built varying edge time, time for adding new neurons and maximum number of neurons, checking the results of these variations on the learned topology.

# Experiments

Three different artificial datasets were used to train the models. They are simple datasets with just 2 features, but this enables an easily understanding of the process of learning the topology.

There are 3 notebooks in this folder with the implementation of the experiments, one for each dataset. The GNG specification parameters tested in the notebooks are the following:

Fixed parameters (were the same for all tests):
* n_start_nodes = 2
* step = 0.1
* neighbour_step = 0.001
* min_distance_for_update = 0.2
* Epochs = 400

Variable parameters:
* Test 1 - Default parameters:
    * max_edge_age = 50
    * max_nodes = 100
    * n_iter_before_neuron_added = 100
* Test 2:
    * max_edge_age = 50
    * max_nodes = 300
    * n_iter_before_neuron_added = 25
* Test 3:
    * max_edge_age = 10
    * max_nodes = 100
    * n_iter_before_neuron_added = 100
* Test 4:
    * max_edge_age = 25
    * max_nodes = 300
    * n_iter_before_neuron_added = 50

For all the test was generated an image of the final learned topology and an iterative GIF showing the evolution of the network through the epochs.

# Datasets
- [Generated Datasets](https://scikit-learn.org/stable/datasets/index.html#generated-datasets)

# Spoiler - evolution of the models:

![](https://media.giphy.com/media/d8PphcE1kujyZxknEp/giphy.gif =3000x)
