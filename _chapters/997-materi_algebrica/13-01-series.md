---
layout: chapter
title: "Series"
chapter: "Series"
chapter_order: 13
section_order: 1
permalink: /materi-algebrica/series/series/
---

## What is a series

The concept of a **series** is closely tied to infinite [sequences](https://algebrica.org/sequences) of [real numbers](https://algebrica.org/types-of-numbers), with the main goal of studying the behavior of their infinite sum. This involves determining whether the sum approaches a finite [limit](https://algebrica.org/limits) (convergence) or grows without bound (divergence). From a formal point of view, let $\left{\right. a_{n} \left.\right}_{n \in \mathbb{N}}$ be a sequence of real numbers. We define the partial sums of the sequence as follows:

$$s_{1} & = a_{1} \\ s_{2} & = a_{1} + a_{2} \\ s_{3} & = a_{1} + a_{2} + a_{3} \\ \vdots \\ s_{n} & = a_{1} + a_{2} + \hdots + a_{n}$$

The sequence $s_{n}$, with $n \geq 1$, is called the sequence of partial sums, and each term is given by:

$$s_{n} = \sum_{k = 1}^{n} a_{k}$$

A series with general term $a_{k}$ is defined as the formal expression:

$$\sum_{k = 1}^{\infty} a_{k}$$

## Nature of a series

The nature of a series is determined by analyzing the limit of its sequence of partial sums:

$$\underset{n \rightarrow \infty}{lim} s_{n} = \underset{n \rightarrow \infty}{lim} \sum_{k = 1}^{n} a_{k}$$

- If the limit exists and is finite, the series $\sum a_{n}$ is said to converge. In this case, the value of the limi is called the sum of the series.
- If the limit is $+ \infty$ or $- \infty$, the series $\sum a_{n}$ is said to diverge.
- In all other cases, such as when the limit does not exist or oscillates, the series $\sum a_{n}$ is considered indeterminate.

A series $\sum a_{k}$ is said to **converge absolutely** if the series of [absolute values](https://algebrica.org/absolute-value) $\sum \left|\right. a_{k} \left|\right.$ also converges. That is, the convergence is not affected by the signs of the terms.

##### The expression “sum of a series” is a conventional term: since infinitely many terms are involved, it is not a finite sum in the traditional sense, but the limit of the sequence of partial sums.

Altering a finite number of terms in the series does not affect its convergence or divergence. That is, two series that differ only by finitely many terms share the same convergence nature. However, they do not necessarily have the same sum.

## Necessary condition for convergence

Suppose that the series $\sum_{n = 1}^{\infty} a_{n}$ is convergent. As discussed above, this means that the sequence of partial sums converges to a finite limit. A necessary condition for convergence is:

$$\underset{n \rightarrow \infty}{lim} a_{n} = 0$$

In other words, the general term of the series must tend to zero. However, this condition is not sufficient: the fact that $a_{n} \rightarrow 0$ does not guarantee that the series converges.

---

This property can be proven by analyzing the sequence of partial sums $s_{n}$, where:

$$s_{n} = \sum_{k = 1}^{n} a_{k}$$

By definition, if the series converges, this sequence must tend to a finite limit. Let $S$ be the sum of the series; then:

$$S = \underset{n \rightarrow \infty}{lim} s_{n} = \underset{n \rightarrow \infty}{lim} s_{n - 1}$$

Since both $s_{n}$ and $s_{n - 1}$ converge to the same limit $S$, the difference between consecutive partial sums must tend to zero:

$$\underset{n \rightarrow \infty}{lim} \left(\right. s_{n} - s_{n - 1} \left.\right) = \underset{n \rightarrow \infty}{lim} a_{n} = S - S = 0$$

## Linear properties of series

Let $\sum_{k = 1}^{\infty} a_{k}$ be a convergent series, and let $\lambda \in \mathbb{R}$, $\lambda \neq 0$. Then the series $\sum_{k = 1}^{\infty} \lambda a_{k}$ also converges, and its sum is:

$$\sum_{k = 1}^{\infty} \lambda a_{k} = \lambda \sum_{k = 0}^{\infty} a_{k}$$

---

If both series $\sum_{k = 1}^{\infty} a_{k}$ and $\sum_{k = 1}^{\infty} b_{k}$ converge, then their term-by-term sum also defines a convergent series:

$$\sum_{k = 1}^{\infty} \left(\right. a_{k} + b_{k} \left.\right)$$

Moreover, the sum of the resulting series is equal to the sum of the individual series:

$$\sum_{k = 1}^{\infty} \left(\right. a_{k} + b_{k} \left.\right) = \sum_{k = 1}^{\infty} a_{k} + \sum_{k = 1}^{\infty} b_{k}$$

## Well-known series

Consider the following series:

$$\sum_{n = 1}^{\infty} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \hdots + \frac{1}{n} + \hdots$$

The series is called the harmonic series, and it is divergent.

---

The following series is called the [generalized harmonic series](https://algebrica.org/harmonic-series):

$$\sum_{n = 1}^{\infty} \frac{1}{n^{p}} = 1 + \frac{1}{2^{p}} + \frac{1}{3^{p}} + \hdots + \frac{1}{n^{p}} + \hdots , p \in \mathbb{R}$$

The convergence of the series depends on the value of $p$:

- If $p > 1$ the series converges.
- If $p \leq 1$ the series diverges.

---

Consider the [geometric series](https://algebrica.org/geometric-series/) of ratio $q$:

$$\sum_{n = 0}^{\infty} q^{n} = 1 + q + q^{2} + q^{3} + \hdots + q^{n} + \hdots$$

The convergence of the series depends on the value of $q$:

- If $- 1 < q < 1$, the series converges.
- If $q \geq 1$, the series diverges.
- If $q \leq - 1$, the series is irregular (diverges or oscillates).

---

Consider the following series, known as a telescoping series:

$$\sum_{n = 1}^{\infty} \frac{1}{n \left(\right. n + 1 \left.\right)} = \frac{1}{2} + \frac{1}{6} + \hdots + \frac{1}{n \left(\right. n + 1 \left.\right)} + \hdots = 1$$

This series is convergent.

## Glossary

- Series: the limit of the sum of the terms of a sequence.
- Sequence: an ordered list of numbers.
- Partial sums $s_{n}$: the sum of the first $n$ terms of a sequence.
- Convergence: a series converges if the limit of its sequence of partial sums is a finite number.
- Converge absolutely: a series $\sum a_{k}$ converges absolutely if the series of absolute values $\sum \left|\right. a_{k} \left|\right.$ converges.
- Divergence: a series diverges if the limit of its sequence of partial sums is $+ \infty$ or $- \infty$.
- Indeterminate: a series is indeterminate if the limit of its sequence of partial sums does not exist or oscillates.
- Sum of the series: the finite limit of the sequence of partial sums for a convergent series.
- General term $a_{n}$ or $a_{k}$: the formula or expression that defines each term of a sequence or series.
