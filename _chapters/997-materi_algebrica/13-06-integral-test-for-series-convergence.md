---
layout: chapter
title: "Integral Test for Series Convergence"
chapter: "Series"
chapter_order: 13
section_order: 6
permalink: /materi-algebrica/series/integral-test-for-series-convergence/
---

## What is the integral test

Determining the sum of an infinite [series](https://algebrica.org/series) and assessing its convergence or divergence is not always straightforward. Several methods are available to study convergence, one of which involves comparing the series to an [improper integral](https://algebrica.org/improper-integrals). This test applies to [series with positive terms](https://algebrica.org/series-with-positive-terms/) and relies on the principle that the convergence of the series can be determined by comparing it to the behavior of an associated improper integral.

---

Let $f$ be a positive, [decreasing function](https://algebrica.org/increasing-and-decreasing-functions/) defined on $\left[\right. 1 , + \infty \left.\right)$, such as a [rational](https://algebrica.org/rational-functions) or [polynomial function](https://algebrica.org/polynomial-function/). Then the series

$$\sum_{n = 1}^{\infty} f \left(\right. n \left.\right)$$

converges or diverges if and only if the improper integral

$$\int_{1}^{\infty} f \left(\right. x \left.\right) d x$$

does the same, assuming that $f$ is [continuous](https://algebrica.org/continuous-functions/) on $\left[\right. 1 , + \infty \left.\right) .$

---

![](https://algebrica.org/wp-content/uploads/resources/images/integral-test-series-1.png)

The graph illustrates the connection between a series and an improper integral as stated by the Integral Test.

- The curve $f \left(\right. x \left.\right)$ represents the continuous [function](https://algebrica.org/functions).
- The gray area shows a portion of the improper integral (the area under the curve from $x = 1$ to some $x = n$).
- The vertical rectangles represent the terms of the series $f \left(\right. n \left.\right)$, each with base 1 and height $f \left(\right. n \left.\right)$.

##### This visual helps compare the discrete sum (the series) and the continuous accumulation (the integral). Since the rectangles overestimate or underestimate the area depending on the function’s behavior, the integral can be used to determine the convergence of the series.

## Proof

Let us consider the partial sum of the series:

$$s_{k} = \sum_{n = 1}^{k} f \left(\right. n \left.\right) k \in \mathbb{N}$$

This represents the sum of the first $k$ terms of the series $\sum f \left(\right. n \left.\right)$. Since the series has positive terms, the [sequence](https://algebrica.org/sequences) of partial sums $s_{k}$ is increasing and admits a limit as $k \rightarrow \infty$:

$$\underset{k \rightarrow + \infty}{lim} s_{k} = s \in \left[\right. 0 , + \infty \left]\right.$$

Just as the series is defined by the limit of its partial sums, the improper integral is defined as the limit of the definite integral as the upper bound tends to infinity:

$$\underset{k \rightarrow + \infty}{lim} \int_{1}^{k} f \left(\right. x \left.\right) d x = \int_{1}^{+ \infty} f \left(\right. x \left.\right) d x$$

By the linearity of the integral, and in particular its additivity over adjacent intervals, we can write:

$$\int_{1}^{k} f \left(\right. x \left.\right) d x = \sum_{n = 1}^{k - 1} \int_{n}^{n + 1} f \left(\right. x \left.\right) d x$$

This holds because the definite integral over $\left[\right. 1 , k \left]\right.$ can be decomposed into a sum of integrals over the unit-length subintervals $\left[\right. n , n + 1 \left]\right.$, which are disjoint and consecutive. Since $f$ is assumed to be decreasing, we obtain the following inequality for all $x \in \left[\right. n , n + 1 \left]\right.$:

$$f \left(\right. n + 1 \left.\right) \leq f \left(\right. x \left.\right) \leq f \left(\right. n \left.\right)$$

By applying the inequality within the integral, we obtain:

$$\int_{n}^{n + 1} f \left(\right. n + 1 \left.\right) d x \leq \int_{n}^{n + 1} f \left(\right. x \left.\right) d x \leq \int_{n}^{n + 1} f \left(\right. n \left.\right) d x$$

By the properties of definite integrals, the first and third terms represent integrals of constant functions. Therefore, the constants can be factored out of the integrals, giving:

$$f \left(\right. n + 1 \left.\right) \leq \int_{n}^{n + 1} f \left(\right. x \left.\right) , d x \leq f \left(\right. n \left.\right)$$

Now summing these inequalities from $n = 1$ to $k - 1$:

$$\sum_{n = 1}^{k - 1} f \left(\right. n + 1 \left.\right) \leq \sum_{n = 1}^{k - 1} \int_{n}^{n + 1} f \left(\right. x \left.\right) d x \leq \sum_{n = 1}^{k - 1} f \left(\right. n \left.\right)$$

By taking the limit as $k \rightarrow \infty$, we obtain:

$$\sum_{n = 2}^{\infty} f \left(\right. n \left.\right) \leq \int_{1}^{\infty} f \left(\right. x \left.\right) d x \leq \sum_{n = 1}^{\infty} f \left(\right. n \left.\right)$$

which shows that the improper integral is bounded between two versions of the series differing only by the first term $f \left(\right. 1 \left.\right)$. Because the integral lies between two versions of the series that differ only by the first term, if the integral converges, so does the series, and if the integral diverges, the series diverges as well.

## Example

Determine whether the following series converges or diverges using the integral test:

$$\sum_{n = 2}^{\infty} \frac{1}{n log ⁡ n}$$

---

First, consider the associated function:

$$f \left(\right. x \left.\right) = \frac{1}{x log ⁡ x}$$

defined on the interval $x \geq 2$. This function is positive, continuous, and decreasing on $\left[\right. 2 , + \infty \left.\right) ,$ so the conditions for using the integral test are satisfied.

---

Now we evaluate the improper integral:

$$\int_{2}^{\infty} \frac{1}{x log ⁡ x} d x$$

To compute this, use the [substitution](https://algebrica.org/integration-by-substitution/) $u = log ⁡ x$, which implies $d u = \frac{1}{x} d x$. The integral becomes:

$$\int_{log ⁡ 2}^{\infty} \frac{1}{u} d u = \underset{t \rightarrow \infty}{lim} \int_{log ⁡ 2}^{t} \frac{1}{u} d u = \underset{t \rightarrow \infty}{lim} \left[\right. log ⁡ u \left]\right._{log ⁡ 2}^{t} = \infty$$

Since the integral diverges, the integral test tells us that the series also diverges.

## Glossary

- Infinite Series: an expression of the form $\sum_{n = 1}^{\infty} a_{n} = a_{1} + a_{2} + a_{3} + \ldots$, where $a_{n}$ are the terms of the series.
- Convergence of a series: an infinite series converges if its sequence of partial sums approaches a finite limit.
- Divergence of a series: an infinite series diverges if its sequence of partial sums does not approach a finite limit (either it goes to infinity or oscillates).
- Improper integral: a definite integral where at least one of the limits of integration is infinite, or the integrand has a discontinuity within the interval of integration.
- Decreasing function: a function $f \left(\right. x \left.\right)$ is decreasing on an interval if for any $x_{1} < x_{2}$ in that interval, $f \left(\right. x_{1} \left.\right) \geq f \left(\right. x_{2} \left.\right) .$
- Continuous function: a function whose graph can be drawn without lifting the pen, meaning there are no abrupt jumps or breaks.
- Partial sum $s_{k}$: the sum of the first $k$ terms of an infinite series, denoted as $s_{k} = \sum_{n = 1}^{k} a_{n}$.
- Limit of a sequence: the value that the terms of a sequence approach as the index tends to infinity.
- Additivity of integrals: the property that the definite integral over a compound interval is the sum of the definite integrals over the disjoint subintervals that make up the compound interval.
