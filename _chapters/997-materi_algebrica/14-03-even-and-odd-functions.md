---
layout: chapter
title: "Even and Odd Functions"
chapter: "Functions"
chapter_order: 14
section_order: 3
permalink: /materi-algebrica/functions/even-and-odd-functions/
---

## Behavior of a function

When analyzing the behavior of a [function](https://algebrica.org/functions), it is useful to investigate whether the function exhibits symmetry with respect to the coordinate axes. In this context, functions can be classified as **even**, showing symmetry with respect to the $y$-axis, or **odd**, exhibiting symmetry with respect to the origin. In general, a function can be:

- even
- odd
- neither even nor odd

## Even function

More specifically, suppose we have a function $f \left(\right. x \left.\right) : \mathbb{R} \rightarrow \mathbb{R}$, and let $D \subseteq \mathbb{R}$ be its [domain](https://algebrica.org/determining-the-domain-of-a-function/). The function $f$ is said to be **even** if the following condition holds:

$$f \left(\right. x \left.\right) = f \left(\right. - x \left.\right) \text{for all} x \in D$$

![](https://algebrica.org/wp-content/uploads/resources/images/even-odd-functions-1.png)

As shown in the figure, the function $f \left(\right. x \left.\right) = x^{2}$ is a [parabola](https://algebrica.org/parabola) symmetric with respect to the $y$-axis. In general, functions of the form $f \left(\right. x \left.\right) = x^{4}$, $x^{6}$, or more generally $x^{2 n}$, where the exponent is even, are examples of even functions.

![](https://algebrica.org/wp-content/uploads/resources/images/even-odd-functions-2-1.png)

Another example of an even function is the [cosine function](https://algebrica.org/cosine-function). It is a periodic function with period $2 \pi$, and its graph is symmetric with respect to the $y$-axis. In fact, it is easy to verify that:
$$cos ⁡ \left(\right. \pi \left.\right) = cos ⁡ \left(\right. - \pi \left.\right) = - 1$$

Another even function is the [absolute value function](https://algebrica.org/absolute-value-function/).

---

More generally, when considering the family of functions of the form $f \left(\right. x \left.\right) = x^{n}$ with $n \in \mathbb{N} ,$ the parity of the function is entirely determined by the exponent: the function behaves as an even function whenever $n$ is an even [integer](https://algebrica.org/integers/), whereas it behaves as an odd function whenever $n$ is odd.

## Definite integral of even function

One of the useful consequences of a function being even is the simplification it allows in [definite integrals](https://algebrica.org/definite-integrals/) over symmetric intervals. If $f \left(\right. x \left.\right)$ is a [continuous](https://algebrica.org/continuous-functions/) and even function, then its graph is symmetric with respect to the $y$-axis.

This symmetry directly influences how we evaluate definite integrals over intervals of the form $\left[\right. - a , a \left]\right.$. Specifically, the following identity holds:

$$\int_{- a}^{a} f \left(\right. x \left.\right) , d x = 2 \int_{0}^{a} f \left(\right. x \left.\right) , d x$$

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-5.png)

That is, the total area under the curve from $- a$ to $a$ is simply twice the area from 0 to (a). This works because the portion of the graph on the negative side of the $x$-axis is a mirror image of the positive side, and contributes the same value to the integral.

## Odd function

Suppose we have a function $f \left(\right. x \left.\right) : \mathbb{R} \rightarrow \mathbb{R}$, and let $D \subseteq \mathbb{R}$ be its domain. The function $f$ is said to be **odd** if the following condition holds:

$$f \left(\right. - x \left.\right) = - f \left(\right. x \left.\right) \text{for all} x \in D$$

![](https://algebrica.org/wp-content/uploads/resources/images/even-odd-functions-3.png)

As shown in the figure, the function $f \left(\right. x \left.\right) = x^{3}$ is symmetric with respect to the origin. Functions of the form $f \left(\right. x \left.\right) = x^{3}$, $x^{5}$, or more generally $x^{2 n + 1}$, where the exponent is odd, are examples of odd functions.

![](https://algebrica.org/wp-content/uploads/resources/images/even-odd-functions-4-1.png)

Another example of an odd function is the [sine function](https://algebrica.org/sine-function). It is a periodic function with period $2 \pi$, and its graph is symmetric with respect to the origin. In fact, it is easy to verify that:
 $$sin ⁡ \left(\right. - \pi \left.\right) = - sin ⁡ \left(\right. \pi \left.\right) = 0$$

## Definite integral of odd function

In the case of an odd function, the area between $\left[\right. - a , 0 \left]\right.$ is equal in magnitude but opposite in sign to the area between $\left[\right. 0 , a \left]\right.$. Therefore, the definite integral is equal to:

$$\int_{- a}^{a} f \left(\right. x \left.\right) d x = 0$$

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-6.png)

In both situations, the area enclosed between the graph of $f \left(\right. x \left.\right)$ and the $x$-axis over the interval $\left[\right. - a , a \left]\right.$ is given by:

$$S = \int_{0}^{a} \left|\right. f \left(\right. x \left.\right) \left|\right. d x$$

## The only function that is both even and odd

The function $f \left(\right. x \left.\right) = 0$ is the only function that is both even and odd, because it satisfies both $f \left(\right. - x \left.\right) = f \left(\right. x \left.\right)$ and $f \left(\right. - x \left.\right) = - f \left(\right. x \left.\right)$ for all $x \in \mathbb{R}$. In fact, if a function were to be both even and odd, we would have:

- $f \left(\right. - x \left.\right) = f \left(\right. x \left.\right)$ when the function is even.
- $f \left(\right. - x \left.\right) = - f \left(\right. x \left.\right)$ when the function is odd.

Therefore, the zero function is the unique case that satisfies both properties.

## Properties

- The sum of two even functions is even.
- The product of an even function by a constant is even.
- The product of two even functions is an even function.
- The [derivative](https://algebrica.org/derivatives) of an even function is an odd function.
- The sum of two odd functions is odd.
- The product of an odd function by a constant is odd.
- The product of two odd functions is an even function.
- The derivative of an odd function is an even function.
- The product of an even function and an odd function is an odd function.
