---
layout: chapter
title: "Cauchy’s Convergence Criterion for Series"
chapter: "Series"
chapter_order: 13
section_order: 2
permalink: /materi-algebrica/series/cauchys-convergence-criterion-for-series/
---

## Introduction

**Cauchy’s criterion** is a useful tool for proving that a [series](https://algebrica.org/series) converges without needing to know its sum. Rather than computing the exact value of the series, the criterion checks whether the partial sums eventually become arbitrarily close to one another. If this condition holds, we can conclude that the series converges even if the actual [limit](https://algebrica.org/limits) remains unknown.

This criterion relies on the [Cauchy convergence criterion](https://algebrica.org/cauchy-sequence/) for [sequences](https://algebrica.org/sequences), which states that a sequence $a_{n}$ is convergent if and only if:

$$\forall \epsilon > 0 \exists \nu \in \mathbb{N} : \left|\right. a_{n} - a_{m} \left|\right. < \epsilon \forall n , m > \nu$$

##### A nice aspect of Cauchy’s approach is that it lets us understand a series by looking only at how its partial sums behave, without chasing the actual value they might approach. This perspective is especially helpful in proofs, where what matters is the structure of the argument rather than the final numerical outcome.

## Cauchy’s convergence criterion

Let $\sum_{k = 1}^{\infty} a_{k}$ be a series. According to Cauchy’s criterion, the series is convergent if and only if the following condition holds:

$$\forall \epsilon > 0 \exists \nu \in \mathbb{N} : \left|\right. \sum_{k = \nu + 1}^{\nu + p} a_{k} \left|\right. < \epsilon \forall p \in \mathbb{N}$$

In simple words, the sum of any tail of the series, starting from some sufficiently large index, must be arbitrarily small. This ensures that the partial sums become closer and closer, which implies convergence.

---

To prove this, we apply the Cauchy convergence criterion for sequences to the given series.

- Recall that a series $\sum a_{k}$ converges if and only if the sequence of its partial sums $s_{n} = \sum_{k = 1}^{n} a_{k}$ converges.
- Therefore, the series converges if and only if the sequence $\left(\right. s_{n} \left.\right)$ is a Cauchy sequence.

In the case of a series, the difference between two partial sums can be written as:

$$s_{n + p} - s_{n} = \sum_{k = n + 1}^{n + p} a_{k}$$

Taking the absolute value, we get:

$$\left|\right. s_{n + p} - s_{n} \left|\right. = \left|\right. \sum_{k = n + 1}^{n + p} a_{k} \left|\right.$$

In simpler terms, the Cauchy criterion for sequences requires that:

$$\left|\right. s_{n + p} - s_{n} \left|\right. < \epsilon$$

for all $p \in \mathbb{N}$, provided that $n$ is large enough. In our case, the expression:

$$\left|\right. \sum_{k = n + 1}^{n + p} a_{k} \left|\right.$$

represents a tail of the series. If this tail becomes small when $n$ is large enough, then it behaves just like the $\epsilon$ in the Cauchy condition for sequences. In other words, the tail plays the role of the difference we want to make arbitrarily small. For this reason, the criterion is proven.

## Example 1

Let’s use Cauchy’s criterion to prove that the [geometric series](https://algebrica.org/geometric-series/):

$$\sum_{k = 0}^{\infty} x^{k}$$

converges when $\left|\right. x \left|\right. < 1$. We consider the tail of the series starting from index $n + 1$:

$$\left|\right. \sum_{k = n + 1}^{n + p} x^{k} \left|\right. = \left|\right. x^{n + 1} + x^{n + 2} + \hdots + x^{n + p} \left|\right.$$

This is a finite geometric sum, which we can compute explicitly:

$$\left|\right. \sum_{k = n + 1}^{n + p} x^{k} \left|\right. = \left|\right. x^{n + 1} \cdot \frac{1 - x^{p}}{1 - x} \left|\right. = \frac{\left|\right. x \left|\right.^{n + 1} \cdot \left|\right. 1 - x^{p} \left|\right.}{\left|\right. 1 - x \left|\right.}$$

Since $\left|\right. x \left|\right. < 1$, we have $\left|\right. x \left|\right.^{n + 1} \rightarrow 0$ as $n \rightarrow \infty$, and the other factors remain bounded. Therefore, for any $\epsilon > 0$, we can find $n$ large enough so that the entire expression is less than $\epsilon .$

##### This works precisely because $x^{k}$ is the general term of a [geometric sequence](https://algebrica.org/geometric-sequence/).

This shows that the tail becomes arbitrarily small, which satisfies Cauchy’s criterion.

## Example 2

Let’s now prove that the geometric series:

$$\sum_{k = 0}^{\infty} x^{k}$$

converges for a specific value, for example $x = 0.5$. Since $\left|\right. x \left|\right. < 1$, we expect the series to converge. To apply Cauchy’s convergence criterion, we examine the size of the tail:

$$\left|\right. \sum_{k = n + 1}^{n + p} x^{k} \left|\right.$$

---

We can evaluate the sum using the formula:

$$\sum_{k = n + 1}^{n + p} x^{k} = x^{n + 1} \cdot \frac{1 - x^{p}}{1 - x}$$

Taking the absolute value gives:

$$\left|\right. \sum_{k = n + 1}^{n + p} x^{k} \left|\right. = \frac{\left(\right. 0.5 \left.\right)^{n + 1} \cdot \left|\right. 1 - \left(\right. 0.5 \left.\right)^{p} \left|\right.}{\left|\right. 1 - 0.5 \left|\right.} = 2 \cdot \left(\right. 0.5 \left.\right)^{n + 1} \cdot \left|\right. 1 - \left(\right. 0.5 \left.\right)^{p} \left|\right.$$

---

Now note:

- $\left(\right. 0.5 \left.\right)^{n + 1} \rightarrow 0$ as $n \rightarrow \infty$
- $\left|\right. 1 - \left(\right. 0.5 \left.\right)^{p} \left|\right. \leq 1$ for all $p \in \mathbb{N}$

Therefore:

$$\left|\right. \sum_{k = n + 1}^{n + p} x^{k} \left|\right. \leq 2 \cdot \left(\right. 0.5 \left.\right)^{n + 1}$$

---

Since the right-hand side tends to zero as $n \rightarrow \infty$, for any $\epsilon > 0$, we can find $n$ large enough so that:

$$\left|\right. \sum_{k = n + 1}^{n + p} x^{k} \left|\right. < \epsilon \text{for all} p \in \mathbb{N}$$

---

This behavior is illustrated in the following plot, which shows how the partial sums $s_{n}$ rapidly approach the exact value of the series, which is $2$ when $x = 0.5$.

![](https://algebrica.org/wp-content/uploads/resources/images/series-cauchy-1.png)

This satisfies Cauchy’s convergence criterion. So the series converges for $x = 0.5$.

## Glossary

- Cauchy’s criterion: a mathematical test used to determine the convergence of sequences and series without necessarily finding the limit or sum.
- Convergent Series: A series whose sequence of partial sums approaches a finite limit.
- Partial sums $s_{n}$: the sum of the first $n$ terms of a series, $s_{n} = \sum_{k = 1}^{n} a_{k}$.
- Cauchy sequence: a sequence in which the terms become arbitrarily close to each other as the sequence progresses.
- Epsilon $\epsilon$: a small positive number, typically used in definitions of limits and continuity to represent an arbitrarily small distance.
- Nu $\nu$: an index (usually an [integer](https://algebrica.org/integers/)) that is sufficiently large to satisfy a given condition in a convergence definition.
- Tail of a series: the sum of the terms of a series starting from a specific index, often represented as $\sum_{k = \nu + 1}^{\infty} a_{k}$ or, in the context of the criterion, a finite portion of the tail $\sum_{k = \nu + 1}^{\nu + p} a_{k}$.
