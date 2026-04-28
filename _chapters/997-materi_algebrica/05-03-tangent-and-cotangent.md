---
layout: chapter
title: "Tangent and Cotangent"
chapter: "Trigonometry"
chapter_order: 5
section_order: 3
permalink: /materi-algebrica/trigonometry/tangent-and-cotangent/
---

## Introduction

Tangent and cotangent are two trigonometric ratios derived from [sine and cosine](https://algebrica.org/sine-and-cosine). Given an oriented angle $\theta$, the tangent is defined as the ratio of the sine of $\theta$ to its cosine, and the cotangent as the reciprocal ratio:

$$tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{cos ⁡ \left(\right. \theta \left.\right)} cot ⁡ \left(\right. \theta \left.\right) = \frac{cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)}$$

Both admit a precise geometric interpretation on the [unit circle](https://algebrica.org/unit-circle), where they appear as signed lengths of segments associated with the terminal side of the angle. Unlike sine and cosine, which are defined for every real number, tangent and cotangent are not defined everywhere: the tangent is undefined where the cosine vanishes, and the cotangent where the sine vanishes.

## Tangent

Consider the unit circle centered at the origin $\text{O} = \left(\right. 0 , 0 \left.\right)$ with radius 1. Let $\theta$ be an angle in standard position, and denote by $\text{P}$ the point on the circle where the terminal side of $\theta$ intersects it.

- The point $\text{S} = \left(\right. 1 , 0 \left.\right)$ is where the circle meets the vertical line $x = 1$. The line through $\text{S}$ perpendicular to the $x$-axis is tangent to the [unit circle](https://algebrica.org/unit-circle) at $\text{S}$.
- Extend the ray from $\text{O}$ through $\text{P}$ until it meets this vertical tangent line at a point $\text{T}$.
- The signed length of the segment $\overset{―}{S T}$ defines the tangent of $\theta$:

$$tan ⁡ \left(\right. \theta \left.\right) = \overset{―}{S T}$$

![](https://algebrica.org/wp-content/uploads/resources/images/tangent-4.png)

From the definition, it follows that the trigonometric tangent is a numerical value representing a ratio, whereas the geometric tangent is a line. The two should not be confused: the trigonometric tangent quantifies the relationship between the [sine and cosine](https://algebrica.org/sine-and-cosine) of an angle, while the geometric tangent is the line touching a circle at exactly one point.

---

Triangles $\text{OST}$ and $\text{ORP}$ are similar by construction. Their proportionality gives:

$$\frac{\overset{―}{S T}}{\overset{―}{O S}} = \frac{\overset{―}{R P}}{\overset{―}{O R}}$$

![](https://algebrica.org/wp-content/uploads/resources/images/tangent-2-3.png)

By the definition of [sine and cosine](https://algebrica.org/sine-and-cosine), one has $\overset{―}{R P} = sin ⁡ \left(\right. \theta \left.\right)$ and $\overset{―}{O R} = cos ⁡ \left(\right. \theta \left.\right)$, so that:

$$tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{cos ⁡ \left(\right. \theta \left.\right)}$$

Since the cosine vanishes at $\theta = \frac{\pi}{2} + k \pi$ for every $k \in \mathbb{Z}$, the tangent is undefined at those values:

$$tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{cos ⁡ \left(\right. \theta \left.\right)} \theta \neq \frac{\pi}{2} + k \pi k \in \mathbb{Z}$$

## Common values of the tangent

The following table collects the values of $tan ⁡ \left(\right. x \left.\right)$ at the most frequently encountered angles, expressed in radians.

$$x & = - \pi / 3 & & tan ⁡ \left(\right. - \pi / 3 \left.\right) = - \sqrt{3} \\ x & = - \pi / 4 & & tan ⁡ \left(\right. - \pi / 4 \left.\right) = - 1 \\ x & = - \pi / 6 & & tan ⁡ \left(\right. - \pi / 6 \left.\right) = - 1 / \sqrt{3} \\ x & = 0 & & tan ⁡ \left(\right. 0 \left.\right) = 0 \\ x & = \pi / 6 & & tan ⁡ \left(\right. \pi / 6 \left.\right) = 1 / \sqrt{3} \\ x & = \pi / 4 & & tan ⁡ \left(\right. \pi / 4 \left.\right) = 1 \\ x & = \pi / 3 & & tan ⁡ \left(\right. \pi / 3 \left.\right) = \sqrt{3}$$

## Trigonometric identities for the tangent

- $$\text{1}. tan ⁡ \left(\right. x + y \left.\right) = \frac{tan ⁡ \left(\right. x \left.\right) + tan ⁡ \left(\right. y \left.\right)}{1 - tan ⁡ \left(\right. x \left.\right) tan ⁡ \left(\right. y \left.\right)}$$
- $$\text{2}. tan ⁡ \left(\right. x - y \left.\right) = \frac{tan ⁡ \left(\right. x \left.\right) - tan ⁡ \left(\right. y \left.\right)}{1 + tan ⁡ \left(\right. x \left.\right) tan ⁡ \left(\right. y \left.\right)}$$
- $$\text{3}. tan ⁡ \left(\right. 2 x \left.\right) = \frac{2 tan ⁡ \left(\right. x \left.\right)}{1 - tan^{2} ⁡ \left(\right. x \left.\right)}$$
- $$\text{4}. tan ⁡ \left(\right. \frac{x}{2} \left.\right) = \frac{sin ⁡ x}{1 + cos ⁡ x} = \frac{1 - cos ⁡ x}{sin ⁡ x}$$
- $$\text{5}. 1 + tan^{2} ⁡ \left(\right. x \left.\right) = sec^{2} ⁡ \left(\right. x \left.\right)$$
- $$\text{6}. tan ⁡ \left(\right. x \left.\right) cot ⁡ \left(\right. x \left.\right) = 1$$

> These identities describe how tangent behaves under angle addition, subtraction, doubling, halving, and reciprocal relationships. They complement the identities for sine and cosine and are especially useful when simplifying expressions or transforming trigonometric equations. For a broader overview, refer to the full collection of [trigonometric identities](https://algebrica.org/trigonometric-identities/).

## Cotangent

The reciprocal of the tangent is called the cotangent and is denoted by $cot ⁡ \left(\right. \theta \left.\right) .$ Geometrically, it corresponds to the signed length of a segment $\overset{―}{Z V}$ constructed on the horizontal tangent line at the top of the unit circle, in a manner analogous to the construction for the tangent. It can be expressed as:

$$cot ⁡ \left(\right. \theta \left.\right) = \frac{1}{tan ⁡ \left(\right. \theta \left.\right)} = \frac{cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)} = \overset{―}{Z V}$$

![](https://algebrica.org/wp-content/uploads/resources/images/cotangent-1.png)

Since the sine vanishes at $\theta = k \pi$ for every $k \in \mathbb{Z}$, the cotangent is undefined at those values:

$$cot ⁡ \left(\right. \theta \left.\right) = \frac{cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)} \theta \neq k \pi k \in \mathbb{Z}$$

## Common values of the cotangent

The following table collects the values of $cot ⁡ \left(\right. x \left.\right)$ at the most frequently encountered angles, expressed in radians.

$$x & = - \pi / 3 & & cot ⁡ \left(\right. - \pi / 3 \left.\right) = - 1 / \sqrt{3} \\ x & = - \pi / 4 & & cot ⁡ \left(\right. - \pi / 4 \left.\right) = - 1 \\ x & = - \pi / 6 & & cot ⁡ \left(\right. - \pi / 6 \left.\right) = - \sqrt{3} \\ x & = \pi / 6 & & cot ⁡ \left(\right. \pi / 6 \left.\right) = \sqrt{3} \\ x & = \pi / 4 & & cot ⁡ \left(\right. \pi / 4 \left.\right) = 1 \\ x & = \pi / 3 & & cot ⁡ \left(\right. \pi / 3 \left.\right) = 1 / \sqrt{3}$$

## Trigonometric identities for the cotangent

- $$\text{1}. cot ⁡ \left(\right. x + y \left.\right) = \frac{cot ⁡ \left(\right. x \left.\right) cot ⁡ \left(\right. y \left.\right) - 1}{cot ⁡ \left(\right. x \left.\right) + cot ⁡ \left(\right. y \left.\right)}$$
- $$\text{2}. cot ⁡ \left(\right. x - y \left.\right) = \frac{cot ⁡ \left(\right. x \left.\right) cot ⁡ \left(\right. y \left.\right) + 1}{cot ⁡ \left(\right. y \left.\right) - cot ⁡ \left(\right. x \left.\right)}$$
- $$\text{3}. cot ⁡ \left(\right. 2 x \left.\right) = \frac{cot^{2} ⁡ \left(\right. x \left.\right) - 1}{2 cot ⁡ \left(\right. x \left.\right)}$$
- $$\text{4}. cot ⁡ \left(\right. \frac{x}{2} \left.\right) = \frac{1 + cos ⁡ x}{sin ⁡ x}$$
- $$\text{5}. 1 + cot^{2} ⁡ \left(\right. x \left.\right) = csc^{2} ⁡ \left(\right. x \left.\right)$$

> These identities describe how cotangent behaves under angle addition, subtraction, doubling, halving, and reciprocal relationships.

## Tangent and cotangent functions

The [tangent function](https://algebrica.org/tangent-function/) $f \left(\right. x \left.\right) = tan ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, expressed in radians, its corresponding tangent value. Its graph is a periodic curve with period $\pi$, crossing the horizontal axis at every integer multiple of $\pi$ and displaying vertical [asymptotes](https://algebrica.org/asymptotes/) at $x = \pi / 2 + k \pi$ for $k \in \mathbb{Z}$, where the cosine vanishes. The [domain](https://algebrica.org/determining-the-domain-of-a-function/) of $tan ⁡ \left(\right. x \left.\right)$ consists of all [real numbers](https://algebrica.org/types-of-numbers) except these values, and its range is the entire real line.

![Tangent function.](https://algebrica.org/wp-content/uploads/resources/images/tangent-function-2.png "Tangent function.")

- Domain: $\left{\right. x \in \mathbb{R} : x \neq \frac{\pi}{2} + k \pi \text{for all} k \in \mathbb{Z} \left.\right}$
- Range: $y \in \mathbb{R}$
- Periodicity: periodic in $x$ with period $\pi$
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $tan ⁡ \left(\right. - x \left.\right) = - tan ⁡ \left(\right. x \left.\right)$

---

The [cotangent function](https://algebrica.org/cotangent-function) $f \left(\right. x \left.\right) = cot ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, expressed in radians, its corresponding cotangent value. Its graph is a periodic curve with period $\pi$, featuring vertical asymptotes at $x = k \pi$ for $k \in \mathbb{Z}$, where the sine vanishes. The domain excludes these points, and the range is the entire real line.

![Cotangent function.](https://algebrica.org/wp-content/uploads/resources/images/cotangent-function-1.png "Cotangent function.")

- Domain: $\left{\right. x \in \mathbb{R} : x \neq k \pi \text{for all} k \in \mathbb{Z} \left.\right}$
- Range: $y \in \mathbb{R}$
- Periodicity: periodic in $x$ with period $\pi$
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $cot ⁡ \left(\right. - x \left.\right) = - cot ⁡ \left(\right. x \left.\right)$

## Tangent and cotangent in the complex setting

In the theory of [complex numbers](https://algebrica.org/complex-numbers-introduction), the tangent and cotangent arise from the [trigonometric form](https://algebrica.org/complex-numbers-trigonometric-form) of a complex number. Any complex number $z = a + b i$ can be written as:

$$z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$$

where $r = \sqrt{a^{2} + b^{2}}$ is the modulus and $\theta$ is the argument. In this representation, the tangent of the argument satisfies:

$$tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{cos ⁡ \left(\right. \theta \left.\right)} = \frac{b / r}{a / r} = \frac{b}{a}$$

so that the tangent of the argument of a complex number coincides with the ratio of its imaginary part to its real part. This is the basis of the formula $\theta = arctan ⁡ \left(\right. b / a \left.\right)$, used to recover the argument from the Cartesian components of $z$.

A deeper connection emerges through the [exponential form](https://algebrica.org/complex-numbers-exponential-form). By Euler’s formula:

$$e^{i \theta} = cos ⁡ \theta + i sin ⁡ \theta$$

one can express the tangent entirely in terms of complex exponentials:

$$tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \theta}{cos ⁡ \theta} = \frac{e^{i \theta} - e^{- i \theta}}{i \left(\right. e^{i \theta} + e^{- i \theta} \left.\right)}$$

This expression mirrors the structure of the [hyperbolic tangent](https://algebrica.org/hyperbolic-tangent-and-cotangent), which is defined as $tanh ⁡ \left(\right. x \left.\right) = \left(\right. e^{x} - e^{- x} \left.\right) / \left(\right. e^{x} + e^{- x} \left.\right)$, and reveals that the two are related by the substitution $x \rightarrow i \theta$:

$$tan ⁡ \left(\right. \theta \left.\right) = - i tanh ⁡ \left(\right. i \theta \left.\right)$$

This identity reflects the deeper unity between circular and hyperbolic trigonometry, both of which emerge from the same exponential framework over the complex numbers.

## The Weierstrass substitution

The half-angle formula for the tangent is the starting point of one of the most useful techniques in [integral](https://algebrica.org/definite-integrals/) calculus, the Weierstrass substitution. The substitution is defined by:

$$t = tan \left(\right. \frac{x}{2} \left.\right)$$

From this assignment one derives the rational expressions of sine and cosine in terms of $t$:

$$sin ⁡ x & = \frac{2 t}{1 + t^{2}} \\ cos ⁡ x & = \frac{1 - t^{2}}{1 + t^{2}}$$

The differential transforms accordingly:

$$d x = \frac{2 d t}{1 + t^{2}}$$

Any integral whose integrand is a rational function of $sin ⁡ x$ and $cos ⁡ x$ becomes an integral of a rational function in the single variable $t$, which can be evaluated by [partial fraction decomposition](https://algebrica.org/partial-fraction-decomposition/). The half-angle identity thus connects trigonometric integration with the integration of rational functions.

complex settingfunction graphsparityasymptotesperiodicitytrigonometric identitiesangle representationsegment interpretationsimilar trianglesgeometric constructiontangent lineunit circleundefined valuesdomain restrictionsreciprocal relationratio of sine and cosinecotangenttangentpropertiesgeometrydefinitions
