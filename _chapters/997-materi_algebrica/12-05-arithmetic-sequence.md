---
layout: chapter
title: "Arithmetic Sequence"
chapter: "Sequences"
chapter_order: 12
section_order: 5
permalink: /materi-algebrica/sequences/arithmetic-sequence/
---

## What is an arithmetic sequence

A [sequence](https://algebrica.org/sequences) $a_{n}$ is called an **arithmetic sequence** (or arithmetic progression) if it consists of numbers arranged in such a way that the difference between any term and the one before it is constant. It is characterized by terms of the form:

$$a_{1} , a_{2} , \ldots , a_{n} \text{with} a_{n} - a_{n - 1} = d$$

- By convention, the first term of an arithmetic progression is typically indexed with $n = 1.$
- $d$ represents the difference between two consecutive terms in an arithmetic progression, and it is known as the common difference.
- If $d > 0$, the progression is increasing.
- If $d < 0$, the progression is decreasing.
- If $d = 0$, the progression is constant.

Let’s consider, for example, the sequence of non-negative even numbers:

![](https://algebrica.org/wp-content/uploads/resources/images/arithmetic-sequence.png)

---

An arithmetic sequence can also be defined using a recursive formula:

$$a_{n} = a_{1} + n \cdot d \text{where} a_{1} , d \in \mathbb{R}$$

![](https://algebrica.org/wp-content/uploads/resources/images/arithmetic-sequence-2.png)

An arithmetic progression exhibits a characteristic stepwise pattern, where the height of each step corresponds to the common difference between consecutive terms in the sequence.

---

In an arithmetic progression, each term $a_{n}$ is obtained by adding the first term $a_{1}$ to the product of the common difference $d$ and $\left(\right. n - 1 \left.\right)$. This gives the general formula for the $n$-th term:

$$a_{n} = a_{1} + \left(\right. n - 1 \left.\right) \cdot d \text{for} n \geq 1$$

This formula allows you to compute any term in the sequence directly, without listing all the previous ones.

## Example

Let’s define an arithmetic sequence with first term $a_{1} = 2$ and common difference $d = 3$. We use the formula:

$$a_{n} = a_{1} + \left(\right. n - 1 \left.\right) \cdot d$$

Plug in the values:

$$a_{n} = 2 + \left(\right. n - 1 \left.\right) \cdot 3$$

Now calculate the first few terms:

- $a_{1} = 2$
- $a_{2} = 2 + 1 \cdot 3 = 5$
- $a_{3} = 2 + 2 \cdot 3 = 8$
- $a_{4} = 2 + 3 \cdot 3 = 11$
- $a_{5} = 2 + 4 \cdot 3 = 14$

The resulting sequence is:
 $$2 , 5 , 8 , 11 , 14 , \ldots$$

## Sum of $n$ terms of an arithmetic progression

The sum $S_{n}$ of the first $n$ terms $a_{1} , a_{2} , \ldots , a_{n}$ of an arithmetic progression is equal to the product of $n$ and the average of the first and last term:

$$S_{n} = n \cdot \frac{a_{1} + a_{n}}{2}$$

This formula allows you to quickly compute the total sum of a finite number of terms in an arithmetic progression. For example, consider the arithmetic progression of non-negative even numbers:
 $$2 , 4 , 6 , 8 , 10$$

We want to calculate the sum of the first 5 terms $\left(\right. n = 5 \left.\right) .$ Using the formula, we have:
 $$S_{5} = 5 \cdot \frac{2 + 10}{2} = 5 \cdot 6 = 30$$

##### This illustrates the same reasoning behind Gauss’s trick: by pairing the first and last terms, you can quickly compute the total sum of an arithmetic progression.
