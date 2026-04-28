---
layout: chapter
title: "Cauchy’s Theorem"
chapter: "Differential Calculus Theorems"
chapter_order: 17
section_order: 5
permalink: /materi-algebrica/differential-calculus-theorems/cauchys-theorem/
---

## Introduction

**Cauchy’s Theorem** establishes a relationship between the changes of two functions over a given interval. Specifically, if $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are [continuous](https://algebrica.org/continuous-functions/) on a closed interval $\left[\right. a , b \left]\right.$ and differentiable in its interior, with $g^{'} \left(\right. x \left.\right) \neq 0$, then there exists at least one point $c$ in $\left(\right. a , b \left.\right)$ where the ratio of their [derivatives](https://algebrica.org/derivatives) matches the ratio of their overall change across the interval:

## Statement

The Cauchy’s theorem states the following. Let $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ be two functions such that:

- $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are continuous on the interval $\left[\right. a , b \left]\right.$.
- $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are differentiable at every point in the interior of the interval.
- $g^{'} \left(\right. x \left.\right) \neq 0$ for every $x$ in the interior of $\left[\right. a , b \left]\right.$.

Then, there exists at least one point $c$ in the interior of the interval $\left[\right. a , b \left]\right.$ such that:

$$\frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{g \left(\right. b \left.\right) - g \left(\right. a \left.\right)}$$

that is, the ratio of the increments of the functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ over the interval $\left[\right. a , b \left]\right.$ is equal to the ratio of their respective derivatives evaluated at a point $c$ in the interior of the interval.

Setting $g \left(\right. x \left.\right) = x$ reduces Cauchy’s theorem directly to [Lagrange’s theorem](https://algebrica.org/lagrange-theorem/). With $g^{'} \left(\right. x \left.\right) = 1$ and $g \left(\right. b \left.\right) - g \left(\right. a \left.\right) = b - a$, the conclusion takes the form:
$$\frac{f^{'} \left(\right. c \left.\right)}{1} = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{b - a}$$
Lagrange’s theorem is therefore a special case of Cauchy’s theorem, obtained when one of the two functions is the identity.

##### Cauchy’s theorem provides the theoretical basis for the proof of [L’Hôpital’s Rule](https://algebrica.org/hopital-rule/).

## Proof of Cauchy’s theorem

To prove the theorem, define a new function $\varphi \left(\right. x \left.\right)$ where $\lambda$ is a constant to be determined.:

$$\varphi \left(\right. x \left.\right) = f \left(\right. x \left.\right) - \lambda g \left(\right. x \left.\right)$$

We want to choose $\lambda$ such that $\varphi \left(\right. a \left.\right) = \varphi \left(\right. b \left.\right)$. From this condition, we obtain:

$$\lambda = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{g \left(\right. b \left.\right) - g \left(\right. a \left.\right)}$$

---

Now the function $\varphi \left(\right. x \left.\right)$ is continuous on $\left[\right. a , b \left]\right.$ and differentiable on $\left(\right. a , b \left.\right)$, with $\varphi \left(\right. a \left.\right) = \varphi \left(\right. b \left.\right)$. We can apply the [Rolle’s Theorem](https://algebrica.org/rolles-theorem), which guarantees that there exists at least one point $c \in \left(\right. a , b \left.\right)$ such that $\varphi^{'} \left(\right. c \left.\right) = 0$. By calculating the derivative of $\varphi \left(\right. x \left.\right)$ and setting $\varphi^{'} \left(\right. c \left.\right) = 0$, we obtain:

$$\varphi^{'} \left(\right. x \left.\right) = f^{'} \left(\right. x \left.\right) - \lambda g^{'} \left(\right. x \left.\right)$$
$$f^{'} \left(\right. c \left.\right) = \lambda g^{'} \left(\right. c \left.\right)$$

---

Substituting the value of $\lambda$, we get:

$$f^{'} \left(\right. c \left.\right) = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{g \left(\right. b \left.\right) - g \left(\right. a \left.\right)} g^{'} \left(\right. c \left.\right)$$

By dividing both sides by $g^{'} \left(\right. c \left.\right)$, we obtain:

$$\frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{g \left(\right. b \left.\right) - g \left(\right. a \left.\right)}$$

Thus, we have proven the conclusion of the theorem.

## Example 1

Let’s verify, for example, that the theorem is applicable to the functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ in the interval [1,3]:

$$f \left(\right. x \left.\right) = 2 x^{2} - 4 x + 2$$
$$g \left(\right. x \left.\right) = x^{2}$$

The two functions are [polynomials](https://algebrica.org/polynomials), therefore they are continuous and differentiable for every $x \in \mathbb{R}$. Moreover, $g^{'} \left(\right. x \left.\right) = 2 x \neq 0$. This satisfies the hypotheses of the theorem.

---

Let’s now verify the existence of a point $c \in \left(\right. 1 , 3 \left.\right)$ such that:

$$\frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \frac{f \left(\right. 3 \left.\right) - f \left(\right. 1 \left.\right)}{g \left(\right. 3 \left.\right) - g \left(\right. 1 \left.\right)}$$

We obtain:

$$\frac{f \left(\right. 3 \left.\right) - f \left(\right. 1 \left.\right)}{g \left(\right. 3 \left.\right) - g \left(\right. 1 \left.\right)} = \frac{18 - 12 + 2 - 2 + 4 - 2}{9 - 1} = \frac{8}{8} = 1$$

---

Now let’s calculate:

$$\frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \frac{4 c - 4}{2 c}$$

From $1$, the equality becomes:

$$\frac{4 c - 4}{2 c} & = 1 \\ \frac{4 c - 4}{2 c} & = \frac{2 c}{2 c} \\ 4 c - 4 & = 2 c \\ 2 c & = 4 \\ c & = 2$$

Since $c = 2 \in \left[\right. 1 , 3 \left]\right.$, the theorem is verified.

## A note on the hypothesis $g^{'} \left(\right. x \left.\right) \neq 0$

Consider the particular case in which $g \left(\right. b \left.\right) = g \left(\right. a \left.\right)$. In this situation, the denominator of the following ratio is zero, and the expression is undefined:
$$\frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{g \left(\right. b \left.\right) - g \left(\right. a \left.\right)}$$
For this reason, the constant cannot be introduced:
$$\lambda = \frac{f \left(\right. b \left.\right) - f \left(\right. a \left.\right)}{g \left(\right. b \left.\right) - g \left(\right. a \left.\right)}$$
As a result, the proof utilising the following auxiliary function is no longer valid:
$$\varphi \left(\right. x \left.\right) = f \left(\right. x \left.\right) - \lambda g \left(\right. x \left.\right)$$
Under the hypotheses of Cauchy’s theorem, this situation does not arise. The condition $g^{'} \left(\right. x \left.\right) \neq 0$ within the interior of the interval ensures that g is strictly monotonic, which in turn guarantees that $g \left(\right. b \left.\right) \neq g \left(\right. a \left.\right)$. Therefore, the case $g \left(\right. b \left.\right) = g \left(\right. a \left.\right)$ is precluded by the theorem’s assumptions.

## Selected references

- **University of Florida J. Keesling**. [The Cauchy Mean Value Theorem](https://people.clas.ufl.edu/kees/files/CauchyMeanValue.pdf)
- **University of Maryland**. [The Cauchy Mean Value Theorem and Consequences](https://math.umd.edu/~immortal/MATH410/lecturenotes/ch4-4.pdf)
- **UC Berkeley A. Vizeff**. [Mean Value Theorem and L’Hôpital’s Rule](https://math.berkeley.edu/~avizeff/calculus-I-F23/lecture-16.pdf)
