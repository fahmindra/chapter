---
layout: chapter
title: "Arcsine and Arccosine"
chapter: "Trigonometry"
chapter_order: 5
section_order: 5
permalink: /materi-algebrica/trigonometry/arcsine-and-arccosine/
---

## Arcsine

The arcsine is the inverse of the [sine](https://algebrica.org/sine-and-cosine) function. Given a number $x \in \left[\right. - 1 , 1 \left]\right.$ (i.e., the range of values the sine function can attain), $arcsin ⁡ \left(\right. x \left.\right)$ is defined as the angle $\theta$ in the interval $\left[\right. - \pi / 2 , \pi / 2 \left]\right.$ whose sine is equal to $x$. In general, an [inverse function](https://algebrica.org/inverse-function/) reverses the operation of the original: if a function $f$ maps a value $x$ to a value $y$, then its inverse $f^{- 1}$ maps $y$ back to $x$. The sine function takes an angle and returns a real number in $\left[\right. - 1 , 1 \left]\right.$ and the arcsine does the opposite, returning the angle whose sine equals the given value. This inverse relationship is expressed by the identity:

$$sin ⁡ \left(\right. arcsin ⁡ \left(\right. x \left.\right) \left.\right) = x \forall x \in \left[\right. - 1 , 1 \left]\right.$$

![](https://algebrica.org/wp-content/uploads/resources/images/arc-sin-1.png "Arcsine.")

In formal terms, the definition of the arcsine is the following:

$$arcsin ⁡ \left(\right. x \left.\right) = \theta \Longleftrightarrow sin ⁡ \left(\right. \theta \left.\right) = x \text{and} \theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$$

The restriction of $\theta$ to the interval $\left[\right. - \pi / 2 , \pi / 2 \left]\right.$ is necessary because the sine function is not injective on its full [domain](https://algebrica.org/determining-the-domain-of-a-function/). Without this restriction, the inverse would not be well-defined.

## Example

Consider the computation of $arcsin \left(\right. \frac{1}{2} \left.\right)$. We seek the angle $\theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$ such that $sin ⁡ \left(\right. \theta \left.\right) = \frac{1}{2}$. From the standard values of the sine function, we know that:

$$sin \left(\right. \frac{\pi}{6} \left.\right) = \frac{1}{2}$$

Since $\frac{\pi}{6}$ belongs to the interval $\left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$, it satisfies all the conditions required by the definition.

We conclude that:
$$arcsin \left(\right. \frac{1}{2} \left.\right) = \frac{\pi}{6}$$

## Common values of the arcsine

The following table collects the standard values of $arcsin ⁡ \left(\right. x \left.\right)$ for the most frequently encountered inputs:

$$x & = - 1 & & arcsin ⁡ \left(\right. - 1 \left.\right) = - \pi / 2 \\ x & = - \sqrt{3} / 2 & & arcsin ⁡ \left(\right. - \sqrt{3} / 2 \left.\right) = - \pi / 3 \\ x & = - 1 / 2 & & arcsin ⁡ \left(\right. - 1 / 2 \left.\right) = - \pi / 6 \\ x & = 0 & & arcsin ⁡ \left(\right. 0 \left.\right) = 0 \\ x & = 1 / 2 & & arcsin ⁡ \left(\right. 1 / 2 \left.\right) = \pi / 6 \\ x & = \sqrt{3} / 2 & & arcsin ⁡ \left(\right. \sqrt{3} / 2 \left.\right) = \pi / 3 \\ x & = 1 & & arcsin ⁡ \left(\right. 1 \left.\right) = \pi / 2$$

## Arccosine

The arccosine is the inverse of the [cosine](https://algebrica.org/sine-and-cosine) function. Given a number $x \in \left[\right. - 1 , 1 \left]\right.$ (i.e., the range of values the cosine function can attain), $arccos ⁡ \left(\right. x \left.\right)$ is defined as the angle $\theta$ in the interval $\left[\right. 0 , \pi \left]\right.$ whose cosine is equal to $x$. As with the arcsine, the restriction of the codomain to $\left[\right. 0 , \pi \left]\right.$ is necessary to ensure that the inverse is well-defined, since the cosine function is not injective on its full domain. The corresponding identity is:

$$cos ⁡ \left(\right. arccos ⁡ \left(\right. x \left.\right) \left.\right) = x \text{for all} x \in \left[\right. - 1 , 1 \left]\right.$$

![](https://algebrica.org/wp-content/uploads/resources/images/arc-cos.png)

In formal terms, the definition of the arccosine is the following:

$$arccos ⁡ \left(\right. x \left.\right) = \theta \text{if and only if} cos ⁡ \left(\right. \theta \left.\right) = x \text{and} \theta \in \left[\right. 0 , \pi \left]\right.$$

## Common values of the arccosine

The following table collects the standard values of $arccos ⁡ \left(\right. x \left.\right)$ for the most frequently encountered inputs:

$$x & = - 1 & & arccos ⁡ \left(\right. - 1 \left.\right) = \pi \\ x & = - \sqrt{3} / 2 & & arccos ⁡ \left(\right. - \sqrt{3} / 2 \left.\right) = 5 \pi / 6 \\ x & = - 1 / 2 & & arccos ⁡ \left(\right. - 1 / 2 \left.\right) = 2 \pi / 3 \\ x & = 0 & & arccos ⁡ \left(\right. 0 \left.\right) = \pi / 2 \\ x & = 1 / 2 & & arccos ⁡ \left(\right. 1 / 2 \left.\right) = \pi / 3 \\ x & = \sqrt{3} / 2 & & arccos ⁡ \left(\right. \sqrt{3} / 2 \left.\right) = \pi / 6 \\ x & = 1 & & arccos ⁡ \left(\right. 1 \left.\right) = 0$$

## Properties of the arcsine and arccosine

The arcsine and arccosine functions are related by the following identity, which holds for every $x \in \left[\right. - 1 , 1 \left]\right.$:

$$arcsin ⁡ \left(\right. x \left.\right) + arccos ⁡ \left(\right. x \left.\right) = \frac{\pi}{2}$$

This identity reflects the complementary nature of the two functions: since the sine and cosine of complementary angles are equal, the angle whose sine is $x$ and the angle whose cosine is $x$ always sum to $\pi / 2$.

---

A second property worth noting concerns the composition of a function with its inverse. One direction is straightforward: applying the arcsine after the sine, or the arccosine after the cosine, recovers the original value, provided the argument lies in the appropriate interval. Formally:

$$sin ⁡ \left(\right. arcsin ⁡ \left(\right. x \left.\right) \left.\right) = x \forall x \in \left[\right. - 1 , 1 \left]\right.$$

$$cos ⁡ \left(\right. arccos ⁡ \left(\right. x \left.\right) \left.\right) = x \forall x \in \left[\right. - 1 , 1 \left]\right.$$

The opposite composition, however, does not hold in general. For an arbitrary angle $\theta$, one has:

$$arcsin ⁡ \left(\right. sin ⁡ \left(\right. \theta \left.\right) \left.\right) = \theta \Longleftrightarrow \theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$$

$$arccos ⁡ \left(\right. cos ⁡ \left(\right. \theta \left.\right) \left.\right) = \theta \Longleftrightarrow \theta \in \left[\right. 0 , \pi \left]\right.$$

> Outside these intervals, the arcsine and arccosine return the unique representative of $\theta$ within their respective ranges, not $\theta$ itself. This asymmetry is a direct consequence of the domain restrictions imposed to make the inverses well-defined, and it is what distinguishes a true inverse from a mere left or right inverse.

## Arcsine and arccosine functions

The arcsine function $f \left(\right. x \left.\right) = arcsin ⁡ \left(\right. x \left.\right)$ assigns to each value $x \in \left[\right. - 1 , 1 \left]\right.$ the angle $\theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$ whose sine equals $x$. Its graph is a continuous, strictly increasing curve.

![](https://algebrica.org/wp-content/uploads/resources/images/arcsin-function.png)

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $x \in \left[\right. - 1 , 1 \left]\right.$
- Range: $y \in \left[\right. - \pi / 2 , \pi / 2 \left]\right.$
- Periodicity: the arcsine function is not periodic.
- Parity: the function is [odd](https://algebrica.org/even-and-odd-functions/), satisfying $arcsin ⁡ \left(\right. - x \left.\right) = - arcsin ⁡ \left(\right. x \left.\right)$.

---

The arccosine function $f \left(\right. x \left.\right) = arccos ⁡ \left(\right. x \left.\right)$ assigns to each value $x \in \left[\right. - 1 , 1 \left]\right.$ the angle $\theta \in \left[\right. 0 , \pi \left]\right.$ whose cosine equals $x$. Its graph is a continuous, strictly decreasing curve.

![](https://algebrica.org/wp-content/uploads/resources/images/arccos-function.png)

- Domain: $x \in \left[\right. - 1 , 1 \left]\right.$
- Range: $y \in \left[\right. 0 , \pi \left]\right.$
- Periodicity: the arccosine function is not periodic.
- Parity: the function is neither odd nor even, but satisfies the identity $arccos ⁡ \left(\right. - x \left.\right) = \pi - arccos ⁡ \left(\right. x \left.\right)$.

comparisonsfunction behaviorinverse mappingunit circleangle interpretationstandard valuesgraphssymmetry relationsnon periodicityparitycontinuitymonotonicityrangedomainprincipal valuesrange selectiondomain restrictionarccosine definitionarcsine definitionrepresentationspropertiesstructure
