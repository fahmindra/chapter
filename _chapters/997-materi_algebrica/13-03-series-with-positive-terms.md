---
layout: chapter
title: "Series with Positive Terms"
chapter: "Series"
chapter_order: 13
section_order: 3
permalink: /materi-algebrica/series/series-with-positive-terms/
---

## What is a series with positive terms?

A series with positive terms is one in which every term $a_{k}$ satisfies $a_{k} > 0$ for all $k \in \mathbb{N}$. As a result, the sequence of partial sums:

$$S_{n} = \sum_{k = 1}^{n} a_{k}$$

is strictly increasing, since each new term contributes a positive quantity. This guarantees that the [series](https://algebrica.org/series) cannot oscillate or decrease. Such a series has only two possible behaviors: it either converges to a finite value if the partial sums are bounded above, or it diverges to infinity if they are not. It is never indeterminate or conditionally convergent. More formally, for a series of the form:

$$\sum_{k = 1}^{\infty} a_{k} \text{with} a_{k} > 0$$

the series converges if and only if the sequence of partial sums $\left(\right. S_{n} \left.\right)$ is bounded. This property makes positive-term series especially suitable for convergence tests such as the comparison test, the integral test, and the ratio test, all of which require non-negative terms.

---

The [harmonic series](https://algebrica.org/harmonic-series/) is an example of a positive-term series that diverges:

$$\sum_{k = 1}^{\infty} \frac{1}{k}$$

In fact, despite the fact that the terms $\frac{1}{k}$ tend to zero, the sequence of partial sums increases without limit.

In general, we refer to a constant-sign series when the terms of the sequence $a_{n}$ all have the same sign for every $n \in \mathbb{N}$; that is, they are either all positive or all negative.

## Comparison test

The **comparison test** is a method used to determine whether a series converges or diverges by comparing it to another series whose behavior is already known. It is particularly useful when dealing with series with positive terms, where direct evaluation of convergence is difficult.

Let $\sum a_{k}$ and $\sum b_{k}$ be two series with positive terms. Suppose there exists an [integer](https://algebrica.org/integers/) $N \in \mathbb{N}$ such that:

$$0 \leq a_{k} \leq b_{k} \text{for all} k \geq N$$

In other words, each term $a_{k}$ is non-negative and is less than or equal to the corresponding term $b_{k}$ (this condition is essential for applying the comparison test correctly). Then:

- If $\sum b_{k}$ converges, then $\sum a_{k}$ also converges.
- If $\sum a_{k}$ diverges, then $\sum b_{k}$ also diverges.

---

Let’s consider the partial sums of each series:

$$S_{n} = \sum_{k = 1}^{n} a_{k} , T_{n} = \sum_{k = 1}^{n} b_{k}$$

Since both sequences $a_{k}$ and $b_{k}$ are made of non-negative terms, both $S_{n}$ and $T_{n}$ are non-decreasing. Now, because $a_{k} \leq b_{k}$ for all $k \geq N$, we have:

$$S_{n} \leq T_{n} \text{for all} n \geq N$$

If the series $\sum b_{k}$ converges, that means $T_{n}$ has a finite limit — it is bounded above. Since $S_{n} \leq T_{n}$, the sequence of partial sums $S_{n}$ is also bounded above. And since $S_{n}$ is non-decreasing and bounded, it must converge. Therefore, $\sum a_{k}$ also converges.

If $\sum a_{k}$ diverges, then $S_{n} \rightarrow \infty$. But since $S_{n} \leq T_{n}$, the only way this inequality can hold is if $T_{n}$ also grows without bound. Therefore, $\sum b_{k}$ also diverges.

## Example

Using the comparison test, we determine the nature of the following series:

$$\sum_{n = 1}^{\infty} \frac{1}{n^{2} + 2 n + 1}$$

The series is a positive-term series, since the denominator is a polynomial and all terms are positive. Therefore, its nature can be determined using the comparison test.

##### It is important to verify this point, since the comparison test is only valid for series in which all terms are positive.

---

First, we check whether the necessary condition for convergence is satisfied:

$$\underset{n \rightarrow + \infty}{lim} \frac{1}{n^{2} + 2 n + 1} = 0$$

It is evident that the [limit](https://algebrica.org/limits) has the form $\frac{1}{\infty}$, which implies that it equals zero. The necessary condition for convergence is therefore satisfied. At this point, using the comparison test, we can state that:

$$\frac{1}{n^{2} + 2 n + 1} < \frac{1}{n^{2}}$$

since the denominator in the first expression is greater than the denominator in the second. Let

$$a_{n} = \frac{1}{n^{2} + 2 n + 1} \text{and} b_{n} = \frac{1}{n^{2}}$$

using the comparison test, we observe that

$$a_{n} < b_{n}$$

The series

$$\sum_{n = 1}^{\infty} b_{n} = \sum_{n = 1}^{\infty} \frac{1}{n^{2}}$$

is a [generalized harmonic series](https://algebrica.org/harmonic-series), which is known to converge when the exponent in the denominator satisfies the condition $p > 1$.

Hence, by the comparison test, since the series $\sum b_{n}$ converges, the series $\sum a_{n}$ also converges.

##### Determining the nature of a positive-term series using the comparison test is relatively straightforward, but it requires plenty of practice to choose the right comparison and justify the inequality correctly.

## Glossary

- Series with positive terms: a series where every term $a_{k}$ is greater than zero for all indices $k$.
- Sequence of partial sums $S_{n}$: the sequence formed by the sum of the first $n$ terms of a series, $S_{n} = \sum_{k = 1}^{n} a_{k}$.
- Strictly increasing sequence: a sequence where each term is greater than the previous term.
- Bounded above: a sequence is bounded above if there exists a number $M$ such that every term in the sequence is less than or equal to $M$.
- Constant-sign series: a series where all terms have the same sign (either all positive or all negative).
- Comparison test: a method used to determine the convergence or divergence of a series by comparing it term-by-term to another series whose behavior is already known.
- Harmonic series: The series $\sum_{k = 1}^{\infty} \frac{1}{k}$, which is a known example of a positive-term series that diverges.
- Generalized harmonic series: A series of the form $\sum_{n = 1}^{\infty} \frac{1}{n^{p}}$, which converges if $p > 1$ and diverges if $p \leq 1$.
- Necessary condition for convergence: For a series $\sum a_{k}$ to converge, it is necessary that $\underset{k \rightarrow \infty}{lim} a_{k} = 0$. However, this condition is not sufficient for convergence.
