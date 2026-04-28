---
layout: chapter
title: "Exponential Function"
chapter: "Functions"
chapter_order: 14
section_order: 15
permalink: /materi-algebrica/functions/exponential-function/
---

exponential modelshyperbolic functionsgrowth hierarchyasymptotic growthlimitsgeneralized formsintegralderivativenatural exponentialinverse logarithmdifferentiabilitycontinuitydomain and rangegrowth rateconstant casedecreasing caseincreasing casey-interceptpositive baseextensionspropertiesbehavior

## Introduction

The exponential function is a [function](https://algebrica.org/functions/) of the form:

$$f \left(\right. x \left.\right) = a^{x} , a \in \mathbb{R}^{+} , a \neq 1$$

In general, for any base $a > 0$, the graph of the exponential function $y = a^{x}$ always intersects the y-axis at the point $\left(\right. 0 , 1 \left.\right)$, because $a^{0} = 1$. It lies entirely above the x-axis, since $a^{x} > 0$ for all $x \in \mathbb{R}$ and never intersects the x-axis; in other words, $a^{x} \neq 0$ for any real $x$. The behavior of the function depends on the value of the base $a$, and three cases are distinguished.

## Properties for $a > 1$

When $a > 1$, the exponential function $y = a^{x}$ is strictly increasing over $\mathbb{R}$.

![Exponential function.](https://algebrica.org/wp-content/uploads/resources/images/exp-function-2.png "Exponential function.")

- [Domain](https://algebrica.org/determining-the-domain-of-a-function/): $\mathbb{R}$.
- Range: $\mathbb{R}^{+}$.
- Monotonicity: the function is strictly increasing over $\mathbb{R}$.
- The function is bijective from $\mathbb{R}$ to $\mathbb{R}^{+}$.
- The function is [continuous](https://algebrica.org/continuous-functions/) and differentiable over $\mathbb{R}$.
- The function has no [maximum or minimum points](https://algebrica.org/maximum-minimum-and-inflection-points/).
- Limits as $x$ approaches the extremes of the domain:
  $$\underset{x \rightarrow - \infty}{lim} a^{x} & = 0^{+} \\ \underset{x \rightarrow + \infty}{lim} a^{x} & = + \infty$$

##### When $a > 1$, the exponential function grows without bound as $x \rightarrow + \infty$ and approaches zero from above as $x \rightarrow - \infty$. Each unit increase in $x$ multiplies the value of the function by the constant factor $a$.

## Properties for $0 < a < 1$

When $0 < a < 1$, the exponential function $y = a^{x}$ is strictly decreasing over $\mathbb{R}$.

![Exponential function.](https://algebrica.org/wp-content/uploads/resources/images/exp-function-1.png "Exponential function.")

- Domain: $\mathbb{R}$.
- Range: $\mathbb{R}^{+}$.
- Monotonicity: the function is strictly decreasing over $\mathbb{R}$.
- The function is bijective from $\mathbb{R}$ to $\mathbb{R}^{+}$.
- The function is continuous and differentiable over $\mathbb{R}$.
- The function has no maximum or minimum points.
- Limits as $x$ approaches the extremes of the domain:
  $$\underset{x \rightarrow - \infty}{lim} a^{x} & = + \infty \\ \underset{x \rightarrow + \infty}{lim} a^{x} & = 0^{+}$$

##### When $0 < a < 1$, the exponential function decreases without bound as $x \rightarrow - \infty$ and approaches zero from above as $x \rightarrow + \infty$. Each unit increase in $x$ multiplies the value of the function by the constant factor $a$, which is less than one.

## Properties for $a = 1$

When $a = 1$, the exponential function reduces to the constant function $y = 1^{x} = 1$, which is excluded from the standard definition. Its graph is a horizontal line at height $y = 1$.

![Exponential function.](https://algebrica.org/wp-content/uploads/resources/images/exp-function-3.png "Exponential function.")

- Domain: $\mathbb{R}$.
- Range: $\left{\right. 1 \left.\right}$.
- Monotonicity: the function is constant over $\mathbb{R}$.
- The function is continuous and differentiable over $\mathbb{R}$.

## Connection with the logarithmic function

The exponential function $y = a^{x}$ is the inverse of the [logarithmic function](https://algebrica.org/logarithmic-function) $y = log_{a} ⁡ \left(\right. x \left.\right)$, provided $a > 0$ and $a \neq 1$. This inverse relationship means:

$$a^{log_{a} ⁡ \left(\right. x \left.\right)} = x$$
$$log_{a} ⁡ \left(\right. a^{x} \left.\right) = x$$

When the base $a$ equals Euler’s number $e \approx 2.71828$, the function is known as the natural exponential function:

$$f \left(\right. x \left.\right) = e^{x}$$

It is the unique function that is equal to its own derivative at every point:

$$\frac{d}{d x} e^{x} = e^{x}$$

This property makes $e^{x}$ a fundamental object in calculus and the theory of differential equations. The same function appears in the definition of the [exponential distribution](https://algebrica.org/exponential-distribution), which models the waiting time between events occurring at a constant rate.

## Generalized exponential functions

Three cases arise when the base or the exponent is replaced by a function of $x$.

- If the function has the form $y = \left[\right. f \left(\right. x \left.\right) \left]\right.^{g \left(\right. x \left.\right)}$, it is defined at those points where $f \left(\right. x \left.\right) > 0$ and $g \left(\right. x \left.\right)$ is defined.
- If the function has the form $y = a^{f \left(\right. x \left.\right)}$ with $a > 0$ and $a \neq 1$, it is defined wherever $f \left(\right. x \left.\right)$ is defined.
- If the function has the form $y = \left[\right. f \left(\right. x \left.\right) \left]\right.^{a}$, the domain condition depends on the sign of the exponent: the function is defined for $f \left(\right. x \left.\right) \geq 0$ when $a \in \mathbb{R}^{+}$, and for $f \left(\right. x \left.\right) > 0$ when $a \in \mathbb{R}^{-}$.

## Limit, derivative and integral

The fundamental [limit](https://algebrica.org/limits) associated with the natural exponential function is:

$$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1}{x} = 1$$

This limit expresses the fact that the derivative of $e^{x}$ at the origin equals one, consistently with $\frac{d}{d x} e^{x} = e^{x}$. For a general base $a > 0$, $a \neq 1$, the corresponding limit is:

$$\underset{x \rightarrow 0}{lim} \frac{a^{x} - 1}{x} = ln ⁡ \left(\right. a \left.\right)$$

---

The [derivative](https://algebrica.org/derivatives) of the exponential function follows directly from the fundamental limit above. Differentiating $a^{x}$ with respect to $x$ gives:

$$\frac{d}{d x} a^{x} = a^{x} ln ⁡ \left(\right. a \left.\right)$$

$$\frac{d}{d x} e^{x} = e^{x}$$

---

The [integral of the exponential function](https://algebrica.org/integral-of-the-exponential-function/) is obtained by reversing the differentiation formulas above:

$$\int a^{x} d x = \frac{a^{x}}{ln ⁡ \left(\right. a \left.\right)} + c$$

$$\int e^{x} d x = e^{x} + c$$

## Asymptotic growth

A fundamental property of the exponential function is that it grows faster than any polynomial or power function, and slower than the [factorial](https://algebrica.org/factorial/). More precisely, for any $a > 1$ and any $k > 0$:

$$\underset{x \rightarrow + \infty}{lim} \frac{x^{k}}{a^{x}} = 0 \underset{x \rightarrow + \infty}{lim} \frac{a^{x}}{x !} = 0$$

This establishes the following hierarchy of growth rates as $x \rightarrow + \infty$:

$$log ⁡ x \ll x^{k} \ll a^{x} \ll x !$$

The table below illustrates this hierarchy for $a = 2$.

| $x$ | $log_{2} ⁡ x$ | $x^{2}$ | $2^{x}$ | $x !$ |
| --- | --- | --- | --- | --- |
| 1 | 0 | 1 | 2 | 1 |
| 2 | 1 | 4 | 4 | 2 |
| 4 | 2 | 16 | 16 | 24 |
| 8 | 3 | 64 | 256 | 40,320 |
| 16 | 4 | 256 | 65,536 | 2.09 × 10¹³ |
| 32 | 5 | 1024 | 4.29 × 10⁹ | 2.63 × 10³⁵ |

##### The hierarchy $log ⁡ x \ll x^{k} \ll a^{x} \ll x !$ is a central result in [asymptotic](https://algebrica.org/asymptotes/) analysis and appears throughout computer science, where it underlies the classification of algorithm complexity in terms of time and space requirements.

## Hyperbolic functions derived from the exponential function

The exponential function provides the natural foundation for defining the hyperbolic functions, which appear in many areas of analysis and geometry. The three fundamental ones are the [hyperbolic sine and cosine](https://algebrica.org/hyperbolic-sine-and-cosine/) and the hyperbolic tangent, defined as follows:

$$cosh ⁡ \left(\right. x \left.\right) = \frac{e^{x} + e^{- x}}{2} x \in \mathbb{R}$$

$$sinh ⁡ \left(\right. x \left.\right) = \frac{e^{x} - e^{- x}}{2} x \in \mathbb{R}$$

$$tanh ⁡ \left(\right. x \left.\right) = \frac{sinh ⁡ \left(\right. x \left.\right)}{cosh ⁡ \left(\right. x \left.\right)} x \in \mathbb{R} tanh ⁡ \left(\right. x \left.\right) \in \left(\right. - 1 , 1 \left.\right)$$

Because they are defined through the exponential function, hyperbolic functions are smooth and differentiable over $\mathbb{R}$. Note that $tanh ⁡ \left(\right. x \left.\right)$ is bounded, unlike $sinh ⁡ \left(\right. x \left.\right)$ and $cosh ⁡ \left(\right. x \left.\right)$, which grow without bound as $x \rightarrow \pm \infty$.

##### Their definitions mirror those of the trigonometric functions, with the key difference that $cosh$ and $sinh$ parametrize the unit [hyperbola](https://algebrica.org/hyperbola/) $x^{2} - y^{2} = 1$ rather than the unit circle $x^{2} + y^{2} = 1$.
