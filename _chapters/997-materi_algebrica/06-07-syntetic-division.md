---
layout: chapter
title: "The Synthetic Division Method"
chapter: "Polynomials"
chapter_order: 6
section_order: 7
permalink: /materi-algebrica/polynomials/the-synthetic-division-method/
---

## Introduction

The synthetic division (or Ruffini’s rule) is a method for dividing a polynomial by a binomial of the form $\left(\right. x - a \left.\right)$. It is widely used to factorize [polynomials](https://algebrica.org/polynomials) and to simplify the resolution of [equations](https://algebrica.org/equations) of degree higher than two, especially when these cannot be reduced to [quadratic equations](https://algebrica.org/quadratic-equations), [monomials](https://algebrica.org/monomials), or standard [trinomials](https://algebrica.org/trinomials). When $a$ is a [root](https://algebrica.org/roots-of-a-polynomial/) of a polynomial $P \left(\right. x \left.\right)$ of degree $n$ and the [binomial](https://algebrica.org/binomials/) $\left(\right. x - r \left.\right)$ is a factor of $P \left(\right. x \left.\right)$ we can write:

$$P \left(\right. x \left.\right) = \left(\right. x - r \left.\right) Q \left(\right. x \left.\right)$$

where $Q \left(\right. x \left.\right)$ is a polynomial of degree $n - 1$.

---

This method offers a compact and efficient procedure for performing the division, avoiding the full algebraic long division while still producing the quotient $Q \left(\right. x \left.\right)$ needed for further analysis or factorization.

- The method provides a fast and structured way to divide by $\left(\right. x - r \left.\right)$, making the factorization of a polynomial almost immediate once a root has been identified.
- By lowering the degree of the polynomial at each step, the synthetic process streamlines the resolution of higher-degree equations and naturally exposes additional roots or factors.

Although this method is often used in conjunction with the Rational Root Theorem, it is not the only available technique. Depending on the structure of the expression, other approaches—such as [special products](https://algebrica.org/notable-products) or alternative [factoring methods](https://algebrica.org/factoring-ac-method/)—may offer a simpler or more direct path to factorization.

## Rational root theorem

Consider a polynomial of the form:

$$a_{n} x^{n} + a_{n - 1} x^{n - 1} + \hdots + a_{1} x + a_{0}$$

where $a_{n} , a_{n - 1} , \ldots , a_{0} \in \mathbb{Z}$. If the polynomial admits rational roots, each of them must be expressible as:

$$r = \frac{p}{q}$$

where $p$ is a divisor of the constant term $a_{0}$ and $q$ is a divisor of the leading coefficient $a_{n}$. This result, known as the rational root theorem, allows us to restrict the search for rational solutions to a finite list of candidates determined solely by the factors of $a_{0}$ and $a_{n}$.

##### The theorem provides the candidates, and Ruffini’s rule is then used to test each one and to perform the polynomial division whenever a valid root is found.

## Example 1

Let us examine a concrete example. Consider the polynomial

$$P \left(\right. x \left.\right) = x^{3} - 6 x^{2} + 11 x - 6$$

We want to identify its rational roots using the Rational Root Theorem.
 According to the theorem, any rational root must have the form

$$r = \frac{p}{q}$$

where $p$ divides the constant term $a_{0} = - 6$ and $q$ divides the leading coefficient $a_{3} = 1$.
 Since the only divisors of 1 are $\pm 1$, the set of possible rational roots is

$$r \in , \pm 1 , \pm 2 , \pm 3 , \pm 6 ,$$

To determine which of these candidates is an actual root, we evaluate $P \left(\right. x \left.\right)$ at each value.
 Testing $x = 1$:

$$P \left(\right. 1 \left.\right) & = 1^{3} - 6 \cdot 1^{2} + 11 \cdot 1 - 6 \\ & = 1 - 6 + 11 - 6 \\ & = 0$$

Since $P \left(\right. 1 \left.\right) = 0$, we conclude that $x = 1$ is a root of the polynomial.

---

Now that we have found a root, we need to construct the following table. In the first row, we insert the coefficients of the initial polynomial $P \left(\right. x \left.\right)$ sorted by degree (if a coefficient of a certain degree $k$ is missing, remember to insert $0$ in its place). In the second row, instead, we insert the value of the root we just found, which is $1$. We have:

$$& 1 & - 6 & 11 & - 6 \\ 1 & \\ & & & &$$

---

We put at the first position of the third row the value of the leading coefficient (third degree in this case): $$& 1 & - 6 & 11 & - 6 \\ 1 & \\ & 1 & & &$$

---

Now let’s multiply the element marked with $\overset{a}{1}$ by the element marked with $\overset{b}{1}$ to obtain the element marked with $\overset{c}{1}$: $$& 1 & - 6 & 11 & - 6 \\ \overset{a}{1} & & \overset{c}{1} \\ & \overset{b}{1} & & &$$

---

Sum the element marked with $\overset{a}{- 6}$ with the element marked with $\overset{b}{1}$ to obtain the element marked with $\overset{c}{- 5}$: $$& 1 & \overset{a}{- 6} & 11 & - 6 \\ 1 & & \overset{b}{1} \\ & 1 & \overset{c}{- 5} & &$$

---

Iterate the process and multiply the element marked with $\overset{a}{1}$ by the element marked with $\overset{b}{- 5}$ to obtain the element marked with $\overset{c}{- 5}$ :$$& 1 & - 6 & 11 & - 6 \\ \overset{a}{1} & & 1 & \overset{c}{- 5} \\ & 1 & \overset{b}{- 5} & &$$

---

Sum the element marked with $\overset{a}{11}$ with the element marked with $\overset{b}{- 5}$ to obtain the element marked with $\overset{c}{- 6}$: $$& 1 & - 6 & \overset{a}{11} & - 6 \\ 1 & & 1 & \overset{b}{- 5} \\ & 1 & - 5 & \overset{c}{- 6} &$$

---

Multiply the element marked with $\overset{a}{1}$ by the element marked with $\overset{b}{6}$ to obtain the element marked with $\overset{c}{6}$: $$& 1 & - 6 & 11 & - 6 \\ \overset{a}{1} & & 1 & - 5 & \overset{c}{6} \\ & 1 & - 5 & \overset{b}{6} &$$

---

Sum the element marked with $\overset{a}{- 6}$ with the element marked with $\overset{b}{6}$ to obtain the element marked with $\overset{c}{0}$: $$& 1 & - 6 & 11 & \overset{a}{- 6} \\ 1 & & 1 & - 5 & \overset{b}{6} \\ & 1 & - 5 & 6 & \overset{c}{0}$$

---

When we reach the end of the table and find that the remainder is zero, then we have found a root $r$ of the polynomial such that we can factorize it as follows:

$$P \left(\right. x \left.\right) = \left(\right. x - r \left.\right) \cdot Q \left(\right. x \left.\right)$$

$r = 1$ is the root we found at the beginning. $Q \left(\right. x \left.\right)$ is a polynomial of degree $n - 1$, with coefficients arranged by degree in the order they appear in the third row. In our example we have: $$P \left(\right. x \left.\right) = \left(\right. x - 1 \left.\right) \left(\right. x^{2} - 5 x + 6 \left.\right)$$

We can now factor the quadratic term. The numbers that multiply to $6$ and sum to $- 5$ are $- 2$ and $- 3$. Therefore,

$$x^{2} - 5 x + 6 = \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)$$

and the complete factorization of the original polynomial is

$$P \left(\right. x \left.\right) = \left(\right. x - 1 \left.\right) \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)$$

##### Remember that if the remainder is not zero, then the value you tested is not a root. In that case, try another candidate from the list of possible rational roots.

The polynomial can therefore be fully factorized as

$$P \left(\right. x \left.\right) = \left(\right. x - 1 \left.\right) \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)$$

which makes its roots immediately identifiable as $1$, $2$, and $3$.

## Limitations

Despite its practicality and ease of use, Ruffini’s rule has some limitations. The standard version of Ruffini’s rule is formulated for polynomials with real coefficients and real linear divisors. For divisors like $x - \left(\right. a + b i \left.\right)$, where $i$ is the [imaginary unit](https://algebrica.org/complex-numbers-introduction/), Ruffini’s rule cannot be applied directly.

If the polynomial has complex roots, Ruffini’s rule cannot identify or utilize them in the division.

---

The rule is primarily useful as a partial method for calculating the quotient and remainder when dividing polynomials. However, when working with higher-degree polynomials, the complete factorization requires the iterative application of the rule, provided that all real roots have already been identified.

For polynomials of very high degree, repeatedly using Ruffini’s rule can be impractical if an efficient method for identifying the roots is not already available.

## A practical case where Ruffini’s rule cannot be applied

Let’s consider the following polynomial:

$$P \left(\right. x \left.\right) = x^{3} - 3 x^{2} + 4 x - 4$$

We want to divide this polynomial by the divisor:

$$D \left(\right. x \left.\right) = x - \left(\right. 1 + i \left.\right)$$

Ruffini’s rule is specifically designed for dividing a polynomial $P \left(\right. x \left.\right)$ by a binomial of the form $x - r$ where $r \in \mathbb{R}$. However, in this case, the divisor is of the form $x - \left(\right. 1 + i \left.\right)$, where $1 + i$ is a [complex number](https://algebrica.org/complex-numbers-introduction/). The rule provides no mechanism for handling complex coefficients during the division process.

## Computational insight

To better appreciate the usefulness of Ruffini’s rule, it helps to look at how demanding different polynomial techniques are from a computational point of view:

- Ruffini’s rule works in linear time $O \left(\right. n \left.\right)$. It relies on a simple chain of additions and multiplications on the coefficients, which makes the division by $\left(\right. x - r \left.\right)$ remarkably quick and lightweight.
- Polynomial long division is more costly, requiring about $O \left(\right. n^{2} \left.\right)$ operations. At each step it multiplies and subtracts polynomials of decreasing degree, and this repeated structure leads to a quadratic growth in the computational effort.
- Polynomial factorization is a much harder task. For general polynomials with [integer](https://algebrica.org/integers/) coefficients, no polynomial-time algorithm is currently known. Factoring may require combining several techniques, testing candidate roots, or applying more advanced algebraic methods.

##### Here $O \left(\right. n \left.\right)$ is expressed in [Big-O notation](https://algebrica.org/big-o-notation/), a standard way to describe how the number of operations grows with the size of the input. In this case it means that the computational cost increases proportionally to the degree of the polynomial.
