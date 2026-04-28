---
layout: chapter
title: "Quadratic Equations"
chapter: "Equations"
chapter_order: 7
section_order: 4
permalink: /materi-algebrica/equations/quadratic-equations/
---

repeated rootdistinct rootsnature of rootsvieta relationscompleting squarefactoringdiscriminantquadratic formuladiscriminant meaningaxis of symmetryvertexopening directionx-axis intersectionparabolaleading coefficientstandard formdegenerate casevariablecoefficientsquadratic formsolutionsgeometrystructure

## Introduction

A quadratic equation is a second-degree [polynomial equation](https://algebrica.org/polynomial-equations/) in one variable. Its standard form is the following:

$$a x^{2} + b x + c = 0$$

where $a$, $b$, and $c$ are real coefficients, $x$ is the unknown, and
$a \neq 0$.

- The coefficients $a$, $b$, and $c$ are constants.
- $x$ represents the variable.
- $a$ is the coefficient of the quadratic term $x^{2}$, $b$ the coefficient of the linear term $x$ and $c$ the constant term.
- When $a = 0$, the equation reduces to the linear equation $b x + c = 0$. If $b = 0$ as well, the equation becomes constant and may have no solution or infinitely many solutions, depending on whether $c \neq 0$ or $c = 0$.

Quadratic equations are a particular type of [trinomial equation](https://algebrica.org/trinomial-equations) with the exponent $n$ equal to 1:

$$a x^{2 n} + b x^{n} + c = 0 , n = 1$$

## Geometrical interpretation

A quadratic equation in the form $y = a x^{2} + b x + c$, where $a \neq 0$,
represents a [parabola](https://algebrica.org/parabola) in the plane defined by the variables $x$ and
$y$. The real solutions of the equation $a x^{2} + b x + c = 0$ correspond to
the points at which the parabola intersects the $x$-axis.

![Parabola.](https://algebrica.org/wp-content/uploads/resources/images/quadratic-equations-params-6.png "Parabola.")

When $a > 0$ the parabola opens upward, and when $a < 0$ it opens downward. This determines whether the vertex represents a minimum or a maximum of the function:

$$y = a x^{2} + b x + c$$

When the [discriminant](https://algebrica.org/quadratic-formula/) $\Delta = b^{2} - 4 a c$ is positive, the parabola crosses the axis at two distinct points; when it is zero, the parabola is tangent to the axis; and when it is negative, the parabola does not intersect the axis and the equation has no real solutions.

###### The condition $a \neq 0$ ensures that the equation describes a parabolic curve rather than a [linear equation](https://algebrica.org/linear-equation).

## Resolution methods

A quadratic equation is [incomplete](https://algebrica.org/incomplete-quadratic-equations/) when either the
coefficient $b$ or $c$ is equal to zero. In this case the equation takes a
simpler form and can be solved directly, without applying the general formula. The first step in solving a quadratic equation is to rewrite it in standard form:

$$a x^{2} + b x + c = 0$$

This form allows the coefficients to be identified and the [discriminant](https://algebrica.org/quadratic-formula/) $\Delta = b^{2} - 4 a c$ to be computed. The discriminant determines the nature of the solutions:

- Two distinct real roots when $\Delta > 0$.
- One real root of multiplicity two when $\Delta = 0$.
- A pair of complex conjugate roots when $\Delta < 0$.

The most general method of resolution is the [quadratic formula](https://algebrica.org/quadratic-formula/).
In some cases, however, [factoring](https://algebrica.org/factoring-quadratic-equations/) or [completing the square](https://algebrica.org/completing-the-square) can offer a more direct route to the
solution.

The [fundamental theorem of algebra](https://algebrica.org/roots-of-a-polynomial/) guarantees that a
quadratic equation has exactly two roots in $\mathbb{C}$, counted with multiplicity.
The roots are both real when $\Delta \geq 0$, and form a pair of [complex conjugates](https://algebrica.org/quadratic-equations-with-complex-solutions/) when $\Delta < 0$.

## Quadratic formula

Given a quadratic equation in the standard form $a x^{2} + b x + c = 0$, the [quadratic formula](https://algebrica.org/quadratic-equations/quadratic-formula/) is:

$$x_{1 , 2} = \frac{- b \pm \sqrt{b^{2} - 4 a c}}{2 a}$$

- $a$, $b$, $c$ are real coefficients and $a \neq 0$.
- The $\pm$ symbol reflects the existence of two solutions, corresponding to the two signs.
- A quadratic equation has exactly two roots in $\mathbb{C}$, counted with multiplicity.
- By Vieta’s formulas, the roots satisfy $x_{1} + x_{2} = - b / a$ and $x_{1} \cdot x_{2} = c / a$.

A further property of the discriminant is the following:

$$\Delta = a^{2} \left(\right. x_{1} - x_{2} \left.\right)^{2}$$

This identity shows directly that $\Delta \geq 0$ when the roots are real, and that
$\Delta = 0$ if and only if the two roots coincide.

###### When the discriminant is negative, the solutions are complex. The dedicated entry on [quadratic equations with complex solutions](https://algebrica.org/quadratic-equations-with-complex-solutions/) covers this case in full.

## Factoring

A quadratic equation can be [factored](https://algebrica.org/factoring-quadratic-equations/) into the following form:

$$a x^{2} + b x + c = 0 \Longleftrightarrow a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right) = 0$$

where $x_{1}$ and $x_{2}$ are the roots of the equation. By [Vieta’s formulas](https://algebrica.org/trinomials/), the roots satisfy the following relations:

$$x_{1} + x_{2} = - \frac{b}{a}$$
$$x_{1} \cdot x_{2} = \frac{c}{a}$$

This method is effective when the roots can be identified by inspection or by simple
trial, but becomes impractical for equations with irrational or complex roots, where the [quadratic formula](https://algebrica.org/quadratic-formula/) is preferable.

## How to solve a quadratic equation

- Rewrite the equation in standard form: $a x^{2} + b x + c = 0$.
- Calculate the discriminant: $\Delta = b^{2} - 4 a c$.
- Use the quadratic formula:
   $$x = \frac{- b \pm \sqrt{\Delta}}{2 a}$$
- Simplify the result.
- If $\Delta \geq 0$, the solutions are real; if $\Delta < 0$, the solutions are complex conjugates.

## Quadratic equations with parameters

A natural extension of the study of quadratic equations is to consider the case in which the coefficients are not fixed numbers but depend on an external parameter. In this setting we speak of [quadratic equations with a parameter](https://algebrica.org/quadratic-equations-with-parameters/),
also called literal quadratic equations, which take the form:

$$a \left(\right. k \left.\right) x^{2} + b \left(\right. k \left.\right) x + c \left(\right. k \left.\right) = 0 , a \left(\right. k \left.\right) \neq 0$$

Varying the parameter $k$ alters the equation and, consequently, the nature of its solutions. The analysis relies on the discriminant:

$$\Delta \left(\right. k \left.\right) = b \left(\right. k \left.\right)^{2} - 4 a \left(\right. k \left.\right) c \left(\right. k \left.\right)$$

which, exactly as in the classical case, determines whether the equation admits two
distinct real solutions, a repeated solution, or a pair of complex conjugate solutions.

## Exercises

- $$\text{1}. x^{2} = 5 x - 6$$ [solution](https://algebrica.org/exercises/quadratic-equation-e-1)
- $$\text{2}. \frac{1}{2} x^{2} + \frac{\sqrt{3}}{2} x + \frac{5}{8} = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-2)
- $$\text{3}. - 7 x + 3 = - 2 x^{2}$$ [solution](https://algebrica.org/tests/quadratic-equation-a-3)
- $$\text{4}. x^{2} - 5 x - 14 = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-4)
- $$\text{5}. 2 x^{2} + 10 x + 11 = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-5)
- $$\text{6}. \left(\right. x - 4 \left.\right)^{2} - 9 = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-6/)
- $$\text{7}. \left(\right. 4 x + 8 \left.\right) \left(\right. \frac{1}{2} x - 6 \left.\right) = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-7)
- $$\text{8}. x^{2} + 0.4 x - 0.16 = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-8)
- $$\text{9}. 7 x^{2} + x + 5 = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-9)
- $$\text{10}. 9 x^{2} - 5 = 0$$ [solution](https://algebrica.org/tests/quadratic-equation-a-10)

###### Some equations are already in standard form, others require preliminary algebraic manipulation before a method can be applied. Try solving them independently before consulting the solutions.

## Selected references

- **Stony Brook University**. [Factoring Quadratic Polynomials](https://www.math.stonybrook.edu/Videos/MAP103Online/Handouts/Lecture-28-Handout.pdf)
- **MIT, H. Mui**. [Vieta’s Formulae](https://www.mit.edu/~hsmui/files/handouts/mathcircle/vieta.pdf)
- **University of Oklahoma, M. Zhu**. [Solving Quadratic Equations](https://math.ou.edu/~mzhu/Algebra/Solving%20quadratic%20equations-3.pdf)
