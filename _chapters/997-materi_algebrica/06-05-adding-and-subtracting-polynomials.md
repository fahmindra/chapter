---
layout: chapter
title: "Adding and Subtracting Polynomials"
chapter: "Polynomials"
chapter_order: 6
section_order: 5
permalink: /materi-algebrica/polynomials/adding-and-subtracting-polynomials/
---

## Definition and basic properties

Let $R$ be a commutative ring and $R \left[\right. x \left]\right.$ the ring of polynomials in one
indeterminate over $R$. Consider two [polynomials](https://algebrica.org/polynomials/) $P \left(\right. x \left.\right)$ and $Q \left(\right. x \left.\right)$,
where any missing coefficients are understood to be zero:

$$P \left(\right. x \left.\right) = \sum_{k = 0}^{n} a_{k} x^{k} Q \left(\right. x \left.\right) = \sum_{k = 0}^{m} b_{k} x^{k}$$

Addition is performed by summing the coefficients of terms with the same degree:

$$P \left(\right. x \left.\right) + Q \left(\right. x \left.\right) = \sum_{k = 0}^{max \left(\right. n , m \left.\right)} \left(\right. a_{k} + b_{k} \left.\right) x^{k}$$

The sum is the Cauchy addition of the coefficient sequences of $P$ and $Q$, which ensures that polynomial addition is well-defined and independent of the particular representation chosen for each polynomial. The result is again a polynomial, and $R \left[\right. x \left]\right.$ forms an abelian group under addition.

###### An abelian group is a set equipped with a binary operation that is commutative, associative, admits a neutral element, and for which every element has an inverse; $\left(\right. R \left[\right. x \left]\right. , + \left.\right)$ satisfies all four conditions, with the zero polynomial as neutral element and $- P \left(\right. x \left.\right)$ as the inverse of $P \left(\right. x \left.\right)$.

---

Subtraction is defined analogously, with each $b_{k}$ replaced by $- b_{k}$.

$$P \left(\right. x \left.\right) - Q \left(\right. x \left.\right) = \sum_{k = 0}^{max \left(\right. n , m \left.\right)} \left(\right. a_{k} - b_{k} \left.\right) x^{k}$$

How these operations affect the degree depends on whether the leading terms cancel.
Denoting $deg ⁡ P = n$ and $deg ⁡ Q = m$, one has:

$$deg ⁡ \left(\right. P \left(\right. x \left.\right) \pm Q \left(\right. x \left.\right) \left.\right) \leq max \left{\right. n , m \left.\right}$$

If $n \neq m$, the leading term of the polynomial with higher degree remains
unchanged, so the degree of the result is exactly $max n , m$. When $n = m$,
the degree may decrease: if $a_{n} + b_{n} = 0$ under addition, or $a_{n} = b_{n}$
under subtraction, the leading term cancels and the degree falls. If every term cancels,
the result is the zero polynomial, assigned degree $- \infty$ by convention, so that
the rule $deg ⁡ \left(\right. P Q \left.\right) = deg ⁡ P + deg ⁡ Q$ holds without treating zero as a special case.

That multiplicative rule extends to $deg ⁡ \left(\right. P^{k} \left.\right) = k deg ⁡ P$ for any integer
$k \geq 1$, provided $R$ is an integral domain. Over a general commutative
ring this need not hold, as zero divisors can cause the leading coefficient of a product
to vanish even when neither factor is zero.

## Example 1

Take the following polynomials of degree 2:
$$P \left(\right. x \left.\right) = x^{2} + 3 x - 1$$
$$Q \left(\right. x \left.\right) = 2 x^{2} - x + 5$$

Their sum is:

$$P \left(\right. x \left.\right) + Q \left(\right. x \left.\right) & = \left(\right. x^{2} + 3 x - 1 \left.\right) + \left(\right. 2 x^{2} - x + 5 \left.\right) \\ & = \left(\right. 1 + 2 \left.\right) x^{2} + \left(\right. 3 - 1 \left.\right) x + \left(\right. - 1 + 5 \left.\right) \\ & = 3 x^{2} + 2 x + 4$$

The leading coefficients sum to $3 \neq 0$, so the degree is unchanged and the
result is a polynomial of degree 2.

## Example 2

Consider the following polynomials:
$$P \left(\right. x \left.\right) = 2 x^{2} + 3 x - 1$$
$$Q \left(\right. x \left.\right) = 2 x^{2} - x + 5$$

Their difference is computed as follows:

$$P \left(\right. x \left.\right) - Q \left(\right. x \left.\right) & = \left(\right. 2 x^{2} + 3 x - 1 \left.\right) - \left(\right. 2 x^{2} - x + 5 \left.\right) \\ & = \left(\right. 2 - 2 \left.\right) , x^{2} + \left(\right. 3 + 1 \left.\right) , x + \left(\right. - 1 - 5 \left.\right) \\ & = 4 x - 6$$

Since both polynomials share the same leading coefficient, the degree-2 term cancels,
reducing the result to a polynomial of degree 1. This is a case where the following bound is strict:

$$deg ⁡ \left(\right. P - Q \left.\right) \leq max \left{\right. deg ⁡ P , deg ⁡ Q \left.\right}$$

## Example 3

Consider the following polynomials:

$$P \left(\right. x \left.\right) = x^{2} + 3 x - 1$$
$$Q \left(\right. x \left.\right) = 2 x^{4} - x + 5$$

Their sum is computed as follows:

$$P \left(\right. x \left.\right) + Q \left(\right. x \left.\right) & = \left(\right. x^{2} + 3 x - 1 \left.\right) + \left(\right. 2 x^{4} - x + 5 \left.\right) \\ & = 2 x^{4} + x^{2} + \left(\right. 3 - 1 \left.\right) x + \left(\right. - 1 + 5 \left.\right) \\ & = 2 x^{4} + x^{2} + 2 x + 4$$

Since the two polynomials have different degrees, the leading term of $Q \left(\right. x \left.\right)$ has no
counterpart in $P \left(\right. x \left.\right)$ to cancel against. The result is a polynomial of degree 4,
consistent with $deg ⁡ \left(\right. P + Q \left.\right) = max \left{\right. 2 , 4 \left.\right} = 4$.
