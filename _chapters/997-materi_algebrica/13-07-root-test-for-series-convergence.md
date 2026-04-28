---
layout: chapter
title: "Root Test for Series Convergence"
chapter: "Series"
chapter_order: 13
section_order: 7
permalink: /materi-algebrica/series/root-test-for-series-convergence/
---

## What is the root test

The root test is a method used to determine whether an infinite [series](https://algebrica.org/series) converges or diverges. It is particularly useful when each term of the series involves an expression raised to the $n$-th [power](https://algebrica.org/powers), such as [exponentials](https://algebrica.org/exponential-function) or [roots](https://algebrica.org/radicals). Suppose we have a series with positive terms of the form:

$$\sum_{n = 1}^{+ \infty} a_{n}$$

Assume that the [limit](https://algebrica.org/limits) exists and is finite:

$$\underset{n \rightarrow \infty}{lim sup} \sqrt[n]{\left|\right. a_{n} \left|\right.} = L$$

We use $lim sup$ because it is always defined for real sequences that are bounded from below. This makes the root test reliable even when the usual limit $\underset{n \rightarrow \infty}{lim} \sqrt[n]{\left|\right. a_{n} \left|\right.}$ does not exist. By taking the limit superior, the test can still detect the long-term behavior of the sequence and determine whether the series converges or diverges.

If the limit $L$ exists, three cases can occur:

- If $L < 1$, the series converges absolutely.
- If $L > 1$ or $L = \infty$, the series diverges.
- If $L = 1$, the test is inconclusive.

##### We use the [absolute value](https://algebrica.org/absolute-value) $\left|\right. a_{n} \left|\right.$ to apply the root test to the absolute convergence of the series. This ensures the test works even if the terms $a_{n}$ are negative or alternate in sign, allowing us to focus only on their magnitude.

## How to recognize when to apply the root test

The root test is especially useful when the general term of a series is expressed in the form $a_{n} = \left(\right. b_{n} \left.\right)^{n}$, that is, when the entire term is raised to the power of $n$. In such cases, taking the $n$-th root of $a_{n}$ simplifies the expression significantly and often leads directly to a manageable limit.

By contrast, other tests may become more complicated in this context, especially when the ratio $\frac{a_{n + 1}}{a_{n}}$ does not simplify easily or when factorials or [exponential](https://algebrica.org/exponential-function) terms are involved in a way that makes limits more difficult to compute.

In summary, the Root Test is particularly effective in the following situations:

- When $a_{n} = \left(\right. f \left(\right. n \left.\right) \left.\right)^{n}$, with $f \left(\right. n \left.\right) > 0$
- When the terms involve exponential-like growth or decay
- When the limit $\sqrt[n]{\left|\right. a_{n} \left|\right.}$ is easier to compute than $\frac{a_{n + 1}}{a_{n}}$

In all other cases, if the general term is not raised to the $n$-th power other tests may be more suitable.

## Proof

Let us consider the case of absolute convergence where $L < 1$. Since $L < 1$, there exists a [real number](https://algebrica.org/types-of-numbers) $r$ such that:

$$L < r < 1$$

By the definition of $lim sup$, there exists an [integer](https://algebrica.org/integers/) $N$ such that for all $n \geq N$:

$$\sqrt[n]{\left|\right. a_{n} \left|\right.} < r \rightarrow \left|\right. a_{n} \left|\right. < r^{n}$$

So the tail of the series satisfies:

$$\sum_{n = N}^{\infty} \left|\right. a_{n} \left|\right. < \sum_{n = N}^{\infty} r^{n}$$

Since $0 < r < 1$, the [geometric series](https://algebrica.org/geometric-series) $\sum r^{n}$ converges. Therefore, by the [comparison test](https://algebrica.org/series-with-positive-terms/), the tail $\sum_{n = N}^{\infty} \left|\right. a_{n} \left|\right.$ converges, and so does the entire series $\sum \left|\right. a_{n} \left|\right.$.

---

Let us now consider the case in which the series diverges, assuming $L > 1$. Then, by definition of $lim sup$, for infinitely many indices $n$, we have:

$$\sqrt[n]{\left|\right. a_{n} \left|\right.} > r \text{for some} r > 1$$

Thus, $\left|\right. a_{n} \left|\right. > r^{n}$ infinitely often. But since $r^{n} \rightarrow \infty$, we know that $\left|\right. a_{n} \left|\right. \nrightarrow 0$.

Therefore, the necessary condition for convergence of $\sum a_{n}$ fails. So, the series diverges.

---

Let us consider the final case, where nothing can be concluded about the convergence of the series, namely, when $L = 1$. If $L = 1$, then for every $\epsilon > 0$, we can find infinitely many $n$ such that:

$$\sqrt[n]{\left|\right. a_{n} \left|\right.} > 1 - \epsilon \text{and} \sqrt[n]{\left|\right. a_{n} \left|\right.} < 1 + \epsilon$$

This range includes both convergent and divergent behaviors. For example, the [harmonic series](https://algebrica.org/harmonic-series) $a_{n} = \frac{1}{n}$ has $\sqrt[n]{\left|\right. a_{n} \left|\right.} \rightarrow 1$ and diverges. The [p-series](https://algebrica.org/harmonic-series) ( a_n = \frac{1}{n^2} ) also has $\sqrt[n]{\left|\right. a_{n} \left|\right.} \rightarrow 1$, but it converges. So, the test is inconclusive when $L = 1$.

## Example

Consider the series:

$$\sum_{n = 1}^{\infty} \left(\left(\right. \frac{3 n}{5 n + 2} \left.\right)\right)^{n}$$

We want to determine whether this series converges or diverges. In this case, we choose to apply the root test because each term of the series is given in the form $a_{n} = \left(\right. \text{expression} \left.\right)^{n}$. This structure makes the root test especially effective and simpler to use than other methods.

---

Let us define the [sequence](https://algebrica.org/sequences):

$$a_{n} = \left(\left(\right. \frac{3 n}{5 n + 2} \left.\right)\right)^{n}$$

To apply the root test, we evaluate the limit superior of the $n$-th root of $a_{n}$:

$$\underset{n \rightarrow \infty}{lim sup} \sqrt[n]{a_{n}} = \underset{n \rightarrow \infty}{lim} \left(\right. \frac{3 n}{5 n + 2} \left.\right)$$

Since the terms are positive, we omit the absolute value. Now we simplify the expression:

$$\frac{3 n}{5 n + 2} = \frac{3}{5 + \frac{2}{n}} \rightarrow \frac{3}{5} \text{as} n \rightarrow \infty$$

Therefore, we find:

$$\underset{n \rightarrow \infty}{lim sup} \sqrt[n]{a_{n}} = \frac{3}{5} < 1$$

Since the limit is less than 1, the Root Test tells us that the series converges absolutely.

## Glossary

- Infinite series: the sum of an infinite sequence of numbers, typically represented as $\sum_{n = 1}^{+ \infty} a_{n} .$
- [Convergence of a series](https://algebrica.org/series): an infinite series converges if the sequence of its partial sums approaches a finite limit.
- Absolute convergence: a series $\sum a_{n}$ converges absolutely if the series of the absolute values of its terms, $\sum \left|\right. a_{n} \left|\right.$, converges. Absolute convergence implies convergence.
- Root test: a method for determining the convergence or divergence of an infinite series by analyzing the limit of the $n$-th root of the absolute value of its terms.
- Limit superior: for a sequence, the largest limit point of the sequence. It is always defined for bounded sequences and provides a way to analyze the long-term behavior even if a standard limit does not exist.
- General term $a_{n}$: the formula or expression that defines the $n$-th term of a sequence or series.
- [Geometric series](https://algebrica.org/geometric-series): a series of the form $\sum_{n = 0}^{\infty} a r^{n}$, which converges if $\left|\right. r \left|\right. < 1$ and diverges if $\left|\right. r \left|\right. \geq 1.$
- [Comparison test](https://algebrica.org/series-with-positive-terms/): a test for the convergence or divergence of a series by comparing it to another series whose convergence or divergence is known.
