# SOM Project
> Author: Rafael Leiniö
> Neural Networks Postgraduate class - National Institute of Space Research (INPE) - Prof. Dr. Marcos Gonçalves Quiles

# Introduction
Self Organizing Maps (SOM) or Kohonen networks, was developed by Teuvo Kohonen in 1982, being considered relatively simple and with the ability to reduce dimensionality of the original features, organizing complex data into clusters according to their relationships. This method only requests input parameters and is ideal for problems where patterns are unknown or undetermined.

![](https://codesachin.files.wordpress.com/2015/11/kohonen1.gif)

The objective of this project is to test SOM, testing models with different sigmas and learning rates. Three classification datasets were tested.

# Experiments
Although SOM networks are for unsupervised learning. Datasets containing the classes were used so that graphs could be plotted showing how the model interpreted and separated the data in the grid map.

There are 3 notebooks in this folder with the implementation of the experiments, one for each dataset. The MLP specification parameters tested in the notebooks are the following:

- Fixed parameters (were the same for all tests):
    - **Input** Layer: specific of each dataset
    - **Grid size**: 32x32 grid map
    - **Neighbor funcion**: Bubble
    - **Learning rate and sigma decay function**: at iteration t: `x = x / (1+t/(max_iterarations/2))`

- Variable parameters (all the combinations were tested):
    - **Sigma (Spread of the neighborhood function)**: 10, 5, 3 and 1
    - **Learning Rate**: 5, 1, 0.1 and 0.01 

The models were built from all the combinations of the parameters. The whole dataset was used for training the model, since is an unsupervised model. For this experiment it was calculated a ranking order by the topological error, showing the best models for each dataset.

Besides topological error and quantization error, it was show the plots:
- U-matrix
- U-matrix with class labels
- Hit map

# Datasets
- [Iris Data Set](https://archive.ics.uci.edu/ml/datasets/Iris)
- [Breast Cancer Wisconsin (Diagnostic) Data Set](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- [Pima Indians Diabetes Database](https://www.kaggle.com/uciml/pima-indians-diabetes-database)



