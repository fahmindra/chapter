---
layout: chapter
title: "Factoring Polynomials: AC Method"
chapter: "Polynomials"
chapter_order: 6
section_order: 11
permalink: /materi-algebrica/polynomials/factoring-polynomials-ac-method/
---

## Introduction

A [trinomial](https://algebrica.org/trinomials/) of the form $a x^{2} + b x + c$, where $a , b , c \in \mathbb{Z}$ and $a \neq 0$, is considered factorable over $\mathbb{Z}$ if it can be written as the product of two linear [polynomials](https://algebrica.org/polynomials) with [integer](https://algebrica.org/integers/) coefficients. Specifically, this occurs if there exist integers $p , q , r , s$ such that:

$$a x^{2} + b x + c = \left(\right. p x + q \left.\right) \left(\right. r x + s \left.\right)$$

Expanding the right-hand side results in $p r \cdot x^{2} + \left(\right. p s + q r \left.\right) x + q s$, which leads to the identities:

$$a & = p r \\ b & = p s + q r \\ c & = q s$$

The AC method exploits the multiplicative relationships among these constraints. Notably:

$$a c = p r \cdot q s = \left(\right. p s \left.\right) \left(\right. q r \left.\right)$$

while simultaneously $b = p s + q r$. Defining $m = p s$ and $n = q r$, the problem reduces to finding two integers satisfying:

$$m n & = a c \\ m + n & = b$$

The existence of such a pair $\left(\right. m , n \left.\right)$ is both necessary and sufficient for the trinomial to be factorable over $\mathbb{Z}$. If no such integer pair exists, the trinomial is irreducible over $\mathbb{Z}$, though it may still admit a factorization over $\mathbb{Q}$ or $\mathbb{R}$, depending on the sign of the [discriminant](https://algebrica.org/quadratic-formula/) $b^{2} - 4 a c$.

## The method

Consider a trinomial with integer coefficients in the standard form:
$$a x^{2} + b x + c$$

The procedure is as follows. Compute the product $a c$. Then identify integers $m$ and $n$, if they exist, such that $m n = a c$ and $m + n = b$. This amounts to enumerating the integer divisor pairs of $a c$ and verifying which pair satisfies the sum condition. Once suitable values have been found, rewrite the middle term by splitting $b x$ into $m x + n x$:

$$a x^{2} + b x + c = a x^{2} + m x + n x + c$$

Group the terms into pairs and factor out the greatest common divisor from each group:

$$a x^{2} + m x + n x + c = \left(\right. a x^{2} + m x \left.\right) + \left(\right. n x + c \left.\right)$$

Each group yields a [monomial](https://algebrica.org/monomials/) factor, and the two resulting expressions share a common linear binomial. Extracting that common factor gives the complete factorisation of the trinomial as a product of two linear polynomials.

The two possible orderings of the pair, $\left(\right. m , n \left.\right)$ and $\left(\right. n , m \left.\right)$, result in different intermediate groupings but necessarily produce the same factorisation, since the product $\left(\right. p x + q \left.\right) \left(\right. r x + s \left.\right)$ is invariant under exchange of its factors.

---

In summary, the procedure reduces to the following steps:

- Compute $a c$.
- List the integer divisor pairs of $a c$.
- Identify the pair $\left(\right. m , n \left.\right)$ whose sum equals $b$.
- Rewrite the middle term as $m x + n x$.
- Factor by grouping to extract the common linear binomial.

## Example 1

Consider the trinomial $2 x^{2} + 7 x + 3$. In this case, $a = 2$, $b = 7$, and $c = 3$, so $a c = 6$. The task is to find integers $m$ and $n$ such that $m n = 6$ and $m + n = 7$. The integer pairs $\left(\right. m , n \left.\right)$ with $m n = 6$, listed by absolute value, are:

$$m & n & m n & m + n \\ 1 & 6 & 6 & 7 \\ 2 & 3 & 6 & 5 \\ - 1 & - 6 & 6 & - 7 \\ - 2 & - 3 & 6 & - 5$$

The pair $\left(\right. m , n \left.\right) = \left(\right. 1 , 6 \left.\right)$ satisfies both conditions. The trinomial can therefore be rewritten as

$$2 x^{2} + 7 x + 3 = 2 x^{2} + x + 6 x + 3$$

Group the first two terms and the last two terms as follows:

$$2 x^{2} + x + 6 x + 3 = x \left(\right. 2 x + 1 \left.\right) + 3 \left(\right. 2 x + 1 \left.\right)$$

The [binomial](https://algebrica.org/binomials/) $\left(\right. 2 x + 1 \left.\right)$ is a common factor in both groups, thus we obtain:

$$x \left(\right. 2 x + 1 \left.\right) + 3 \left(\right. 2 x + 1 \left.\right) = \left(\right. x + 3 \left.\right) \left(\right. 2 x + 1 \left.\right)$$

Therefore, the trinomial factors as:

$$2 x^{2} + 7 x + 3 = \left(\right. x + 3 \left.\right) \left(\right. 2 x + 1 \left.\right)$$

Consequently, the [roots](https://algebrica.org/roots-of-a-polynomial/) of the associated equation $2 x^{2} + 7 x + 3 = 0$ follow from the zero-product property, which states that a product of real numbers is zero if and only if at least one factor is zero.

This yields:

$$x_{1} = - 3 x_{2} = - \frac{1}{2}$$

> These results can be verified using the [quadratic formula](https://algebrica.org/quadratic-formula/) which returns the same values, confirming that the factorisation $\left(\right. x + 3 \left.\right) \left(\right. 2 x + 1 \left.\right)$ is correct.

## Relation to Vieta’s formulas

The conditions $m n = a c$ and $m + n = b$, which are central to the AC method, are closely related to a classical result in polynomial theory. [Vieta’s formulas](https://algebrica.org/trinomials/) state that, for a monic quadratic $x^{2} + p x + q$ with roots $x_{1}$ and $x_{2}$, the following relationships hold:

$$x_{1} + x_{2} & = - p \\ x_{1} \cdot x_{2} & = q$$

In the special case where $a = 1$, the trinomial simplifies to $x^{2} + b x + c$, and the AC conditions become $m n = c$ and $m + n = b$. Vieta’s formulas for this polynomial give $x_{1} + x_{2} = - b$ and $x_{1} x_{2} = c$, so one has $m = - x_{1}$ and $n = - x_{2}$: the integers sought by the AC method are the negatives of the roots, and the search for the pair is equivalent to a direct application of Vieta’s formulas.

---

When $a \neq 1$, the correspondence is less direct but remains present. Multiplying the trinomial by $a$ yields

$$a \left(\right. a x^{2} + b x + c \left.\right) = \left(\right. a x \left.\right)^{2} + b \left(\right. a x \left.\right) + a c$$

which is a monic quadratic in the auxiliary variable $u = a x$. Applying Vieta’s formulas to this scaled polynomial requires identifying two numbers whose sum is $b$ and whose product is $a c$, which aligns precisely with the conditions imposed on $m$ and $n$ by the AC method.

> The AC method can therefore be interpreted as an application of Vieta’s formulas to a rescaled polynomial, with the splitting of the middle term serving as the mechanism that transfers the factorisation of the auxiliary polynomial back to the original trinomial.

## On the irreducibility of quadratic trinomials

When no integer pair $\left(\right. m , n \left.\right)$ satisfies $m n = a c$ and $m + n = b$, the trinomial is irreducible over $\mathbb{Z}$. This occurs precisely when the discriminant $\Delta = b^{2} - 4 a c$ is not a perfect square integer.

When $\Delta > 0$ but not a perfect square integer, the trinomial has two distinct irrational real roots and is irreducible over both $\mathbb{Z}$ and $\mathbb{Q}$; when $\Delta < 0$, it has two complex conjugate roots and is likewise irreducible over $\mathbb{R}$.

When $\Delta = 0$, the trinomial has a repeated root $x = - b / \left(\right. 2 a \left.\right)$, which is rational but not necessarily an integer, so irreducibility over $\mathbb{Z}$ depends on whether $2 a \mid b$. The AC method, being combinatorial in nature, terminates without output once all integer divisor pairs of $a c$ have been checked without success, and this exhaustion of cases constitutes a constructive proof of irreducibility over $\mathbb{Z}$.

---

For illustration, consider the trinomial $3 x^{2} + 5 x + 4$. In this case, $a = 3$, $b = 5$, and $c = 4$, yielding $a c = 12$. The integer divisor pairs of $12$ are as follows:

$$m & n & m n & m + n \\ 1 & 12 & 12 & 13 \\ 2 & 6 & 12 & 8 \\ 3 & 4 & 12 & 7 \\ - 1 & - 12 & 12 & - 13 \\ - 2 & - 6 & 12 & - 8 \\ - 3 & - 4 & 12 & - 7$$

None of these pairs satisfies the condition $m + n = 5$. The discriminant confirms this: $\Delta = b^{2} - 4 a c = 25 - 48 = - 23 < 0$. Because $\Delta < 0$, the trinomial has two [complex conjugate roots](https://algebrica.org/quadratic-equations-with-complex-solutions/):

$$x_{1 , 2} & = \frac{- 5 \pm i \sqrt{23}}{6}$$

So, the trinomial admits no factorisation over $\mathbb{R}$, nor over $\mathbb{Z}$.

## Limitations of the AC method

The AC method is effective when the coefficients are small integers and the divisor search concludes rapidly. Its computational cost grows with the number of integer divisor pairs of $a c$.

When $\left|\right. a c \left|\right.$ is large, the enumeration becomes laborious and the method loses its practical advantage over direct application of the quadratic formula. More fundamentally, the method is inherently tied to factorisation over $\mathbb{Z}$.

When the trinomial is irreducible over $\mathbb{Z}$ but possesses real roots, one must resort to the [quadratic formula](https://algebrica.org/quadratic-formula/), which returns the exact roots regardless of whether the discriminant is a perfect square.

## An additional connection

Multiplying the trinomial $a x^{2} + b x + c$ by $a$ produces a monic quadratic in the auxiliary variable $u = a x$:

$$a \left(\right. a x^{2} + b x + c \left.\right) & = \left(\right. a x \left.\right)^{2} + b \left(\right. a x \left.\right) + a c \\ & = u^{2} + b u + a c$$

This polynomial factors over $\mathbb{Z}$ as $\left(\right. u + m \left.\right) \left(\right. u + n \left.\right)$, where $m n = a c$ and $m + n = b$.

Substituting back $u = a x$ gives $\left(\right. a x + m \left.\right) \left(\right. a x + n \left.\right) = a^{2} x^{2} + b \left(\right. a x \left.\right) + a c$, which equals $a \left(\right. a x^{2} + b x + c \left.\right)$, confirming the identity without leaving $\mathbb{Z} \left[\right. x \left]\right.$.

This scaling argument demonstrates that the AC method is equivalent to factoring a monic quadratic in a rescaled variable, and connects to the notion of reducibility in the polynomial [ring](https://algebrica.org/rings/) $\mathbb{Z} \left[\right. x \left]\right.$. The trinomial $a x^{2} + b x + c$ is reducible in $\mathbb{Z} \left[\right. x \left]\right.$ if and only if the integer pair $\left(\right. m , n \left.\right)$ exists.

polynomial ringirreducible casescomplex rootsreal rootsdiscriminantzero productvieta formulaslinear factorscommon factorfactoring by groupingmiddle term splitdivisor pairsproduct acac methodquadratic formleading coefficientfactorable trinomialsinteger coefficientscoefficientsstandard formpropertiesmethodsstructure
