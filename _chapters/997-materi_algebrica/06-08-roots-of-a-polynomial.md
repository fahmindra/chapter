---
layout: chapter
title: "Roots of a Polynomial"
chapter: "Polynomials"
chapter_order: 6
section_order: 8
permalink: /materi-algebrica/polynomials/roots-of-a-polynomial/
---

axis touchingaxis crossingsign behaviorodd multiplicityeven multiplicityfactorizationleading divisorsconstant divisorsrational root theoremcomplex rootsnumber of rootsfundamental theoremrepeated rootssimple rootsroot multiplicityx-interceptsevaluation p®=0polynomial zeropropertiestheoremsdefinition

## Definition

Let $p \left(\right. x \left.\right)$ be a [polynomial](https://algebrica.org/polynomials/) with coefficients in a field $\mathbb{F}$, typically $\mathbb{R}$ or $\mathbb{C}$. A root or zero of $p$ is any element $r \in \mathbb{F}$ such that

$$p \left(\right. r \left.\right) = 0$$

More precisely, if we have the polynomial:

$$p \left(\right. x \left.\right) = a_{n} x^{n} + a_{n - 1} x^{n - 1} + \hdots + a_{1} x + a_{0}$$

with $a_{n} \neq 0$, then $r$ is a root. Substituting $x = r$ gives a linear combination of the coefficients that equals zero. The terms root and zero are used interchangeably.

---

For a polynomial $p : \mathbb{R} \rightarrow \mathbb{R}$, the real roots are the $x$-intercepts of its graph. The multiplicity of a root affects the graph locally. At a simple root (multiplicity one), the graph crosses the $x$-axis cleanly and is not tangent.

![Roots of a polynomial.](https://algebrica.org/wp-content/uploads/resources/images/roots-1.png "Roots of a polynomial.")

For a root with even multiplicity, the graph touches the $x$-axis but does not cross it. Since $\left(\right. x - r \left.\right)^{m} \geq 0$ for even $m$, the polynomial does not [change sign](https://algebrica.org/sign-analysis-in-inequalities/) at $r$, and the graph bounces back to the same side of the axis.

![Roots of a polynomial.](https://algebrica.org/wp-content/uploads/resources/images/roots-2.png "Roots of a polynomial.")

For roots with odd multiplicity greater than one ($m \geq 3$), the graph crosses the axis but appears flatter at the intercept, with this flattening becoming more pronounced as multiplicity increases, giving an [inflexion-like](https://algebrica.org/maximum-minimum-and-inflection-points/) appearance.

![Roots of a polynomial.](https://algebrica.org/wp-content/uploads/resources/images/roots-3.png "Roots of a polynomial.")

---

These properties follow from the local factorization:

$$p \left(\right. x \left.\right) = \left(\right. x - r \left.\right)^{m} q \left(\right. x \left.\right)$$

with $q \left(\right. r \left.\right) \neq 0$. Since $q$ is [continuous](https://algebrica.org/continuous-functions/) and nonzero at $r$, it maintains a constant sign in some neighborhood of $r$, so the sign of $p \left(\right. x \left.\right)$ near $r$ is determined entirely by the factor $\left(\right. x - r \left.\right)^{m}$.

- When $m$ is odd, $\left(\right. x - r \left.\right)^{m}$ changes sign as $x$ passes through $r$, so $p$ crosses the axis.
- When $m$ is even, $\left(\right. x - r \left.\right)^{m} \geq 0$ on both sides of $r$, so $p$ does not change sign and the graph returns to the same side of the axis.

A non-zero polynomial of degree $n$ over any field has at most $n$ roots, counted with multiplicity. This follows from the fact that a polynomial of degree $n$ cannot be divisible by more than $n$ linear factors.

###### In particular, two distinct polynomials of degree at most $n$ cannot agree at more than $n$ points. If $p \left(\right. x \left.\right) - q \left(\right. x \left.\right)$ has degree at most $n$ and vanishes at $n + 1$ points, then $p \equiv q$.

## Rational root theorem

Given a polynomial with integer coefficients:

$$p \left(\right. x \left.\right) = a_{n} x^{n} + \hdots + a_{0} \in \mathbb{Z} \left[\right. x \left]\right.$$

the [rational root theorem](https://algebrica.org/polynomial-equations/) identifies a finite set of candidates for rational roots. If $r = s / q$ in lowest terms, with $s , q \in \mathbb{Z}$ and $q > 0$, is a root of $p \left(\right. x \left.\right)$, then necessarily $s \mid a_{0}$ and $q \mid a_{n}$.

This reduces the search for rational roots to a finite collection of fractions, each of which can be verified by direct substitution or [synthetic division](https://algebrica.org/syntetic-division/).

## The Fundamental Theorem of Algebra

In the field of [complex numbers](https://algebrica.org/complex-numbers-introduction/) $\mathbb{C}$, every non-constant polynomial has at least one root. Applying the factor theorem repeatedly, any polynomial of degree $n \geq 1$ decomposes completely into linear factors over $\mathbb{C}$:

$$p \left(\right. x \left.\right) = a_{n} \left(\right. x - r_{1} \left.\right)^{m_{1}} \left(\right. x - r_{2} \left.\right)^{m_{2}} \hdots \left(\right. x - r_{k} \left.\right)^{m_{k}}$$

where $m_{1} + m_{2} + \hdots + m_{k} = n$. Counting roots with their multiplicities, a degree-$n$ polynomial has exactly $n$ roots in $\mathbb{C}$. This property characterises $\mathbb{C}$ as an algebraically closed field.

Over $\mathbb{R}$, the complex roots of a real polynomial occur in conjugate pairs. If $r = \alpha + \beta i$ with $\beta \neq 0$ is a root of $p \in \mathbb{R} \left[\right. x \left]\right.$, then $\bar{r} = \alpha - \beta i$ is also a root, and the two factors combine into an irreducible quadratic over $\mathbb{R}$:

$$\left(\right. x - r \left.\right) \left(\right. x - \bar{r} \left.\right) = x^{2} - 2 \alpha x + \left(\right. \alpha^{2} + \beta^{2} \left.\right)$$

Consequently, every real polynomial of odd degree has at least one real root. The factored form also establishes a direct relationship between roots and coefficients. Expanding we have:

$$a_{n} \left(\right. x - r_{1} \left.\right) \left(\right. x - r_{2} \left.\right) \hdots \left(\right. x - r_{n} \left.\right)$$

Comparing with:

$$a_{n} x^{n} + a_{n - 1} x^{n - 1} + \hdots + a_{0}$$

this yields Vieta’s formulas, which express each coefficient as an elementary symmetric polynomial in the roots. In particular:

$$r_{1} + r_{2} + \hdots + r_{n} = \frac{- a_{n - 1}}{a_{n}}$$
$$r_{1} r_{2} \hdots r_{n} = \frac{\left(\right. - 1 \left.\right)^{n} a_{0}}{a_{n}}$$

The quadratic case is treated in detail in the page on [trinomials](https://algebrica.org/trinomials/).

## Finding roots: an overview of methods

For polynomials of degree 1 and 2, exact formulas are elementary. A linear polynomial $a x + b$ has the unique root $x = - b / a$. For a quadratic $a x^{2} + b x + c$, the roots are given by the quadratic formula:

$$x = \frac{- b \pm \sqrt{b^{2} - 4 a c}}{2 a}$$

The quantity $\Delta = b^{2} - 4 a c$ is the discriminant.

- If $\Delta > 0$ the polynomial has two distinct real roots.
- If $\Delta = 0$ it has one real root of multiplicity 2.
- If $\Delta < 0$ it has two complex conjugate roots.

###### Closed-form solutions also exist for degree 3 (Cardano’s formula) and degree 4 (Ferrari’s method), though they are considerably more involved. For higher degrees, the problem requires more advanced techniques.

---

Roots of a polynomial are precisely the solutions to the corresponding [polynomial equation](https://algebrica.org/polynomial-equations/) $p \left(\right. x \left.\right) = 0$, and the methods outlined above apply directly to both settings.

---

An important application of polynomial roots occurs in [partial fraction decomposition](https://algebrica.org/partial-fraction-decomposition/), where a rational function $P \left(\right. x \left.\right) / Q \left(\right. x \left.\right)$ is expressed as a sum of simpler terms. The structure of these terms is determined by the roots and multiplicities of the denominator $Q \left(\right. x \left.\right)$. Simple roots of $Q \left(\right. x \left.\right)$ correspond to distinct linear factors, whereas repeated roots result in sequences of terms with increasing order.

## Selected references

- **University of Maryland,m C. D. Levermore**. [Formulas for Roots of Polynomials](https://terpconnect.umd.edu/~lvrmr/2019-2020-F/Classes/MATH410/NOTES/Zeros.pdf)
- **Stanford University, S. Boyd**. [Rational Functions and Partial Fraction Expansion](https://web.stanford.edu/~boyd/ee102/rational.pdf)
- **Northeastern University**. [Polynomial Functions, Factorization in $F \left[\right. x \left]\right.$](https://dummit.cos.northeastern.edu/teaching_sp20_3527/3527_lecture_24_factorization_in_F%5Bx%5D.pdf)
