---
layout: chapter
title: "Non-Differentiable Points"
chapter: "Derivatives"
chapter_order: 16
section_order: 4
permalink: /materi-algebrica/derivatives/non-differentiable-points/
---

## What are non differentiable points

In the entry on [derivatives](https://algebrica.org/derivatives), we saw that if a function $f \left(\right. x \left.\right)$ is differentiable at a point $c$, then the function is [continuous](https://algebrica.org/continuous-functions/) at that point. However, there are cases where a function is continuous at $c$ but not differentiable. More generally, the **non-differentiable points** of a function $f \left(\right. x \left.\right)$ occur when:

- The right-hand and left-hand [limits](https://algebrica.org/limits/) of the [difference quotient](https://algebrica.org/difference-quotient) exist and are finite but are not equal. $$f_{-}^{'} \left(\right. c \left.\right) \neq f_{+}^{'} \left(\right. c \left.\right)$$
- The limit of the difference quotient is infinite.

These points are categorized into three main types, which we will discuss below.

## Inflection point with vertical tangent

An **inflection point** is a point where the concavity of a function changes. In this case, we have a point of non-differentiability $c$ of the function, which results in an [inflection point](https://algebrica.org/maximum-minimum-and-inflection-points/) with a tangent parallel to the $y$-axis (a vertical tangent). At such a point, the following occurs:

![](https://algebrica.org/wp-content/uploads/resources/images/non-differentiable-points-1.png)

This behavior indicates that the slope of the tangent becomes vertical at $x = c$ while the function may change concavity around this point. In the case shown in the figure, we have $$f_{-}^{'} \left(\right. c \left.\right) = f_{+}^{'} \left(\right. c \left.\right) = + \infty$$

If the curve were reflected across the y-axis, we would have $$f_{-}^{'} \left(\right. c \left.\right) = f_{+}^{'} \left(\right. c \left.\right) = - \infty$$

## Cusps

In the case of **cusps**, the right-hand and left-hand limits are infinite and have opposite signs.

![](https://algebrica.org/wp-content/uploads/resources/images/non-differentiable-points-2.png)

In the case shown in the figure, we have:
$$f_{-}^{'} \left(\right. c \left.\right) = - \infty \text{and} f_{+}^{'} \left(\right. c \left.\right) = + \infty$$

If the cusp were facing upwards instead of downwards, we would have:
$$f_{-}^{'} \left(\right. c \left.\right) = + \infty \text{and} f_{+}^{'} \left(\right. c \left.\right) = - \infty$$

## Corners

A **corner** occurs when the left-hand derivative and the right-hand derivative exist but are not equal. In the case of corners points, there are two tangents to the graph at the same point, and they are different from each other.

![](https://algebrica.org/wp-content/uploads/resources/images/non-differentiable-points-3.png)

In this case we have:

$$f_{-}^{'} \left(\right. c \left.\right) \neq f_{+}^{'} \left(\right. c \left.\right)$$

How can we verify the differentiability of a function without relying on the limit of its difference quotient?

In general, let $f \left(\right. x \left.\right)$ be a function continuous on an interval ([a,b]) and differentiable on that interval, except possibly at the point $x_{0} \in \left[\right. a , b \left]\right.$. If the limits $\underset{x \rightarrow x_{0}^{-}}{lim} f^{'} \left(\right. x \left.\right)$ and $\underset{x \rightarrow x_{0}^{+}}{lim} f^{'} \left(\right. x \left.\right)$ exist, then:

$$f_{-}^{'} \left(\right. x_{o} \left.\right) = \underset{x \rightarrow x_{0}^{-}}{lim} f^{'} \left(\right. x \left.\right) \text{and} f_{+}^{'} \left(\right. x_{o} \left.\right) = \underset{x \rightarrow x_{0}^{+}}{lim} f^{'} \left(\right. x \left.\right)$$

if $\underset{x \rightarrow x_{0}^{-}}{lim} f ′ \left(\right. x \left.\right) = \underset{x \rightarrow x_{0}^{+}}{lim} f ′ \left(\right. x \left.\right) = ℓ$, with $ℓ \in \mathbb{R}$ then the function is differentiable at $x_{0}$, and it follows that $f^{'} \left(\right. x_{0} \left.\right) = ℓ$.
