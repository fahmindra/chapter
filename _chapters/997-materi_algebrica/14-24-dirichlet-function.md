---
layout: chapter
title: "Dirichlet Function"
chapter: "Functions"
chapter_order: 14
section_order: 24
permalink: /materi-algebrica/functions/dirichlet-function/
---

measure propertieszero integralfunction comparisonthomae functionlebesgue measuredarboux sumsriemann integrabilitypointwise analysisoscillating behaviorlimit nonexistencesequence oscillationdensity argumenteverywhere discontinuousfunction valuespiecewise definitionreal domainindicator ruleirrational valuesrational valuesanalysisbehaviordefinition

## Definition

The Dirichlet function is defined on $\mathbb{R}$ by the following rule:

$$D \left(\right. x \left.\right) = \left{\right. 1 & \text{if} x \in \mathbb{Q} \\ 0 & \text{if} x \in \mathbb{R} \backslash \mathbb{Q}$$

At first glance this appears to be an almost trivial definition, a simple distinction between rationals and irrationals. Yet precisely this simplicity conceals an extremely irregular analytic behaviour, which has made this function a key reference object in [integration](https://algebrica.org/definite-integrals/) theory and real analysis.

---

A notable property of $D$ is its [discontinuity](https://algebrica.org/discontinuities-of-real-functions/) at every point of $\mathbb{R}$. This result follows from the mutual density of $\mathbb{Q}$ and $\mathbb{R} \backslash \mathbb{Q}$ in the real line.

For any fixed point $x_{0} \in \mathbb{R}$ and any $\epsilon > 0$, the [interval](https://algebrica.org/intervals/) $\left(\right. x_{0} - \epsilon , x_{0} + \epsilon \left.\right)$ contains both rational and irrational numbers. Therefore, there is no neighborhood of $x_{0}$ on which $D$ is constant, and any sequence converging to $x_{0}$ can be constructed so that the values of $D$ alternate indefinitely between $0$ and $1$. As a result, the following [limit](https://algebrica.org/limits/):

$$\underset{x \rightarrow x_{0}}{lim} D \left(\right. x \left.\right)$$

does not exist for any $x_{0}$, establishing discontinuity at every point. Since a function that is discontinuous everywhere cannot be [Riemann integrable](https://algebrica.org/riemann-integrability-criteria/) on any non-degenerate interval, this can be confirmed by noting that the upper and lower Darboux sums remain fixed at $1$ and $0$, respectively, for every partition of the interval.

###### Darboux sums are sums obtained by multiplying the maximum or minimum value of a function on each subinterval of a partition by the width of that subinterval. These sums are used to approximate the integral from above and below.

## Non-integrability in the Riemann sense

Consider an interval $\left[\right. a , b \left]\right.$ with $a < b$ and any partition $\mathcal{P}$ such that:

$$\mathcal{P} = a = x_{0} < x_{1} < \hdots < x_{n} = b$$

On each subinterval $\left[\right. x_{i - 1} , x_{i} \left]\right.$, the supremum of $D$ is $1$ due to the density of the rationals, while the infimum is $0$ due to the density of the irrationals. Therefore:

$$U \left(\right. D , \mathcal{P} \left.\right) = \sum_{i = 1}^{n} 1 \cdot \left(\right. x_{i} - x_{i - 1} \left.\right) = b - a$$
$$L \left(\right. D , \mathcal{P} \left.\right) = \sum_{i = 1}^{n} 0 \cdot \left(\right. x_{i} - x_{i - 1} \left.\right) = 0$$

Because $U \left(\right. D , \mathcal{P} \left.\right) - L \left(\right. D , \mathcal{P} \left.\right) = b - a > 0$ for every partition $\mathcal{P}$, the Riemann criterion is not satisfied. Consequently, the function is not integrable in the classical sense on any non-trivial interval.

---

Lebesgue’s integration theory introduces a significant shift in perspective. The set $\mathbb{Q}$ is countable and therefore has Lebesgue measure zero: $\lambda \left(\right. \mathbb{Q} \left.\right) = 0$. It follows that $D \left(\right. x \left.\right) = 0$ almost everywhere with respect to the Lebesgue measure, and since a function that equals zero almost everywhere has integral zero, one obtains

$$\int_{a}^{b} D \left(\right. x \left.\right) d \lambda = 0$$

for every interval $\left[\right. a , b \left]\right.$. This is one of the more immediate illustrations of the greater reach of Lebesgue’s theory relative to Riemann’s: by construction, it assigns no weight to sets of measure zero, even when those sets are dense in the real line.

## Differentiability

The question of whether $D$ possesses a [derivative](https://algebrica.org/derivatives/) at any point has a definitive answer: $D$ is nowhere differentiable. The derivative of $D$ at a point $x_{0}$ is defined as the limit:

$$D^{'} \left(\right. x_{0} \left.\right) = \underset{h \rightarrow 0}{lim} \frac{D \left(\right. x_{0} + h \left.\right) - D \left(\right. x_{0} \left.\right)}{h}$$

provided this limit exists. Since differentiability implies [continuity](https://algebrica.org/continuous-functions/) and $D$ is discontinuous at every point of $\mathbb{R}$, it follows immediately that $D$ cannot be differentiable anywhere.

This conclusion can also be seen directly through [difference quotients](https://algebrica.org/difference-quotient/). Fix any $x_{0}$ and consider two sequences $\left(\right. r_{n} \left.\right)$ and $\left(\right. s_{n} \left.\right)$ converging to $x_{0}$, with $r_{n} \in \mathbb{Q}$ and $s_{n} \in \mathbb{R} \backslash \mathbb{Q}$ for all $n$. If $x_{0} \in \mathbb{Q}$, then:

$$\frac{D \left(\right. r_{n} \left.\right) - D \left(\right. x_{0} \left.\right)}{r_{n} - x_{0}} = \frac{1 - 1}{r_{n} - x_{0}} = 0$$
$$\frac{D \left(\right. s_{n} \left.\right) - D \left(\right. x_{0} \left.\right)}{s_{n} - x_{0}} = \frac{0 - 1}{s_{n} - x_{0}} = \frac{- 1}{s_{n} - x_{0}}$$

The second expression is unbounded as $s_{n} \rightarrow x_{0}$. If instead $x_{0} \in \mathbb{R} \backslash \mathbb{Q}$, then:

$$\frac{D \left(\right. r_{n} \left.\right) - D \left(\right. x_{0} \left.\right)}{r_{n} - x_{0}} = \frac{1 - 0}{r_{n} - x_{0}} = \frac{1}{r_{n} - x_{0}}$$
$$\frac{D \left(\right. s_{n} \left.\right) - D \left(\right. x_{0} \left.\right)}{s_{n} - x_{0}} = \frac{0 - 0}{s_{n} - x_{0}} = 0$$

It is now the first expression that grows without bound as $r_{n} \rightarrow x_{0}$. In either case, the difference quotient admits no finite limit, confirming that $D^{'} \left(\right. x_{0} \left.\right)$ does not exist.

## The Thomae function

A function closely related to the Dirichlet function, known as the Thomae function or the popcorn function, is defined as follows:

$$T \left(\right. x \left.\right) = \left{\right. \frac{1}{q} & \text{if} x = \frac{p}{q} \\ 0 & \text{if} x \in \mathbb{R} \backslash \mathbb{Q}$$

We have $p \in \mathbb{Z}$, $q \in \mathbb{N}_{> 0}$, and $gcd \left(\right. \left|\right. p \left|\right. , q \left.\right) = 1$, that is, the fraction $p / q$ is in lowest terms.

In contrast to the Dirichlet function, the Thomae function is continuous at every irrational point and discontinuous at every rational point. This behaviour exemplifies the boundary case allowed by the Lebesgue criterion for Riemann integrability: a Riemann-integrable function may be discontinuous on a set of measure zero, and the rationals, though dense, constitute precisely such a set.

Consequently, the Thomae function is Riemann integrable, with integral equal to zero on every interval, and serves as a well-behaved counterpart to the Dirichlet function.

## Selected resources

- **Harvard University, C. T. McMullen**. [Math 55b Course Notes](https://people.math.harvard.edu/~ctm/home/text/class/harvard/55b/10/html/home/course/course.pdf)
- **Harvard University, A. Varilly**. [Thomae Function and Riemann Integrability](https://people.math.harvard.edu/~ctm/home/text/class/harvard/112/02/html/home/solns/sol11.pdf)
- **MIT, R. B. Melrose**. [Dirichlet Function and Darboux Sums](https://math.mit.edu/~rbm/18.100B/HW8-solved.pdf)
- **Princeton University, J. Shapiro**. [Lebesgue’s Theorem and the Dirichlet Function](https://web.math.princeton.edu/~js129/PDFs/teaching/MAT425_spring_2025/MAT425_Lecture_Notes.pdf)
- **UC Davis J. K. Hunter**. [The Riemann Integral](https://www.math.ucdavis.edu/~hunter/m125b/ch1.pdf)
