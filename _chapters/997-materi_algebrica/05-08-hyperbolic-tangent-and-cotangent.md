---
layout: chapter
title: "Hyperbolic Tangent and Cotangent"
chapter: "Trigonometry"
chapter_order: 5
section_order: 8
permalink: /materi-algebrica/trigonometry/hyperbolic-tangent-and-cotangent/
---

## Introduction

The hyperbolic tangent and cotangent arise from the hyperbolic sine and cosine in exactly the same way that the circular [tangent and cotangent](https://algebrica.org/tangent-and-cotangent/) arise from the circular [sine and cosine](https://algebrica.org/sine-and-cosine/). Given the [hyperbolic sine and cosine](https://algebrica.org/hyperbolic-sine-and-cosine/), both introduced in relation to the right branch of the equilateral [hyperbola](https://algebrica.org/hyperbola/):

$$X^{2} – Y^{2} = 1$$

The hyperbolic tangent is defined as their ratio, provided that $cosh ⁡ \left(\right. x \left.\right)$ is not zero. Since $cosh ⁡ \left(\right. x \left.\right) \geq 1$ for all real $x$, the denominator is never zero, and the hyperbolic tangent is therefore defined on the entire real line. The hyperbolic cotangent involves the reciprocal ratio and requires $sinh ⁡ \left(\right. x \left.\right) \neq 0$, which excludes only $x = 0$.

Once the point $P \left(\right. cosh ⁡ \left(\right. x \left.\right) , sinh ⁡ \left(\right. x \left.\right) \left.\right)$ on the hyperbola has been identified as the one corresponding to a signed hyperbolic sector of area $x / 2$, the hyperbolic tangent and cotangent can be read from its coordinates. The hyperbolic tangent is the ratio of the vertical coordinate to the horizontal coordinate:

$$tanh ⁡ \left(\right. x \left.\right) := \frac{sinh ⁡ \left(\right. x \left.\right)}{cosh ⁡ \left(\right. x \left.\right)}$$

![](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-thangent.png "hyperbolic tangent")

> To make the construction more intuitive, consider the unit hyperbola $x^{2} - y^{2} = 1$ and the point $P = \left(\right. cosh ⁡ x , sinh ⁡ x \left.\right)$, associated with a hyperbolic angle $x$. Draw the [line](https://algebrica.org/lines/) passing through the origin $O$ and $P$, and consider the vertical line $x = 1$. Their intersection defines the point $T$, which has coordinates $T = \left(\right. 1 , tanh ⁡ x \left.\right)$, since the slope of the line $O P$ is $sinh ⁡ x / cosh ⁡ x = tanh ⁡ x$. The vertical segment joining $\left(\right. 1 , 0 \left.\right)$ to $T$ therefore represents geometrically the length of the hyperbolic tangent.

---

The hyperbolic cotangent is the reciprocal ratio, that is, the horizontal coordinate divided by the vertical one:

$$coth ⁡ \left(\right. x \left.\right) := \frac{cosh ⁡ \left(\right. x \left.\right)}{sinh ⁡ \left(\right. x \left.\right)}$$

![Hyperbolic cotangent.](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-cotangent-1.png "Hyperbolic cotangent.")

> As in the case illustrated above for the hyperbolic tangent, to make the construction more intuitive, consider the unit hyperbola $x^{2} - y^{2} = 1$ and the point $P = \left(\right. cosh ⁡ x , sinh ⁡ x \left.\right)$, associated with a hyperbolic angle $x$. Draw the [line](https://algebrica.org/lines/) passing through the origin $O$ and $P$, and consider the horizontal line $y = 1$. Their intersection defines the point $S$, which has coordinates $S = \left(\right. coth ⁡ x , 1 \left.\right)$, since the slope of the line $O P$ is $sinh ⁡ x / cosh ⁡ x = tanh ⁡ x$, and thus its reciprocal gives $coth ⁡ x = cosh ⁡ x / sinh ⁡ x$. The horizontal segment joining $\left(\right. 0 , 1 \left.\right)$ to $S$ therefore represents geometrically the length of the hyperbolic cotangent.

---

In this geometric picture, the hyperbolic tangent and cotangent measure a kind of slope of the point on the hyperbola relative to its two coordinates, in analogy with the way the circular tangent expresses the slope of the point on the [unit circle](https://algebrica.org/unit-circle/).

## Fundamental hyperbolic identity for tangent and cotangent

The hyperbolic tangent and cotangent satisfy an identity that follows directly from the [fundamental hyperbolic identity](https://algebrica.org/hyperbolic-sine-and-cosine/). Starting from:

$$cosh^{2} ⁡ \left(\right. x \left.\right) – sinh^{2} ⁡ \left(\right. x \left.\right) = 1$$

and dividing both sides by $cosh^{2} ⁡ \left(\right. x \left.\right)$, which is always positive, we obtain the identity for the hyperbolic tangent:

$$1 – tanh^{2} ⁡ \left(\right. x \left.\right) = \frac{1}{cosh^{2} ⁡ \left(\right. x \left.\right)}$$

Analogously, dividing the fundamental identity by $sinh^{2} ⁡ \left(\right. x \left.\right)$ for $x \neq 0$ gives the identity for the hyperbolic cotangent:

$$coth^{2} ⁡ \left(\right. x \left.\right) – 1 = \frac{1}{sinh^{2} ⁡ \left(\right. x \left.\right)}$$

Both identities record a direct consequence of the hyperbola equation: the coordinates of the point $P$ are constrained to satisfy $X^{2} – Y^{2} = 1$, and dividing by either coordinate squared translates this constraint into a relation involving the ratio functions.

## Hyperbolic identities

- $$\text{1}. tanh ⁡ \left(\right. x + y \left.\right) = \frac{tanh ⁡ \left(\right. x \left.\right) + tanh ⁡ \left(\right. y \left.\right)}{1 + tanh ⁡ \left(\right. x \left.\right) tanh ⁡ \left(\right. y \left.\right)}$$
- $$\text{2}. tanh ⁡ \left(\right. x - y \left.\right) = \frac{tanh ⁡ \left(\right. x \left.\right) – tanh ⁡ \left(\right. y \left.\right)}{1 – tanh ⁡ \left(\right. x \left.\right) tanh ⁡ \left(\right. y \left.\right)}$$
- $$\text{3}. tanh ⁡ \left(\right. 2 x \left.\right) = \frac{2 tanh ⁡ \left(\right. x \left.\right)}{1 + tanh^{2} ⁡ \left(\right. x \left.\right)}$$
- $$\text{4}. coth ⁡ \left(\right. x + y \left.\right) = \frac{1 + coth ⁡ \left(\right. x \left.\right) coth ⁡ \left(\right. y \left.\right)}{coth ⁡ \left(\right. x \left.\right) + coth ⁡ \left(\right. y \left.\right)}$$
- $$\text{5}. coth ⁡ \left(\right. x - y \left.\right) = \frac{- 1 + coth ⁡ \left(\right. x \left.\right) coth ⁡ \left(\right. y \left.\right)}{coth ⁡ \left(\right. x \left.\right) – coth ⁡ \left(\right. y \left.\right)}$$
- $$\text{6}. tanh ⁡ \left(\right. x \left.\right) coth ⁡ \left(\right. x \left.\right) = 1$$

> The addition and subtraction formulas for the hyperbolic tangent and cotangent closely mirror their circular counterparts, but are governed by the algebra of the equilateral hyperbola. The last identity simply states that $tanh$ and $coth$ are reciprocal functions wherever both are defined.

## Analytical expression of the hyperbolic tangent

Using the analytical expressions of the hyperbolic sine and cosine in terms of the [exponential function](https://algebrica.org/exponential-function/), we can write the hyperbolic tangent directly. Substituting:

$$sinh ⁡ \left(\right. x \left.\right) = \frac{e^{x} – e^{- x}}{2}$$
$$cosh ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{2}$$

into the definition $tanh ⁡ \left(\right. x \left.\right) = sinh ⁡ \left(\right. x \left.\right) / cosh ⁡ \left(\right. x \left.\right)$ and simplifying the factor $1 / 2$ that appears in both numerator and denominator, we obtain:

$$tanh ⁡ \left(\right. x \left.\right) = \frac{e^{x} – e^{- x}}{e^{x} + e^{- x}}$$

An equivalent and often more compact form is obtained by multiplying numerator and denominator by $e^{- x}$:

$$tanh ⁡ \left(\right. x \left.\right) = \frac{1 – e^{- 2 x}}{1 + e^{- 2 x}}$$

or, equivalently, by multiplying by $e^{x}$:

$$tanh ⁡ \left(\right. x \left.\right) = \frac{e^{2 x} – 1}{e^{2 x} + 1}$$

All three expressions are equivalent and each makes apparent a different aspect of the function: in the first form, the numerator and denominator are the analytically defined [hyperbolic sine and cosine](https://algebrica.org/hyperbolic-sine-and-cosine/) themselves. In the latter two, the exponential growth as $x \rightarrow + \infty$ or $x \rightarrow - \infty$ becomes immediately visible, and from them one can read off at once that the function tends to $1$ and $- 1$ respectively.

## Analytical expression of the hyperbolic cotangent

The derivation of the analytical expression for the hyperbolic cotangent follows the same pattern. Substituting the expressions of $sinh ⁡ \left(\right. x \left.\right)$ and $cosh ⁡ \left(\right. x \left.\right)$ into the definition $coth ⁡ \left(\right. x \left.\right) = cosh ⁡ \left(\right. x \left.\right) / sinh ⁡ \left(\right. x \left.\right)$, and again cancelling the common factor $1 / 2$, we get:

$$coth ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{e^{x} – e^{- x}}$$

As before, multiplying numerator and denominator by $e^{- x}$ or by $e^{x}$ gives the equivalent forms:

$$coth ⁡ \left(\right. x \left.\right) = \frac{1 + e^{- 2 x}}{1 – e^{- 2 x}} = \frac{e^{2 x} + 1}{e^{2 x} – 1}$$

The latter expressions show that for large positive $x$ the function approaches $1$ from above, while for large negative $x$ it approaches $- 1$ from below, with a vertical asymptote at $x = 0$ in both cases.

## Hyperbolic tangent and cotangent functions

The hyperbolic tangent function $f \left(\right. x \left.\right) = tanh ⁡ \left(\right. x \left.\right)$ is defined for all real numbers. Unlike the circular tangent, it does not have vertical [asymptotes](https://algebrica.org/asymptotes/): its graph is a smooth, monotonically increasing curve that passes through the origin with slope $1$ and remains bounded for all $x$. As $x \rightarrow + \infty$ the function approaches $1$ asymptotically, while as $x \rightarrow - \infty$ it approaches $- 1$, so the range is the open interval $\left(\right. - 1 , 1 \left.\right)$.

![Hyperbolic tangent function.](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-thangent-function-2.png "Hyperbolic tangent function.")

- Domain: $x \in \mathbb{R}$
- Range: $y \in \left(\right. - 1 , 1 \left.\right)$
- Periodicity: not periodic
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $tanh ⁡ \left(\right. - x \left.\right) = - tanh ⁡ \left(\right. x \left.\right)$
- Horizontal asymptotes: $y = 1$ as $x \rightarrow + \infty$; $y = - 1$ as $x \rightarrow - \infty$

---

The hyperbolic cotangent function $f \left(\right. x \left.\right) = coth ⁡ \left(\right. x \left.\right)$ is defined for all real $x \neq 0$. Its graph consists of two branches: one for $x > 0$, where the function decreases from $+ \infty$ toward $1$, and one for $x < 0$, where it increases from $- \infty$ toward $- 1$. The origin is a vertical asymptote, and the lines $y = 1$ and $y = - 1$ are horizontal asymptotes.

![Hyperbolic cotangent function.](https://algebrica.org/wp-content/uploads/resources/images/hyperbolic-cotangent-function-1.png "Hyperbolic cotangent function.")

- Domain: $x \in \mathbb{R} , ; x \neq 0$
- Range: $y \in \left(\right. - \infty , - 1 \left.\right) \cup \left(\right. 1 , + \infty \left.\right)$
- Periodicity: not periodic
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $coth ⁡ \left(\right. - x \left.\right) = - coth ⁡ \left(\right. x \left.\right)$
- Vertical asymptote: $x = 0$
- Horizontal asymptotes: $y = 1$ as $x \rightarrow + \infty$; $y = - 1$ as $x \rightarrow - \infty$

## Relation to the circular tangent and cotangent

The circular [tangent and cotangent](https://algebrica.org/tangent-and-cotangent/) are defined as ratios of the circular sine and cosine, which in turn arise from the geometry of the unit circle. By exact analogy, the hyperbolic tangent and cotangent are ratios of the hyperbolic sine and cosine, which arise from the geometry of the equilateral hyperbola. In both settings, the underlying identity constraining the coordinates of a point on the curve propagates to a corresponding identity for the ratio functions.

There is, however, a fundamental difference between the two cases: while the circular tangent is periodic with period $\pi$ and is unbounded, the hyperbolic tangent is monotone and bounded between $- 1$ and $1$. Similarly, the circular cotangent has vertical asymptotes at every integer multiple of $\pi$, whereas the hyperbolic cotangent has only one, at the origin.

> Both the circular and the hyperbolic tangent measure a kind of ratio of coordinates of a point on a curve, one on the unit circle and the other on the equilateral hyperbola. The structural parallelism between the two families of functions is one of the most elegant features of classical analysis.

paritymonotonicityasymptoteslimitsexponential formalgebraic relationsreciprocal relationaddition formulascoth identitytanh identityfundamental identityunit hyperbolageometric interpretationhyperbolic ratiocoth definitiontanh definitionanalysisidentitiesdefinitions
