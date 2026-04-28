---
layout: chapter
title: "Operations with Complex Numbers"
chapter: "Complex Numbers"
chapter_order: 4
section_order: 2
permalink: /materi-algebrica/complex-numbers/operations-with-complex-numbers/
---

## Introduction

A [complex number](https://algebrica.org/complex-numbers-introduction/) $z$ is an expression of the form $z = a + b i$, where $a$ and $b$ are [real numbers](https://algebrica.org/properties-of-real-numbers/) and $i$ is the imaginary unit, characterized by the defining relation $i^{2} = - 1$.

The [real number](https://algebrica.org/real-numbers/) $a$ is called the real part of $z$ and is denoted $Re \left(\right. z \left.\right)$. The real number $b$ is called the imaginary part and is denoted $Im \left(\right. z \left.\right)$. The set of all complex numbers is defined as follows:

$$\mathbb{C} := \left{\right. z = a + b i \mid a , b \in \mathbb{R} \left.\right}$$

Every real number $a \in \mathbb{R}$ can be identified with the complex number $a + 0 i$, so $\mathbb{R}$ embeds naturally into $\mathbb{C}$ as a subfield.

---

The set $\mathbb{C}$, equipped with the addition and multiplication defined in the sections below, forms a [field](https://algebrica.org/fields/). Before examining each operation individually, it is useful to recall the field axioms that govern the arithmetic of complex numbers.

- Closure: for any $z_{1} , z_{2} \in \mathbb{C}$, the sum $z_{1} + z_{2}$ and the product $z_{1} \cdot z_{2}$ both belong to $\mathbb{C}$.
- Commutativity and associativity: addition and multiplication are commutative and associative, in strict analogy with $\mathbb{R}$.
- Neutral elements: the number $0 = 0 + 0 i$ is the additive identity, and $1 = 1 + 0 i$ is the multiplicative identity.
- Additive inverse: for every $z = a + b i$, the additive inverse is $- z = - a - b i$, and one has $z + \left(\right. - z \left.\right) = 0$.
- Multiplicative inverse: for every $z \neq 0$, there exists a unique $z^{- 1} \in \mathbb{C}$ such that $z \cdot z^{- 1} = 1$. Its explicit form is derived in the section on division below.
- Distributivity: for all $z_{1} , z_{2} , z_{3} \in \mathbb{C}$, the following identity holds:
  $$z_{1} \cdot \left(\right. z_{2} + z_{3} \left.\right) = z_{1} \cdot z_{2} + z_{1} \cdot z_{3}$$

Two structural properties distinguish $\mathbb{C}$ from $\mathbb{R}$. Unlike $\mathbb{R}$, the field $\mathbb{C}$ is not an ordered field. There is no total order on $\mathbb{C}$ compatible with its field operations, and expressions such as $z_{1} < z_{2}$ are therefore undefined for general complex numbers.

More remarkably, $\mathbb{C}$ is algebraically closed. Every nonconstant [polynomial](https://algebrica.org/polynomials/) with coefficients in $\mathbb{C}$ has at least one root in $\mathbb{C}$. This result, known as the [fundamental theorem of algebra](https://algebrica.org/roots-of-a-polynomial/), has no analogue in $\mathbb{R}$, where polynomials such as $x^{2} + 1$ admit no [real roots](https://algebrica.org/roots-of-a-polynomial/).

## Sum and difference of complex numbers

The sum and difference of two complex numbers are defined componentwise, by operating separately on the real and imaginary parts. Given $z_{1} = a + b i$ and $z_{2} = c + d i$, the definitions are the following.

$$z_{1} + z_{2} = \left(\right. a + c \left.\right) + \left(\right. b + d \left.\right) i$$
$$z_{1} - z_{2} = \left(\right. a - c \left.\right) + \left(\right. b - d \left.\right) i$$

---

Let $z_{1} = 2 - 3 i$ and $z_{2} = 3 + 5 i$. To compute $z_{1} - z_{2}$, we subtract the real parts and the imaginary parts separately. Subtracting $z_{2}$ is equivalent to adding the additive inverse $- z_{2} = - 3 - 5 i$, so the operation reduces to a componentwise subtraction.

$$z_{1} - z_{2} & = \left(\right. 2 - 3 i \left.\right) - \left(\right. 3 + 5 i \left.\right) \\ & = \left(\right. 2 - 3 \left.\right) + \left(\right. - 3 - 5 \left.\right) i \\ & = - 1 - 8 i$$

Let $z_{1} = - 4 + 2 i$ and $z_{2} = 6 - 7 i$. To compute $z_{1} + z_{2}$, we add the real parts and the imaginary parts separately, since addition in $\mathbb{C}$ acts componentwise by definition.

$$z_{1} + z_{2} & = \left(\right. - 4 + 2 i \left.\right) + \left(\right. 6 - 7 i \left.\right) \\ & = \left(\right. - 4 + 6 \left.\right) + \left(\right. 2 - 7 \left.\right) i \\ & = 2 - 5 i$$

> The sum and difference of complex numbers inherit from the field structure of $\mathbb{C}$ all the algebraic properties that hold in $\mathbb{R}$: commutativity, associativity, and distributivity with respect to multiplication.

---

From a geometric point of view, complex numbers can be interpreted as [vectors](https://algebrica.org/vectors/) in the complex plane, where the horizontal axis represents the real part and the vertical axis represents the imaginary part. Given two complex numbers $z_{1}$ and $z_{2}$, represented as vectors from the origin, their sum $z_{1} + z_{2}$ corresponds to vector addition by the parallelogram rule.

- The vector corresponding to $z_{2}$ is translated so that its tail coincides with the tip of the vector corresponding to $z_{1}$.
- The vector drawn from the origin to the new tip represents the resulting complex number $z_{1} + z_{2}$.

![Sum and difference of complex numbers.](https://algebrica.org/wp-content/uploads/resources/images/complex-numbers-sum.png "Sum and difference of complex numbers.")

The two constructions together provide a complete geometric interpretation of addition and subtraction in the complex plane.

The difference $z_{1} - z_{2}$ is obtained by adding $z_{1}$ to the additive inverse $- z_{2}$, whose vector is the reflection of $z_{2}$ through the origin. Geometrically, $z_{1} - z_{2}$ corresponds to the vector from the tip of $z_{2}$ to the tip of $z_{1}$, when both vectors originate at the origin.

## Product of complex numbers

The product of two complex numbers is defined by applying the distributive property and the fundamental relation $i^{2} = - 1$. Given $z_{1} = a + b i$ and $z_{2} = c + d i$, expanding the product yields the following.

$$\left(\right. a + b i \left.\right) \left(\right. c + d i \left.\right) = \left(\right. a c - b d \left.\right) + \left(\right. a d + b c \left.\right) i$$

This formula need not be memorized as a rule: it is simply the result of distributing the multiplication and substituting $i^{2} = - 1$, as shown in the examples below.

An important property of multiplication in $\mathbb{C}$ is the multiplicativity of the modulus. Recalling that [the modulus](https://algebrica.org/complex-numbers-introduction/) of $z = a + b i$ is defined as $\left|\right. z \left|\right. = \sqrt{a^{2} + b^{2}}$, one can verify that for any $z_{1} , z_{2} \in \mathbb{C}$ the following identity holds.

$$\left|\right. z_{1} \cdot z_{2} \left|\right. = \left|\right. z_{1} \left|\right. \cdot \left|\right. z_{2} \left|\right.$$

This means that multiplication scales the moduli of the two factors. The same identity extends to division: for any $z_{1} , z_{2} \in \mathbb{C}$ with $z_{2} \neq 0$, one has the following.

$$\left|\right. \frac{z_{1}}{z_{2}} \left|\right. = \frac{\left|\right. z_{1} \left|\right.}{\left|\right. z_{2} \left|\right.}$$

The geometric significance of both identities becomes fully transparent in the [trigonometric representation](https://algebrica.org/complex-numbers-trigonometric-form/), where multiplication adds the arguments and division subtracts them.

## Properties of the complex conjugate

The complex [conjugate](https://algebrica.org/complex-numbers-introduction/) satisfies several algebraic identities that follow directly from its definition. Let $z , z_{1} , z_{2} \in \mathbb{C}$. The conjugation map is an involution, meaning that applying it twice returns the original number:

$$\overset{―}{\overset{―}{z}} = z$$

Conjugation is compatible with addition, subtraction, and multiplication in the following sense:

$$\overset{―}{z_{1} + z_{2}} = \overset{―}{z_{1}} + \overset{―}{z_{2}}$$
$$\overset{―}{z_{1} - z_{2}} = \overset{―}{z_{1}} - \overset{―}{z_{2}}$$
$$\overset{―}{z_{1} \cdot z_{2}} = \overset{―}{z_{1}} \cdot \overset{―}{z_{2}}$$

These identities show that conjugation is a field automorphism of $\mathbb{C} .$ It preserves the algebraic structure of the field while fixing every element of $\mathbb{R} .$ Finally, the product of a complex number with its own conjugate yields the square of the modulus, a nonnegative real number.

$$z \cdot \overset{―}{z} = a^{2} + b^{2} = \left|\right. z \left|\right.^{2}$$

This last identity is the key step in the computation of both the reciprocal and the quotient of complex numbers: multiplying the denominator by its conjugate produces the real number $\left|\right. z \left|\right.^{2} ,$ which can then be divided out without leaving any imaginary part.

> field automorphism is a bijective map from a field to itself that preserves addition and multiplication. Conjugation satisfies this condition, and since it fixes every real number, it is an automorphism of $\mathbb{C}$ over $\mathbb{R}$.

## Division of complex numbers

To divide two complex numbers, we multiply both the numerator and the denominator by the complex conjugate of the denominator. This eliminates the imaginary part from the denominator and reduces the quotient to standard form. Given $z_{1} = a + b i$ and $z_{2} = c + d i$ with $z_{2} \neq 0$, the conjugate of the denominator is $\overset{―}{z_{2}} = c - d i$, and the procedure begins as follows.

$$\frac{a + b i}{c + d i} = \frac{\left(\right. a + b i \left.\right) \left(\right. c - d i \left.\right)}{\left(\right. c + d i \left.\right) \left(\right. c - d i \left.\right)}$$

Since $\left(\right. c + d i \left.\right) \left(\right. c - d i \left.\right) = c^{2} + d^{2}$, which is a strictly positive real number whenever $z_{2} \neq 0$, the quotient reduces to the following explicit form.

$$\frac{a + b i}{c + d i} = \frac{a c + b d}{c^{2} + d^{2}} + \frac{b c - a d}{c^{2} + d^{2}} i$$

As with multiplication, this closed form need not be memorized: it is more instructive to multiply by the conjugate directly in each case.

---

Let $z_{1} = 5 + 3 i$ and $z_{2} = 2 - i$. To compute the quotient $z_{1} / z_{2}$, we multiply both numerator and denominator by the conjugate of the denominator, which is $\overset{―}{z_{2}} = 2 + i$. Since we are multiplying by $\overset{―}{z_{2}} / \overset{―}{z_{2}} = 1$, the value of the expression is unchanged, while the denominator becomes a positive real number.

$$\frac{5 + 3 i}{2 - i} & = \frac{\left(\right. 5 + 3 i \left.\right) \left(\right. 2 + i \left.\right)}{\left(\right. 2 - i \left.\right) \left(\right. 2 + i \left.\right)} \\ & = \frac{10 + 5 i + 6 i + 3 i^{2}}{4 + 1} \\ & = \frac{10 + 11 i + 3 \left(\right. - 1 \left.\right)}{5} \\ & = \frac{7 + 11 i}{5} \\ & = \frac{7}{5} + \frac{11}{5} i$$

## Reciprocal of a complex number

The reciprocal of a nonzero complex number $z = a + b i$ is the multiplicative inverse $z^{- 1}$, defined by the condition $z \cdot z^{- 1} = 1$. It is a special case of division with numerator equal to $1$, and is computed by the same technique: multiplying numerator and denominator by the conjugate $\overset{―}{z} = a - b i$. The general formula is the following.

$$z^{- 1} = \frac{1}{a + b i} = \frac{a - b i}{a^{2} + b^{2}} = \frac{a}{a^{2} + b^{2}} - \frac{b}{a^{2} + b^{2}} i$$

---

Let $z = 3 - 2 i$. To compute $z^{- 1}$, we multiply numerator and denominator by the conjugate $\overset{―}{z} = 3 + 2 i$. The denominator becomes $\left|\right. z \left|\right.^{2} = 3^{2} + 2^{2} = 13$, a positive real number, so the expression reduces to a standard complex number.

$$\frac{1}{3 - 2 i} & = \frac{3 + 2 i}{\left(\right. 3 - 2 i \left.\right) \left(\right. 3 + 2 i \left.\right)} \\ & = \frac{3 + 2 i}{9 + 4} \\ & = \frac{3 + 2 i}{13} \\ & = \frac{3}{13} + \frac{2}{13} i$$

## Multiplication and division in trigonometric form

The operations of multiplication and division acquire a particularly transparent geometric interpretation when complex numbers are expressed in trigonometric or exponential form. Consider the following complex numbers:
$$z_{1} = r_{1} \left(\right. cos ⁡ \theta_{1} + i sin ⁡ \theta_{1} \left.\right)$$
$$z_{2} = r_{2} \left(\right. cos ⁡ \theta_{2} + i sin ⁡ \theta_{2} \left.\right)$$

Their product and quotient take the following form:

$$z_{1} \cdot z_{2} = r_{1} r_{2} \left(\right. cos ⁡ \left(\right. \theta_{1} + \theta_{2} \left.\right) + i sin ⁡ \left(\right. \theta_{1} + \theta_{2} \left.\right) \left.\right)$$
$$\frac{z_{1}}{z_{2}} = \frac{r_{1}}{r_{2}} \left(\right. cos ⁡ \left(\right. \theta_{1} - \theta_{2} \left.\right) + i sin ⁡ \left(\right. \theta_{1} - \theta_{2} \left.\right) \left.\right)$$

Multiplication therefore scales the moduli and adds the arguments, while division divides the moduli and subtracts the arguments. This geometric structure is entirely hidden in the algebraic form $a + b i$, and becomes visible only in the [trigonometric](https://algebrica.org/complex-numbers-trigonometric-form/) and [exponential](https://algebrica.org/complex-numbers-exponential-form/) representations of complex numbers.

distanceanglescalingrotationpolar formvector formnorminverseabsolute valueargumentmoduluscomplex conjugateclosureconjugate divisionreciprocaldivisionmultiplicationsubtractionadditiongeometrytoolsoperations
