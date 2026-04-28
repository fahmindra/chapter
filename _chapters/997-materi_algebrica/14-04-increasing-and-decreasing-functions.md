---
layout: chapter
title: "Increasing, Decreasing and Monotonic Functions"
chapter: "Functions"
chapter_order: 14
section_order: 4
permalink: /materi-algebrica/functions/increasing-decreasing-and-monotonic-functions/
---

## Introduction

Understanding the behavior of [functions](https://algebrica.org/functions) is fundamental in mathematics. Depending on how their output values change with respect to the input, functions can be classified as:

- increasing
- decreasing
- monotonic

##### These characteristics are closely tied to the geometry of their graphs in the Cartesian plane, revealing whether a function rises, falls, or maintains a consistent directional trend.

---

Let $y = f \left(\right. x \left.\right)$ be a function defined on a [domain](https://algebrica.org/determining-the-domain-of-a-function/) $X \subseteq \mathbb{R}$. We say that $f$ is **strictly increasing** on an interval $I \subseteq X$ if, for any two values $x_{1} , x_{2} \in I$ such that $x_{1} < x_{2}$, the following condition holds:
$$f \left(\right. x_{1} \left.\right) < f \left(\right. x_{2} \left.\right)$$

![](https://algebrica.org/wp-content/uploads/resources/images/increasing-decreasing-functions-1-3.png)

This means that as the input $x$ increases within the interval $I$, the output $f \left(\right. x \left.\right)$ also strictly increases, without any flat or decreasing segments.

---

Let $y = f \left(\right. x \left.\right)$ be a function defined on a domain $X \subseteq \mathbb{R}$.
We say that $f$ is **strictly decreasing** on an interval $I \subseteq X$ if, for any two values $x_{1} , x_{2} \in I$ such that $x_{1} < x_{2}$, the following condition holds:

$$f \left(\right. x_{1} \left.\right) > f \left(\right. x_{2} \left.\right)$$

![](https://algebrica.org/wp-content/uploads/resources/images/increasing-decreasing-functions-2-1.png)

This means that as the input $x$ increases within the interval $I$,
the output $f \left(\right. x \left.\right)$ strictly decreases, with no flat or increasing sections.

---

A function with domain $X \subseteq \mathbb{R}$ is said to be **strictly monotonic** on an interval $I \subseteq X$ if it is either strictly increasing or strictly decreasing throughout the entire interval $I$, with no change in direction or flat segments. In other words, the function maintains a consistent trend, either upward or downward, across $I$.

To summarize: let $X \subseteq \mathbb{R}$, and let $x_{1} , x_{2} \in X$ with $x_{1} < x_{2}$. Then the function $f : X \rightarrow \mathbb{R}$ is said to be:

- Increasing: if $f \left(\right. x_{1} \left.\right) \leq f \left(\right. x_{2} \left.\right)$.
- Strictly increasing: if $f \left(\right. x_{1} \left.\right) < f \left(\right. x_{2} \left.\right)$.
- Decreasing: if $f \left(\right. x_{1} \left.\right) \geq f \left(\right. x_{2} \left.\right)$.
- Strictly decreasing: if $f \left(\right. x_{1} \left.\right) > f \left(\right. x_{2} \left.\right)$.
- (Strictly) monotonic: if the function is either (strictly) increasing or (strictly) decreasing.

## Derivatives and monotonic behavior

We know that [derivatives](https://algebrica.org/derivatives) are used to describe the shape and graph of functions. In particular, the first derivative of a function, $f^{'} \left(\right. x \left.\right)$, can indicate the intervals where the original function $f \left(\right. x \left.\right)$ is increasing and where it is decreasing.

In general, given a function $y = f \left(\right. x \left.\right)$ that is [continuous](https://algebrica.org/continuous-functions/) on an interval $I$ and differentiable at the interior points of $I$:

- If $f^{'} \left(\right. x \left.\right) > 0$ for every $x$ in the interior of $I$, then $f \left(\right. x \left.\right)$ is increasing on $I$.
- If $f^{'} \left(\right. x \left.\right) < 0$ for every $x$ in the interior of $I$, then $f \left(\right. x \left.\right)$ is decreasing on $I$.
- If $f^{'} \left(\right. x \left.\right) = 0$ for every $x$ in the interior of $I$, then $f \left(\right. x \left.\right)$ is constant on $I$.

---

To demonstrate these properties, we use the [Lagrange’s Theorem](https://algebrica.org/lagrange-theorem). Let’s imagine having two points $a$ and $b$ $\in I$ with $a < b$. Next, let us consider a point $c$ belonging to the interval $\left]\right. a , b \left[\right.$.

![](https://algebrica.org/wp-content/uploads/resources/images/increasing-decreasing-function.png)

By the Lagrange’s Theorem, we have:

$$f^{′} \left(\right. c \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$

Since we have $b - a > 0$ and $f^{'} \left(\right. c \left.\right) > 0$, it follows that $f \left(\right. b \left.\right) - f \left(\right. a \left.\right) > 0$, which implies $f \left(\right. b \left.\right) > f \left(\right. a \left.\right)$. Since $a$ and $b$ are arbitrary points in $I$, the function is increasing on $I$.

Similarly, considering the opposite case, since we have $b - a > 0$ and $f^{'} \left(\right. c \left.\right) < 0$, it follows that $f \left(\right. b \left.\right) - f \left(\right. a \left.\right) < 0$, which implies $f \left(\right. b \left.\right) < f \left(\right. a \left.\right)$. Since $a$ and $b$ are arbitrary points in $I$, the function is decreasing on $I$.

## Example 1

Let us consider the function:
$$f \left(\right. x \left.\right) = \frac{x^{4}}{4} - \frac{x^{2}}{2}$$

---

Let us compute its derivative:
$$f^{'} \left(\right. x \left.\right) = x \left(\right. x^{2} - 1 \left.\right)$$

Let us find the intervals where the derivative is greater than zero. We have:

$$x > 0$$
$$x^{2} - 1 > 0 \Longrightarrow x < - 1 \text{or} x > 1$$

By multiplying the signs of the first and second factors, we obtain the intervals where the derivative is positive.

|  |  | $$- 1$$ | $$0$$ | $$1$$ |
| --- | --- | --- | --- | --- |
| $x > 0$ | $-$ | $-$ | $+$ | $+$ |
| $x^{2} - 1 > 0$ | $+$ | $-$ | $-$ | $+$ |
| $$f^{'} \left(\right. x \left.\right)$$ | $-$ | $+$ | $-$ | $+$ |

Therefore, the derivative $x \left(\right. x^{2} - 1 \left.\right)$ is positive for:

$$x \in \left(\right. - 1 , 0 \left.\right) \cup \left(\right. 1 , + \infty \left.\right)$$

##### For the sake of completeness, we recall that the sign analysis of a function, as in the given example, requires examining the signs of its individual factors and determining the overall sign for each interval by computing the product of these signs.

---

Graphically, its behavior is as follows:

![](https://algebrica.org/wp-content/uploads/resources/images/increasing-decreasing-functions-2.png)

Therefore, the function is increasing in the interval $\left(\right. - 1 , 0 \left.\right) \cup \left(\right. 1 , + \infty \left.\right)$ and decreasing in the interval $\left(\right. - \infty , - 1 \left.\right) \cup \left(\right. 0 , 1 \left.\right)$.
