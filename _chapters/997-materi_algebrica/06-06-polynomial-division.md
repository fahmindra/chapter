---
layout: chapter
title: "Polynomial Division"
chapter: "Polynomials"
chapter_order: 6
section_order: 6
permalink: /materi-algebrica/polynomials/polynomial-division/
---

## The division algorithm

Let $P \left(\right. x \left.\right)$ and $D \left(\right. x \left.\right)$ be [polynomials](https://algebrica.org/polynomials/) in $\mathbb{R} \left[\right. x \left]\right.$ with $D \left(\right. x \left.\right) \neq 0$. The division algorithm asserts the existence of unique polynomials $Q \left(\right. x \left.\right)$ and $R \left(\right. x \left.\right)$ in $\mathbb{R} \left[\right. x \left]\right.$ such that:

$$P \left(\right. x \left.\right) = Q \left(\right. x \left.\right) \cdot D \left(\right. x \left.\right) + R \left(\right. x \left.\right)$$

$$deg ⁡ R \left(\right. x \left.\right) < deg ⁡ D \left(\right. x \left.\right) \text{or} R \left(\right. x \left.\right) = 0$$

- The polynomial $P \left(\right. x \left.\right)$ is referred to as the dividend.
- $D \left(\right. x \left.\right)$ as the divisor.
- $Q \left(\right. x \left.\right)$ as the quotient.
- $R \left(\right. x \left.\right)$ as the remainder.

If $R \left(\right. x \left.\right) = 0$, the division is exact and $D \left(\right. x \left.\right)$ divides $P \left(\right. x \left.\right)$ in $\mathbb{R} \left[\right. x \left]\right.$. This result is directly analogous to the Euclidean division of integers and holds in any polynomial ring $F \left[\right. x \left]\right.$, where $F$ is a field. The existence of such a representation can be established by induction on $deg ⁡ P$, while uniqueness follows from a degree argument. Suppose that two representations exist:

$$P \left(\right. x \left.\right) & = Q_{1} \left(\right. x \left.\right) \cdot D \left(\right. x \left.\right) + R_{1} \left(\right. x \left.\right) \\ & = Q_{2} \left(\right. x \left.\right) \cdot D \left(\right. x \left.\right) + R_{2} \left(\right. x \left.\right)$$

Subtracting yields $\left(\right. Q_{1} \left(\right. x \left.\right) - Q_{2} \left(\right. x \left.\right) \left.\right) \cdot D \left(\right. x \left.\right) = R_{2} \left(\right. x \left.\right) - R_{1} \left(\right. x \left.\right)$. If $Q_{1} \neq Q_{2}$, the left-hand side has degree at least $deg ⁡ D$, whereas the right-hand side satisfies $deg ⁡ \left(\right. R_{2} - R_{1} \left.\right) < deg ⁡ D$, a contradiction. Therefore $Q_{1} = Q_{2}$, and consequently $R_{1} = R_{2}$.

###### A ring is defined as an algebraic structure with two operations, addition and multiplication, that satisfy associativity, distributivity, and the existence of additive inverses. A field is a ring in which every nonzero element possesses a multiplicative inverse. Common examples of fields are $\mathbb{Q}$, $\mathbb{R}$, and $\mathbb{C}$.

---

Let $P \left(\right. x \left.\right)$ and $D \left(\right. x \left.\right)$ be nonzero polynomials such that $deg ⁡ P \geq deg ⁡ D$. The degrees of the quotient and remainder are as follows:

$$deg ⁡ Q \left(\right. x \left.\right) = deg ⁡ P \left(\right. x \left.\right) - deg ⁡ D \left(\right. x \left.\right)$$
$$deg ⁡ R \left(\right. x \left.\right) < deg ⁡ D \left(\right. x \left.\right)$$

If $deg ⁡ P < deg ⁡ D$, then the quotient is the zero polynomial and the remainder is $P \left(\right. x \left.\right)$.

## Polynomial long division

The long division algorithm involves repeatedly dividing the leading term of the current remainder by the leading term of $D \left(\right. x \left.\right)$, subtracting the resulting product, and continuing this process until the degree of the remainder is less than that of $D \left(\right. x \left.\right)$. The procedure can be summarized in the following steps:

- First, divide the leading term of the current dividend by the leading term of $D \left(\right. x \left.\right)$ to determine the next term of $Q \left(\right. x \left.\right)$.
- Next, multiply this term by $D \left(\right. x \left.\right)$ and subtract the result from the current dividend.
- Repeat these steps until the degree of the remaining expression is strictly less than $deg ⁡ D \left(\right. x \left.\right)$.

###### When the divisor is a linear polynomial of the form $x - c$, the procedure can be carried out more efficiently using the [synthetic division method](https://algebrica.org/syntetic-division/), which reduces the computation to operations on coefficients alone.

## Example 1

We apply the method outlined above to compute the quotient of $P \left(\right. x \left.\right)$ and $D \left(\right. x \left.\right)$ where:

$$P \left(\right. x \left.\right) = x^{3} + 2 x^{2} - x - 2$$
$$D \left(\right. x \left.\right) = x - 1$$

The division table is constructed with terms arranged in descending order of degree:

$$+ x^{3} & + 2 x^{2} & - x & - 2 & + x & - 1 \\$$

Dividing the leading term $x^{3}$ by $x$ yields $x^{2}$. Next, multiply $x^{2}$ by $D \left(\right. x \left.\right) = x - 1$ and subtract the result:

$$+ x^{3} & + 2 x^{2} & - x & - 2 & x & - 1 \\ - x^{3} & + x^{2} & & & x^{2} & \\ // & + 3 x^{2} & - x & - 2 & &$$

Dividing $3 x^{2}$ by $x$ yields $3 x$. Multiply and subtract as before:

$$+ x^{3} & + 2 x^{2} & - x & - 2 & x & - 1 \\ - x^{3} & + x^{2} & & & x^{2} & + 3 x \\ // & + 3 x^{2} & - x & - 2 & & \\ & - 3 x^{2} & + 3 x & & & \\ // & // & + 2 x & - 2 & &$$

Dividing $2 x$ by $x$ yields $2$. Multiply and subtract to complete the process:

$$+ x^{3} & + 2 x^{2} & - x & - 2 & x & - 1 \\ - x^{3} & + x^{2} & & & x^{2} & + 3 x + 2 \\ // & + 3 x^{2} & - x & - 2 & & \\ & - 3 x^{2} & + 3 x & & & \\ // & // & + 2 x & - 2 & & \\ & & - 2 x & + 2 & & \\ & & // & 0 & &$$

Since the remainder is zero, the division is exact. The result is:

$$Q \left(\right. x \left.\right) = x^{2} + 3 x + 2 R \left(\right. x \left.\right) = 0$$

and therefore:

$$x^{3} + 2 x^{2} - x - 2 = \left(\right. x^{2} + 3 x + 2 \left.\right) \left(\right. x - 1 \left.\right)$$

## Example 2

The following example demonstrates a case where the division is not exact; specifically, the remainder $R \left(\right. x \left.\right)$ is a nonzero polynomial whose degree is strictly less than $deg ⁡ D \left(\right. x \left.\right)$.

The method outlined above is applied to compute the quotient of the following polynomials:

$$P \left(\right. x \left.\right) = x^{3} + x^{2} + x + 2$$
$$D \left(\right. x \left.\right) = x^{2} + 1$$

The division table is constructed with terms arranged in descending order of degree:

$$+ x^{3} & + x^{2} & + x & + 2 & x^{2} & + 1 \\$$

Dividing $x^{3}$ by $x^{2}$ yields $x$. Multiplying $x$ by $D \left(\right. x \left.\right)$ and subtracting produces the next row:

$$+ x^{3} & + x^{2} & + x & + 2 & x^{2} & + 1 \\ - x^{3} & & - x & & x & \\ // & + x^{2} & // & + 2 & &$$

Dividing $x^{2}$ by $x^{2}$ yields $1$. Multiplying and subtracting results in the following:

$$+ x^{3} & + x^{2} & + x & + 2 & x^{2} & + 1 \\ - x^{3} & & - x & & x & + 1 \\ // & + x^{2} & // & + 2 & & \\ & - x^{2} & & - 1 & & \\ & // & & + 1 & &$$

The degree of the remainder $1$ is $0$, which is strictly less than $deg ⁡ D \left(\right. x \left.\right) = 2$. Therefore, the algorithm terminates. The quotient and remainder are:

$$Q \left(\right. x \left.\right) = x + 1 R \left(\right. x \left.\right) = 1$$

The division can be written as:

$$x^{3} + x^{2} + x + 2 = \left(\right. x + 1 \left.\right) \left(\right. x^{2} + 1 \left.\right) + 1$$

## The remainder theorem and the factor theorem

The division algorithm leads to a result that connects polynomial division with the evaluation of a polynomial at a specific point. Instead of computing $P \left(\right. c \left.\right)$ directly, the same value can be obtained as a consequence of dividing $P \left(\right. x \left.\right)$ by the linear polynomial $x - c$. Let $P \left(\right. x \left.\right) \in \mathbb{R} \left[\right. x \left]\right.$ and $c \in \mathbb{R}$. When $P \left(\right. x \left.\right)$ is divided by the linear polynomial $x - c$, the remainder equals $P \left(\right. c \left.\right)$.

Applying the division algorithm with divisor $D \left(\right. x \left.\right) = x - c$, since $deg ⁡ D = 1$, the remainder $R \left(\right. x \left.\right)$ must satisfy $deg ⁡ R < 1$, implying that $R \left(\right. x \left.\right)$ is a constant, denoted $r$. The division algorithm then yields:

$$P \left(\right. x \left.\right) = Q \left(\right. x \left.\right) \left(\right. x - c \left.\right) + r$$

Substituting $x = c$ into both sides:

$$P \left(\right. c \left.\right) = Q \left(\right. c \left.\right) \left(\right. c - c \left.\right) + r = 0 + r = r$$

Thus $r = P \left(\right. c \left.\right)$, which establishes the result.

##### The remainder theorem offers a direct method for evaluating a polynomial at a specific point without performing the complete division. The value $P \left(\right. c \left.\right)$ is given by the remainder when dividing by $x - c$.

---

The following result, known as the factor theorem, is a direct consequence of the remainder theorem. Let $P \left(\right. x \left.\right) \in \mathbb{R} \left[\right. x \left]\right.$ and $c \in \mathbb{R}$. The polynomial $x - c$ divides $P \left(\right. x \left.\right)$ in $\mathbb{R} \left[\right. x \left]\right.$ if and only if $P \left(\right. c \left.\right) = 0$.

This result can be proved directly using the remainder theorem. Dividing $P \left(\right. x \left.\right)$ by $x - c$ gives $P \left(\right. x \left.\right) = Q \left(\right. x \left.\right) \left(\right. x - c \left.\right) + r$, where $r = P \left(\right. c \left.\right)$. Therefore, $x - c$ divides $P \left(\right. x \left.\right)$ if and only if $r = 0$, which is equivalent to $P \left(\right. c \left.\right) = 0$.

The factor theorem establishes a correspondence between the [roots](https://algebrica.org/roots-of-a-polynomial/) of a polynomial and its linear factors: $c$ is a root of $P \left(\right. x \left.\right)$ if and only if $x - c$ is a factor of $P \left(\right. x \left.\right)$ in $\mathbb{R} \left[\right. x \left]\right.$.

###### This principle underlies the factorisation of polynomials over a field and will be explored further in the section on [polynomial factorisation](https://algebrica.org/polynomials/).

## Example 3

As an application of the remainder theorem, consider the polynomial:

$$P \left(\right. x \left.\right) = 2 x^{3} - 3 x^{2} + x - 5$$

and the value $c = 2$. According to the theorem, dividing $P \left(\right. x \left.\right)$ by $x - 2$ yields a remainder equal to $P \left(\right. 2 \left.\right)$. Computing $P \left(\right. 2 \left.\right)$ directly by substitution we obtain:

$$P \left(\right. 2 \left.\right) = 2 \left(\right. 2 \left.\right)^{3} - 3 \left(\right. 2 \left.\right)^{2} + \left(\right. 2 \left.\right) - 5 = 16 - 12 + 2 - 5 = 1$$

The remainder theorem predicts that the remainder of dividing $P \left(\right. x \left.\right)$ by $x - 2$ is $1$. This result can be verified using the long division method:

$$+ 2 x^{3} & - 3 x^{2} & + x & - 5 & x & - 2 \\$$

Dividing the leading term $2 x^{3}$ by $x$ yields $2 x^{2}$, which serves as the initial term of the quotient. Multiplying $2 x^{2}$ by $D \left(\right. x \left.\right) = x - 2$ and subtracting the result from the dividend produces:

$$+ 2 x^{3} & - 3 x^{2} & + x & - 5 & x & - 2 \\ - 2 x^{3} & + 4 x^{2} & & & 2 x^{2} & \\ // & + x^{2} & + x & - 5 & &$$

Dividing $x^{2}$ by $x$ yields $x$. Multiplying and subtracting we obtain:

$$+ 2 x^{3} & - 3 x^{2} & + x & - 5 & x & - 2 \\ - 2 x^{3} & + 4 x^{2} & & & 2 x^{2} & + x \\ // & + x^{2} & + x & - 5 & & \\ & - x^{2} & + 2 x & & & \\ // & // & + 3 x & - 5 & &$$

Dividing $3 x$ by $x$ yields $3$. Multiplying and subtracting:

$$+ 2 x^{3} & - 3 x^{2} & + x & - 5 & x & - 2 \\ - 2 x^{3} & + 4 x^{2} & & & 2 x^{2} & + x + 3 \\ // & + x^{2} & + x & - 5 & & \\ & - x^{2} & + 2 x & & & \\ // & // & + 3 x & - 5 & & \\ & & - 3 x & + 6 & & \\ & & // & + 1 & &$$

The remainder is $1$, confirming that $R = P \left(\right. 2 \left.\right) = 1$ in accordance with the remainder theorem. The quotient and remainder are:

$$Q \left(\right. x \left.\right) = 2 x^{2} + x + 3 R = 1$$

The division can be written as:

$$2 x^{3} - 3 x^{2} + x - 5 = \left(\right. 2 x^{2} + x + 3 \left.\right) \left(\right. x - 2 \left.\right) + 1$$

## Rational functions and polynomial division

When the division of two polynomials is performed without separating the remainder, the result is represented as a [rational function](https://algebrica.org/rational-functions/) where $D \left(\right. x \left.\right) \neq 0$:

$$F \left(\right. x \left.\right) = \frac{P \left(\right. x \left.\right)}{D \left(\right. x \left.\right)}$$

In this context, polynomial division offers a systematic method to decompose $F \left(\right. x \left.\right)$ into a polynomial component and a proper rational component. A proper rational function is defined as one in which the numerator has a strictly lower degree than the denominator:

$$\frac{P \left(\right. x \left.\right)}{D \left(\right. x \left.\right)} = Q \left(\right. x \left.\right) + \frac{R \left(\right. x \left.\right)}{D \left(\right. x \left.\right)}$$

This decomposition is unique. The polynomial part $Q \left(\right. x \left.\right)$ and the proper rational part $R \left(\right. x \left.\right) / D \left(\right. x \left.\right)$ are uniquely determined by $P \left(\right. x \left.\right)$ and $D \left(\right. x \left.\right)$, as a direct consequence of the uniqueness of the division algorithm.

This decomposition serves as the foundation for [partial fraction decomposition](https://algebrica.org/partial-fraction-decomposition/), a technique that expresses the proper rational component as a sum of simpler fractions. This method is widely utilised in integration.

## Selected References

- **Cornell University, J. Belk**. [Number Theory for Polynomials](https://e.math.cornell.edu/people/belk/numbertheory/NumberTheoryPolynomials.pdf)
- **University of Connecticut, K. Conrad**. [The Division Algorithm in Z](https://kconrad.math.uconn.edu/blurbs/ugradnumthy/divthmZF%5BT%5D.pdf)
- **Harvard University, S. Vadhan**. [Polynomial Rings and Division with Remainder](https://people.seas.harvard.edu/~salil/am106/fall09/lec16.pdf)
- **Harvard University, C. McMullen**. [Algebra II: Rings and Fields](https://people.math.harvard.edu/~ctm/home/text/class/harvard/123/23/html/home/course/course.pdf)
