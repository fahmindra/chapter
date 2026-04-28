---
layout: chapter
title: "Riemann Integrability Criteria"
chapter: "Integrals"
chapter_order: 18
section_order: 12
permalink: /materi-algebrica/integrals/riemann-integrability-criteria/
---

## Introduction

The Riemann integral is built to measure the net area under a bounded [function](https://algebrica.org/functions/) on a [closed interval](https://algebrica.org/intervals/) by approximating it with rectangles. The subtle point is not computing the integral once it exists, but deciding when the [limiting](https://algebrica.org/limits) process is well-defined. This page collects the most useful criteria for Riemann integrability, in a form that is easy to apply when you meet a function that is not obviously [continuous](https://algebrica.org/continuous-functions/).

##### If you want the definition and basic properties of the definite integral first, see: [Definite Integrals](https://algebrica.org/definite-integrals/).

## Partitions, upper sums, lower sums

Let $f : \left[\right. a , b \left]\right. \rightarrow \mathbb{R}$ be bounded. A partition $P$ of $\left[\right. a , b \left]\right.$ is a finite collection of points

$$P = x_{0} , x_{1} , \ldots , x_{n}$$
$$a = x_{0} < x_{1} < \hdots < x_{n} = b$$

On each subinterval $\left[\right. x_{i - 1} , x_{i} \left]\right.$ we record how high and how low the function can reach. Since $f$ is bounded, both quantities are well defined:

$$M_{i} = \underset{x \in \left[\right. x_{i - 1} , x_{i} \left]\right.}{sup} f \left(\right. x \left.\right)$$
$$m_{i} = \underset{x \in \left[\right. x_{i - 1} , x_{i} \left]\right.}{inf} f \left(\right. x \left.\right)$$

- $M_{i}$ is the least upper bound of $f$ on that subinterval (the smallest value that is still at least as large as every value $f$ takes there).
- $m_{i}$ is the greatest lower bound (the largest value that is still no greater than any value $f$ takes there).

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-2.png)

The diagram above shows the lower sum: each rectangle is built using the infimum of $f$ on its subinterval, so every rectangle fits entirely below the curve. No part of any rectangle sticks out above it. The diagram below shows the upper sum: here each rectangle uses the supremum, so the rectangles overshoot the curve and cover more area than is actually there. The true area under the curve lies somewhere between the two.

![](https://algebrica.org/wp-content/uploads/resources/images/definite-integrals-3.png)

As the partition gets finer and the subintervals shrink, the rectangles in both sums become thinner and more numerous, and the two approximations are forced closer and closer together.

---

When $f$ is continuous, these coincide with the actual maximum and minimum on the subinterval. For a general bounded function, sup and inf are used because a maximum or minimum may not be attained. Using $M_{i}$ and $m_{i}$, we define the Darboux upper and lower sums:

$$U \left(\right. f , P \left.\right) = \sum_{i = 1}^{n} M_{i} \left(\right. x_{i} - x_{i - 1} \left.\right)$$
$$L \left(\right. f , P \left.\right) = \sum_{i = 1}^{n} m_{i} \left(\right. x_{i} - x_{i - 1} \left.\right)$$

Two facts keep the whole construction coherent. First, making a partition finer, adding points to it, can only push upper sums down and lower sums up. Second, no matter which partition you choose, the lower sum never exceeds the upper sum:

$$L \left(\right. f , P \left.\right) \leq U \left(\right. f , P \left.\right)$$

Together, these mean that as partitions get finer, the upper and lower sums are squeezed toward each other. When they meet at a common limit, the function is integrable and that limit is the integral.

## The Darboux criterion

Before stating the criterion, it helps to fix two numbers that summarize all possible upper and lower sums at once. Define the upper and lower integrals as:

$$U \left(\right. f \left.\right) = \underset{P}{inf} U \left(\right. f , P \left.\right)$$
$$L \left(\right. f \left.\right) = \underset{P}{sup} L \left(\right. f , P \left.\right)$$

where the infimum and supremum range over all partitions $P$ of $\left[\right. a , b \left]\right.$. In plain terms:

- $U \left(\right. f \left.\right)$ is the smallest value the upper sums can be pushed down to, by choosing finer and finer partitions.
- $L \left(\right. f \left.\right)$ is the largest value the lower sums can be pushed up to.

One can show that $L \left(\right. f \left.\right) \leq U \left(\right. f \left.\right)$ always holds, regardless of the function.

---

A bounded function $f$ is Riemann integrable on $\left[\right. a , b \left]\right.$ if and only if these two numbers coincide:

$$U \left(\right. f \left.\right) = L \left(\right. f \left.\right)$$

In that case, their common value is the integral:

$$\int_{a}^{b} f \left(\right. x \left.\right) d x = U \left(\right. f \left.\right) = L \left(\right. f \left.\right)$$

This is clean as a definition, but in practice it is hard to compute $U \left(\right. f \left.\right)$ and $L \left(\right. f \left.\right)$ directly. The following equivalent formulation is far more useful when you actually want to prove integrability: a bounded function $f$ is Riemann integrable on $\left[\right. a , b \left]\right.$ if and only if for every $\epsilon > 0$ there exists a partition $P$ such that

$$U \left(\right. f , P \left.\right) - L \left(\right. f , P \left.\right) < \epsilon$$

![](https://algebrica.org/wp-content/uploads/resources/images/riemann-integrability-1.png)

The difference becomes clear looking at the two diagrams. With a coarse partition, each rectangle is wide enough to leave a noticeable gap between the upper and lower bounds. Narrowing the subintervals forces both sums to track the curve more closely, and the space between them shrinks accordingly.

![](https://algebrica.org/wp-content/uploads/resources/images/riemann-integrability-2.png)

In other words, you can always find a partition that forces the upper and lower sums as close together as you like. This is the criterion to reach for when you want to prove integrability by squeezing the two sums toward each other.

---

On each subinterval $\left[\right. x_{i - 1} , x_{i} \left]\right.$, the difference $M_{i} - m_{i}$ represents the range of values taken by $f$ on that portion of the interval, that is, its oscillation over that segment. A straightforward computation then shows that:

$$U \left(\right. f , P \left.\right) - L \left(\right. f , P \left.\right) = \sum_{i = 1}^{n} \left(\right. M_{i} - m_{i} \left.\right) \left(\right. x_{i} - x_{i - 1} \left.\right)$$

This is the central idea. A function is integrable if we can divide the interval into sufficiently small pieces so that the variation of the function on each piece contributes only a negligible error to the total sum. If, on the contrary, the function keeps oscillating in an uncontrollable way on every subinterval, no matter how fine the partition, then this condition cannot be met, and the function fails to be integrable in the Riemann sense.

###### Once a function is known to be Riemann integrable, the [Fundamental Theorem of Calculus](https://algebrica.org/fundamental-theorem-of-calculus/) provides the main tool for evaluating it.

## Common sufficient conditions

The Darboux criterion is the foundation, but in practice most functions you encounter fall into one of three categories that guarantee integrability without any direct computation of sums. A function $f$ on $\left[\right. a , b \left]\right.$ is Riemann integrable if it satisfies any one of the following conditions.

- If $f$ is [continuous](https://algebrica.org/continuous-functions/) on $\left[\right. a , b \left]\right.$, integrability follows from uniform continuity: on a closed bounded interval, continuity forces the oscillation $M_{i} - m_{i}$ to be uniformly small on every sufficiently short subinterval, which is exactly what the Darboux criterion requires.
- If $f$ is monotone on $\left[\right. a , b \left]\right.$, the oscillation on each subinterval reduces to a difference of endpoint values. These differences telescope when summed across the partition, and the total $U \left(\right. f , P \left.\right) - L \left(\right. f , P \left.\right)$ can be made small simply by taking the mesh fine enough.
- If $f$ is bounded and has only finitely many discontinuities, each can be enclosed in a subinterval of arbitrarily small length, while the function remains continuous and well-behaved everywhere else.

###### These three conditions are independent: a function can be monotone without being continuous, and can have finitely many discontinuities without being monotone. What they share is that none of them allows discontinuities to accumulate densely, and that is the key.

## The discontinuity-set criterion

A bounded function $f : \left[\right. a , b \left]\right. \rightarrow \mathbb{R}$ is Riemann integrable if and only if its set of discontinuities has Lebesgue measure zero. A set $D \subset \left[\right. a , b \left]\right.$ has measure zero if for every $\epsilon > 0$ you can cover $D$ with a countable collection of intervals whose total length is less than $\epsilon$. The discontinuities can be hidden inside intervals that, taken together, occupy as little of the real line as you want. Two examples show what this means in practice.

##### Lebesgue measure is the standard way of assigning length to subsets of the real line. For an interval $\left[\right. c , d \left]\right.$ it equals $d - c$. A set has measure zero if it can be covered by intervals of arbitrarily small total length — it occupies no space on the line in any meaningful sense. Finite and countable sets, such as the rationals, all have measure zero.

---

[Dirichlet’s function](https://algebrica.org/dirichlet-function/) is defined as:

$$f \left(\right. x \left.\right) = \left{\right. 1 & x \in \mathbb{Q} \\ 0 & x \notin \mathbb{Q}$$

It is [discontinuous](https://algebrica.org/discontinuities-of-real-functions/) at every point of $\left[\right. a , b \left]\right.$, so its discontinuity set is the entire interval, which does not have measure zero. It is not Riemann integrable. Every subinterval contains both rationals and irrationals, so every $M_{i} = 1$ and every $m_{i} = 0$, which gives $U \left(\right. f , P \left.\right) - L \left(\right. f , P \left.\right) = b - a$ for every partition $P$, regardless of how fine it is.

---

Thomae’s function is defined as

$$t \left(\right. x \left.\right) = \left{\right. 0 & x \notin \mathbb{Q} \\ \frac{1}{q} & x = \frac{p}{q} \text{in lowest terms}$$

It is discontinuous exactly at the rationals and continuous at every irrational. The rationals in $\left[\right. a , b \left]\right.$ form a countable set, and every countable set has measure zero. So Thomae’s function is Riemann integrable and its integral over any interval is zero, despite being discontinuous at infinitely many points.

## Recognising Riemann integrability

When you encounter a bounded function $f$ on $\left[\right. a , b \left]\right.$ and need to decide whether it is Riemann integrable, the following sequence of checks usually settles the question quickly.

- If $f$ is continuous on $\left[\right. a , b \left]\right.$, then it is integrable.
- If $f$ is monotone on $\left[\right. a , b \left]\right.$, then it is integrable.
- If $f$ has only finitely many discontinuities, then it is integrable.
- If the discontinuities of $f$ form a set of measure zero, then it is integrable.
- If $f$ is discontinuous on a set that cannot be made small, show that $U \left(\right. f , P \left.\right) - L \left(\right. f , P \left.\right)$ stays bounded away from zero for every partition $P$. Then $f$ is not Riemann integrable.

## Selected references

- **University of California, Davis**. [The Riemann Integral](https://www.math.ucdavis.edu/~hunter/intro_analysis_pdf/ch11.pdf)
- **University of California, Davis**. [Lecture Notes: Riemann Integration](https://www.math.ucdavis.edu/~hunter/m125b/125bLectureNotes_5-26-11.pdf)
- **University of California, Berkeley**. [Notes on Riemann Integral](https://math.berkeley.edu/~wodzicki/H104.F10/Integral.pdf)
