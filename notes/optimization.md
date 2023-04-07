---
title: optimization
title_custom: true
created: 2023-04-01T05:20:40.736Z
modified: 2023-04-07T22:00:03.690Z
---

## Optimization

**Gradient-based optimization algorithms** are a class of iterative optimization techniques used to find the optimal parameters of a model by minimizing a predefined objective function (often a "loss" or "cost" function). They use the gradient of the function with respect to the model parameters. They update the model parameters iteratively, using the gradient to move the parameters in the direction that minimizes the objective function.

Some popular functions include:

- Gradient Descent (the simplest)
- Stochastic Gradient Descent (SGD)
- Momentum
- AdaGrad
- RMSProp
- Adam (Adaptive Movement Estimation)

**Adam** Adaptive Movement Estimation combines elements of Momentum and RMSProp, adapting the learning rate for each parameter.

Axon treats optimizers as the tuple:

`{init_fn, update_fn}`

where `init_fn` returns the initial optimizer state and `update_fn` scales input gradients.
`init_fn` accepts a model's parameters and attaches state to each.
`update_fn` accepts gradients, optimizer state, and current model parameters and returns updated optimizer state and gradients.

Axon provides the following optimizer functions:

- adabelief
- adagrad
- adam
- adamw (adam with weight decay optimizer)
- lamb
- noisy_sgd
- radam (rectified adam)
- rmsprop
- sgd
- yogi

**Weight Decay**
Weight decay is a regularization technique used to prevent overfitting in machine learning models by adding a penalty term to the objective function. This penalty term is proportional to the magnitude of the weights, encouraging the model to learn smaller weights. In traditional gradient-based optimization algorithms, such as SGD, weight decay can be achieved by subtracting a fraction of the current weight from the weight update step.

**AdamW**
Adam with Weight Decay Optimizer
The main idea behind AdamW is to apply weight decay directly to the weights rather than incorporating it into the gradient update, as done in the standard Adam algorithm.

The update rule for AdamW can be written as:

Compute the gradient g_t for the current mini-batch.
Update the first moment estimate:

$$m_t = \beta_1 * m_{t-1} + (1 - \beta_1) * g_t$$

Update the second moment estimate:

$$v_t = \beta_2 * v_{t-1} + (1 - \beta_2) * (g_t * g_t)$$


Compute the bias-corrected first and second moment estimates:

$$\hat{m}_t = \frac{m_t}{1 - \beta_1^t} \quad \text{and} \quad \hat{v}_t = \frac{v_t}{1 - \beta_2^t}$$


Update the weights with weight decay and the bias-corrected estimates:

```math
{w_t} = (1 - \text{weight\_decay} \cdot \text{lr}) \cdot w_{t-1} - \text{lr} \cdot \hat{m}_t / (\sqrt{\hat{v}_t} + \epsilon)
```

In these algorithms, $m_t$ and $v_t$ are the running averages of the first and second moments of the gradients, updated at each time step t.
$m̂_t$ and $v̂_t$ represent the bias-corrected estimates.
Here, β₁ and β₂ are the exponential decay rates for the first and second moments. 

_In mathematical notation, placing a "hat" (^) over a letter, such as m̂ or v̂, is commonly used to represent an estimate, approximation, or a modified version of the original variable. In the context of optimization algorithms like Adam or AdamW, the "hat" notation is used to denote bias-corrected estimates of the first and second moments (m and v, respectively)._


