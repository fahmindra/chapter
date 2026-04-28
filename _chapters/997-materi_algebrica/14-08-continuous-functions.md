---
layout: chapter
title: "Continuous Functions"
chapter: "Functions"
chapter_order: 14
section_order: 8
permalink: /materi-algebrica/functions/continuous-functions/
---

## Continuous function at a point

The concept of continuity of a [function](https://algebrica.org/functions) is used to determine whether the function behaves predictably near a point, without jumps, holes, or abrupt changes. Formally, a function $y = f \left(\right. x \left.\right)$ is said to be continuous at a point $x_{0}$ if the following [limit](https://algebrica.org/limits) holds:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right)$$

In other words, this means that the limit of the function as $x$ approaches $x_{0}$ exists and is finite, and that this limit is equal to the value of the function at $x_{0}$. For example, the function $f \left(\right. x \left.\right) = sin ⁡ \left(\right. x \left.\right)$ is continuous on all of $\mathbb{R}$. At every point $x_{0} \in \mathbb{R}$, the limit of $sin ⁡ \left(\right. x \left.\right)$ as $x \rightarrow x_{0}$ exists, is finite, and satisfies $\underset{x \rightarrow x_{0}}{lim} sin ⁡ \left(\right. x \left.\right) = sin ⁡ \left(\right. x_{0} \left.\right)$.

![](https://algebrica.org/wp-content/uploads/resources/images/sine-graph.png)

In fact, consider $x_{0} = \frac{\pi}{2}$ as a specific example. We have:

$$\underset{x \rightarrow \frac{\pi}{2}}{lim} sin ⁡ \left(\right. x \left.\right) = sin \left(\right. \frac{\pi}{2} \left.\right) = 1$$

The condition for continuity for the [sine function](https://algebrica.org/sine-function/) is satisfied at $x_{0}$, and the same reasoning extends to all other points in the domain.

---

Another way to express the continuity of a function at a point is to state that the right-hand and left-hand limits of the function at that point exist, are finite, and coincide with the function’s value. Referring to a generic point $x_{0}$, this can be written as:

$$\underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) = \underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right)$$

This condition guarantees that the graph of the function has no breaks or discontinuities at the point $x_{0} .$

> This property is evident in the graph of $f \left(\right. x \left.\right) = sin ⁡ \left(\right. x \left.\right)$. At each point $x_{0}$, the curve approaches the same value from both the left and the right, and this value matches $f \left(\right. x_{0} \left.\right)$. The graph forms a continuous, uninterrupted path across the entire real line, and this visual continuity reflects the analytical condition that the one-sided limits of the function and its value are equal.

## Example 1

Let us consider the [polynomial function](https://algebrica.org/polynomial-function/):

$$f \left(\right. x \left.\right) = 3 x + 1$$

We are interested in verifying whether this function is continuous at the point $x_{0} = 2$. To do so, we first compute the limit of the function as $x$ approaches $2$:

$$\underset{x \rightarrow 2}{lim} f \left(\right. x \left.\right) = \underset{x \rightarrow 2}{lim} \left(\right. 3 x + 1 \left.\right) = 3 \cdot 2 + 1 = 7$$

Next, we evaluate the function directly at the point:

$$f \left(\right. 2 \left.\right) = 3 \cdot 2 + 1 = 7$$

Since the function is a first-degree [polynomial](https://algebrica.org/polynomials), its graph is a straight [line](https://algebrica.org/lines).

![](https://algebrica.org/wp-content/uploads/resources/images/continuous-functions.png)

The limit exists, is finite, and coincides with the value of the function at that point. Therefore, we can conclude that

$$\underset{x \rightarrow 2}{lim} f \left(\right. x \left.\right) = f \left(\right. 2 \left.\right) = 7$$

This confirms that the function $f \left(\right. x \left.\right) = 3 x + 1$ is continuous at $x = 2.$

> This reasoning extends to higher-degree polynomial functions. For example, the quadratic function $f \left(\right. x \left.\right) = x^{2}$ has a [parabolic](https://algebrica.org/parabola/) graph, and for every point $x_{0} \in \mathbb{R}$, the limit exists, is finite, and satisfies $\underset{x \rightarrow x_{0}}{lim} x^{2} = x_{0}^{2} = f \left(\right. x_{0} \left.\right)$.

## Continuous function on an interval

When we consider an interval instead of a single point, we say that a function $y = f \left(\right. x \left.\right)$ is continuous on a closed and bounded interval $\left[\right. a , b \left]\right.$ if the following condition holds:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right) \forall x_{0} \in \left(\right. a , b \left.\right)$$

Just as with continuity at a point, continuity over a closed interval can be expressed in terms of one-sided limits at the endpoints of the interval. Specifically, the function must satisfy:

$$\underset{x \rightarrow a^{+}}{lim} f \left(\right. x \left.\right) & = f \left(\right. a \left.\right) \\ \underset{x \rightarrow b^{-}}{lim} f \left(\right. x \left.\right) & = f \left(\right. b \left.\right)$$

For example, the function $f \left(\right. x \left.\right) = \sqrt{x}$ defined on the interval $\left[\right. 0 , 4 \left]\right.$ is continuous at every interior point, as the square root function is continuous on $\left(\right. 0 , + \infty \left.\right)$.

![Example of continuous function.](https://algebrica.org/wp-content/uploads/resources/images/continuity-2.png "Example of continuous function.")

At the left and right endpoints, the one-sided continuity conditions are respectively satisfied:
$$\underset{x \rightarrow 0^{+}}{lim} \sqrt{x} & = 0 = f \left(\right. 0 \left.\right) \\ \underset{x \rightarrow 4^{-}}{lim} \sqrt{x} & = 2 = f \left(\right. 4 \left.\right)$$

Therefore, all three conditions for continuity are met, and $f \left(\right. x \left.\right) = \sqrt{x}$ is continuous on $\left[\right. 0 , 4 \left]\right.$.

## Functions continuous on their domain

The following functions are continuous on their respective [domains](https://algebrica.org/determining-the-domain-of-a-function/):

- Polynomial functions of the form $P \left(\right. x \left.\right) = a_{0} + a_{1} x + \hdots + a_{n} x^{n} .$
- [Rational functions](https://algebrica.org/rational-functions/).
- The [exponential function](https://algebrica.org/exponential-function) $a^{x} .$
- The [logarithmic function](https://algebrica.org/logarithmic-function) $log_{a} ⁡ x .$
- The [absolute value function](https://algebrica.org/absolute-value-function) $\left|\right. x \left|\right. .$
- The trigonometric functions [sine](https://algebrica.org/sine-and-cosine) $sin ⁡ x$, cosine $cos ⁡ x$, and [tangent](https://algebrica.org/tangent-and-cotangent) $tan ⁡ x$, as well as their inverse functions.

## Discontinuity

A function that is not continuous at a given point is said to exhibit a [discontinuity](https://algebrica.org/discontinuities-of-real-functions/) at that point. Discontinuities occur when the local stability provided by continuity fails to hold. Specifically, this may happen if the function is undefined at the point, if the limit does not exist, or if the limit exists but differs from the function’s value. Discontinuities are categorised into three mutually exclusive types:

- A removable discontinuity occurs when the limit of the function exists and is finite, but the function is either undefined at the point or its value does not equal the limit.
- A jump discontinuity occurs when both the left-hand and right-hand limits exist and are finite, but these limits are not equal.
- An infinite discontinuity is present when at least one of the one-sided limits is infinite, resulting in the function diverging near the point instead of approaching a finite value.

> A single point cannot simultaneously exhibit more than one type of discontinuity.

---

Let us look at an example of a simple function that is not continuous: the [sign function](https://algebrica.org/sign-function/), denoted by $sign \left(\right. x \left.\right)$. This function is defined as:

$$sign \left(\right. x \left.\right) = \left{\right. - 1 & \text{if} x < 0 \\ 0 & \text{if} x = 0 \\ 1 & \text{if} x > 0$$

At first glance, it may seem straightforward, but this function is not continuous at $x = 0$. To be continuous at a point, the limit from the left and the limit from the right must exist and be equal to the function’s value at that point. Let’s examine the limits:

- As $x \rightarrow 0^{-}$, the function approaches $- 1.$
- As $x \rightarrow 0^{+}$, the function approaches $1.$

So we have:

$$\underset{x \rightarrow 0^{-}}{lim} sign \left(\right. x \left.\right) & = - 1 \\ \underset{x \rightarrow 0^{+}}{lim} sign \left(\right. x \left.\right) & = 1$$

Since the two one-sided limits are not equal, the overall limit as $x \rightarrow 0$ does not exist. And although the function is defined at $x = 0$, we cannot match it with a limit value. Therefore, the function is discontinuous at $x = 0$, even though it is continuous everywhere else on $\mathbb{R} \backslash \left{\right. 0 \left.\right}$.

## Properties

The sum or difference of two continuous functions is also continuous. Suppose $f$ and $g$ are functions from $\mathbb{R}$ to $\mathbb{R}$, and let $x_{0}$ be a point belonging to both $Dom \left(\right. f \left.\right)$ and $Dom \left(\right. g \left.\right)$, where both functions are continuous. Then the function $f + g$, as well as $f - g$, is continuous at the point $x_{0}$. In other words, if both $f$ and $g$ are continuous at a point $x_{0}$, that is:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) & = f \left(\right. x_{0} \left.\right) \\ \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) & = g \left(\right. x_{0} \left.\right)$$

then the sum $f + g$ is also continuous at $x_{0}$, meaning:

$$\underset{x \rightarrow x_{0}}{lim} \left[\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left]\right. = f \left(\right. x_{0} \left.\right) + g \left(\right. x_{0} \left.\right)$$

---

The product of two continuous functions is a continuous function. Let $f , g : \mathbb{R} \rightarrow \mathbb{R}$, and let $x_{0} \in Dom \left(\right. f \left.\right) \cap Dom \left(\right. g \left.\right)$ be a point where both functions are continuous. Then the product function $f \cdot g$ is continuous at $x_{0}$. In other words, if:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) & = f \left(\right. x_{0} \left.\right) \\ \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) & = g \left(\right. x_{0} \left.\right)$$

then:

$$\underset{x \rightarrow x_{0}}{lim} \left[\right. f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) \left]\right. = f \left(\right. x_{0} \left.\right) \cdot g \left(\right. x_{0} \left.\right)$$

---

The quotient of two continuous functions remains continuous, provided that the denominator does not vanish. Let $f , g : \mathbb{R} \rightarrow \mathbb{R}$, and let $x_{0} \in Dom \left(\right. f \left.\right) \cap Dom \left(\right. g \left.\right)$ be a point where both functions are continuous, and such that $g \left(\right. x_{0} \left.\right) \neq 0$. Under these conditions then the quotient function $f / g$ is continuous at $x_{0}$. In other words, if we have:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) & = f \left(\right. x_{0} \left.\right) \\ \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) & = g \left(\right. x_{0} \left.\right) \\ g \left(\right. x_{0} \left.\right) & \neq 0$$

then the following equality holds:

$$\underset{x \rightarrow x_{0}}{lim} \left[\right. \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} \left]\right. = \frac{f \left(\right. x_{0} \left.\right)}{g \left(\right. x_{0} \left.\right)}$$

---

The [composition](https://algebrica.org/composite-functions/) of continuous functions is also a continuous function. Let $f , g : \mathbb{R} \rightarrow \mathbb{R}$, and let $x_{0} \in Dom \left(\right. f \left.\right)$ be a point where $f$ is continuous. Suppose that $g$ is continuous at $y_{0} = f \left(\right. x_{0} \left.\right)$. Then the composite function $g \circ f$ is continuous at $x_{0}$, meaning:

$$\underset{x \rightarrow x_{0}}{lim} \left[\right. g \left(\right. f \left(\right. x \left.\right) \left.\right) \left]\right. = g \left(\right. \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) \left.\right) = g \left(\right. f \left(\right. x_{0} \left.\right) \left.\right)$$

---

If a function $f$ is continuous and [strictly monotonic](https://algebrica.org/increasing-and-decreasing-functions/) on an interval $I \subset \mathbb{R}$, then it is invertible on $I$, and its [inverse function](https://algebrica.org/inverse-function/) $f^{- 1}$ remains continuous on $f \left(\right. I \left.\right)$. Equivalently, for any $y_{0} = f \left(\right. x_{0} \left.\right)$, the following holds:

$$\underset{y \rightarrow y_{0}}{lim} f^{- 1} \left(\right. y \left.\right) = x_{0}$$

Strict monotonicity guarantees that the function does not change direction, thereby preventing distinct nearby inputs from mapping to the same output. In the absence of monotonicity, continuity alone is insufficient to ensure the continuity of the inverse function.

## From continuity to uniform continuity

Continuity is a local property. At each point $x_{0}$ and for every $\epsilon > 0$, there exists a $\delta > 0$, which may depend on $x_{0}$, such that

$$\left|\right. x - x_{0} \left|\right. < \delta \rightarrow \left|\right. f \left(\right. x \left.\right) - f \left(\right. x_{0} \left.\right) \left|\right. < \epsilon$$

The value of $\delta$ may vary from point to point. In regions where the function grows rapidly, smaller values of $\delta$ are often necessary.

[Uniform continuity](https://algebrica.org/uniform-continuity/) extends this concept by imposing a single global constraint. A function $f : A \rightarrow \mathbb{R}$ is uniformly continuous on $A$ if, for every $\epsilon > 0$, there exists a $\delta > 0$ such that

$$\left|\right. x - y \left|\right. < \delta ; \Rightarrow ; \left|\right. f \left(\right. x \left.\right) - f \left(\right. y \left.\right) \left|\right. < \epsilon \forall x , y \in A$$

In this context, $\delta$ depends solely on $\epsilon$ and is independent of the specific points in the domain. In general, we have:

- Continuity does not imply uniform continuity.
- Uniform continuity does imply continuity.

For example, the function $f \left(\right. x \left.\right) = x^{2}$ is continuous on $\mathbb{R}$, but it is not uniformly continuous on $\mathbb{R}$ because no single $\delta$ can regulate its growth across the entire real line.

epsilon deltauniform continuitymonotonicityinverse continuitycompositionbehavior near pointclassificationundefined pointlimit mismatchsign functioninfinitejumpdomain continuityendpointsinterval continuityone-sided limitslimit conditioncontinuity at pointpropertiesdiscontinuitiesdefinition
