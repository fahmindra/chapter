---
layout: chapter
title: "Binomial Equations"
chapter: "Equations"
chapter_order: 7
section_order: 11
permalink: /materi-algebrica/equations/binomial-equations/
---

## What are binomial equations

Binomial equations are a specific type of algebraic [equations](https://algebrica.org/equations) that involve only two terms, typically expressed in the form:

$$a x^{n} + b = 0$$

- $a$ and $b$ are constants.
- $x$ is a variable raised to a power of $n$, where $n$ is a positive [integer](https://algebrica.org/integers/).

##### Different strategies exist to solve these equations based on the value of $n$. When $n$ is an odd integer, the equation typically has a unique real solution. If $n$ is even, the presence of real solutions depends on the sign of the right-hand side: for example, the equation has no real solutions if it requires taking an even root of a negative number. In more advanced contexts, solutions may also include complex numbers, especially when working with negative or non-real results.

## Equations with a degree less than two

If the value of $n$ equals $1$, the given equation reduces to a simple [linear equation](https://algebrica.org/linear-equations) in the form of $a x + b = 0$ that can be solved by isolating the variable $x$ and finding its corresponding value.

$$a x + b = 0 \rightarrow x = \frac{- b}{a}$$

If the value of $n$ equals $2$, the given equation reduces to a [quadratic equation](https://algebrica.org/quadratic-equations) in the form of $a x^{2} + b = 0$ that can be solved using the [quadratic formula](https://algebrica.org/quadratic-formula) or in a more straightforward calculating the square root of the term $\frac{- b}{a}$:

$$x = \pm \sqrt{\frac{- b}{a}}$$

##### This formula yields real solutions only when $- \frac{b}{a} \geq 0$. Otherwise, the equation has [complex solutions](https://algebrica.org/quadratic-equations-with-complex-solutions/).

## Equations with a degree greater the than two

If $n$ is greater than 2, we are dealing with a relatively simple case of an equation with a degree higher than two. Generally, such [equations](https://algebrica.org/equations) can be solved by calculating the nth root of the value $\frac{- b}{a}$ while considering two two distinct cases, depending on whether $n$ os even or $n$ odd:

When $n$ is even and $\frac{- b}{a}$ is positive, we have two distinct solutions, or a single solution if $\frac{- b}{a}$ equals $0$ in the form:

$$x = \pm \sqrt[n]{\frac{- b}{a}}$$

When $n$ is even and $\frac{- b}{a}$ is negative, the equation has no solutions in the [real number](https://algebrica.org/types-of-numbers) field.

---

When $n$ is odd, there is always a single solution in the form:

$$x = \sqrt[n]{\frac{- b}{a}}$$

In fact, the nth [root](https://algebrica.org/roots) of a negative number is feasible only when the root’s index is odd. This arithmetic operation is mathematically valid and can be executed using the same methodology as real positive numbers. The result of extracting the nth root of a negative number is also negative, except when the index is an even number. In such cases, there is no real solution.

## Example 1

Solve the binomial equation $x^{3} - 27 = 0$.

We have:

$$x^{3} & = 27 \\ x & = \sqrt[3]{27} x & = 3$$

##### In this case, $n$ is odd, and the number under the root is positive, so the equation admits a single real solution.

The solution to the equation is:
$$x = 3$$

## Example 2

Solve the binomial equation $x^{3} + 8 = 0$.

We have:

$$x^{3} & = - 8 \\ x & = \sqrt[3]{- 8}$$

In this case, $n$ is odd, and the number under the root is negative, so the equation admits a single real solution.

The solution to the equation is:
$$x = - 2$$

## Example 3

Solve the binomial equation $x^{4} + 5 = 0$.

We have:

$$x^{4} & = - 5 \\ x & = \sqrt[4]{- 5}$$

In this case, $n$ is even, and the number under the root is negative, so the equation does not admit real solutions.

The solution to the equation is:
$$∄ x \in \mathbb{R}$$

##### Indeed, the examples presented are merely generic illustrations of easily solvable equations. In practice, it is possible to encounter instances where complex [polynomial equations](https://algebrica.org/polynomial-equations/) may be reduced to binomial equations, which, as demonstrated, can be resolved using straightforward methods
