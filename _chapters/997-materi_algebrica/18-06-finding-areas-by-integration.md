---
layout: chapter
title: "Finding Areas by Integration"
chapter: "Integrals"
chapter_order: 18
section_order: 6
permalink: /materi-algebrica/integrals/finding-areas-by-integration/
---

## Area between two curves using definite integrals

Building on the concept of [definite integrals](https://algebrica.org/definite-integrals), which measure the area between a curve and the x-axis, we can extend the same idea to find the area enclosed between two curves. Let $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ be two [continuous](https://algebrica.org/continuous-functions/) functions defined on the same [interval](https://algebrica.org/intervals/) $\left[\right. a , b \left]\right.$, such that $f \left(\right. x \left.\right) \geq g \left(\right. x \left.\right)$ for every $x \in \left[\right. a , b \left]\right.$, and suppose their graphs enclose a region. The area of this region is given by:

$$(\text{1}) A = \int_{a}^{b} \left[\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left]\right. d x$$

##### Since both $f$ and $g$ are continuous on $\left[\right. a , b \left]\right.$, their difference $f \left(\right. x \left.\right) - g \left(\right. x \left.\right)$ is also continuous on the same interval. A continuous function on a closed and bounded interval is [Riemann-integrable](https://algebrica.org/riemann-integrability-criteria/). Therefore, the function $f \left(\right. x \left.\right) - g \left(\right. x \left.\right)$ is integrable on $\left[\right. a , b \left]\right.$, and the area between the two curves is well defined through a definite integral.

---

We want to calculate the area of the gray-shaded region between the curves $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$:

![Finding areas by integration
](https://algebrica.org/wp-content/uploads/resources/images/areas-by-integration-1.png)

Intuitively, we can see that the area $A$ is given by the difference between the area under the curve $f \left(\right. x \left.\right)$ and the area under the curve $g \left(\right. x \left.\right)$. In other words, formally:

$$A = \int_{a}^{b} f \left(\right. x \left.\right) d x - \int_{a}^{b} g \left(\right. x \left.\right) d x$$

By the linearity of the [integral](https://algebrica.org/indefinite-integrals), this becomes equation $1$.

## Areas between intersecting curves

So far we assumed that $f \left(\right. x \left.\right) \geq g \left(\right. x \left.\right)$ throughout the entire interval $\left[\right. a , b \left]\right.$. In many cases, however, the interval itself is not given: the two curves determine it, and the first step is to find where they meet. To locate the intersection points, set $f \left(\right. x \left.\right) = g \left(\right. x \left.\right)$ and solve for $x$. The solutions are the limits of integration.

Once the interval is known, the two curves can cross inside it, meaning that $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ swap their relative position at some interior point $c$. When this happens, the integrand $f \left(\right. x \left.\right) - g \left(\right. x \left.\right)$ changes sign, and a single integral over $\left[\right. a , b \left]\right.$ would cause areas above and below the x-axis to cancel out, producing an incorrect result.

---

The correct approach is to split the interval at each crossing point and integrate separately over each subinterval, always subtracting the lower curve from the upper one:

$$A = \int_{a}^{c} \left[\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left]\right. d x + \int_{c}^{b} \left[\right. g \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left]\right. d x$$

A compact way to write this without tracking which curve is on top is:

$$A = \int_{a}^{b} \left|\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left|\right. d x$$

![](https://algebrica.org/wp-content/uploads/resources/images/finding-areas-by-integration-5.png)

The [absolute value](https://algebrica.org/absolute-value/) guarantees that each piece of area is counted as positive, regardless of which [function](https://algebrica.org/functions/) is larger on that subinterval.

###### The formula $A = \int_{a}^{b} \left|\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left|\right. d x$ is valid provided that all intersection points of the two curves are included among the limits of integration. The absolute value ensures that the difference between the two functions is always taken as positive, so that no portion of the enclosed region cancels out when the curves swap their relative position.

## Example 1

Suppose we want to find the area enclosed between the curves $y_{1} = e^{x}$ and $y_{2} = x^{2} - 1$ over the interval $x \in \left[\right. - 1 , 1 \left]\right.$. Graphically, we have the following situation:

![](https://algebrica.org/wp-content/uploads/resources/images/areas-by-integration-2.png)

To calculate the area, we use equation $\left(\right. 1 \left.\right)$ and set up the following definite integral:

$$A = \int_{- 1}^{1} \left[\right. e^{x} - \left(\right. x^{2} - 1 \left.\right) \left]\right. d x$$

---

Solving the integral, we obtain:

$$A & = \int_{- 1}^{1} \left[\right. e^{x} - x^{2} + 1 \left]\right. d x \\ & = \left(\left[\right. e^{x} - \frac{x^{3}}{3} + x \left]\right.\right)_{- 1}^{1} \\ & = \left(\right. e - \frac{1}{3} + 1 \left.\right) - \left(\right. e^{- 1} + \frac{1}{3} - 1 \left.\right) \\ & = e - \frac{1}{e} + \frac{4}{3}$$

Therefore, the area between the two curves is:

$$A = e - \frac{1}{e} + \frac{4}{3}$$

## Example 2

Find the area of the region enclosed between the curves $f \left(\right. x \left.\right) = x^{3} - 3 x$ and $g \left(\right. x \left.\right) = x$. The interval is not given. We start by finding where the two curves intersect, setting $f \left(\right. x \left.\right) = g \left(\right. x \left.\right)$:

$$x^{3} - 3 x & = x \\ x^{3} - 4 x & = 0 \\ x \left(\right. x^{2} - 4 \left.\right) & = 0$$

The solutions are $x = - 2$, $x = 0$, and $x = 2$. These are the limits of integration.

---

Since the curves cross at $x = 0$, we check which function is on top in each subinterval. Evaluating at $x = - 1$ we obtain:

$$f \left(\right. - 1 \left.\right) & = \left(\right. - 1 \left.\right)^{3} - 3 \left(\right. - 1 \left.\right) = 2 \\ g \left(\right. - 1 \left.\right) & = - 1$$

So $f \left(\right. x \left.\right) \geq g \left(\right. x \left.\right)$ on $\left[\right. - 2 , 0 \left]\right.$. By symmetry, $g \left(\right. x \left.\right) \geq f \left(\right. x \left.\right)$ on $\left[\right. 0 , 2 \left]\right.$.

---

We now split the integral accordingly:

$$A = \int_{- 2}^{0} \left[\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left]\right. d x + \int_{0}^{2} \left[\right. g \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left]\right. d x$$

$$A = \int_{- 2}^{0} \left(\right. x^{3} - 4 x \left.\right) d x + \int_{0}^{2} \left(\right. 4 x - x^{3} \left.\right) d x$$

---

Computing the first integral, we have:

$$\int_{- 2}^{0} \left(\right. x^{3} - 4 x \left.\right) d x & = \left(\left[\right. \frac{x^{4}}{4} - 2 x^{2} \left]\right.\right)_{- 2}^{0} \\ & = \left(\right. 0 \left.\right) - \left(\right. \frac{16}{4} - 2 \cdot 4 \left.\right) \\ & = 0 - \left(\right. 4 - 8 \left.\right) \\ & = 4$$

Computing the second integral, we obtain:

$$\int_{0}^{2} \left(\right. 4 x - x^{3} \left.\right) d x & = \left(\left[\right. 2 x^{2} - \frac{x^{4}}{4} \left]\right.\right)_{0}^{2} \\ & = \left(\right. 2 \cdot 4 - \frac{16}{4} \left.\right) - 0 \\ & = 8 - 4 \\ & = 4$$

The total area is:

$$A = 4 + 4 = 8$$

The symmetry of the result is not a coincidence: $f \left(\right. x \left.\right) = x^{3} - 3 x$ is an [odd function](https://algebrica.org/even-and-odd-functions/), and the two regions are mirror images of each other across the origin.

## Selected references

- **New York University, S.R.S. Varadhan**. [Area Between Curves](https://math.nyu.edu/~varadhan/Calculus09/Notes12.pdf)
- **University of Washington, A. Nichifor**. [Areas Between Curves: Applications of Integration](https://sites.math.washington.edu//~nichifor/125_2012_Winter/2012%20Handout%206_1%20Areas.pdf)
- **University of Washington**. [Area Between Curves](https://sites.math.washington.edu/~m125/Worksheets/AreaBetweenCurves.pdf)
- **UC Davis, D. Kouba**. [Areas of Enclosed Regions](https://www.math.ucdavis.edu/~kouba/CalcTwoDIRECTORY/areadirectory/Area.html)
- **Columbia University, A. Vizeff**. [Applications of Integration](https://www.math.columbia.edu/~avizeff/calculus-I-F22/lecture-20.pdf)
