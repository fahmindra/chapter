---
layout: chapter
title: "Monomials"
chapter: "Polynomials"
chapter_order: 6
section_order: 2
permalink: /materi-algebrica/polynomials/monomials/
---

## Definition

A monomial is an algebraic expression consisting of a single term. It is written as the product of a numerical coefficient and one or more variables, each raised to a non-negative [integer](https://algebrica.org/integers/) exponent. The general form of a monomial is:

$$a \cdot x_{1}^{n_{1}} \cdot x_{2}^{n_{2}} \cdot \hdots \cdot x_{k}^{n_{k}}$$

- $a \in \mathbb{R}$ is the numerical coefficient.
- $x_{1} , x_{2} , \ldots , x_{k}$ are the variables.
- $n_{1} , n_{2} , \ldots , n_{k} \in \mathbb{N}_{0}$ are the exponents.

The zero monomial is the special case where $a = 0$. It is considered a monomial but its degree is left undefined.

---

Examples of monomials include:

- $4$: a non-zero real constant (coefficient only, no variables).
- $- 2 x$: coefficient $- 2$ and variable $x$ with exponent $1$.
- $3 x^{2} y$: coefficient $3$, variable $x$ with exponent $2$, variable $y$ with exponent $1$.
- $0$: the zero monomial.

A monomial in $k$ variables can be viewed as an element of the polynomial ring $\mathbb{R} \left[\right. x_{1} , \ldots , x_{k} \left]\right.$, where it corresponds to a single term of the form $a \cdot x_{1}^{n_{1}} \hdots x_{k}^{n_{k}}$.

> A [ring](https://algebrica.org/rings/) is an algebraic structure with two operations, addition and multiplication, that satisfy associativity, distributivity, and the existence of an additive identity and additive inverses.

---

A [polynomial](https://algebrica.org/polynomials/) is called homogeneous if all its terms have the same total degree. Since a monomial consists of a single term, every monomial is homogeneous by definition. The monomials of degree $d$ in $k$ variables form a basis for the $\mathbb{R}$ [vector](https://algebrica.org/vectors/) space of homogeneous polynomials of degree $d$. For example, $x^{2} , x y , y^{2}$ form a basis for the space of homogeneous polynomials of degree $2$ in two variables.

## Why exponents in a monomial must be non-negative integers

The constraint that exponents be non-negative integers follows directly from the definition of a [polynomial](https://algebrica.org/polynomials): each variable must appear with an exponent in $\mathbb{N}_{0}$. This ensures that a monomial represents a finite product of variables, with no divisions or radicals involved. The following expressions are not monomials:

$$3 x^{- 1} 5 x^{1 / 2} \frac{4}{x}$$

In the first case, $x^{- 1} = 1 / x$, a negative exponent introduces a division.
In the second, $x^{1 / 2} = \sqrt{x}$, a fractional exponent introduces a radical.
The third case, $4 / x = 4 x^{- 1}$, is simply a negative exponent in disguise.

## Degree of a monomial

The degree of a monomial is the sum of the exponents of all its variables. For the monomial $a b^{2} c^{3}$, the exponents are $1$, $2$, and $3$, so its degree is:

$$1 + 2 + 3 = 6$$

The degree of a non-zero constant is $0$, since no variables are present. The zero monomial has no defined degree.

---

The partial degree of a monomial with respect to a given variable is the exponent of that variable. For the monomial $3 x^{2} y^{3}$, the partial degree in $x$ is $2$ and the partial degree in $y$ is $3$. The total degree is the sum of all partial degrees:

$$2 + 3 = 5$$

---

The total number of monomials of degree $d$ in $k$ variables can be determined using the following [binomial coefficient](https://algebrica.org/binomial-coefficient/):

$$\left(\right. \frac{d + k - 1}{k - 1} \left.\right)$$

For instance, the monomials of degree $2$ in $2$ variables are $x^{2}$, $x y$, and $y^{2}$. This corresponds to: $$\left(\right. \frac{2 + 2 - 1}{2 - 1} \left.\right) = \left(\right. \frac{3}{1} \left.\right) = 3$$

## Similar, opposite and equal monomials

Two monomials are defined as similar if they possess identical variable parts, meaning the same variables raised to the same exponents. For example, $3 x^{2} y$ and $- 5 x^{2} y$ are similar monomials.

Two monomials are considered opposite if they are similar and their coefficients sum to zero. For instance, $4 x y$ and $- 4 x y$ are opposite monomials.

Two monomials are defined as equal if they have both the same variable part and the same coefficient. Formally, two monomials are equal if and only if they are similar and their coefficients are equal.

## Addition and subtraction of monomials

In polynomial algebra, the addition or subtraction of monomials is governed by specific rules. Monomials may be combined only if their variables and corresponding exponents are identical. In these cases, the coefficients are added or subtracted, while the variables and exponents remain unchanged. For example:

$$3 x + 2 x = 5 x$$

For the expression $3 x^{2} + 2 x$, the monomials cannot be combined because they have different variable parts.

## Product of monomials

Monomials can be multiplied by multiplying their coefficients and adding the [exponents](https://algebrica.org/powers) of the like variables. For instance, the product of $\left(\right. 3 x^{2} \left.\right) \left(\right. 2 x^{3} \left.\right)$ can be computed as follows:

- First, we multiply the coefficients: $3 \times 2 = 6$
- Next, we add the exponents of the like variables: $2 + 3 = 5$

Thus, we get:

$$\left(\right. 3 x^{2} \left.\right) \left(\right. 2 x^{3} \left.\right) = 6 x^{2 + 3} = 6 x^{5}$$

The same rule applies to monomials with multiple variables: multiply the coefficients and add the exponents of each variable independently. For example:

$$\left(\right. 3 x^{2} y \left.\right) \left(\right. 2 x y^{3} \left.\right) = 6 x^{2 + 1} y^{1 + 3} = 6 x^{3} y^{4}$$

---

The product of monomials is both commutative and associative, since multiplication in $\mathbb{R} \left[\right. x_{1} , \ldots , x_{k} \left]\right.$ inherits these properties from $\mathbb{R}$. This means the order and grouping of factors does not affect the result:

$$\left(\right. 3 x^{2} y \left.\right) \left(\right. 2 x y^{3} \left.\right) = \left(\right. 2 x y^{3} \left.\right) \left(\right. 3 x^{2} y \left.\right) = 6 x^{3} y^{4}$$

---

The set of all monomials in $k$ variables with coefficients in $\mathbb{R}$ is closed under multiplication, as the product of any two monomials yields another monomial. Consequently, the monomials constitute a multiplicative semigroup within the polynomial ring $\mathbb{R} \left[\right. x_{1} , \ldots , x_{k} \left]\right. .$

## Division of monomials

To divide monomials, divide their coefficients and subtract the exponents of like variables. For example:

$$\frac{6 x^{5}}{2 x^{2}} = 3 x^{5 - 2} = 3 x^{3}$$

This rule also applies to monomials with multiple variables: divide the coefficients and subtract the exponents of each variable independently. For example:

$$\frac{6 x^{3} y^{2}}{2 x y} = 3 x^{3 - 1} y^{2 - 1} = 3 x^{2} y$$

If the exponent in the divisor is greater than that in the dividend, the result will have a negative exponent, which can be rewritten as a fraction. For example:

$$\frac{x^{2}}{3 x^{3}} = \frac{1}{3} x^{2 - 3} = \frac{1}{3} x^{- 1} = \frac{1}{3 x}$$

Dividing monomials is straightforward when the bases are the same. In contrast, dividing polynomials is more complex and requires structured methods such as [long division](https://algebrica.org/polynomials) or [Ruffini’s rule](https://algebrica.org/ruffinis-rule/).

## Powers

When a monomial is raised to a [power](https://algebrica.org/powers), the exponent applies to each factor: the coefficient is raised to that power, and the exponents of the variables are multiplied by it. For a monomial raised to a positive integer power $n$:

$$\left(\right. a \cdot x_{1}^{n_{1}} \hdots x_{k}^{n_{k}} \left.\right)^{n} = a^{n} \cdot x_{1}^{n_{1} \cdot n} \hdots x_{k}^{n_{k} \cdot n}$$

For example:

$$\left(\right. 3 x^{3} \left.\right)^{2} = 3^{2} \cdot x^{3 \cdot 2} = 9 x^{6}$$

The same rule extends to monomials in multiple variables:

$$\left(\right. 2 x^{2} y^{3} \left.\right)^{3} = 2^{3} \cdot x^{2 \cdot 3} \cdot y^{3 \cdot 3} = 8 x^{6} y^{9}$$

When $n = 0$, any non-zero monomial raised to the zeroth power equals $1$, since $a^{0} = 1$ and $x_{i}^{0} = 1$ for all $i$.

## GCD and LCM of monomials

The greatest common divisor (GCD) of two or more monomials is defined as the monomial with the largest coefficient that divides all given coefficients and the smallest exponent for each variable present in all monomials. In contrast, the least common multiple (LCM) is the monomial with the smallest coefficient divisible by all given coefficients and the largest exponent for each variable present in any of the monomials.

For example, consider the monomials $12 x^{3} y^{2}$ and $8 x^{2} y^{4}$. The GCD of the coefficients is $gcd \left(\right. 12 , 8 \left.\right) = 4$. For each variable, the minimum exponent is selected: $min \left(\right. 3 , 2 \left.\right) = 2$ for $x$ and $min \left(\right. 2 , 4 \left.\right) = 2$ for $y$. Therefore, the GCD is:

$$gcd \left(\right. 12 x^{3} y^{2} , 8 x^{2} y^{4} \left.\right) = 4 x^{2} y^{2}$$

For the LCM, the least common multiple of the coefficients is $\text{lcm} \left(\right. 12 , 8 \left.\right) = 24$. For each variable, the maximum exponent is selected: $max \left(\right. 3 , 2 \left.\right) = 3$ for $x$ and $max \left(\right. 2 , 4 \left.\right) = 4$ for $y$. Therefore, the LCM is:

$$\text{lcm} \left(\right. 12 x^{3} y^{2} , 8 x^{2} y^{4} \left.\right) = 24 x^{3} y^{4}$$

A variable that appears in only one of the monomials is included in the LCM with its full exponent, but is excluded from the GCD.

homogeneouspolynomial relationequal monomialsopposite monomialssimilar monomialsclosureexponent rulespowersdivisionproductsubtractionadditiondegreezero monomialnotationexponentsvariablescoefficientdefinitionstructuresoperationsfoundations
