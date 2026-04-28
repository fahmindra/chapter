---
layout: chapter
title: "Leibniz’s Criterion"
chapter: "Series"
chapter_order: 13
section_order: 8
permalink: /materi-algebrica/series/leibnizs-criterion/
---

## What is Leibniz’s criterion used for

Leibniz’s criterion is used to study the convergence of alternating [series](https://algebrica.org/series), those composed of an infinite sequence of positive and negative terms that alternate in sign. Consider the alternating series
$$\sum_{n = 1}^{+ \infty} \left(\right. - 1 \left.\right)^{n} a_{n}$$

where $a_{n} \geq 0 \forall n \in \mathbb{N}$. Leibniz’s criterion states that the series converges if the following conditions are satisfied:

- The [sequence](https://algebrica.org/sequence) $a_{n}$ is infinitesimal, that is the [limit](https://algebrica.org/limits) exists and is finite: $$\underset{n \rightarrow + \infty}{lim} a_{n} = 0$$
- $a_{n}$ is eventually non-increasing, that is there exists an index $n_{0}$ such that for every $n \geq n_{0}$, it holds that:
  $$a_{n + 1} \leq a_{n}$$

---

In practice, Leibniz’s criterion allows one to immediately establish the convergence of a series based solely on the verification of the above conditions. However, the test is not generalizable and applies only to alternating series.

---

If the series

$$\sum_{n = 1}^{+ \infty} \left(\right. - 1 \left.\right)^{k} a_{k}$$

is convergent and $S$ is its sum, then for every $n \in \mathbb{N}$, the error made by truncating the series at the $n$-th term is at most equal to the next term $a_{n + 1}$:

$$\left|\right. S - \sum_{k = 1}^{n} \left(\right. - 1 \left.\right)^{k} a_{k} \left|\right. \leq a_{n + 1} .$$

This means that if you are summing the alternating [harmonic series](https://algebrica.org/harmonic-series):

$$\sum_{n = 1}^{+ \infty} \frac{\left(\right. - 1 \left.\right)^{n}}{n}$$

and you stop at the term $n = 10$, then the maximum error you are making is:

$$\left|\right. S - \sum_{k = 1}^{10} \frac{\left(\right. - 1 \left.\right)^{k}}{k} \left|\right. \leq \frac{1}{11}$$

Leibniz’s criterion only tells us whether an alternating series converges; it provides no information about the actual sum of the series. To compute the sum, one must use other tools such as Taylor or Maclaurin series expansions, when available.

## Proof

Let $a_{n}$ be a sequence of [positive real numbers](https://algebrica.org/series-with-positive-terms/) such that $a_{n} \geq a_{n + 1} \forall n$, and $\underset{n \rightarrow \infty}{lim} a_{n} = 0$. We consider the alternating series:

$$\sum_{n = 1}^{\infty} \left(\right. - 1 \left.\right)^{n + 1} a_{n}$$

and aim to prove that it converges.

---

To do this, we examine the sequence of partial sums:

$$S_{n} = \sum_{k = 1}^{n} \left(\right. - 1 \left.\right)^{k + 1} a_{k}$$

We analyze this sequence by distinguishing between the even and odd partial sums. When $n$ is even, say $n = 2 m$, the sum becomes:

$$S_{2 m} = a_{1} - a_{2} + a_{3} - a_{4} + \hdots + a_{2 m - 1} - a_{2 m} .$$

Grouping the terms in pairs gives:

$$S_{2 m} = \left(\right. a_{1} - a_{2} \left.\right) + \left(\right. a_{3} - a_{4} \left.\right) + \hdots + \left(\right. a_{2 m - 1} - a_{2 m} \left.\right) .$$

Since the sequence $a_{n}$ is decreasing, each difference $a_{k} - a_{k + 1}$ is non-negative. Therefore, each term in the grouped sum is positive, and the sequence $\left{\right. S_{2 m} \left.\right}$ is increasing. Additionally, since each $a_{n} > 0$, the total sum is bounded above by $a_{1}$. Thus the subsequence $\left{\right. S_{2 m} \left.\right}$ converges.

---

Next, we observe that the odd partial sums can be written as

$$S_{2 m + 1} = S_{2 m} + a_{2 m + 1} .$$

Since $\underset{n \rightarrow \infty}{lim} a_{n} = 0$, the difference between $S_{2 m + 1}$ and $S_{2 m}$ tends to zero as $m \rightarrow \infty$. Therefore, both subsequences $\left{\right. S_{2 m} \left.\right}$ and $\left{\right. S_{2 m + 1} \left.\right}$ converge to the same limit.

It follows that the full sequence $\left{\right. S_{n} \left.\right}$ of partial sums converges, and hence the alternating series is convergent.

## Example

Let us consider the following alternating series:

$$\sum_{n = 1}^{+ \infty} \frac{\left(\right. - 1 \left.\right)^{n}}{n !}$$

We define $a_{n} = \frac{1}{n !}$, in this way we focus on analyzing the behavior of the [absolute values](https://algebrica.org/absolute-value) of the terms, which is essential when applying Leibniz’s criterion.

---

To apply Leibniz’s criterion, we need to verify three conditions. First, the terms $a_{n}$ are all positive for every $n \in \mathbb{N}$. Second, the sequence $a_{n}$ is decreasing. In fact, since the [factorial](https://algebrica.org/factorial) function grows rapidly, we have:

$$a_{n + 1} = \frac{1}{\left(\right. n + 1 \left.\right) !} < \frac{1}{n !} = a_{n}$$

This confirms that the sequence is strictly decreasing. Third, the limit of the general term is zero:

$$\underset{n \rightarrow + \infty}{lim} \frac{1}{n !} = 0$$

Since all three conditions are satisfied, Leibniz’s criterion ensures that the series

$$\sum_{n = 1}^{+ \infty} \frac{\left(\right. - 1 \left.\right)^{n}}{n !}$$

converges.

## Determine the nature of the following series.

- $$\text{1}. \sum_{n = 3}^{\infty} \left(\right. - 1 \left.\right)^{n} \frac{1}{log ⁡ n}$$ [solution](https://algebrica.org/)
- $$\text{2}. \sum_{n = 1}^{\infty} \left(\right. - 1 \left.\right)^{n} sin ⁡ \left(\right. \frac{1}{n} \left.\right)$$ [solution](https://algebrica.org/)
- $$\text{3}. \sum_{n = 1}^{\infty} \left(\right. - 1 \left.\right)^{n} \frac{log ⁡ n}{n e^{n}}$$ [solution](https://algebrica.org/)

##### The proposed alternating series are selected to help you strengthen your understanding of convergence using Leibniz’s criterion. Try analyzing each series to determine whether the conditions are satisfied before checking the provided solutions.

## Glossary

- Alternating series: a series in which the terms alternate in sign.
- Convergence: the property of an infinite series whose partial sums approach a finite limit as the number of terms increases indefinitely.
- Leibniz’s Criterion: a test used to determine the convergence of alternating series based on the properties of the sequence of the absolute values of the terms.
- Infinitesimal sequence: a sequence whose limit as the index approaches infinity is zero.
- Sum of a series: the finite limit that the partial sums of a convergent series approach.
  Partial Sum: The sum of the first n terms of an infinite series.
