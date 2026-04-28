---
layout: chapter
title: "Secant Function"
chapter: "Functions"
chapter_order: 14
section_order: 22
permalink: /materi-algebrica/functions/secant-function/
---

## Secant function

The [secant](https://algebrica.org/secant-and-cosecant/) function $f \left(\right. x \left.\right) = sec ⁡ \left(\right. x \left.\right)$ is defined as the reciprocal of the [cosine function](https://algebrica.org/cosine-function/). For any real angle $x$ (measured in radians), the secant takes the value:

$$sec ⁡ \left(\right. x \left.\right) = \frac{1}{cos ⁡ \left(\right. x \left.\right)}$$

as long as the $cos ⁡ \left(\right. x \left.\right) \neq 0 \left.\right)$. This reciprocal relationship means that the behaviour of the secant function is entirely determined by the properties of the cosine function.

###### This section focuses on the analytical properties of the secant function. For a geometric interpretation based on the [unit circle](https://algebrica.org/unit-circle/), including how the secant arises from the extension of the radius and the corresponding right–triangle construction, see the dedicated entry.

---

Its graph is a periodic curve with period $2 \pi$. Because cosine reaches the value zero at isolated and regularly spaced points, the secant function exhibits vertical [asymptotes](https://algebrica.org/asymptotes/) at:

$$x = \frac{\pi}{2} + k \pi k \in \mathbb{Z}$$

where the reciprocal $1 / cos ⁡ \left(\right. x \left.\right)$ becomes undefined.

![Secant graph with asymptotic behaviour.](https://algebrica.org/wp-content/uploads/resources/images/secant-1-1.png "Secant graph with asymptotic behaviour.")

These asymptotes separate the graph into distinct branches in which the function grows without bound as the angle approaches any of these points. The [domain](https://algebrica.org/determining-the-domain-of-a-function/) of $sec ⁡ \left(\right. x \left.\right)$ is therefore the set of all real numbers except the points where $cos ⁡ \left(\right. x \left.\right) = 0$. Its range consists of the unbounded intervals $\left(\right. - \infty , - 1 \left]\right. \cup \left[\right. 1 , \infty \left.\right)$ reflecting the fact that the cosine function never takes values whose absolute value exceeds $1$, making its reciprocal always greater than or equal to 1 in magnitude.

## Key properties

- Domain: $x \in \mathbb{R} : cos ⁡ \left(\right. x \left.\right) \neq 0 = x \in \mathbb{R} : x \neq \pi / 2 + k \pi \text{for all} k \in \mathbb{Z} .$
- Range: $y \in \left(\right. - \infty , - 1 \left]\right. \cup \left[\right. 1 , \infty \left.\right) .$
- Periodicity: periodic in $x$ with period $2 \pi .$
- Parity: [even](https://algebrica.org/even-and-odd-functions/), $sec ⁡ \left(\right. - x \left.\right) = sec ⁡ \left(\right. x \left.\right) .$
- The graph has vertical asymptotes at $x = \frac{\pi}{2} + k \pi .$

## Additional identity

There is a simple but meaningful relation that ties the secant and the [tangent](https://algebrica.org/tangent-function/) together. Starting from the [pythagorean identity](https://algebrica.org/pythagorean-identity/) for sine and cosine and rewriting everything in terms of cosine, we arrive at:

$$sec^{2} ⁡ \left(\right. x \left.\right) = 1 + tan^{2} ⁡ \left(\right. x \left.\right)$$

This identity shows how closely the two functions are linked: when the tangent becomes large, the secant grows as well, and both share the same vertical asymptotes. It is a handy relation that often appears in calculus, especially when dealing with derivatives, integrals, or trigonometric equations involving reciprocal functions.

## Limits, derivatives, and integrals of the secant function

Several limits help illustrate how the secant function behaves near key points of its domain. When the angle approaches values where the cosine is close to one, the secant remains bounded and approaches a finite value. As the angle nears those points at which the cosine tends to zero, the reciprocal grows without bound, giving rise to the vertical asymptotes characteristic of the function. These behaviours can be summarised through the following limits:

$$1. \underset{x \rightarrow 0}{lim} sec ⁡ \left(\right. x \left.\right) = 1$$
$$2. \underset{x \rightarrow \left(\frac{\pi}{2}\right)^{-}}{lim} sec ⁡ \left(\right. x \left.\right) = + \infty$$
$$3. \underset{x \rightarrow \left(\frac{\pi}{2}\right)^{+}}{lim} sec ⁡ \left(\right. x \left.\right) = - \infty$$

---

The secant function is [continuous](https://algebrica.org/continuous-functions/) and differentiable at every point where it is defined, that is, on the entire real line except at the angles where the cosine function vanishes. Within this domain it varies smoothly, and its rate of change follows from differentiating the reciprocal of the cosine. Using standard differentiation rules gives the derivative:

$$4. \frac{d}{d x} sec ⁡ \left(\right. x \left.\right) = sec ⁡ \left(\right. x \left.\right) tan ⁡ \left(\right. x \left.\right)$$

which expresses how the secant function grows or decreases depending on the combined behaviour of $sec ⁡ \left(\right. x \left.\right)$ and $tan ⁡ \left(\right. x \left.\right)$ at each point of its domain.

---

The antiderivative of the secant function can be obtained by a classical substitution that rewrites the integrand in a form suitable for logarithmic integration. This procedure leads to a compact expression involving both the secant and the tangent functions. The result is the following [indefinite integral](https://algebrica.org/indefinite-integral/):

$$5. \int sec ⁡ \left(\right. x \left.\right) d x = ln \left|\right. sec ⁡ \left(\right. x \left.\right) + tan ⁡ \left(\right. x \left.\right) \left|\right. + c$$

##### A comprehensive overview of trigonometric integrals, together with the most useful transformation and substitution techniques for handling more complex cases, is available in the page on [trigonometric function integrals](https://algebrica.org/integral-of-trigonometric-functions/).

---

An alternative expression for the function $sec ⁡ \left(\right. x \left.\right)$ can be obtained by rewriting the cosine in exponential form through [Euler’s](https://algebrica.org/euler-number-limit-sequence/) identity. This approach highlights the connection between trigonometric and complex exponential functions, and it often proves useful in contexts such as Fourier analysis or complex integration. Using the identity:

$$6. cos ⁡ \left(\right. x \left.\right) = \frac{e^{i x} + e^{- i x}}{2}$$

the secant function can be expressed as the reciprocal of this quantity, which yields:

$$7. sec ⁡ \left(\right. x \left.\right) = \frac{2}{ e^{i x} + e^{- i x} }$$

This formulation emphasises the analytic structure of $sec ⁡ \left(\right. x \left.\right)$ and provides a bridge between its trigonometric definition and its complex exponential representation.
