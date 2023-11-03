# Optimizing-Neural-Networks-Backpropagation-and-Gradient-Based-Optimization-Methods

## Project Description

The BackPropagation project focuses on implementing backpropagation in a computational graph. It involves various tasks, such as loading data, implementing forward propagation, and optimizing weights using different optimizers. The primary goal is to learn and understand backpropagation while working on a practical example.

## Project Tasks

### Task 1: Implementing Backpropagation and Gradient Checking

In this task, you'll implement backpropagation and gradient checking. The computational graph consists of input features and weights, and you'll calculate the loss and gradients.

- **Forward Propagation**: Implement the forward propagation function, which computes intermediate values, including the loss.
- **Backward Propagation**: Create a function for backward propagation to compute gradients for each weight.

### Task 2: Optimizers

As part of this task, you will implement three different weight update methods using the same computational graph.

- **Vanilla Update**: Implement weight updates using the vanilla gradient descent method.
- **Momentum Update**: Implement weight updates using the momentum method.
- **Adam Update**: Implement weight updates using the Adam optimizer.

## Getting Started

### Loading Data

The project begins with loading data from the 'data.pkl' file and preparing it for use.

```
import pickle
import numpy
# Load the data
with open('data.pkl', 'rb') as f:
    data = pickle.load(f)
X = data[:, :5]
y = data[:, -1]
```

### Computational Graph
The computational graph consists of input features [f1, f2, f3, f4, f5] and 9 weights [w1, w2, w3, w4, w5, w6, w7, w8, w9]. The final output of this graph is a value L, which is computed as (Y - Y')^2.

### Backward Propagation
In this project, you'll implement the backpropagation algorithm to calculate gradients for each weight. The grader functions are provided to validate the correctness of your implementation.

### Gradient Checking
To ensure that backpropagation is correctly implemented, the project includes a gradient checking function. This helps validate the accuracy of the computed gradients.

### Optimization Methods
Three optimization methods are implemented in this project:

- Vanilla Update: Updates weights using vanilla gradient descent.
- Momentum Update: Updates weights using momentum.
- Adam Update: Updates weights using the Adam optimizer.

### How to Run
- Load the data using the provided code.
- Implement the forward and backward propagation functions as per the project description.
- Run the optimization methods (Vanilla, Momentum, Adam) to update the weights.
- Observe the loss values for each optimization method and analyze the comparisons.

### Comparison of Optimizers
The project provides a comparison of the minimum and maximum loss values for the three optimization methods:
| Optimizer | Minimum Loss | Maximum Loss |
|-----------|--------------|--------------|
| Vanilla   | 4.4215e-06   | 0.5983       |
| Momentum  | 1.1414e-07   | 0.4135       |
| Adam      | 2.1679e-07   | 0.0059       |

### Graphical Comparison
The following plot illustrates the loss values for each optimizer over 100 epochs:
```
# Plot the loss values
plt.plot(epochs, momentum_losses, 'r', label='Momentum update', marker='o')
plt.plot(epochs, adam_losses, 'b', label='Adam update', marker='o')
plt.plot(epochs, vanilla_losses, 'g', label='Vanilla update', marker='o')
plt.title 'Comparison of different weight optimizers'
plt.xlabel 'Epoch'
plt.ylabel 'Loss'
plt.legend()
plt.xticks(epochs)
plt.show()
```
