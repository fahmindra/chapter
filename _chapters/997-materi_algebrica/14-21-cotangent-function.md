---
layout: chapter
title: "Cotangent Function"
chapter: "Functions"
chapter_order: 14
section_order: 21
permalink: /materi-algebrica/functions/cotangent-function/
---

## Cotangent function

The cotangent function $f \left(\right. x \left.\right) = cot ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, expressed in radians, its corresponding [cotangent](https://algebrica.org/tangent-and-cotangent) value. Its graph is a periodic curve with a period of $\pi$ and features vertical [asymptotes](https://algebrica.org/asymptotes) where the sine of $x$ equals zero, specifically at $x = k \pi$ for $k \in \mathbb{Z}$. The function $f \left(\right. x \left.\right) = cot ⁡ \left(\right. x \left.\right)$ has a [domain](https://algebrica.org/determining-the-domain-of-a-function/) of all real numbers except these points, and its range is all real numbers.

![](https://algebrica.org/wp-content/uploads/resources/images/cotangent-chart-1.png)

- Domain: $x \in \mathbb{R} : x \neq k \pi \text{for all} k \in \mathbb{Z}$
- Range: $y \in \mathbb{R}$
- Periodicity: periodic in $x$ with period $\pi$
- Parity: odd, $cot ⁡ \left(\right. - x \left.\right) = - cot ⁡ \left(\right. x \left.\right)$

---

- The cotangent of $x$ is defined as the ratio between the [cosine and sine](https://algebrica.org/sine-and-cosine) of the angle $x$.
  $$cot ⁡ \left(\right. x \left.\right) = \frac{cos ⁡ \left(\right. x \left.\right)}{sin ⁡ \left(\right. x \left.\right)}$$

---

- Roots: $x = \frac{\pi}{2} + \pi n , n \in \mathbb{Z}$
- Fundamental root: $x = \frac{\pi}{2}$

---

- Notable limits:

  $$\underset{x \rightarrow 0}{lim} x cot ⁡ \left(\right. x \left.\right) = 1$$

  $$\underset{x \rightarrow 0^{+}}{lim} cot ⁡ \left(\right. x \left.\right) = + \infty \text{and} \underset{x \rightarrow 0^{-}}{lim} cot ⁡ \left(\right. x \left.\right) = - \infty$$

---

- The function is [continuous](https://algebrica.org/continuous-functions/) and differentiable on its domain.
- [Derivative](https://algebrica.org/derivatives):
  $$\frac{d}{d x} cot ⁡ \left(\right. x \left.\right) = - csc^{2} ⁡ \left(\right. x \left.\right)$$

---

- [Indefinite integral](https://algebrica.org/indefinite-integrals/):
  $$\int cot ⁡ \left(\right. x \left.\right) d x = ln ⁡ \left|\right. sin ⁡ \left(\right. x \left.\right) \left|\right. + c$$

##### A comprehensive overview of trigonometric integrals, together with the most useful transformation and substitution techniques for handling more complex cases, is available in the page on [trigonometric function integrals](https://algebrica.org/integral-of-trigonometric-functions/).

---

- An alternative form of the function $cot ⁡ \left(\right. x \left.\right)$ using imaginary numbers is given by Euler’s formula. Here, $e^{i x}$ is the [exponential function](https://algebrica.org/exponential-function) with base $e$ and $i$ is the [imaginary](https://algebrica.org/complex-numbers) unit. By expressing sine and cosine as
  $$sin ⁡ \left(\right. x \left.\right) = \frac{e^{i x} - e^{- i x}}{2 i} \text{and} cos ⁡ \left(\right. x \left.\right) = \frac{e^{i x} + e^{- i x}}{2}$$ we obtain the cotangent function as
  $$cot ⁡ \left(\right. x \left.\right) = \frac{cos ⁡ \left(\right. x \left.\right)}{sin ⁡ \left(\right. x \left.\right)} = i \frac{e^{i x} + e^{- i x}}{e^{i x} - e^{- i x}} .$$
