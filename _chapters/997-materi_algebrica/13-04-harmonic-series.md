---
layout: chapter
title: "Harmonic Series"
chapter: "Series"
chapter_order: 13
section_order: 4
permalink: /materi-algebrica/series/harmonic-series/
---

## What is a harmonic series

The **harmonic series** is defined as the infinite sum:

$$\sum_{k = 1}^{\infty} \frac{1}{k}$$

where each term is the reciprocal of a [natural number](https://algebrica.org/natural-numbers). Despite the terms approaching zero, the [series](https://algebrica.org/series) diverges, meaning the sum grows without bound. In particular, since the harmonic series is a series with [positive terms](https://algebrica.org/series-with-positive-terms/), it can be shown that it diverges to positive infinity. In fact, since the series has positive terms, the limit of the sequence of its partial sums exists:

$$S = \underset{n \rightarrow + \infty}{lim} s_{n} = \underset{n \rightarrow + \infty}{lim} \sum_{k = 1}^{n} \frac{1}{k}$$

At first glance, one might think that as $n \rightarrow \infty$, the terms of the harmonic series tend to zero and therefore the series itself might converge. However, this is a logical error: although the terms $\frac{1}{n}$ do approach zero, they do not do so fast enough for the series to converge.

![](https://algebrica.org/wp-content/uploads/resources/images/harmonic-series-1-2.png)

##### Here is the graph of the partial sums of the harmonic series up to $n = 100.$ As can be seen, the curve rises slowly yet unceasingly, confirming that the series is divergent.

---

There are several ways to demonstrate that the harmonic series diverges. One approach involves using [partial sums](https://algebrica.org/series/), as shown below:

$$\sum_{k = 1}^{\infty} \frac{1}{k} = 1 + \frac{1}{2} + \left(\right. \frac{1}{3} + \frac{1}{4} \left.\right) + \left(\right. \frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} \left.\right) + \hdots$$

Each group contains twice as many terms as the previous one. By observing that each group adds at least $\frac{1}{2}$ to the sum, we conclude that the overall series grows without bound:

$$\sum_{k = 1}^{\infty} \frac{1}{k} = \infty$$

Hence, the harmonic series diverges.

Knowing how the harmonic series and its variants behave is useful, since the comparison test often lets us relate a complex series to a harmonic one to check whether it converges.

## Generalized harmonic series (p-series)

Let’s consider a generalized version of the harmonic series, where the denominator is raised to a [power](https://algebrica.org/powers) $a$:

$$\sum_{k = 1}^{\infty} \frac{1}{k^{a}}$$

This series, known as **generalized harmonic series**, has an additional feature compared to the standard harmonic series: its convergence or divergence depends on the value of the exponent $a$. We have:

- If $a > 1$, the series converges.
- If $a \leq 1$, the series diverges.

---

A necessary condition for the convergence of a series $\sum a_{k}$ is that the general term tends to zero:

$$\underset{k \rightarrow \infty}{lim} a_{k} = 0.$$

If this condition is not satisfied, that is, if $\underset{k \rightarrow \infty}{lim} a_{k} \neq 0$, then the series diverges. In the case of the generalized harmonic series with exponent $a \leq 1$, this condition fails. For example, when $a = 0$, the terms become constant $a_{k} = 1$, and:

$$\underset{k \rightarrow \infty}{lim} \frac{1}{k^{0}} = \underset{k \rightarrow \infty}{lim} 1 = 1 \neq 0.$$

Hence, the series diverges because its general term does not tend to zero.

---

When $a > 1$, we can apply the [integral test](https://algebrica.org/integral-test-for-series-convergence/) to determine the convergence of the series. Consider the corresponding improper integral, we have:

$$\int_{1}^{\infty} \frac{1}{x^{a}} d x$$

Since $a > 1$, we have:

$$\int_{1}^{\infty} \frac{1}{x^{a}} d x = \underset{t \rightarrow \infty}{lim} \int_{1}^{t} x^{- a} d x$$

By evaluating the integral at the endpoints, we obtain:

$$\underset{t \rightarrow \infty}{lim} \left(\left[\right. \frac{x^{1 - a}}{1 - a} \left]\right.\right)_{1}^{t} = \underset{t \rightarrow \infty}{lim} \left(\right. \frac{t^{1 - a}}{1 - a} - \frac{1}{1 - a} \left.\right)$$

Because $a > 1$, the exponent $1 - a < 0$, so $t^{1 - a} \rightarrow 0$. Therefore:

$$\int_{1}^{\infty} \frac{1}{x^{a}} d x = \frac{1}{a - 1}$$

which is finite. Hence the series converges for all $a > 1$.

## Logarithmically modified harmonic series

Finally, let us consider the following series:

$$\sum_{k = 2}^{\infty} \frac{1}{k \left(\right. log^{\alpha} ⁡ k \left.\right)}$$

This is a so-called **logarithmically modified** series, where the presence of the [logarithmic](https://algebrica.org/logarithms) term affects the rate at which the series converges or diverges. The convergence of the series depends on the exponent $\alpha$ in the logarithmic term:

- If $\alpha > 1$, the series converges.
- If $\alpha \leq 1$, the series diverges.

The summation starts at $k = 2$ to avoid the singularities at $k = 0$ (where $log ⁡ 0$ is undefined) and $k = 1$ (where $log ⁡ 1 = 0$, causing division by zero).

---

To demonstrate the convergence, we apply the improper integral test. We consider the function:

$$f \left(\right. x \left.\right) = \frac{1}{x \left(\right. log ⁡ x \left.\right)^{\alpha}}$$

which is positive, [continuous](https://algebrica.org/continuous-functions/), and [decreasing](https://algebrica.org/increasing-and-decreasing-functions/) for $x \geq 2$. We then evaluate the improper integral:

$$\int_{2}^{\infty} \frac{1}{x \left(\right. log ⁡ x \left.\right)^{\alpha}} d x$$

Using the substitution $u = log ⁡ x$, we get:

$$\int_{2}^{\infty} \frac{1}{x \left(\right. log ⁡ x \left.\right)^{\alpha}} d x = \int_{log ⁡ 2}^{\infty} \frac{1}{u^{\alpha}} d u$$

This integral converges if and only if $\alpha > 1$. Therefore, by the integral test, the series converges if and only if $\alpha > 1$.

## Example

Let us determine the nature of the following series:

$$\sum_{n = 2}^{\infty} \frac{1}{n \sqrt{log ⁡ n}}$$

---

We observe that this series has the general form:

$$\sum_{n = 2}^{\infty} \frac{1}{n \left(\right. log ⁡ n \left.\right)^{\alpha}}$$

with $\alpha = \frac{1}{2}$. This is known as a logarithmically modified harmonic series. According to known results, the series converges if and only if $\alpha > 1$.

Since $\alpha = \frac{1}{2} < 1$, the series diverges.

We conclude that the series diverges by comparison with a divergent harmonic series modified by a logarithmic term.
