---
layout: chapter
title: "Arctangent and Arccotangent"
chapter: "Trigonometry"
chapter_order: 5
section_order: 6
permalink: /materi-algebrica/trigonometry/arctangent-and-arccotangent/
---

## Arctangent definition

In the [unit circle](https://algebrica.org/unit-circle/), the [tangent](https://algebrica.org/tangent-and-cotangent) of an angle $\theta$ can be visualized as the length of the segment tangent to the circle at the point where the terminal side meets it, measured along the vertical tangent line at $\left(\right. 1 , 0 \left.\right)$. The arctangent performs the reverse process: given a [real number](https://algebrica.org/properties-of-real-numbers/) $x$, it returns the unique angle $\theta$ in the interval $\left(\right. - \pi / 2 , \pi / 2 \left.\right)$ whose tangent equals $x$. This geometric relationship illustrates how the tangent and arctangent are interconnected as a function and its inverse, each reversing the role of angle and ratio.

![Arctangent.](https://algebrica.org/wp-content/uploads/resources/images/arc-tang-1.png "Arctangent.")

By relating the arctangent to the concept of a [function](https://algebrica.org/functions), we can formally express the relationship between tangent and arctangent as follows:

$$arctan ⁡ \left(\right. x \left.\right) = \theta \Longleftrightarrow tan ⁡ \left(\right. \theta \left.\right) = x$$
$$\theta \in \left(\right. - \frac{\pi}{2} , \frac{\pi}{2} \left.\right)$$

The arctangent establishes a correspondence between a real number $x$ and the unique angle $\theta$ in the interval $\left(\right. - \pi / 2 , \pi / 2 \left.\right)$ whose tangent equals $x$. The restriction to this interval is necessary because the tangent function is periodic and therefore not injective over its full domain. By confining it to $\left(\right. - \pi / 2 , \pi / 2 \left.\right)$, one obtains a strictly increasing bijection, which admits a well-defined [inverse](https://algebrica.org/inverse-function/). This reciprocal relationship is summarized by the identity:

$$tan ⁡ \left(\right. arctan ⁡ \left(\right. x \left.\right) \left.\right) = x \forall x \in \mathbb{R}$$

- When the tangent value $x$ is positive, the corresponding angle $\theta$ lies in the first quadrant.
- When $x$ is negative, the angle lies in the fourth quadrant; and when $x = 0$, the angle is zero.

As $x$ grows without bound, the corresponding angle $\theta$ approaches the [asymptotic](https://algebrica.org/asymptotes/) values:

$$\underset{x \rightarrow + \infty}{lim} arctan ⁡ \left(\right. x \left.\right) = \frac{\pi}{2}$$
$$\underset{x \rightarrow - \infty}{lim} arctan ⁡ \left(\right. x \left.\right) = - \frac{\pi}{2}$$

These values are never attained, since no finite value of $x$ has tangent equal to $\pm \pi / 2$. They correspond to the directions in which the terminal side of the angle becomes parallel to the y-axis.

## Reference values of arctangent

Below are some commonly known values of $arctan ⁡ \left(\right. x \left.\right)$ for selected inputs, useful in various applications of trigonometry:

$$x & \rightarrow - \infty & & arctan ⁡ \left(\right. x \left.\right) \rightarrow - \pi / 2 \\ x & = - \sqrt{3} & & arctan ⁡ \left(\right. - \sqrt{3} \left.\right) = - \pi / 3 \\ x & = - 1 & & arctan ⁡ \left(\right. - 1 \left.\right) = - \pi / 4 \\ x & = - 1 / \sqrt{3} & & arctan ⁡ \left(\right. - 1 / \sqrt{3} \left.\right) = - \pi / 6 \\ x & = 0 & & arctan ⁡ \left(\right. 0 \left.\right) = 0 \\ x & = 1 / \sqrt{3} & & arctan ⁡ \left(\right. 1 / \sqrt{3} \left.\right) = \pi / 6 \\ x & = 1 & & arctan ⁡ \left(\right. 1 \left.\right) = \pi / 4 \\ x & = \sqrt{3} & & arctan ⁡ \left(\right. \sqrt{3} \left.\right) = \pi / 3 \\ x & \rightarrow + \infty & & arctan ⁡ \left(\right. x \left.\right) \rightarrow \pi / 2$$

## Arctangent function

The arctangent function $f \left(\right. x \left.\right) = arctan ⁡ \left(\right. x \left.\right)$ assigns to each real number $x \in \mathbb{R}$ the unique angle $\theta \in \left(\right. - \pi / 2 , \pi / 2 \left.\right)$ whose tangent equals $x$. Its graph is a continuous, strictly increasing curve that admits two horizontal asymptotes, namely $y = - \pi / 2$ and $y = \pi / 2$. The function is the [inverse](https://algebrica.org/inverse-function/) of the tangent restricted to its principal domain $\left(\right. - \pi / 2 , \pi / 2 \left.\right)$, over which the tangent is strictly increasing and bijective.

- Domain: $x \in \mathbb{R}$
- Range: $y \in \left(\right. - \frac{\pi}{2} , \frac{\pi}{2} \left.\right)$
- The arctangent is an [odd function](https://algebrica.org/even-and-odd-functions/), meaning that:
  $$arctan ⁡ \left(\right. - x \left.\right) = - arctan ⁡ \left(\right. x \left.\right) \forall x \in \mathbb{R}$$ This follows directly from the fact that the tangent is itself an odd function, and reflects the symmetry of the graph of $arctan$ with respect to the origin.

> A [bijective function](https://algebrica.org/functions/) is both injective and surjective, that is, if for every $y \in B$ there exists a unique $x \in A$ such that $f \left(\right. x \left.\right) = y$.

## Analytical expression of the arctangent

The arctangent can also be written using the [sine and cosine](https://algebrica.org/sine-and-cosine) functions, which highlights its geometric foundation within the unit circle and its connection with the other inverse trigonometric functions. Starting from the identity:
$$tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{cos ⁡ \left(\right. \theta \left.\right)}$$
one can consider a [right triangle](https://algebrica.org/right-triangle-trigonometry/) in which the angle $\theta$ satisfies $tan ⁡ \left(\right. \theta \left.\right) = x$, that is, the ratio of the opposite side to the adjacent side equals $x$. Taking the adjacent side equal to $1$ and the opposite side equal to $x$, the hypotenuse is $\sqrt{1 + x^{2}}$ by the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/), so that:

$$sin ⁡ \left(\right. \theta \left.\right) = \frac{x}{\sqrt{1 + x^{2}}}$$
$$cos ⁡ \left(\right. \theta \left.\right) = \frac{1}{\sqrt{1 + x^{2}}}$$

Reversing these relationships yields two equivalent expressions for the arctangent:
$$arctan ⁡ \left(\right. x \left.\right) = arcsin \left(\right. \frac{x}{\sqrt{1 + x^{2}}} \left.\right)$$
$$arctan ⁡ \left(\right. x \left.\right) = arccos \left(\right. \frac{1}{\sqrt{1 + x^{2}}} \left.\right)$$

> This equivalence is often useful in calculus and in analytical derivations, because it allows expressions involving the arctangent to be rewritten in terms of the [arcsine or arccosine](https://algebrica.org/arcsine-and-arccosine/), depending on which form simplifies the computation.

## Addition formula for the arctangent

The arctangent satisfies a notable identity that expresses the arctangent of a sum in terms of the individual arctangents. For any two real numbers $x$ and $y$ satisfying $x y < 1$, the following identity holds:

$$arctan ⁡ \left(\right. x \left.\right) + arctan ⁡ \left(\right. y \left.\right) = arctan \left(\right. \frac{x + y}{1 - x y} \left.\right)$$

This formula follows directly from the addition formula for the tangent function. If $\alpha = arctan ⁡ \left(\right. x \left.\right)$ and $\beta = arctan ⁡ \left(\right. y \left.\right)$, then $tan ⁡ \left(\right. \alpha \left.\right) = x$ and $tan ⁡ \left(\right. \beta \left.\right) = y$, and the tangent addition formula gives:

$$tan ⁡ \left(\right. \alpha + \beta \left.\right) = \frac{tan ⁡ \left(\right. \alpha \left.\right) + tan ⁡ \left(\right. \beta \left.\right)}{1 - tan ⁡ \left(\right. \alpha \left.\right) tan ⁡ \left(\right. \beta \left.\right)} = \frac{x + y}{1 - x y}$$

Applying the arctangent to both sides then yields the identity. The condition $x y < 1$ ensures that $\alpha + \beta \in \left(\right. - \pi / 2 , \pi / 2 \left.\right)$, which is the principal interval of the arctangent; when $x y > 1$, a correction term of $\pm \pi$ must be added depending on the sign of $x$.

---

A particularly useful special case arises by setting $y = 1 / x$ with $x > 0$, so that $x y = 1$. In this situation the general formula does not apply directly, but one can verify the result by observing that $arctan ⁡ \left(\right. x \left.\right)$ and $arctan \left(\right. 1 / x \left.\right)$ are complementary angles. The identity takes the form:

$$arctan ⁡ \left(\right. x \left.\right) + arctan \left(\right. \frac{1}{x} \left.\right) = \frac{\pi}{2} \left(\right. x > 0 \left.\right)$$

This follows from the fact that for $x > 0$ one has $arccot \left(\right. x \left.\right) = arctan \left(\right. 1 / x \left.\right)$, and the complementarity relation $arctan ⁡ \left(\right. x \left.\right) + arccot \left(\right. x \left.\right) = \pi / 2$ holds for all positive $x$.

## Arccotangent definition

In the [unit circle](https://algebrica.org/unit-circle), the [cotangent](https://algebrica.org/tangent-and-cotangent) of an angle $\theta$ can be visualized as the length of the segment tangent to the circle at the point where the terminal side meets it, measured along the horizontal tangent line at $\left(\right. 0 , 1 \left.\right)$. The arccotangent performs the reverse process: given a real number $x$, it returns the unique angle $\theta$ in the interval $\left(\right. 0 , \pi \left.\right)$ whose cotangent equals $x$. This geometric relationship illustrates how the cotangent and arccotangent are interconnected as a function and its inverse, each reversing the role of angle and ratio.

![Arccotangent.](https://algebrica.org/wp-content/uploads/resources/images/arccotangent-2.png "Arccotangent.")

By relating the arccotangent to the concept of a [function](https://algebrica.org/functions), we can formally express the relationship between cotangent and arccotangent as follows:

$$arccot \left(\right. x \left.\right) = \theta \Longleftrightarrow cot ⁡ \left(\right. \theta \left.\right) = x$$
$$\theta \in \left(\right. 0 , \pi \left.\right)$$

The arccotangent establishes a correspondence between a real number $x$ and the unique angle $\theta$ in the interval $\left(\right. 0 , \pi \left.\right)$ whose cotangent equals $x$. The restriction to this interval is necessary because the cotangent function is periodic and therefore not injective over its full domain; by confining it to $\left(\right. 0 , \pi \left.\right)$, one obtains a strictly decreasing bijection, which admits a well-defined [inverse](https://algebrica.org/inverse-function/). This reciprocal relationship is summarized by the identity:
$$cot ⁡ \left(\right. arccot \left(\right. x \left.\right) \left.\right) = x \text{for all} x \in \mathbb{R}$$

- When the cotangent value $x$ is positive, the corresponding angle $\theta$ lies in the first quadrant.
- when $x$ is negative, the angle lies in the second quadrant; and when $x = 0$, the angle equals $\frac{\pi}{2}$.

As $x$ grows without bound, the corresponding angle $\theta$ approaches the asymptotic values:

$$\underset{x \rightarrow + \infty}{lim} arccot \left(\right. x \left.\right) = 0$$
$$\underset{x \rightarrow - \infty}{lim} arccot \left(\right. x \left.\right) = \pi$$

These values are never attained, since no finite value of $x$ has cotangent equal to $0$ or $\pi$; they correspond to the directions in which the terminal side of the angle becomes parallel to the x-axis.

## Reference values of arccotangent

Below are some commonly known values of $arccot \left(\right. x \left.\right)$ for selected inputs, useful in various applications of trigonometry:
$$x & \rightarrow - \infty & & arccot \left(\right. x \left.\right) \rightarrow \pi \\ x & = - \sqrt{3} & & arccot \left(\right. - \sqrt{3} \left.\right) = 2 \pi / 3 \\ x & = - 1 & & arccot \left(\right. - 1 \left.\right) = 3 \pi / 4 \\ x & = - 1 / \sqrt{3} & & arccot \left(\right. - 1 / \sqrt{3} \left.\right) = 5 \pi / 6 \\ x & = 0 & & arccot \left(\right. 0 \left.\right) = \pi / 2 \\ x & = 1 / \sqrt{3} & & arccot \left(\right. 1 / \sqrt{3} \left.\right) = \pi / 3 \\ x & = 1 & & arccot \left(\right. 1 \left.\right) = \pi / 4 \\ x & = \sqrt{3} & & arccot \left(\right. \sqrt{3} \left.\right) = \pi / 6 \\ x & \rightarrow + \infty & & arccot \left(\right. x \left.\right) \rightarrow 0$$

## Arccotangent function

The arccotangent function $f \left(\right. x \left.\right) = arccot \left(\right. x \left.\right)$ assigns to each real number $x \in \mathbb{R}$ the unique angle $\theta \in \left(\right. 0 , \pi \left.\right)$ whose cotangent equals $x$. Its graph is a continuous, strictly decreasing curve that admits two horizontal asymptotes, namely $y = 0$ and $y = \pi$. The function is the [inverse](https://algebrica.org/inverse-function/) of the cotangent restricted to its principal domain $\left(\right. 0 , \pi \left.\right)$, over which the cotangent is strictly decreasing and bijective.

- Domain: $x \in \mathbb{R}$
- Range: $y \in \left(\right. 0 , \pi \left.\right)$
- The arccotangent satisfies the identity:
  $$arccot \left(\right. - x \left.\right) = \pi - arccot \left(\right. x \left.\right) \forall x \in \mathbb{R}$$
  This follows from the fact that the cotangent is an odd function, and reflects the symmetry of the graph of $arccot$ with respect to the point $\left(\right. 0 , \pi / 2 \left.\right)$.

## Analytical expression of the arccotangent

The arccotangent can also be expressed in relation to the arctangent, sine, and cosine functions, emphasizing its complementary nature within the family of inverse trigonometric functions. Starting from the identity:

$$cot ⁡ \left(\right. \theta \left.\right) = \frac{cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)}$$

one can consider a right triangle in which $cot ⁡ \left(\right. \theta \left.\right) = x$, that is, the ratio of the adjacent side to the opposite side equals $x$. Taking the opposite side equal to $1$ and the adjacent side equal to $x ,$ the hypotenuse is $\sqrt{1 + x^{2}}$ by the Pythagorean theorem, so that:

$$sin ⁡ \left(\right. \theta \left.\right) = \frac{1}{\sqrt{1 + x^{2}}}$$
$$cos ⁡ \left(\right. \theta \left.\right) = \frac{x}{\sqrt{1 + x^{2}}}$$

Reversing these relationships yields two equivalent expressions for the arccotangent:
$$arccot \left(\right. x \left.\right) & = arcsin \left(\right. \frac{1}{\sqrt{1 + x^{2}}} \left.\right) \\ arccot \left(\right. x \left.\right) & = arccos \left(\right. \frac{x}{\sqrt{1 + x^{2}}} \left.\right)$$

Two further identities connect the arccotangent directly to the arctangent. For positive values of $x$, one has:

$$arccot \left(\right. x \left.\right) = arctan \left(\right. \frac{1}{x} \left.\right)$$

since the cotangent and tangent of the same angle are reciprocals of each other. A more general identity, valid for all $x \in \mathbb{R}$, is:
$$arccot \left(\right. x \left.\right) = \frac{\pi}{2} - arctan ⁡ \left(\right. x \left.\right)$$

which follows from the complementary relationship between tangent and cotangent: for any angle $\theta$, one has $cot ⁡ \left(\right. \theta \left.\right) = tan \left(\right. \frac{\pi}{2} - \theta \left.\right)$, so inverting both sides yields the identity directly.

expressions with arccosexpressions with arcsinrelations between functionssymmetry propertiescomplement identityaddition formulareference valuesrange arccotdomain arccotrange arctandomain arctanarccotangent functionarctangent functioninverse cotangentinverse tangentprincipal interval arccotprincipal interval arctanarccotangentarctangentpropertiesfunctionsdefinitions
