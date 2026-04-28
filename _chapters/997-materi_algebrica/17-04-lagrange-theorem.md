---
layout: chapter
title: "Lagrange’s Theorem"
chapter: "Differential Calculus Theorems"
chapter_order: 17
section_order: 4
permalink: /materi-algebrica/differential-calculus-theorems/lagranges-theorem/
---

## Statement

The Lagrange’s theorem, also known as the mean value theorem, states the following. Consider a function $f \left(\right. x \left.\right)$, [continuous](https://algebrica.org/continuous-functions/) in the closed and bounded interval $\left[\right. a , b \left]\right.$ and differentiable at every point inside the interval. Then, there exists at least one point $c$ inside the interval such that the following relation holds:

$$f^{'} \left(\right. c \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$

##### This means that there exists at least one point where the derivative of the function is equal to the slope of the secant line connecting $a$ and $b$. In other words, at some point in the interval, the instantaneous rate of change of the function matches its average rate of change.

## A geometric view of Lagrange’s theorem

From a geometric point of view, the theorem states that there exists at least one point $c$ where the tangent line at that point is parallel to the secant line connecting points $A$ and $B$ on the graph.

![Lagrange’s theorem.](https://algebrica.org/wp-content/uploads/resources/images/lagrange-theoreme-4.png "Lagrange’s theorem.")

In the right-angled triangle $A B H$, we have $\overset{―}{B H} = \overset{―}{A H} \cdot tan ⁡ \alpha$ that is:

$$tan ⁡ \alpha = \frac{\overset{―}{B H}}{\overset{―}{A H}}$$

We have:

$$\overset{―}{B H} = f \left(\right. b \left.\right) - f \left(\right. a \left.\right) , \overset{―}{A H} = b - a$$

The slope of segment $A B$ is equal to $tan ⁡ \alpha$ that is:

$$tan ⁡ \alpha = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$

Since the tangent at $c$ to the curve is parallel to $A B$, both have the same slope, hence:

$$f^{'} \left(\right. c \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$

## Proof

To prove Lagrange’s theorem we define an auxiliary function $\varphi \left(\right. x \left.\right)$ as follows:

$$\varphi \left(\right. x \left.\right) = f \left(\right. x \left.\right) - f \left(\right. a \left.\right) - \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \cdot \left(\right. x - a \left.\right)$$

We verify that $\varphi \left(\right. x \left.\right)$ satisfies the hypotheses of [Rolle’s Theorem](https://algebrica.org/rolles-theorem/):

- $f \left(\right. x \left.\right)$ is continuous on the closed interval $\left[\right. a , b \left]\right.$.
- $f \left(\right. x \left.\right)$ is differentiable on the open interval $\left(\right. a , b \left.\right)$.
- $\varphi \left(\right. a \left.\right) = \varphi \left(\right. b \left.\right)$.

By calculating $\varphi \left(\right. a \left.\right)$ and $\varphi \left(\right. b \left.\right)$, we obtain:

$$\varphi \left(\right. a \left.\right) = f \left(\right. a \left.\right) - f \left(\right. a \left.\right) - \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \cdot \left(\right. a - a \left.\right) = 0$$

$$\varphi \left(\right. b \left.\right) & = f \left(\right. b \left.\right) - f \left(\right. a \left.\right) - \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} \cdot \left(\right. b - a \left.\right) \\ & = f \left(\right. b \left.\right) - \left(\right. f \left(\right. b \left.\right) - f \left(\right. a \left.\right) \left.\right) = 0$$

Therefore, $\varphi \left(\right. a \left.\right) = \varphi \left(\right. b \left.\right) = 0$.

---

Applying Rolle’s Theorem to $\varphi \left(\right. x \left.\right)$, we find that there exists at least one point $c$ within the interval $\left]\right. a , b \left[\right.$ such that $\varphi^{'} \left(\right. c \left.\right) = 0$. Calculating the derivative of $\varphi \left(\right. x \left.\right)$, we have:

$$\varphi^{'} \left(\right. x \left.\right) = f^{'} \left(\right. x \left.\right) - \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$

---

Now, we calculate the derivative of $\varphi \left(\right. x \left.\right)$ at the point $c$ and set it equal to 0. From this, we obtain:

$$\varphi^{'} \left(\right. c \left.\right) = f^{'} \left(\right. c \left.\right) - \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a} = 0$$

That is:

$$f^{'} \left(\right. c \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$

which corresponds exactly to the thesis we wanted to prove.

## A special case: when the derivative is zero everywhere

From Lagrange’s theorem, it follows that if a function $f \left(\right. x \left.\right)$ is continuous on the interval $\left[\right. a , b \left]\right.$, differentiable on the interval $\left]\right. a , b \left[\right.$, and $f^{'} \left(\right. x \left.\right)$ is zero at every point in the interior of the interval, then $f \left(\right. x \left.\right)$ is constant on the entire interval $\left[\right. a , b \left]\right.$.

![](https://algebrica.org/wp-content/uploads/resources/images/lagrange-theorem-2.png)

Indeed, if we take a point $\overset{―}{x} \in \left[\right. a , b \left]\right.$ and apply the theorem to the interval $\left[\right. a , \overset{―}{x} \left]\right.$, then there exists a point $c \in \left]\right. a , \overset{―}{x} \left[\right.$ such that:
$$f^{'} \left(\right. c \left.\right) = \frac{f \left(\right. \overset{―}{x} \left.\right) - f \left(\right. a \left.\right)}{\overset{―}{x} - a}$$

Since $f^{'} \left(\right. \overset{―}{x} \left.\right) = 0$ for every point in $\left]\right. a , b \left[\right.$, it follows that $f^{'} \left(\right. c \left.\right) = 0$ as well. For this reason, it must be:

$$f \left(\right. \overset{―}{x} \left.\right) – f \left(\right. a \left.\right) = 0 \rightarrow f \left(\right. \overset{―}{x} \left.\right) = f \left(\right. a \left.\right) \forall \overset{―}{x} \in \left[\right. a , b \left]\right.$$

For this reason, $f$ is constant on the entire interval $\left[\right. a , b \left]\right.$.

## A numerical example

To see the theorem at work, let us examine a concrete case. We want to identify a point $c$ inside a given interval where the instantaneous rate of change of a function coincides with its average rate of change on that interval. The computation also shows that such a point is not something one can usually predict by inspection. Consider the [polynomial](https://algebrica.org/polynomials/):

$$f \left(\right. x \left.\right) = x^{3} - 4 x^{2} + x + 6$$

on the closed interval $\left[\right. 1 , 4 \left]\right.$. Being a polynomial, $f$ is [continuous](https://algebrica.org/continuous-functions/) on $\left[\right. 1 , 4 \left]\right.$ and differentiable on $\left(\right. 1 , 4 \left.\right)$. The assumptions of Lagrange’s theorem are therefore satisfied. We begin by evaluating the function at the endpoints:

$$f \left(\right. 1 \left.\right) = 1 - 4 + 1 + 6 = 4$$
$$f \left(\right. 4 \left.\right) = 64 - 64 + 4 + 6 = 10$$

The slope of the secant line through the points $\left(\right. 1 , 4 \left.\right)$ and $\left(\right. 4 , 10 \left.\right)$ is

$$\frac{f \left(\right. 4 \left.\right) - f \left(\right. 1 \left.\right)}{4 - 1} = \frac{10 - 4}{3} = 2$$

This number represents the average rate of change of $f$ over $\left[\right. 1 , 4 \left]\right.$. Next we compute the derivative:

$$f^{'} \left(\right. x \left.\right) = 3 x^{2} - 8 x + 1$$

We look for values of $c$ such that $f^{'} \left(\right. c \left.\right) = 2.$ This leads to the equation:

$$3 c^{2} - 8 c + 1 = 2$$
$$3 c^{2} - 8 c - 1 = 0$$

Applying the [quadratic formula](https://algebrica.org/quadratic-formula/) gives:

$$c = \frac{8 \pm \sqrt{64 + 12}}{6} = \frac{8 \pm \sqrt{76}}{6} = \frac{4 \pm \sqrt{19}}{3}$$

We obtain two candidates:

$$c_{1} = \frac{4 - \sqrt{19}}{3} \approx 0.21$$
$$c_{2} = \frac{4 + \sqrt{19}}{3} \approx 2.79$$

Lagrange’s theorem guarantees a solution inside the open interval $\left]\right. 1 , 4 \left[\right.$. Among the two values found, only:

$$c = \frac{4 + \sqrt{19}}{3} \approx 2.79$$

lies in $\left]\right. 1 , 4 \left[\right.$. The other root falls outside the interval and is therefore not relevant in this context. At this point, the tangent line to the graph of $f$ is parallel to the secant line joining $\left(\right. 1 , 48 \left.\right)$ and $\left(\right. 4 , 10 \left.\right)$.

###### This example shows that the equation $f^{'} \left(\right. c \left.\right) = 2$ may admit more than one solution, yet only those inside the interval are meaningful for the theorem.

The solution is:
$$c = \frac{4 + \sqrt{19}}{3}$$

## Selected references

- **Harvard University, O. Knill**. [The Mean Value Theorem](https://people.math.harvard.edu/~knill/teaching/math1a_2014/handouts/26-rolle.pdf)
- **Stony Brook University**. [Lecture 18: Mean Value Theorem](https://www.math.stonybrook.edu/Videos/MAT131Online/Handouts/Lecture-18-Handout.pdf)
- **University of California Davis, D. Kouba**. [Mean Value Theorem – Problems and Proofs](https://www.math.ucdavis.edu/~kouba/CalcOneDIRECTORY/meanvaluetheoremdirectory/MeanValueTheorem.html)
- **University of Cambridge, W. T. Gowers**. [What is the point of the Mean Value Theorem?](https://www.dpmms.cam.ac.uk/~wtg10/meanvalue.html)
