---
layout: chapter
title: "Definite Integrals"
chapter: "Integrals"
chapter_order: 18
section_order: 2
permalink: /materi-algebrica/integrals/definite-integrals/
---

## Area under a function: from curve to integral

To introduce the concept of the definite integral, consider a [function](https://algebrica.org/functions/) $f \left(\right. x \left.\right)$ defined on a [closed interval](https://algebrica.org/intervals/) $\left[\right. a , b \left]\right.$. The definite integral of the function $f \left(\right. x \left.\right)$ over this interval is defined as the oriented area of the region bounded by the graph of the function, the x -axis, and the vertical lines $x = a$ and $x = b$, and it is represented by the formula:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x$$

Given a function $y = f \left(\right. x \left.\right)$ and a closed and bounded interval $\left[\right. a , b \left]\right.$ where the function is [continuous](https://algebrica.org/continuous-functions/), a curvilinear trapezoid is the planar region bounded by the graph of $f \left(\right. x \left.\right)$, the x-axis, and the vertical lines $x = a$ and $x = b$.

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-1.png)

This region is essentially a quadrilateral with a curved top, and its area, as illustrated in the diagram, cannot be straightforwardly determined using the classical formulas for plane figures from geometry. The challenge lies in the irregularity of the curve, which requires a more sophisticated approach to measure the area accurately.

## Approximating area with rectangular sums

In principle, the area of the curvilinear trapezoid can be approximated by considering a sequence of $n$ subintervals obtained by dividing the segment $\left[\right. a , b \left]\right.$ into equal parts. The width of each subinterval is calculated using the formula:

$$\Delta x = \frac{b - a}{n}$$

This approach breaks down the complex region into simpler shapes whose areas can be more easily calculated and then summed to approximate the total area of the curvilinear trapezoid.

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-2.png)

Let $m_{i}$ be the minimum value assumed by the function $f \left(\right. x \left.\right)$ within the i-th subinterval. The area of the curvilinear trapezoid is then approximated from below by $s_{n}^{-}$, which represents the sum of the areas of all these $n$ rectangles:

$$s_{n}^{-} = m_{1} \Delta x_{1} + m_{2} \Delta x_{2} + \ldots + m_{n} \Delta x_{n} = \sum_{i = 1}^{n} m_{i} \Delta x_{i}$$

This approximation is a lower sum because it uses the minimum value of the function in each subinterval. Similarly, we can calculate the upper sum given by:

$$s_{n}^{+} = M_{1} \Delta x_{1} + M_{2} \Delta x_{2} + \ldots + M_{n} \Delta x_{n} = \sum_{i = 1}^{n} M_{i} \Delta x_{i}$$

Where $M_{i}$ is the maximum value of the function $f \left(\right. x \left.\right)$ within the i-th subinterval.

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-3.png)

The two sums, therefore, represent a lower and an upper approximation of the area of the curvilinear trapezoid we want to determine. As the widths $\Delta x$ of the rectangles become smaller, these sums provide a more accurate approximation of the area of the curvilinear trapezoid. When the widths $\Delta x$ approach zero, the upper and lower sums converge to the same value $I$. This common [limit](https://algebrica.org/limits) of the two sums is precisely the value of the definite integral. This approach, based on the convergence of lower and upper sums, is known as the [Riemann definition](https://algebrica.org/riemann-integrability-criteria/) of the integral.

A function $f \left(\right. x \left.\right)$ that is bounded on a closed interval $\left[\right. a , b \left]\right.$ is said to be integrable if:

$$\underset{\Delta x \rightarrow 0}{lim} s_{n}^{-} = \underset{\Delta x \rightarrow 0}{lim} s_{n}^{+} = I$$

The value $I$ is called the definite integral of $f \left(\right. x \left.\right)$ over $\left[\right. a , b \left]\right.$ and is defined as:

$$I = \int_{a}^{b} f \left(\right. x \left.\right) d x$$

The endpoints $\left[\right. a , b \left]\right.$ of the interval are called the limits of integration, where $a$ is the lower limit and $b$ is the upper limit. The function $f \left(\right. x \left.\right)$ is called the integrand. From a geometric perspective, the quantities $d x$ and $f \left(\right. x \left.\right)$ represent, respectively, the base and the height of infinitesimal rectangles used to approximate the area under the curve.

## Computing definite integrals

How can we practically calculate the value of a definite integral? If $f \left(\right. x \left.\right)$ is a continuous function on $\left[\right. a , b \left]\right.$ and $F \left(\right. x \left.\right)$ is any [antiderivative](https://algebrica.org/indefinite-integrals) of $f \left(\right. x \left.\right)$, then the following holds:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$$

- $F \left(\right. x \left.\right)$ is such that $F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$ for all $x \in \left[\right. a , b \left]\right.$.
- $F \left(\right. b \left.\right)$ and $F \left(\right. a \left.\right)$ represent the values of the antiderivative evaluated at the upper and lower limits of integration, respectively.

This formula is the conclusion of the Second Fundamental Theorem of Calculus, which proves that for any continuous function $f$ on $\left[\right. a , b \left]\right.$, the definite integral can be computed by evaluating an antiderivative at the two endpoints of the interval. The Second Theorem builds on the First Fundamental Theorem of Calculus, which shows that the function defined by accumulating area from a fixed point:

$$F \left(\right. x \left.\right) = \int_{a}^{x} f \left(\right. t \left.\right) d t$$

is differentiable, and its derivative is exactly the original function: $F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$. This is what makes differentiation and integration inverse operations in a precise sense. Both results, along with their proofs and examples, are covered in the dedicated page on the [Fundamental Theorem of Calculus](https://algebrica.org/fundamental-theorem-of-calculus/).

## Properties

When the two [limits](https://algebrica.org/limits) of integration coincide, the integral is zero:

$$\int_{a}^{a} f \left(\right. x \left.\right) d x = 0$$

This follows directly from the definition: if the interval has no width, there is no area to accumulate.

---

Reversing the limits of integration changes the sign of the integral:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = - \int_{b}^{a} f \left(\right. x \left.\right) d x$$

This reflects the oriented nature of the definite integral. When you integrate from $b$ to $a$ instead of from $a$ to $b$, you are traversing the interval in the opposite direction, and the sign of the accumulated area flips accordingly.

---

If a function $f \left(\right. x \left.\right)$ is constant over the interval $\left[\right. a , b \left]\right.$, meaning $f \left(\right. x \left.\right) = k$, then the definite integral can be calculated as follows:

$$\int_{a}^{b} k d x = k \left(\right. b - a \left.\right)$$

This result comes from the fact that the area under a constant function is simply a rectangle with height $k$ and base $b - a$.

---

If $f \left(\right. x \left.\right)$ is continuous on $\left[\right. a , b \left]\right.$ and $k$ is a constant, the constant factor can be moved outside the integral:

$$\int_{a}^{b} k \cdot f \left(\right. x \left.\right) d x = k \int_{a}^{b} f \left(\right. x \left.\right) d x$$

This property, combined with the additivity of the integral over sums, is what makes the definite integral a linear operator.

---

If $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are continuous functions on $\left[\right. a , b \left]\right.$, then their sum $f \left(\right. x \left.\right) + g \left(\right. x \left.\right)$ is also continuous on $\left[\right. a , b \left]\right.$. The integral of the sum of these functions is given by:

$$\int_{a}^{b} \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) d x = \int_{a}^{b} f \left(\right. x \left.\right) d x + \int_{a}^{b} g \left(\right. x \left.\right) d x$$

---

If $f \left(\right. x \left.\right)$ is continuous on an interval and $a$, $b$, and $c$ are points within this interval, then the following property holds:

$$\int_{a}^{c} f \left(\right. x \left.\right) d x = \int_{a}^{b} f \left(\right. x \left.\right) d x + \int_{b}^{c} f \left(\right. x \left.\right) d x$$

---

Now, let’s consider the comparison between the integrals of two functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ that are continuous on an interval $\left[\right. a , b \left]\right.$ and such that $f \left(\right. x \left.\right) \leq g \left(\right. x \left.\right)$ for every point in the interval. If these conditions hold, then:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x \leq \int_{a}^{b} g \left(\right. x \left.\right) d x$$

This property states that if one function is always less than or equal to another on the interval $\left[\right. a , b \left]\right.$, then the integral of the first function is less than or equal to the integral of the second function.

##### This is known as the Comparison Property of Integrals and is essential for establishing inequalities involving integrals. In geometric terms, this means that the area under the curve of the function $f \left(\right. x \left.\right)$ is less than or equal to the area under the curve of the function $g \left(\right. x \left.\right)$.

## Mean Value Theorem for Integrals

If $f \left(\right. x \left.\right)$ is continuous on $\left[\right. a , b \left]\right.$, then there exists at least one point $c \in \left(\right. a , b \left.\right)$ such that:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = f \left(\right. c \left.\right) \left(\right. b - a \left.\right)$$

The value $f ©$ is the average value of the function over the interval. Geometrically, this means that there is always a rectangle with base $b - a$ and height $f ©$ whose area equals exactly the area under the curve. The theorem guarantees the existence of such a point, but does not tell us how to find it — that depends on the specific function.

The average value of $f$ over $\left[\right. a , b \left]\right.$ can be written explicitly as:

$$f \left(\right. c \left.\right) = \frac{1}{b - a} \int_{a}^{b} f \left(\right. x \left.\right) d x$$

##### The Mean Value Theorem for Integrals is the integral counterpart of [Lagrange’s Mean Value Theorem](https://algebrica.org/lagrange-theorem/). While the latter guarantees a point where the instantaneous rate of change equals the average rate of change, this theorem guarantees a point where the function value equals the average value over the interval. Both results say something similar: continuous functions cannot avoid their averages.

## Example 1

Let’s calculate the definite integral of the following function:

$$\int_{0}^{3} \left(\right. 3 x - x^{2} \left.\right) d x$$

##### Before proceeding with the calculations, it is useful to delve into the method of finding [antiderivatives](https://algebrica.org/indefinite-integrals) of functions and their properties.

---

By applying the property of linearity, the integral can be split into two separate integrals:

$$\int_{0}^{3} 3 x d x - \int_{0}^{3} x^{2} d x$$

By moving the constant factor outside the first integral:

$$3 \int_{0}^{3} x d x - \int_{0}^{3} x^{2} d x$$

---

Computing the antiderivative of each term, we obtain:

$$F \left(\right. x \left.\right) = \frac{3 x^{2}}{2} - \frac{x^{3}}{3}$$

---

Applying the Second Fundamental Theorem of Calculus, $F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$, with $a = 0$ and $b = 3$:

$$F \left(\right. 3 \left.\right) - F \left(\right. 0 \left.\right) & = \left(\right. \frac{3 \cdot 9}{2} - \frac{27}{3} \left.\right) - \left(\right. \frac{3 \cdot 0}{2} - \frac{0}{3} \left.\right) \\ & = \frac{27}{2} - 9 - 0 \\ & = \frac{27 - 18}{2} \\ & = \frac{9}{2}$$

Therefore, the area of the plane figure bounded by the [parabolic](https://algebrica.org/parabola) arc and the $x$-axis over $\left[\right. 0 , 3 \left]\right.$ is:

$$\frac{9}{2}$$

This is just a simple example that generally shows the procedure for calculating definite integrals. Very often, integrals are not so straightforward to compute, and it is necessary to resort to other solving methods such as [substitution](https://algebrica.org/integration-by-substitution/) and [integration by parts](https://algebrica.org/integration-by-parts/).

## Example 2

Let’s calculate the definite integral of the following function:

$$\int_{0}^{\pi} \left(\right. x + sin ⁡ \left(\right. x \left.\right) \left.\right) d x$$

##### This example combines a polynomial term with a trigonometric function. Before proceeding, it may be useful to review the [integrals of trigonometric functions](https://algebrica.org/integral-of-trigonometric-functions/).

---

By applying the property of linearity, the integral can be split into two separate integrals:

$$\int_{0}^{\pi} x d x + \int_{0}^{\pi} sin ⁡ \left(\right. x \left.\right) d x$$

---

Computing the antiderivative of each term:

$$F \left(\right. x \left.\right) = \frac{x^{2}}{2} - cos ⁡ \left(\right. x \left.\right)$$

---

Applying the Second Fundamental Theorem of Calculus, $F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$, with $a = 0$ and $b = \pi$:

$$F \left(\right. \pi \left.\right) - F \left(\right. 0 \left.\right) & = \left(\right. \frac{\pi^{2}}{2} - cos ⁡ \left(\right. \pi \left.\right) \left.\right) - \left(\right. \frac{0^{2}}{2} - cos ⁡ \left(\right. 0 \left.\right) \left.\right) \\ & = \left(\right. \frac{\pi^{2}}{2} + 1 \left.\right) - \left(\right. 0 - 1 \left.\right) \\ & = \frac{\pi^{2}}{2} + 1 + 1 \\ & = \frac{\pi^{2}}{2} + 2$$

Therefore, the area of the plane figure bounded by the curve $x + sin ⁡ \left(\right. x \left.\right)$ and the $x$-axis over $\left[\right. 0 , \pi \left]\right.$ is:

$$\frac{\pi^{2}}{2} + 2$$

## Handling definite integrals with positive and negative areas

We have seen that the definite integral represents the area of the region bounded by the graph of $f \left(\right. x \left.\right)$, the x-axis, and the vertical lines $x = a$ and $x = b$.

$$\int_{a}^{b} f \left(\right. x \left.\right) d x$$

This is true when $f \left(\right. x \left.\right)$ is always greater than zero over the interval where we are calculating the area of the curvilinear trapezoid. However, when $f \left(\right. x \left.\right)$ changes sign within the interval $\left[\right. a , b \left]\right.$, we must proceed differently. We can observe such behavior in the following image:

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-4.png)

In this case, the interval $\left[\right. a , b \left]\right.$ must be divided into subintervals where the function maintains the same sign. For example, $\left[\right. a , c \left]\right.$ where the function $f \left(\right. x \left.\right)$ is positive, and $\left[\right. c , b \left]\right.$ where the function is negative.

The definite integrals are then calculated separately over each subinterval, and the results are combined algebraically, taking into account their signs. This process ensures that areas below the x-axis are counted as negative, while areas above the x-axis are counted as positive. In this case we have:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = \int_{a}^{c} f \left(\right. x \left.\right) d x + \int_{c}^{b} f \left(\right. x \left.\right) d x$$

---

In the case of an [even function](https://algebrica.org/even-and-odd-functions/) (symmetric with respect to the y-axis), the area between $\left[\right. - a , 0 \left]\right.$ is equal to the area between $\left[\right. 0 , a \left]\right.$. Therefore, the definite integral is equal to:

$$\int_{- a}^{a} f \left(\right. x \left.\right) d x = 2 \int_{0}^{a} f \left(\right. x \left.\right) d x$$

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-5.png)

---

In the case of an [odd function](https://algebrica.org/even-and-odd-functions/) (symmetric with respect to the origin), the area between $\left[\right. - a , 0 \left]\right.$ is equal in magnitude but opposite in sign to the area between $\left[\right. 0 , a \left]\right.$. Therefore, the definite integral is equal to:

$$\int_{- a}^{a} f \left(\right. x \left.\right) d x = 0$$

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-6.png)

In the case of an even function, the area enclosed between the graph of $f \left(\right. x \left.\right)$ and the $x$-axis over $\left[\right. - a , a \left]\right.$ is:

$$S = 2 \int_{0}^{a} f \left(\right. x \left.\right) d x$$

In the case of an odd function, where the contributions above and below the $x$-axis cancel out in the definite integral, the geometric area is:

$$S = 2 \int_{0}^{a} \left|\right. f \left(\right. x \left.\right) \left|\right. d x$$

## Improper integrals

Everything covered on this page assumes that the interval $\left[\right. a , b \left]\right.$ is finite and that $f \left(\right. x \left.\right)$ stays bounded throughout. In practice, these conditions are not always met. It is common to encounter integrals over intervals that stretch to infinity, or [functions](https://algebrica.org/functions/) that blow up at some point inside the [domain](https://algebrica.org/determining-the-domain-of-a-function/).

The standard Riemann integral cannot handle these cases directly. The way out is to replace the problematic bound with a limit and ask whether that limit converges to a finite value. For instance, an integral over an unbounded interval is defined as:

$$\int_{a}^{+ \infty} f \left(\right. x \left.\right) d x = \underset{t \rightarrow + \infty}{lim} \int_{a}^{t} f \left(\right. x \left.\right) d x$$

When the limit exists and is finite, the integral converges. When it does not, it diverges. Integrals of this kind are studied in detail in the dedicated page on [improper integrals](https://algebrica.org/improper-integrals/).

The definite integral, as developed on this page, measures signed area and provides a precise way to compute accumulated quantities. One of the most direct applications is finding the area of regions bounded by curves, a problem that reduces entirely to setting up and evaluating definite integrals of the kind studied here. This is covered in detail in the dedicated page on [finding areas by integration](https://algebrica.org/finding-areas-by-integration/).

## Selected references

- **Harvard University, O. Knill**. [Density and Definite Integral](https://people.math.harvard.edu/~knill/teaching/fall2023/handouts/lecture02.pdf)
- **MIT, G. Strang**. [Integrals](https://ocw.mit.edu/courses/res-18-001-calculus-fall-2023/mitres_18_001_f17_ch05.pdf)
- **UC Davis, J. Hunter**. [Properties and Applications of the Integral](https://www.math.ucdavis.edu/~hunter/intro_analysis_pdf/ch12.pdf)
- **MIT, D. Jerison**. [Proof of the First Fundamental Theorem of Calculus](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/e5e4813ac3a0b21f61532842c7ce8a8c_MIT18_01SCF10_Ses52b.pdf)
- **UC Berkeley, T. Scanlon**. [Approximation of Definite Integrals](https://math.berkeley.edu/~scanlon/m16bs04/ln/16b2lec15.pdf)
- **UC Davis, J. Hunter**. [The Riemann Integral](https://www.math.ucdavis.edu/~hunter/m125b/ch1.pdf)
