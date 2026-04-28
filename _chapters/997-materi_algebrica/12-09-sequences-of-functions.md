---
layout: chapter
title: "Sequences of Functions"
chapter: "Sequences"
chapter_order: 12
section_order: 9
permalink: /materi-algebrica/sequences/sequences-of-functions/
---

## Introduction

Imagine you have a list of different [functions](https://algebrica.org/functions), where each function in the list is linked to a number $n = 1 , 2 , 3 \ldots \in \mathbb{N}$. So, for each $n$, you get a different function, and that ordered list of functions is essentially what a [sequence](https://algebrica.org/sequences) of functions is. In formal terms, let $A \subseteq \mathbb{R}$ be a non-empty subset and suppose that for each $n \in \mathbb{N}$ we have a function $f_{n} : A \rightarrow \mathbb{R}$. We then say that $\left(\right. f_{n} \left.\right) = \left(\right. f_{1} , f_{2} , f_{3} , \ldots \left.\right)$ is a **sequence of functions** on $A .$

---

Let’s consider a simple practical example. Let $\left(\right. f_{n} \left.\right)$ be a sequence of functions, with $n \in \mathbb{N}_{0}$ and $x \in \mathbb{R}$, defined by:

$$f_{n} \left(\right. x \left.\right) = \frac{x}{n + 1}$$

This is a family of functions where each function is linear, and the slope decreases as $n$ increases. For $n = 0 , 1 , 2 , 3 , \ldots$, we have:

$$f_{0} \left(\right. x \left.\right) & = \frac{x}{0 + 1} = x \\ f_{1} \left(\right. x \left.\right) & = \frac{x}{1 + 1} = \frac{x}{2} \\ f_{2} \left(\right. x \left.\right) & = \frac{x}{2 + 1} = \frac{x}{3} \\ f_{3} \left(\right. x \left.\right) & = \frac{x}{3 + 1} = \frac{x}{4} \\ \vdots$$

Thus, the sequence of functions is:

$$\left(\right. f_{n} \left.\right) = \left(\right. x , \frac{x}{2} , \frac{x}{3} , \frac{x}{4} , \ldots \left.\right)$$

Graphically, this situation can be observed as follows:

![](https://algebrica.org/wp-content/uploads/resources/images/sequence-functions-1.png)

The graph shows how, as the index $n$ increases, the slope of the line $f_{n} \left(\right. x \left.\right)$ progressively decreases. This reflects the fact that the function flattens toward the zero function $f \left(\right. x \left.\right) = 0$ for every $x$. In other words, the sequence of functions $f_{n} \left(\right. x \left.\right)$ converges pointwise to the zero function as $n$ approaches infinity.

## Pointwise convergence

Let $\left{\right. f_{n} \left(\right. x \left.\right) \left.\right}$ be a sequence of functions defined on a common [domain](https://algebrica.org/determining-the-domain-of-a-function/) $A \subseteq \mathbb{R}$, with $n \in \mathbb{N}$. We say that the sequence $\left{\right. f_{n} \left(\right. x \left.\right) \left.\right}$ converges pointwise on a set $C \subseteq A$ if, for every $x \in C$, the numerical sequence $\left{\right. f_{n} \left(\right. x \left.\right) \left.\right}$ converges. In this case, the [limit](https://algebrica.org/limits) function $f \left(\right. x \left.\right)$ is defined as:

$$f \left(\right. x \left.\right) = \underset{n \rightarrow + \infty}{lim} f_{n} \left(\right. x \left.\right) \forall x \in C$$

The set $C$ is called the **pointwise convergence** set of the sequence $f_{n} \left(\right. x \left.\right)$.

---

Pointwise convergence can also be expressed as follows. Let $\left(\right. f_{n} \left.\right)$ be a sequence of functions defined on a set $A$. Then $\left(\right. f_{n} \left.\right)$ converges pointwise to $f : A \rightarrow \mathbb{R}$ if and only if $\forall x \in A$ and $\forall \epsilon > 0$ exists $K \in \mathbb{N}$ such that:

$$\left|\right. f_{n} \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left|\right. < \epsilon \forall n \geq K$$

##### In other words, for each fixed point $x$, we can make $f_{n} \left(\right. x \left.\right)$ as close as we like to $f \left(\right. x \left.\right)$ by choosing $n$ large enough. The index $K$ required to achieve the desired accuracy may vary depending on $x$ and $\epsilon$.

---

Let us consider the sequence of functions as previously discussed:

$$f_{n} \left(\right. x \left.\right) = \frac{x}{n + 1} , x \in \mathbb{R} , n \in \mathbb{N}_{0}$$

Let us examine what happens for each $x$ as $n \rightarrow \infty$. If we fix a generic $x$, for example $x = 2$, the associated sequence is:

$$f_{0} \left(\right. 2 \left.\right) & = 2 \\ f_{1} \left(\right. 2 \left.\right) & = 1 \\ f_{2} \left(\right. 2 \left.\right) & = \frac{2}{3} \\ f_{3} \left(\right. 2 \left.\right) & = \frac{2}{4} \\ & \vdots$$

This sequence of numbers tends to zero as $n \rightarrow \infty$. In general, for every $x \in \mathbb{R}$:

$$\underset{n \rightarrow \infty}{lim} f_{n} \left(\right. x \left.\right) = \underset{n \rightarrow \infty}{lim} \frac{x}{n + 1} = 0$$

Therefore, the limit function is:

$$f \left(\right. x \left.\right) = 0 \forall x \in \mathbb{R}$$

By the uniqueness of limits of sequences of real numbers, the pointwise limit of a sequence of functions $\left(\right. f_{n} \left.\right)$ is unique.

## Example

Let’s study the behavior of the following sequence of functions in the interval $- 1 < x < 1$:

$$f_{n} \left(\right. x \left.\right) = x^{n}$$

For a fixed value of $x$ in this interval, we know that the [absolute value](https://algebrica.org/absolute-value) of $x$ is less than $1$, that is, $\left|\right. x \left|\right. < 1$. This means we are considering [powers](https://algebrica.org/powers) of a number smaller than $1$ in absolute value. By properties of [exponents](https://algebrica.org/exponential-function), when the base has an absolute value less than $1$, the sequence $x^{n}$ tends to zero as $n$ tends to infinity:

$$\underset{n \rightarrow \infty}{lim} x^{n} = 0$$

The sequence of powers of a real number $x$ with $\left|\right. x \left|\right. < 1$ converges to zero.

Therefore, for every $x$ in the interval $- 1 < x < 1$, the sequence of functions $f_{n} \left(\right. x \left.\right) = x^{n}$ converges pointwise to the zero function.

$$f \left(\right. x \left.\right) = 0 \forall x \in \left(\right. - 1 , 1 \left.\right)$$

## Consequences of pointwise convergence

Let $f_{n}$ be a sequence of functions $f_{n} : A \rightarrow \mathbb{R}$ that converges pointwise to a function $f : A \rightarrow \mathbb{R}$. The following properties hold:

- If each $f_{n} \left(\right. x \left.\right) \geq 0$ for all $x \in A$, then $f \left(\right. x \left.\right) \geq 0$ for all $x \in A$. In practice, if each function $f_{n} \left(\right. x \left.\right)$ is non-negative on $A$, then the limit function $f \left(\right. x \left.\right)$ will also be non-negative on $A$. This reflects the fact that the limit of a sequence of non-negative real numbers cannot be negative.
- If each $f_{n}$ is non-decreasing on $A$, then $f$ is non-decreasing on $A$. Consequently, if each function $f_{n}$ is non-decreasing on $A$, then the limit function $f$ will also be non-decreasing on $A$. In other words, the property of monotonicity is preserved under pointwise convergence.

## Uniform convergence

Let $\left(\right. f_{n} \left.\right)$ be a sequence of functions defined on a set $A \subseteq \mathbb{R}$. We say that $\left(\right. f_{n} \left.\right)$ **converges uniformly** on $A$ to the function $f : A \rightarrow \mathbb{R}$ if, for any $\epsilon > 0$, there exists a [natural number](https://algebrica.org/natural-numbers/) $K$ such that, for all $n \geq K$ and all $x \in A$, the following inequality holds:

$$\left|\right. f_{n} \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left|\right. < \epsilon$$

If $\left(\right. f_{n} \left.\right)$ converges uniformly to $f$, then $\left(\right. f_{n} \left.\right)$ also converges pointwise to $f .$

---

Let us consider the sequence of functions:

$$f_{n} \left(\right. x \left.\right) = \frac{x}{n} , x \in \left[\right. 0 , 1 \left]\right. , n \in \mathbb{N} .$$

For each fixed $x$ in the interval $\left[\right. 0 , 1 \left]\right.$, we have:

$$\underset{n \rightarrow \infty}{lim} f_{n} \left(\right. x \left.\right) = 0$$

This means that the sequence $f_{n} \left(\right. x \left.\right)$ converges pointwise to the function (f(x) = 0). Let us now check whether the convergence is uniform on $\left[\right. 0 , 1 \left]\right.$. We compute the difference between $f_{n} \left(\right. x \left.\right)$ and the limit function $f \left(\right. x \left.\right)$:

$$\left|\right. f_{n} \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left|\right. = \left|\right. \frac{x}{n} - 0 \left|\right. = \frac{x}{n}$$

The maximum value of this difference on the interval $\left[\right. 0 , 1 \left]\right.$ is:

$$\underset{x \in \left[\right. 0 , 1 \left]\right.}{sup} \left|\right. f_{n} \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left|\right. = \frac{1}{n}$$

Given any $\epsilon > 0$, we can choose $N$ such that:

$$\frac{1}{N} < \epsilon$$

Therefore, for all $n \geq N$ and for all $x \in \left[\right. 0 , 1 \left]\right.$, we have:

$$\left|\right. f_{n} \left(\right. x \left.\right) - f \left(\right. x \left.\right) \left|\right. < \epsilon$$

This confirms that the sequence of functions $f_{n} \left(\right. x \left.\right) = \frac{x}{n}$ converges uniformly to the limit function $f \left(\right. x \left.\right) = 0$ on the interval $\left[\right. 0 , 1 \left]\right.$.
