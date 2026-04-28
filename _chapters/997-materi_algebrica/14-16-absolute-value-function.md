---
layout: chapter
title: "Absolute Value Function"
chapter: "Functions"
chapter_order: 14
section_order: 16
permalink: /materi-algebrica/functions/absolute-value-function/
---

## Introduction

The [absolute value](https://algebrica.org/absolute-value) of a number, is defined as follows:

$$\left|\right. x \left|\right. = \left{\right. + x & \text{if} x \geq 0 \\ - x & \text{if} x < 0 \forall x \in \mathbb{R}$$

The absolute value function assigns to each real number its distance from zero on the number line. This means that negative numbers are mapped to their positive counterparts, while positive numbers remain unchanged, since distance is always non-negative.

![Geometrically, the absolute value of x, written |x|, represents the distance between x and 0 on the number line.](https://algebrica.org/wp-content/uploads/resources/images/absolute-value-1.png)

More generally, the absolute value expression $\left|\right. x - a \left|\right.$ can be interpreted as the distance between the point $x$ and the point $a$ on the number line. We have:

$$\left|\right. x - a \left|\right. = \left|\right. a - x \left|\right.$$

In fact, we can observe that $a - x$ is simply the opposite of $x - a$; in other words $a - x = - \left(\right. x - a \left.\right)$. It follows that $\left|\right. a - x \left|\right. = \left|\right. - \left(\right. x - a \left.\right) \left|\right. = \left|\right. x - a \left|\right.$. This shows that the two expressions have the same absolute value, even though the terms inside the parentheses appear in reverse order.

## Graph and symmetry of the absolute value function

The absolute value function is:

$$y = \left|\right. x \left|\right. = \left{\right. + x & \text{if} x \geq 0 \\ - x & \text{if} x < 0$$

The graph of $y = \left|\right. x \left|\right.$ is:

![The graph of the absolute value function is symmetric with respect to the y-axis. This symmetry implies that the function is even.](https://algebrica.org/wp-content/uploads/resources/images/absolute-value-6.png)

---

The graph of the absolute value function $\left|\right. x \left|\right.$ is symmetric with respect to the y-axis. This symmetry implies that the function is [even](https://algebrica.org/even-and-odd-functions/), meaning it satisfies the identity:

$$\left|\right. - x \left|\right. = \left|\right. x \left|\right. \text{for all} x \in \mathbb{R}$$

## Properties

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $\mathbb{R}$.
- Range: $\mathbb{R}_{0}^{+}$.
- The function is [decreasing](https://algebrica.org/increasing-and-decreasing-functions/) on $\left(\right. - \infty , 0 \left]\right.$and increasing on $\left[\right. 0 , + \infty \left.\right)$.
- The function is [even](https://algebrica.org/even-and-odd-functions/), since $\left|\right. - x \left|\right. = \left|\right. x \left|\right.$.
- The function is [continuous](https://algebrica.org/continuous-functions/) over the entire real line $\mathbb{R}$.
- The function is differentiable everywhere except at $x = 0$ where it has a [corner point](https://algebrica.org/points-of-non-differentiability/).
- The function has an [absolute minimum](https://algebrica.org/maximum-minimum-and-inflection-points/) at $x = 0$, where $\left|\right. x \left|\right. = 0$ and it has no maximum.
- Limits as $x$ approaches the extremes of the domain:
  $$\underset{x \rightarrow - \infty}{lim} \left|\right. x \left|\right. & = + \infty \\ \underset{x \rightarrow + \infty}{lim} \left|\right. x \left|\right. & = + \infty$$

## How to graph the absolute value of a function: flip the negative part

Let us consider the [parabola](https://algebrica.org/parabola) defined by the equation

$$y = x^{2} - 1$$

This graph includes a portion of the curve that lies below the x-axis, specifically in the interval where the function takes negative values.

![](https://algebrica.org/wp-content/uploads/resources/images/absolute-value-3.png)

To find this interval, we solve:

$$x^{2} - 1 < 0 \rightarrow - 1 < x < 1.$$

So, the function $y = x^{2} - 1$ is negative on the open interval $\left(\right. - 1 , 1 \left.\right)$, and the graph dips below the x-axis in that region.

---

To graph the function $f \left(\right. x \left.\right) = \left|\right. x^{2} - 1 \left|\right.$, we start from the graph of $y = x^{2} - 1$. We leave unchanged the portions of the graph that lie on or above the x-axis, and we reflect across the x-axis all portions that were originally below it. We obtain:

![](https://algebrica.org/wp-content/uploads/resources/images/absolute-value-4.png)

This transformation ensures that all function values become non-negative, as required by the absolute value.

## Limits, derivatives, and integrals of the absolute value function

The fundamental [limit](https://algebrica.org/limits) associated with the absolute value function is:
$$\underset{x \rightarrow 0}{lim} \frac{\left|\right. x \left|\right.}{x}$$
This limit does not exist, because the left-hand and right-hand limits are different:
$$\underset{x \rightarrow 0^{-}}{lim} \frac{\left|\right. x \left|\right.}{x} = - 1 \text{and} \underset{x \rightarrow 0^{+}}{lim} \frac{\left|\right. x \left|\right.}{x} = 1$$
This behavior highlights the non-differentiability of $\left|\right. x \left|\right.$ at $x = 0$.

---

The [derivative](https://algebrica.org/derivatives) of the absolute value function is defined piecewise as:
$$\frac{d}{d x} \left|\right. x \left|\right. = \left{\right. 1 & \text{if} x > 0 \\ - 1 & \text{if} x < 0$$
The derivative does not exist at $x = 0$, because the function has a [sharp corner](https://algebrica.org/points-of-non-differentiability/) at that point.

---

The [indefinite integral](https://algebrica.org/indefinite-integrals) of the absolute value function is:
$$\int \left|\right. x \left|\right. d x = \frac{x^{2} \cdot sgn \left(\right. x \left.\right)}{2} + c$$
where $sgn \left(\right. x \left.\right)$ is the [sign function](https://algebrica.org/sign-function/), defined as:
$$sgn \left(\right. x \left.\right) = \left{\right. - 1 & \text{if} x < 0 \\ 0 & \text{if} x = 0 \\ 1 & \text{if} x > 0$$
