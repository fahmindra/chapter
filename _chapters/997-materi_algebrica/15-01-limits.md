---
layout: chapter
title: "Limits"
chapter: "Limits"
chapter_order: 15
section_order: 1
permalink: /materi-algebrica/limits/limits/
---

## Understanding limits in calculus

The concept of a **limit** is fundamental in mathematics. Intuitively, the limit of a [function](https://algebrica.org/functions) $f \left(\right. x \left.\right)$ as $x$ approaches a point $x_{0}$ allows us to analyse the behaviour of the function as the values of $x$ get arbitrarily close to $x_{0}$.

A neighbourhood of $x$ refers to an interval consisting of all points sufficiently close to $x$. More formally, a neighbourhood of $x$ is any open interval $\left(\right. x - \delta , x + \delta \left.\right)$ where $\delta > 0$. This concept is essential for defining limits and understanding the behaviour of functions as they approach a given point.

![](https://algebrica.org/wp-content/uploads/resources/images/limits-1.png)

The smaller the neighbourhood, the closer the points are to $x$. In other words, as the interval $\left(\right. x - \delta , x + \delta \left.\right)$ becomes narrower (with $\delta$ approaching zero), the distance between the points within the neighbourhood and $x$ decreases.

## Definition

Suppose we have a function $f \left(\right. x \left.\right)$ whose behaviour we wish to study as $x$ approaches the point $x_{0}$. We say that as $x$ tends to $x_{0}$, the function $f \left(\right. x \left.\right)$ has a limit $ℓ$, and we write:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = ℓ$$

Formally, this statement asserts that for every tolerance $\epsilon > 0$, there exists a corresponding distance $\delta > 0$ such that whenever:

$$0 < \left|\right. x - x_{0} \left|\right. < \delta$$

it follows that:

$$\left|\right. f \left(\right. x \left.\right) - ℓ \left|\right. < \epsilon$$

In other words, for every neighbourhood of $ℓ$, there exists a sufficiently small neighbourhood of $x_{0}$ such that all corresponding function values remain within this neighbourhood. This formal definition precisely articulates the intuitive concept that the limit represents the value approached by $f \left(\right. x \left.\right)$ as $x$ becomes arbitrarily close to $x_{0}$.

---

When the definition of a limit applies only to a right neighbourhood or a left neighbourhood of $x_{0}$, we refer to these as the right-hand limit and left-hand limit, respectively. They are represented as follows:

$$\underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) \text{and} \underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right)$$

## Asymptotes and infinite limits

In general, the value of $x$ in a limit can approach a real number $x_{0}$ or $\pm \infty$.

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = ℓ \text{or} \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = \pm \infty$$

Additionally, the value of the limit itself can be either a finite number or $\pm \infty$.

$$\underset{x \rightarrow \pm \infty}{lim} f \left(\right. x \left.\right) = ℓ \text{or} \underset{x \rightarrow \pm \infty}{lim} f \left(\right. x \left.\right) = \pm \infty$$

---

When the limit of $f \left(\right. x \left.\right)$ exists and tends to $\pm \infty$ as $x$ approaches a finite real number, the behaviour of the function can resemble the simplified pattern shown in the figure. The line $x = k$ is called a **vertical asymptote**:

![](https://algebrica.org/wp-content/uploads/resources/images/limits-2.png)

In the example, we have the case where the right-hand and left-hand limits of $f \left(\right. x \left.\right)$ are, respectively:

$$\underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) = - \infty \text{and} \underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right) = + \infty$$

---

When the limit of $f \left(\right. x \left.\right)$ exists and approaches a finite value $L$ as $x$ tends to $\pm \infty$, the behaviour of the function can resemble the simplified pattern shown in the figure. The line $y = L$ is called a **horizontal asymptote**:

![](https://algebrica.org/wp-content/uploads/resources/images/limits-3.png)

In the example, we have the case where the right-hand and left-hand limits of $f \left(\right. x \left.\right)$ are, respectively:

$$\underset{x \rightarrow + \infty}{lim} f \left(\right. x \left.\right) = L \text{and} \underset{x \rightarrow - \infty}{lim} f \left(\right. x \left.\right) = L$$

##### An asymptote is defined as a line that the graph of a function approaches arbitrarily closely as either the $x$-value or $y$-value increases or decreases without bound. Consequently, the distance between the curve and the asymptote approaches zero as the graph extends toward the extremes of the coordinate plane.

## Conditions for limit existence and continuity

When the left-hand and right-hand limits of a function both exist and are finite, but have different values with $ℓ_{1} \neq ℓ_{2}$, we have:

$$\left{\right. \underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right) = ℓ_{1} \in \mathbb{R} \\ \underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) = ℓ_{2} \in \mathbb{R} \Longrightarrow ∄ \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right)$$

In this scenario, the limit of $f \left(\right. x \left.\right)$ as $x$ approaches $x_{0}$ does not exist because the function approaches two distinct values depending on the direction of approach. However, the left-hand limit and the right-hand limit are well-defined and finite when considered separately.

---

According to the Uniqueness Theorem of Limits, if the limit of a function $f \left(\right. x \left.\right)$ as $x$ approaches $x_{0}$ exists, whether finite or infinite, such a limit is unique. This statement can be formally represented as:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = ℓ \in \overset{―}{\mathbb{R}} \Longrightarrow ℓ \text{is unique}$$

The theorem ensures that if a limit exists, there cannot be two different values satisfying the definition of a limit for the same function and point.

---

The concept of a limit is fundamental for introducing and defining the concept of a [continuous](https://algebrica.org/continuous-functions/) function. A function $y = f \left(\right. x \left.\right)$ is said to be continuous at a point $x_{0}$ if the limit of the function as $x$ approaches $x_{0}$ exists and is equal to the value of the function at that point. Formally, this is expressed as:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right)$$

## Properties

The following properties of limits are particularly useful for performing calculations and simplifying complex expressions. They establish the foundational rules for manipulating limits and are essential for working with more advanced mathematical problems.

---

The limit of the product of a **constant** and a function is equal to the product of the constant and the limit of the function, provided the limit exists.

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. c f \left(\right. x \left.\right) \left.\right) = c \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = c \cdot ℓ$$

Multiplying a function by a constant does not affect the process of taking the limit, other than scaling the result by that constant.

---

The limit of the algebraic **sum** of two functions is equal to the sum of their individual limits, provided both limits exist.

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) = \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) + \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) = ℓ_{1} + ℓ_{2}$$

The limits of each function can therefore be evaluated separately and then added. This is particularly useful when working with [polynomial functions](https://algebrica.org/polynomial-function/), [trigonometric functions](https://algebrica.org/sine-and-cosine), and other common mathematical expressions.

---

The limit of the **product** of two functions is equal to the product of their individual limits, provided both limits exist.

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left.\right) = \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) \cdot \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) = ℓ_{1} \cdot ℓ_{2}$$

---

The limit of the **quotient** of two functions is equal to the quotient of their individual limits, provided both limits exist and the limit of the denominator is not zero.

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} \left.\right) = \frac{\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right)}{\underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right)} = \frac{ℓ_{1}}{ℓ_{2}}$$

## When standard properties do not apply

The previously outlined properties are valid only when all relevant limits exist and are finite, and the denominator remains nonzero. However, in practical applications, it is common to encounter expressions where direct substitution produces an undefined result, such as:

$$\frac{0}{0} \frac{\infty}{\infty} \infty - \infty$$

Such expressions are classified as [indeterminate forms](https://algebrica.org/indeterminate-forms/). Resolving them requires specialised techniques that extend beyond standard algebraic manipulation of limits. A classic example illustrates this point:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x}$$

Direct substitution of $x = 0$ yields $\frac{0}{0}$, which is undefined. The quotient property of limits does not apply in this case because the limit of the denominator is zero. The resolution of such expressions requires a specialised analytical approach, as detailed in the referenced page.

## Fundamental limits of elementary functions

The following limits characterise the asymptotic behaviour of common elementary functions. These limits provide foundational tools for evaluating more complex limits and are frequently encountered in mathematical analysis.

---

For the constant function $f \left(\right. x \left.\right) = k$ with $k \in \mathbb{R}$, we have:

$$\underset{x \rightarrow - \infty}{lim} k = k \text{and} \underset{x \rightarrow + \infty}{lim} k = k$$

---

For the function $f \left(\right. x \left.\right) = x$, we have:

$$\underset{x \rightarrow - \infty}{lim} x = - \infty \text{and} \underset{x \rightarrow + \infty}{lim} x = + \infty$$

---

For the [exponential function](https://algebrica.org/exponential-function/) with base $a > 1$, we have:

$$\underset{x \rightarrow - \infty}{lim} a^{x} = 0 \text{and} \underset{x \rightarrow + \infty}{lim} a^{x} = + \infty$$

---

For the exponential function with base $0 < a < 1$, we have:

$$\underset{x \rightarrow - \infty}{lim} a^{x} = + \infty \text{and} \underset{x \rightarrow + \infty}{lim} a^{x} = 0$$

###### If the base is greater than $1$, the exponential function increases without bound in one direction and approaches zero in the other. If the base is strictly between $0$ and $1$, this behaviour is reversed.

---

For the power function with an even exponent, we have:

$$\underset{x \rightarrow - \infty}{lim} x^{n} = + \infty \text{and} \underset{x \rightarrow + \infty}{lim} x^{n} = + \infty$$

---

For the power function with an odd exponent, we have:

$$\underset{x \rightarrow - \infty}{lim} x^{n} = - \infty \text{and} \underset{x \rightarrow + \infty}{lim} x^{n} = + \infty$$

---

For root functions with an even index, we have:

$$\underset{x \rightarrow + \infty}{lim} \sqrt[n]{x} = + \infty$$

###### For even indices, the root function is defined only for $x \geq 0$. Therefore, the limit as $x \rightarrow - \infty$ is not applicable.

---

For root functions with an odd index, we have:

$$\underset{x \rightarrow + \infty}{lim} \sqrt[n]{x} = + \infty \text{and} \underset{x \rightarrow - \infty}{lim} \sqrt[n]{x} = - \infty$$

---

For the [logarithmic function](https://algebrica.org/logarithmic-function) with base $a > 1$, we have:

$$\underset{x \rightarrow 0^{+}}{lim} log_{a} ⁡ x = - \infty \text{and} \underset{x \rightarrow + \infty}{lim} log_{a} ⁡ x = + \infty$$

---

For the [logarithmic function](https://algebrica.org/logarithmic-function) with base $0 < a < 1$, we have:

$$\underset{x \rightarrow 0^{+}}{lim} log_{a} ⁡ x = + \infty \text{and} \underset{x \rightarrow + \infty}{lim} log_{a} ⁡ x = - \infty$$

---

For the [absolute value function](https://algebrica.org/absolute-value-function/) $f \left(\right. x \left.\right) = \left|\right. x \left|\right.$, we have:

$$\underset{x \rightarrow - \infty}{lim} \left|\right. x \left|\right. = + \infty \text{and} \underset{x \rightarrow + \infty}{lim} \left|\right. x \left|\right. = + \infty$$

---

For the sign function $\text{sgn} \left(\right. x \left.\right)$, we have:

$$\underset{x \rightarrow - \infty}{lim} \text{sgn} \left(\right. x \left.\right) = - 1 \text{and} \underset{x \rightarrow + \infty}{lim} \text{sgn} \left(\right. x \left.\right) = 1$$

---

When working with limits, you use algebraic operations to combine, break apart, and work with functions in a systematic way. These rules, such as limits of sums, products, quotients, powers, and compositions, are explained in more detail on the page about the [algebra of limits](https://algebrica.org/algebra-of-limits/).

## Selected references

- **Harvard University O. Knill**. [Unit 3: Limits](https://people.math.harvard.edu/~knill/teaching/math1a2021/handouts/lecture03.pdf)
- **University of California, Berkeley A. Vizeff**. [Continuity and Discontinuities](https://math.berkeley.edu/~avizeff/calculus-I-F22/lecture-5.pdf)
- **University of California, Los Angeles N. Hu**. [Limits of Functions](https://www.math.ucla.edu/~njhu/teaching/math-131a-2024u/notes/10-compact.pdf)
- **University of California, Berkeley R. Wang**. [Limits](https://math.berkeley.edu/~ruiwang/pdf/104.pdf)
- **MIT D. Jerison**. [Limits and Continuity](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/pages/1.-differentiation/part-a-definition-and-basic-rules/session-4-limits-and-continuity/)
