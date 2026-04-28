---
layout: chapter
title: "Maximum, Minimum, and Inflection Points"
chapter: "Derivatives"
chapter_order: 16
section_order: 7
permalink: /materi-algebrica/derivatives/maximum-minimum-and-inflection-points/
---

## Global maximum and minimum points

The maximum and minimum of a function $f \left(\right. x \left.\right)$ represent, respectively, the highest and lowest values that the function can attain within its [domain](https://algebrica.org/determining-the-domain-of-a-function/). In other words, they indicate the extreme points of the function, showing where $f \left(\right. x \left.\right)$ reaches its greatest possible value or its smallest possible value for all permissible values of $x$ in the given domain.

Given a function $y = f \left(\right. x \left.\right)$ with domain $D$, a point $x_{0} \in D$ is a **global maximum** if $f \left(\right. x_{0} \left.\right) \geq f \left(\right. x \left.\right)$ for every $x \in D$. The value $f \left(\right. x_{0} \left.\right) = M$ is the global maximum of the function.

![Graph of a function f(x) showing a maximum point, where the curve reaches its highest value at a smooth peak.](https://algebrica.org/wp-content/uploads/resources/images/max-min-1.png "Graph of a function f(x) showing a maximum point, where the curve reaches its highest value at a smooth peak.")

---

Given a function $y = f \left(\right. x \left.\right)$ with domain $D$, a point $x_{0} \in D$ is a **global minimum** if $f \left(\right. x_{0} \left.\right) \leq f \left(\right. x \left.\right)$ for every $x \in D$. The value $f \left(\right. x_{0} \left.\right) = m$ is the global minimum of the function.

![Graph of a function f(x) showing a minimum point, where the curve reaches its lowest value at a smooth valley.](https://algebrica.org/wp-content/uploads/resources/images/max-min-2.png)

If the global maximum and global minimum of a function exist, they are unique. By the [Weierstrass’s Theorem](https://algebrica.org/weierstrass-theorem/), if a function is [continuous](https://algebrica.org/continuous-functions/) on a closed and bounded interval $\left[\right. a , b \left]\right.$, then it attains both a global maximum and a global minimum on that interval.

## Local maximum and minimum points

In some cases, a function can display more than one peak or valley within a particular interval. Such points are known as local maxima and local minima. They correspond to positions where the function reaches a relatively highest or lowest value compared to its immediate surroundings, without necessarily being the absolute extremes over the entire domain.

Given a function $y = f \left(\right. x \left.\right)$ defined on an interval $\left[\right. a , b \left]\right.$, the point $x_{0} \in \left[\right. a , b \left]\right.$ is a **local maximum** if there exists a neighborhood $I$ of the point $x_{0}$ such that $f \left(\right. x_{0} \left.\right) \geq f \left(\right. x \left.\right)$ for every $x$ in the interval $I$.

![Graph of a function f(x) showing a local maximum point, where the curve reaches a temporary highest value compared to nearby points.](https://algebrica.org/wp-content/uploads/resources/images/max-min-3-1.png "Graph of a function f(x) showing a local maximum point, where the curve reaches a temporary highest value compared to nearby points.")

In more formal terms, given a function $y = f \left(\right. x \left.\right)$ that is defined and continuous in a neighborhood of the point $x_{0}$, and differentiable in the same neighborhood for every $x \neq x_{0}$, if for every $x$ in the neighborhood the following conditions hold:

$$f^{'} \left(\right. x \left.\right) & > 0 \text{for} x < x_{0} \\ f^{'} \left(\right. x \left.\right) & < 0 \text{for} x > x_{0}$$

then, $x_{0}$ is a point of **local maximum** for the function $f \left(\right. x \left.\right)$. We have:

|  |  | $$x_{0}$$ |
| --- | --- | --- |
| $f^{'} \left(\right. x \left.\right)$ | $+$ | $-$ |
| $f \left(\right. x \left.\right)$ | $\nearrow$ | $\searrow$ |

---

Given a function $y = f \left(\right. x \left.\right)$ defined on an interval $\left[\right. a , b \left]\right.$, the point $x_{0} \in \left[\right. a , b \left]\right.$ is a **local minimum** if there exists a neighborhood $I$ of the point $x_{0}$ such that $f \left(\right. x_{0} \left.\right) \leq f \left(\right. x \left.\right)$ for every $x$ in the interval $I$.

![Graph of a function f(x) showing a local minimum point, where the curve reaches a temporary lowest value compared to nearby points.](https://algebrica.org/wp-content/uploads/resources/images/max-min-4.png "Graph of a function f(x) showing a local minimum point, where the curve reaches a temporary lowest value compared to nearby points.")

If the following conditions hold:

$$f^{'} \left(\right. x \left.\right) & < 0 \text{for} x < x_{0} \\ f^{'} \left(\right. x \left.\right) & > 0 \text{for} x > x_{0}$$

then, $x_{0}$ is a point of **local minimum** for the function $f \left(\right. x \left.\right)$. We have:

|  |  | $$x_{0}$$ |
| --- | --- | --- |
| $f^{'} \left(\right. x \left.\right)$ | $-$ | $+$ |
| $f \left(\right. x \left.\right)$ | $\searrow$ | $\nearrow$ |

---

A function can have at most one global maximum and at most one global minimum, but it can have multiple local maxima and local minima within its domain. By [Fermat’s theorem](https://algebrica.org/fermat-theorem/), the relative maximum and minimum points of a differentiable function, located within the domain of the function, are **stationary points**. This implies that the tangent line at a point of a relative maximum or minimum is parallel to the x-axis. In this case, the [derivative](https://algebrica.org/derivatives/) of the function at $x_{0}$ is zero, and we have $f ′ \left(\right. x_{0} \left.\right) = 0$.

## Upward and downward concavity

We say that the function $f \left(\right. x \left.\right)$ is **concave upward** at $x_{0}$ if there exists a neighborhood $I$ of $x_{0}$ such that, for every $x \in I$ with $x \neq x_{0}$, the function $f \left(\right. x \left.\right)$ takes values greater than those of the line $y = t \left(\right. x \left.\right)$, which is the tangent line to the graph of $f \left(\right. x \left.\right)$ at $x_{0}$.

$$f \left(\right. x \left.\right) > t \left(\right. x \left.\right) \forall x \in I - \left{\right. x_{0} \left.\right}$$

![](https://algebrica.org/wp-content/uploads/resources/images/max-min-5.png)

---

Similarly, we say that the function $f \left(\right. x \left.\right)$ is **concave downward** at $x_{0}$ if there exists a neighborhood $I$ of $x_{0}$ such that, for every $x \in I$ with $x \neq x_{0}$, the function $f \left(\right. x \left.\right)$ takes values less than those of the line $y = t \left(\right. x \left.\right)$.

$$f \left(\right. x \left.\right) < t \left(\right. x \left.\right) \forall x \in I - \left{\right. x_{0} \left.\right}$$

![](https://algebrica.org/wp-content/uploads/resources/images/maximum-minimum-6-1.png)

The concepts of concavity and convexity are discussed in detail and in their analytical formulation in the entry [Convexity and Concavity of Functions](https://algebrica.org/convexity-and-concavity-of-functions/)

## Inflection points and change in concavity

An **inflection point** is a point where the concavity of a function changes.

Let us consider the case where a function $y = f \left(\right. x \left.\right)$ is defined on an interval $\left(\right. a , b \left.\right)$, and let $x_{0} \in \left(\right. a , b \left.\right)$ be either a point where $f \left(\right. x \left.\right)$ is differentiable, or a point where:

$$\underset{x \rightarrow x_{0}}{lim} f^{'} \left(\right. x \left.\right) = + \infty \text{or} \underset{x \rightarrow x_{0}}{lim} f^{'} \left(\right. x \left.\right) = - \infty$$

The point $x_{0}$ is defined as an inflection point if the function changes concavity at $x_{0}$.

![An _inflection point_ is a point where the concavity of a function changes.](https://algebrica.org/wp-content/uploads/resources/images/maximum-minimum-7.png)

An inflection point is called horizontal if the tangent at the inflection point is parallel to the x-axis. When the tangent is parallel to the y-axis, the inflection point is called vertical. In all other cases, as in the case shown in the figure, it is called oblique.

![](https://algebrica.org/wp-content/uploads/resources/images/maximum-minimum-8.png)

$x_{0}$ is an **horizontal inflection point** for a function $f \left(\right. x \left.\right)$ if $f^{'} \left(\right. x \left.\right) = 0$ and the sign of $f^{'} \left(\right. x \left.\right)$ is the same$^{1}$ for every $x \neq x_{0}$ in the neighborhood $I$.

|  |  | $$x_{0}$$ |
| --- | --- | --- |
| $f^{'} \left(\right. x \left.\right)$ | $+$ | $+$ |
| $f \left(\right. x \left.\right)$ | $\nearrow$ | $\nearrow$ |

###### The signs in the neighborhood of $x_{0}$ can be both positive (as in the scheme above) or both negative.

## How to calculate the points of local maximum and minimum

Given a continuous function, to find the local maximum and minimum points, we analyze the sign of the first derivative. The procedure involves the following steps:

- Compute the derivative $f^{'} \left(\right. x \left.\right)$ and determine its domain to identify points where the function is not differentiable (e.g., cusps, corners).
- Study the sign of the derivative by analyzing where $f^{'} \left(\right. x \left.\right)$ is positive, negative, or zero.
- Identify local maxima and minima: a point $x_{0}$ is a local maximum if $f^{'} \left(\right. x \left.\right)$ changes from positive to negative around $x_{0}$. A point $x_{0}$ is a local minimum if $f^{'} \left(\right. x \left.\right)$ changes from negative to positive around $x_{0}$.

## Example 1

Let us calculate the local maximum and minimum points of the following function:

$$y = f \left(\right. x \left.\right) = x^{3} - \frac{1}{2} x^{2}$$

---

Being a [polynomial function](https://algebrica.org/polynomial-function/), it is continuous and differentiable for all $x \in \mathbb{R}$. Therefore, it does not have any points of discontinuity within its domain. Let us now calculate the first derivative of the function. We obtain:

$$f^{'} \left(\right. x \left.\right) = 3 x^{2} - x$$

---

Now, we study the sign of the derivative by imposing:
$$3 x^{2} - x > 0$$

Passing to the associated equation, we obtain:

$$3 x^{2} - x = 0 \Longrightarrow x \left(\right. 3 x - 1 \left.\right) = 0$$

The equation is satisfied for $x = 0$ and $x = \frac{1}{3}$.

---

Returning to the inequality, we obtain that $f^{'} \left(\right. x \left.\right) > 0$ for $x < 0$ and $x > \frac{1}{3}$.

---

Let us now represent the sign chart and observe that the function is increasing for $x < 0$, decreasing for $0 < x < \frac{1}{3}$, and increasing again for $x > \frac{1}{3}$.

|  |  | $$0$$ | $$+ \frac{1}{3}$$ |
| --- | --- | --- | --- |
| $f^{'} \left(\right. x \left.\right)$ | $+$ | $-$ | $+$ |
| $f \left(\right. x \left.\right)$ | $\nearrow$ | $\searrow$ | $\nearrow$ |

---

For ( x = 0 ) the function takes the value $f \left(\right. 0 \left.\right) = 0^{3} - \frac{1}{2} 0^{2} = 0$. The point $\left(\right. 0 , 0 \left.\right)$ is therefore a local maximum.

---

For $x = \frac{1}{3}$, the function takes the value:
$$f \left(\right. \frac{1}{3} \left.\right) & = \left(\left(\right. \frac{1}{3} \left.\right)\right)^{3} - \frac{1}{2} \left(\left(\right. \frac{1}{3} \left.\right)\right)^{2} \\ & = \frac{1}{27} - \frac{1}{2} \times \frac{1}{9} \\ & = - \frac{1}{54}$$

The point $\left(\right. \frac{1}{3} , - \frac{1}{54} \left.\right)$ is therefore a local minimum.
In this way, we have found the local maximum and minimum points of the function $f \left(\right. x \left.\right)$.

## How to determine the concavity of a function

Let $y = f \left(\right. x \left.\right)$ be a continuous function defined in a neighborhood of the point $x_{0}$, along with its first and second derivatives.

If at $x_{0}$ we have $f^{''} \left(\right. x_{0} \left.\right) \neq 0$, then:

- The function is concave upward if $f^{''} \left(\right. x_{0} \left.\right) > 0$.
- The function is concave downward if $f^{''} \left(\right. x_{0} \left.\right) < 0$.

## Example 2

Let us consider the function from Example 1 and determine its [convexity and concavity](https://algebrica.org/convexity-and-concavity-of-functions/):

$$y = f \left(\right. x \left.\right) = x^{3} - \frac{1}{2} x^{2}$$

---

The second derivative of the function is:

$$f^{''} \left(\right. x \left.\right) = 6 x - 1$$

Let us now study the sign by imposing:

$$6 x - 1 > 0 \Longrightarrow x > \frac{1}{6}$$

---

Let’s represent the sign chart, obtaining the intervals in which the function is concave upward or concave downward.

|  |  | $$0$$ |
| --- | --- | --- |
| $f^{''} \left(\right. x \left.\right)$ | $+$ | $-$ |
| $f \left(\right. x \left.\right)$ | $\cup$ | $\cap$ |
| Concavity | Upward | Downward |

In this way, we have obtained the intervals of concavity of the function.

## Identifying inflection points

An inflection point occurs when the concavity of a function changes sign. This change indicates a transition from a concave upward shape to a concave downward shape, or vice versa. To determine if a point is truly an inflection point, we need to verify if the second derivative $f ′ ′ \left(\right. x \left.\right)$ changes sign as we pass through that point.

- A point $x_{0}$ is a horizontal inflection point if:
  $$f^{'} \left(\right. x_{0} \left.\right) = 0 , f^{''} \left(\right. x_{0} \left.\right) = 0$$
  but the concavity changes sign in the neighborhood of $x_{0}$. In this case, the tangent line at $x_{0}$ is horizontal.
- A point $x_{0}$ is a vertical inflection point if the function is not differentiable at $x_{0}$ and the concavity changes sign around $x_{0}$. This type of inflection point often occurs at points with sharp corners or cusps where the function is continuous but not smooth.
- A point $x_{0}$ is an oblique inflection point if:
  $$f^{'} \left(\right. x_{0} \left.\right) \neq 0 , f^{''} \left(\right. x_{0} \left.\right) = 0$$
  and the concavity changes sign around $x_{0}$. In this case, the tangent line is neither horizontal nor vertical but has a non-zero slope.

## Exercises to find maxima, minima, and inflection points of functions

- $$\text{1}. f \left(\right. x \left.\right) = x^{3} - 6 x^{2} + 9 x$$ [solution](https://algebrica.org/)
- $$\text{2}. f \left(\right. x \left.\right) = \frac{x^{2}}{x^{2} + 1}$$ [solution](https://algebrica.org/)
- $$\text{3}. f \left(\right. x \left.\right) = ln ⁡ \left(\right. x^{2} + 1 \left.\right)$$ [solution](https://algebrica.org/)
- $$\text{4}. f \left(\right. x \left.\right) = x e^{- x}$$ [solution](https://algebrica.org/)
- $$\text{5}. f \left(\right. x \left.\right) = sin ⁡ \left(\right. x \left.\right) + cos ⁡ \left(\right. x \left.\right)$$ [solution](https://algebrica.org/)
- $$\text{5}. f \left(\right. x \left.\right) = x^{2} ln ⁡ \left(\right. x \left.\right)$$ [solution](https://algebrica.org/)

##### The proposed functions are carefully designed to help you consolidate your understanding of local maxima, minima, and inflection points. Each function requires you to compute the first and second derivatives, identify critical points, and analyze concavity changes. Some are more direct, while others involve algebraic manipulation or mixed expressions ([polynomial](https://algebrica.org/polynomials), [exponential](https://algebrica.org/exponential-function/), [logarithmic](https://algebrica.org/logarithms/), or [trigonometric](https://algebrica.org/unit-circle/)). Try to determine and classify all relevant points independently before checking the solutions.
