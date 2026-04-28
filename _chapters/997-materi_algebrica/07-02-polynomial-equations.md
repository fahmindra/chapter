---
layout: chapter
title: "Polynomial Equations"
chapter: "Equations"
chapter_order: 7
section_order: 2
permalink: /materi-algebrica/equations/polynomial-equations/
---

## Definition

A polynomial equation is an equation in which one side consists of a [polynomial](https://algebrica.org/polynomials) expression and the other is zero. The general form of such an equation is the following:

$$a_{n} x^{n} + a_{n - 1} x^{n - 1} + \hdots + a_{1} x + a_{0} = 0$$

In this expression:

- $n$ is a non-negative integer called the degree of the equation.
- The coefficients $a_{0} , a_{1} , \ldots , a_{n}$ are real or [complex numbers](https://algebrica.org/complex-numbers-introduction/).
- The leading coefficient $a_{n}$ is assumed to be non-zero.
- The unknown $x$ is the variable for which a solution is sought.

A value $x_{0}$ that satisfies the equation is called a [root](https://algebrica.org/roots-of-a-polynomial/), or a solution, of the polynomial equation.

## Degree and classification

The degree of a polynomial equation determines much of its behaviour and governs how many solutions one may expect to find. A polynomial equation of degree one is called a [linear equation](https://algebrica.org/linear-equations/). Its general form is the following:

$$a_{1} x + a_{0} = 0$$

Since $a_{1} \neq 0$, this equation has exactly one real solution, which is obtained by isolating $x$.

$$x = - \frac{a_{0}}{a_{1}}$$

---

A polynomial equation of degree two is called a [quadratic equation](https://algebrica.org/quadratic-equations/). Its general form is the following:

$$a_{2} x^{2} + a_{1} x + a_{0} = 0$$

The solutions of a quadratic equation are described by the [quadratic formula](https://algebrica.org/quadratic-formula/), which expresses them in terms of the discriminant $\Delta = a_{1}^{2} - 4 a_{2} a_{0}$. A polynomial equation of degree three is called a cubic equation, and one of degree four is called a quartic equation.

###### Beyond degree four, equations are generally referred to by their numerical degree: degree-five equations, degree-six equations, and so forth.

Solving a polynomial equation is equivalent to factoring the polynomial into linear or irreducible quadratic factors and setting each factor equal to zero. Every root corresponds to a linear factor, and finding all roots is therefore the same problem as achieving a complete factorisation of the polynomial.

## The Fundamental Theorem of Algebra

The existence and count of roots of a polynomial equation are governed by the Fundamental Theorem of Algebra, which guarantees that every polynomial equation of degree $n \geq 1$ with complex coefficients has exactly $n$ roots in $\mathbb{C}$, counted with multiplicity.

The implications of this theorem, including the factorisation into linear factors over $\mathbb{C}$ and the conjugate-pair structure of [complex roots](https://algebrica.org/quadratic-equations-with-complex-solutions/) of real polynomials, are discussed in the entry on [roots of a polynomial](https://algebrica.org/roots-of-a-polynomial/).

## Multiplicity of roots

A root $x_{0}$ is said to have multiplicity $m$ if the factor $\left(\right. x - x_{0} \left.\right)^{m}$ divides the polynomial but $\left(\right. x - x_{0} \left.\right)^{m + 1}$ does not.

- A root of multiplicity one is called a simple root.
- A root of multiplicity two is called a double root, and so on.

The multiplicity of a root has a [geometric interpretation](https://algebrica.org/roots-of-a-polynomial/): a simple root corresponds to a transversal crossing of the graph of the polynomial with the horizontal axis, while a root of even multiplicity corresponds to a tangency point where the graph touches but does not cross the axis.

## Rational Root Theorem

When the coefficients of a polynomial equation are [integers](https://algebrica.org/integers/), it is possible to identify all candidates for rational roots without solving the equation directly. Suppose the equation is the following.

$$a_{n} x^{n} + a_{n - 1} x^{n - 1} + \hdots + a_{1} x + a_{0} = 0$$

If $x = p / q$ is a rational root expressed in lowest terms, then $p$ must be a divisor of the constant term $a_{0}$ and $q$ must be a divisor of the leading coefficient $a_{n}$. This result, known as the Rational Root Theorem, reduces the search for rational solutions to a finite list of candidates. As an illustration, consider the following equation.

$$2 x^{3} - 3 x^{2} - 11 x + 6 = 0$$

The divisors of the constant term $6$ are $\pm 1 , \pm 2 , \pm 3 , \pm 6$, and the divisors of the leading coefficient $2$ are $\pm 1 , \pm 2$. The rational root candidates are therefore all fractions of the form $p / q$ drawn from these two sets. Testing $x = 3$ by direct substitution gives the following.

$$2 \left(\right. 27 \left.\right) - 3 \left(\right. 9 \left.\right) - 11 \left(\right. 3 \left.\right) + 6 = 54 - 27 - 33 + 6 = 0$$

Since $x = 3$ is a root, the factor $\left(\right. x - 3 \left.\right)$ divides the polynomial. Performing the division yields the following factorisation.

$$2 x^{3} - 3 x^{2} - 11 x + 6 = \left(\right. x - 3 \left.\right) \left(\right. 2 x^{2} + 3 x - 2 \left.\right)$$

The residual quadratic $2 x^{2} + 3 x - 2$ can be factored as $\left(\right. 2 x - 1 \left.\right) \left(\right. x + 2 \left.\right)$, giving the complete factorisation.

$$2 x^{3} - 3 x^{2} - 11 x + 6 = \left(\right. x - 3 \left.\right) \left(\right. 2 x - 1 \left.\right) \left(\right. x + 2 \left.\right)$$

The three real roots are therefore $x = 3$, $x = 1 / 2$, and $x = - 2$.

## Vieta’s formulas

The coefficients of a polynomial equation are not independent of its roots: they are related to them through a set of identities known as Vieta’s formulas. For a monic polynomial equation of degree $n$ with roots $x_{1} , x_{2} , \ldots , x_{n}$, these identities take the following form.

$$x_{1} + x_{2} + \hdots + x_{n} & = - c_{n - 1} \\ \underset{i < j}{\sum} x_{i} x_{j} & = c_{n - 2} \\ & \vdots \\ x_{1} x_{2} \hdots x_{n} & = \left(\right. - 1 \left.\right)^{n} c_{0}$$

In other words, each coefficient is an elementary symmetric polynomial in the roots. The derivation and a detailed discussion of the quadratic case are given in the entry on [trinomials](https://algebrica.org/trinomials/).

## Reduction to a polynomial equation

Many equations that do not appear polynomial at first sight can be reduced to polynomial form through algebraic manipulation, after which the methods discussed in this entry apply directly. A rational equation such as the following

$$x + \frac{1}{x} = 3$$

becomes polynomial upon multiplying both sides by $x$, yielding $x^{2} - 3 x + 1 = 0$. An [irrational equation](https://algebrica.org/irrational-equations/) such as:

$$\sqrt{x + 1} + x = 5$$

becomes polynomial after isolating the radical and squaring both sides. Isolating the radical gives the following.

$$\sqrt{x + 1} = 5 - x$$

Squaring both sides yields the following:

$$x + 1 = \left(\right. 5 - x \left.\right)^{2} = 25 - 10 x + x^{2}$$

Rearranging, we obtains the quadratic equation:

$$x^{2} - 11 x + 24 = 0$$

whose solutions are $x = 3$ and $x = 8$. Substituting back into the original equation, $x = 3$ satisfies it, while $x = 8$ does not, since:

$$\sqrt{9} + 8 = 11 \neq 5$$

The value $x = 8$ is an extraneous solution introduced by the squaring step.

In both cases the reduction introduces constraints that must be checked: multiplying by $x$ requires $x \neq 0$, and squaring may introduce extraneous solutions that do not satisfy the original equation.

The reduction technique and the verification of solutions are treated in detail in the entries on [rational equations](https://algebrica.org/rational-equations/) and [irrational equations](https://algebrica.org/irrational-equations/).

## Solvability by radicals

For polynomial equations of degree up to four, explicit formulas expressing the roots in terms of the coefficients by means of arithmetic operations and radicals are known. The quadratic formula handles degree two. Analogous but considerably more involved formulas, due to Cardano and Ferrari, handle degrees three and four respectively.

For degree five and beyond, no such general formula exists. This result, established rigorously by Abel and [Ruffini](https://algebrica.org/syntetic-division/) and placed within a definitive theoretical framework by Galois, is one of the landmark theorems of modern algebra.

The Galois group of a general polynomial of degree five or higher is not solvable, which rules out any solution expressible solely by radicals. Particular equations of high degree may still be solvable by radicals if their Galois group happens to be solvable, but no universal formula of that type can exist.

---

To appreciate what this means concretely, consider this equations:

$$x^{5} - 1 = 0$$

The equations factors as:
$$\left(\right. x - 1 \left.\right) \left(\right. x^{4} + x^{3} + x^{2} + x + 1 \left.\right) = 0$$

and its five roots are the fifth roots of unity, which can be written explicitly in terms of radicals and trigonometric values.

Now consider the following equation:

$$x^{5} - x - 1 = 0$$

This equation has no such closed form. Its real root cannot be expressed by any finite combination of arithmetic operations and radicals applied to the coefficients. Both equations have degree five, but their algebraic structure differs in a way that determines whether a radical formula is possible.

## Numerical methods

When an analytic solution is unavailable or impractical, polynomial equations are typically solved by numerical methods. The most widely used of these is Newton’s method, which generates successive approximations to a root by iterating the following update rule:

$$x_{k + 1} = x_{k} - \frac{p \left(\right. x_{k} \left.\right)}{p^{'} \left(\right. x_{k} \left.\right)}$$

Starting from an initial estimate $x_{0}$ sufficiently close to a simple root, the [sequence](https://algebrica.org/sequences/) $\left(\right. x_{k} \left.\right)$ converges quadratically to that root, meaning that the number of correct decimal digits roughly doubles with each iteration. Other methods, such as the bisection method and Brent’s method, sacrifice speed for guaranteed convergence and are preferred when robustness is a priority.
