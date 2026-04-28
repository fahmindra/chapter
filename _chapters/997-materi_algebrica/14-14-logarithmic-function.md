---
layout: chapter
title: "Logarithmic Function"
chapter: "Functions"
chapter_order: 14
section_order: 14
permalink: /materi-algebrica/functions/logarithmic-function/
---

## Introduction

The [logarithmic](https://algebrica.org/logarithms) function is the inverse of the [exponential function](https://algebrica.org/exponential-function). Therefore, its [domain](https://algebrica.org/determining-the-domain-of-a-function/) and range are inverted compared to the exponential function. A logarithmic function is defined as a function of the form:

$$y = log ⁡ _{a} x \text{with} a > 0 a \neq 1 \forall x \in \mathbb{R}^{+}$$

There are two cases to consider when examining the logarithmic function $log_{a} ⁡ \left(\right. x \left.\right)$.

- If the base $a > 1$, the function is increasing, meaning it grows as $x$ increases.
- If $0 < a < 1$, the function is decreasing, meaning it diminishes as $x$ increases.

![](https://algebrica.org/wp-content/uploads/resources/images/logharithm-6.png)

In both cases, the only point where the logarithmic function takes the value $0$ is at $x = 1$. This is because: $log_{a} ⁡ \left(\right. 1 \left.\right) = 0$. This result is true because by definition, by the property of [powers](https://algebrica.org/powers), we have $a^{0} = 1$.

##### The value of the base, whether it is greater than 1 or between 0 and 1, plays a crucial role in many applications. In particular, when dealing with [logarithmic inequalities](https://algebrica.org/logarithmic-inequalities/), a base between 0 and 1 requires reversing the direction of the inequality, due to the decreasing nature of the logarithmic function.

## Properties

- Domain: $\left(\right. 0 , + \infty \left.\right)$.
- Range: $\mathbb{R}$.
- Roots: $x = 1$.
- The logarithmic function is strictly [increasing](https://algebrica.org/increasing-and-decreasing-functions/) on $\left(\right. 0 , + \infty \left.\right)$ when the base satisfies $a > 1$. If $0 < a < 1$, the function is strictly decreasing on the same interval.
- The function is neither even nor odd, because it is not defined for negative values of $x$.
- The function is [continuous](https://algebrica.org/continuous-functions/) on $\left(\right. 0 , + \infty \left.\right)$.
- The function is differentiable on its entire domain, with derivative $f^{'} \left(\right. x \left.\right) = 1 / x$.
- The function has no [maximum or minimum](https://algebrica.org/maximum-minimum-and-inflection-points/) on its domain.

## Limits, derivatives, and integrals

A fundamental [limit](https://algebrica.org/limits/) involving the logarithmic function describes its behavior near zero and at infinity and plays an important role in the study of logarithmic functions. For a logarithmic function with base $a > 1$, as the variable approaches zero from the right, the value of the logarithm decreases without bound, while it grows without bound as the variable tends to infinity. This behavior is formally expressed by the following limits:

$$1. \underset{x \rightarrow 0^{+}}{lim} log_{a} ⁡ x = - \infty$$
$$2. \underset{x \rightarrow + \infty}{lim} log_{a} ⁡ x = + \infty$$

When the logarithm base is $0 < a < 1$, we have:

$$3. \underset{x \rightarrow 0^{+}}{lim} log_{a} ⁡ x = + \infty$$
$$4. \underset{x \rightarrow + \infty}{lim} log_{a} ⁡ x = - \infty$$

---

The [derivative](https://algebrica.org/derivatives) of the logarithmic function with base $a$ can be obtained by applying the standard differentiation rules for logarithms. In particular, for $x > 0$ and $a > 0$ with $a \neq 1$, the derivative of $log_{a} ⁡ \left(\right. x \left.\right)$ with respect to $x$ is given by:
$$5. \frac{d}{d x} log_{a} ⁡ \left(\right. x \left.\right) = \frac{1}{x ln ⁡ \left(\right. a \left.\right)}$$

---

The [indefinite integral](https://algebrica.org/indefinite-integrals/) of the logarithmic function with base $a$ can be derived by recalling the relationship between logarithms with different bases. Since:
$$log_{a} ⁡ \left(\right. x \left.\right) = \frac{log ⁡ \left(\right. x \left.\right)}{log ⁡ \left(\right. a \left.\right)}$$

the integration can be reduced to the integral of the natural logarithm. Using standard techniques from calculus, in particular [integration by parts](https://algebrica.org/integration-by-parts/), we obtain the following result:
$$6. \int \frac{log ⁡ \left(\right. x \left.\right)}{log ⁡ \left(\right. a \left.\right)} d x = \frac{x \left(\right. log ⁡ \left(\right. x \left.\right) - 1 \left.\right)}{log ⁡ \left(\right. a \left.\right)} + c$$

## Natural logarithm

More generally, considering the function $y = ln ⁡ \left(\right. x \left.\right)$, the natural logarithm, we have:
$$7. ln ⁡ \left(\right. x \left.\right) = log_{e} ⁡ \left(\right. x \left.\right)$$

Using the change of base formula, this can be rewritten as:
$$8. ln ⁡ \left(\right. x \left.\right) = \frac{log_{a} ⁡ \left(\right. x \left.\right)}{log_{a} ⁡ \left(\right. e \left.\right)}$$

---

For the natural logarithm $ln ⁡ \left(\right. x \left.\right)$, which is defined for all $x > 0$, the rate of change with respect to $x$ is particularly simple. Indeed, the derivative of $ln ⁡ \left(\right. x \left.\right)$ is given by:
$$9. \frac{d}{d x} ln ⁡ \left(\right. x \left.\right) = \frac{1}{x}$$

##### This result reflects the fact that the natural logarithm is the inverse function of the [exponential function](https://algebrica.org/exponential-function) $e^{x}$, and it explains why $ln ⁡ \left(\right. x \left.\right)$ grows slowly as $x$ increases.

---

An important integral representation of the natural logarithm involves the [definite integral](https://algebrica.org/definite-integrals) of $ln ⁡ \left(\right. t \left.\right)$ over an interval starting at the origin. Specifically, consider the integral
$$10 . \int_{0}^{x} ln ⁡ \left(\right. t \left.\right) d t$$
which is defined for $x > 0$. Although the integrand $ln ⁡ \left(\right. t \left.\right)$ is not defined at $t = 0$, the integral is interpreted as an improper integral. Its value can be computed using integration by parts, yielding:
$$\int ln ⁡ \left(\right. t \left.\right) d t = t ln ⁡ \left(\right. t \left.\right) - t + c$$
Applying this antiderivative and taking the limit as the lower bound approaches zero, we obtain:
$$\int_{0}^{x} ln ⁡ \left(\right. t \left.\right) d t = \left[\right. t ln ⁡ \left(\right. t \left.\right) - t \left]\right._{0}^{x} = x ln ⁡ \left(\right. x \left.\right) - x + 1$$

---

A fundamental definite integral involving the natural logarithm is
$$11. \int_{0}^{1} ln ⁡ \left(\right. x \left.\right) d x = - 1$$
This integral is interpreted as an improper integral, since the natural logarithm is not defined at $x = 0$. Its value can be obtained by using the antiderivative $x ln ⁡ \left(\right. x \left.\right) - x$ and evaluating the limit at the lower bound. The result shows that, on the interval $\left(\right. 0 , 1 \left.\right)$, the negative values of $ln ⁡ \left(\right. x \left.\right)$ dominate, leading to a net negative area equal to $- 1$.

The logarithmic function models the growth of information in binary decisions. Each step in binary search answers one yes/no question, which corresponds to one binary bit. This is a deep reason why logarithms are fundamental in computer science and information theory.

## Binary search and the logarithmic function

Imagine we want to find an item in a sorted list of $N$ elements. If we check the elements one by one, and the target is in the $n$-th position, we may need up to $n$ steps to find it. This approach is known as linear search, and its worst-case time complexity is:

$$\mathcal{O} \left(\right. n \left.\right)$$

However, linear search is inefficient for large lists. Can we do better? Yes — by using an algorithm that reduces the search space at each step. This leads us to **binary search**, which has logarithmic complexity:

$$\mathcal{O} \left(\right. log ⁡ n \left.\right)$$

Binary search is an efficient algorithm used to find a target element in a sorted list. The core idea is simple: at each step, the algorithm divides the list in half and keeps only the half that may contain the target. This process continues until the element is found or the list can no longer be divided.

At each step, the search space is divided by 2. This means that if the initial list has $n$ elements, the number of steps required to complete the search is proportional to the number of times we can divide $n$ by 2 before reaching 1. This is exactly the definition of the base-2 logarithm:

$$\text{Number of steps} \approx log_{2} ⁡ n$$

Thus, the time complexity of binary search is:

$$\mathcal{O} \left(\right. log ⁡ n \left.\right)$$

This connection shows how logarithmic functions naturally describe processes that involve repeated halving, such as decision trees, divide-and-conquer algorithms, and exponential decay.

---

If a list contains 1,000,000 elements, binary search can find any element in at most:

$$log_{2} ⁡ \left(\right. 1 , 000 , 000 \left.\right) \approx 19.9$$

So, fewer than 20 steps are needed—an enormous efficiency gain compared to linear search, which may require up to 1,000,000 steps.

##### The elements must be sorted according to an ordering criterion. Binary search only works on sequences that are ordered—typically in ascending order. Without a defined ordering, the algorithm cannot determine which half of the list to discard at each step.
