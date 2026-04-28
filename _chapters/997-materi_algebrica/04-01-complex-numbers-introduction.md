---
layout: chapter
title: "Complex Numbers"
chapter: "Complex Numbers"
chapter_order: 4
section_order: 1
permalink: /materi-algebrica/complex-numbers/complex-numbers/
---

## Introduction

Complex numbers arise to overcome the limitations of the set of [real numbers](https://algebrica.org/types-of-numbers) $\mathbb{R}$, particularly the impossibility of taking even-indexed roots of negative numbers. One major consequence of this restriction is the inability to determine the solutions of a [quadratic equation](https://algebrica.org/quadratic-equations) with a negative [discriminant](https://algebrica.org/quadratic-formula).

In the set of [real numbers](https://algebrica.org/properties-of-real-numbers/) $\mathbb{R}$, it is impossible to find a number whose square is $- 1$, since the square of any real number is always non-negative. Consequently, solving the equation $p \left(\right. x \left.\right) = x^{2} + 1 = 0$ has no solutions in $\mathbb{R}$. Indeed, this would lead to $x^{2} = - 1$, which is never satisfied in the set of real numbers $\mathbb{R}$.

Starting from this very equation, we introduce the symbol $i$, known as the imaginary unit, which is defined by the property:
$$i^{2} = - 1$$

In this way, the equation $x^{2} + 1 = 0$ has two distinct complex roots, given by $\pm i$.

## Construction of the complex numbers

The introduction of complex numbers is sometimes treated as a matter of convenient notation, as though the symbol $i$ were simply declared to satisfy $i^{2} = - 1$ and the matter were settled.This approach leaves an important question unanswered: does such an object actually exist, and if so, in what mathematical sense? The answer requires a short excursion into the construction of $\mathbb{C}$ from the [real numbers](https://algebrica.org/real-numbers).

The starting point is the Cartesian product $\mathbb{R}^{2}$, the set of all ordered pairs of real numbers. Each element of this set is a pair of the form $\left(\right. a , b \left.\right)$ with $a , b \in \mathbb{R}$. This [set](https://algebrica.org/sets/) is the familiar Euclidean plane but here we want to equip it with an algebraic structure that makes it a [field](https://algebrica.org/fields/). To do so, addition and multiplication must be defined on $\mathbb{R}^{2}$.

Addition is defined componentwise. Given two pairs $\left(\right. a , b \left.\right)$ and $\left(\right. c , d \left.\right)$, their sum is the following:
$$\left(\right. a , b \left.\right) + \left(\right. c , d \left.\right) = \left(\right. a + c , b + d \left.\right)$$
This is the natural extension of [vector](https://algebrica.org/vectors/) addition in the plane and presents no difficulty.

---

Multiplication is more subtle, and it is precisely here that the algebraic structure of the complex numbers diverges from that of $\mathbb{R}^{2}$ viewed merely as a [vector space](https://algebrica.org/vector-spaces/). The product of two pairs is defined as follows.
$$\left(\right. a , b \left.\right) \cdot \left(\right. c , d \left.\right) = \left(\right. a c - b d , a d + b c \left.\right)$$
This rule is not arbitrary. It is the unique multiplication that turns $\mathbb{R}^{2}$ into a field extending $\mathbb{R}$, as will become apparent once the connection with the standard algebraic notation is made explicit. The set $\mathbb{R}^{2}$ equipped with these two operations is denoted $\mathbb{C}$ and its elements are called complex numbers.

The real numbers embed into $\mathbb{C}$ through the identification $a \rightarrowtail \left(\right. a , 0 \left.\right)$. One can verify directly that this map preserves both addition and multiplication, so $\mathbb{R}$ sits inside $\mathbb{C}$ as a subfield in a precise algebraic sense. The element $\left(\right. 0 , 1 \left.\right)$, which has no counterpart in this embedded copy of $\mathbb{R}$, plays a distinguished role. Computing its square according to the multiplication rule gives the following result.
$$\left(\right. 0 , 1 \left.\right) \cdot \left(\right. 0 , 1 \left.\right) = \left(\right. 0 \cdot 0 - 1 \cdot 1 , 0 \cdot 1 + 1 \cdot 0 \left.\right) = \left(\right. - 1 , 0 \left.\right)$$
Under the identification above, the pair $\left(\right. - 1 , 0 \left.\right)$ corresponds to the real number $- 1$. In other words, the element $\left(\right. 0 , 1 \left.\right)$ of $\mathbb{C}$ satisfies exactly the relation that the symbol $i$ is traditionally required to satisfy. This element is called the imaginary unit and is denoted $i$, so that by definition $i = \left(\right. 0 , 1 \left.\right)$ and consequently $i^{2} = - 1$. The property $i^{2} = - 1$ is therefore not a postulate imposed on an undefined symbol: it is a theorem that follows from the multiplication rule on $\mathbb{R}^{2}$.

With this notation established, every complex number $\left(\right. a , b \left.\right)$ can be decomposed as a combination of the two basis elements $\left(\right. 1 , 0 \left.\right)$ and $\left(\right. 0 , 1 \left.\right)$, which correspond to $1$ and $i$ respectively. The decomposition takes the familiar form $a + b i$, since the following chain of equalities holds.
$$\left(\right. a , b \left.\right) & = \left(\right. a , 0 \left.\right) + \left(\right. 0 , b \left.\right) \\ & = a \cdot \left(\right. 1 , 0 \left.\right) + b \cdot \left(\right. 0 , 1 \left.\right) \\ & = a + b i$$
The notation $z = a + b i$ is thus a compact encoding of the ordered pair $\left(\right. a , b \left.\right)$, with $a$ called the real part and $b$ the imaginary part of $z$. These are written as $Re \left(\right. z \left.\right) = a$ and $Im \left(\right. z \left.\right) = b$. Note that the imaginary part is the real number $b$, not the quantity $b i$.

---

It remains to verify that the algebraic properties expected of a field actually hold. The verification is mechanical but worth summarising. Under addition, $\mathbb{C}$ forms an abelian [group](https://algebrica.org/groups/): commutativity and associativity are inherited directly from $\mathbb{R}$, the additive identity is $\left(\right. 0 , 0 \left.\right)$, and the additive inverse of $\left(\right. a , b \left.\right)$ is $\left(\right. - a , - b \left.\right)$.

Multiplication is also commutative and associative, as can be confirmed by direct computation, and the multiplicative identity is $\left(\right. 1 , 0 \left.\right)$. The distributive law holds. The only property requiring genuine attention is the existence of multiplicative inverses for nonzero elements. Given $\left(\right. a , b \left.\right) \neq \left(\right. 0 , 0 \left.\right)$, one checks that its multiplicative inverse is the following pair.
$$\left(\right. a , b \left.\right)^{- 1} = \left(\right. \frac{a}{a^{2} + b^{2}} , \frac{- b}{a^{2} + b^{2}} \left.\right)$$
The denominator $a^{2} + b^{2}$ is strictly positive when $\left(\right. a , b \left.\right) \neq \left(\right. 0 , 0 \left.\right)$, which ensures the formula is well defined for every nonzero complex number. The conclusion is that $\mathbb{C}$, as constructed, is a field. Moreover, since $\mathbb{R}$ embeds into it as a subfield, $\mathbb{C}$ is an extension field of $\mathbb{R}$. This is the precise mathematical sense in which the complex numbers extend the real number system.

One may also observe that, as a vector space over $\mathbb{R}$, the field $\mathbb{C}$ has dimension two, with basis $1 , i$. This two-dimensionality is what makes the geometric interpretation in the complex plane so natural: the real and imaginary parts of a complex number serve as coordinates with respect to this basis.

The construction just described also generalises: replacing $\mathbb{R}$ with an arbitrary field $F$ and seeking an extension in which a chosen irreducible [polynomial](https://algebrica.org/polynomials/) has a root leads to the broader theory of field extensions, of which $\mathbb{C} \cong \mathbb{R} \left[\right. x \left]\right. / \left(\right. x^{2} + 1 \left.\right)$ is the simplest and most important example.

## Definition

A complex number $z$ is a number of the form $z = a + b i$, where $a$ and $b$ are real numbers. The set of complex numbers is denoted by $\mathbb{C}$ and is formally defined as follows.
$$\mathbb{C} := z = a + i b \mid a , b \in \mathbb{R}$$
Let $z$ be any complex number. The quantity $a$ is referred to as the real part of $z$ and is denoted by $Re \left(\right. z \left.\right)$, while $b$ is called the imaginary part of $z$ and is denoted by $Im \left(\right. z \left.\right)$:
$$z = a + i b \rightarrow \left{\right. Re \left(\right. z \left.\right) = a \\ Im \left(\right. z \left.\right) = b$$

- The representation $z = a + i b$ is called the algebraic form of a complex number. As established in the construction above, the complex number $a + b i$ is the ordered pair $\left(\right. a , b \left.\right) \in \mathbb{R} \times \mathbb{R}$, and the set $\mathbb{C}$ coincides with the Cartesian product $\mathbb{R} \times \mathbb{R}$ equipped with the operations defined there.
- The complex number $z = 2 + 3 i$ has a real part of $2$ and an imaginary part of $3$.
- Numbers of the form $z = i b$ are called purely imaginary numbers.

---

While the algebraic form is the most familiar representation of complex numbers, an alternative and often more powerful way to express them is through their polar [trigonometric form](https://algebrica.org/complex-numbers-trigonometric-form):
$$z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$$
Another representation is the [exponential form](https://algebrica.org/complex-numbers-exponential-form/):
$$z = r e^{i \theta}$$

## Complex plane

Due to the structure of the set $\mathbb{C}$ as a Cartesian product, complex numbers can be represented geometrically in the complex plane (also known as the Gaussian or Argand plane), where the real part corresponds to the $x$-coordinate and the imaginary part corresponds to the $y$-coordinate. Thus, the complex number:

$$z = x + i y$$

can be represented as the point $\left(\right. x , y \left.\right)$ in the plane, which is known as the Gaussian plane (or complex plane).

![](https://algebrica.org/wp-content/uploads/resources/images/complex-numbers-8.png)

A purely imaginary number is represented by the ordered pair $i = \left(\right. 0 , 1 \left.\right)$.

## Conjugate and modulus

Given the complex number $z = a + b i$, the conjugate of $z$ is defined as the complex number:

$$\overset{―}{z} = a - b i$$

$\overset{―}{z}$ is represented in the complex plane by the point symmetric to $z$ with respect to the $x$-axis.

![](https://algebrica.org/wp-content/uploads/resources/images/quad-eq-complex-roots.png)

---

Given the complex number $z = a + b i$, the modulus of $z$ is defined as:

$$\left|\right. z \left|\right. = \sqrt{a^{2} + b^{2}}$$

It represents the distance from the origin to the point $\left(\right. a , b \left.\right)$ in the complex plane. This definition is directly derived from the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/), since the modulus corresponds to the hypotenuse of a right triangle with legs of lengths $\left|\right. a \left|\right.$ and $\left|\right. b \left|\right.$:

$$\left|\right. z \left|\right.^{2} = a^{2} + b^{2}$$

![](https://algebrica.org/wp-content/uploads/resources/images/complex-numbers-6.png)

## Example

Let’s consider the complex number $z = 3 + 2 i$. Using the modulus formula, we substitute $a = 3$ and $b = 2$:

$$\left|\right. z \left|\right. = \sqrt{3^{2} + 2^{2}} = \sqrt{9 + 4} = \sqrt{13}$$

Thus, the modulus of $z = 3 + 2 i$ is:

$$\left|\right. z \left|\right. = \sqrt{13} \approx 3.61$$

> This value represents the distance of $z$ from the origin in the complex plane for the complex number $3 + 2 i$.

## Argument

The argument of a complex number $z = a + b i$ is the angle $\theta$ formed between the positive real axis and the segment connecting the origin to the point $\left(\right. a , b \left.\right)$ in the complex plane. It is measured in radians, counterclockwise from the positive real axis, and is denoted by $arg ⁡ \left(\right. z \left.\right)$.

The argument is not uniquely determined: any two angles differing by an integer multiple of $2 \pi$ describe the same geometric direction. To resolve this ambiguity, one typically works with the principal argument, denoted $Arg \left(\right. z \left.\right)$, which is the unique value of $\theta$ satisfying the following condition.
$$- \pi < Arg \left(\right. z \left.\right) \leq \pi$$

Computing the argument requires care, because the naive formula $\theta = arctan ⁡ \left(\right. b / a \left.\right)$ is insufficient: the arctangent function returns values only in the interval $\left(\right. - \pi / 2 , , \pi / 2 \left.\right)$, which covers only the right half of the complex plane and fails entirely when $a = 0$. The correct determination of $\theta$ depends on the quadrant in which $\left(\right. a , b \left.\right)$ lies, and must be handled case by case.

When $a > 0$, the point lies in the right half-plane and the principal argument is given by the [arctangent](https://algebrica.org/arctangent-and-arccotangent/).
$$Arg \left(\right. z \left.\right) = arctan \left(\right. \frac{b}{a} \left.\right)$$
When $a < 0$ and $b \geq 0$, the point lies in the second quadrant, and a correction of $\pi$ must be added to bring the angle into the correct range.
$$Arg \left(\right. z \left.\right) = arctan \left(\right. \frac{b}{a} \left.\right) + \pi$$
When $a < 0$ and $b < 0$, the point lies in the third quadrant, and the correction is $- \pi$.
$$Arg \left(\right. z \left.\right) = arctan \left(\right. \frac{b}{a} \left.\right) - \pi$$
When $a = 0$, the point lies on the imaginary axis and the arctangent is undefined. In this case the argument is determined directly from the sign of $b$: if $b > 0$ then $Arg \left(\right. z \left.\right) = \pi / 2$, and if $b < 0$ then $Arg \left(\right. z \left.\right) = - \pi / 2$. The case $z = 0$ is excluded, since the argument of the origin is undefined.

---

As an illustration, consider the complex number $z = - 1 + i$. Its real part is negative and its imaginary part is positive, so the point lies in the second quadrant. Applying the arctangent to the ratio $b / a = 1 / \left(\right. - 1 \left.\right) = - 1$ gives $arctan ⁡ \left(\right. - 1 \left.\right) = - \pi / 4$, which falls in the fourth quadrant and is therefore incorrect. Since $a < 0$ and $b \geq 0$, the correction of $+ \pi$ must be applied, yielding the following.
$$Arg \left(\right. z \left.\right) = - \frac{\pi}{4} + \pi = \frac{3 \pi}{4}$$
This value is consistent with the geometric position of $z = - 1 + i$: the point lies at equal distances from both axes in the second quadrant, forming an angle of $135 \circ$ with the positive real axis.

## Properties of $\mathbb{C}$

The [sum and product](https://algebrica.org/complex-number-operations) of complex numbers satisfy the associative, commutative, and distributive properties, just like the set of real numbers.
Associative property for sum and product. When adding or multiplying complex numbers, the way in which the numbers are grouped does not affect the result.
$$\left(\right. z_{1} + z_{2} \left.\right) + z_{3} = z_{1} + \left(\right. z_{2} + z_{3} \left.\right)$$
$$\left(\right. z_{1} \cdot z_{2} \left.\right) \cdot z_{3} = z_{1} \cdot \left(\right. z_{2} \cdot z_{3} \left.\right)$$
Commutative property. The order in which two complex numbers are added or multiplied does not change the result.
$$z_{1} + z_{2} = z_{2} + z_{1}$$
$$z_{1} \cdot z_{2} = z_{2} \cdot z_{1}$$
Distributive property. Multiplying a number by a sum gives the same result as multiplying each addend individually and then adding the products.
$$z_{1} \cdot \left(\right. z_{2} + z_{3} \left.\right) = z_{1} \cdot z_{2} + z_{1} \cdot z_{3}$$

---

The complex number $0 + 0 i$ is the additive identity in $\mathbb{C}$, since for every complex number $z = a + b i$, we have:
$$z + \left(\right. 0 + 0 i \left.\right) & = \left(\right. a + b i \left.\right) + \left(\right. 0 + 0 i \left.\right) \\ & = \left(\right. a + 0 \left.\right) + \left(\right. b + 0 \left.\right) i \\ & = a + b i \\ & = z$$
The complex number $1 + 0 i$ is the multiplicative identity in $\mathbb{C}$, since for every complex number $z = a + b i$, we have:
$$z \cdot \left(\right. 1 + 0 i \left.\right) & = \left(\right. a + b i \left.\right) \cdot \left(\right. 1 + 0 i \left.\right) \\ & = a \cdot 1 + a \cdot 0 i + b i \cdot 1 + b i \cdot 0 i \\ & = a + b i \\ & = z$$

---

The opposite of $a + b i$ is the complex number:
$$- \left(\right. a + b i \left.\right) = - a - b i$$
The reciprocal of a nonzero complex number $z = a + b i$ is the complex number:
$$\frac{1}{z} = \frac{a}{a^{2} + b^{2}} - \frac{b}{a^{2} + b^{2}} i$$
Complex numbers of the form $z = a + 0 i$, where the imaginary part is zero, are precisely the real numbers.

---

The set of complex numbers $\mathbb{C}$ cannot be ordered in a way that is compatible with addition and multiplication. If there existed a total order $\leq$ on $\mathbb{C}$, we should be able to compare $i$ with $0$. There are two possible cases:

- If $i > 0$, then multiplying both sides by $i$ gives $i^{2} = - 1 > 0$, which is a contradiction.
- If $i < 0$, multiplying both sides by $i$ again leads to the same contradiction: $- 1 > 0$.
   Since neither case is valid, no total order on $\mathbb{C}$ can be defined.

non orderabilityidentities and inversesfield structurepythagorean relationmodulusargand planeargumentcomplex conjugatepurely imaginaryimaginary partreal partalgebraic formclosure propertiesmultiplication ruleaddition ruleordered pairscartesian productimaginary unitgeometry and propertiesrepresentationconstruction
