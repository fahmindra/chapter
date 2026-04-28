---
layout: chapter
title: "Hyperbolic Sine and Cosine"
chapter: "Trigonometry"
chapter_order: 5
section_order: 7
permalink: /materi-algebrica/trigonometry/hyperbolic-sine-and-cosine/
---

## Introduction to hyperbolic sine and cosine

We have seen that the [sine](https://algebrica.org/sine-and-cosine/) of an angle can be introduced geometrically by looking at how a point moves along the [unit circle](https://algebrica.org/unit-circle/). The hyperbolic sine, instead, is obtained by relating a point on the right branch of the equilateral [hyperbola](https://algebrica.org/hyperbola/):

$$X^{2} - Y^{2} = 1$$

to the area of a corresponding hyperbolic sector. For any real value $x$, we select a point:

$$P \left(\right. X_{P} , Y_{P} \left.\right)$$

on the branch with $X > 0$ such that the signed area enclosed by the $O X$ axis, the segment from the origin to $P$, and the portion of the hyperbola between $\left(\right. 1 , 0 \left.\right)$ and $P$ is equal to $x / 2$.

![Hyperbolic sine.](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-sine.png "Hyperbolic sine.")

The notion of signed area makes it possible to accommodate both positive and negative values in a continuous way: when $x > 0$ the sector lies in the first quadrant, while for $x < 0$ it extends into the fourth quadrant, without breaking the correspondence between the parameter $x$ and the position of $P$. Once this point has been determined, the hyperbolic sine of $x$ is simply its vertical coordinate:

$$sinh ⁡ \left(\right. x \left.\right) := Y_{P}$$

Specularly to what has just been shown for the hyperbolic sine, we can introduce the hyperbolic cosine by looking at the same equilateral hyperbola. Once the point:
$$P \left(\right. X_{P} , Y_{P} \left.\right)$$
has been identified as the one corresponding to a signed hyperbolic sector of area $x / 2$, the hyperbolic cosine of $x$ is defined simply as its horizontal coordinate.

![Hyperbolic cosine.](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-cosine.png "Hyperbolic cosine.")

While $sinh ⁡ \left(\right. x \left.\right)$ reflects how far the point rises or falls along the branch of the hyperbola, $cosh ⁡ \left(\right. x \left.\right)$ captures its horizontal position:

$$cosh ⁡ \left(\right. x \left.\right) := X_{P}$$

In this geometric interpretation, the pair $\left(\right. cosh ⁡ \left(\right. x \left.\right) , sinh ⁡ \left(\right. x \left.\right) \left.\right)$ represents the coordinates of the unique point $P$ that produces the assigned sector $A$.

## Fundamental hyperbolic identity

The hyperbolic sine and hyperbolic cosine satisfy a relationship that plays a role analogous to the [Pythagorean identity](https://algebrica.org/pythagorean-identity/). This relationship is known as the fundamental hyperbolic identity:

$$cosh^{2} ⁡ x - sinh^{2} ⁡ x = 1$$

From a geometric point of view, this equality expresses the fact that the point $\left(\right. cosh ⁡ \left(\right. x \left.\right) , sinh ⁡ \left(\right. x \left.\right) \left.\right)$ lies exactly on the right branch of the equilateral hyperbola:

$$X^{2} - Y^{2} = 1$$

Here the horizontal coordinate $cosh ⁡ \left(\right. x \left.\right)$ and the vertical coordinate $sinh ⁡ \left(\right. x \left.\right)$ play roles similar to those of the adjacent and opposite sides in the unit-circle setting, but the geometry is governed by a hyperbola instead of a circle. The identity emerges from this construction: the coordinates of the point must satisfy the defining equation of the hyperbola, and this is precisely what leads to $cosh^{2} ⁡ x - sinh^{2} ⁡ x = 1$.

## Hyperbolic identities

- $$\text{1}. sinh ⁡ \left(\right. 2 x \left.\right) = 2 sinh ⁡ \left(\right. x \left.\right) cosh ⁡ \left(\right. x \left.\right)$$
- $$\text{2}. cosh ⁡ \left(\right. 2 x \left.\right) = 1 + 2 sinh^{2} ⁡ \left(\right. x \left.\right)$$
- $$\text{3}. sinh ⁡ \left(\right. x + y \left.\right) = sinh ⁡ \left(\right. x \left.\right) cosh ⁡ \left(\right. y \left.\right) + cosh ⁡ \left(\right. x \left.\right) sinh ⁡ \left(\right. y \left.\right)$$
- $$\text{4}. cosh ⁡ \left(\right. x + y \left.\right) = cosh ⁡ \left(\right. x \left.\right) cosh ⁡ \left(\right. y \left.\right) + sinh ⁡ \left(\right. x \left.\right) sinh ⁡ \left(\right. y \left.\right)$$
- $$\text{5}. sinh ⁡ \left(\right. x - y \left.\right) = sinh ⁡ \left(\right. x \left.\right) cosh ⁡ \left(\right. y \left.\right) - cosh ⁡ \left(\right. x \left.\right) sinh ⁡ \left(\right. y \left.\right)$$
- $$\text{6}. cosh ⁡ \left(\right. x - y \left.\right) = cosh ⁡ \left(\right. x \left.\right) cosh ⁡ \left(\right. y \left.\right) - sinh ⁡ \left(\right. x \left.\right) sinh ⁡ \left(\right. y \left.\right)$$

> Each identity reflects the deep algebraic symmetry of the hyperbolic functions. Their addition and double-angle formulas closely parallel the circular case, but follow the geometry of the equilateral hyperbola, where $cosh ⁡ \left(\right. x \left.\right)$ and $sinh ⁡ \left(\right. x \left.\right)$ arise as the coordinates of the point associated with a hyperbolic sector.

## Analytical expression of the hyperbolic sine

A first derivation comes directly from the [exponential function](https://algebrica.org/exponential-function/). If we look at how $e^{x}$ and $e^{- x}$ behave, we notice that they naturally split into a symmetric and an antisymmetric part. Writing them as:

$$e^{x} = cosh ⁡ \left(\right. x \left.\right) + sinh ⁡ \left(\right. x \left.\right)$$
$$e^{- x} = cosh ⁡ \left(\right. x \left.\right) - sinh ⁡ \left(\right. x \left.\right)$$

we can treat these two expressions as a simple system in the unknowns $cosh ⁡ \left(\right. x \left.\right)$ and $sinh ⁡ \left(\right. x \left.\right)$. Subtracting one equation from the other isolates the antisymmetric component, giving:

$$e^{x} - e^{- x} = 2 sinh ⁡ \left(\right. x \left.\right)$$

and therefore:

$$sinh ⁡ \left(\right. x \left.\right) = \frac{e^{x} - e^{- x}}{2}$$

---

A complementary way to obtain the same formula is to go back to geometry. The point $\left(\right. cosh ⁡ \left(\right. x \left.\right) , sinh ⁡ \left(\right. x \left.\right) \left.\right)$ belongs to the equilateral hyperbola:

$$X^{2} - Y^{2} = 1$$

Since we already know that the horizontal coordinate satisfies:

$$X = cosh ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{2}$$

we can plug this expression directly into the hyperbola’s equation and solve for $Y$. We have:

$$Y^{2} = X^{2} - 1 = \left(\left(\right. \frac{e^{x} + e^{- x}}{2} \left.\right)\right)^{2} - 1$$

Expanding the square and simplifying leads to:

$$Y^{2} = \left(\left(\right. \frac{e^{x} - e^{- x}}{2} \left.\right)\right)^{2}$$

Taking the square root requires paying attention to the sign of $Y$.

- If $x > 0$, the point lies in the first quadrant and $Y$ is positive.
- If $x < 0$, it lies in the fourth quadrant and $Y$ is negative.

In both cases, the correct choice is:
$$Y = \frac{e^{x} - e^{- x}}{2}$$

Thus the analytical expression emerges naturally from the geometry of the hyperbola:

$$sinh ⁡ \left(\right. x \left.\right) = \frac{e^{x} - e^{- x}}{2}$$

## Analytical expression of the hyperbolic cosine

Compared to the derivation of the hyperbolic sine, there is another way to obtain the analytical expression of the hyperbolic cosine, and it emerges directly from the classical geometric construction. In this approach, we start from the computation of the signed area $A$ of the hyperbolic sector on the right branch of the equilateral hyperbola. The integral that describes this area leads to the relation:

$$A = \frac{1}{2} ln \left(\right. X + \sqrt{X^{2} - 1} \left.\right)$$

This motivates the introduction of the hyperbolic parameter $x$, which is defined so that it depends only on the horizontal coordinate $X$:

$$x = ln \left(\right. X + \sqrt{X^{2} - 1} \left.\right) = 2 A$$

Once this link between the sector area and the coordinate $X$ has been established, we can reverse the relation to express (X) in terms of (x). Exponentiating gives:

$$X + \sqrt{X^{2} - 1} = e^{x}$$

and from here we isolate the square root:

$$\sqrt{X^{2} - 1} = e^{x} - X$$

Squaring both sides and simplifying the resulting expression shows that the admissible solution must satisfy:

$$X = \frac{e^{x} + e^{- x}}{2}$$

This value is therefore taken as the analytical definition of the hyperbolic cosine:

$$cosh ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{2}$$

## Analytical hyperbolic definitions

- $$\text{1}. sinh ⁡ \left(\right. x \left.\right) = \frac{e^{x} - e^{- x}}{2}$$
- $$\text{2}. cosh ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{2}$$

> These analytic definitions express the hyperbolic sine and cosine directly in terms of the [exponential function](https://algebrica.org/exponential-function/). Their symmetry follows from the structure of the equilateral hyperbola.

## Hyperbolic sine and cosine function

The hyperbolic sine function $f \left(\right. x \left.\right) = sinh ⁡ \left(\right. x \left.\right)$ associates each [real number](https://algebrica.org/types-of-numbers/) $x$ with a value derived from the exponential function. Unlike the circular sine, it does not oscillate: its graph grows exponentially for large positive or negative values of $x$, crossing the origin with slope $1$. The function $f \left(\right. x \left.\right) = sinh ⁡ \left(\right. x \left.\right)$ is defined for all real numbers, and its range also spans the entire real line.

![](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-sine-function.png "Hyperbolic sine function chart.")

- Domain: $x \in \mathbb{R}$
- Range: $y \in \mathbb{R}$
- Periodicity: not periodic; grows exponentially as $\left|\right. x \left|\right.$ increases
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $sinh ⁡ \left(\right. - x \left.\right) = - sinh ⁡ \left(\right. x \left.\right)$

---

The hyperbolic cosine function $f \left(\right. x \left.\right) = cosh ⁡ \left(\right. x \left.\right)$ assigns to each real number $x$ a value obtained from the symmetric part of the exponential function. Unlike the circular cosine, it is not periodic: its graph has a minimum at $x = 0$, where $cosh ⁡ \left(\right. 0 \left.\right) = 1$, and increases exponentially as the [absolute value](https://algebrica.org/absolute-value/) of $x$ becomes larger. The function $f \left(\right. x \left.\right) = cosh ⁡ \left(\right. x \left.\right)$ is defined for all real numbers, and its range is given by $cosh ⁡ \left(\right. x \left.\right) \geq 1$.

![](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-cosine-function.png "Hyperbolic cosine function chart.")

- Domain: $x \in \mathbb{R}$
- Range: $y \in \mathbb{R} : y \geq 1$
- Periodicity: not periodic; grows exponentially as $\left|\right. x \left|\right.$ increases
- Parity: [even](https://algebrica.org/even-and-odd-functions/), $cosh ⁡ \left(\right. - x \left.\right) = cosh ⁡ \left(\right. x \left.\right)$

## Relation to the circular sine and cosine

Hyperbolic sine and cosine originate from the geometry of the equilateral hyperbola:
$$x^{2} - y^{2} = 1$$
where a hyperbolic sector determines a parameter $x$. The point on the hyperbola associated with this area has coordinates:

$$X_{P} = cosh ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{2}$$
$$Y_{P} = sinh ⁡ \left(\right. x \left.\right) = \frac{e^{x} - e^{- x}}{2}$$

In the circular setting, the corresponding quantities arise from the [unit circle](https://algebrica.org/unit-circle/) of radius $1$, where a central angle $\theta$ determines the circular [sine and cosine](https://algebrica.org/sine-and-cosine/), identified by the point:
$$P \left(\right. X_{P} , Y_{P} \left.\right) = P \left(\right. cos ⁡ \theta , sin ⁡ \theta \left.\right)$$

> Both constructions follow the same basic idea: whether on a circle or on a hyperbola, a sector picks out a point on the curve. In the circular case this leads to the familiar sine and cosine, while in the hyperbolic case it gives the hyperbolic sine and cosine, which mirror the circular behaviour but within the geometry of the hyperbola.

graph behaviorderivationcosh formulasinh formulaexp definitionnon periodicdomain rangemonotonicityparitydouble angleaddition formulasfundamental identityhyperbolageometric modelhyperbolic definitionanalytic formspropertiesfoundations
