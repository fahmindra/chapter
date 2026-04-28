---
layout: chapter
title: "Complex Numbers in Exponential Form"
chapter: "Complex Numbers"
chapter_order: 4
section_order: 4
permalink: /materi-algebrica/complex-numbers/complex-numbers-in-exponential-form/
---

## Introduction

While the [algebraic form](https://algebrica.org/complex-numbers-introduction/) $z = a + b i$ is the most familiar representation of complex numbers, an alternative and often more powerful way to express them is through their exponential form:

$$z = r e^{i \theta}$$

The quantities appearing in this expression have the following meaning:

- $r = \left|\right. z \left|\right. = \sqrt{a^{2} + b^{2}}$ is the modulus, representing the distance of $z$ from the origin in the complex plane.
- $\theta = arg ⁡ \left(\right. z \left.\right)$ is the argument, the angle in radians between the positive real axis and the vector representing $z$.
- $r$ and $\theta$ retain their respective interpretations from the [trigonometric representation](https://algebrica.org/complex-numbers-trigonometric-form) of a complex number.

![](https://algebrica.org/wp-content/uploads/resources/images/trig-form-1.png)

> The point $P$ can be represented either in rectangular coordinates $\left(\right. a , b \left.\right)$ or in polar coordinates $\left(\right. r , \theta \left.\right)$. This duality highlights the connection between the algebraic and geometric perspectives of complex numbers.

---

The equation $z = r e^{i \theta}$ follows directly from Euler’s formula:

$$e^{i \theta} = cos ⁡ \theta + i sin ⁡ \theta$$

This identity shows that the [exponential](https://algebrica.org/exponential-function) representation is equivalent to the trigonometric form:
$$z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$$

Euler’s formula can be established by expanding $e^{i x}$, $cos ⁡ x$, and $sin ⁡ x$ as [Taylor series](https://algebrica.org/taylor-series/) and observing that the series for $e^{i x}$ splits naturally into real and imaginary parts:
$$e^{i x} = \sum_{n = 0}^{\infty} \frac{\left(\right. i x \left.\right)^{n}}{n !} = cos ⁡ x + i sin ⁡ x$$

> The formula involves Euler’s number $e$, a fundamental constant in mathematics. To understand its origin, one may consult the topic [Euler’s number as the limit of a sequence](https://algebrica.org/euler-number-limit-sequence/), where it arises as the limit of a sequence. Geometrically, this corresponds to a reflection of $z$ across the real axis in the complex plane.

---

Given the complex number $z = a + b i$, its complex conjugate is defined as:

$$\overset{―}{z} = a - b i$$

In exponential form, the conjugate of $z = r e^{i \theta}$ is obtained by negating the argument:

$$\overset{―}{z} = r e^{- i \theta}$$

## How to express a complex number in exponential form

Given a complex number $z = a + b i$, the conversion to exponential form proceeds as follows.

- Compute the modulus of $z$ according to the definition:
  $$r = \sqrt{a^{2} + b^{2}}$$
- Determine the argument $\theta$, that is, the angle that the [vector](https://algebrica.org/vectors/) representing $z$ forms with the positive real axis. When $a > 0$, one may use the formula:
  $$\theta = tan^{- 1} \left(\right. \frac{b}{a} \left.\right)$$
  When $a \leq 0$, the quadrant of $z$ must be taken into account to select the correct value of $\theta$.
- Write $z$ in exponential form by applying Euler’s formula:
  $$z = r e^{i \theta}$$

---

The argument of a complex number is not uniquely determined: if $\theta$ is an argument of $z$, then so is $\theta + 2 k \pi$ for any integer $k$. More precisely, one has:

$$z = r e^{i \left(\right. \theta + 2 k \pi \left.\right)}$$
$$k \in \mathbb{Z}$$

The exponential representation is therefore not unique; it is defined modulo $2 \pi$. To remove this ambiguity, one conventionally selects the principal argument, denoted $\text{Arg} \left(\right. z \left.\right)$, which satisfies:

$$- \pi < \text{Arg} \left(\right. z \left.\right) \leq \pi$$

Unless otherwise stated, the argument is understood to mean the principal argument.

## Example 1

Consider the complex number $z = 2 + 3 i$ and its conversion to exponential form. The modulus is computed by applying the definition directly. Since $a = 2$ and $b = 3$, one obtains:
$$r = \left|\right. z \left|\right. & = \sqrt{a^{2} + b^{2}} \\ & = \sqrt{2^{2} + 3^{2}} \\ & = \sqrt{4 + 9} \\ & = \sqrt{13}$$
The argument $\theta$ is the angle that the vector representing $z$ forms with the positive real axis. Since $a = 2 > 0$, the number lies in the first quadrant and the arctangent formula applies without adjustment:
$$\theta = tan^{- 1} \left(\right. \frac{b}{a} \left.\right) = tan^{- 1} \left(\right. \frac{3}{2} \left.\right) \approx 0.98 \text{rad}$$

Substituting $r = \sqrt{13}$ and $\theta \approx 0.98$ into the exponential form, the result is:
$$z = \sqrt{13} e^{ i \cdot 0.98}$$

## Example 2

Consider the complex number $z = - 1 + i$ and its conversion to exponential form. The modulus is computed by applying the definition. Since $a = - 1$ and $b = 1$, one obtains:
$$r = \left|\right. z \left|\right. & = \sqrt{\left(\right. - 1 \left.\right)^{2} + 1^{2}} \\ & = \sqrt{1 + 1} \\ & = \sqrt{2}$$

The argument requires more care. Since $a = - 1 < 0$ and $b = 1 > 0$, the number lies in the second quadrant. The arctangent formula alone would give:
$$tan^{- 1} ! \left(\right. \frac{b}{a} \left.\right) = tan^{- 1} \left(\right. \frac{1}{- 1} \left.\right) = tan^{- 1} ⁡ \left(\right. - 1 \left.\right) = - \frac{\pi}{4}$$
which corresponds to the fourth quadrant and is therefore incorrect. The correct argument is obtained by adding $\pi$:
$$\theta = - \frac{\pi}{4} + \pi = \frac{3 \pi}{4}$$

Substituting $r = \sqrt{2}$ and $\theta = \frac{3 \pi}{4}$ into the exponential form, the result is:
$$z = \sqrt{2} e^{ i \frac{3 \pi}{4}}$$

## Properties of the exponential form

One of the principal advantages of the exponential form is the simplicity it confers on multiplication, division, and exponentiation of complex numbers. Given two complex numbers $z_{1} = r_{1} e^{i \theta_{1}}$ and $z_{2} = r_{2} e^{i \theta_{2}}$, their product is obtained by multiplying the moduli and adding the arguments:
$$z_{1} z_{2} = r_{1} r_{2} e^{i \left(\right. \theta_{1} + \theta_{2} \left.\right)}$$

As a concrete illustration, consider $z_{1} = 2 e^{i \pi / 3}$ and $z_{2} = 3 e^{i \pi / 6} .$ Their product is:
$$z_{1} z_{2} = 2 \cdot 3 e^{i \left(\right. \pi / 3 + \pi / 6 \left.\right)} = 6 e^{i \pi / 2}$$
The modulus of the product is $6$ and its argument is $\pi / 2$, corresponding to the imaginary unit direction in the complex plane.

---

Similarly, provided $z_{2} \neq 0$, the quotient is obtained by dividing the moduli and subtracting the arguments:
$$\frac{z_{1}}{z_{2}} = \frac{r_{1}}{r_{2}} e^{i \left(\right. \theta_{1} - \theta_{2} \left.\right)}$$
Both operations correspond to simple geometric transformations in the complex plane: a dilation and a rotation. Integer [powers](https://algebrica.org/powers/) are handled with equal efficiency. For any integer $n$, the rules of exponentiation give directly:
$$z^{n} = \left(\left(\right. r e^{i \theta} \left.\right)\right)^{n} = r^{n} e^{i n \theta}$$
The modulus is raised to the $n$-th power and the argument is scaled by $n$. Applying Euler’s formula to $e^{i n \theta}$, this is equivalent to [De Moivre’s Theorem](https://algebrica.org/de-moivre-theorem/):
$$\left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)^{n} = cos ⁡ \left(\right. n \theta \left.\right) + i sin ⁡ \left(\right. n \theta \left.\right)$$
As an illustration, squaring $z = r e^{i \theta}$ gives:
$$z^{2} = r^{2} e^{i 2 \theta}$$

![](https://algebrica.org/wp-content/uploads/resources/images/exponent-form-2-1.png "De Moivre's Theorem.")

The resulting complex number has modulus $r^{2}$ and argument $2 \theta$. Ggeometrically, the vector is stretched by a factor of $r^{2}$ and rotated to twice its original angle.

## Roots in exponential form

The exponential form provides a natural framework for computing the $n$-th roots of a complex number. Given $z = r e^{i \theta}$, the solutions of the equation $w^{n} = z$ are exactly $n$ distinct complex numbers, given by:
$$w_{k} = \sqrt[n]{r} e^{i \left(\right. \theta + 2 k \pi \left.\right) / n}$$
$$k = 0 , 1 , \ldots , n - 1$$
The modulus of each root is $\sqrt[n]{r}$, while the arguments are equally spaced by $2 \pi / n$. Geometrically, the $n$ roots correspond to the vertices of a regular polygon inscribed in a circle of radius $\sqrt[n]{r}$ in the complex plane.

---

As an illustration, consider the cube roots of $z = 8$. Writing $z = 8 e^{i \cdot 0}$, one has $r = 8$ and $\theta = 0$, so the three roots are:

$$w_{k} = \sqrt[3]{8} e^{i \cdot 2 k \pi / 3} = 2 e^{i \cdot 2 k \pi / 3}$$
$$k = 0 , 1 , 2$$

Explicitly we have:

$$w_{0} & = 2 e^{i \cdot 0} = 2 \\ w_{1} & = 2 e^{i \cdot 2 \pi / 3} = 2 \left(\right. - \frac{1}{2} + i \frac{\sqrt{3}}{2} \left.\right) = - 1 + i \sqrt{3} \\ w_{2} & = 2 e^{i \cdot 4 \pi / 3} = 2 \left(\right. - \frac{1}{2} - i \frac{\sqrt{3}}{2} \left.\right) = - 1 - i \sqrt{3}$$

> The three roots have equal modulus $2$ and are separated by angles of $2 \pi / 3$, forming the vertices of an equilateral triangle inscribed in a circle of radius $2$ centered at the origin.

complex conjugatede moivre theorempowersdivisionmultiplicationargument determinationmodulus computationconversion stepsangle representationunit circlecomplex exponentialtaylor serieseuler numbereuler formulaprincipal argumentargumentmodulusexponential formtrigonometric formalgebraic formoperationsfoundationsrepresentation
