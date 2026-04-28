---
layout: chapter
title: "Cauchy Sequence"
chapter: "Sequences"
chapter_order: 12
section_order: 7
permalink: /materi-algebrica/sequences/cauchy-sequence/
---

## What is a Cauchy sequence

A **Cauchy sequence** is a special type of [sequence](https://algebrica.org/sequences) where, as you move further along, the terms get closer and closer to each other. It doesn’t matter what the [limit](https://algebrica.org/limits) is or even if you know it: what matters is that the difference between the terms becomes smaller and smaller. This idea is important because it helps us understand whether a sequence is behaving in a stable way, even before knowing exactly what it’s approaching. In formal terms:

---

Let $a_{n}$ be a sequence. Then $a_{n}$ is a Cauchy sequence if and only if it is convergent. In other words, the following condition holds:

$$\forall \epsilon > 0 \exists \nu \in \mathbb{N} : \left|\right. a_{n} - a_{m} \left|\right. < \epsilon \forall n , m > \nu$$

##### This criterion also applies to [series](https://algebrica.org/series) and allows us to prove [convergence](https://algebrica.org/cauchy-convergence-criterion-series/) without knowing the exact value of the sum. Instead of computing a limit, we check whether the terms of the sequence of partial sums get arbitrarily close to one another.

---

A sequence of the form $a_{n} = \frac{1}{n}$ is a Cauchy sequence, where the values get closer and closer to each other as ( n ) increases. When plotted on a graph, it shows:

- a curve starting from $a_{1} = 1$ that decreases rapidly,
- points that become increasingly dense near zero,
- the distance between any two terms $a_{n}$ and $a_{m}$, for large $n$ and $m$, becomes smaller and smaller.

![Convergent sequence.](https://algebrica.org/wp-content/uploads/resources/images/sequences-conv-1.png)

As $n$ increases, the terms become smaller and smaller, approaching zero. This is a classic example of a sequence that converges to 0.

---

Another example of a Cauchy sequence is given by the sequence defined as:

$$a_{n} = 1 + \frac{1}{2} + \frac{1}{4} + \hdots + \frac{1}{2^{n}}$$

This is the sum of the first $n$ terms of a geometric progression with ratio $\frac{1}{2}$. This sequence is a Cauchy sequence because:

- The terms get closer and closer to each other.
- Each new term adds less and less to the total sum.
- The distance between $a_{n}$ and $a_{m}$ (for $m > n$) becomes extremely small, since you are only adding values like:
   $\\ \frac{1}{2^{n + 1}} , \frac{1}{2^{n + 2}} , \ldots$

![](https://algebrica.org/wp-content/uploads/resources/images/cauchy-sequence-1.png)

In the limit, this sequence converges to $2$, reinforcing that it is both a Cauchy and convergent sequence.

##### In general, a numerical sequence is called a [geometric progression](https://algebrica.org/sequences) when the ratio between each term and its previous one is constant

## Theorem

Every convergent sequence $\left(\right. x_{n} \left.\right)_{n}$ is a Cauchy sequence.

##### A Cauchy allows us to detect convergence based solely on how close the terms get to each other, without needing to know the actual limit. In complete spaces like the real numbers, this internal consistency is enough to ensure the sequence converges.

---

In fact, let $\left(\right. x_{n} \left.\right)$ be a convergent sequence in $\mathbb{R}$, and let $L \in \mathbb{R}$ be its limit. By definition of convergence we have:

$$\forall \epsilon > 0 , \exists N \in \mathbb{N} \text{such that} \left|\right. x_{n} - L \left|\right. < \frac{\epsilon}{2} \forall n \geq N$$

Now, for any $n , m \geq N$, we apply the triangle inequality:

$$\left|\right. x_{n} - x_{m} \left|\right. = \left|\right. x_{n} - L + L - x_{m} \left|\right. \leq \left|\right. x_{n} - L \left|\right. + \left|\right. x_{m} - L \left|\right. < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

Thus, we have:

$$\forall \epsilon > 0 , \exists N \in \mathbb{N} \text{such that} \left|\right. x_{n} - x_{m} \left|\right. < \epsilon \forall n , m \geq N$$

This is exactly the definition of a Cauchy sequence. Therefore, every convergent sequence is a Cauchy sequence.

## Theorem

Every Cauchy sequence $\left(\right. x_{n} \left.\right)$ is also a [bounded sequence](https://algebrica.org/convergent-and-divergent-sequences/). In fact, by definition, if $\left(\right. x_{n} \left.\right)$ is a Cauchy sequence, then:

$$\forall \epsilon > 0 , \exists N \in \mathbb{N} \text{such that} \left|\right. x_{n} - x_{m} \left|\right. < \epsilon \forall n , m \geq N$$

Let’s choose $\epsilon = 1$. Then there exists $N \in \mathbb{N}$ such that:

$$\left|\right. x_{n} - x_{m} \left|\right. < 1 \forall n , m \geq N$$

Fix $m = N$, so we get:

$$\left|\right. x_{n} - x_{N} \left|\right. < 1 \Rightarrow \left|\right. x_{n} \left|\right. \leq \left|\right. x_{N} \left|\right. + 1 \forall n \geq N$$

Now define:

$$M_{1} := max \left|\right. x_{0} \left|\right. , \left|\right. x_{1} \left|\right. , \ldots , \left|\right. x_{N - 1} \left|\right. , M_{2} := \left|\right. x_{N} \left|\right. + 1$$

Let:

$$M := max M_{1} , M_{2} \Rightarrow \left|\right. x_{n} \left|\right. \leq M \forall n \in \mathbb{N}$$

Therefore, the sequence $\left(\right. x_{n} \left.\right)$ stays entirely within a finite interval and is thus bounded.
