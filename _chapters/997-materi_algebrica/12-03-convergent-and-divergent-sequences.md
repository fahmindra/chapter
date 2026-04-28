---
layout: chapter
title: "Convergent and Divergent Sequences"
chapter: "Sequences"
chapter_order: 12
section_order: 3
permalink: /materi-algebrica/sequences/convergent-and-divergent-sequences/
---

## Behavior of a sequence

We introduced [sequences](https://algebrica.org/sequences) as an ordered collection of elements, each assigned to a specific position indexed by a [natural number](https://algebrica.org/types-of-numbers). To every sequence $\left(\right. a_{n} \left.\right)_{n \in \mathbb{N}}$, there is an associated behavior of its terms $a_{n}$ that describes how they evolve as the index $n$ increases. Analyzing this behavior helps determine whether the sequence converges to a finite [limit](https://algebrica.org/limits), diverges to infinity, or exhibits an oscillating pattern.

## Convergent sequence

A sequence $\left(\right. a_{n} \left.\right)_{n \in \mathbb{N}}$ is said to be **convergent to the limit** $ℓ \in \mathbb{R}$ if for every $\epsilon > 0$, there exists $n_{0} \in \mathbb{N}$ such that:

$$\left|\right. a_{n} - ℓ \left|\right. < \epsilon \text{for all} n \geq n_{0} .$$

In this case, we write:

$$\underset{n \rightarrow + \infty}{lim} a_{n} = ℓ \text{or} a_{n} \rightarrow ℓ \text{as} n \rightarrow + \infty .$$

In other words, this means that the terms of the sequence get increasingly close to the number $ℓ$ as $n$ grows larger. No matter how tight a margin $\epsilon$, from a certain index onward all terms will stay within that distance from $ℓ$. For example, consider the following sequence:
$$a_{n} = \left(\left(\right. \frac{1}{n} \left.\right)\right)_{n \geq} = \left(\right. 1 , \frac{1}{2} , \frac{1}{3} , \ldots \left.\right)$$

![Convergent sequence.](https://algebrica.org/wp-content/uploads/resources/images/sequences-conv-1.png)

As $n$ increases, the terms become smaller and smaller, approaching zero. This is a classic example of a sequence that converges to 0. A sequence is said to be **infinitesimal** when its terms get arbitrarily close to zero as the index grows and:

$$\underset{n \rightarrow + \infty}{lim} a_{n} = 0.$$

The limit of a sequence $\left(\right. a_{n} \left.\right)_{n \in \mathbb{N}}$, if it exists, is unique.

## Example

Let’s consider the sequence defined by:

$$a_{n} = \frac{n}{n + 2}$$

We aim to demonstrate that this sequence converges to 1 as $n \rightarrow + \infty$, using the formal definition of convergence.

---

To prove this, we must show that for every $\epsilon > 0$, there exists a natural number $n_{0}$ such that for all $n \geq n_{0}$:

$$\left|\right. \frac{n}{n + 2} - 1 \left|\right. < \epsilon$$

Let’s simplify the absolute value expression:

$$\left|\right. \frac{n}{n + 2} - 1 \left|\right. = \left|\right. \frac{- 2}{n + 2} \left|\right. = \frac{2}{n + 2} .$$

Now, we want:

$$\frac{2}{n + 2} < \epsilon$$

Solving the inequality:

$$n + 2 > \frac{2}{\epsilon} \Rightarrow n > \frac{2}{\epsilon} - 2$$

So we can define:

$$n_{0} = \lceil \frac{2}{\epsilon} - 2 \rceil$$

From this point onward, every term of the sequence stays within a distance $\epsilon$ of the limit $1.$ Hence, by definition:

$$\underset{n \rightarrow + \infty}{lim} \frac{n}{n + 2} = 1.$$

## Divergent sequence

A sequence $\left(\right. a_{n} \left.\right)_{n \in \mathbb{N}}$ is said to be **divergent** if it does not converge to a finite limit. This can happen in the following ways.

A sequence diverges to $+ \infty$ if, for every $M > 0$, there exists an index $n_{0} \in \mathbb{N}$ such that
 $$a_{n} > M \text{for all} n \geq n_{0}$$
In this case, we write:
$$\underset{n \rightarrow + \infty}{lim} a_{n} = + \infty \text{or} a_{n} \rightarrow + \infty \text{as} n \rightarrow + \infty$$

---

A sequence diverges to $- \infty$ if, for every $M < 0$, there exists an index $n_{0} \in \mathbb{N}$ such that
 $$a_{n} < M \text{for all} n \geq n_{0}$$
In this case, we write:
$$\underset{n \rightarrow + \infty}{lim} a_{n} = - \infty \text{or} a_{n} \rightarrow - \infty \text{as} n \rightarrow + \infty$$

## Bounded sequence

A bounded sequence is a sequence of numbers whose terms always stay within a fixed, finite interval, no matter how large the index becomes. In formal terms, let $a_{n}$ be a sequence. We say that the sequence is bounded if there exists a constant $M > 0$ such that:

$$\left|\right. a_{n} \left|\right. \leq M \forall n \in \mathbb{N}$$

We say that a sequence $a_{n}$ is bounded above if there exists a constant $M \in \mathbb{R}$ such that:

$$a_{n} \leq M \forall n \in \mathbb{N}$$

We say that the sequence is bounded below if there exists a constant $M \in \mathbb{R}$ such that:

$$a_{n} \geq M \forall n \in \mathbb{N}$$

## Oscillating sequence

Oscillating sequences are a special type of bounded sequence. Let us consider the sequence:

$$\left(\right. a_{n} \left.\right)_{n \in \mathbb{N}} = \left(\right. \left(\right. - 1 \left.\right)^{n} \left.\right)_{n \in \mathbb{N}} = \left(\right. + 1 , - 1 , + 1 , - 1 , + 1 , - 1 , \ldots \left.\right)$$

As the index $n$ increases, the terms of the sequence alternate consistently between $+ 1$ and $- 1$. This type of sequence does not approach any finite value and is called an **oscillating sequence**. It does not converge to a finite limit, nor does it diverge to $+ \infty$ or $- \infty$, and its terms continue to fluctuate between different values

![Oscillating sequence.](https://algebrica.org/wp-content/uploads/resources/images/sequences-conv-2.png)

## Geometric sequence

Let us consider an example of a sequence, called a [geometric sequence](https://algebrica.org/geometric-sequence/), which can display different behaviors depending on the fixed real number $q$. In general, a numerical sequence is called a geometric progression when the ratio between each term and its previous one is constant. More precisely, a geometric sequence is defined as follows:

$$a_{n} := q^{n}$$

It exhibits the following behavior:

- It diverges to $+ \infty$ if $q > 1$.
- It is constant (that is, $a_{n} = a_{0}$ for every $n \in \mathbb{N}$) if $q = 1$, and thus $\underset{n \rightarrow + \infty}{lim} a_{n} = a_{0} = 1.$
- It is infinitesimal if $\left|\right. q \left|\right. < 1$, meaning the terms approach zero.
- It is oscillatory (irregular) if $q \leq - 1$, due to alternating signs and unbounded growth.

![](https://algebrica.org/wp-content/uploads/resources/images/sequences-conv-3.png)

As shown in the graph, when $q = 2$, the values of the geometric sequence $a_{n} = q^{n}$ grow [exponentially](https://algebrica.org/exponential-function). As $n$ increases, each term doubles the previous one, leading to a rapid escalation in magnitude.

##### Take a closer look at the difference between an [arithmetic progression](https://algebrica.org/arithmetic-sequence) and a geometric progression to better understand how their structures and growth patterns differ.
