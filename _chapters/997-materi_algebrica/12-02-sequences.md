---
layout: chapter
title: "Sequences"
chapter: "Sequences"
chapter_order: 12
section_order: 2
permalink: /materi-algebrica/sequences/sequences/
---

## What is a sequence

A sequence is an ordered collection of elements, each assigned to a specific position indexed by a [natural number](https://algebrica.org/natural-numbers/). Let us consider the set of real numbers $\mathbb{R}$. A sequence with values in $\mathbb{R}$ is a function of the form $\mathbb{N} \rightarrow \mathbb{R}$, that assigns to each $n \in \mathbb{N}$ a unique real number $a \left(\right. n \left.\right) \in \mathbb{R}$.

- A sequence $a : \mathbb{N} \rightarrow \mathbb{R}$ is denoted by $\left{\right. a_{n} \left.\right}_{n \in \mathbb{N}} .$
- Each element produced by the sequence is known as a term.
- The expression for $a_{n}$ defines the rule that determines every term of the sequence.

It is often useful to consider sequences defined only on a subset of natural numbers, such as those starting from a specific [integer](https://algebrica.org/integers/) value. These are sequences of the form:

$$a : n \in \mathbb{N} : n \geq n_{0} \rightarrow \mathbb{R} .$$

This means the sequence is defined for all natural numbers greater than or equal to some initial index $n_{0}$.

---

Consider, for example, the [function](https://algebrica.org/functions) $a : \mathbb{N}^{+} \rightarrow \mathbb{R}$ defined by $a \left(\right. n \left.\right) := \frac{1}{n}$. This is a real-valued sequence defined for every $n \in \mathbb{N}^{+}$, and its terms are:

$$a_{1} = 1 , a_{2} = \frac{1}{2} , \ldots , a_{n} = \frac{1}{n} \forall n \in \mathbb{N}^{+} .$$

---

Another example of a sequence is $a_{n} = n !$, the [factorial](https://algebrica.org/factorial) of $n$, which is defined as the product of all positive integers from 1 to $n$. The first few terms of the sequence are:

$$a_{1} = 1 , a_{2} = 2 , a_{3} = 6 , a_{4} = 24 , a_{5} = 120 , \ldots$$

## Example

Consider, for example, the formula:

$$a_{n} := \frac{1}{n - 2}$$

defines a real-valued sequence $a : 3 , 4 , 5 , \ldots \rightarrow \mathbb{R}$, where the values $3 , 4 , 5 , \ldots$ represent the indices of the sequence. Indeed, since the denominator becomes zero for $n = 2$, the term $a_{2}$ is undefined. To avoid this singularity, we restrict the [domain](https://algebrica.org/determining-the-domain-of-a-function/) to $n \geq 3$. In this case, we write the sequence as:

$$\left(\right. a_{n} \left.\right)_{n \geq 3} = \left(\left(\right. \frac{1}{n - 2} \left.\right)\right)_{n \geq 3}$$

The first few terms of the sequence are:

$$a_{3} = 1 , a_{4} = \frac{1}{2} , a_{5} = \frac{1}{3} , a_{6} = \frac{1}{4} , a_{7} = \frac{1}{5} , \ldots$$

As we can see, this sequence decreases and converges to zero as $n \rightarrow \infty$ (we will see later what this means).

## Recursively defined sequences

A recursive sequence is a sequence where each term is defined in terms of one or more of the preceding terms. To define such a sequence, two components are needed:

- An initial value.
- A recurrence relation, which determines how to compute each new term.

---

One of the most famous recursive sequences is the Fibonacci sequence, defined as:

$$\left{\right. a_{0} = 0 , \\ a_{1} = 1 , \\ a_{n} = a_{n - 1} + a_{n - 2} \text{for all} n \geq 2$$

This means that every term is the sum of the two preceding ones. The first few terms of the sequence are:

$$a_{0} & = 0 \\ a_{1} & = 1 \\ a_{2} & = 1 \\ a_{3} & = 2 \\ a_{4} & = 3 \\ a_{5} & = 5 \\ a_{6} & = 8 \\ & \vdots$$

##### Recursion is a common strategy in programming that allows complex tasks to be solved by repeatedly applying the same rule until a base case is reached. It’s especially effective for generating sequences and solving problems with a self-repeating structure.

## Monotonic sequences

A sequence can be classified based on how its terms evolve. In general, a sequence that satisfies any of these conditions is called a [monotonic sequence](https://algebrica.org/monotone-sequences/):

- Constant: if every term is equal to the previous one: $a_{n} = a_{n + 1} \forall n \in \mathbb{N}$.
- Increasing: if each term is greater than the previous one: $a_{n} < a_{n + 1} \forall n \in \mathbb{N}$.
- Decreasing: if each term is less than the previous one: $a_{n} > a_{n + 1} \forall n \in \mathbb{N}$.
- Non-decreasing: $a_{n} \leq a_{n + 1} \forall n \in \mathbb{N}$.
- Non-increasing: $a_{n} \geq a_{n + 1} \forall n \in \mathbb{N}$.

---

If a sequence $\left(\right. a_{n} \left.\right)_{n \in \mathbb{N}}$ is monotonic, then it admits a limit and this limit is finite. Moreover, the following holds:

$$\underset{n \rightarrow + \infty}{lim} a_{n} = \left{\right. sup a_{n} : n \in \mathbb{N} & \text{if} \left(\right. a_{n} \left.\right)_{n \in \mathbb{N}} \text{is increasing} \\ inf a_{n} : n \in \mathbb{N} & \text{if} \left(\right. a_{n} \left.\right)_{n \in \mathbb{N}} \text{is decreasing}$$

This result guarantees that bounded monotonic sequences always converge, and their limit corresponds to the supremum or infimum depending on the direction of monotonicity.

## Glossary

- Sequence: an ordered collection of elements, each assigned to a specific position indexed by a natural number.
- Term: each individual element produced by a sequence.
- Index: a natural number that indicates the position of a term within a sequence.
- Monotonic sequence: a sequence that is either constant, increasing, decreasing, non-decreasing, or non-increasing.
- Limit: the value that the terms of a sequence approach as the index $n$ goes to infinity.
- Supremum: the least upper bound of a set of numbers.
- Infimum: the greatest lower bound of a set of numbers.
