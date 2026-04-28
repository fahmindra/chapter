---
layout: chapter
title: "Quadratic Equations with Parameters"
chapter: "Equations"
chapter_order: 7
section_order: 22
permalink: /materi-algebrica/equations/quadratic-equations-with-parameters/
---

parameter inequalityvieta relationproduct of rootscomplex rootsdouble roottwo real rootsparameter variationroot behaviordouble rootcomplex rootsreal rootsparameter intervalssign analysisdiscriminantstandard formleading coefficientparabola modelparameter conditionparameter coefficientsquadratic formpropertiesanalysisstructure

## Definition

[Quadratic equations](https://algebrica.org/quadratic-equations/) are usually introduced in their classical form, where all coefficients are fixed real numbers. The standard expression serves as the basic model for every second-degree equation:
$$a x^{2} + b x + c = 0$$

The key ideas behind quadratic equations are closely linked to the geometry of the [parabola](https://algebrica.org/parabola/) and to the behaviour of the [discriminant](https://algebrica.org/quadratic-formula/). These elements determine how the graph bends, where its vertex lies, and whether the equation has two real solutions, a repeated solution, or a pair of [complex roots](https://algebrica.org/quadratic-equations-with-complex-solutions/).

![](https://algebrica.org/wp-content/uploads/resources/images/quadratic-equations-params-6.png "Graph of a parabola defined by a quadratic equation.")

In many situations, however, the coefficients are not constant but depend on an external quantity that we treat as a parameter. Instead of being fixed, the numbers $a$, $b$, and $c$ become functions of a real parameter $k$. A parametrised quadratic equation can therefore be written in the more general form:

$$a \left(\right. k \left.\right) x^{2} + b \left(\right. k \left.\right) x + c \left(\right. k \left.\right) = 0$$
$$a \left(\right. k \left.\right) \neq 0$$

The condition $a \left(\right. k \left.\right) \neq 0$ prevents the equation from collapsing into a [linear equation with parameters](https://algebrica.org/linear-equations-with-parameters/) when the parameter varies, ensuring that it retains the structure of a quadratic for all admissible values of $k$.

###### This page focuses on the quadratic case. For a broader discussion of parametric equations across different degrees, see [equations with parameters](https://algebrica.org/equations-with-parameters/).

## The role of the discriminant

The discriminant allows to understand how the solutions of a quadratic equation behave. When the coefficients depend on a parameter, this idea remains the same, but the discriminant itself becomes a function of that parameter. Starting from the coefficients $a \left(\right. k \left.\right)$, $b \left(\right. k \left.\right)$, and $c \left(\right. k \left.\right)$, we obtain:

$$\Delta \left(\right. k \left.\right) = b \left(\right. k \left.\right)^{2} - 4 a \left(\right. k \left.\right) c \left(\right. k \left.\right)$$

Once written in this form, the discriminant gives a picture of what happens to the roots for each value of $k$. Its sign tells us everything we need:

- When $\Delta \left(\right. k \left.\right) > 0$, the equation has two distinct real solutions.
- When $\Delta \left(\right. k \left.\right) = 0$, the equation has one real solution that appears as a double root.
- When $\Delta \left(\right. k \left.\right) < 0$, the equation has two [complex conjugate solutions](https://algebrica.org/quadratic-equations-with-complex-solutions/).

## Example 1

Let us begin with a very simple case and look at the quadratic equation:
$$x^{2} + k x + 1 = 0$$

This example is useful because each coefficient depends on the parameter $k$ in a straightforward way:

$$a \left(\right. k \left.\right) = 1 b \left(\right. k \left.\right) = k c \left(\right. k \left.\right) = 1$$

Before analysing the roots, it is useful to recall how the discriminant is defined in the general case. For a quadratic equation in the standard form the discriminant is:

$$\Delta = b^{2} - 4 a c$$

and its sign determines the nature of the solutions. We now examine how the discriminant changes when the coefficients depend on the parameter $k$. By substituting $a \left(\right. k \left.\right)$, $b \left(\right. k \left.\right)$, and $c \left(\right. k \left.\right)$ into the same formula, we obtain:

$$\Delta \left(\right. k \left.\right) = b \left(\right. k \left.\right)^{2} - 4 a \left(\right. k \left.\right) c \left(\right. k \left.\right)$$

The expression simplifies to:

$$\Delta \left(\right. k \left.\right) = k^{2} - 4$$

To understand when real solutions exist, we study the [quadratic inequality](https://algebrica.org/quadratic-inequalities/):

$$k^{2} - 4 \geq 0$$

Solving it yields two separate intervals:

$$k \leq - 2 \text{or} k \geq 2$$

For these values of the parameter, the discriminant is positive and the quadratic has two distinct real roots. At the boundary points $k = \pm 2$, the discriminant becomes zero and the equation collapses to a single repeated solution. When:

$$- 2 < k < 2$$

the discriminant is negative, and the equation no longer has real roots. Instead, it produces a pair of complex conjugate solutions. The following table summarises the [sign analysis](https://algebrica.org/sign-analysis-in-inequalities/) of the expressions $k - 2$, $k + 2$, and their product, highlighting how the sign changes across the three intervals determined by the critical points $k = - 2$ and (k = 2).

|  |  | $$- 2$$ | $$2$$ |
| --- | --- | --- | --- |
| $k - 2 > 0$ | $-$ | $-$ | $+$ |
| $k + 2 > 0$ | $-$ | $+$ | $+$ |
| $\left(\right. k - 2 \left.\right) \left(\right. k + 2 \left.\right) > 0$ | $+$ | $-$ | $+$ |

---

Whenever the roots turn out to be real, it is useful to have an explicit expression for them.
 By applying the quadratic formula to this particular family, the two real solutions can be written in closed form as

$$x = \frac{- k \pm \sqrt{k^{2} - 4}}{2}$$

This expression shows directly how each root depends on the parameter $k$ and makes it possible to study how the solutions move along the real line as $k$ varies.

From the analysis above, the final outcomes are:

- If $k < - 2$ or $k > 2$, the equation has two real and distinct solutions.
- If $k = \pm 2$, there is one real double solution.
- If $- 2 < k < 2$, the equation has two complex conjugate solutions.

## Geometric interpretation of parameter changes

Making reference to the quadratic equation used in example 1, it is also helpful to look at how the graph of the corresponding parabola changes as the parameter $k$ varies. To each value of $k$ we can associate the [parabola](https://algebrica.org/parabola/):

$$y = x^{2} + k x + 1$$

so analysing the roots is equivalent to studying where this curve intersects the x-axis. As the parameter moves, the entire family of parabolas shifts in a smooth and predictable way. One way to describe this evolution is to examine what happens in three key regimes of the parameter.

---

When $\left|\right. k \left|\right.$ becomes very large ($k \rightarrow + \infty$ or $k \rightarrow - \infty$), the linear term $k x$ dominates the expression and the two roots separate widely. A simple [asymptotic](https://algebrica.org/asymptotes/) argument shows that one root tends to $0$, while the other behaves approximately like $- k$. Geometrically, this means that the intersection points move far apart: one stays close to the origin, while the other drifts further and further along the negative axis. The parabola becomes increasingly tilted in appearance.

---

At the critical values $k = \pm 2$, the discriminant becomes zero. This corresponds to the moment when the parabola touches the x-axis at exactly one point. In these cases the graph has a single point of tangency, the equation has one repeated root, and the vertex lies precisely on the axis.

---

Within the interval $- 2 < k < 2$, the discriminant is negative, so the equation has no real solutions. From a geometric perspective, this means that the parabola does not intersect the x-axis at all. Because the leading coefficient is positive, the parabola always opens upward, and in this parameter region the vertex lies strictly above the x-axis. As a result, the entire curve stays on one side of the axis, reflecting the fact that the solutions move into the complex plane.

## Example 2

Let us now consider a slightly more elaborate example than the previous one. We look at the parameter-dependent quadratic equation:

$$\left(\right. a + 2 \left.\right) x^{2} + \left(\right. 3 a - 1 \left.\right) x + \left(\right. a - 4 \left.\right) = 0 a \neq - 2$$

where the condition $a \neq - 2$ ensures that the coefficient of $x^{2}$ does not vanish, so the expression remains a genuine quadratic equation for every admissible value of the parameter. Our goal is to determine for which values of $a$ the equation admits two distinct real solutions. As usual, this depends on the sign of the [discriminant](https://algebrica.org/quadratic-formula/). To avoid confusion with the parameter $a$, we denote the coefficients of the present quadratic by $A$, $B$, $C$, so that the general formula reads:

$$\Delta = B^{2} - 4 A C$$

We substitute the coefficients of the present quadratic equation and obtain:

$$\Delta \left(\right. a \left.\right) = \left(\right. 3 a - 1 \left.\right)^{2} - 4 \left(\right. a + 2 \left.\right) \left(\right. a - 4 \left.\right)$$

---

Expanding the two parts with only the essential intermediate steps, we first compute the square:

$$\left(\right. 3 a - 1 \left.\right)^{2} = 9 a^{2} - 6 a + 1$$

Then the product involving the quadratic and constant coefficients:

$$\left(\right. a + 2 \left.\right) \left(\right. a - 4 \left.\right) = a^{2} - 2 a - 8$$

Inserting these expressions back into the discriminant and collecting like terms leads to the simplified form

$$\Delta \left(\right. a \left.\right) = 5 a^{2} + 2 a + 33$$

---

This is a quadratic function of $a$ with positive leading coefficient. To understand whether it can ever be zero or negative, we examine its discriminant:

$$2^{2} - 4 \cdot 5 \cdot 33 = 4 - 660 < 0$$

Since this value is negative, the parabola associated with (5a^{2} + 2a + 33) never intersects the horizontal axis: it remains strictly positive for all real values of $a$. Therefore:

$$\Delta \left(\right. a \left.\right) > 0 \forall a \in \mathbb{R}$$

The equation has two real and distinct solutions for every real value of the parameter $a$, except for $a = - 2$, which must be excluded because it would make the coefficient of $x^{2}$ vanish and reduce the expression to a first-degree equation.

## Example 3

Consider the parameter-dependent quadratic equation:

$$x^{2} - \left(\right. a - 4 \left.\right) x + \left(\right. a^{2} - a \left.\right) = 0$$

where $a$ is a real parameter. We want to determine the values of $a$ for which the product of the two solutions is strictly less than $2$. For a general quadratic equation of the form:

$$x^{2} + b x + c = 0$$

the product of the solutions satisfies the identity $x_{1} x_{2} = c$.

###### This identity follows from the [factorised form](https://algebrica.org/factoring-quadratic-equations/) of a monic quadratic, where $x^{2} + b x + c = \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$. By expanding the product, the constant term appears as $x_{1} x_{2}$, which explains why the product of the solutions is equal to $c$.

---

In this case the constant term is $c = a^{2} - a$, and requiring the product of the two solutions to be less than $2$ translates into the inequality:

$$a^{2} - a < 2$$

Bringing all the terms to the left gives the inequality:

$$a^{2} - a - 2 < 0$$

The quadratic [polynomial](https://algebrica.org/polynomials/) on the left factors as

$$a^{2} - a - 2 = \left(\right. a - 2 \left.\right) \left(\right. a + 1 \left.\right)$$

The critical points are therefore (a = -1) and (a = 2). To determine where the expression is negative, we analyse the signs of the two factors.

|  |  | $$- 1$$ | $$2$$ |
| --- | --- | --- | --- |
| $a - 2 > 0$ | $-$ | $-$ | $+$ |
| $a + 1 > 0$ | $-$ | $+$ | $+$ |
| $\left(\right. a - 2 \left.\right) \left(\right. a + 1 \left.\right) < 0$ | $+$ | $-$ | $+$ |

---

The sign chart shows that $\left(\right. a - 2 \left.\right) \left(\right. a + 1 \left.\right) < 0$ when the parameter lies between the two roots:

$$- 1 < a < 2$$

The product of the solutions satisfies $x_{1} x_{2} < 2$ if and only if $- 1 < a < 2.$
