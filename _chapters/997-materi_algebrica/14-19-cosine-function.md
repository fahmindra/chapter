---
layout: chapter
title: "Cosine Function"
chapter: "Functions"
chapter_order: 14
section_order: 19
permalink: /materi-algebrica/functions/cosine-function/
---

## Cosine function

The cosine [function](https://algebrica.org/functions/) $f \left(\right. x \left.\right) = cos ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, expressed in radians, its corresponding [cosine](https://algebrica.org/sine-and-cosine/) value. Its graph is a periodic wave with a period of $2 \pi$ and an amplitude of 1, oscillating between $- 1$ and $1$. The function $f \left(\right. x \left.\right) = cos ⁡ x$ has all real numbers in its [domain](https://algebrica.org/determining-the-domain-of-a-function/), but its range is $- 1 \leq cos ⁡ \left(\right. x \left.\right) \leq 1$.

![](https://algebrica.org/wp-content/uploads/resources/images/sine-cosine-4.png)

##### Together with the [sine function](https://algebrica.org/sine-function/), it represents one of the fundamental models of periodic waves, and is widely used to describe cyclic phenomena in physics, engineering, and mathematics. For example, in simple [harmonic motion](https://algebrica.org/simple-harmonic-motion/) in physics, the cosine function often appears in the equations for displacement and [acceleration](https://algebrica.org/acceleration/), describing the oscillatory behavior of systems like springs and pendulums.

## Properties

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $x \in \mathbb{R}$
- Range: $y \in \mathbb{R} : - 1 \leq y \leq 1$
- Periodicity: periodic in $x$ with period $2 \pi$
- Parity: [even](https://algebrica.org/even-and-odd-functions/), $cos ⁡ \left(\right. - x \left.\right) = cos ⁡ \left(\right. x \left.\right)$
- Roots: $x = \frac{\pi}{2} + n \pi , n \in \mathbb{Z}$
- [Integer](https://algebrica.org/integers/) root: $x = \frac{\pi}{2}$
- [Maximum and minimum points](https://algebrica.org/maximum-minimum-and-inflection-points/): $cos ⁡ \left(\right. x \left.\right)$ reaches its $1$ at $x = 2 k \pi$ with $k \in \mathbb{Z}$ and its minimum $- 1$ at $x = \pi + 2 k \pi$ with $k \in \mathbb{Z}$.

## Limits, derivatives, and integrals of the cosine function

A fundamental [limit](https://algebrica.org/limits) involving the cosine function is: $$\underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ \left(\right. x \left.\right)}{x} = 0$$

---

The function is [continuous](https://algebrica.org/continuous-functions/) and differentiable at all real numbers. The [derivative](https://algebrica.org/derivatives) is:
$$\frac{d}{d x} cos ⁡ \left(\right. x \left.\right) = - sin ⁡ \left(\right. x \left.\right)$$

---

[Indefinite integral](https://algebrica.org/indefinite-integrals/):
$$\int cos ⁡ \left(\right. x \left.\right) d x = sin ⁡ \left(\right. x \left.\right) + c$$

##### A comprehensive overview of trigonometric integrals, together with the most useful transformation and substitution techniques for handling more complex cases, is available in the page on [trigonometric function integrals](https://algebrica.org/integral-of-trigonometric-functions/).

---

An alternative form of the function $cos ⁡ \left(\right. x \left.\right)$ using imaginary numbers is given by Euler’s formula, where $e^{i x}$ is the [exponential function](https://algebrica.org/exponential-function) with base $e$ and $i$ is the [imaginary](https://algebrica.org/complex-numbers) unit:
$$cos ⁡ \left(\right. x \left.\right) = \frac{e^{i x} + e^{- i x}}{2}$$
