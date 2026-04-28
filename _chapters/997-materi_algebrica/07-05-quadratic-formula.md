---
layout: chapter
title: "Quadratic Formula"
chapter: "Equations"
chapter_order: 7
section_order: 5
permalink: /materi-algebrica/equations/quadratic-formula/
---

## Definition

Given a [quadratic equation](https://algebrica.org/quadratic-equations/) in standard form $a x^{2} + b x + c = 0$, the quadratic formula provides an explicit expression for its roots in terms of the coefficients $a$, $b$, and $c$:

$$x_{1 , 2} = \frac{- b \pm \sqrt{b^{2} - 4 a c}}{2 a}$$

The formula is derived by applying the method of [completing the square](https://algebrica.org/completing-the-square/) to the general standard form, and constitutes one of the central results of algebra. It is universally applicable to any quadratic equation with real or complex coefficients, provided that $a \neq 0$.

- $a , b , c$ are the coefficients of the equation, with $a \neq 0$.
- The plus-minus symbol reflects the fact that the formula yields two values, corresponding to the two roots of the polynomial.
- By the [Fundamental Theorem of Algebra](https://algebrica.org/roots-of-a-polynomial/), a polynomial of degree 2 has exactly two roots in $\mathbb{C}$, counted with multiplicity. These may be two distinct real numbers, a repeated real root, or a pair of complex conjugates depending on the sign of the discriminant.

The quadratic formula is valid only when square roots can be computed. When the coefficients are [real](https://algebrica.org/properties-of-real-numbers/), the formula always yields solutions in $\mathbb{C}$, since every complex number has a square root in $\mathbb{C}$. This guarantees that no quadratic equation is ever without solutions, provided one works in the right setting.

> The quadratic formula also provides a natural framework for studying how the roots vary when the coefficients depend on a parameter. In that setting, the discriminant becomes a function of the parameter itself, and its sign determines how the nature of the roots changes as the parameter varies. This analysis is developed in detail in the dedicated entry on [quadratic equations with parameters](https://algebrica.org/quadratic-equations-with-parameters/).

## Discriminant

The term within the square root, $\Delta = b^{2} - 4 a c$, is known as the discriminant, and it is crucial in determining the nature and number of solutions of a quadratic equation.

If $\Delta > 0$, the quadratic equation has two distinct real solutions. $$S = \left{\right. x_{1} , x_{2} \left.\right} x_{1} , x_{2} \in \mathbb{R} x_{1} \neq x_{2}$$ $$x_{1 , 2} = \frac{- b \pm \sqrt{b^{2} - 4 a c}}{2 a}$$

---

If $\Delta = 0$, the quadratic equation has two coincident real solutions. $$S = \left{\right. x \left.\right} x \in \mathbb{R} x = x_{1} = x_{2}$$ $$x = - \frac{b}{2 a}$$

---

If $\Delta < 0$, the quadratic equation has no real solutions. Instead, it gives rise to a pair of complex conjugate solutions with nonzero imaginary part. $$∄ x \in \mathbb{R}$$ $$x_{1 , 2} = \frac{- b \pm i \sqrt{4 a c - b^{2}}}{2 a}$$
A detailed treatment of this case is presented in the entry on [quadratic equations with complex solutions](https://algebrica.org/quadratic-equations-with-complex-solutions/).

---

The discriminant $\Delta = b^{2} - 4 a c$ also determines how the graph of the quadratic function $f \left(\right. x \left.\right) = a x^{2} + b x + c$ behaves with respect to the x-axis. Geometrically, a quadratic equation represents a [parabola](https://algebrica.org/parabola). Consider for example the following equation $y = x^{2} + 4 x + 4$:

![](https://algebrica.org/wp-content/uploads/resources/images/quadr-formula-parabola.png "Quadratic formula.")

In general we have:

- If $\Delta > 0$, the graph of the parabola intersects the x-axis at two distinct points.
- if $\Delta = 0$, the graph of the parabola is tangent to the x-axis at a single point (the vertex).
- if $\Delta < 0$, the graph of the parabola does not intersect the $x$-axis at all.

## Vieta’s formulas

For a quadratic equation $a x^{2} + b x + c = 0$ with roots $x_{1}$ and $x_{2}$, the sum and product of the roots are given by:

$$x_{1} + x_{2} = - \frac{b}{a} x_{1} \cdot x_{2} = \frac{c}{a}$$

These relations hold in $\mathbb{C}$ for any value of the discriminant, and follow directly from expanding the factored form $a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$ and comparing coefficients. Their derivation and applications, including the role they play in factoring higher-degree polynomials, are discussed in detail in the entry on [trinomial equations](https://algebrica.org/trinomial-equations/).

## Example 1

Solve the equation $x^{2} - 4 x + 2 = 0$ using the quadratic formula. The equation is already in standard form, with $a = 1$, $b = - 4$, and $c = 2$. Substituting into the formula:

$$x_{1 , 2} & = \frac{- \left(\right. - 4 \left.\right) \pm \sqrt{\left(\right. - 4 \left.\right)^{2} - 4 \left(\right. 1 \left.\right) \left(\right. 2 \left.\right)}}{2 \left(\right. 1 \left.\right)} \\ & = \frac{4 \pm \sqrt{16 - 8}}{2} \\ & = \frac{4 \pm \sqrt{8}}{2}$$

Since $\Delta = 8 > 0$, the equation has two distinct real solutions. Simplifying $\sqrt{8} = 2 \sqrt{2}$ we obtain:

$$x_{1 , 2} = \frac{4 \pm 2 \sqrt{2}}{2} = 2 \pm \sqrt{2}$$

The solutions are therefore:
$$x_{1} = 2 - \sqrt{2}$$
$$x_{2} = 2 + \sqrt{2}$$

fundamental theoremmultiplicitytwo rootsproduct of rootssum of rootsvieta formulasparabola intersectioncomplex rootsdouble rootreal rootsnegative casezero casepositive caseleading coefficientstandard formsolution formulacompleting squarecoefficients a b cquadratic formrelationsdiscriminantstructure
