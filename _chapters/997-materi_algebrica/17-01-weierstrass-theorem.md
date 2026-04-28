---
layout: chapter
title: "Weierstrass Theorem"
chapter: "Differential Calculus Theorems"
chapter_order: 17
section_order: 1
permalink: /materi-algebrica/differential-calculus-theorems/weierstrass-theorem/
---

## Statement

Let $f : \left[\right. a , b \left]\right. \rightarrow \mathbb{R}$ be a continuous [function](https://algebrica.org/functions/) on a closed and bounded interval $\left[\right. a , b \left]\right.$. Then there exist points $x_{min} , x_{max} \in \left[\right. a , b \left]\right.$ such that:

$$f \left(\right. x_{min} \left.\right) \leq f \left(\right. x \left.\right) \leq f \left(\right. x_{max} \left.\right) \forall x \in \left[\right. a , b \left]\right.$$

In other words, a [continuous function](https://algebrica.org/continuous-functions/) on a closed interval attains both its minimum and its maximum. This result is often referred to as the Extreme Value Theorem. The following graph illustrates the theorem: the function reaches a maximum and a minimum at two interior points of the interval $\left[\right. a , b \left]\right.$.

![](https://algebrica.org/wp-content/uploads/resources/images/weierstrass-theorem-1.png "Weierstrass Theorem.")

It is helpful to relate the notation to the figure. The quantity $f \left(\right. x_{max} \left.\right)$ denotes the value of the function at the point marked Max in the graph, that is, the highest point reached on the interval. Likewise, $f \left(\right. x_{min} \left.\right)$ represents the value of the function at the point marked min, where the graph attains its lowest value.

---

Each assumption plays a precise role.

- The interval must be closed and bounded. Closed means that the endpoints are included. Bounded means that it has finite length. Together, these conditions express compactness on the real line.
- Continuity is equally essential. The theorem does not require differentiability. It only requires that the function have no jumps or breaks on the interval.
- If either condition is removed, the conclusion may fail.

A full proof lies beyond this page, but the main idea is straightforward. On a closed and bounded interval, a continuous function cannot diverge or skip values. Because the interval includes its endpoints and continuity prevents jumps, the function does not merely approach its largest and smallest values; it actually attains them.

## Why closed and bounded matters

Consider the function $f \left(\right. x \left.\right) = x$ on the open interval $\left(\right. 0 , 1 \left.\right)$.

![](https://algebrica.org/wp-content/uploads/resources/images/weierstrass-theorem-2.png)

The function is continuous, yet it has no maximum and no minimum on that interval. The infimum is $0$ and the supremum is $1$, but neither value is attained because the endpoints are not included.

---

Now consider $f \left(\right. x \left.\right) = \frac{1}{x}$ on $\left(\right. 0 , 1 \left]\right.$. The interval is bounded but not closed. The function is continuous on its [domain](https://algebrica.org/determining-the-domain-of-a-function/), yet it does not attain a maximum. As $x \rightarrow 0^{+}$, the function grows without bound.

###### These examples show that compactness of the domain is not a technical detail but the structural reason the theorem holds.

## Example 1

Let us now see a concrete application of the theorem. Consider the function:

$$f \left(\right. x \left.\right) = x^{3} - 3 x$$

on the interval $\left[\right. - 2 , 2 \left]\right.$. This is a [polynomial](https://algebrica.org/polynomials/), therefore continuous on the whole real line. In particular, it is continuous on the closed and bounded interval $\left[\right. - 2 , 2 \left]\right.$. By Weierstrass’ theorem, we already know that the function must attain both a maximum and a minimum somewhere in this interval. To determine where these extreme values occur, we proceed using differential calculus. First compute the [derivative](https://algebrica.org/derivatives/):

$$f^{'} \left(\right. x \left.\right) = 3 x^{2} - 3 = 3 \left(\right. x^{2} - 1 \left.\right)$$

The critical points are obtained by solving $f^{'} \left(\right. x \left.\right) = 0$:

$$3 \left(\right. x^{2} - 1 \left.\right) = 0 \rightarrow x^{2} = 1$$

so we have:

$$x = - 1 x = 1$$

These are the only interior points where the slope of the tangent line vanishes. However, the absolute extrema on a closed interval may also occur at the endpoints. For this reason, we evaluate the function at all candidates: the critical points and the endpoints.

$$f \left(\right. - 2 \left.\right) = - 2 & f \left(\right. - 1 \left.\right) = 2 \\ f \left(\right. 1 \left.\right) = - 2 & f \left(\right. 2 \left.\right) = 2$$

Comparing these values, we observe that the maximum value is $2$, attained at $x = - 1$ and $x = 2$, while the minimum value is $- 2$, attained at $x = - 2$ and $x = 1$.

###### To summarize, one important point of this example is that Weierstrass’ theorem does not tell us where the extreme values are located, nor how many there are. It simply guarantees that they exist. It is the derivative that allows us to find them explicitly.

## The range of a continuous function

Let $f$ be continuous on a closed and bounded interval $\left[\right. a , b \left]\right.$. By the Weierstrass theorem, $f$ attains a minimum value $m$ and a maximum value $M$ on $\left[\right. a , b \left]\right.$. This means there exist points $x_{min} , x_{max} \in \left[\right. a , b \left]\right.$ such that

$$f \left(\right. x_{min} \left.\right) = m f \left(\right. x_{max} \left.\right) = M$$

By the Intermediate Value Theorem, the function takes every value between $m$ and $M$. In other words, if $y$ satisfies:

$$m \leq y \leq M$$

then there exists some $x \in \left[\right. a , b \left]\right.$ such that $f \left(\right. x \left.\right) = y$. Putting these two facts together, we conclude that the image of $f$ is exactly $f \left(\right. \left[\right. a , b \left]\right. \left.\right) = \left[\right. m , M \left]\right. .$ So a continuous function on a closed interval does not leave gaps in its values, and its range is itself a closed interval.

## Where this theorem is used

The Weierstrass theorem plays a direct role in the proofs of several fundamental theorems of differential calculus.

- [Fermat’s theorem](https://algebrica.org/fermat-theorem/) relies on it to guarantee that a maximum or minimum actually exists on the interval before concluding that the derivative must vanish at that point.
- [Rolle’s theorem](https://algebrica.org/rolles-theorem/) uses it to establish that the function attains its maximum and minimum on the closed interval, which is the first step of its proof.
- [Lagrange’s theorem](https://algebrica.org/lagrange-theorem/) depends on Rolle’s theorem and therefore, indirectly, on Weierstrass as well.

## Selected references

- **University of Washington, J. Burke**. [Weierstrass Extreme Value Theorem](https://sites.math.washington.edu/~burke/crs/408/notes/nlp/unoc.pdf)
- **University of California Davis, J. Hunter**. [Continuous Functions](https://www.math.ucdavis.edu/~hunter/m125a/intro_analysis_ch3.pdf)
- **University of Washington, J. Lee**. [The Extreme Value Theorem in Two Variables](https://sites.math.washington.edu/~lee/Courses/135-2017/EVT.pdf)
- **University of Chicago, J. Murphy**. [Topological Proofs of the Extreme Value Theorems](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2008/REUPapers/Murphy.pdf)
