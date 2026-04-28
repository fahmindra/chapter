---
layout: chapter
title: "Partial Derivatives"
chapter: "Derivatives"
chapter_order: 16
section_order: 8
permalink: /materi-algebrica/derivatives/partial-derivatives/
---

## Definition

Partial derivatives generalise the concept of the [derivative](https://algebrica.org/derivatives) to functions of several real variables. For a [function](https://algebrica.org/functions/) of a single variable, the derivative quantifies the rate of change of the function value along the sole available direction. In the context of multiple variables, it is necessary to specify the variable with respect to which the rate of change is computed, while holding all other variables constant. Formally:

- Let $f : A \subseteq \mathbb{R}^{n} \rightarrow \mathbb{R}$ denote a function defined on an open set $A$.
- Let $x_{0} = \left(\right. x_{1}^{0} , \ldots , x_{n}^{0} \left.\right) \in A$ be a fixed point.

The partial derivative of $f$ with respect to the variable $x_{i}$ at $x_{0}$ is defined as the following limit:

$$\frac{\partial f}{\partial x_{i}} \left(\right. x_{0} \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. x_{1}^{0} , \ldots , x_{i}^{0} + h , \ldots , x_{n}^{0} \left.\right) - f \left(\right. x_{0} \left.\right)}{h}$$

This definition applies whenever the [limit](https://algebrica.org/limits/) exists and is finite. In such cases, $f$ is said to be partially differentiable with respect to $x_{i}$ at $x_{0}$.

---

The notation is analogous to that of the ordinary derivative:

$$f^{'} \left(\right. c \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$

For the partial derivative the symbol $\partial$ indicates that only one coordinate is varied. Common alternative notations include $\partial_{x_{i}} f \left(\right. x_{0} \left.\right)$ and $f_{x_{i}} \left(\right. x_{0} \left.\right)$. From a computational perspective, evaluating $\partial f / \partial x_{i}$ involves differentiating $f$ with respect to $x_{i}$ using standard calculus rules, while treating all other variables as constants.

---

Consider the setting: $f : A \subseteq \mathbb{R}^{2} \rightarrow \mathbb{R}$, where $A$ is open and $\left(\right. x_{0} , y_{0} \left.\right) \in A$. The two partial derivatives are defined as:

$$\frac{\partial f}{\partial x} \left(\right. x_{0} , y_{0} \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. x_{0} + h , y_{0} \left.\right) - f \left(\right. x_{0} , y_{0} \left.\right)}{h}$$

$$\frac{\partial f}{\partial y} \left(\right. x_{0} , y_{0} \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. x_{0} , y_{0} + h \left.\right) - f \left(\right. x_{0} , y_{0} \left.\right)}{h}$$

Geometrically, $\frac{\partial f}{\partial x} \left(\right. x_{0} , y_{0} \left.\right)$ represents the slope of the curve formed by intersecting the graph of $f$ with the plane $y = y_{0}$, while $\frac{\partial f}{\partial y} \left(\right. x_{0} , y_{0} \left.\right)$ corresponds to the slope of the intersection with the plane $x = x_{0}$. Along each of these curves, $f$ becomes a function of a single real variable.

![Partial derivatives.](https://algebrica.org/wp-content/uploads/resources/images/partial-derivatives-1.png "Partial derivatives.")

For example, consider the function of two variables:

$$f \left(\right. x , y \left.\right) = x^{3} y^{2} - sin ⁡ \left(\right. x y \left.\right)$$

Treating $y$ and $x$ as constants in turn yields:

$$\frac{\partial f}{\partial x} & = 3 x^{2} y^{2} - y cos ⁡ \left(\right. x y \left.\right) \\ \frac{\partial f}{\partial y} & = 2 x^{3} y - x cos ⁡ \left(\right. x y \left.\right)$$

###### The first expression results from differentiating $f$ with respect to $x$ while keeping $y$ constant. The second expression is obtained by differentiating with respect to $y$ while keeping $x$ constant. In both cases, standard differentiation rules such as the power rule and [chain rule](https://algebrica.org/the-derivative-of-a-composite-function/) apply as they do in the single-variable context.

## Example 1

To illustrate the process of partial differentiation, consider a function of three variables instead of two. The inclusion of an additional variable does not introduce conceptual complexity and the procedure remains unchanged. This example clarifies how each variable is treated independently, with the remaining variables regarded as constants. For example, let us compute the partial derivatives of the following function:

$$f \left(\right. x , y , z \left.\right) = e^{x^{2} z} ln ⁡ \left(\right. 1 + y^{2} z \left.\right)$$

Differentiation with respect to $x$ is straightforward. Here, $y$ and $z$ are treated as constants, so $ln ⁡ \left(\right. 1 + y^{2} z \left.\right)$ factors out, and the chain rule is applied to $e^{x^{2} z}$ with the inner function $x^{2} z$:

$$\frac{\partial f}{\partial x} = 2 x z e^{x^{2} z} ln ⁡ \left(\right. 1 + y^{2} z \left.\right)$$

The derivative with respect to $y$ follows a similar structure but operates on the other factor. In this case, $e^{x^{2} z}$ serves as the constant multiplier, and the chain rule is applied to $ln ⁡ \left(\right. 1 + y^{2} z \left.\right)$ with the inner function $1 + y^{2} z$:

$$\frac{\partial f}{\partial y} = \frac{2 y z e^{x^{2} z}}{1 + y^{2} z}$$

The derivative with respect to $z$ is the most complex of the three cases. Since neither factor is constant in $z$, the product rule must be applied. The exponential term $e^{x^{2} z}$ yields $x^{2} e^{x^{2} z}$ as its derivative, while $ln ⁡ \left(\right. 1 + y^{2} z \left.\right)$ yields $\frac{y^{2}}{1 + y^{2} z}$:

$$\frac{\partial f}{\partial z} = x^{2} e^{x^{2} z} ln ⁡ \left(\right. 1 + y^{2} z \left.\right) + \frac{y^{2} e^{x^{2} z}}{1 + y^{2} z}$$

## Higher-order partial derivatives

If the partial derivatives are differentiable functions on $A$, they can be further differentiated with respect to any variable $x_{j}$, resulting in second-order partial derivatives. For a function of two variables $f \left(\right. x , y \left.\right)$, there are four possible second-order partial derivatives:

$$\frac{\partial^{2} f}{\partial x^{2}} \frac{\partial^{2} f}{\partial y^{2}} \frac{\partial^{2} f}{\partial y \partial x} \frac{\partial^{2} f}{\partial x \partial y}$$

The last two are called mixed partial derivatives. They differ in the sequence of differentiation:

- In $\frac{\partial^{2} f}{\partial y \partial x}$, differentiation is first performed with respect to $x$, followed by differentiation with respect to $y$.
- In $\frac{\partial^{2} f}{\partial x \partial y}$, the order of differentiation is reversed: differentiation is first performed with respect to $y$, then with respect to $x$.

---

Consider the function $f \left(\right. x , y \left.\right) = x^{3} sin ⁡ \left(\right. x y \left.\right)$ in order to compute all four second-order partial derivatives. Begin by determining the first-order partial derivatives:

$$\frac{\partial f}{\partial x} & = 3 x^{2} sin ⁡ \left(\right. x y \left.\right) + x^{3} y cos ⁡ \left(\right. x y \left.\right) \\ \frac{\partial f}{\partial y} & = x^{4} cos ⁡ \left(\right. x y \left.\right)$$

The four second-order derivatives are obtained by differentiating each first-order derivative with respect to the relevant variable. Differentiating $\frac{\partial f}{\partial x}$ with respect to $x$ requires application of the product rule twice:

$$\frac{\partial^{2} f}{\partial x^{2}} & = 6 x sin ⁡ \left(\right. x y \left.\right) + 3 x^{2} y cos ⁡ \left(\right. x y \left.\right) + 3 x^{2} y cos ⁡ \left(\right. x y \left.\right) - x^{3} y^{2} sin ⁡ \left(\right. x y \left.\right) \\ & = 6 x sin ⁡ \left(\right. x y \left.\right) + 6 x^{2} y cos ⁡ \left(\right. x y \left.\right) - x^{3} y^{2} sin ⁡ \left(\right. x y \left.\right)$$

Differentiating $\frac{\partial f}{\partial y}$ with respect to $y$ is more straightforward due to the simpler structure:

$$\frac{\partial^{2} f}{\partial y^{2}} = - x^{5} sin ⁡ \left(\right. x y \left.\right)$$

For the mixed derivatives, differentiating $\frac{\partial f}{\partial x}$ with respect to $y$ yields:

$$\frac{\partial^{2} f}{\partial y \partial x} & = 3 x^{2} \cdot x cos ⁡ \left(\right. x y \left.\right) + x^{3} cos ⁡ \left(\right. x y \left.\right) - x^{3} y \cdot x sin ⁡ \left(\right. x y \left.\right) \\ & = 4 x^{3} cos ⁡ \left(\right. x y \left.\right) - x^{4} y sin ⁡ \left(\right. x y \left.\right)$$

Similarly, differentiating $\frac{\partial f}{\partial y}$ with respect to $x$ yields:

$$\frac{\partial^{2} f}{\partial x \partial y} = 4 x^{3} cos ⁡ \left(\right. x y \left.\right) - x^{4} y sin ⁡ \left(\right. x y \left.\right)$$

## Schwarz’s theorem

Schwarz’s theorem addresses whether the order of differentiation affects the computation of mixed partial derivatives. A fundamental result in analysis establishes that, under appropriate regularity conditions, the order does not matter. Specifically, the Schwarz theorem states the following.

Let $f : A \subseteq \mathbb{R}^{2} \rightarrow \mathbb{R}$ be a function for which the mixed partial derivatives exist on $A$ and are [continuous](https://algebrica.org/continuous-functions/) at a point $\left(\right. x_{0} , y_{0} \left.\right) \in A$. Then these mixed derivatives are equal at that point:
$$\frac{\partial^{2} f}{\partial y \partial x} \left(\right. x_{0} , y_{0} \left.\right) = \frac{\partial^{2} f}{\partial x \partial y} \left(\right. x_{0} , y_{0} \left.\right)$$

---

Continuity of the mixed partial derivatives is the essential hypothesis in Schwarz’s theorem. There are functions for which both mixed derivatives exist but are [discontinuous](https://algebrica.org/discontinuities-of-real-functions/), resulting in different values at certain points. A classical counterexample is provided below.

$$f \left(\right. x , y \left.\right) = \left{\right. x y \frac{x^{2} - y^{2}}{x^{2} + y^{2}} & \left(\right. x , y \left.\right) \neq \left(\right. 0 , 0 \left.\right) \\ 0 & \left(\right. x , y \left.\right) = \left(\right. 0 , 0 \left.\right)$$

Both mixed partial derivatives exist at the origin and can be computed directly from their definitions. To compute $\frac{\partial^{2} f}{\partial y \partial x} \left(\right. 0 , 0 \left.\right)$, first evaluate

$$\frac{\partial f}{\partial x} \left(\right. 0 , y \left.\right) & = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. h , y \left.\right) - f \left(\right. 0 , y \left.\right)}{h} \\ & = \underset{h \rightarrow 0}{lim} \frac{h y \frac{h^{2} - y^{2}}{h^{2} + y^{2}}}{h} \\ & = \underset{h \rightarrow 0}{lim} y \frac{h^{2} - y^{2}}{h^{2} + y^{2}} \\ & = - y$$

Next, differentiating with respect to $y$ at the origin:

$$\frac{\partial^{2} f}{\partial y \partial x} \left(\right. 0 , 0 \left.\right) = \frac{\partial}{\partial y} \left(\right. - y \left.\right) \left|\right._{y = 0} = - 1$$

A similar calculation in the reverse order yields:

$$\frac{\partial f}{\partial y} \left(\right. x , 0 \left.\right) = x \frac{\partial^{2} f}{\partial x \partial y} \left(\right. 0 , 0 \left.\right) = \frac{\partial}{\partial x} \left(\right. x \left.\right) \left|\right._{x = 0} = + 1$$

Therefore, the two mixed derivatives take opposite values at the origin confirming that the conclusion of Schwarz’s theorem does not hold when the continuity hypothesis is not satisfied:

$$\frac{\partial^{2} f}{\partial y \partial x} \left(\right. 0 , 0 \left.\right) = - 1 \neq + 1 = \frac{\partial^{2} f}{\partial x \partial y} \left(\right. 0 , 0 \left.\right)$$

## Gradient

If $f : A \subseteq \mathbb{R}^{n} \rightarrow \mathbb{R}$ is partially differentiable with respect to each variable at a point $x_{0} \in A$, the collection of all partial derivatives forms a [vector](https://algebrica.org/vectors/) known as the gradient of $f$ at $x_{0}$. This gradient is denoted by $\nabla f \left(\right. x_{0} \left.\right)$ or $grad f \left(\right. x_{0} \left.\right)$:

$$\nabla f \left(\right. x_{0} \left.\right) = \left(\right. \frac{\partial f}{\partial x_{1}} \left(\right. x_{0} \left.\right) , \frac{\partial f}{\partial x_{2}} \left(\right. x_{0} \left.\right) , \ldots , \frac{\partial f}{\partial x_{n}} \left(\right. x_{0} \left.\right) \left.\right) \in \mathbb{R}^{n}$$

The gradient is fundamental in multivariable analysis providing the optimal linear approximation to the variation of $f$ near $x_{0}$, and its direction indicates the direction of steepest ascent. The precise meaning of this linear approximation is clarified in the definition of differentiability below.

###### This geometric property is also the foundation of gradient descent, the iterative optimization algorithm widely used in machine learning to minimize loss functions by moving in the direction opposite to the gradient.

## Differentiability and the total differential

The existence of partial derivatives at a point does not, in general, ensure differentiability. Differentiability is a stronger condition that requires the function to admit a linear approximation at the given point. A function $f : A \subseteq \mathbb{R}^{n} \rightarrow \mathbb{R}$ is differentiable at $x_{0} \in A$ if there exists a linear map $L : \mathbb{R}^{n} \rightarrow \mathbb{R}$ such that:

$$\underset{h \rightarrow 0}{lim} \frac{f \left(\right. x_{0} + h \left.\right) - f \left(\right. x_{0} \left.\right) - L \left(\right. h \left.\right)}{\left|\right. h \left|\right.} = 0$$

The linear map $L$ is uniquely determined and takes the form:

$$L \left(\right. h \left.\right) = \nabla f \left(\right. x_{0} \left.\right) \cdot h$$

Differentiability implies that in a neighbourhood of $x_{0}$, the function admits the following expansion:

$$f \left(\right. x_{0} + h \left.\right) = f \left(\right. x_{0} \left.\right) + \nabla f \left(\right. x_{0} \left.\right) \cdot h + o \left(\right. \left|\right. h \left|\right. \left.\right)$$

In this formula $o \left(\right. \left|\right. h \left|\right. \left.\right)$ denotes a term that vanishes faster than $\left|\right. h \left|\right.$ as $h \rightarrow 0$. The linear map $h \rightarrowtail \nabla f \left(\right. x_{0} \left.\right) \cdot h$ is called the total differential of $f$ at $x_{0}$.

## Jacobian matrix

Consider a function that takes vector values, specifically $f : A \subseteq \mathbb{R}^{n} \rightarrow \mathbb{R}^{m}$ with $f = \left(\right. f_{1} , \ldots , f_{m} \left.\right)$. The partial derivative of each component $f_{k}$ with respect to each variable $x_{j}$ can be computed. The Jacobian matrix of $f$ at $x_{0}$ organises this information and is defined as the $m \times n$ [matrix](https://algebrica.org/matrices/):

$$J_{f} \left(\right. x_{0} \left.\right) = \left(\right. \frac{\partial f_{1}}{\partial x_{1}} \left(\right. x_{0} \left.\right) & \hdots & \frac{\partial f_{1}}{\partial x_{n}} \left(\right. x_{0} \left.\right) \\ \vdots & \ddots & \vdots \\ \frac{\partial f_{m}}{\partial x_{1}} \left(\right. x_{0} \left.\right) & \hdots & \frac{\partial f_{m}}{\partial x_{n}} \left(\right. x_{0} \left.\right) \left.\right)$$

The $k$-th row of $J_{f} \left(\right. x_{0} \left.\right)$ corresponds to the gradient $\nabla f_{k} \left(\right. x_{0} \left.\right)$. When $m = 1$, the Jacobian matrix reduces to a row vector, which is equivalent to the gradient of $f$.

## Directional derivatives

The partial derivative with respect to $x_{i}$ represents a specific instance of the broader concept of the directional derivative, taken in the direction of the $i$-th canonical basis vector $e_{i}$. For any unit vector $v \in \mathbb{R}^{n}$ with $\left|\right. v \left|\right. = 1$, the directional derivative of $f$ at $x_{0}$ in the direction of $v$ is defined as follows:

$$D_{v} f \left(\right. x_{0} \left.\right) = \underset{t \rightarrow 0}{lim} \frac{f \left(\right. x_{0} + t v \left.\right) - f \left(\right. x_{0} \left.\right)}{t}$$

When $f$ is differentiable at $x_{0}$, the following formula holds:

$$D_{v} f \left(\right. x_{0} \left.\right) = \nabla f \left(\right. x_{0} \left.\right) \cdot v = \sum_{i = 1}^{n} \frac{\partial f}{\partial x_{i}} \left(\right. x_{0} \left.\right) v_{i}$$

The dot represents the Euclidean inner product on $\mathbb{R}^{n}$. Selecting $v = e_{i}$ yields $\frac{\partial f}{\partial x_{i}} \left(\right. x_{0} \left.\right)$, which aligns with the original definition of the partial derivative. This formula is valid only when $f$ is differentiable at $x_{0}$, rather than when only the partial derivatives exist.

## The chain rule in multivariable calculus

The chain rule for composite functions is fundamental in multivariable analysis. Suppose $g : U \subseteq \mathbb{R}^{k} \rightarrow \mathbb{R}^{n}$ is differentiable at $t_{0} \in U$, and $f : A \subseteq \mathbb{R}^{n} \rightarrow \mathbb{R}$ is differentiable at $x_{0} = g \left(\right. t_{0} \left.\right) \in A$. The composite function $h = f \circ g$ is then differentiable at $t_{0}$, and its partial derivative with respect to $t_{j}$ is given by.

$$\frac{\partial h}{\partial t_{j}} \left(\right. t_{0} \left.\right) = \sum_{i = 1}^{n} \frac{\partial f}{\partial x_{i}} \left(\right. x_{0} \left.\right) \frac{\partial g_{i}}{\partial t_{j}} \left(\right. t_{0} \left.\right)$$

In matrix notation, this relationship can be expressed as:

$$J_{h} \left(\right. t_{0} \left.\right) = J_{f} \left(\right. x_{0} \left.\right) J_{g} \left(\right. t_{0} \left.\right)$$

This formula represents the product of the Jacobian matrices in the correct order. In the particular case where $k = 1$ and $g \left(\right. t \left.\right)$ defines a curve, the formula reduces to the standard derivative of $h \left(\right. t \left.\right) = f \left(\right. g \left(\right. t \left.\right) \left.\right)$:

$$\frac{d}{d t} f \left(\right. g \left(\right. t \left.\right) \left.\right) \left|\right._{t = t_{0}} = \nabla f \left(\right. g \left(\right. t_{0} \left.\right) \left.\right) \cdot g^{'} \left(\right. t_{0} \left.\right)$$

## Classes of regularity

A function $f$ is said to be of class $C^{1}$ on an open set $A$, denoted $f \in C^{1} \left(\right. A \left.\right)$, if all first-order partial derivatives exist and are continuous on $A$. More generally, $f \in C^{k} \left(\right. A \left.\right)$ if all partial derivatives up to order $k$ exist and are continuous on $A$. The notation $f \in C^{\infty} \left(\right. A \left.\right)$ indicates that $f \in C^{k} \left(\right. A \left.\right)$ for every $k \geq 1$.

- Functions of class $C^{1}$ possess a significant property: continuity of the partial derivatives ensures differentiability. Specifically, if $f \in C^{1} \left(\right. A \left.\right)$, then $f$ is differentiable at every point of $A$. However, this condition is sufficient but not necessary, as there exist differentiable functions whose partial derivatives are not continuous.
- For functions of class $C^{2}$, Schwarz’s theorem applies automatically because the required continuity is assumed. Consequently, the equality of mixed partial derivatives holds throughout $A$.

## The Hessian matrix

Given a function $f : A \subseteq \mathbb{R}^{n} \rightarrow \mathbb{R}$ of class $C^{2}$ defined on an open set $A$, the second-order partial derivatives may be arranged into a single square matrix. The Hessian matrix of $f$ at a point $x_{0} \in A$ is the $n \times n$ symmetric matrix defined as follows:

$$H_{f} \left(\right. x_{0} \left.\right) = \left(\right. \frac{\partial^{2} f}{\partial x_{1}^{2}} \left(\right. x_{0} \left.\right) & \hdots & \frac{\partial^{2} f}{\partial x_{1} \partial x_{n}} \left(\right. x_{0} \left.\right) \\ \vdots & \ddots & \vdots \\ \frac{\partial^{2} f}{\partial x_{n} \partial x_{1}} \left(\right. x_{0} \left.\right) & \hdots & \frac{\partial^{2} f}{\partial x_{n}^{2}} \left(\right. x_{0} \left.\right) \left.\right)$$

The entry in position $\left(\right. j , k \left.\right)$ is given by:

$$\frac{\partial^{2} f}{\partial x_{j} \partial x_{k}} \left(\right. x_{0} \left.\right)$$

Because $f \in C^{2} \left(\right. A \left.\right)$, Schwarz’s theorem ensures that all mixed partial derivatives are equal, so the Hessian is symmetric:

$$H_{f} \left(\right. x_{0} \left.\right) = H_{f} \left(\right. x_{0} \left.\right)^{T}$$

The Hessian is fundamental in the second-order analysis of $f$. At a critical point $x_{0}$ where $\nabla f \left(\right. x_{0} \left.\right) = 0$, the definiteness of $H_{f} \left(\right. x_{0} \left.\right)$ determines the character of the point: if $H_{f} \left(\right. x_{0} \left.\right)$ is positive definite, then $x_{0}$ is a local minimum; if negative definite, a local maximum; if indefinite, a saddle point. This result generalises the second derivative test to functions of several variables, as discussed in the entry on [maximum, minimum, and inflection Points](https://algebrica.org/maximum-minimum-and-inflection-points/).

## Selected references

- **MIT OCW, A. Mattuck**. [Partial Derivatives and Multivariable Calculus](https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/3299372c0b77500ada4ea558fea4db80_MIT18_02SC_MNotes_ta1.pdf)
- **Harvard University, O. Knill**. [Partial Derivatives](https://people.math.harvard.edu/~knill/teaching/summer2012/handouts/week3.pdf)
- **UC Berkeley, N. Srivastava**. [The Multivariable Chain Rule](https://math.berkeley.edu/~nikhil/courses/121a/chain.pdf)
- **UC Berkeley**. [Multivariable Calculus Worksheets](https://math.berkeley.edu/sites/default/files/bulk_6/Math53.Berkeley.pdf)
- **City University of New York, A. Máté**. [On the Equality of Mixed Partial Derivatives](http://www.sci.brooklyn.cuny.edu/~mate/misc/mixedpartial.pdf)
