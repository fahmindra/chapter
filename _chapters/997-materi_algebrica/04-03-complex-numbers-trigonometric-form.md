---
layout: chapter
title: "Complex Numbers in Trigonometric Form"
chapter: "Complex Numbers"
chapter_order: 4
section_order: 3
permalink: /materi-algebrica/complex-numbers/complex-numbers-in-trigonometric-form/
---

## Definition

The [algebraic form](https://algebrica.org/complex-numbers-introduction) $z = a + b i$ represents a complex number through its real and imaginary components directly. Every nonzero complex number can also be described by two geometric quantities, its distance from the origin and its angular position in the complex plane. This leads to the trigonometric form of a complex number:

$$z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$$

- $r = \left|\right. z \left|\right. = \sqrt{a^{2} + b^{2}}$ is the modulus, representing the distance of $z$ from the origin in the complex plane.
- $\theta = arg ⁡ \left(\right. z \left.\right)$ is the argument, the angle in radians between the positive real axis and the [vector](https://algebrica.org/vectors/) representing $z$.

![](https://algebrica.org/wp-content/uploads/resources/images/trig-form-1.png)

Since the point $z = \left(\right. a , b \left.\right)$ lies in the complex plane at distance $r$ from the origin, and $\theta$ is the angle it forms with the positive real axis, the real and imaginary components can be expressed through the definitions of [sine](https://algebrica.org/sine-and-cosine) and [cosine](https://algebrica.org/sine-and-cosine) in a right triangle. The projections onto the two axes are the following.

$$\overset{―}{O A} = \overset{―}{O P} \cdot cos ⁡ \left(\right. \theta \left.\right) = r cos ⁡ \left(\right. \theta \left.\right)$$
$$\overset{―}{O B} = \overset{―}{O P} \cdot sin ⁡ \left(\right. \theta \left.\right) = r sin ⁡ \left(\right. \theta \left.\right)$$

That is, $a = r cos ⁡ \left(\right. \theta \left.\right)$ and $b = r sin ⁡ \left(\right. \theta \left.\right)$. Substituting these into the algebraic form of a complex number yields its trigonometric representation.

$$z = \left(\right. a , b \left.\right) & = a + i b \\ & = r cos ⁡ \left(\right. \theta \left.\right) + i r sin ⁡ \left(\right. \theta \left.\right) \\ & = r \left[\right. cos ⁡ \left(\right. \theta \left.\right) + i sin ⁡ \left(\right. \theta \left.\right) \left]\right.$$

---

The complex conjugate $\bar{z}$ of a complex number $z$ in trigonometric form is obtained by replacing $\theta$ with $- \theta$, which corresponds geometrically to reflecting $z$ across the real axis. Since cosine is an even function and sine is odd, the result takes the following form.

$$\bar{z} = r \left(\right. cos ⁡ \theta - i sin ⁡ \theta \left.\right)$$

> See also how to express a complex number in its [exponential form](https://algebrica.org/complex-numbers-exponential-form).

## Operations

Given two complex numbers in trigonometric form:

$$z_{1} = r_{1} \left[\right. cos ⁡ \left(\right. \theta_{1} \left.\right) + i sin ⁡ \left(\right. \theta_{1} \left.\right) \left]\right.$$
$$z_{2} = r_{2} \left[\right. cos ⁡ \left(\right. \theta_{2} \left.\right) + i sin ⁡ \left(\right. \theta_{2} \left.\right) \left]\right.$$

their product is another complex number whose modulus is the product of the moduli and whose argument is the sum of the arguments. The multiplication formula is the following.

$$z_{1} z_{2} = r_{1} r_{2} \left[\right. cos ⁡ \left(\right. \theta_{1} + \theta_{2} \left.\right) + i sin ⁡ \left(\right. \theta_{1} + \theta_{2} \left.\right) \left]\right.$$

Geometrically, [multiplying two complex numbers](https://algebrica.org/complex-number-operations/) corresponds to scaling their distances from the origin by the product of their moduli and rotating the result by the sum of their arguments, combining a dilation and a rotation in a single operation.

> This interpretation extends naturally to integer powers through [De Moivre’s theorem](https://algebrica.org/de-moivre-theorem/).

---

The quotient of two complex numbers in trigonometric form, defined for $z_{2} \neq 0$, follows a symmetric rule: the modulus of the result is the ratio of the moduli, and the argument is the difference of the arguments.

$$\frac{z_{1}}{z_{2}} = \frac{r_{1}}{r_{2}} \left[\right. cos ⁡ \left(\right. \theta_{1} - \theta_{2} \left.\right) + i sin ⁡ \left(\right. \theta_{1} - \theta_{2} \left.\right) \left]\right.$$

---

Addition does not admit a comparably compact formula. The most direct approach is to convert both numbers to algebraic form, add their real and imaginary parts separately, and then convert the result back to trigonometric form if needed. The real and imaginary parts of the sum are the following.

$$x = r_{1} cos ⁡ \theta_{1} + r_{2} cos ⁡ \theta_{2}$$
$$y = r_{1} sin ⁡ \theta_{1} + r_{2} sin ⁡ \theta_{2}$$

The sum $z_{1} + z_{2}$ is then expressed in algebraic form as $x + i y$. To recover the trigonometric form, one computes the modulus and the argument of the result. The modulus is given by the following.

$$r = \sqrt{x^{2} + y^{2}}$$

The argument requires attention to the quadrant of the point $\left(\right. x , y \left.\right)$ in the complex plane. When $x > 0$, one has the following.

$$\theta = arctan \left(\right. \frac{y}{x} \left.\right)$$

When $x < 0$, a correction of $\pm \pi$ must be applied depending on the sign of $y$, and when $x = 0$ the argument is $\pm \pi / 2$ according to the sign of $y$.

## Modulus and argument

The modulus $r$ of a complex number represents its distance from the origin in the complex plane. It is computed via the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/) applied to the real and imaginary components, and its value is always non-negative.

$$r = \left|\right. z \left|\right. = \sqrt{a^{2} + b^{2}} \geq 0$$

Since the modulus measures a geometric length, it cannot be negative. When $r = 0$, the only complex number satisfying this condition is $z = 0$, which corresponds to the origin of the complex plane. In that case, there is no directional component and the argument $\theta$ is undefined. For every nonzero complex number, the modulus is strictly positive, that is, $r > 0$.

---

The argument $\theta$ of a complex number describes its angular position in the complex plane, measured in radians from the positive real axis. Unlike the modulus, which is uniquely determined, the argument is not unique: two angles that differ by an [integer](https://algebrica.org/integers/) multiple of $2 \pi$ describe the same direction, and therefore the same complex number. More precisely, for any $k \in \mathbb{Z}$, the angles $\theta$ and $\theta + 2 k \pi$ correspond to the same point in the complex plane. This is often written in the following compact form:

$$arg ⁡ \left(\right. z \left.\right) = \theta + 2 k \pi , k \in \mathbb{Z}$$

To obtain a unique representative, one typically selects the principal argument, denoted $\text{Arg} \left(\right. z \left.\right) ,$ which is the value of $\theta$ lying in the interval below.

$$- \pi < \theta \leq \pi$$

In this convention, angles are measured counterclockwise from the positive real axis, with negative values corresponding to directions below it. An alternative convention, common in engineering and applied mathematics, restricts the argument to the interval below.

$$0 \leq \theta < 2 \pi$$

In this case all arguments are taken as non-negative. Both conventions are equally valid; the choice depends on the context. Regardless of the convention adopted, the argument of $z = 0$ remains undefined, since the origin carries no directional information.

## How to express a complex number in trigonometric form

- Given a complex number $z = a + b i$, compute its modulus using the following formula.
  $$r = \sqrt{a^{2} + b^{2}}$$
- Determine the argument $\theta$ by identifying the quadrant of the point $\left(\right. a , b \left.\right)$ in the complex plane. When $a > 0$, the argument is given by the following.
  $$\theta = arctan \left(\right. \frac{b}{a} \left.\right)$$
  When $a < 0$, a correction of $\pm \pi$ must be added depending on the sign of $b$. When $a = 0$ the argument is $\pi / 2$ if $b > 0$ and $- \pi / 2$ if $b < 0$.
- Substitute $r$ and $\theta$ into the trigonometric form.
  $$z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$$

## Example

Consider the complex number $z = 1 + i$ and its conversion to trigonometric form. The modulus is computed by applying the definition directly. Since $a = 1$ and $b = 1$, one obtains the following:

$$r = \sqrt{a^{2} + b^{2}} = \sqrt{1^{2} + 1^{2}} = \sqrt{2}$$

To determine the argument, observe that the point $\left(\right. 1 , 1 \left.\right)$ lies in the first quadrant of the complex plane, where both components are positive. Since $a > 0$, the argument is given by the arctangent of the ratio $b / a$. Substituting the values yields the following:

$$\theta = arctan \left(\right. \frac{b}{a} \left.\right) = arctan \left(\right. \frac{1}{1} \left.\right) = arctan ⁡ \left(\right. 1 \left.\right) = \frac{\pi}{4}$$

This result is consistent with the geometry of the situation: the complex number $1 + i$ lies along the bisector of the first quadrant, which forms an angle of $\pi / 4$ radians with the positive real axis.

Substituting $r = \sqrt{2}$ and $\theta = \frac{\pi}{4}$ into the trigonometric form gives the final result.

The complex number $1 + i$ in its trigonometric form is:

$$z = \sqrt{2} \left(\right. cos ⁡ \frac{\pi}{4} + i sin ⁡ \frac{\pi}{4} \left.\right)$$

conversion stepsargument of summodulus of sumsum via algebraic formrootspowersdivisionmultiplicationrotationcomplex conjugatesine projectioncosine projectionpolar coordinatescomplex planeunit circlepolar interpretationargumentmodulustrigonometric formalgebraic formoperationsgeometryrepresentation
