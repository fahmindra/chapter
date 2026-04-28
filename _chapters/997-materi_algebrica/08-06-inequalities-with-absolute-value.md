---
layout: chapter
title: "Inequalities with Absolute Value"
chapter: "Inequalities"
chapter_order: 8
section_order: 6
permalink: /materi-algebrica/inequalities/inequalities-with-absolute-value/
---

solution checkvariable boundparameter casesmultiple absolute valuesinterval representationcase splittingsolution stepspiecewise forminterval solutionscompound inequalitiesnon-positive boundgreater than caseless than casesymmetry propertynon-negative propertyabsolute expressiondistance from a pointdistance on real lineabsolute valuemethodscasesdefinition

## Introduction

The [absolute value](https://algebrica.org/absolute-value/) of a real number $x$ is defined as follows:

$$\left|\right. x \left|\right. = \left{\right. + x & \text{if} x \geq 0 \\ - x & \text{if} x < 0 \forall x \in \mathbb{R}$$

Geometrically, $\left|\right. x \left|\right.$ represents the distance of $x$ from the origin on the real line, and more generally $\left|\right. x - a \left|\right.$ represents the distance between $x$ and the point $a$. This geometric interpretation is often the most natural way to understand inequalities involving absolute value, and it will guide the intuition behind the solution methods discussed below.

---

The properties that underlie the resolution of such inequalities are the following. For every [real number](https://algebrica.org/properties-of-real-numbers/) $k > 0$ and every real expression $f \left(\right. x \left.\right)$, the following equivalences hold:

- $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq k$ if $- k \leq f \left(\right. x \left.\right) \leq k .$
- $\left|\right. f \left(\right. x \left.\right) \left|\right. \geq k$ if $f \left(\right. x \left.\right) \leq - k$ or $f \left(\right. x \left.\right) \geq k .$

The same equivalences extend naturally to the strict inequality cases, replacing $\leq$ with $<$ and $\geq$ with $>$. When $k = 0$, the inequality $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq 0$ is satisfied only when $f \left(\right. x \left.\right) = 0$, since the absolute value is always non-negative. For $k < 0$, the inequality $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq k$ has no solution for any $x$.

An alternative method, applicable whenever the expression inside the absolute value is [linear](https://algebrica.org/linear-inequalities/), consists in analysing the sign of the argument by means of its piecewise definition. One identifies the point at which the argument vanishes, divides the real line into the two corresponding half-lines, and rewrites the inequality separately on each of them, removing the absolute value. The partial solutions are then collected by union.

###### Solving an inequality involving absolute value follows the same principle as solving an [equation with absolute value](https://algebrica.org/absolute-value-equations/): one applies the defining properties of the absolute value function to remove it algebraically, reducing the problem to a set of ordinary inequalities to be solved and combined.

## The triangle inequality

A fundamental result closely related to inequalities with absolute value is the triangle inequality. For any two real numbers $a$ and $b$, the following relation holds:

$$\left|\right. a + b \left|\right. \leq \left|\right. a \left|\right. + \left|\right. b \left|\right.$$

This inequality states that the absolute value of a sum never exceeds the sum of the absolute values. Its proof and a detailed discussion of its consequences are presented in the entry on the [absolute value](https://algebrica.org/absolute-value/).

###### The result is worth keeping in mind when working with expressions involving sums of absolute values, as it provides an immediate upper bound that can simplify estimates without requiring a full case-by-case analysis.

## Example 1

Consider the following simple inequality:

$$\left|\right. x - 3 \left|\right. \leq 5$$

Applying the fundamental property for the case $\leq$, one obtains a [system](https://algebrica.org/systems-of-inequalities/) of two simultaneous inequalities:

$$- 5 \leq x - 3 \leq 5$$

To isolate $x$, one adds $3$ to all three members of the compound inequality. This operation is admissible because adding the same quantity to both sides of an inequality does not alter its direction.

$$- 5 + 3 \leq x \leq 5 + 3$$

$$- 2 \leq x \leq 8$$

Representing the values obtained on the real line gives the following picture:

|  | $$- 2$$ | $$8$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

The highlighted row represents the intersection of the two conditions: the solution is the set of values of $x$ for which both inequalities are simultaneously satisfied. The solution is therefore the closed interval $\left[\right. - 2 , 8 \left]\right.$.

The solution is therefore the closed interval $\left[\right. - 2 , 8 \left]\right.$.

## Example 2

Consider the following inequality:

$$\left|\right. 2 x + 1 \left|\right. > 3$$

Applying the fundamental property for the case $>$, the inequality splits into two alternative conditions, each of which must be satisfied independently.

$$2 x + 1 < - 3$$
$$2 x + 1 > 3$$

Resolving the first condition, subtracting $1$ from both sides gives $2 x < - 4$, and dividing by $2$ yields $x < - 2$. Since the divisor is positive, the direction of the inequality is preserved.

Resolving the second condition in the same way and subtracting $1$ gives $2 x > 2$, and dividing by $2$ yields $x > 1$.

Representing the values obtained on the real line gives the following picture:

|  | $$- 2$$ | $$1$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

As in the case seen previously, the highlighted row represents the union of the two conditions: the solution is the set of values of $x$ for which at least one of the two inequalities is satisfied.

The solution is therefore the union of open intervals $\left(\right. - \infty , - 2 \left.\right) \cup \left(\right. 1 , + \infty \left.\right)$.

## Example 3

Consider the following inequality, in which two distinct absolute values appear:

$$\left|\right. x + 1 \left|\right. + \left|\right. x - 2 \left|\right. > 4$$

When an inequality contains more than one absolute value, the most systematic approach is to partition the real line according to the zeros of the arguments. The expressions $x + 1$ and $x - 2$ vanish at $x = - 1$ and $x = 2$ respectively, giving three regions to be analysed separately.

---

Case $x < - 1$. In this region $x + 1 < 0$ and $x - 2 < 0$, so both arguments are negative and the absolute value reverses their sign. The inequality becomes the following:

$$- \left(\right. x + 1 \left.\right) + \left(\right. - \left(\right. x - 2 \left.\right) \left.\right) > 4$$

$$- x - 1 - x + 2 > 4$$

$$- 2 x + 1 > 4$$

Subtracting $1$ from both sides gives $- 2 x > 3$. Dividing by $- 2$ and reversing the direction of the inequality, since the divisor is negative, one obtains the following:

$$x < - \frac{3}{2}$$

This condition must hold within the region $x < - 1$. Since $- \frac{3}{2} < - 1$, the condition $x < - \frac{3}{2}$ is the more restrictive of the two, and the intersection with $x < - 1$ reduces to $x < - \frac{3}{2}$. The contribution of this case is therefore $\left(\right. - \infty , - \frac{3}{2} \left.\right)$.

---

Case $- 1 \leq x < 2$. In this region $x + 1 \geq 0$ and $x - 2 < 0$. The inequality becomes the following:

$$\left(\right. x + 1 \left.\right) + \left(\right. - \left(\right. x - 2 \left.\right) \left.\right) > 4$$

$$x + 1 - x + 2 > 4$$

$$3 > 4$$

This is a contradiction, which holds for no value of $x$. Case II therefore yields no solution.

---

Case $x \geq 2$. In this region $x + 1 > 0$ and $x - 2 \geq 0$, so both arguments are non-negative and the absolute value leaves them unchanged. The inequality becomes the following:

$$\left(\right. x + 1 \left.\right) + \left(\right. x - 2 \left.\right) > 4$$

$$2 x - 1 > 4$$

Adding $1$ to both sides gives $2 x > 5$, and dividing by $2$ yields the following:

$$x > \frac{5}{2}$$

Intersecting with $x \geq 2$: since $\frac{5}{2} > 2$, the effective condition is $x > \frac{5}{2}$. The contribution of this case is therefore $\left(\right. \frac{5}{2} , + \infty \left.\right)$.

---

Collecting the contributions from all three cases, the partial solutions obtained on each region of the real line are plotted below.

|  | $$- \frac{3}{2}$$ | $$\frac{5}{2}$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

The union of the two open half-lines gives the complete solution set.

The solution of the inequality is therefore:

$$\left(\right. - \infty , - \frac{3}{2} \left.\right) \cup \left(\right. \frac{5}{2} , + \infty \left.\right)$$

## Example 4

We now consider a more involved case, in which the right-hand side of the inequality is not a fixed number but a [real parameter](https://algebrica.org/equations-with-parameters/) $k$. The structure of the solution set depends on the value of $k$, and a complete discussion requires treating several cases separately. Consider the following inequality:

$$\left|\right. x - 1 \left|\right. > k$$

The behaviour of the solution changes substantially depending on whether $k$ is negative, zero, or positive, and this is what we set out to determine.

---

Case $k < 0$. Since the absolute value is always non-negative, the left-hand side satisfies $\left|\right. x - 1 \left|\right. \geq 0 > k$ for every real $x$. The inequality is therefore satisfied by all real numbers, and the solution is $\mathbb{R}$.

---

Case $k = 0$. The inequality reduces to $\left|\right. x - 1 \left|\right. > 0$, which holds for every $x$ except the point where the absolute value vanishes. Since $\left|\right. x - 1 \left|\right. = 0$ if and only if $x = 1$, the solution is $\mathbb{R} \backslash 1$.

---

Case $k > 0$. Applying the fundamental property for the case $>$, the inequality splits into two alternative conditions:

$$x - 1 < - k$$
$$x - 1 > k$$

Adding $1$ to both sides of each condition yields the following:

$$x < 1 - k \text{or} x > 1 + k$$

---

Representing the solution on the real line gives the following picture:

|  | $$1 - k$$ | $$1 + k$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Note that as $k \rightarrow 0^{+}$ the two boundary points $1 - k$ and $1 + k$ approach $1$ from opposite sides, and the solution set approaches $\mathbb{R} \backslash \left{\right. 1 \left.\right}$, consistently with case $k = 0$.

The solution is therefore the union of two open intervals:
$$\left(\right. - \infty , 1 - k \left.\right) \cup \left(\right. 1 + k , + \infty \left.\right)$$

## Inequalities with a non-constant right-hand side

The equivalences stated above assume that the right-hand side is a positive constant $k$. When the right-hand side is itself a function of $x$, say $g \left(\right. x \left.\right)$, the situation requires additional care. Consider the following inequality.

$$\left|\right. f \left(\right. x \left.\right) \left|\right. \leq g \left(\right. x \left.\right)$$

Applying the same reasoning as before, this is equivalent to the following compound inequality.

$$- g \left(\right. x \left.\right) \leq f \left(\right. x \left.\right) \leq g \left(\right. x \left.\right)$$

However, this reduction is valid only when $g \left(\right. x \left.\right) > 0$. If $g \left(\right. x \left.\right) \leq 0$ at some point, the inequality $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq g \left(\right. x \left.\right)$ cannot be satisfied there, since the left-hand side is always non-negative. The correct approach is therefore to impose $g \left(\right. x \left.\right) > 0$ as a necessary condition and intersect it with the solution of the compound inequality. As a concrete instance, consider the following.

$$\left|\right. x - 1 \left|\right. \leq 2 x - 3$$

The right-hand side $g \left(\right. x \left.\right) = 2 x - 3$ is positive only when $x > \frac{3}{2}$. Outside this region the inequality has no solution regardless of the value of $\left|\right. x - 1 \left|\right.$. Within the region $x > \frac{3}{2}$, the inequality is equivalent to the following system.

$$- \left(\right. 2 x - 3 \left.\right) \leq x - 1 \leq 2 x - 3$$

The left inequality $- \left(\right. 2 x - 3 \left.\right) \leq x - 1$ simplifies to $- 2 x + 3 \leq x - 1$, that is $4 \leq 3 x$, yielding $x \geq \frac{4}{3}$. The right inequality $x - 1 \leq 2 x - 3$ simplifies to $2 \leq x$, yielding $x \geq 2$. Since $\frac{4}{3} < \frac{3}{2} < 2$, the condition $x \geq \frac{4}{3}$ is already implied by the requirement $x > \frac{3}{2}$, and the binding constraint among all three is $x \geq 2$. Representing the solution on the real line gives the following picture.

|  | $$\frac{4}{3}$$ | $$\frac{3}{2}$$ | $$2$$ |  |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

The three critical values appearing in the graph reflect the three independent conditions derived during the solution: the threshold $\frac{4}{3}$ from the left inequality, the threshold $\frac{3}{2}$ from the positivity requirement on $g \left(\right. x \left.\right)$, and the threshold $2$ from the right inequality. Since each condition is more restrictive than the previous one, the effective solution is determined entirely by the rightmost bound.

The solution is therefore the interval $\left[\right. 2 , + \infty \left.\right)$.
