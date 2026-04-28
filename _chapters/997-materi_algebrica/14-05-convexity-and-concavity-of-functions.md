---
layout: chapter
title: "Convexity and Concavity of Functions"
chapter: "Functions"
chapter_order: 14
section_order: 5
permalink: /materi-algebrica/functions/convexity-and-concavity-of-functions/
---

## Introduction

The study of a [function’s behaviour](https://algebrica.org/analyzing-the-graphs-of-functions/) involves not only determining where it [increases or decreases](https://algebrica.org/increasing-and-decreasing-functions/), but also understanding how its graph bends within an interval. A [function](https://algebrica.org/functions/) may be entirely increasing or decreasing on a region while still exhibiting distinct geometric shapes: the curve may arch upward or downward, affecting the overall appearance of the graph and the nature of its variation.

These qualitative features are described by the notions of **convexity** and **concavity**. From a geometric perspective, they characterise whether the graph lies above or below its tangents; analytically, they are determined through the sign of the second [derivative](https://algebrica.org/derivatives/) , which quantifies the curvature of the function. Establishing this connection provides a precise criterion for identifying how a function bends across its domain.

## Convexity

A function $f$ is said to be convex on an interval when, for any two points $a$ and $b$ within that interval, the straight line that connects $\left(\right. a , f \left(\right. a \left.\right) \left.\right)$ and $\left(\right. b , f \left(\right. b \left.\right) \left.\right)$ remains above the graph of $f$ at every point between $a$ and $b$. In other words, the chord linking these two points does not dip below the curve.

![](https://algebrica.org/wp-content/uploads/resources/images/convexity-1-1.png "The graph illustrates how the convexity of the function ensures that every secant line lies above the curve.")

The equation of the secant line passing through the points $\left(\right. a , f \left(\right. a \left.\right) \left.\right)$ and $\left(\right. b , f \left(\right. b \left.\right) \left.\right)$ is

$$h \left(\right. x \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \left(\right. x - a \left.\right) + f \left(\right. a \left.\right)$$

For the function $f$ to be convex, this line must lie above the graph of $f$ for every $x$ in the interval between $a$ and $b$. This requirement can be expressed by the inequality $h \left(\right. x \left.\right) > f \left(\right. x \left.\right)$ which explicitly becomes:

$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \left(\right. x - a \left.\right) + f \left(\right. a \left.\right) > f \left(\right. x \left.\right)$$

Rearranging the terms yields:

$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \left(\right. x - a \left.\right) > f \left(\right. x \left.\right) - f \left(\right. a \left.\right)$$

and consequently:

$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} > \frac{f \left(\right. x \left.\right) - f \left(\right. a \left.\right)}{x - a}$$

##### The expression highlights how convexity forces the secant slope over the whole interval $\left[\right. a , b \left]\right.$ to dominate the slopes over any shorter subinterval starting at $a$ (for example the line that connects $\left(\right. f , f \left(\right. a \left.\right) \left.\right) \left.\right)$ and $\left(\right. k , f \left(\right. k \left.\right) \left.\right)$.

## Concavity

A function $f$ is concave on an interval when, for any two points $a$ and $b$ in that interval, the line segment joining $\left(\right. a , f \left(\right. a \left.\right) \left.\right)$ and $\left(\right. b , f \left(\right. b \left.\right) \left.\right)$ lies below the graph of $f$ for every point between $a$ and $b$. Equivalently, the chord connecting the two points never rises above the curve.

![The graph illustrates how the concavity of the function ensures that every secant line lies below the curve.](https://algebrica.org/wp-content/uploads/resources/images/convexity-1-2.png "The graph illustrates how the concavity of the function ensures that every secant line lies below the curve.")

In an analogous way to the convex case, the equation of the secant line passing through the points ((a, f(a))) and ((b, f(b))) is

$$h \left(\right. x \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \left(\right. x - a \left.\right) + f \left(\right. a \left.\right)$$

For the function $f$ to be concave, this line must lie *below* the graph of $f$ for every $x$ in the interval between $a$ and $b$. This condition can be expressed by the inequality (h(x) < f(x)), which explicitly becomes:

$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \left(\right. x - a \left.\right) + f \left(\right. a \left.\right) < f \left(\right. x \left.\right)$$

Rearranging the terms yields:

$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \left(\right. x - a \left.\right) < f \left(\right. x \left.\right) - f \left(\right. a \left.\right)$$

and consequently:

$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} < \frac{f \left(\right. x \left.\right) - f \left(\right. a \left.\right)}{x - a}$$

##### The expression illustrates how concavity forces the secant slope over the entire interval $\left[\right. a , b \left]\right.$ to be smaller than the slopes over any shorter subinterval starting at $a$ (such as the line connecting $\left(\right. a , f \left(\right. a \left.\right) \left.\right)$ and $\left(\right. k , f \left(\right. k \left.\right) \left.\right)$.

## Second derivative criteria for convexity and concavity

A direct way to determine the curvature of a function, in terms of concavity and convexity, is to examine its second derivative. If a function $f \left(\right. x \left.\right)$ is differentiable, the behaviour of its second derivative $f^{''} \left(\right. x \left.\right)$ identifies the intervals where the function is concave or convex. In other words, we have:

- $f^{''} \left(\right. x \left.\right) > 0$, the function $f \left(\right. x \left.\right)$ is convex.
- $f^{''} \left(\right. x \left.\right) < 0$, the function $f \left(\right. x \left.\right)$ is concave.
- Points where $f^{''} \left(\right. x \left.\right) = 0$ are candidates for changes in curvature, marking where the function may switch between concavity and convexity.

---

Let us consider, for example, a simple [polynomial function](https://algebrica.org/polynomial-function/):

$$f \left(\right. x \left.\right) = x^{3} - 3 x^{2} + 2 x$$

We examine the concavity and convexity of the function by analysing the behaviour of its second derivative. As a first step, we compute the first derivative of $f \left(\right. x \left.\right)$, which, being a polynomial, can be obtained immediately:

$$f^{'} \left(\right. x \left.\right) = 3 x^{2} - 6 x + 2$$

By solving the associated [quadratic inequality](https://algebrica.org/quadratic-inequalities/), we identify the values for which the first derivative is positive or negative, and therefore the intervals on which $f \left(\right. x \left.\right)$ is increasing or decreasing. For:

$$f^{'} \left(\right. x \left.\right) = 3 x^{2} - 6 x + 2 > 0$$

we obtain:

$$x < \frac{3 - \sqrt{3}}{3} \lor x > \frac{3 + \sqrt{3}}{3}$$

By plotting the solutions on the real line, we can visualize the intervals where the function $f \left(\right. x \left.\right)$ is increasing or decreasing:

|  |  | $$\frac{3 - \sqrt{3}}{3}$$ | $$\frac{3 + \sqrt{3}}{3}$$ |
| --- | --- | --- | --- |
| $f^{'} \left(\right. x \left.\right)$ | $+$ | $-$ | $+$ |
| $f \left(\right. x \left.\right)$ | $\nearrow$ | $\searrow$ | $\nearrow$ |

We now analyse the behaviour of $f \left(\right. x \left.\right)$ with respect to its convexity and concavity. To do so, we compute the second derivative of $f \left(\right. x \left.\right)$, which is given by:

$$f^{''} \left(\right. x \left.\right) = 6 x - 6 = 0$$

The equation is satisfied at $x = 1$. For $x < 1$, the second derivative is negative, which means that the function is concave on this interval. For $x > 1$, the second derivative becomes positive, so the function is convex.

|  |  | $$1$$ |
| --- | --- | --- |
| $f^{''} \left(\right. x \left.\right)$ | $-$ | $+$ |
| $f \left(\right. x \left.\right)$ | $\cap$ | $\cup$ |
| Concavity | Downward | Upward |

At $x = 1$, the second derivative becomes zero, which shows that the function has an [inflection point](https://algebrica.org/maximum-minimum-and-inflection-points/) at $\left(\right. 1 , 0 \left.\right)$. In fact, we have:

$$f \left(\right. 1 \left.\right) = 13 - 3 \cdot 12 + 2 \cdot 1 = 0$$

##### This confirms the effectiveness of the second derivative in describing changes in curvature and detecting inflection points.
