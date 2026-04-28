---
layout: chapter
title: "Intervals"
chapter: "Sets and Numbers"
chapter_order: 1
section_order: 9
permalink: /materi-algebrica/sets-and-numbers/intervals/
---

## Definition

An interval is a subset of the real line with the property that, whenever two points belong to it, every point lying between them also belongs to it. More precisely, a subset $I \subseteq \mathbb{R}$ is an interval if and only if, for every pair of points $a , b \in I$ with $a < b$, the entire set $x \in \mathbb{R} : a \leq x \leq b$
is contained in $I$. This property, known as convexity on the [real line](https://algebrica.org/real-numbers/), distinguishes intervals from arbitrary subsets of $\mathbb{R}$ such as finite sets or unions of disconnected pieces.

Intervals are among the most fundamental objects in mathematical analysis. They appear
as [domains of functions](https://algebrica.org/determining-the-domain-of-a-function/), as regions of integration](…/definite-integrals/), as sets on which [continuity](https://algebrica.org/continuous-functions/) and [differentiability](https://algebrica.org/derivatives/) are studied and as the building blocks for describing more complex subsets of the real line.

Intervals are classified according to whether their endpoints are included or excluded, and
according to whether they are bounded or extend indefinitely in one or both directions.

## Bounded intervals

A bounded interval is one that is contained within a finite portion of the real line, that
is, one for which there exist real numbers $a$ and $b$ with $a \leq b$
such that the interval is a subset of $\left[\right. a , b \left]\right.$. The open interval with endpoints $a$ and $b$ is the set of all real numbers strictly between $a$ and $b$, excluding both endpoints. It is defined as follows:
$$\left(\right. a , b \left.\right) = x \in \mathbb{R} : a < x < b$$

|  | $$a$$ | $$b$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

The closed interval with endpoints $a$ and $b$ is the set of all real numbers
between $a$ and $b$, including both endpoints. It is defined as follows:
$$\left[\right. a , b \left]\right. = x \in \mathbb{R} : a \leq x \leq b$$

|  | $$a$$ | $$b$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

The two half-open intervals with endpoints $a$ and $b$ include one endpoint and
exclude the other. They are defined as follows:
$$\left[\right. a , b \left.\right) = x \in \mathbb{R} : a \leq x < b$$

|  | $$a$$ | $$b$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

$$\left(\right. a , b \left]\right. = x \in \mathbb{R} : a < x \leq b$$

|  | $$a$$ | $$b$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

A degenerate interval is the special case $\left[\right. a , a \left]\right. = \left{\right. a \left.\right}$, which contains exactly
one point. It satisfies the definition of an interval vacuously, since there are no two
distinct points between which additional points could be required.

## Unbounded intervals

An unbounded interval extends indefinitely in at least one direction. Since infinity is not
a real number, the symbols $+ \infty$ and $- \infty$ are used purely as notational
conventions to indicate that the interval has no finite bound in the corresponding direction.
Consequently, the endpoints $+ \infty$ and $- \infty$ are always excluded, and
the corresponding bracket is always a parenthesis. The four unbounded intervals are defined as follows.
$$\left[\right. a , + \infty \left.\right) = x \in \mathbb{R} : x \geq a$$

|  | $$a$$ |  |
| --- | --- | --- |
|  |  |  |
|  |  |  |

$$\left(\right. a , + \infty \left.\right) = x \in \mathbb{R} : x > a$$

|  | $$a$$ |  |
| --- | --- | --- |
|  |  |  |
|  |  |  |

$$\left(\right. - \infty , b \left]\right. = x \in \mathbb{R} : x \leq b$$

|  | $$b$$ |  |
| --- | --- | --- |
|  |  |  |
|  |  |  |

$$\left(\right. - \infty , b \left.\right) = x \in \mathbb{R} : x < b$$

|  | $$b$$ |  |
| --- | --- | --- |
|  |  |  |
|  |  |  |

Finally, the entire real line is itself an interval, denoted $\left(\right. - \infty , + \infty \left.\right) = \mathbb{R}$, which contains every real number and has no restriction of any kind.

## Operations on intervals

Given two intervals, one may form new sets by combining them through the standard
set-theoretic operations of intersection and union. The intersection $I \cap J$ is the set of all points belonging to both intervals simultaneously. The intersection of two intervals is always an interval, possibly empty or degenerate. Consider for example $I = \left(\right. 1 , 5 \left.\right)$ and $J = \left(\right. 3 , 7 \left.\right)$. The values belonging to both are precisely those in $\left(\right. 3 , 5 \left.\right)$.

|  | $$1$$ | $$3$$ | $$5$$ | $$7$$ |  |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

The third row shows the intersection $\left(\right. 3 , 5 \left.\right)$, which is the portion shared by both
intervals.

---

The union $I \cup J$ is the set of all points belonging to at least one of the two
intervals. Unlike intersection, the union of two intervals is not always an interval: it is
an interval if and only if the two intervals overlap or share an endpoint. Consider the same
example, $I = \left(\right. 1 , 5 \left.\right)$ and $J = \left(\right. 3 , 7 \left.\right)$. Since the two intervals overlap, their
union is the interval $\left(\right. 1 , 7 \left.\right)$.

|  | $$1$$ | $$3$$ | $$5$$ | $$7$$ |  |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

The third row shows the union $\left(\right. 1 , 7 \left.\right)$. By contrast, the union $\left(\right. 1 , 3 \left.\right) \cup \left(\right. 5 , 7 \left.\right)$
is not an interval, because the points between $3$ and $5$ belong to neither set.

## Intervals and neighborhoods

A concept closely related to intervals and central to mathematical analysis is that of a
neighborhood of a point. Given a point $x_{0} \in \mathbb{R}$ and a real number
$\epsilon > 0$, the open interval:

$$\left(\right. x_{0} - \epsilon , x_{0} + \epsilon \left.\right)$$

is called the $\epsilon$-neighborhood of $x_{0}$, or simply a neighborhood of
$x_{0}$. It consists of all points whose distance from $x_{0}$ is strictly less than
$\epsilon$, that is, all $x$ satisfying $\left|\right. x - x_{0} \left|\right. < \epsilon$,
where $\left|\right. \cdot \left|\right.$ denotes the [absolute value](https://algebrica.org/absolute-value/).

|  | $$x_{0} - \epsilon$$ | $$x_{0}$$ | $$x_{0} + \epsilon$$ |  |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |

Neighborhoods provide the language in which the definitions of [limit](https://algebrica.org/limits/), continuity, and differentiability are naturally expressed. A function $f$ is continuous at $x_{0}$ if for every neighborhood of $f \left(\right. x_{0} \left.\right)$ there exists a neighborhood of $x_{0}$ whose image under $f$ is contained in the former. This formulation is equivalent to the classical $\epsilon$-$\delta$ definition and makes the role of intervals explicit.

A point $x_{0}$ is said to be interior to a set $S \subseteq \mathbb{R}$ if some
neighborhood of $x_{0}$ is entirely contained in $S$. Every point of an open
interval is interior to it, which is one reason open intervals play a privileged role in
analysis. By contrast, the endpoints of a closed interval are not interior points: every
neighborhood of an endpoint contains points outside the interval.

## Length of an interval

The length of a bounded interval with endpoints $a$ and $b$ is defined as
$b - a$, regardless of whether the endpoints are included or excluded. That is, the
four intervals $\left(\right. a , b \left.\right)$, $\left[\right. a , b \left.\right)$, $\left(\right. a , b \left]\right.$, and $\left[\right. a , b \left]\right.$ all have
the same length, given by the following expression.
$$ℓ \left(\right. I \left.\right) = b - a$$
This reflects the fact that a single point has no extent: adding or removing a finite number
of points from an interval does not alter its length. A degenerate interval $\left[\right. a , a \left]\right.$
has length $ℓ \left(\right. \left[\right. a , a \left]\right. \left.\right) = 0$, consistently with this observation. Unbounded intervals
have infinite length, in the sense that for every $M > 0$ there exist points in the
interval whose distance exceeds $M$, so no finite value can be assigned as their
length.

This notion of length is the starting point for the theory of measure on the real [line](https://algebrica.org/lines/), which assigns a generalized notion of size to arbitrary subsets of
$\mathbb{R}$. The measure of an interval $\left[\right. a , b \left]\right.$ coincides with its length
$b - a$, and the extension of this assignment to more complex sets, through the
notion of outer measure and measurability, forms the foundation of the [Lebesgue integral](https://algebrica.org/riemann-integrability-criteria/).

## Characterization of intervals

A subset of the real line is said to be connected if it cannot be written as the union of
two disjoint non-empty open sets. The following theorem provides a complete characterization
of intervals in terms of this property. A subset $S \subseteq \mathbb{R}$ is an interval if and only if it is connected.

This result makes precise the intuitive idea that an interval is a portion of the real line
with no gaps. The condition of connectedness rules out sets such as $\left(\right. 1 , 2 \left.\right) \cup \left(\right. 3 , 4 \left.\right)$,
which fail to be intervals precisely because they can be separated into two disjoint open pieces.

|  | $$1$$ | $$2$$ | $$3$$ | $$4$$ |  |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

> The two intervals occupy separate, non-overlapping portions of the real line and cannot be joined into a single connected piece, which confirms that their union is not an interval.

interval theoremconnected subsetsinterval lengthinterior pointsepsilon neighborhoodneighborhoodsinterval relationsdisjoint intervalsoverlapping intervalsinterval inclusionset differenceunionintersectionhalf-open intervalsopen and closedinterval notationpoints between endpointsconvexity propertyreal line subsetanalysisoperationsdefinition
