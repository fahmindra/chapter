---
layout: chapter
title: "Sign Function"
chapter: "Functions"
chapter_order: 14
section_order: 17
permalink: /materi-algebrica/functions/sign-function/
---

## Introduction

The sign function assigns to each real number its sign, disregarding its magnitude. The function is defined as follows:

$$sgn \left(\right. x \left.\right) = \left{\right. - 1 & \text{if} x < 0 \\ 0 & \text{if} x = 0 \\ 1 & \text{if} x > 0 \forall x \in \mathbb{R}$$

Specifically, $sgn \left(\right. x \left.\right)$ returns $- 1$ for negative values, $0$ when $x = 0$, and $1$ for positive values. The function does not quantify the magnitude of $x$ but solely indicates the position of $x$ relative to zero. For example, applying the definition we have:

$$sgn \left(\right. - 7 \left.\right) = - 1 sgn \left(\right. 0 \left.\right) = 0 sgn \left(\right. 4 \left.\right) = 1$$

---

The graph of $y = sgn \left(\right. x \left.\right)$ consists of two horizontal rays and one isolated point. The ray on $y = - 1$ extends over all $x < 0$, the ray on $y = 1$ extends over all $x > 0$, and the isolated point at the origin $\left(\right. 0 , 0 \left.\right)$ lies on $y = 0$. The two rays approach but do not intersect the y-axis.

![Sign function.](https://algebrica.org/wp-content/uploads/resources/images/sign-function-1.png "Sign function.")

The sign function is classified as an [odd function](https://algebrica.org/even-and-odd-functions/) because it satisfies the identity:

$$sgn \left(\right. - x \left.\right) = - sgn \left(\right. x \left.\right) \forall x \in \mathbb{R}$$

## Properties

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $\mathbb{R}$.
- Range: $- 1 , 0 , 1$.
- The function is [odd](https://algebrica.org/even-and-odd-functions/), since $sgn \left(\right. - x \left.\right) = - sgn \left(\right. x \left.\right)$.
- The function has exactly one root at $x = 0$, since $sgn \left(\right. x \left.\right) = 0$ only when $x = 0$.
- The function is constant on $\left(\right. - \infty , 0 \left.\right)$ and on $\left(\right. 0 , + \infty \left.\right)$, hence [increasing](https://algebrica.org/increasing-and-decreasing-functions/) in the sense that it is non-decreasing over $\mathbb{R}$.
- The function has a [jump discontinuity](https://algebrica.org/discontinuities-of-real-functions/) at $x = 0$; it is [continuous](https://algebrica.org/continuous-functions/) everywhere else.
- The function is not differentiable at $x = 0$. It is differentiable, with zero [derivative](https://algebrica.org/derivatives/), at every other point.
- Limits approaching $x = 0$ from either side:
  $$\underset{x \rightarrow 0^{-}}{lim} sgn \left(\right. x \left.\right) & = - 1 \\ \underset{x \rightarrow 0^{+}}{lim} sgn \left(\right. x \left.\right) & = 1$$

Since the two one-sided limits differ, the two-sided the following limit does not exist:
$$\underset{x \rightarrow 0}{lim} sgn \left(\right. x \left.\right)$$

## Limits at infinity

As $x$ moves away from the origin in either direction, the sign function stabilizes at a constant value:

$$\underset{x \rightarrow - \infty}{lim} sgn \left(\right. x \left.\right) & = - 1 \\ \underset{x \rightarrow + \infty}{lim} sgn \left(\right. x \left.\right) & = 1$$

These are simply a consequence of the fact that $sgn \left(\right. x \left.\right) = - 1$ for all $x < 0$ and $sgn \left(\right. x \left.\right) = 1$ for all $x > 0$, so the function value does not change as $x$ moves further from zero.

## Derivative and integral

On each of the two open half-lines where the sign function is constant, its [derivative](https://algebrica.org/derivatives/) is zero:

$$\frac{d}{d x} sgn \left(\right. x \left.\right) = 0 \text{for} x \neq 0$$

At $x = 0$, the derivative does not exist because the function is discontinuous there. In the sense of distributions, however, the derivative of the sign function is:

$$\frac{d}{d x} sgn \left(\right. x \left.\right) = 2 \delta \left(\right. x \left.\right)$$

$\delta \left(\right. x \left.\right)$ is the Dirac delta, a generalised function that is zero everywhere except at the origin and integrates to one over the entire real line. This distributional identity demonstrates that the sign function exhibits a discontinuity of amplitude $2$ at the origin, as:

$$\underset{x \rightarrow 0^{-}}{lim} sgn \left(\right. x \left.\right) = - 1$$
$$\underset{x \rightarrow 0^{+}}{lim} sgn \left(\right. x \left.\right) = 1$$

This amplitude explains the presence of the factor $2$ preceding the Dirac delta function.

---

The [indefinite integral](https://algebrica.org/indefinite-integrals/) of the sign function, computed away from the origin, gives back the [absolute value](https://algebrica.org/absolute-value-function/):

$$\int sgn \left(\right. x \left.\right) d x = \left|\right. x \left|\right. + c$$

This is consistent with the fact that the derivative of $\left|\right. x \left|\right.$ equals $sgn \left(\right. x \left.\right)$ wherever the former is differentiable.

## Relationship with the absolute value function

A direct algebraic relationship exists between the sign function and the [absolute value](https://algebrica.org/absolute-value-function/). For any $x \neq 0$, the following identity holds:

$$sgn \left(\right. x \left.\right) = \frac{x}{\left|\right. x \left|\right.}$$

This result is consistent with the definition: when $x > 0$, the ratio $x / \left|\right. x \left|\right. = x / x = 1$. When $x < 0$, the ratio $x / \left|\right. x \left|\right. = x / \left(\right. - x \left.\right) = - 1$. The formula is undefined at $x = 0$, so the value $sgn \left(\right. 0 \left.\right) = 0$ is assigned separately by convention.

Conversely, the absolute value can be expressed in terms of the sign function using the following identity:

$$\left|\right. x \left|\right. = x \cdot sgn \left(\right. x \left.\right)$$

This identity holds for all $x \in \mathbb{R}$, including $x = 0$, where both sides are zero. Together, these two identities demonstrate that $\left|\right. x \left|\right.$ and $sgn \left(\right. x \left.\right)$ are complementary: the absolute value preserves magnitude and omits sign, whereas the sign function preserves sign and omits magnitude.

---

Two additional identities arise from the relationship between the sign function and the absolute value. The first identity is as follows:

$$x = \left|\right. x \left|\right. \cdot sgn \left(\right. x \left.\right)$$

This identity expresses any real number as the product of its magnitude and its sign. The second identity utilises the equality $\left|\right. x \left|\right. = \sqrt{x^{2}}$, which is valid for all $x \in \mathbb{R}$, and provides an alternative representation of the sign function for $x \neq 0$:

$$sgn \left(\right. x \left.\right) = \frac{x}{\sqrt{x^{2}}}$$

## Relationship with the Heaviside step function

The [Heaviside step function](https://algebrica.org/heaviside-function/) $H \left(\right. x \left.\right)$ is defined as:

$$H \left(\right. x \left.\right) = \left{\right. 0 & \text{if} x < 0 \\ \frac{1}{2} & \text{if} x = 0 \\ 1 & \text{if} x > 0$$

![Heaviside step function.](https://algebrica.org/wp-content/uploads/resources/images/Heaviside-function-1.png "Heaviside step function.")

The sign function and the Heaviside step function are related by a simple linear transformation. Specifically:

$$sgn \left(\right. x \left.\right) = 2 H \left(\right. x \left.\right) - 1$$

Equivalently, we have:

$$H \left(\right. x \left.\right) = \frac{1 + sgn \left(\right. x \left.\right)}{2}$$

This relationship is frequently utilised as converting between these representations can simplify calculations. The Heaviside function maps $\left(\right. - \infty , 0 \left.\right)$ to $0$ and $\left(\right. 0 , + \infty \left.\right)$ to $1$, and may therefore be interpreted as a shifted and rescaled form of the sign function.
