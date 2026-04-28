---
layout: chapter
title: "Exponential Equations"
chapter: "Equations"
chapter_order: 7
section_order: 16
permalink: /materi-algebrica/equations/exponential-equations/
---

## Introduction

Exponential equations are [equations](https://algebrica.org/equations) in which the unknown appears in the exponent of a [power](https://algebrica.org/powers). They generally take the form:

$$a^{f \left(\right. x \left.\right)} = b^{g \left(\right. x \left.\right)}$$

or more commonly, in the simpler cases:

$$a^{x} = b$$

We assume that $a$ and $b$ are positive [real numbers](https://algebrica.org/types-of-numbers) and that $a \neq 1$. Since $a^{x} > 0$ for all $x \in \mathbb{R}$ when $a > 0$, an exponential equation is impossible if $b \leq 0$, while it has a unique solution if $b > 0$.

---

We recall the general behavior of the [exponential function](https://algebrica.org/exponential-function), for example, when $a > 1$.

![](https://algebrica.org/wp-content/uploads/resources/images/exponential-function-1.png)

In this case the graph of the function $y = a^{x}$ lies entirely above the x-axis, never touches it, always passes through the point $\left(\right. 0 , 1 \left.\right)$ on the y-axis, and increases from left to right.

The fundamental principle of $1^{x}$

The equation

$$1^{x} = 1$$

is satisfied for every real number $x$. This means that, when $a = 1$ and $b = 1$, the exponential equation has infinitely many solutions and is therefore considered undetermined. $1^{x} = 1$ is considered a fundamental principle in mathematics. This is because, regardless of the value of $x$, the expression $1^{x}$ always equals $1$.

## How to solve quadratic equations of the form $a^{f \left(\right. x \left.\right)} = b$

Equations of the form $a^{f \left(\right. x \left.\right)} = b$ can be solved by rewriting $b$ as a power of $a$. In this case, we have:

$$a^{f \left(\right. x \left.\right)} = a^{k}$$

Since the base is the same on both sides of the equation, we proceed by setting the exponents equal to each other:

$$f \left(\right. x \left.\right) = k$$

## Example 1

Let us solve, for example, the following exponential equation:

$$3^{x^{2} - 2 x} - 27 = 0$$

---

Let us rewrite the equation to bring it to the form $a^{f \left(\right. x \left.\right)} = b$. We have:

$$& 3^{x^{2} - 2 x} - 27 = 0 \\ & 3^{x^{2} - 2 x} = 27 \\ & 3^{x^{2} - 2 x} = 3^{3}$$

---

At this point, since both sides of the equation have the same base, we can equate the exponents:

$$& x^{2} - 2 x = 3 \\ & x^{2} - 2 x - 3 = 0$$

We have obtained a [quadratic equation](https://algebrica.org/quadratic-equations) that can be immediately solved by [factoring the polynomial](https://algebrica.org/factoring-ac-method/). We get:

$$\left(\right. x + 1 \left.\right) \left(\right. x - 3 \left.\right) = 0$$

The solutions that satisfy the equation are:

$$x_{1} = - 1 \text{and} x_{2} = 3$$

## When bases differ: solving with logarithms

In the example above, we considered an equation that could be reduced to an equality between powers with the same base. But what if this is not possible, when the two sides of the equation have different bases? How can we proceed in such cases? Let us consider the exponential equation:

$$3^{x^{2}} = 4$$

Since the expressions on the left and right sides of the equation cannot be rewritten with the same base, we use [logarithms](https://algebrica.org/logarithms) to rewrite them in a way that allows us to bring $x$ out of the exponent. We have:

$$log_{3} ⁡ 3^{x^{2}} = log_{3} ⁡ 4$$

By the properties of logarithms, we can rewrite the left-hand side as:

$$& x^{2} log_{3} ⁡ 3 = log_{3} ⁡ 4 \\ & x^{2} = log_{3} ⁡ 4 \\ & x = \pm \sqrt{log_{3} ⁡ 4}$$

In equations of the form $a^{f \left(\right. x \left.\right)} = b^{f \left(\right. x \left.\right)}$, if $f \left(\right. x \left.\right) \neq 0$, we can reduce the equation by expressing $b$ as a power of $a$, so that both sides share the same base. This allows us to compare the exponents directly as in example 1. Let us consider the equation:

$$3^{x + 3} = 9^{\frac{1 - x}{2}}$$

By the properties of [powers](https://algebrica.org/powers), we have:

$$& 3^{x + 3} = \left(\right. 3^{2} \left.\right)^{\frac{1 - x}{2}} \\ & 3^{x + 3} = 3^{1 - x}$$

At this point, we have rewritten both sides as powers with the same base, so we can equate the exponents:

$$& x + 3 = 1 - x \\ & 2 x = 1 - 3 \\ & x = - 1$$
