---
layout: chapter
title: "Tangent Function"
chapter: "Functions"
chapter_order: 14
section_order: 20
permalink: /materi-algebrica/functions/tangent-function/
---

## Tangent function

The tangent function $f \left(\right. x \left.\right) = tan ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, expressed in radians, its corresponding [tangent](https://algebrica.org/tangent-and-cotangent) value. Its graph is a periodic curve with a period of $\pi$ and features vertical [asymptotes](https://algebrica.org/asymptotes/) where the cosine of $x$ equals zero, specifically at $x = \pi / 2 + k \pi$ for $k \in \mathbb{Z}$. The function $f \left(\right. x \left.\right) = tan ⁡ \left(\right. x \left.\right)$ has a [domain](https://algebrica.org/determining-the-domain-of-a-function/) of all real numbers except these points, and its range is all real numbers.

![](https://algebrica.org/wp-content/uploads/resources/images/tangent-function.png)

A useful way to read this graph is to keep in mind that the tangent is defined as
 $$tan ⁡ \left(\right. x \left.\right) = \frac{sin ⁡ \left(\right. x \left.\right)}{cos ⁡ \left(\right. x \left.\right)}$$
Thinking of it as a ratio helps make sense of the curve: the tangent varies gently where the underlying [sine and cosine](https://algebrica.org/sine-and-cosine/) change smoothly, while it rises or falls sharply as the cosine approaches zero, shaping the overall appearance of the graph.

###### The graph also shows that near the origin the tangent function behaves almost like a straight line: for small values of $x$, $tan ⁡ \left(\right. x \left.\right)$ increases smoothly before its growth becomes more pronounced as it approaches the discontinuities.

## Properties

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $x \in \mathbb{R} : x \neq \frac{\pi}{2} + k \pi \text{for all} k \in \mathbb{Z}$
- Range: $y \in \mathbb{R}$
- Periodicity: periodic in $x$ with period $\pi$
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $tan ⁡ \left(\right. - x \left.\right) = - tan ⁡ \left(\right. x \left.\right)$
- Roots: $x = \pi n , n \in \mathbb{Z}$
- [Integer](https://algebrica.org/integers/) root: $x = 0$

## Limits, derivatives, and integrals of the tangent function

The tangent of $x$ is defined as the ratio between the [sine and cosine](https://algebrica.org/sine-and-cosine) of the angle $x$.
$$tan ⁡ \left(\right. x \left.\right) = \frac{sin ⁡ \left(\right. x \left.\right)}{cos ⁡ \left(\right. x \left.\right)}$$

---

A useful limit to remember is:
$$\underset{x \rightarrow 0}{lim} \frac{tan ⁡ \left(\right. x \left.\right)}{x} = 1$$
which shows that, near the origin, the tangent behaves almost like the function $x$. The behaviour of the tangent near its first vertical asymptote is also well described by limits. As $x$ approaches $\pi / 2$ from the left, the function grows without bound:
$$\underset{x \rightarrow \left(\frac{\pi}{2}\right)^{-}}{lim} tan ⁡ \left(\right. x \left.\right) = + \infty$$
Coming from the right, the values instead diverge negatively:
$$\underset{x \rightarrow \left(\frac{\pi}{2}\right)^{+}}{lim} tan ⁡ \left(\right. x \left.\right) = - \infty$$

---

The function is [continuous](https://algebrica.org/continuous-functions/) and differentiable on its domain.
The [derivative](https://algebrica.org/derivatives) is:
$$\frac{d}{d x} tan ⁡ \left(\right. x \left.\right) = sec^{2} ⁡ \left(\right. x \left.\right)$$

---

The [indefinite integral](https://algebrica.org/indefinite-integrals/) is:
$$\int tan ⁡ \left(\right. x \left.\right) d x = - ln ⁡ \left|\right. cos ⁡ \left(\right. x \left.\right) \left|\right. + c$$

##### A comprehensive overview of trigonometric integrals, together with the most useful transformation and substitution techniques for handling more complex cases, is available in the page on [trigonometric function integrals](https://algebrica.org/integral-of-trigonometric-functions/).

---

An alternative form of the function $tan ⁡ \left(\right. x \left.\right)$ using imaginary numbers is given by Euler’s formula. Here, $e^{i x}$ is the [exponential function](https://algebrica.org/exponential-function) with base $e$ and $i$ is the [imaginary](https://algebrica.org/complex-numbers) unit:
$$tan ⁡ \left(\right. x \left.\right) = \frac{e^{i x} - e^{- i x}}{i \left(\right. e^{i x} + e^{- i x} \left.\right)}$$
