---
layout: chapter
title: "Logarithms"
chapter: "Powers, Radicals and Logarithms"
chapter_order: 3
section_order: 3
permalink: /materi-algebrica/powers-radicals-and-logarithms/logarithms/
---

## Definition

If $a$ and $b$ are positive [real numbers](https://algebrica.org/properties-of-real-numbers/), where $a \neq 1$, the logarithm of $b$ to the base $a$, denoted as $log_{a} ⁡ \left(\right. b \left.\right)$, is defined as the real number $c$ such that $a^{c} = b$.

$$log_{a} ⁡ b = c \Longleftrightarrow a^{c} = b$$

The following conditions must be satisfied:

$$a > 0 a \neq 1 b > 0$$

In simpler terms, the logarithm of a number refers to the exponent to which a specified base must be raised to obtain that number. Therefore, the logarithm is the inverse operation of [exponentiation](https://algebrica.org/exponential-function).

- $a$ is the base of the logarithm.
- $b$ is the argument.

> To clarify the concept, let’s consider a simple example: $log ⁡ _{2} 8 = 3 \rightarrow 2^{3} = 8$.

---

The condition $a \neq 1$ is essential. In fact, when $a = 1$, the exponential expression $a^{x}$ becomes $1^{x} = 1 \forall x \in \mathbb{R}$ In this case, the exponential function is constant and therefore not [invertible](https://algebrica.org/inverse-function/). Since the logarithm is defined as the inverse operation of exponentiation, it cannot be defined when the base is equal to $1$. For this reason, the base of a logarithm must satisfy $a > 0$ and $a \neq 1$.

## Basic identities

Understanding logarithms requires a review of the concept of [powers](https://algebrica.org/powers), as these two mathematical ideas are closely related. The following identities arise directly from the principle that logarithms are the inverse operation of exponentiation:

$$a^{0} = 1 \rightarrow log ⁡ _{a} 1 = 0$$
$$a^{1} = a \rightarrow log ⁡ _{a} a = 1$$

Since the exponential is always positive, it is not possible to determine the logarithm of a negative number. In formal terms, $∄$ a number $c \in \mathbb{R}$ such that $a^{c} < 0$.

- Logarithms with base $e$, known as natural or Napierian logarithms, are typically denoted as $ln ⁡ a$ without specifying the base, where $e \approx 2.71828$ is [Euler’s number](https://algebrica.org/euler-number-limit-sequence/), the base of the natural exponential function $e^{x}$.
- Logarithms with the base of the number $10$, known as common logarithms, are typically denoted as $\text{Log} a$ without specifying the base.

> The base-10 logarithm is especially useful when dealing with very large or very small numbers. It helps reduce the scale, making the values easier to interpret and compare. That’s why it’s commonly used in scientific and technical fields, often represented on logarithmic scales.

## Logarithmic function

As previously introduced, the [logarithmic function](https://algebrica.org/logarithmic-function) is the [inverse](https://algebrica.org/inverse-function/) of the exponential function. Consequently, its [domain](https://algebrica.org/determining-the-domain-of-a-function/) and range are inverted compared to the exponential function. A logarithmic function is typically expressed in the following form:

$$log_{a} : \left(\right. 0 , + \infty \left.\right) \rightarrow \mathbb{R} , a > 0 , a \neq 1$$

The domain is $x \in \mathbb{R}^{+}$ and the range is $\mathbb{R}$. The function is [continuous](https://algebrica.org/continuous-functions/) and [differentiable](https://algebrica.org/derivatives/) on $\left(\right. 0 , + \infty \left.\right)$.

![](https://algebrica.org/wp-content/uploads/resources/images/logarithms.png)

---

The graph above illustrates the monotonic behaviour and asymptotic properties of the logarithmic function. For values of $a > 1$, the function $f \left(\right. x \left.\right) = log_{a} ⁡ x$ is strictly increasing on $\left(\right. 0 , + \infty \left.\right)$. It has a vertical [asymptote](https://algebrica.org/asymptotes/) at $x = 0$, and its limits are:

$$\underset{x \rightarrow 0^{+}}{lim} log_{a} ⁡ x & = - \infty \\ \underset{x \rightarrow + \infty}{lim} log_{a} ⁡ x & = + \infty$$

---

For $0 < a < 1$, the function is strictly decreasing on $\left(\right. 0 , + \infty \left.\right)$. The line $x = 0$ is again a vertical asymptote, but the limiting behaviour is reversed:

$$\underset{x \rightarrow 0^{+}}{lim} log_{a} ⁡ x & = + \infty \\ \underset{x \rightarrow + \infty}{lim} log_{a} ⁡ x & = - \infty$$

> The logarithmic function is utilised across various disciplines, for example in computer science, where it is fundamental to the analysis of algorithmic complexity. For example, algorithms such as [binary search](https://algebrica.org/logarithmic-function) exhibit logarithmic time complexity, indicating that their performance remains efficient as input sizes increase. This characteristic demonstrates how logarithmic growth enables concise and effective representations of exponential processes.

## Logarithmic function explorer

This interactive graph illustrates how the shape of a logarithmic function depends on the value of its base. By selecting bases greater than 1 or between 0 and 1, one can observe how the function changes from increasing to decreasing, along with its behavior near zero and at infinity, providing a clear visual interpretation of its fundamental properties and underlying structure.

---

Base

1/4 1/2 e 2 4

y = ln(x)

With base b = e, where b > 1, we obtain the natural logarithm. The function is strictly increasing, passes through (1, 0) and (e, 1), has domain (0, +∞), range ℝ, and vertical asymptote x = 0.

## Properties of logarithms

Logarithms have properties that facilitate the manipulation of mathematical expressions and [equations](https://algebrica.org/equations). These properties are fundamentally linked to those of exponential functions as each logarithmic identity directly results from a corresponding law of exponents.

Because the logarithm is defined as the inverse of the exponential function, the following identities are valid:

$$a^{log_{a} ⁡ x} = x \forall x \in \left(\right. 0 , + \infty \left.\right)$$

$$log_{a} ⁡ \left(\right. a^{x} \left.\right) = x \forall x \in \mathbb{R}$$

---

The product rule states that the logarithm of a product of two numbers is equal to the sum of their logarithms in the same base: $$log_{a} ⁡ \left(\right. x y \left.\right) = log_{a} ⁡ x + log_{a} ⁡ y$$

---

The quotient rule states that the logarithm of a quotient of two numbers is equal to the difference of the numerator and the denominator: $$log_{a} ⁡ \frac{x}{y} = log_{a} ⁡ x - log_{a} ⁡ y$$ From the previous expression, if the numerator $x$ is equal to $1$, we obtain: $$log_{a} ⁡ \frac{1}{y} = - log_{a} ⁡ y$$ This means that the logarithm of the reciprocal of a number $\frac{1}{y}$ is the opposite of its logarithm, and this is called the co-logarithm, indicated as: $$\text{colog}_{a} y = - l o g_{a} y = log_{a} ⁡ \frac{1}{y}$$

---

The property of the logarithm of a power states that the logarithm of a [power](https://algebrica.org/powers) of a number is equal to the product of the exponent and the logarithm of the base number: $$log ⁡ _{a} x^{n} = n \cdot log ⁡ _{a} x$$ This property directly follows from the properties of exponentials, as an expression like $x^{n}$ can be understood as the result of multiplying $x$ by itself $n$ times.

---

From the previous property and the property of [radicals](https://algebrica.org/radicals), it follows that the logarithm of a radical is equal to the quotient between the logarithm of the radicand and the index of the root: $$log_{a} ⁡ \sqrt[n]{b} = \frac{1}{n} log_{a} ⁡ b$$

## Fundamental inequality for the natural logarithm

A key inequality involving the natural logarithm $ln$is given by:

$$ln ⁡ x \leq x - 1 \forall x > 0$$

This equality holds if and only if $x = 1$. This result follows directly from the concavity of the function $ln ⁡ x$ on the interval $\left(\right. 0 , + \infty \left.\right)$. Since the second derivative satisfies:

$$\left(\right. ln ⁡ x \left.\right)^{′ ′} = - \frac{1}{x^{2}} < 0 \forall x > 0$$

The graph of the logarithm always lies below each of its tangent lines. In particular, consider the tangent at $x = 1$, where:

$$ln ⁡ 1 = 0 \text{and} \left(\right. ln ⁡ x \left.\right)^{'} \left|\right._{x = 1} = 1$$

The equation of the tangent line is:

$$y = x - 1$$

Therefore, the inequality expresses the geometric fact that the curve $y = ln ⁡ x$ does not rise above its tangent at $x = 1$.

## The role of logarithms in algebraic structure

The logarithm acts as a structural bridge between two distinct algebraic systems. Within the set of positive real numbers $\left(\right. 0 , + \infty \left.\right)$, multiplication is the primary operation, while addition serves this role in $\mathbb{R}$. The logarithm connects these systems by transforming multiplicative relationships into additive relationships. For example, consider the following product:

$$x^{3} y^{2}$$

Taking logarithms gives:

$$log_{a} ⁡ \left(\right. x^{3} y^{2} \left.\right) = 3 log_{a} ⁡ x + 2 log_{a} ⁡ y$$

This process converts the multiplicative structure, characterised by products and powers, into an additive structure, characterised by sums and scalar multiples. In this context, the logarithm functions as a homomorphism from the multiplicative group $\left(\right. 0 , + \infty \left.\right)$ to the additive group $\mathbb{R}$, preserving the underlying structure while altering the operation. The standard logarithmic rules provide exact algebraic formulations of this transformation.

> A homomorphism is a function between two algebraic structures that preserves the operation, meaning $\varphi \left(\right. x \star y \left.\right) = \varphi \left(\right. x \left.\right) \circ \varphi \left(\right. y \left.\right)$. Here $\star$ and $\circ$ denote the operations of the two algebraic structures, such as addition or multiplication.

## Example 1

Let’s simplify the following logarithmic expression using the properties of logarithms:

$$log_{a} ⁡ \left(\right. \frac{x^{3} \cdot y}{z^{2}} \left.\right)$$

---

First, we apply the quotient rule, which states that the logarithm of a quotient is the difference between the logarithms of the numerator and the denominator:

$$log_{a} ⁡ \left(\right. \frac{x^{3} \cdot y}{z^{2}} \left.\right) = log_{a} ⁡ \left(\right. x^{3} \cdot y \left.\right) - log_{a} ⁡ \left(\right. z^{2} \left.\right)$$

Next, we apply the product rule, which tells us that the logarithm of a product is the sum of the logarithms of the factors:

$$log_{a} ⁡ \left(\right. x^{3} \cdot y \left.\right) = log_{a} ⁡ \left(\right. x^{3} \left.\right) + log_{a} ⁡ \left(\right. y \left.\right)$$

Thus, the expression becomes:

$$log_{a} ⁡ \left(\right. \frac{x^{3} \cdot y}{z^{2}} \left.\right) = log_{a} ⁡ \left(\right. x^{3} \left.\right) + log_{a} ⁡ \left(\right. y \left.\right) - log_{a} ⁡ \left(\right. z^{2} \left.\right)$$

---

Now, we apply the power rule, which states that the logarithm of a power is the exponent times the logarithm of the base:

$$log_{a} ⁡ \left(\right. x^{3} \left.\right) = 3 log_{a} ⁡ \left(\right. x \left.\right) \text{and} log_{a} ⁡ \left(\right. z^{2} \left.\right) = 2 log_{a} ⁡ \left(\right. z \left.\right)$$

Finally, we substitute and simplify, obtaining the expression:

$$log_{a} ⁡ \left(\right. \frac{x^{3} \cdot y}{z^{2}} \left.\right) = 3 log_{a} ⁡ \left(\right. x \left.\right) + log_{a} ⁡ \left(\right. y \left.\right) - 2 log_{a} ⁡ \left(\right. z \left.\right)$$

## Changing the base of a logarithm

Any logarithm with base $a$ can be represented as the ratio of logarithms with a common base. Specifically, a logarithm with base $a$ and argument $b$ can be written as the ratio of two logarithms with base $p$, where the numerator has argument $b$ and the denominator has argument $a$:

$$log ⁡ _{a} b = \frac{log ⁡ _{p} b}{log ⁡ _{p} a}$$

> This property is advantageous because it significantly simplifies calculations in various contexts.

## Example 2

Let’s use a simple example to demonstrate the formula for changing the base of the logarithms. According to the definition of logarithm, the logarithm in base $a$ of a number $x$, denoted as $log_{a} ⁡ \left(\right. x \left.\right)$, represents the exponent to which we must raise the base $a$ to get the number $x$. We can write the change of base property as: $$log_{a} ⁡ \left(\right. x \left.\right) = \frac{log_{b} ⁡ \left(\right. x \left.\right)}{log_{b} ⁡ \left(\right. a \left.\right)}$$

---

Let’s consider the substitution $y = log_{a} ⁡ \left(\right. x \left.\right)$, which means, according to the definition of logarithm, $a^{y} = x$. We have: $$log_{b} ⁡ \left(\right. a^{y} \left.\right) = log_{b} ⁡ \left(\right. x \left.\right)$$

---

For the property of the power of a logarithm, we obtain: $$y \cdot log_{b} ⁡ \left(\right. a \left.\right) = log_{b} ⁡ \left(\right. x \left.\right)$$

---

Now, dividing both sides by $log_{b} ⁡ \left(\right. a \left.\right)$ we obtain: $$y = \frac{log_{b} ⁡ \left(\right. x \left.\right)}{log_{b} ⁡ \left(\right. a \left.\right)}$$

While $y = log_{a} ⁡ \left(\right. x \left.\right)$, we have proved that:

$$log_{a} ⁡ \left(\right. x \left.\right) = \frac{log_{b} ⁡ \left(\right. x \left.\right)}{log_{b} ⁡ \left(\right. a \left.\right)}$$

## Logarithmic equations

[Logarithmic equations](https://algebrica.org/logarithmic-equations) are mathematical expressions in which the variable appears within a logarithmic function. Solving such equations requires a thorough understanding of logarithmic properties, which are essential for isolating and determining the variable’s value. A typical logarithmic equation is structured as follows:

$$log_{a} ⁡ f \left(\right. x \left.\right) = g \left(\right. x \left.\right)$$

- $a$ is the base of the logarithm and it must meet the condition $a > 0 , a \neq 1.$
- The function $f \left(\right. x \left.\right)$ serves as the argument of the logarithm and must be greater than zero. This requirement arises because the logarithm function is defined only for positive numbers.

## The natural logarithm

From an analytical standpoint, the natural logarithm is defined independently of exponentiation using a [definite integral](https://algebrica.org/definite-integrals/). For every real number $x > 0$, the natural logarithm is given by:

$$ln ⁡ x = \int_{1}^{x} \frac{1}{t} d t$$

This definition ensures that $ln ⁡ x$ is well-defined for all positive real numbers because the function $\frac{1}{t}$ is continuous on $\left(\right. 0 , + \infty \left.\right)$. By the [Fundamental Theorem of Calculus](https://algebrica.org/fundamental-theorem-of-calculus/), the natural logarithm is differentiable and satisfies:

$$\left(\right. ln ⁡ x \left.\right)^{'} = \frac{1}{x} x > 0$$

Furthermore, the natural logarithm is [strictly increasing](https://algebrica.org/increasing-and-decreasing-functions/) because its [derivative](https://algebrica.org/derivatives/) is positive on $\left(\right. 0 , + \infty \left.\right)$. It is also concave, as:

$$\left(\right. ln ⁡ x \left.\right)^{′ ′} = - \frac{1}{x^{2}} < 0$$

---

The exponential function $e^{x}$ is defined as the inverse of $ln ⁡ x$. Once the natural logarithm is established, logarithms with any base $a > 0$, $a \neq 1$, are defined by:

$$log_{a} ⁡ x = \frac{ln ⁡ x}{ln ⁡ a}$$

This construction offers a rigorous analytical foundation for logarithms and accounts for their continuity, differentiability, and structural properties.

## The AM-GM inequality via logarithms

The [arithmetic mean](https://algebrica.org/arithmetic-mean/) and the [geometric mean](https://algebrica.org/geometric-mean/) of a finite set of positive real numbers satisfy a fundamental inequality: the arithmetic mean is always greater than or equal to the geometric mean. For positive real numbers $x_{1} , x_{2} , \ldots , x_{n}$, this is stated as:

$$\frac{x_{1} + x_{2} + \hdots + x_{n}}{n} \geq \left(\left(\right. x_{1} x_{2} \hdots x_{n} \left.\right)\right)^{\frac{1}{n}}$$

with equality if and only if $x_{1} = x_{2} = \hdots = x_{n}$. The logarithm provides one of the most elegant proofs of this result, relying on a single concavity argument.

---

The key observation is that $ln$ is a strictly concave function on $\left(\right. 0 , + \infty \left.\right)$, since its second derivative satisfies $\left(\right. ln ⁡ x \left.\right)^{''} = - 1 / x^{2} < 0$ for all $x > 0$. Since $ln$ is concave, the following holds for any positive real numbers $x_{1} , \ldots , x_{n}$:

$$\frac{1}{n} \sum_{i = 1}^{n} ln ⁡ x_{i} \leq ln \left(\right. \frac{1}{n} \sum_{i = 1}^{n} x_{i} \left.\right)$$

The left-hand side is the arithmetic mean of $ln ⁡ x_{1} , \ldots , ln ⁡ x_{n}$, which by the logarithmic form of the [geometric mean](https://algebrica.org/geometric-mean/) equals $ln ⁡ M_{g}$. The right-hand side is $ln ⁡ M_{a}$, where $M_{a}$ denotes the [arithmetic mean](https://algebrica.org/arithmetic-mean/). The inequality therefore becomes:

$$ln ⁡ M_{g} \leq ln ⁡ M_{a}$$

Since $ln$ is strictly increasing, this is equivalent to $M_{g} \leq M_{a}$, which is the AM-GM inequality. Equality holds if and only if all arguments are equal, that is, $x_{1} = x_{2} = \hdots = x_{n}$.

> This proof makes explicit the structural role of the logarithm: by mapping the multiplicative structure of $M_{g}$ into the additive structure of $M_{a}$, it reduces the inequality between two different types of mean to a single analytic property of $ln$.

integral definitionhomomorphismlogarithmic equationsmonotonicitygraph and asymptoteslogarithmic functionidentitieschange of baselog of reciprocalpower rulequotient ruleproduct rulecommon logarithmnatural logarithmdomain and conditionsinverse of exponentiationbase and argumentdefinitionstructuresoperationsfoundations
