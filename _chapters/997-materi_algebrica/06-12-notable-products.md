---
layout: chapter
title: "Notable Products"
chapter: "Polynomials"
chapter_order: 6
section_order: 12
permalink: /materi-algebrica/polynomials/notable-products/
---

## Introduction

Notable products are identities describing the expansion or [factorisation](https://algebrica.org/factoring-ac-method/) of [polynomials](https://algebrica.org/polynomials) such as [binomials](https://algebrica.org/binomials) or [trinomials](https://algebrica.org/trinomials). They allow rewriting such expressions in a simpler form, and this is often what makes polynomial factorisation tractable in practice or what allows us to actually solve an [equation](https://algebrica.org/equations/).

Consider for example the identity $\left(\right. a + b \left.\right)^{2} = a^{2} + 2 a b + b^{2}$. A useful property is that, read from left to right, it gives us the expansion of the square, while read from right to left it gives us its factorisation.

Most of the identities collected here are special cases of the [binomial theorem](https://algebrica.org/binomial-theorem/), which gives the expansion of $\left(\right. a + b \left.\right)^{n}$ for arbitrary non-negative integer $n$. The square and the cube of a binomial are just the cases $n = 2$ and $n = 3$ of this general expansion. Other identities on this page, like the difference of two squares or the factorisation of $a^{3} \pm b^{3}$, cannot be obtained from the binomial theorem, although the underlying mechanism is essentially the same.

## Square of a binomial

The square of a binomial is what we obtain when a binomial is multiplied by itself. There are two cases, depending on whether the two terms are added or subtracted:

$$\left(\right. a + b \left.\right)^{2} & = a^{2} + 2 a b + b^{2} \\ \left(\right. a - b \left.\right)^{2} & = a^{2} - 2 a b + b^{2}$$

Working out the expansion of $\left(\right. a + b \left.\right)^{2}$, we obtain three terms:

$$\left(\right. a + b \left.\right)^{2} & = \left(\right. a + b \left.\right) \left(\right. a + b \left.\right) \\ & = a^{2} + a b + a b + b^{2} \\ & = a^{2} + 2 a b + b^{2}$$

Two of them are the squares of $a$ and $b$, and the third one is twice their product. The case $\left(\right. a - b \left.\right)^{2}$ is analogous, with the only difference that the middle term comes out negative, since multiplying $a$ by $- b$ introduces a minus sign.

## Difference of two squares

When we multiply a sum and a difference of the same two terms, the result is the difference of their squares:

$$a^{2} - b^{2} = \left(\right. a + b \left.\right) \left(\right. a - b \left.\right)$$

The product on the right-hand side expands as follows:

$$\left(\right. a + b \left.\right) \left(\right. a - b \left.\right) & = a \left(\right. a - b \left.\right) + b \left(\right. a - b \left.\right) \\ & = a^{2} - a b + a b - b^{2} \\ & = a^{2} - b^{2}$$

The terms $- a b$ and $+ a b$ cancel out, so what is left is just $a^{2} - b^{2}$.

## Cube of a binomial

When we multiply a binomial by itself three times, the result is one of the following two identities, depending on the sign between the two terms:

$$\left(\right. a + b \left.\right)^{3} & = a^{3} + 3 a^{2} b + 3 a b^{2} + b^{3} \\ \left(\right. a - b \left.\right)^{3} & = a^{3} - 3 a^{2} b + 3 a b^{2} - b^{3}$$

Both are special cases of the [binomial theorem](https://algebrica.org/binomial-theorem/) with $n = 3$.

---

Closely related to the cube of a binomial are the sum and difference of two cubes, which work the other way around: they take an expression of the form $a^{3} \pm b^{3}$ and rewrite it as a product.

$$a^{3} + b^{3} & = \left(\right. a + b \left.\right) \left(\right. a^{2} - a b + b^{2} \left.\right) \\ a^{3} - b^{3} & = \left(\right. a - b \left.\right) \left(\right. a^{2} + a b + b^{2} \left.\right)$$

The first identity can be verified by expanding the right-hand side:

$$\left(\right. a + b \left.\right) \left(\right. a^{2} - a b + b^{2} \left.\right) & = a^{3} - a^{2} b + a b^{2} + a^{2} b - a b^{2} + b^{3} \\ & = a^{3} + b^{3}$$

The same procedure works for $a^{3} - b^{3}$:

$$\left(\right. a - b \left.\right) \left(\right. a^{2} + a b + b^{2} \left.\right) & = a^{3} + a^{2} b + a b^{2} - a^{2} b - a b^{2} - b^{3} \\ & = a^{3} - b^{3}$$

In both cases the mixed terms cancel in pairs, and only the cubes $a^{3}$ and $\pm b^{3}$ survive.

> In the expansion of $\left(\right. a + b + c \left.\right)^{3}$, the coefficient $6$ in the term $6 a b c$ arises from the number of permutations of the three distinct factors $a$, $b$, $c$, that is $3 ! = 6$. This is an instance of the multinomial theorem, which generalises the [binomial theorem](https://algebrica.org/binomial-theorem/) to sums of more than two terms.

## Notable products and the binomial theorem

The square and the cube of a binomial both come from a more general formula, the [binomial theorem](https://algebrica.org/binomial-theorem/), which expands $\left(\right. a + b \left.\right)^{n}$ for any non-negative integer $n$:

$$\left(\right. a + b \left.\right)^{n} = \sum_{k = 0}^{n} \left(\right. \frac{n}{k} \left.\right) a^{n - k} b^{k}$$

The coefficients $\left(\right. \frac{n}{k} \left.\right)$ are the [binomial coefficients](https://algebrica.org/binomial-coefficient/):

$$\left(\right. \frac{n}{k} \left.\right) = \frac{n !}{k ! \left(\right. n - k \left.\right) !}$$

If we now want to use this general formula to recover the cube of a binomial, we just need to set $n = 3$ and work out the four coefficients, which turn out to be $\left(\right. \frac{3}{0} \left.\right) = \left(\right. \frac{3}{3} \left.\right) = 1$ and $\left(\right. \frac{3}{1} \left.\right) = \left(\right. \frac{3}{2} \left.\right) = 3$. Substituting these numbers back into the formula, the expansion comes out as:

$$\left(\right. a + b \left.\right)^{3} = a^{3} + 3 a^{2} b + 3 a b^{2} + b^{3}$$

## Example 1

Consider the following equation:

$$x^{3} - 27 = 0$$

Since $27 = 3^{3}$, the left-hand side is a difference of two cubes. Applying the identity $a^{3} - b^{3} = \left(\right. a - b \left.\right) \left(\right. a^{2} + a b + b^{2} \left.\right)$ with $a = x$ and $b = 3$, we factorise:

$$\left(\right. x - 3 \left.\right) \left(\right. x^{2} + 3 x + 9 \left.\right) = 0$$

The equation holds when either factor equals zero:

$$\left{\right. x - 3 = 0 \\ x^{2} + 3 x + 9 = 0$$

The first case yields $x = 3$ directly. For the second case, the [quadratic formula](https://algebrica.org/quadratic-formula/) is applied:

$$x & = \frac{- 3 \pm \sqrt{3^{2} - 4 \left(\right. 1 \left.\right) \left(\right. 9 \left.\right)}}{2 \left(\right. 1 \left.\right)} \\ & = \frac{- 3 \pm \sqrt{9 - 36}}{2} \\ & = \frac{- 3 \pm \sqrt{- 27}}{2}$$

Because the discriminant $\Delta = - 27 < 0$, the two remaining solutions are [complex](https://algebrica.org/quadratic-equations-with-complex-solutions/). Substituting $\sqrt{- 27} = 3 i \sqrt{3}$ gives:

$$x = \frac{- 3 + 3 i \sqrt{3}}{2} x = \frac{- 3 - 3 i \sqrt{3}}{2}$$

Therefore, by applying the expansion of the difference of two cubes, we were able to easily determine the solutions of the third-degree equation, which are:

$$x = 3 , x = \frac{- 3 + 3 i \sqrt{3}}{2} , x = \frac{- 3 - 3 i \sqrt{3}}{2}$$

## Sum and difference of nth powers

The identities seen so far cover only the cases $n = 2$ and $n = 3$. For a generic $n$, the parity of the exponent decides whether $a^{n} + b^{n}$ and $a^{n} - b^{n}$ admit a factorisation.

The difference $a^{n} - b^{n}$ factorises for any positive integer $n$, with no parity restrictions, as:

$$a^{n} - b^{n} = \left(\right. a - b \left.\right) \left(\right. a^{n - 1} + a^{n - 2} b + a^{n - 3} b^{2} + \hdots + a b^{n - 2} + b^{n - 1} \left.\right)$$

For the sum $a^{n} + b^{n}$ when $n$ is odd, an analogous factorisation does exist, with alternating signs in the second factor:

$$a^{n} + b^{n} = \left(\right. a + b \left.\right) \left(\right. a^{n - 1} - a^{n - 2} b + a^{n - 3} b^{2} - \hdots - a b^{n - 2} + b^{n - 1} \left.\right)$$

When $n$ is even, on the other hand, no such factorisation is available over $\mathbb{R}$ in general. The expressions $a^{2} + b^{2}$ and $a^{4} + b^{4}$, for instance, are irreducible over the reals unless further structure is brought in.

> The factorisation of $a^{n} - b^{n}$ is closely related to the structure of the $n$-th roots of unity in the [complex plane](https://algebrica.org/complex-numbers-introduction/). The [roots](https://algebrica.org/roots-of-a-polynomial/) of $a^{n} - b^{n} = 0$ are precisely $a / b = e^{2 \pi i k / n}$ for $k = 0 , 1 , \ldots , n - 1$.

---

The case of even $n$ admits one exception, known as Sophie Germain’s identity, which has some consequences in showing that certain integers of the form $n^{4} + 4 m^{4}$ admit a non-trivial factorisation and are therefore not prime. The identity is:

$$a^{4} + 4 b^{4} = \left(\right. a^{2} + 2 b^{2} + 2 a b \left.\right) \left(\right. a^{2} + 2 b^{2} - 2 a b \left.\right)$$

At first sight this might seem like a contradiction, since we have just said that sums of even powers do not generally factorise over $\mathbb{R}$. In this case the coefficient $4$ makes it possible to complete the square and obtain:

$$a^{4} + 4 b^{4} = \left(\right. a^{2} + 2 b^{2} \left.\right)^{2} - \left(\right. 2 a b \left.\right)^{2}$$

In this way the expression is a difference of two squares, and the factorisation follows from the standard identity.

> The identities for $a^{n} \pm b^{n}$ are related to Newton’s identities, which express power sums $p_{k} = a^{k} + b^{k}$ in terms of the elementary symmetric polynomials $e_{1} = a + b$ and $e_{2} = a b$.

## Example 2

Let’s consider the following expression:

$$a^{4} + b^{4}$$

Since $n = 4$ is even, $a^{4} + b^{4}$ does not factorise over $\mathbb{R}$ using the sum of nth powers formula, which applies only for odd $n$. However, it admits the following factorisation:

$$a^{4} + b^{4} = \left(\right. a^{2} + \sqrt{2} a b + b^{2} \left.\right) \left(\right. a^{2} - \sqrt{2} a b + b^{2} \left.\right)$$

The factorisation can be verified by expanding the right-hand side:

$$\left(\right. a^{2} + \sqrt{2} a b + b^{2} \left.\right) \left(\right. a^{2} - \sqrt{2} a b + b^{2} \left.\right) & = \left(\right. a^{2} + b^{2} \left.\right)^{2} - \left(\right. \sqrt{2} a b \left.\right)^{2} \\ & = a^{4} + 2 a^{2} b^{2} + b^{4} - 2 a^{2} b^{2} \\ & = a^{4} + b^{4}$$

## List of the main notable products

|  |  |
| --- | --- |
| $$\left(\right. a + b \left.\right)^{2}$$ | $$a^{2} + 2 a b + b^{2}$$ |
| $$\left(\right. a - b \left.\right)^{2}$$ | $$a^{2} - 2 a b + b^{2}$$ |
| $$a^{2} - b^{2}$$ | $$\left(\right. a + b \left.\right) \left(\right. a - b \left.\right)$$ |
| $$\left(\right. a + b \left.\right)^{3}$$ | $$a^{3} + 3 a^{2} b + 3 a b^{2} + b^{3}$$ |
| $$\left(\right. a - b \left.\right)^{3}$$ | $$a^{3} - 3 a^{2} b + 3 a b^{2} - b^{3}$$ |
| $$a^{3} + b^{3}$$ | $$\left(\right. a + b \left.\right) \left(\right. a^{2} - a b + b^{2} \left.\right)$$ |
| $$a^{3} - b^{3}$$ | $$\left(\right. a - b \left.\right) \left(\right. a^{2} + a b + b^{2} \left.\right)$$ |
| $$a^{n} + b^{n} \left(\right. n \text{odd} \left.\right)$$ | $$\left(\right. a + b \left.\right) \left(\right. a^{n - 1} - a^{n - 2} b + \hdots + b^{n - 1} \left.\right)$$ |
| $$a^{n} - b^{n}$$ | $$\left(\right. a - b \left.\right) \left(\right. a^{n - 1} + a^{n - 2} b + \hdots + b^{n - 1} \left.\right)$$ |
| $$a^{2 n} - b^{2 n}$$ | $$\left(\right. a^{n} - b^{n} \left.\right) \left(\right. a^{n} + b^{n} \left.\right)$$ |
| $$a^{4} - b^{4}$$ | $$\left(\right. a - b \left.\right) \left(\right. a + b \left.\right) \left(\right. a^{2} + b^{2} \left.\right)$$ |
| $$a^{4} + b^{4}$$ | $$\left(\right. a^{2} + \sqrt{2} a b + b^{2} \left.\right) \left(\right. a^{2} - \sqrt{2} a b + b^{2} \left.\right)$$ |
| $$\left(\right. a + b + c \left.\right)^{2}$$ | $$a^{2} + b^{2} + c^{2} + 2 \left(\right. a b + a c + b c \left.\right)$$ |
| $$\left(\right. a + b + c \left.\right)^{3}$$ | $$a^{3} + b^{3} + c^{3} + 3 \left(\right. a^{2} b + a^{2} c + b^{2} a + b^{2} c + c^{2} a + c^{2} b \left.\right) + 6 a b c$$ |

algebraic patternsdifference of powerssum of powersnth powersmultinomial structurebinomial theoremcommon factorspattern recognitionquadratic reductionequation solvingsimplificationfactorizationexpansionpower identitiesdifference cubessum cubescube binomialdifference squaressquare binomialpropertiesoperationsidentities
