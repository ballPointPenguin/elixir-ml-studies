---
title: activation_layers
title_custom: true
created: 2023-04-01T04:54:54.210Z
modified: 2023-04-10T15:40:05.144Z
---

## Activation Layers

**Activation Function**
An activation function's purpose is to introduce non-linearity into the model, allowing the neural network to learn complex patterns and relationships in the data.

**Dense Layer**
A dense layer, particularly in neural networks and deep learning, is a layer in which each neuron is connected to every neuron in the previous layer. It is a "fully connected layer".
As opposed to sparse connections such as in Convolutional or Recurrent Layers.
Dense layers are commonly used in feedforward networks and deep learning models, to perform tasks such as classification, regression, and feature extraction.

**Hyperbolic Tangent (tanh)**
In math, the hyperbolic tangent function (tanh) is the ration of the the hyperbolic sine function (sinh) to the hyperbolic cosine function (cosh):

$$\text{tanh}(x) = \frac{\sinh(x)}{\cosh(x)}$$

Or alternately, expressed using exponential functions:

$$\text{tanh}(x) = \frac{e^{x} - e^{-x}}{e^{x} + e^{-x}}$$

The tanh function has an "S-curve" (hyperbola) and maps inputs to a range between -1 and 1. Properties include:

1. It is an "odd" function, such that $\text{tanh}(-x) = -\text{tanh}(x)$
2. It is smooth and differentiable, with a continuous first derivative.
3. As x approaches ∞, tanh(x) approaches 1, and as x approaches -∞, tanh(x) approaches -1.
4. The derivative of tanh(x) with respect to x is $1 - \text{tanh}^2(x)$.

**Softmax**
Softmax is a popular activation function used for classification problems such as multi-class classification tasks. It can be applied to the final layer to convert the raw output (logits) into a probability distribution across classes.
The softmax function takes an input vector of real numbers and normalizes them so the output values sum is 1.
The formula may be described as:

$$\text{softmax}(x_i) = \frac{\exp(x_i)}{\sum_j \exp(x_j)}$$

Where:
- $x_i$ is the value of the i-th class
- $\text{exp}(x_i)$ is the exponential of the value $x_i%$ (in other words, $e^{(x_i)}$)
- $\sum_j \exp(x_j)$ is the sum of the exponentials of all values in the input vector
- $j$ iterates over all the classes


