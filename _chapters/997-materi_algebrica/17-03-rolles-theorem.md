---
layout: chapter
title: "Rolle’s Theorem"
chapter: "Differential Calculus Theorems"
chapter_order: 17
section_order: 3
permalink: /materi-algebrica/differential-calculus-theorems/rolles-theorem/
---

## Statement

Given a function $f \left(\right. x \left.\right)$ defined on a closed and bounded interval $\left[\right. a , b \left]\right.$, such that the following conditions are satisfied:

- $f \left(\right. x \left.\right)$ is [continuous](https://algebrica.org/continuous-functions/) on the closed interval $\left[\right. a , b \left]\right.$.
- $f \left(\right. x \left.\right)$ is [differentiable](https://algebrica.org/derivatives) on the open interval $\left(\right. a , b \left.\right)$.
- $f \left(\right. a \left.\right) = f \left(\right. b \left.\right)$.

Then, there exists at least one point $c \in \left(\right. a , b \left.\right)$ such that $f^{'} \left(\right. c \left.\right) = 0$

###### Rolle’s Theorem is a special case of the [Mean Value Theorem](https://algebrica.org/lagrange-theorem/) (Lagrange). Under the same hypotheses of continuity on $\left[\right. a , b \left]\right.$ and differentiability on $\left(\right. a , b \left.\right)$, if $f \left(\right. a \left.\right) = f \left(\right. b \left.\right)$, then the secant slope is zero and there exists $c \in \left(\right. a , b \left.\right)$ such that \( f’(c) = 0 ).

## A geometric view of Rolle’s theorem

From a geometric point of view, Rolle’s theorem states that there always exists at least one point $c$ where the tangent to the graph is parallel to the line $A B$ passing through the points $A$ and $B$, and thus parallel to the $x$-axis.

![](https://algebrica.org/wp-content/uploads/resources/images/rolle-theorem-1-1.png)

##### Rolle’s Theorem helps illustrate the idea that a function reaching the same value at two points must have a flat tangent somewhere in between. This concept underlies many real-world applications, such as finding the peak of a parabolic trajectory.

## Proof

By the [Weierstrass’s Theorem](https://algebrica.org/weierstrass-theorem/), since $f \left(\right. x \left.\right)$ is continuous on $\left[\right. a , b \left]\right.$, it attains a maximum and a minimum on $\left[\right. a , b \left]\right.$. Let:

$$M = f \left(\right. x_{M} \left.\right) , m = f \left(\right. x_{m} \left.\right)$$

where $x_{M} , x_{m} \in \left[\right. a , b \left]\right.$ are points where $f \left(\right. x \left.\right)$ reaches its maximum $M$ and minimum $m$, respectively. If $M = m$, the function $f \left(\right. x \left.\right)$ is constant, and hence for all $x \in \left(\right. a , b \left.\right)$ $f^{'} \left(\right. x \left.\right) = 0$. In this case, the theorem is trivially true.

---

Now assume $M > m$. Since $f \left(\right. a \left.\right) = f \left(\right. b \left.\right)$, if both the maximum and the minimum were attained only at the endpoints, we would have $f \left(\right. a \left.\right) = f \left(\right. b \left.\right) = M = m$, contradicting $M > m$. Therefore, at least one of $M$ or $m$ is attained at some interior point $c \in \left(\right. a , b \left.\right)$.

- $f \left(\right. x \left.\right)$ reaches a local maximum at $c \in \left(\right. a , b \left.\right)$: since $f$ is differentiable at $c$ and $c$ is an interior extremum, by [Fermat’s Theorem](https://algebrica.org/fermat-theorem/) the derivative satisfies $f^{'} \left(\right. c \left.\right) = 0.$
- $f \left(\right. x \left.\right)$ reaches a local minimum at $c \in \left(\right. a , b \left.\right)$: similarly, by [Fermat’s Theorem](https://algebrica.org/fermat-theorem/), the derivative satisfies: $f^{'} \left(\right. c \left.\right) = 0.$

Thus, in both cases, there exists at least one $c \in \left(\right. a , b \left.\right)$ such that $f^{'} \left(\right. c \left.\right) = 0.$

## Failure of the hypotheses in Rolle’s Theorem

Rolle’s Theorem is a conditional statement, and its conclusion is valid only if all three hypotheses are satisfied simultaneously. To demonstrate the necessity of each condition, it is instructive to analyse cases where one hypothesis is omitted.

---

The first hypothesis requires continuity on the closed interval $\left[\right. a , b \left]\right.$, so consider the following function:

$$f \left(\right. x \left.\right) = \left{\right. x & \text{if} x \in \left[\right. 0 , 1 \left.\right) \\ 0 & \text{if} x = 1$$

This function satisfies $f \left(\right. 0 \left.\right) = f \left(\right. 1 \left.\right) = 0$ and is differentiable on $\left(\right. 0 , 1 \left.\right)$ with derivative $f^{'} \left(\right. x \left.\right) = 1$ throughout the open interval. However, there is no point $c \in \left(\right. 0 , 1 \left.\right)$ where $f^{'} \left(\right. c \left.\right) = 0$. The failure arises from a jump discontinuity at $x = 1$, violating the continuity hypothesis. The derivative remains nonzero because the function increases strictly until the discontinuity.

---

The second hypothesis requires differentiability on the open interval $\left(\right. a , b \left.\right)$. The absolute value function $f \left(\right. x \left.\right) = \left|\right. x \left|\right.$ on $\left[\right. - 1 , 1 \left]\right.$ is continuous on the closed interval and satisfies $f \left(\right. - 1 \left.\right) = f \left(\right. 1 \left.\right) = 1$, so the first and third hypotheses are met. However, at $x = 0$, the function has a corner and the derivative does not exist.

The left and right derivatives at this point are $- 1$ and $1$, respectively, indicating non-differentiability on all of $\left(\right. - 1 , 1 \left.\right)$. Consequently, there is no horizontal tangent in the interior, demonstrating that differentiability is essential.

---

The third hypothesis requires that the function values at the endpoints are equal. A strictly monotonic function can be continuous and differentiable everywhere, yet may lack an interior stationary point. For example, $f \left(\right. x \left.\right) = x$ on $\left[\right. 0 , 1 \left]\right.$ satisfies $f \left(\right. 0 \left.\right) \neq f \left(\right. 1 \left.\right)$.

Since $f^{'} \left(\right. x \left.\right) = 1$ for all $x \in \left(\right. 0 , 1 \left.\right)$, the derivative never vanishes. This demonstrates that equal endpoint values are necessary to guarantee an interior stationary point, regardless of other properties.

## Example

Let’s consider the function:

$$f \left(\right. x \left.\right) = x^{2} - 4 x + 3$$

on the closed interval $\left[\right. 1 , 3 \left]\right.$. We want to verify whether Rolle’s Theorem applies, and if so, find the value of $c$ such that $f^{′} \left(\right. c \left.\right) = 0$.

---

First, we check the three conditions required by Rolle’s Theorem:

- Continuity: the function is a [polynomial](https://algebrica.org/polynomials), so it is continuous on the entire real [line](https://algebrica.org/lines), including the interval $\left[\right. 1 , 3 \left]\right.$.
- Differentiability: since $f \left(\right. x \left.\right)$ is a polynomial, it is differentiable on $\left(\right. 1 , 3 \left.\right)$.
- Let’s now verify that the value of the function at the endpoints is the same:

$$f \left(\right. 1 \left.\right) = 1^{2} - 4 \left(\right. 1 \left.\right) + 3 = 0 f \left(\right. 3 \left.\right) = 3^{2} - 4 \left(\right. 3 \left.\right) + 3 = 0$$

Since all three conditions are satisfied, Rolle’s Theorem guarantees that there is at least one value $c \in \left(\right. 1 , 3 \left.\right)$ such that $f^{′} \left(\right. c \left.\right) = 0$. Let’s find it.

---

We compute the derivative:
$$f^{'} \left(\right. x \left.\right) = 2 x - 4$$

Now solve:
$$f^{′} \left(\right. c \left.\right) = 0 \rightarrow 2 c - 4 = 0 \rightarrow c = 2$$

So, the point $c = 2$ lies within the interval $\left(\right. 1 , 3 \left.\right)$, and at that point, the derivative is zero. This means the function has a horizontal tangent line at $x = 2$, as predicted by Rolle’s Theorem.

## Exercises: check whether Rolle’s Theorem is applicable to the following functions, and if so, find the point $c$ where $f^{′} \left(\right. c \left.\right) = 0.$

- $$\text{1}. f \left(\right. x \left.\right) = \sqrt{4 - x^{2}}$$ [solution](https://algebrica.org/#e1)
- $$\text{2}. f \left(\right. x \left.\right) = \left|\right. x - 1 \left|\right.$$ [solution](https://algebrica.org/#e2)

## Exercise 1

Let’s consider the following function on the closed interval $\left[\right. - 2 , 2 \left]\right.$:

$$f \left(\right. x \left.\right) = \sqrt{4 - x^{2}}$$

This is not a polynomial, but we can still check whether Rolle’s Theorem applies. The function is a square [root](https://algebrica.org/radicals) of a [quadratic expression](https://algebrica.org/quadratic-equations), and it is defined and continuous for all $x$ such that $4 - x^{2} \geq 0$. This [inequality](https://algebrica.org/linear-inequalities) holds exactly on the interval $\left[\right. - 2 , 2 \left]\right.$, so the function is continuous on the entire interval.

---

The function is differentiable on the open interval $\left(\right. - 2 , 2 \left.\right)$ because there are no corners or cusps, and the square root is smooth where defined. The derivative of the function is given by:

$$f^{'} \left(\right. x \left.\right) = \frac{- x}{\sqrt{4 - x^{2}}}$$

The derivative diverges as $x \rightarrow \pm 2$, indicating that the function is not differentiable at the endpoints. However, this does not violate Rolle’s Theorem, which requires differentiability only on the open interval $\left(\right. - 2 , 2 \left.\right)$.

---

Let’s check the values of the function at $x = - 2$ and $x = 2$:

$$& f \left(\right. - 2 \left.\right) = \sqrt{4 - \left(\right. - 2 \left.\right)^{2}} = \sqrt{0} = 0 \\ & f \left(\right. 2 \left.\right) = \sqrt{4 - 2^{2}} = \sqrt{0} = 0$$

Since the function values at the endpoints are equal, all the conditions of Rolle’s Theorem are satisfied.

---

Now we apply the theorem. It tells us that there must be at least one value $c \in \left(\right. - 2 , 2 \left.\right)$ such that the $f^{'} \left(\right. c \left.\right) = 0$. We first compute the derivative:

$$f^{′} \left(\right. x \left.\right) = \frac{- x}{\sqrt{4 - x^{2}}}$$

Now we solve:

$$f^{′} \left(\right. c \left.\right) = 0 \Rightarrow \frac{- c}{\sqrt{4 - c^{2}}} = 0 \rightarrow c = 0$$

The function satisfies all the conditions of Rolle’s Theorem, and the point $c = 0$ is the value where the derivative is zero. So, the function has a horizontal tangent line at $x = 0.$

## Exercise 2

Now let’s consider the following function on the closed interval $\left[\right. 0 , 2 \left]\right.$:

$$f \left(\right. x \left.\right) = \left|\right. x - 1 \left|\right.$$

---

The function $f \left(\right. x \left.\right) = \left|\right. x - 1 \left|\right.$ is an [absolute value function](https://algebrica.org/absolute-value-function). It is continuous on the entire real line, including the interval $\left[\right. 0 , 2 \left]\right.$.

---

To analyze $f \left(\right. x \left.\right) = \left|\right. x - 1 \left|\right.$, observe the following:
$$f \left(\right. x \left.\right) = \left{\right. 1 - x & \text{if} x < 1 \\ x - 1 & \text{if} x \geq 1$$

The left and right derivatives at $x = 1$ are computed as follows. The left derivative is:

$$\underset{h \rightarrow 0^{-}}{lim} \frac{f \left(\right. 1 + h \left.\right) - f \left(\right. 1 \left.\right)}{h} = \underset{h \rightarrow 0^{-}}{lim} \frac{\left|\right. h \left|\right.}{h} = - 1$$

The right derivative is:
$$\underset{h \rightarrow 0^{+}}{lim} \frac{f \left(\right. 1 + h \left.\right) - f \left(\right. 1 \left.\right)}{h} = \underset{h \rightarrow 0^{+}}{lim} \frac{\left|\right. h \left|\right.}{h} = 1$$

Because the left and right derivatives are not equal, the derivative does not exist at $x = 1$.

To apply Rolle’s Theorem, the function must be differentiable on the open interval $\left(\right. 0 , 2 \left.\right)$. But here’s the problem: At $x = 1$, the function has a [corner](https://algebrica.org/points-of-non-differentiability/), which means the derivative does not exist at that point. So the second condition of Rolle’s Theorem fails.

## Selected references

- **Harvard University O. Knill**. [The Mean Value Theorem](https://people.math.harvard.edu/~knill/teaching/math1a_2014/handouts/26-rolle.pdf)
- **UC Davis J. Hunter**. [Differentiable Functions](https://www.math.ucdavis.edu/~hunter/m125a/intro_analysis_ch4.pdf)
- **University of Washington J. Burke**. [Weierstrass Extreme Value Theorem](https://sites.math.washington.edu/~burke/crs/408/lectures/L3-Multivariable-Calc-Review.pdf)
- **University of Chicago J. Murphy**. [Topological Proofs of the Extreme and Intermediate Value Theorems](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2008/REUPapers/Murphy.pdf)
