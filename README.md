# Vanishing Gradient in Deep Learning: An Analysis and Solutions

This project explores the Vanishing Gradient Problem, a common issue in deep neural networks, particularly in Multi-Layer Perceptrons (MLPs) with many layers. The project analyzes the problem, investigates its causes, and experiments with various strategies to mitigate its effects, enhancing the learning efficiency of deep neural networks.

## Key Concepts

### What is Vanishing Gradient?

Vanishing Gradient occurs when the gradients used to update the weights during backpropagation become exceedingly small in deeper layers of the network. This causes:
- Minimal weight updates in earlier layers.
- Slow learning or even stagnation in training.
- Difficulty in propagating information through the network.

### Symptoms of Vanishing Gradient

- Weights of layers near the output layer change significantly, while those near the input layer remain almost unchanged.
- The model experiences stalled training early in the process.
- Weight values tend to concentrate around zero, reducing the network's ability to transfer meaningful signals.

### Causes

The problem arises primarily due to the chain rule in backpropagation. The gradient diminishes exponentially as it propagates through multiple layers, especially when activation functions like Sigmoid or Tanh are used.

## Objectives

1. Simulate the Vanishing Gradient Problem using a basic MLP model with:
    - Sigmoid activation function.
    - A deep network structure.
    - Poor weight initialization.
2. Mitigate the Issue: Implement and evaluate various strategies to address the vanishing gradient problem and compare their effectiveness.

## Solutions Explored

The project investigates the following strategies:

1. **Weight Initialization**: Modify weight initialization to amplify gradients and reduce vanishing effects.

2. **Improved Activation Functions**: Test advanced activation functions like ReLU that are less prone to saturation.

3. **Modern Optimizers**: Experiment with optimizers like Adam for better convergence.

4. **Normalization Techniques**: Introduce techniques such as Batch Normalization to stabilize outputs across layers.

5. **Skip Connections**: Incorporate skip connections (e.g., ResNet-style architecture) to create direct gradient paths.

6. **Layer-wise Fine-Tuning**: Train layers sequentially to prevent deeper layers from causing vanishing gradients in earlier layers.

7. **Gradient Normalization**: Normalize gradients during backpropagation to maintain reasonable values.

## Installation

1. Clone the repository:

```sh
git clone https://github.com/linhlinhle997/vanishing-gradient-mlp.git
cd vanishing-gradient-mlp
```

2. Install dependencies:

```sh
pip install -r requirements.txt
```

3. Run Experiments

Open the `vanishing_gradient_mlp.ipynb` notebook and execute each cell to observe the experiments and results.

## Results

- Comparative analysis of solutions with visualizations of gradient behavior, loss trends, and accuracy improvements.
- Detailed discussion on the strengths, weaknesses, and applicability of each method.
