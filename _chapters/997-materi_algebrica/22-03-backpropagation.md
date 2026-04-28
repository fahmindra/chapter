---
layout: chapter
title: "The Backpropagation Algorithm"
chapter: "Other Topics"
chapter_order: 22
section_order: 3
permalink: /materi-algebrica/other-topics/the-backpropagation-algorithm/
---

general casedeep networksactivation derivativesvanishing gradientgradient reusegradient propagationouter productactivation functionslinear layerslocal derivativesgradient flowreverse mode autodiffbackward passforward passcomputational graphchain rulegradientloss functionbackpropagation definitionpropertiesmechanismfoundations

## What is backpropagation

Training a neural network means finding the values of the parameters, typically weight [matrices](https://algebrica.org/matrices), that minimize a loss function with respect to the training data. The fundamental problem is that even a moderately deep network can contain millions of parameters and computing the [gradient](https://algebrica.org/partial-derivatives/) of the loss with respect to each of them naively would require a number of operations proportional to the square of the network size.

Backpropagation solves this problem by exploiting the compositional structure of the network and the [chain rule](https://algebrica.org/the-derivative-of-a-composite-function/) of differential calculus. In this way it is possible to compute all gradients in a time proportional to that required by a single forward pass through the network.

Intuitively, backpropagation answers the question: by how much should each weight be adjusted in order to reduce the error produced by the network? The answer is contained in the gradient of the loss with respect to every parameter. The algorithm proceeds in two distinct phases.

- In the first, called the forward pass, the input is propagated layer by layer up to the output, and the intermediate values of every computation are stored.
- In the second, the backward pass, one starts from the error committed at the output and propagates it backwards through the network, iteratively computing the gradients with respect to each layer by means of the chain rule.

This mechanism underlies the training of virtually all modern deep learning models, from convolutional networks for computer vision to transformers employed in natural language processing.

> The backpropagation algorithm was formalized in 1986 by David E. Rumelhart, Geoffrey E. Hinton, and Ronald J. Williams in their seminal paper [Learning representations by back-propagating errors (1986)](https://www.nature.com/articles/323533a0). Their work shows that training a neural network can be reduced to a systematic application of the chain rule, enabling the computation of gradients of the loss function with respect to each parameter through local derivative updates.

## The chain rule as theoretical foundation

The computation of gradients in a neural network rests entirely on the [chain rule](https://algebrica.org/the-derivative-of-a-composite-function/). If a variable $Z$ depends on $Y$ and $Y$ depends on $X$, then the [derivative](https://algebrica.org/derivatives/) of $Z$ with respect to $X$ is obtained as follows:

$$\frac{\partial Z}{\partial X} = \frac{\partial Z}{\partial Y} \cdot \frac{\partial Y}{\partial X}$$

This identity is the mechanism that allows to connect the gradient of the loss at the network output to the gradient with respect to any internal parameter, however far from the output it may be. Each layer of the network contributes a local factor to the overall product, and backpropagation exploits this structure so that no quantity is ever recomputed twice.

---

For completeness, it is useful to express the chain rule in its Jacobian form. If $y = g \left(\right. x \left.\right)$ and $z = f \left(\right. y \left.\right)$, then holds:

$$\nabla_{x} z = J_{g} \left(\right. x \left.\right)^{\top} \nabla_{y} z$$

Here $J_{g} \left(\right. x \left.\right)$ denotes the Jacobian matrix of $g$ at $x$, that is, the matrix of all [partial derivatives](https://algebrica.org/partial-derivatives/) of the components of $y$ with respect to the components of $x$. This formulation makes explicit how gradients are propagated backward through vector-valued transformations. For simplicity, this level of generality is not explicitly considered in the example discussed here.

## The computational graph

To make the reasoning precise, it is convenient to describe the computation performed by a neural network by means of a directed computational graph. In this graph, square nodes represent variables (parameters, activations, inputs, outputs) while circular nodes represent operations (matrix multiplication, application of a nonlinearity, computation of the loss). Directed edges indicate the dependencies between variables and operations.

![Neural network.](https://algebrica.org/wp-content/uploads/resources/images/neural-network.png "Neural network.")

> For simplicity, in the example presented below, the effect of bias terms along the backpropagation chain is not explicitly considered, as their contribution follows analogous derivative rules.

---

For example, consider a two-layer fully connected network with an activation function $\phi$ applied element-wise between the two linear layers. The equations describing the forward pass are the following:

$$\mathbf{z} = W^{\left(\right. 1 \left.\right)} \mathbf{x}$$

$$\mathbf{h} = \phi \left(\right. \mathbf{z} \left.\right)$$

$$\mathbf{o} = W^{\left(\right. 2 \left.\right)} \mathbf{h}$$

$$L = ℓ \left(\right. \mathbf{o} , \mathbf{y} \left.\right)$$

In these expressions, $\mathbf{x}$ is the input vector, $W^{\left(\right. 1 \left.\right)}$ and $W^{\left(\right. 2 \left.\right)}$ are the weight matrices of the two layers, $\mathbf{y}$ is the target, and $L$ is the scalar value of the loss. The goal of backpropagation is to compute the gradients $\frac{\partial L}{\partial W^{\left(\right. 1 \left.\right)}}$ and $\frac{\partial L}{\partial W^{\left(\right. 2 \left.\right)}}$, which will then be used by a gradient descent algorithm to update the weights.

> Typically, the problems encountered in practice are not linear in nature, and a model that applies only linear transformations to its input would be fundamentally limited in its expressive power. An activation function is a nonlinear function applied element-wise to the output of a linear layer, whose role is precisely to introduce nonlinearity into the network. Without it, the composition of any number of linear layers would itself reduce to a single linear transformation, making deeper architectures equivalent to a single-layer model. Common choices include the [sigmoid function](https://algebrica.org/sigmoid-function/) $\sigma \left(\right. s \left.\right) = \frac{1}{1 + e^{- s}}$, the [hyperbolic tangent](https://algebrica.org/hyperbolic-tangent-and-cotangent/), and the rectified linear unit $\text{ReLU} \left(\right. s \left.\right) = max \left(\right. 0 , s \left.\right)$.

## Reverse-mode automatic differentiation

The concrete technique by which backpropagation is implemented is called reverse-mode automatic differentiation, or reverse autodiff. The idea is that one traverses the computational graph in reverse order, from the output towards the input, and at each node computes the gradient of the loss with respect to the corresponding variable, accumulating the contributions received from the subsequent layers. The computation always starts from the derivative of the loss with respect to itself, which is trivially equal to one:

$$\frac{\partial L}{\partial L} = 1$$

![Nerual network: backpropagation.](https://algebrica.org/wp-content/uploads/resources/images/neural-network-2.png "Nerual network: backpropagation.")

This initial value constitutes the starting point from which the gradient is propagated backwards through all the nodes of the graph. In the following steps, we trace this propagation in detail, moving from the output layer back to the first set of parameters, and deriving at each stage the gradient that will eventually be used to update the weights.

## Step 1: gradient with respect to the output $\mathbf{o}$

The next node encountered when proceeding backwards is the one that computes the loss from the output $\mathbf{o}$ and the target $\mathbf{y} .$ Applying the chain rule gives:

$$\frac{\partial L}{\partial \mathbf{o}} = \left(\right. \frac{\partial L}{\partial L} \cdot \frac{\partial L}{\partial \mathbf{o}} \left.\right) = \frac{\partial L}{\partial \mathbf{o}}$$

![](https://algebrica.org/wp-content/uploads/resources/images/neural-network-3.png)

This gradient depends on the specific form of the loss function. For a quadratic loss $ℓ \left(\right. \mathbf{o} , \mathbf{y} \left.\right) = \left|\right. \mathbf{o} - \mathbf{y} \left|\right.^{2}$, for instance, one has $\frac{\partial L}{\partial \mathbf{o}} = 2 \left(\right. \mathbf{o} - \mathbf{y} \left.\right)$. The concrete value of $\mathbf{o}$ is available because it was computed and stored during the forward pass.

## Step 2: gradient with respect to $W^{\left(\right. 2 \left.\right)}$

The second linear layer computes $\mathbf{o} = W^{\left(\right. 2 \left.\right)} \mathbf{h}$. To determine the gradient of the loss with respect to the matrix $W^{\left(\right. 2 \left.\right)}$, the chain rule is applied:

$$\frac{\partial L}{\partial W^{\left(\right. 2 \left.\right)}} = \frac{\partial L}{\partial \mathbf{o}} \cdot \frac{\partial \mathbf{o}}{\partial W^{\left(\right. 2 \left.\right)}}$$

![](https://algebrica.org/wp-content/uploads/resources/images/neural-network-4.png)

Since $\mathbf{o} = W^{\left(\right. 2 \left.\right)} \mathbf{h}$ is a linear transformation, the derivative of $\mathbf{o}$ with respect to $W^{\left(\right. 2 \left.\right)}$ applied to the already known gradient produces the following result:

$$\frac{\partial L}{\partial W^{\left(\right. 2 \left.\right)}} = \frac{\partial L}{\partial \mathbf{o}} \mathbf{h}^{\top}$$

The outer product between the gradient vector $\frac{\partial L}{\partial \mathbf{o}} \in \mathbb{R}^{m}$ and the transposed activation vector $\mathbf{h}^{\top} \in \mathbb{R}^{1 \times d}$ returns a matrix of the same dimensions as $W^{\left(\right. 2 \left.\right)}$, as is necessary. Note that the value of $\mathbf{h}$ is available because it was computed and retained during the forward pass.

## Step 3: propagating the gradient towards $\mathbf{h}$

Before being able to ascend to the first layer, it is necessary to compute the gradient of the loss with respect to the activation vector $\mathbf{h}$. Once again the chain rule is applied, exploiting the fact that $\mathbf{o} = W^{\left(\right. 2 \left.\right)} \mathbf{h}$:

$$\frac{\partial L}{\partial \mathbf{h}} = \left(\left(\right. \frac{\partial \mathbf{o}}{\partial \mathbf{h}} \left.\right)\right)^{\top} \frac{\partial L}{\partial \mathbf{o}} = \left(\left(\right. W^{\left(\right. 2 \left.\right)} \left.\right)\right)^{\top} \frac{\partial L}{\partial \mathbf{o}}$$

![](https://algebrica.org/wp-content/uploads/resources/images/neural-network-5.png)

The transpose of $W^{\left(\right. 2 \left.\right)}$ arises naturally in the computation of the gradient with respect to the input of a linear transformation, and this is the mechanism that allows the error signal to propagate from the output towards the input of the network.

## Step 4: gradient through the activation function

The next node in the graph, proceeding further backwards, is the one that applies the activation function $\phi$ element-wise, computing $\mathbf{h} = \phi \left(\right. \mathbf{z} \left.\right)$. Since $\phi$ acts separately on each component, its derivative is diagonal and the gradient propagates as follows:

$$\frac{\partial L}{\partial \mathbf{z}} = \frac{\partial L}{\partial \mathbf{h}} \bigodot \phi^{'} \left(\right. \mathbf{z} \left.\right)$$

![](https://algebrica.org/wp-content/uploads/resources/images/neural-network-6.png)

Here $\bigodot$ denotes the element-wise product and $\phi^{'} \left(\right. \mathbf{z} \left.\right)$ is the [vector](https://algebrica.org/vectors/) containing the values of the derivative of $\phi$ evaluated at the points $z_{1} , z_{2} , \ldots , z_{d}$ stored during the forward pass. This formula highlights an important aspect: if the derivative of the activation function is systematically small, the gradient attenuates at every layer until it vanishes in the deepest layers. This phenomenon is known as the vanishing gradient problem and is one of the reasons why the choice of activation function has important consequences for the training of deep networks.

## The vanishing gradient problem

The analysis above shows that every time the gradient passes through a layer with activation function $\phi$, it is multiplied by $\phi^{'} \left(\right. \mathbf{z} \left.\right)$. In a network with $n$ layers, the gradient with respect to the parameters of the first layer contains a product of $n$ such factors. If $\phi^{'}$ is systematically less than one in absolute value, this product decreases exponentially with $n$, making the gradient negligible and rendering the update of the weights in the earliest layers effectively impossible. The sigmoid function is a particularly unfavorable example in this respect. It has the form:

$$\sigma \left(\right. s \left.\right) = \frac{1}{1 + e^{- s}}$$

Its derivative satisfies $\sigma^{'} \left(\right. s \left.\right) \leq \frac{1}{4}$ everywhere. In a deep network, the repeated multiplication of these factors causes the gradient to decay exponentially with depth, so the earliest layers receive a signal that is a small fraction of what was computed at the output. Learning in those layers becomes extremely slow or entirely ineffective.

---

The ReLU function was introduced precisely to mitigate this problem:
$$\text{ReLU} \left(\right. s \left.\right) = max \left(\right. 0 , s \left.\right)$$
Its derivative equals one for all positive values of the argument, which avoids the systematic attenuation of the gradient along the direction of activated neurons.

## Step 5: gradient with respect to $W^{\left(\right. 1 \left.\right)}$

The last parametric node encountered when ascending the graph is the multiplication $\mathbf{z} = W^{\left(\right. 1 \left.\right)} \mathbf{x}$. The gradient with respect to $W^{\left(\right. 1 \left.\right)}$ is computed with the same scheme already used for $W^{\left(\right. 2 \left.\right)}$:

$$\frac{\partial L}{\partial W^{\left(\right. 1 \left.\right)}} = \frac{\partial L}{\partial \mathbf{z}} \mathbf{x}^{\top}$$

![](https://algebrica.org/wp-content/uploads/resources/images/neural-network-7.png)

Here again the gradient has the same shape as the weight matrix, and is expressed as the outer product between the error signal propagated up to this point and the input vector $\mathbf{x}$, also available from the forward pass.

## Summary of the computational flow

The entire procedure can be outlined as follows. During the forward pass, $\mathbf{z}$, $\mathbf{h}$, $\mathbf{o}$ and $L$ are computed in sequence, with intermediate values stored. During the backward pass, the following gradients are computed in reverse order:

$$\frac{\partial L}{\partial L} = 1 \\ \downarrow \\ \frac{\partial L}{\partial \mathbf{o}} = \frac{\partial ℓ \left(\right. \mathbf{o} , \mathbf{y} \left.\right)}{\partial \mathbf{o}} \\ \downarrow \\ \frac{\partial L}{\partial W^{\left(\right. 2 \left.\right)}} = \frac{\partial L}{\partial \mathbf{o}} \mathbf{h}^{\top} \\ \downarrow \\ \frac{\partial L}{\partial \mathbf{h}} = \left(\left(\right. W^{\left(\right. 2 \left.\right)} \left.\right)\right)^{\top} \frac{\partial L}{\partial \mathbf{o}} \\ \downarrow \\ \frac{\partial L}{\partial \mathbf{z}} = \frac{\partial L}{\partial \mathbf{h}} \bigodot \phi^{'} \left(\right. \mathbf{z} \left.\right) \\ \downarrow \\ \frac{\partial L}{\partial W^{\left(\right. 1 \left.\right)}} = \frac{\partial L}{\partial \mathbf{z}} \mathbf{x}^{\top}$$

Each of these gradients depends exclusively on quantities already computed in previous steps, which makes the algorithm computationally efficient: every intermediate value is computed once and then reused as many times as necessary. The total number of operations is of the same order of magnitude as the forward pass, regardless of the depth of the network.

> The condition that makes backpropagation possible is the differentiability of all operations in the graph. For activation functions that are not differentiable everywhere, such as ReLU, the subgradient is adopted in practice at the point of non-differentiability, and the algorithm continues to work correctly in the context of stochastic training.

## The general case

The two-layer example developed above generalises directly to a network of arbitrary depth. Consider a network with $n$ weight matrices $W^{\left(\right. 1 \left.\right)} , \ldots , W^{\left(\right. n \left.\right)}$ and activation functions $\phi^{\left(\right. 1 \left.\right)} , \ldots , \phi^{\left(\right. n - 1 \left.\right)}$ applied between successive layers. Denoting the pre-activation at layer $k$ as $\mathbf{z}^{\left(\right. k \left.\right)}$ and the post-activation as $\mathbf{h}^{\left(\right. k \left.\right)}$, the forward pass computes, for $k = 1 , \ldots , n$:

$$\mathbf{z}^{\left(\right. k \left.\right)} = W^{\left(\right. k \left.\right)} \mathbf{h}^{\left(\right. k - 1 \left.\right)}$$
$$\mathbf{h}^{\left(\right. k \left.\right)} = \phi^{\left(\right. k \left.\right)} \left(\right. \mathbf{z}^{\left(\right. k \left.\right)} \left.\right)$$

In this case$\mathbf{h}^{\left(\right. 0 \left.\right)} = \mathbf{x}$ by convention. The backward pass then propagates the gradient from layer $n$ down to layer $1$. Given the gradient $\frac{\partial L}{\partial \mathbf{h}^{\left(\right. k \left.\right)}}$ arriving at layer $k$, the three local
updates are the following:

$$\frac{\partial L}{\partial \mathbf{z}^{\left(\right. k \left.\right)}} = \frac{\partial L}{\partial \mathbf{h}^{\left(\right. k \left.\right)}} \bigodot \left(\left(\right. \phi^{\left(\right. k \left.\right)} \left.\right)\right)^{'} \left(\right. \mathbf{z}^{\left(\right. k \left.\right)} \left.\right) \\ \downarrow \\ \frac{\partial L}{\partial W^{\left(\right. k \left.\right)}} = \frac{\partial L}{\partial \mathbf{z}^{\left(\right. k \left.\right)}} \left(\left(\right. \mathbf{h}^{\left(\right. k - 1 \left.\right)} \left.\right)\right)^{\top} \\ \downarrow \\ \frac{\partial L}{\partial \mathbf{h}^{\left(\right. k - 1 \left.\right)}} = \left(\left(\right. W^{\left(\right. k \left.\right)} \left.\right)\right)^{\top} \frac{\partial L}{\partial \mathbf{z}^{\left(\right. k \left.\right)}}$$

The third equation propagates the gradient to the layer below, making the recursion self-sustaining. Starting from $\frac{\partial L}{\partial \mathbf{h}^{\left(\right. n \left.\right)}} = \frac{\partial L}{\partial \mathbf{o}}$ and iterating from $k = n$ down to $k = 1$, one recovers all the gradients needed to update every weight matrix in the network.
