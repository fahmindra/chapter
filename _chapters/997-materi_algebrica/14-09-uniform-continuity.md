---
layout: chapter
title: "Uniform Continuity"
chapter: "Functions"
chapter_order: 14
section_order: 9
permalink: /materi-algebrica/functions/uniform-continuity/
---

## Introduction

[Ordinary continuity](https://algebrica.org/continuous-functions/) describes the local behaviour of a [function](https://algebrica.org/functions/), where small changes in the input near each point result in small changes in the output. This property can depend on the specific point, and in many contexts, a more robust form of continuity is required to ensure consistent regulation of oscillations across the entire [domain](https://algebrica.org/determining-the-domain-of-a-function/). Uniform continuity addresses this need by requiring a single tolerance for input variations to apply everywhere in the set.

This stability property leads to several important consequences:

- Continuous functions can be extended from dense subsets to their closures.
- [Integrability](https://algebrica.org/indefinite-integrals/) and [limit](https://algebrica.org/limits/) operations behave in a controlled, predictable manner.
- Uncontrolled oscillations near infinity are prevented whenever the domain is compact.

###### Oscillations refer to the variation in the output values of a function over a given region, specifically how much the function rises and falls within a small portion of the domain. For example, the function $sin ⁡ \left(\right. 1 / x \left.\right)$ near the origin exhibits infinite oscillations within any small interval, which makes its behaviour increasingly difficult to control.

## Definition

Consider a function $f : A \subset \mathbb{R} \rightarrow \mathbb{R}$. The function is uniformly continuous on $A$ if, for every $\epsilon > 0$ there exists a $\delta > 0$ such that for all $x , y \in A$ the following implication holds:

$$\left|\right. x - y \left|\right. < \delta \rightarrow \left|\right. f \left(\right. x \left.\right) - f \left(\right. y \left.\right) \left|\right. < \epsilon$$

The essential feature of this definition is that the value of $\delta$ depends solely on $\epsilon$, and not on the particular points $x$ and $y$. The same $\delta$ must be valid for every pair of points in the domain.

![Uniform continuity.](https://algebrica.org/wp-content/uploads/resources/images/uniform-continuity-1.png "Uniform continuity.")

The graph shows the global nature of the condition, highlighting that the same $\delta$ controls the function’s variation throughout the domain. Specifically, whenever $\left|\right. x - y \left|\right. < \delta$, it follows that $\left|\right. f \left(\right. x \left.\right) - f \left(\right. y \left.\right) \left|\right. < \epsilon$ for all $x , y \in A$.

---

The distinction between [continuity](https://algebrica.org/continuous-functions/) and uniform continuity is clarified by comparing the standard definition of continuity at a point $x_{0}$. A function is continuous at $x_{0}$ if, for every $\epsilon > 0$, there exists a $\delta > 0$, which may depend on $x_{0}$, such that:

$$\left|\right. x - x_{0} \left|\right. < \delta \rightarrow \left|\right. f \left(\right. x \left.\right) - f \left(\right. x_{0} \left.\right) \left|\right. < \epsilon$$

The distinction lies in the dependence of $\delta$:

- For ordinary continuity, $\delta$ may vary with each point in the domain.
- For uniform continuity, a single value of $\delta$ is valid for all points in the set.

## Heine–Cantor Theorem

The Heine–Cantor theorem establishes the conditions under which continuity implies uniform continuity. Specifically, on compact sets, the local property of continuity suffices to guarantee the existence of a single global control parameter $\delta$ applicable to the entire domain.

Let $K \subset \mathbb{R}$ be a compact set. If a function $f : K \rightarrow \mathbb{R}$ is continuous on $K$, then it is uniformly continuous on $K$. In particular, since compactness in $\mathbb{R}$ is equivalent to the set being closed and bounded, the theorem admits the following equivalent formulation:

If $f : \left[\right. a , b \left]\right. \rightarrow \mathbb{R}$ is continuous on a closed and bounded interval $\left[\right. a , b \left]\right.$, then $f$ is uniformly continuous on $\left[\right. a , b \left]\right.$.

###### The theorem identifies compactness as the precise structural property of the domain that prevents local continuity from degenerating into purely pointwise behaviour, ensuring instead a global form of regularity.

## Sequential characterization

Uniform continuity can be equivalently formulated in terms of [sequences](https://algebrica.org/sequences/). Specifically, a function $f : A \rightarrow \mathbb{R}$ is uniformly continuous on $A$ if and only if, for every pair of sequences $\left(\right. x_{n} \left.\right)$ and $\left(\right. y_{n} \left.\right)$ in $A$ that satisfy $\left|\right. x_{n} - y_{n} \left|\right. \rightarrow 0$ we also have:

$$\left|\right. f \left(\right. x_{n} \left.\right) - f \left(\right. y_{n} \left.\right) \left|\right. \rightarrow 0$$

This formulation highlights that uniformly continuous functions preserve infinitesimal closeness between sequences, which is also why they map [Cauchy sequences](https://algebrica.org/cauchy-sequence/) to Cauchy sequences.

###### This criterion is particularly useful for establishing that a function is not uniformly continuous, as shown in Example 1.

## Example 1

Consider the function $f \left(\right. x \left.\right) = x^{2}$ on the interval $\mathbb{R}$. This function is continuous everywhere, since it is a [polynomial](https://algebrica.org/polynomials/), but it is not uniformly continuous on $\mathbb{R}$. The reason is that the function grows faster and faster as $\left|\right. x \left|\right.$ increases. For points far from the origin, even a small variation in ( x ) can produce a large variation in $f \left(\right. x \left.\right)$ and no single $\delta$ can control this behaviour simultaneously across the real line.

In contrast, when the function is restricted to a closed and bounded interval $\left[\right. a , b \left]\right.$, it becomes uniformly continuous. On such domains, the growth of the function is effectively bounded. This can be made precise using the sequential characterization and considering the sequences defined by $x_{n} = n + \frac{1}{n}$ and $y_{n} = n .$ The difference between these sequences is given by:

$$\left|\right. x_{n} - y_{n} \left|\right. = \frac{1}{n} \rightarrow 0$$

The difference between the images of these sequences under the function satisfies:

$$\left|\right. f \left(\right. x_{n} \left.\right) - f \left(\right. y_{n} \left.\right) \left|\right. = \left(\left(\right. n + \frac{1}{n} \left.\right)\right)^{2} - n^{2} = 2 + \frac{1}{n^{2}} \rightarrow 2$$

Since $\left|\right. f \left(\right. x_{n} \left.\right) - f \left(\right. y_{n} \left.\right) \left|\right.$ does not tend to zero, the function fails the sequential criterion for uniform continuity, therefore, the function is not uniformly continuous on $\mathbb{R}$.

---

This example clarifies the relationship between continuity and uniform continuity. In general terms we have:

- Continuity does not imply uniform continuity. A function may be continuous at every point of its domain without satisfying a single global $\delta$ that works uniformly for all pairs of points.
- Uniform continuity, however, is a stronger condition. If a function is uniformly continuous on $A$, then it is necessarily continuous at every point of $A$.

## Lipschitz Continuity

A particular form of uniform continuity is Lipschitz continuity. A function $f : A \subset \mathbb{R} \rightarrow \mathbb{R}$ is said to be Lipschitz continuous on $A$ if there exists a constant $L > 0$, called a Lipschitz constant, such that, for all ( x,y \in A ) we have:

$$\left|\right. f \left(\right. x \left.\right) - f \left(\right. y \left.\right) \left|\right. \leq L \left|\right. x - y \left|\right.$$

This condition guarantees that nearby points are mapped to nearby values and establishes a global linear bound on the function’s oscillation: the output’s variation is proportional to the input’s variation. The same constant $L$ must work everywhere on the domain. The implication for uniform continuity follows directly. Given any $\epsilon > 0$, selecting $\delta = \epsilon / L$ guarantees that:

$$\left|\right. x - y \left|\right. < \delta \rightarrow \left|\right. f \left(\right. x \left.\right) - f \left(\right. y \left.\right) \left|\right. \leq L \left|\right. x - y \left|\right. < L \delta = \epsilon$$

Therefore, every Lipschitz continuous function is uniformly continuous.

However, the converse does not hold in general. A function may be uniformly continuous without satisfying any global linear bound of this form. Thus, Lipschitz continuity constitutes a strictly stronger condition.

A useful criterion links Lipschitz continuity to [differentiability](https://algebrica.org/derivatives/). If a function $f$ is differentiable on an interval and its derivative is bounded, that is, there exists $M > 0$ such that for all $x$ in the interval:

$$\left|\right. f^{'} \left(\right. x \left.\right) \left|\right. \leq M$$

Then, by the [Mean Value Theorem](https://algebrica.org/lagrange-theorem/), $f$ is Lipschitz continuous with Lipschitz constant $L = M$. For any two points $x , y$ in the interval, there exists $c$ between them such that:

$$f \left(\right. x \left.\right) - f \left(\right. y \left.\right) = f^{'} \left(\right. c \left.\right) \left(\right. x - y \left.\right)$$

Taking [absolute values](https://algebrica.org/absolute-value/) then yields $\left|\right. f \left(\right. x \left.\right) - f \left(\right. y \left.\right) \left|\right. \leq M \left|\right. x - y \left|\right.$, which is the Lipschitz condition with constant $L = M$.

###### Geometrically, Lipschitz continuity restricts the steepness of the graph. The slopes of all secant lines are uniformly bounded in magnitude by $L$. Thus, the function cannot oscillate more rapidly than a fixed linear rate.

## Example 2

###### The Heine–Cantor theorem guarantees uniform continuity whenever the [domain](https://algebrica.org/determining-the-domain-of-a-function/) is compact. However, compactness is a sufficient but not necessary condition, and uniform continuity can also hold on domains that are not compact. This example demonstrates this situation.

Consider the function $f \left(\right. x \left.\right) = sin ⁡ \left(\right. x \left.\right)$ defined on the entire real line $\mathbb{R}$. The domain is unbounded and not compact, so uniform continuity is not guaranteed a priori and must be verified directly.

Given $\epsilon > 0$ and arbitrary $x , y \in \mathbb{R}$, the objective is to find a single $\delta > 0$, depending only on $\epsilon$, such that whenever $\left|\right. x - y \left|\right. < \delta$, it follows that $\left|\right. sin ⁡ \left(\right. x \left.\right) - sin ⁡ \left(\right. y \left.\right) \left|\right. < \epsilon$. Applying the [sum-to-product identity](https://algebrica.org/trigonometric-identities/) yields:

$$\left|\right. sin ⁡ \left(\right. x \left.\right) - sin ⁡ \left(\right. y \left.\right) \left|\right. = 2 \left|\right. cos \left(\right. \frac{x + y}{2} \left.\right) sin \left(\right. \frac{x - y}{2} \left.\right) \left|\right.$$

Since $\left|\right. cos ⁡ \left(\right. \cdot \left.\right) \left|\right. \leq 1$ everywhere, this simplifies to:

$$\left|\right. sin ⁡ \left(\right. x \left.\right) - sin ⁡ \left(\right. y \left.\right) \left|\right. \leq 2 \left|\right. sin \left(\right. \frac{x - y}{2} \left.\right) \left|\right.$$

Applying the standard inequality $\left|\right. sin ⁡ \left(\right. t \left.\right) \left|\right. \leq \left|\right. t \left|\right.$, valid for all $t \in \mathbb{R}$, gives:

$$\left|\right. sin ⁡ \left(\right. x \left.\right) - sin ⁡ \left(\right. y \left.\right) \left|\right. \leq 2 \cdot \frac{\left|\right. x - y \left|\right.}{2} = \left|\right. x - y \left|\right.$$

This satisfies the Lipschitz condition with constant $L = 1$, which holds for every pair of points in $\mathbb{R}$ without restriction. By selecting $\delta = \epsilon$, whenever $\left|\right. x - y \left|\right. < \delta$, it follows that:

$$\left|\right. sin ⁡ \left(\right. x \left.\right) - sin ⁡ \left(\right. y \left.\right) \left|\right. \leq \left|\right. x - y \left|\right. < \delta = \epsilon$$

Here, $\delta$ depends solely on $\epsilon$, therefore, $f$ is uniformly continuous on $\mathbb{R}$.

###### The underlying reason is geometric: the [sine function](https://algebrica.org/sine-function/) oscillates indefinitely, but its oscillations remain permanently bounded in amplitude, and its slope never exceeds one in absolute value, since $\left|\right. f^{'} \left(\right. x \left.\right) \left|\right. = \left|\right. cos ⁡ \left(\right. x \left.\right) \left|\right. \leq 1$ everywhere. This global bound on the rate of change prevents the uncontrolled growth observed in Example 1 and ensures that a uniform $\delta$ is attainable across the entire real line.

## Summary

|  |
| --- |
| Pointwise continuity does not imply uniform continuity. |
| Uniform continuity implies pointwise continuity. |
| Lipschitz continuity implies uniform continuity. |

## Selected references

- **MIT, S. Rodriguez**. [Uniform Continuity and Derivative](https://ocw.mit.edu/courses/18-100a-real-analysis-fall-2020/mit18_100af20_lec17.pdf)
- **University of Wisconsin–Madison, J.W. Robbin**. [Continuity and Uniform Continuity](https://people.math.wisc.edu/~jwrobbin/521dir/cont.pdf)
- **University of Maryland, D. Cellarosi**. [Uniform Continuity](https://www.math.umd.edu/~immortal/MATH410/lecturenotes/ch3-4.pdf)
- **University of California, N. Donaldson**. [Continuity and Uniform Continuity](https://www.math.uci.edu/~ndonalds/math140b/1contrev.pdf)
- **Michigan State University, J. Shapiro**. [Notes on Uniform Continuity](https://users.math.msu.edu/users/shapiro/Teaching/classes/320/Handouts/Unif_contin_notes.pdf)
