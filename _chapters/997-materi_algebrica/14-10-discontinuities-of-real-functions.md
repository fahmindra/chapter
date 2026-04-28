---
layout: chapter
title: "Discontinuities of Real Functions"
chapter: "Functions"
chapter_order: 14
section_order: 10
permalink: /materi-algebrica/functions/discontinuities-of-real-functions/
---

## Introduction

Continuity is a property of a [function](https://algebrica.org/functions/) in which small variations in the input result in correspondingly small variations in the output within the neighbourhood of a given point. If this local stability does not hold, the function is considered discontinuous. Discontinuities are typically classified into three distinct types:

- A removable discontinuity occurs when the limit exists and is finite, but the function is either undefined at the point or its value does not equal the limit.
- A jump discontinuity is present when both the left-hand and right-hand limits exist and are finite, but these limits are not equal.
- An infinite discontinuity occurs when at least one of the one-sided limits is infinite, causing the function to diverge near the point rather than approach a finite value.

A discontinuity at $x_{0}$ can occur in exactly one of the three mutually exclusive ways described above. A point cannot simultaneously exhibit more than one type of discontinuity.

###### Each of these types will be examined in detail in the following sections. In this discussion, $f$ denotes a real-valued function, and $x_{0}$ represents a point in its [domain](https://algebrica.org/determining-the-domain-of-a-function/) or a point at which the function may fail to be defined.

## Recall of continuity

A function $f$ is [continuous](https://algebrica.org/continuous-functions/) at $x_{0}$ if the limit as $x$ approaches $x_{0}$ exists, is finite, and coincides with the value of the function at that point. This condition is expressed by the following [limit](https://algebrica.org/limits/):

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right)$$

[Polynomials](https://algebrica.org/polynomials/) constitute a fundamental class of elementary continuous functions. These functions represent smooth curves in the plane and exhibit no points of discontinuity. Below is the graph of the quadratic function $x^{2} + 2 x + 1$, which represents a [parabola](https://algebrica.org/parabola/):

![The graph of a second-degree polynomial is a continuous parabola, with no jumps or interruptions.](https://algebrica.org/wp-content/uploads/resources/images/discontinuity.png "The graph of a second-degree polynomial is a continuous parabola, with no jumps or interruptions.")

A discontinuity at $x_{0}$ arises whenever this equality does not hold, and the specific way in which the condition fails determines the type of discontinuity.

###### Intuitively, a function is continuous if its graph can be drawn in the plane without any interruptions, breaks, or sudden jumps.

## Removable discontinuity

A removable discontinuity arises when a function possesses a well-defined finite limit at $x_{0}$, yet the function’s value at that point is either undefined or does not coincide with the limit. Formally, a function $f$ has a removable discontinuity at $x_{0}$ if the following limit exists and is finite:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = ℓ \in \mathbb{R}$$

Moreover, at least one of the following conditions is satisfied:

- $f \left(\right. x_{0} \left.\right)$ is undefined.
- $f \left(\right. x_{0} \left.\right) \neq ℓ$.

In such cases, the discontinuity may be removed by redefining the function at a single point as follows:
$$g \left(\right. x \left.\right) = \left{\right. ℓ & \text{if} x = x_{0} \\ f \left(\right. x \left.\right) & \text{if} x \neq x_{0}$$

With this definition, the function $g$ becomes continuous at $x_{0}$. The term “removable” refers to the fact that the discontinuity can be resolved in this manner.

###### Removable discontinuities typically occur in rational functions containing cancellable factors, resulting in a hole in the graph. They can also be present in piecewise-defined functions or in functions where the value at a single point has been modified, provided the limit at that point exists and is finite.

## Example 1

Consider the function defined by the following [rational](https://algebrica.org/rational-functions/) expression, which is undefined at $x = 1$:

$$f \left(\right. x \left.\right) = \frac{x^{2} - 1}{x - 1}$$

[Factoring](https://algebrica.org/factoring-ac-method/) the numerator demonstrates that the expression simplifies for all values of $x$ except $1$ since $x = 1$ would cancel the denominator and make the function undefined.

$$x^{2} - 1 = \left(\right. x - 1 \left.\right) \left(\right. x + 1 \left.\right)$$

For all $x \neq 1$, the function is equivalent to a linear function:
$$f \left(\right. x \left.\right) = x + 1$$

Although the function is undefined at $x = 1$, the limit as $x$ approaches $1$ exists and is finite:

$$\underset{x \rightarrow 1}{lim} \frac{x^{2} - 1}{x - 1} = 2$$

This demonstrates that $x = 1$ is a removable discontinuity, as the graph corresponds to the straight line $y = x + 1$ with a single missing point at$\left(\right. 1 , 2 \left.\right) .$

Redefining the function at that point by assigning it the value of the limit eliminates the discontinuity:
$$g \left(\right. x \left.\right) = \left{\right. 2 & \text{if} x = 1 \\ f \left(\right. x \left.\right) & \text{if} x \neq 1$$

###### With this modification, the function is continuous at $x = 1$.

## Jump discontinuity

A jump discontinuity arises when both the left-hand and right-hand limits at $x_{0}$ exist and are finite, yet these limits are not equal. Formally, $f$ has a jump discontinuity at $x_{0}$ if:

$$\underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right) & = ℓ_{1} \in \mathbb{R} \\ \underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) & = ℓ_{2} \in \mathbb{R} \\ ℓ_{1} & \neq ℓ_{2}$$

In this case, the limit $\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right)$ does not exist. The function approaches two distinct finite values depending on the direction of approach. Unlike a removable discontinuity, this type cannot be resolved by redefining the function at a single point, as the discrepancy is inherent to the local behavior.

## Example 2

To analyse the jump discontinuity, consider the following simple function, which exhibits a discontinuity at the point $x = 1.$

$$f \left(\right. x \left.\right) = \left{\right. 0 & \text{if} x < 1 \\ 2 & \text{if} x \geq 1$$

![](https://algebrica.org/wp-content/uploads/resources/images/discontinuity-2.png)

For values of $x$ approaching $1$ from the left, the function remains constant at $0$. Therefore:

$$\underset{x \rightarrow 1^{-}}{lim} f \left(\right. x \left.\right) = 0$$

For values of $x$ approaching 1 from the right, the function remains constantly equal to $2$, and therefore the limit is:
$$\underset{x \rightarrow 1^{+}}{lim} f \left(\right. x \left.\right) = 2$$

Both one-sided limits exist and are finite but they are not equal. Since $0 \neq 2$, it follows that the two one-sided limits do not coincide, and consequently, the limit $\underset{x \rightarrow 1}{lim} f \left(\right. x \left.\right)$ does not exist. The graph of the function shows a vertical jump at $x = 1$, transitioning from $0$ to $2$.

This discontinuity cannot be removed by redefining the function at $x = 1$, as the difference between the two limiting values indicates a break in the local behaviour of the function.

## Infinite discontinuity

An infinite discontinuity occurs when a function diverges as $x$ approaches $x_{0}$, with at least one of the one-sided limits being infinite. Formally, a function $f$ exhibits an infinite discontinuity at $x_{0}$ if at least one of the following conditions is satisfied:

$$\underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right) & = \pm \infty \\ \underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) & = \pm \infty$$

In such cases, the function does not approach any finite value as $x$ nears $x_{0}$. The graph typically displays a vertical [asymptote](https://algebrica.org/asymptotes/). This discontinuity reflects unbounded growth rather than a finite discontinuity.

## Example 3

For example, consider the following function:

$$f \left(\right. x \left.\right) = \frac{1}{x - 2}$$

![](https://algebrica.org/wp-content/uploads/resources/images/discontinuity-3.png)

The behaviour of this function near $x_{0} = 2$ is analysed as follows. As $x \rightarrow 2^{-}$, the denominator $x - 2$ becomes negative and approaches zero, causing the function to decrease without bound. Therefore we have:

$$\underset{x \rightarrow 2^{-}}{lim} f \left(\right. x \left.\right) = - \infty$$

As $x \rightarrow 2^{+}$, the denominator is positive and approaches zero, which causes the function to increase without bound. The limit is:

$$\underset{x \rightarrow 2^{+}}{lim} f \left(\right. x \left.\right) = + \infty$$

At least one of the one-sided limits is infinite, and they diverge with opposite signs. Consequently, the function exhibits an infinite discontinuity at $x = 2$. The graph displays a [vertical asymptote](https://algebrica.org/asymptotes/) at the line $x = 2$, and this divergence indicates unbounded growth rather than a finite jump or a removable discontinuity.

## Discontinuity, continuity and differentiability

It is instructive to establish a precise link between the notions of discontinuity and [differentiability](https://algebrica.org/derivatives/). We know that if a function f is differentiable at a point $x_{0}$, it must also be [continuous](https://algebrica.org/continuous-functions/) at that point. The existence of the derivative ensures that the function satisfies the condition of continuity:

$$f^{'} \left(\right. x_{0} \left.\right) = \underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right) - f \left(\right. x_{0} \left.\right)}{x - x_{0}}$$
$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right)$$

Therefore, if a function exhibits a discontinuity of the type just described at $x_{0}$, meaning the limit does not exist or does not equal the function’s value the derivative at that point does not exist.

However, the converse is not true. A function can be continuous at $x_{0}$ yet not differentiable there. This situation arises when the one-sided derivatives exist but differ, when at least one is infinite, or when one of the limits diverges.

$$\underset{x \rightarrow x_{0}^{-}}{lim} \frac{f \left(\right. x \left.\right) - f \left(\right. x_{0} \left.\right)}{x - x_{0}} \neq \underset{x \rightarrow x_{0}^{+}}{lim} \frac{f \left(\right. x \left.\right) - f \left(\right. x_{0} \left.\right)}{x - x_{0}}$$

A common example is the [absolute value function](https://algebrica.org/absolute-value-function/), which is continuous at $x = 0$ but not differentiable there, resulting in a corner on its graph. In summary, every discontinuity implies non-differentiability, whereas not every point of non-differentiability is associated with a discontinuity.

## A particular case: essential discontinuity

An additional category, known as essential discontinuity, is sometimes recognised but not universally adopted as a formal classification. This type arises when the limit does not exist and cannot be described as infinite. Unlike a jump discontinuity, where both one-sided limits exist but are unequal, or an infinite discontinuity, where the function diverges in a particular direction, an essential discontinuity reflects fundamentally irregular behaviour that cannot be reduced to simpler forms.

A classic example is the following function, which exhibits an essential discontinuity at $x = 0$:

$$f \left(\right. x \left.\right) = sin ⁡ \left(\right. \frac{1}{x} \left.\right)$$

As $x$ approaches $0$, the argument $1 / x$ grows without bound, causing the function to oscillate between $- 1$ and $1$ with increasing frequency. Neither one-sided limit exists, and no value can be assigned to $f \left(\right. 0 \left.\right)$ that would restore any form of continuity.

## Selected references

- **Harvard University N. Masson**. [Discontinuities and Monotonic Functions](https://people.math.harvard.edu/~nate/teaching/UPenn/2009/spring/math_360/lectures/week_8/lecture_14/lecture_14.pdf)
- **Harvard University O. Knill**. [Introduction to Functions and Calculus – Continuity](https://people.math.harvard.edu/~knill/teaching/math1a_2012/handouts/14-continuity.pdf)
- **UC Berkeley A. Vizeff**. [Lecture 5: Continuity and Discontinuities](https://math.berkeley.edu/~avizeff/calculus-I-F22/lecture-5.pdf)
