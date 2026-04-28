---
layout: chapter
title: "Sine Function"
chapter: "Functions"
chapter_order: 14
section_order: 18
permalink: /materi-algebrica/functions/sine-function/
---

## Sine function

The sine function $f \left(\right. x \left.\right) = sin ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, expressed in radians, its corresponding [sine](https://algebrica.org/sine-and-cosine) value. Its graph is a periodic wave with a period of $2 \pi$ and an amplitude of 1, oscillating between $- 1$ and $1$. The function $f \left(\right. x \left.\right) = cos ⁡ x$ has all real numbers in its [domain](https://algebrica.org/determining-the-domain-of-a-function/), but its range is $- 1 \leq cos ⁡ \left(\right. x \left.\right) \leq 1$.

![](https://algebrica.org/wp-content/uploads/resources/images/sine-cosine-3-1.png)

##### Together with the [cosine function](https://algebrica.org/cosine-function), it represents one of the fundamental models of periodic waves, and is widely used to describe cyclic phenomena in physics, engineering, and mathematics. For example, in simple [harmonic motion](https://algebrica.org/simple-harmonic-motion/) in physics, the sine function typically appears in the equations for both displacement and [velocity](https://algebrica.org/velocity), describing the oscillatory behavior of systems like springs and pendulums.

## Properties

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $x \in \mathbb{R}$
- Range: $y \in \mathbb{R} : - 1 \leq y \leq 1$
- Periodicity: periodic in $x$ with period $2 \pi$
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $sin ⁡ \left(\right. - x \left.\right) = - sin ⁡ \left(\right. x \left.\right)$
- Roots: $x = \pi n , n \in \mathbb{Z}$
- [Integer](https://algebrica.org/integers/) root: $x = 0$
- [Maximum and minimum points](https://algebrica.org/maximum-minimum-and-inflection-points/): $sin ⁡ \left(\right. x \left.\right)$ reaches its maximum $1$ at $x = \frac{\pi}{2} + 2 k \pi$ with $k \in \mathbb{Z}$ and its minimum $- 1$ at $x = \frac{3 \pi}{2} + 2 k \pi$ with $k \in \mathbb{Z}$.

## Limits, derivatives, and integrals of the cosine function

A fundamental [limit](https://algebrica.org/limits/) involving the sine function captures how $sin ⁡ \left(\right. x \left.\right)$ behaves in a neighbourhood of the origin and plays a central role in differential calculus. As $x$ approaches zero, the value of $sin ⁡ \left(\right. x \left.\right)$ becomes increasingly close to $x$ itself when both are measured in radians. This reflects the fact that, near the origin, the sine curve is almost indistinguishable from the line $y = x$. This relationship is formalised through the following limit:

$$\text{1}. \underset{x \rightarrow 0}{lim} \frac{sin ⁡ \left(\right. x \left.\right)}{x} = 1$$

---

The function $sin ⁡ \left(\right. x \left.\right)$ is [continuous](https://algebrica.org/continuous-functions/) and differentiable for every real value of $x$. Its behaviour is smooth and regular across the entire real line, with no points of discontinuity or non-differentiability. Moreover, since $sin ⁡ \left(\right. x \left.\right)$ is differentiable everywhere, its [derivative](https://algebrica.org/derivatives/) is defined at all real numbers and is given by:

$$2. \frac{d}{d x} sin ⁡ \left(\right. x \left.\right) = cos ⁡ \left(\right. x \left.\right)$$

---

Since the derivative of $- cos ⁡ \left(\right. x \left.\right)$ is $sin ⁡ \left(\right. x \left.\right)$, the [indefinite integral](https://algebrica.org/indefinite-integrals/) of the sine function can be written as:
$$3. \int sin ⁡ \left(\right. x \left.\right) d x = - cos ⁡ \left(\right. x \left.\right) + c$$

##### A comprehensive overview of trigonometric integrals, together with the most useful transformation and substitution techniques for handling more complex cases, is available in the page on [trigonometric function integrals](https://algebrica.org/integral-of-trigonometric-functions/).

---

An alternative form of the function $sin ⁡ \left(\right. x \left.\right)$ using imaginary numbers is given by Euler’s formula, where $e^{i x}$ is the [exponential function](https://algebrica.org/exponential-function) with base $e$ and $I$ is the [imaginary](https://algebrica.org/complex-numbers) unit:
$$4. sin ⁡ \left(\right. x \left.\right) = \frac{e^{i x} - e^{- i x}}{2 i}$$
