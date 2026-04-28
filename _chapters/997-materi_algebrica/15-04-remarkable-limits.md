---
layout: chapter
title: "Remarkable Limits"
chapter: "Limits"
chapter_order: 15
section_order: 4
permalink: /materi-algebrica/limits/remarkable-limits/
---

approximationtaylor expansionderivative linklocal linearizationlittle-o notationasymptotic equivalencegrowth ratesinverse relationlogarithmic behaviordiscrete formcontinuous formdefinition of epower limitlogarithmic limitexponential limitcosine limittangent limitsine limitasymptoticsexponential and loglimits

## Introduction

Notable [limits](https://algebrica.org/limits/) play a central role in mathematical analysis. They are repeatedly used in calculations and help describe both the local behaviour of [functions](https://algebrica.org/functions) and their behaviour at infinity. The most important cases are collected below. They include trigonometric, exponential, and logarithmic expressions, as well as standard comparisons between quantities that grow without bound and those that tend to zero.

## The trigonometric fundamental limit

The most fundamental and structurally significant trigonometric limit is given by:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x} = 1$$

This result characterizes the local linearity of the [sine function](https://algebrica.org/sine-function/) at the origin and is equivalent to the following statement:

$$\left( \frac{d}{d x} sin ⁡ x \left|\right.\right)_{x = 0} = 1$$

From this limit, it follows directly that for any real constant a we have:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ \left(\right. a x \left.\right)}{a x} = 1$$
$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ \left(\right. a x \left.\right)}{x} = a$$

## The tangent limit

To evaluate the [tangent](https://algebrica.org/tangent-function/) limit, consider the following identity:

$$\frac{tan ⁡ x}{x} = \frac{sin ⁡ x}{x} \cdot \frac{1}{cos ⁡ x}$$

Applying the continuity of the cosine function at the origin yields:

$$\underset{x \rightarrow 0}{lim} \frac{tan ⁡ x}{x} = 1$$

More generally, for any real constant $a$ we have:

$$\underset{x \rightarrow 0}{lim} \frac{tan ⁡ \left(\right. a x \left.\right)}{x} = a$$

## The cosine limit

Quadratic, or second-order, behaviour emerges in the evaluation of this limit:

$$\underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ x}{x^{2}} = \frac{1}{2}$$

In this case, the numerator vanishes quadratically with respect to $x$, rather than linearly. The [cosine function](https://algebrica.org/cosine-function/) is tangent to the horizontal line $y = 1$ at the origin: its first derivative at $x = 0$ is zero, and the first non-vanishing term in its Taylor expansion is of order $x^{2}$. Indeed:
$$cos ⁡ x = 1 - \frac{x^{2}}{2} + o \left(\right. x^{2} \left.\right)$$

###### Here $o \left(\right. x^{2} \left.\right)$ denotes the [little-o notation](https://algebrica.org/little-o-notation/), meaning a term that becomes negligible compared to $x^{2}$ as $x \rightarrow 0$.

Dividing by $x^{2}$ isolates the leading quadratic term and yields the limit. More generally we have:

$$\underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ \left(\right. a x \left.\right)}{x^{2}} = \frac{a^{2}}{2}$$

## The exponential fundamental limit

The [exponential function](https://algebrica.org/exponential-function/) exhibits first-order behaviour near the origin: the deviation from the constant 1 is linear in $x$:
$$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1}{x} = 1$$
This limit reflects the fact that the derivative of $e^{x}$ at the origin equals one:
$$\left( \frac{d}{d x} e^{x} \left|\right.\right)_{x = 0} = 1$$
This result follows directly from the Taylor expansion of $e^{x}$ near the origin:
$$e^{x} = 1 + x + \frac{x^{2}}{2 !} + o \left(\right. x^{2} \left.\right)$$
from which dividing by $x$ and taking the limit immediately yields 1, as all higher-order terms vanish. More generally, for any real constant $a$ we have:
$$\underset{x \rightarrow 0}{lim} \frac{e^{a x} - 1}{x} = a$$
which follows by substituting $u = a x$ and reducing to the standard form.

###### Here $n !$ denotes the [factorial](https://algebrica.org/factorial/) of $n$, defined as the product of all positive integers up to $n$; in particular, $2 ! = 2$.

## The logarithmic fundamental limit

For the natural [logarithm](https://algebrica.org/logarithmic-function/), the following limit holds:
$$\underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x} = 1$$
This result corresponds to the derivative of $ln ⁡ x$ evaluated at $x = 1$:
$$\left( \frac{d}{d x} ln ⁡ x \left|\right.\right)_{x = 1} = 1$$
More generally, for any real constant $a$ we have:
$$\underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + a x \left.\right)}{x} = a$$

## Limits defining exponential functions

A standard limit that defines Euler’s number is given by:
$$\underset{x \rightarrow 0}{lim} \left(\right. 1 + x \left.\right)^{\frac{1}{x}} = e$$
or equivalently, in its discrete form:
$$\underset{n \rightarrow \infty}{lim} \left(\left(\right. 1 + \frac{1}{n} \left.\right)\right)^{n} = e$$

###### The discrete form is obtained by restricting $x$ to values of the form $\frac{1}{n}$, where $n$ is a positive integer, so that $x \rightarrow 0$ corresponds to $n \rightarrow \infty$. Substituting yields the sequence $\left(\left(\right. 1 + \frac{1}{n} \left.\right)\right)^{n}$, whose limit as $n \rightarrow \infty$ coincides with that of the continuous form.

More generally, for any real constant $a$ we have:
$$\underset{x \rightarrow 0}{lim} \left(\right. 1 + a x \left.\right)^{\frac{1}{x}} = e^{a}$$

## Limits involving power functions

For any real exponent $\alpha$ we have:
$$\underset{x \rightarrow 0}{lim} \frac{\left(\right. 1 + x \left.\right)^{\alpha} - 1}{x} = \alpha$$

This result may be derived using the binomial expansion when $\alpha$ is rational, or by applying logarithmic differentiation in the general case.

## Asymptotic equivalence

The following notable limits illustrate local [asymptotic](https://algebrica.org/asymptotes/) relationships:
$$sin ⁡ x sim x tan ⁡ x sim x 1 - cos ⁡ x sim \frac{x^{2}}{2}$$
$$e^{x} - 1 sim x ln ⁡ \left(\right. 1 + x \left.\right) sim x$$
More precisely, the notation $f \left(\right. x \left.\right) sim g \left(\right. x \left.\right)$ as $x \rightarrow 0$ indicates that the two functions are asymptotically equivalent near the origin, meaning that:
$$\underset{x \rightarrow 0}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = 1$$
Each of these relationships corresponds to the first nonzero term in the local Taylor expansion of a smooth function near a regular point. Consequently, these equivalences can be used to replace more complex expressions with simpler ones when evaluating limits.

## Structural interpretation

From an advanced perspective, remarkable limits serve as expressions of differentiability and local linearization. Every limit of the form:

$$\underset{x \rightarrow 0}{lim} \frac{f \left(\right. x \left.\right) - f \left(\right. 0 \left.\right)}{x}$$

corresponds to the definition of the [derivative](https://algebrica.org/derivatives/) of $f$ at the origin. Classical remarkable limits represent particular cases where this derivative can be calculated explicitly and then utilised as a foundational method for addressing more complex [indeterminate forms](https://algebrica.org/indeterminate-forms/).

## Summary of the main remarkable limits

|  |  |
| --- | --- |
| $$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x}$$ | $$1$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ \left(\right. a x \left.\right)}{a x}$$ | $$1$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ \left(\right. a x \left.\right)}{x}$$ | $$a$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{tan ⁡ x}{x}$$ | $$1$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{tan ⁡ \left(\right. a x \left.\right)}{x}$$ | $$a$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ x}{x^{2}}$$ | $$\frac{1}{2}$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ \left(\right. a x \left.\right)}{x^{2}}$$ | $$\frac{a^{2}}{2}$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1}{x}$$ | $$1$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{e^{a x} - 1}{x}$$ | $$a$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x}$$ | $$1$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + a x \left.\right)}{x}$$ | $$a$$ |
| $$\underset{x \rightarrow 0}{lim} \left(\right. 1 + x \left.\right)^{1 / x}$$ | $$e$$ |
| $$\underset{n \rightarrow \infty}{lim} \left(\left(\right. 1 + \frac{1}{n} \left.\right)\right)^{n}$$ | $$e$$ |
| $$\underset{x \rightarrow 0}{lim} \left(\right. 1 + a x \left.\right)^{1 / x}$$ | $$e^{a}$$ |
| $$\underset{x \rightarrow 0}{lim} \frac{\left(\right. 1 + x \left.\right)^{\alpha} - 1}{x}$$ | $$\alpha$$ |

## Selected references

- **Stanford University G. B. Folland**. [Limits and Continuity](https://web.stanford.edu/class/math19/limits.pdf)
- **MIT, D. Jerison**. [Calculus](https://ocw.mit.edu/courses/res-18-001-calculus-fall-2023/mitres_18_001_f17_full_book.pdf)
- **Harvard University P. Knill**. [Calculus One](https://people.math.harvard.edu/~knill/teaching/math1a_2011/calculus.pdf)
- **University of Oxford J. Norbury**. [Analysis I: Limits and Continuity](https://people.maths.ox.ac.uk/norbury/MT1/analysisI.pdf)
- **University of Cambridge N. D. Trefethen**. [Mathematical Analysis (Part IA)](https://www.maths.cam.ac.uk/undergrad/course/PartIA/analysis/analysis.pdf)
