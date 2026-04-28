---
layout: chapter
title: "Factorial"
chapter: "Sets and Numbers"
chapter_order: 1
section_order: 11
permalink: /materi-algebrica/sets-and-numbers/factorial/
---

## Definition

The factorial of a non-negative [integer](https://algebrica.org/types-of-numbers/) $n$, written $n !$, is the product of all positive integers from $1$ to $n$:

$$n ! & = n \cdot \left(\right. n - 1 \left.\right) \cdot \left(\right. n - 2 \left.\right) \cdot \ldots \cdot 2 \cdot 1 \\ & = n \cdot \left(\right. n - 1 \left.\right) !$$

For example, the factorial of $4$ is computed as follows:

$$4 ! = 4 \cdot 3 \cdot 2 \cdot 1 = 24$$

By convention, the factorial of $0$ is equal to $1$. The factorial can also be expressed through a recursive [function](https://algebrica.org/functions/) defined by cases:

$$n ! = \left{\right. n \cdot \left(\right. n - 1 \left.\right) ! & \text{if} n \in \mathbb{N} , n > 0 \\ 1 & \text{if} n = 0$$

The same definition can be written more compactly using the product symbol $\prod$, where the index $k$ ranges from $1$ to $n$:

$$n ! = \left{\right. \prod_{k = 1}^{n} k & \text{if} n \in \mathbb{N} , n > 0 \\ 1 & \text{if} n = 0$$

The factorial is used to compute the [binomial coefficient](https://algebrica.org/binomial-coefficient/), which represents the number of ways to select a given number of elements from a larger set.

## Simplifying factorial ratios

Suppose we are given two non-negative integers $n$ and $k$ with $n > k$, and we want to compute the following ratio:

$$\frac{n !}{\left(\right. n - k \left.\right) !}$$

The denominator cancels the factors from $\left(\right. n - k \left.\right)$ to $1$, leaving $k$ terms in the numerator.

$$\frac{n !}{\left(\right. n - k \left.\right) !} = n \cdot \left(\right. n - 1 \left.\right) \cdot \ldots \cdot \left(\right. n - k + 1 \left.\right)$$

Consider the ratio between $7 !$ and $4 !$. The factors from $4$ down to $1$ appear in both numerator and denominator and therefore cancel. What remains in the numerator is the product of the integers from $7$ down to $5$, which is equal to $210$:

$$\frac{7 !}{4 !} = \frac{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}{4 \cdot 3 \cdot 2 \cdot 1} = 7 \cdot 6 \cdot 5 = 210$$

## Factorial in combinatorics

In combinatorics, $n !$ counts the possible permutations of $n$ objects. For example, with $n = 3$ objects there are $3 ! = 6$ possible permutations:

$$& o_{1} & o_{2} & o_{3} \\ & 1 & 2 & 3 \\ & 1 & 3 & 2 \\ & 2 & 1 & 3 \\ & 2 & 3 & 1 \\ & 3 & 1 & 2 \\ & 3 & 2 & 1$$

If the order of selection does not matter, many of these orderings become equivalent. Choosing the objects $1 , 2 , 3$ is the same as choosing $3 , 2 , 1$ or any other arrangement of the same three elements. Since each group of $k$ elements can be arranged in $k !$ different ways, dividing by $k !$ eliminates these repetitions and yields the [binomial coefficient](https://algebrica.org/binomial-coefficient/):

$$\left(\right. \frac{n}{k} \left.\right) = \frac{n !}{k ! \left(\right. n - k \left.\right) !}$$

## A useful identity involving factorial

Starting from the recursive definition $n ! = n \cdot \left(\right. n - 1 \left.\right) !$ and substituting it into the denominator of the fraction $n / n !$, the factor $n$ cancels out and we obtain the following identity, which is often useful to simplify expressions involving factorials:

$$\frac{n}{n !} = \frac{n}{n \cdot \left(\right. n - 1 \left.\right) !} = \frac{1}{\left(\right. n - 1 \left.\right) !}$$

A typical application is the derivation of the mean of the [Poisson distribution](https://algebrica.org/poisson-distribution/) or the rewriting of binomial coefficients in a simpler form.

## Relationship between the factorial and the gamma function

The gamma function can be seen as the natural extension of the factorial. Where the factorial is defined only on the [natural numbers](https://algebrica.org/natural-numbers), the gamma function is defined for every positive real value. For any $c \in \mathbb{R}^{+}$, the gamma function is defined by the following integral:

$$\Gamma \left(\right. c \left.\right) = \int_{0}^{+ \infty} x^{c - 1} e^{- x} d x$$

For integer arguments, the gamma function agrees with the factorial, as shown by the identity below:

$$\Gamma \left(\right. n \left.\right) = \left(\right. n - 1 \left.\right) !$$

So the factorial can be seen as the discrete restriction of the gamma function to the natural numbers.

> The gamma function also appears in the [Beta distribution](https://algebrica.org/beta-distribution/), where it provides the normalizing constant that makes the total probability integrate to one.

## Stirling’s approximation

Stirling’s approximation is used to estimate $n !$ for large values of $n$ when direct multiplication of all terms is not practical. It gives the following asymptotic form:

$$n ! \approx \sqrt{2 \pi n} \left(\left(\right. \frac{n}{e} \left.\right)\right)^{n}$$

This approximation is needed because the factorial grows faster than both [polynomial](https://algebrica.org/polynomial-function/) and [exponential functions](https://algebrica.org/exponential-function/). Already for relatively small values, it can exceed $10^{6}$, while $2^{n}$ is still around $10^{3}$.

| $n$ | Polynomial $n^{2}$ | Exponential $2^{n}$ | Factorial $n !$ |
| --- | --- | --- | --- |
| 2 | 4 | 4 | 2 |
| 5 | 25 | 32 | 120 |
| 10 | 100 | 1,024 | 3,628,800 |
| 15 | 225 | 32,768 | ~1.307 billion |

The ratio between $n !$ and its Stirling approximation tends to $1$ as $n$ grows without bound:

$$\underset{n \rightarrow \infty}{lim} \frac{n !}{\sqrt{2 \pi n} \left(\left(\right. \frac{n}{e} \left.\right)\right)^{n}} = 1$$

This approximation becomes increasingly accurate as $n$ grows. At $n = 10$, the exact value $10 ! = 3,628,800$ compares with Stirling’s estimate of roughly $3,598,696$, an error below $1 \%$, while for $n > 100$ the relative error drops under $0.1 \%$. Another way to express the approximation is by introducing a correction term:

$$n ! \approx \sqrt{2 \pi n} \left(\left(\right. \frac{n}{e} \left.\right)\right)^{n} \left(\right. 1 + \frac{1}{12 n} \left.\right)$$

> Stirling’s approximation is used in the asymptotic analysis of [binomial coefficients](https://algebrica.org/binomial-coefficient/). For any base $a > 1$, the factorial $n !$ always dominates the [exponential](https://algebrica.org/exponential-function/) $a^{n}$, that is, $\underset{n \rightarrow \infty}{lim} a^{n} / n ! = 0$.

growthstirling approximationintegral formgamma functioncombinationsbinomial coefficientpermutationsindex shiftidentitiescancellationratiosnotationzero caserecursiveproductextensionscombinatoricsmanipulationdefinitions
