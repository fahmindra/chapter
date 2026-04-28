---
layout: chapter
title: "Fundamental Theorem of Calculus"
chapter: "Integrals"
chapter_order: 18
section_order: 3
permalink: /materi-algebrica/integrals/fundamental-theorem-of-calculus/
---

## Introduction

The Fundamental Theorem of Calculus establishes the exact relationship between [differentiation](https://algebrica.org/derivatives/) and [integration](https://algebrica.org/indefinite-integrals/). These two operations arise from different initial motivations. Differentiation describes instantaneous variation, while integration measures accumulated quantity. The theorem proves that, under suitable regularity assumptions, they are inverse processes. The result is traditionally divided into two complementary statements:

- The First Fundamental Theorem of Calculus
- The Second Fundamental Theorem of Calculus

###### As will be shown in the following sections, the First Fundamental Theorem guarantees that every continuous function on a closed interval admits an antiderivative, constructed explicitly via integration. The Second expresses the practical consequence: the definite integral of a function over an interval can be computed directly from any of its antiderivatives, evaluated at the endpoints.

## The First Fundamental Theorem of Calculus

Let $f$ be [continuous](https://algebrica.org/continuous-functions/) on a [closed interval](https://algebrica.org/intervals/) $\left[\right. a , b \left]\right.$. Define the function:

$$F \left(\right. x \left.\right) = \int_{a}^{x} f \left(\right. t \left.\right) d t$$

for $x \in \left[\right. a , b \left]\right.$. Then $F$ is continuous on $\left[\right. a , b \left]\right.$, differentiable on $\left(\right. a , b \left.\right)$, and:

$$F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$$

This statement asserts that the function defined by accumulation of area from a fixed lower bound up to a variable upper limit is differentiable, and its derivative coincides with the original integrand. To justify this result, consider the [difference quotient](https://algebrica.org/difference-quotient/):

$$\frac{F \left(\right. x + h \left.\right) - F \left(\right. x \left.\right)}{h} = \frac{1}{h} \left(\right. \int_{a}^{x + h} f \left(\right. t \left.\right) d t - \int_{a}^{x} f \left(\right. t \left.\right) d t \left.\right)$$

[Definite integrals](https://algebrica.org/definite-integrals/) satisfy the additivity property over adjacent intervals:
$$\int_{a}^{b} f \left(\right. t \left.\right) d t + \int_{b}^{c} f \left(\right. t \left.\right) d t = \int_{a}^{c} f \left(\right. t \left.\right) d t$$
Applying this to our case, we obtain:
$$\frac{1}{h} \int_{x}^{x + h} f \left(\right. t \left.\right) d t$$

Since $f$ is continuous on $\left[\right. x , x + h \left]\right.$, the Mean Value Theorem for integrals guarantees the existence of a point $c$ between $x$ and $x + h$ such that:

$$\int_{x}^{x + h} f \left(\right. t \left.\right) d t = f \left(\right. c \left.\right) h$$

Hence:

$$\frac{F \left(\right. x + h \left.\right) - F \left(\right. x \left.\right)}{h} = f \left(\right. c \left.\right)$$

As $h \rightarrow 0$, the point $c \rightarrow x$. By continuity of $f$, it follows that

$$\underset{h \rightarrow 0}{lim} \frac{F \left(\right. x + h \left.\right) - F \left(\right. x \left.\right)}{h} = f \left(\right. x \left.\right)$$

which proves $F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$. Conceptually, this theorem shows that accumulation produces a function whose instantaneous rate of change recovers the original density.

---

From a geometric point of view, The First Fundamental Theorem interprets the function:

$$F \left(\right. x \left.\right) = \int_{a}^{x} f \left(\right. t \left.\right) d t$$

as accumulated signed area. The derivative $F^{'} \left(\right. x \left.\right)$ represents the instantaneous rate at which this area grows. If $f \left(\right. x \left.\right) > 0$, the area increases; if $f \left(\right. x \left.\right) < 0$, it decreases.

![](https://algebrica.org/wp-content/uploads/resources/images/fundamental-theorem-calculus-1.png)

## The Second Fundamental Theorem of Calculus

Let $f$ be continuous on $\left[\right. a , b \left]\right.$, and suppose $F$ is any antiderivative of $f$, meaning:

$$F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$$

Then:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$$

This second statement converts the evaluation of a definite integral into the computation of a difference of antiderivative values. To see the structural connection with the first part, define:

$$G \left(\right. x \left.\right) = \int_{a}^{x} f \left(\right. t \left.\right) d t$$

From the First Fundamental Theorem, $G^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$. Since both $F$ and $G$ have the same derivative, their difference is constant:

$$F \left(\right. x \left.\right) = G \left(\right. x \left.\right) + c$$

Evaluating at $x = a$ gives:

$$F \left(\right. a \left.\right) = G \left(\right. a \left.\right) + c$$

Because $G \left(\right. a \left.\right) = 0$, we obtain $c = F \left(\right. a \left.\right)$, and therefore:

$$G \left(\right. x \left.\right) = F \left(\right. x \left.\right) - F \left(\right. a \left.\right)$$

Setting $x = b$ yields:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = G \left(\right. b \left.\right) = F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$$

Thus the definite integral measures the net change of any primitive over the interval.

---

The Second Fundamental Theorem has a geometric side that is worth pausing on. Given a continuous function $f$ on $\left[\right. a , b \left]\right.$ and any antiderivative $F$, the definite integral measures the net signed area between the graph of $f$ and the horizontal axis. The theorem tells us that this area equals $F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$, nothing more than the net change in $F$ across the interval.

What makes this striking is that one does not need to reconstruct the area piece by piece. The antiderivative $F$ already carries that information inside it, accumulated continuously. Evaluating it at the two endpoints and taking the difference is enough. The entire geometry of the curve between $a$ and $b$ collapses into a single arithmetic operation.

## Example 1

Consider the following integral:
$$\int_{0}^{1} 3 x^{2} d x$$
An antiderivative of $3 x^{2}$ is $F \left(\right. x \left.\right) = x^{3}$. By the Second Fundamental Theorem we have:
$$\int_{0}^{1} 3 x^{2} d x = F \left(\right. 1 \left.\right) - F \left(\right. 0 \left.\right) = 1^{3} - 0^{3} = 1$$
The area under the curve $3 x^{2}$ over the interval $\left[\right. 0 , 1 \left]\right.$ is therefore exactly $1$, obtained without any geometric argument, but solely through the evaluation of an antiderivative at the endpoints.

---

As a second illustration, define:
$$H \left(\right. x \left.\right) = \int_{1}^{x} ln ⁡ t d t$$
Note that $H \left(\right. 1 \left.\right) = 0$, since the integral over a degenerate interval is zero. Since $ln ⁡ t$ is continuous for $t > 0$, the function $H$ is defined for $x > 0$, and the First Fundamental Theorem implies:
$$H^{'} \left(\right. x \left.\right) = ln ⁡ x$$
The derivative of the accumulation function recovers the integrand exactly, confirming that integration and differentiation are inverse operations in the precise sense established by the theorem.

## Example 2

Apply the First Fundamental Theorem of Calculus to find the following derivative:

$$\frac{d}{d x} \int_{1}^{x} e^{- t^{2}} d t$$

- The integrand here is $f \left(\right. t \left.\right) = e^{- t^{2}}$, a continuous function on all of $\mathbb{R}$.
- The lower bound of integration is the constant $1$, and the upper bound is the variable $x$.

This is precisely the setting of the First Fundamental Theorem: if $F \left(\right. x \left.\right) = \int_{a}^{x} f \left(\right. t \left.\right) d t$, then $F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$.

Applying this directly we obtain:

$$\frac{d}{d x} \int_{1}^{x} e^{- t^{2}} d t = e^{- x^{2}}$$

###### The derivative of the accumulation function recovers the integrand evaluated at $x$. Note that $e^{- t^{2}}$ has no closed-form antiderivative in terms of elementary functions, yet the First Fundamental Theorem allows us to differentiate the integral without ever computing it explicitly.

## Selected references

- **MIT**. [Proof of the First Fundamental Theorem of Calculus](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/e5e4813ac3a0b21f61532842c7ce8a8c_MIT18_01SCF10_Ses52b.pdf)
- **University of California, Berkeley**. [The Fundamental Theorem of Calculus](https://math.berkeley.edu/~ogus/Math_1A/lectures/fundamental.pdf)
- **Michigan State University**. [The Fundamental Theorem of Calculus](https://users.math.msu.edu/users/mccarthy/MTH132/fundamental.theorem.pdf)
- **Dartmouth College**. [The Fundamental Theorem of Calculus](https://math.dartmouth.edu/opencalc2/dcsbook/c4pdf/sec43.pdf)
- **Stony Brook University**. [The Fundamental Theorem of Calculus](https://www.math.stonybrook.edu/~ndang/mat126-fall20/sec_1.3.pdf)
