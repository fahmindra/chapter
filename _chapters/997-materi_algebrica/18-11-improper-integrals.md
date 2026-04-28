---
layout: chapter
title: "Improper Integrals"
chapter: "Integrals"
chapter_order: 18
section_order: 11
permalink: /materi-algebrica/integrals/improper-integrals/
---

## Definition

Improper integrals are [integrals](https://algebrica.org/indefinite-integrals/) in which either the interval of integration is unbounded, or the integrand becomes unbounded at one or more points, or both. In elementary calculus, the [definite integral](https://algebrica.org/definite-integrals/):

$$\int_{a}^{b} f \left(\right. x \left.\right) d x$$

is defined under the assumption that:

- The interval $\left[\right. a , b \left]\right.$ is bounded.
- The function $f$ is [continuous](https://algebrica.org/continuous-functions/) or at least integrable on that interval.

However, many relevant problems in mathematics and applications naturally lead beyond these restrictions. We may encounter an [unbounded interval](https://algebrica.org/intervals/), such as $\left(\right. a , + \infty \left.\right)$ or a function that becomes unbounded at one or more points of the interval. In such cases, the integral is called an **improper integral**. Its meaning is not immediate: it must be defined through a limiting process.

###### Improper integrals do not enlarge the class of [Riemann integrable](https://algebrica.org/riemann-integrability-criteria/) functions. They reinterpret problematic situations through limits of ordinary integrals. Convergence is a global property: it depends on how the function behaves near infinity or near a singularity, not just locally.

**Why a limiting process?** Consider applying the [Fundamental Theorem of Calculus](https://algebrica.org/fundamental-theorem-of-calculus/) directly to the following integral:

$$\int_{- 1}^{1} \frac{1}{x^{2}} d x$$

A naive calculation gives $\left(\left[\right. - x^{- 1} \left]\right.\right)_{- 1}^{1} = - 2$, which is clearly wrong: the integrand is strictly positive, so the integral cannot be negative. The issue is that $1 / x^{2}$ has a singularity at $x = 0$, which lies inside the interval (the Fundamental Theorem does not apply here). This example shows that extending integration beyond its classical domain requires more than mechanical computation: it requires a definition built on limits.

###### Blindly applying the Fundamental Theorem of Calculus to an improper integral is not just imprecise; it can produce results that are not merely inaccurate, but mathematically nonsensical.

## Improper integrals over unbounded intervals

Suppose $f$ is [continuous](https://algebrica.org/continuous-functions/) on $\left[\right. a , + \infty \left.\right)$. The integral:
$$\int_{a}^{+ \infty} f \left(\right. x \left.\right) d x$$
is defined as the [limit](https://algebrica.org/limits):
$$\int_{a}^{+ \infty} f \left(\right. x \left.\right) d x := \underset{b \rightarrow + \infty}{lim} \int_{a}^{b} f \left(\right. x \left.\right) d x$$

provided that this limit exists and is finite. In other words, we integrate up to a finite upper bound $b$ and then let $b$ grow without bound:

![](https://algebrica.org/wp-content/uploads/resources/images/improper-integrals-1.png)

- If the limit exists and is finite, the integral is said to converge: the area under the curve accumulates to a well-defined value despite the unbounded domain.
- If the limit does not exist or is infinite, the integral diverges: no finite value can be assigned to it.

---

The same idea applies when the lower limit is $- \infty$. For an integral of the form:
$$\int_{- \infty}^{b} f \left(\right. x \left.\right) d x$$
the definition is symmetric:
$$\int_{- \infty}^{b} f \left(\right. x \left.\right) d x := \underset{a \rightarrow - \infty}{lim} \int_{a}^{b} f \left(\right. x \left.\right) d x$$

For integrals over the entire real line, neither endpoint is finite, so a single limit no longer suffices. Instead, we split the integral at an arbitrary point $c$ and handle each half separately:
$$\int_{- \infty}^{+ \infty} f \left(\right. x \left.\right) d x$$
is defined as:
$$\int_{- \infty}^{+ \infty} f \left(\right. x \left.\right) d x = \int_{- \infty}^{c} f \left(\right. x \left.\right) d x + \int_{c}^{+ \infty} f \left(\right. x \left.\right) d x$$
for some real $c$, provided both integrals converge separately. The result does not depend on the choice of $c$.

## Example 1

To illustrate convergence, we compute the following integral:
$$\int_{1}^{+ \infty} \frac{1}{x^{2}} d x$$

Following the definition, we replace the infinite upper limit with a finite bound $b$ and compute the resulting ordinary integral:

$$\int_{1}^{b} \frac{1}{x^{2}} d x = \int_{1}^{b} x^{- 2} d x = \left(\left[\right. - x^{- 1} \left]\right.\right)_{1}^{b} = - \frac{1}{b} + 1$$

It remains to take the limit as $b \rightarrow + \infty$. As $b$ grows without bound, the term $\frac{1}{b}$ vanishes, and we obtain:

$$\underset{b \rightarrow + \infty}{lim} \left(\right. 1 - \frac{1}{b} \left.\right) = 1$$

The limit exists and is finite, so we conclude:
$$\int_{1}^{+ \infty} \frac{1}{x^{2}} d x = 1$$
and the integral converges to $1$.

## Example 2

We now consider a case where the limit fails to be finite. The integral:

$$\int_{1}^{+ \infty} \frac{1}{x} d x$$

looks structurally similar to the previous one, but the behavior is fundamentally different. We compute:

$$\int_{1}^{b} \frac{1}{x} d x = \left(\left[\right. ln ⁡ x \left]\right.\right)_{1}^{b} = ln ⁡ b$$

Taking the limit as $b \rightarrow + \infty$:
$$\underset{b \rightarrow + \infty}{lim} ln ⁡ b = + \infty$$

The limit does not exist as a finite value, and therefore the integral diverges.

## Improper integrals with infinite discontinuities

A second type of improper integral occurs when $f$ is unbounded at some point in the interval. Suppose $f$ is continuous on $\left(\right. a , b \left]\right.$, but becomes unbounded as $x \rightarrow a^{+}$. Then we define

$$\int_{a}^{b} f \left(\right. x \left.\right) d x := \underset{t \rightarrow a^{+}}{lim} \int_{t}^{b} f \left(\right. x \left.\right) d x$$

provided the limit exists and is finite.

---

Symmetrically, if $f$ is continuous on $\left[\right. a , b \left.\right)$ but becomes unbounded as $x \rightarrow b^{-}$, we define:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x := \underset{t \rightarrow b^{-}}{lim} \int_{a}^{t} f \left(\right. x \left.\right) d x$$

If the singularity occurs at an interior point $c \in \left(\right. a , b \left.\right)$, the integral is split at $c$:
$$\int_{a}^{b} f \left(\right. x \left.\right) d x = \int_{a}^{c} f \left(\right. x \left.\right) d x + \int_{c}^{b} f \left(\right. x \left.\right) d x$$

provided both integrals converge separately.

## Example 3

To illustrate the case of an infinite discontinuity, we compute an integral whose integrand blows up at one of the endpoints. Consider:

$$\int_{0}^{1} \frac{1}{\sqrt{x}} d x$$

The function $\frac{1}{\sqrt{x}}$ is unbounded as $x \rightarrow 0^{+}$, so this is an improper integral of the second type. Following the definition, we remove the singularity by introducing a lower bound $t > 0$ and taking the limit as $t \rightarrow 0^{+}$:

$$\int_{0}^{1} \frac{1}{\sqrt{x}} d x := \underset{t \rightarrow 0^{+}}{lim} \int_{t}^{1} x^{- 1 / 2} d x$$

We compute the antiderivative:

$$\int x^{- 1 / 2} d x = 2 x^{1 / 2} + c$$

Evaluating over $\left[\right. t , 1 \left]\right.$:
$$\int_{t}^{1} x^{- 1 / 2} d x = 2 - 2 \sqrt{t}$$

Taking the limit as $t \rightarrow 0^{+}$:
$$\underset{t \rightarrow 0^{+}}{lim} \left(\right. 2 - 2 \sqrt{t} \left.\right) = 2$$
The limit exists and is finite, so the integral converges and equals $2$.

## The $p$-Integral Test

A fundamental reference example is the family of integrals:

$$\int_{1}^{+ \infty} \frac{1}{x^{p}} d x$$

where $p$ is a [real](https://algebrica.org/properties-of-real-numbers/) parameter. The behavior of this integral depends entirely on $p$, and the result serves as a benchmark for comparing more complex integrands. For $p \neq 1$, we compute:
$$\int_{1}^{b} x^{- p} d x = \left(\left[\right. \frac{x^{1 - p}}{1 - p} \left]\right.\right)_{1}^{b} = \frac{b^{1 - p} - 1}{1 - p}$$
Taking the limit as $b \rightarrow + \infty$:

- If $p > 1$, then $1 - p < 0$, so $b^{1 - p} \rightarrow 0$ and the integral converges to $\frac{1}{p - 1}$.
- If $p < 1$, then $1 - p > 0$, so $b^{1 - p} \rightarrow + \infty$ and the integral diverges.
- If $p = 1$, the antiderivative is $ln ⁡ x$, and $\underset{b \rightarrow + \infty}{lim} ln ⁡ b = + \infty$, so the integral diverges.

In summary:

$$\int_{1}^{+ \infty} \frac{1}{x^{p}} d x \text{converges if and only if} p > 1.$$

---

An analogous result holds near the origin. For the integral:
$$\int_{0}^{1} \frac{1}{x^{p}} d x$$
the singularity is now at $x = 0$, and the roles are reversed:
$$\int_{0}^{1} \frac{1}{x^{p}} d x \text{converges if and only if} p < 1.$$

###### The $p$-integral test illustrates a fundamental principle: the convergence of an improper integral is governed by the rate at which the integrand decays or blows up. What ultimately matters is not the exact form of the function, but its asymptotic behavior near infinity or near the singular point. For this reason, powers of $x$ serve as natural comparison models in a wide range of convergence arguments.

## Convergence and comparison

Directly computing an improper integral is not always feasible and often not even necessary. In many situations, what one needs to know is not the exact value of the integral, but simply whether it converges or diverges. Comparison principles make it possible to answer this question by looking at how the integrand behaves, rather than by finding its antiderivative.

The most immediate tool is the direct **comparison test**. Suppose $0 \leq f \left(\right. x \left.\right) \leq g \left(\right. x \left.\right)$ for all $x \geq a$.

- If $\int_{a}^{+ \infty} g \left(\right. x \left.\right) d x$ converges, so does $\int_{a}^{+ \infty} f \left(\right. x \left.\right) d x$
- If $\int_{a}^{+ \infty} f \left(\right. x \left.\right) d x$ diverges, so does $\int_{a}^{+ \infty} g \left(\right. x \left.\right) d x$

###### The reasoning is elementary: if a larger function accumulates only a finite area, a smaller one certainly cannot do worse; conversely, if a smaller function already forces the area to grow without bound, a larger one has no hope of staying finite.

---

A pointwise bound is not always easy to establish, and this is where the limit comparison test becomes useful. If $f \left(\right. x \left.\right) , g \left(\right. x \left.\right) > 0$ and:

$$\underset{x \rightarrow + \infty}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = L \text{with} 0 < L < + \infty$$

then $\int_{a}^{+ \infty} f \left(\right. x \left.\right) d x$ and $\int_{a}^{+ \infty} g \left(\right. x \left.\right) d x$ either both converge or both diverge. When two functions are asymptotically equivalent, convergence of one implies convergence of the other, and the same holds for divergence. In practice, the reference of choice is almost always a [power](https://algebrica.org/powers/) $1 / x^{p}$, whose behavior is fully characterized by the $p$-integral test.

## Example 4

To illustrate the limit comparison test, consider the integral:

$$\int_{1}^{+ \infty} \frac{1}{x^{2} + 1} d x$$

Finding an explicit antiderivative is possible here, it involves $arctan ⁡ x$, but the point of the example is different: we want to establish convergence without computing the integral, purely by comparing asymptotic rates. For large $x$, the term $+ 1$ in the denominator becomes negligible relative to $x^{2}$, so the integrand behaves like $1 / x^{2}$. To make this precise, we compute the limit:

$$\underset{x \rightarrow + \infty}{lim} \frac{\frac{1}{x^{2} + 1}}{\frac{1}{x^{2}}} = \underset{x \rightarrow + \infty}{lim} \frac{x^{2}}{x^{2} + 1} = 1$$

The limit is finite and strictly positive. By the limit comparison test, $\int_{1}^{+ \infty} \frac{1}{x^{2} + 1} d x$ and $\int_{1}^{+ \infty} \frac{1}{x^{2}} d x$ either both converge or both diverge.

Since the latter converges by the $p$-integral test with $p = 2 > 1$, we conclude that
$$\int_{1}^{+ \infty} \frac{1}{x^{2} + 1} d x$$
converges as well.

## Selected references

- **Simon Fraser University**. [Improper Integrals](https://www.sfu.ca/math-coursenotes/Math%20158%20Course%20Notes/sec_ImproperIntegrals.html)
- **MIT OpenCourseWare**. [Lecture 36: Improper Integrals](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/resources/lecture-36-improper-integrals/)
- **Harvard University**. [Lecture 9: Improper Integrals](https://people.math.harvard.edu/~knill/teaching/fall2023/handouts/lecture09.pdf)
- **Harvard University**. [Lecture 10: Improper Integrals](https://people.math.harvard.edu/~knill/teaching/fall2023/handouts/lecture10.pdf)
- **University of California, Davis**. [Chapter 12: Improper Integrals](https://www.math.ucdavis.edu/~hunter/intro_analysis_pdf/ch12.pdf)
