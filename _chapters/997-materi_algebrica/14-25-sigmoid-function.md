---
layout: chapter
title: "Sigmoid Function"
chapter: "Functions"
chapter_order: 14
section_order: 25
permalink: /materi-algebrica/functions/sigmoid-function/
---

applicationsprobabilistic interpretationlogitinverse functionhyperbolic tangentlogistic functiongrowth behaviourinflection pointconcavitysecond derivativederivative formfirst derivativebijectivitymonotonicityasymptotic behaviourdomain and rangeexponential formdefinitionrelations and applicationsanalysisdefinition and structure

## Definition

The sigmoid function is a real-valued [function](https://algebrica.org/functions/) of a real variable that takes values strictly between $0$ and $1$, approaching each of the two extremes [asymptotically](https://algebrica.org/asymptotes/). It provides a smooth mapping from the real line to the unit interval and is widely used in analysis and machine learning. Its definition is the following:

$$\sigma \left(\right. x \left.\right) = \frac{1}{1 + e^{- x}}$$

The sigmoid function can be written in equivalent forms that are sometimes more convenient for computation or for establishing certain properties. One such form is obtained by multiplying both numerator and denominator by $e^{x}$:

$$\sigma \left(\right. x \left.\right) = \frac{e^{x}}{e^{x} + 1}$$

This expression is entirely equivalent to the original definition and can simplify certain algebraic manipulations.

![Sigmoid function.](https://algebrica.org/wp-content/uploads/resources/images/sigmoid-function.png "Sigmoid function.")

- The [domain](https://algebrica.org/determining-the-domain-of-a-function/) is $\mathbb{R}$, while the range is the open interval $\left(\right. 0 , 1 \left.\right)$.
- The function is strictly increasing on $\mathbb{R}$, since its [derivative](https://algebrica.org/derivatives/) is always positive, and is therefore bijective from $\mathbb{R}$ onto $\left(\right. 0 , 1 \left.\right)$.
- The function has no local extrema and exactly one [inflection point](https://algebrica.org/maximum-minimum-and-inflection-points/) at $\left(\right. 0 , \frac{1}{2} \left.\right)$.
- The [limits](https://algebrica.org/limits/) at infinity are the following: $$\underset{x \rightarrow - \infty}{lim} \sigma \left(\right. x \left.\right) = 0$$ $$\underset{x \rightarrow + \infty}{lim} \sigma \left(\right. x \left.\right) = 1$$

> The S-shaped curve reflects the behaviour of the function: slow growth for very negative values of $x$, a rapid transition in a neighbourhood of the origin, and saturation for very positive values.

## Properties of the sigmoid function

The following properties characterise the sigmoid function analytically and justify its widespread use in both mathematical analysis and applications. The function satisfies the following symmetry relation with respect to the origin:

$$\sigma \left(\right. - x \left.\right) = 1 - \sigma \left(\right. x \left.\right)$$

This identity, which can be verified by direct substitution, implies that the graph of $\sigma$ is symmetric about the point:

$$\left(\right. 0 , \frac{1}{2} \left.\right)$$

The value of the function at the origin is:

$$\sigma \left(\right. 0 \left.\right) = \frac{1}{1 + e^{0}} = \frac{1}{2}$$

The limits at the extremes of the real line are the following:

$$\underset{x \rightarrow - \infty}{lim} \sigma \left(\right. x \left.\right) = 0$$
$$\underset{x \rightarrow + \infty}{lim} \sigma \left(\right. x \left.\right) = 1$$

The lines $y = 0$ and $y = 1$ are therefore [horizontal asymptotes](https://algebrica.org/asymptotes/) of the graph.

## Derivative of the sigmoid function

One of the most notable properties of the sigmoid function is that its derivative can be expressed in a remarkably compact form in terms of the function itself. The first derivative is the following:

$$\sigma^{'} \left(\right. x \left.\right) = \sigma \left(\right. x \left.\right) \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right)$$

To verify this identity one may proceed by direct computation. Writing $\sigma \left(\right. x \left.\right) = \left(\right. 1 + e^{- x} \left.\right)^{- 1}$ and applying the chain rule gives the following:

$$\sigma^{'} \left(\right. x \left.\right) = \frac{e^{- x}}{\left(\right. 1 + e^{- x} \left.\right)^{2}}$$

Observing that the numerator can be written as $\left(\right. 1 + e^{- x} \left.\right) - 1$, the expression separates into the product:

$$\sigma^{'} \left(\right. x \left.\right) & = \frac{1}{1 + e^{- x}} \cdot \frac{e^{- x}}{1 + e^{- x}} \\ & = \sigma \left(\right. x \left.\right) \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right)$$

Since $\sigma \left(\right. x \left.\right) \in \left(\right. 0 , 1 \left.\right)$ for every $x \in \mathbb{R}$, the derivative is always strictly positive, confirming that the function is [strictly increasing](https://algebrica.org/increasing-and-decreasing-functions/). The maximum value of the derivative is attained at $x = 0$, where $\sigma^{'} \left(\right. 0 \left.\right) = 1 / 4$.

## Second derivative and concavity

The second derivative of the sigmoid function is obtained by differentiating the expression:
$$\sigma^{'} \left(\right. x \left.\right) = \sigma \left(\right. x \left.\right) \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right)$$

Applying the product rule and substituting the expression for $\sigma^{'} \left(\right. x \left.\right)$ gives the following:

$$\sigma^{'} ` \left(\right. x \left.\right) & = \sigma^{'} \left(\right. x \left.\right) , \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right) - \sigma \left(\right. x \left.\right) \sigma^{'} \left(\right. x \left.\right) \\ & = \sigma^{'} \left(\right. x \left.\right) \left(\right. 1 - 2 \sigma \left(\right. x \left.\right) \left.\right) \\ & = \sigma \left(\right. x \left.\right) \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right) \left(\right. 1 - 2 \sigma \left(\right. x \left.\right) \left.\right)$$

The sign of $\sigma^{''} \left(\right. x \left.\right)$ is determined entirely by the factor $1 - 2 \sigma \left(\right. x \left.\right)$, since $\sigma \left(\right. x \left.\right) \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right) > 0$ for all $x \in \mathbb{R}$. Since $\sigma$ is strictly increasing and $\sigma \left(\right. 0 \left.\right) = \frac{1}{2}$, the factor $1 - 2 \sigma \left(\right. x \left.\right)$ is positive for $x < 0$ and negative for $x > 0$.

![](https://algebrica.org/wp-content/uploads/resources/images/sigmoid-function-second-derivative-1-1024x558.png "Sigmoid function, second derivative.")

It follows that the function is concave upward on $\left(\right. - \infty , 0 \left.\right)$ and concave downward on $\left(\right. 0 , + \infty \left.\right)$. The point $x = 0$ is therefore an inflection point, at which $\sigma^{''} \left(\right. 0 \left.\right) = 0$ and the concavity changes sign.

## Relation to the logistic function

The sigmoid function coincides with the special case of the logistic function in which the growth rate equals $1$ and the inflection point is located at the origin. The general form of the logistic function is the following:

$$f \left(\right. x \left.\right) = \frac{L}{1 + e^{- k \left(\right. x - x_{0} \left.\right)}}$$

In this expression $L$ denotes the upper asymptotic value, $k$ the growth rate, and $x_{0}$ the inflection point. The standard sigmoid function corresponds to the choice $L = 1$, $k = 1$, and $x_{0} = 0$.

## Relation to the hyperbolic tangent

The sigmoid function is closely related to the [hyperbolic tangent](https://algebrica.org/hyperbolic-tangent-and-cotangent/) $tanh .$ The following identity holds:

$$\sigma \left(\right. x \left.\right) = \frac{1 + tanh \left(\right. \frac{x}{2} \left.\right)}{2}$$

An equivalent form is the following:

$$tanh ⁡ \left(\right. x \left.\right) = 2 \sigma \left(\right. 2 x \left.\right) - 1$$

This relation shows that the two functions differ essentially by a vertical translation and a rescaling. While the sigmoid maps $\mathbb{R}$ into the interval $\left(\right. 0 , 1 \left.\right)$, the hyperbolic tangent maps $\mathbb{R}$ into the interval $\left(\right. - 1 , 1 \left.\right)$. Both functions exhibit the same S-shaped curve and the same type of saturation at the extremes.

## Inverse of the sigmoid function

Since the sigmoid function is strictly monotone, it admits an inverse function defined on $\left(\right. 0 , 1 \left.\right)$. This inverse is known as the logit function, and its expression is the following:

$$\sigma^{- 1} \left(\right. p \left.\right) = ln \left(\right. \frac{p}{1 - p} \left.\right)$$

The argument of the [logarithm](https://algebrica.org/logarithms/) is called the odds ratio. The logit function therefore maps a probability $p \in \left(\right. 0 , 1 \left.\right)$ to the corresponding real value on the log-odds scale.

## Example

Consider the problem of computing the value of the sigmoid function at $x = 2$ and verifying that its derivative at that point is consistent with the formula $\sigma^{'} \left(\right. x \left.\right) = \sigma \left(\right. x \left.\right) \left(\right. 1 - \sigma \left(\right. x \left.\right) \left.\right)$. The value of the function is the following:

$$\sigma \left(\right. 2 \left.\right) = \frac{1}{1 + e^{- 2}}$$

Since $e^{- 2} \approx 0.1353$, one obtains:

$$\sigma \left(\right. 2 \left.\right) \approx \frac{1}{1.1353} \approx 0.8808$$

Applying the derivative formula, the value of $\sigma^{'} \left(\right. 2 \left.\right)$ is the following:

$$\sigma^{'} \left(\right. 2 \left.\right) = \sigma \left(\right. 2 \left.\right) , \left(\right. 1 - \sigma \left(\right. 2 \left.\right) \left.\right) \approx 0.8808 \cdot 0.1192 \approx 0.1050$$

The value of the derivative of the sigmoid function at $x = 2$ is therefore approximately $0.1050$, confirming both the formula and the fact that the function grows very slowly in that region, having already approached saturation.
