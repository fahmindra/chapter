---
layout: chapter
title: "Trigonometric Inequalities"
chapter: "Inequalities"
chapter_order: 8
section_order: 8
permalink: /materi-algebrica/inequalities/trigonometric-inequalities/
---

general solutionssystemsmonotonicityperiodic solutionstangent inequalitiescosine inequalitiessine inequalitiessolution setsinterval solutionsfactorizationquadratic reductionsubstitutiontrigonometric identitiesisolationrangesdomainsreference anglesunit circleperiodicitytrigonometric functionscasesmethodsstructure

## Introduction

A trigonometric inequality is an inequality in which the unknown appears as the argument of one or more trigonometric functions. Unlike algebraic inequalities, the solution set is typically an infinite union of intervals, a consequence of the periodic nature of the functions involved. This page focuses on the three fundamental cases involving [sine and cosine](https://algebrica.org/sine-and-cosine/), and [tangent](https://algebrica.org/tangent-and-cotangent/), and then examines how more complex expressions can be reduced to these standard forms.

---

The method for solving trigonometric inequalities is based on a geometric interpretation of the unit circle. As a reminder, $sin ⁡ x$ corresponds to the vertical coordinate, and $cos ⁡ x$ to the horizontal coordinate, of the point determined by the angle $x$ on the [unit circle](https://algebrica.org/unit-circle/).

![](https://algebrica.org/wp-content/uploads/resources/images/unit-circle-4-1.png)

- The vertical segment $\overset{―}{P R}$ is defined as the [sine](https://algebrica.org/sine-and-cosine) of the angle $\theta$.
- The horizontal segment $\overset{―}{O R}$ is defined as the [cosine](https://algebrica.org/sine-and-cosine) of the angle $\theta$.
- The vertical segment $\overset{―}{S T}$ is defined as the [tangent](https://algebrica.org/tangent-and-cotangent) of the angle $\theta$.

Determining where these coordinates are greater or less than a specified value constitutes the geometric approach to solving such inequalities. Since sine and cosine are periodic with period $2 \pi$, and tangent with period $\pi$, solutions identified within a single period must be generalised to the entire real line by adding integer multiples of the relevant period.

## Inequalities involving sine

Consider an inequality of the form below, where $k$ is a real constant with $\left|\right. k \left|\right. \leq 1$.

$$sin ⁡ x > k$$

The first step is to locate the [reference angle](https://algebrica.org/reduction-formulas-and-reference-angles/) $\alpha = arcsin ⁡ k$, which lies in $\left[\right. - \pi / 2 , \pi / 2 \left]\right.$. On the unit circle, the condition $sin ⁡ x > k$ is satisfied on the arc where the vertical coordinate exceeds $k$. This arc runs counterclockwise from $\alpha$ to $\pi - \alpha$.

![](https://algebrica.org/wp-content/uploads/resources/images/trig-inequ-1-2.png)

The solution within one period is therefore the open interval $\left(\right. \alpha , \pi - \alpha \left.\right)$, and the general solution on $\mathbb{R}$ is the following.

$$\alpha + 2 k \pi < x < \pi - \alpha + 2 k \pi$$
$$k \in \mathbb{Z}$$

For the non-strict version $sin ⁡ x \geq k$, the endpoints are included and the intervals become closed.

- When $k > 1$ the inequality has no solution, since $sin ⁡ x \leq 1$ for all $x$.
- When $k < - 1$ the inequality is satisfied for every real number.

---

For example, find all real solutions to the following inequality:

$$sin ⁡ x > \frac{\sqrt{3}}{2}$$

The reference angle is $arcsin ⁡ \left(\right. \sqrt{3} / 2 \left.\right) = \pi / 3$. Since the sine function exceeds $\sqrt{3} / 2$ on the arc between $\pi / 3$ and $\pi - \pi / 3 = 2 \pi / 3$, the general solution is:

$$\frac{\pi}{3} + 2 k \pi < x < \frac{2 \pi}{3} + 2 k \pi$$
$$k \in \mathbb{Z}$$

###### A practical remark: solving trigonometric inequalities in closed form requires familiarity with the principal values of sine and cosine at the standard angles $\pi / 6$, $\pi / 4$, $\pi / 3$, and $\pi / 2$. Without this, the step from $arcsin ⁡ \left(\right. \sqrt{3} / 2 \left.\right)$ to $\pi / 3$ is not immediate.

## Inequalities involving cosine

An inequality of the form below is handled similarly, though the relevant arc on the unit circle is now symmetric about the horizontal axis.

$$cos ⁡ x < k$$

Let $\alpha = arccos ⁡ k \in \left[\right. 0 , \pi \left]\right.$. The condition $cos ⁡ x < k$ is satisfied where the horizontal coordinate of the unit circle point falls below $k$. This occurs on the arc running from $\alpha$ to $2 \pi - \alpha$ (equivalently, from $\alpha$ to $- \alpha$ going clockwise through $\pi$).

![](https://algebrica.org/wp-content/uploads/resources/images/trig-inequ-2-1.png)

The general solution is stated as follows:

$$\alpha + 2 k \pi < x < 2 \pi - \alpha + 2 k \pi$$
$$k \in \mathbb{Z}$$

An equivalent and often more compact form uses the symmetric interval around $\pi$.

---

For example, determine the solution set of the inequality below:

$$cos ⁡ x \leq - \frac{1}{2}$$

The [reference angle](https://algebrica.org/reduction-formulas-and-reference-angles/) is $arccos ⁡ \left(\right. - 1 / 2 \left.\right) = 2 \pi / 3$. Since the inequality is non-strict, the solution in each period is the closed interval $\left[\right. 2 \pi / 3 , 4 \pi / 3 \left]\right.$, and the general solution on $\mathbb{R}$ is the following.

$$\frac{2 \pi}{3} + 2 k \pi \leq x \leq \frac{4 \pi}{3} + 2 k \pi$$
$$k \in \mathbb{Z}$$

###### As with the sine case discussed above, solving cosine inequalities in closed form requires familiarity with the principal values of cosine at the standard angles $\pi / 6$, $\pi / 4$, $\pi / 3$, and $\pi / 2$. Without this, the step from $arccos ⁡ \left(\right. - 1 / 2 \left.\right)$ to $2 \pi / 3$ is not immediate.

## Inequalities involving tangent

The tangent function has period $\pi$ and is strictly increasing on each interval of the form $\left(\right. - \pi / 2 + k \pi , \pi / 2 + k \pi \left.\right)$. This monotonicity considerably simplifies the analysis: within each such interval, the inequality $tan ⁡ x > k$ reduces to a straightforward comparison with the reference angle $arctan ⁡ k$.

![](https://algebrica.org/wp-content/uploads/resources/images/trig-inequ-3.png)

Consider the following inequality:

$$tan ⁡ x > k$$

The general solution is:

$$arctan ⁡ k + n \pi < x < \frac{\pi}{2} + n \pi$$
$$n \in \mathbb{Z}$$

The upper bound $\pi / 2 + n \pi$ is a vertical asymptote and is therefore always excluded, regardless of whether the inequality is strict or not.

---

For example, solve the inequality stated below:

$$tan ⁡ x \leq - 1$$

The reference angle is $arctan ⁡ \left(\right. - 1 \left.\right) = - \pi / 4$. Since [tangent](https://algebrica.org/tangent-and-cotangent/) is increasing on each branch, the condition $tan ⁡ x \leq - 1$ is satisfied from the left endpoint of each branch up to and including $- \pi / 4$. The general solution is the following.

$$- \frac{\pi}{2} + n \pi < x \leq - \frac{\pi}{4} + n \pi$$
$$n \in \mathbb{Z}$$

The left endpoint is excluded because the tangent function is not defined there.

## Reducible inequalities

Many trigonometric inequalities do not appear in standard form but can be reduced to one of the cases above through algebraic manipulation or the application of trigonometric identities.

Consider the inequality below, obtained by isolating the sine function from a linear expression.

$$2 sin ⁡ x - \sqrt{2} \geq 0$$

Isolating the sine function gives $sin ⁡ x \geq \sqrt{2} / 2$. This is now in standard form with $k = \sqrt{2} / 2$ and reference angle $\pi / 4$, so the general solution is the following.

$$\frac{\pi}{4} + 2 k \pi \leq x \leq \frac{3 \pi}{4} + 2 k \pi$$
$$k \in \mathbb{Z}$$

---

A second class of reducible inequalities arises when the argument of the trigonometric function is not simply $x$ but a linear expression in $x$. Consider the following inequality:

$$sin \left(\right. 2 x - \frac{\pi}{3} \left.\right) > \frac{1}{2}$$

Introducing the substitution $t = 2 x - \pi / 3$, the inequality becomes:

$$sin ⁡ t > 1 / 2$$

The solution is:

$$\pi / 6 + 2 k \pi < t < 5 \pi / 6 + 2 k \pi$$

Substituting back and solving for $x$: since $t = 2 x - \pi / 3$, we can write:

$$\pi / 6 + 2 k \pi < 2 x - \pi / 3 < 5 \pi / 6 + 2 k \pi$$

Adding $\pi / 3$ throughout gives:

$$\pi / 2 + 2 k \pi < 2 x < 7 \pi / 6 + 2 k \pi$$

Dividing every term by 2, because all expressions are being scaled uniformly without altering the direction of the inequalities, one obtains the following.

$$\frac{\pi}{4} + k \pi < x < \frac{7 \pi}{12} + k \pi$$
$$k \in \mathbb{Z}$$

---

A third reduction technique applies when the inequality is [quadratic](https://algebrica.org/quadratic-equations/) in a trigonometric function. Consider the following:

$$2 cos^{2} ⁡ x - cos ⁡ x - 1 > 0$$

Setting $u = cos ⁡ x$, this becomes the [quadratic inequality](https://algebrica.org/quadratic-inequalities/):
$$2 u^{2} - u - 1 > 0$$

[Factoring](https://algebrica.org/factoring-ac-method/) yields $\left(\right. 2 u + 1 \left.\right) \left(\right. u - 1 \left.\right) > 0$, which holds when $u < - 1 / 2$ or $u > 1$. Since $cos ⁡ x \leq 1$ for all real $x$, the condition $cos ⁡ x > 1$ is never satisfied.

The inequality therefore reduces to $cos ⁡ x < - 1 / 2$, which is the standard cosine case with reference angle $2 \pi / 3$, giving the following.

$$\frac{2 \pi}{3} + 2 k \pi < x < \frac{4 \pi}{3} + 2 k \pi$$
$$k \in \mathbb{Z}$$

## Example 1

A more involved reduction arises when the inequality contains both $sin ⁡ x$ and $cos^{2} ⁡ x$, making a direct substitution impossible without first applying a [trigonometric identity](https://algebrica.org/trigonometric-identities/). Consider the following equations:

$$cos^{2} ⁡ x - sin ⁡ x - 1 > 0$$

The presence of both $cos^{2} ⁡ x$ and $sin ⁡ x$ prevents an immediate substitution. Replacing $cos^{2} ⁡ x$ with $1 - sin^{2} ⁡ x$ via the [Pythagorean identity](https://algebrica.org/pythagorean-identity/) reduces the expression to a single trigonometric function. The inequality becomes the following.

$$1 - sin^{2} ⁡ x - sin ⁡ x - 1 > 0$$

Simplifying, one obtains $- sin^{2} ⁡ x - sin ⁡ x > 0$, or equivalently $sin^{2} ⁡ x + sin ⁡ x < 0$. Setting $u = sin ⁡ x$, this becomes:

$$u^{2} + u < 0$$

which factors as:
$$u \left(\right. u + 1 \left.\right) < 0$$

This holds when $- 1 < u < 0$, that is, when $- 1 < sin ⁡ x < 0$. Since the boundary values $u = 0$ and $u = - 1$ are excluded, the solution within one period is the open interval $\left(\right. \pi , 2 \pi \left.\right)$ with the endpoint $x = 3 \pi / 2$ retained, except that $sin ⁡ \left(\right. 3 \pi / 2 \left.\right) = - 1$ is excluded by the strict inequality.

The general solution is therefore the following.

$$\pi + 2 k \pi < x < 2 \pi + 2 k \pi , k \in \mathbb{Z}$$

## Example 2

A more demanding case arises when none of the three standard reductions applies in isolation. Consider the inequality below, which requires both a substitution and a quadratic factoring step before reaching standard form:

$$sin^{2} ⁡ x - sin ⁡ x \cdot cos ⁡ x < 0$$

Factoring the left-hand side directly, we obtains the following:

$$sin ⁡ x \left(\right. sin ⁡ x - cos ⁡ x \left.\right) < 0$$

This expression involves a product of two factors, each depending on $x$, so neither a simple substitution nor an identity elimination is immediately applicable. Dividing both sides by $cos^{2} ⁡ x$ would introduce tangent but would also require tracking the sign of $cos^{2} ⁡ x$, which is always non-negative and vanishes at the [asymptotes](https://algebrica.org/asymptotes/).

---

A cleaner approach is to divide by $cos^{2} ⁡ x > 0$ on each interval where cosine does not vanish, which does not alter the direction of the inequality, and rewrite the expression in terms of $tan ⁡ x .$

Dividing through by $cos^{2} ⁡ x$, the inequality becomes the following.

$$\frac{sin ⁡ x}{cos ⁡ x} \left(\right. \frac{sin ⁡ x}{cos ⁡ x} - 1 \left.\right) < 0$$

Setting $u = tan ⁡ x$, this reduces to the algebraic inequality $u \left(\right. u - 1 \left.\right) < 0$, which holds when $0 < u < 1$, that is, when $0 < tan ⁡ x < 1$. This is now a system of two standard tangent inequalities to be solved simultaneously within each branch of the tangent function. The inequality $tan ⁡ x > 0$ is satisfied on the following interval:

$$\left(\right. 0 + n \pi , \frac{\pi}{2} + n \pi \left.\right)$$

The inequality $tan ⁡ x < 1$ is satisfied on the following interval:

$$\left(\right. - \frac{\pi}{2} + n \pi , \frac{\pi}{4} + n \pi \left.\right)$$

Taking the intersection within each branch, the general solution is the following.

$$n \pi < x < \frac{\pi}{4} + n \pi$$
$$n \in \mathbb{Z}$$

## Systems of trigonometric inequalities

A system of trigonometric inequalities consists of two or more inequalities that must be satisfied simultaneously. The solution set is the intersection of the individual solution sets, computed period by period.

---

For example, solve the system formed by the two inequalities below:

$$\left{\right. sin ⁡ x \geq 0 \\ cos ⁡ x < \frac{1}{2}$$

The first inequality, $sin ⁡ x \geq 0$, is satisfied for each $k \in \mathbb{Z}$ on:
$$\left[\right. 0 + 2 k \pi , \pi + 2 k \pi \left]\right.$$

The second inequality, $cos ⁡ x < 1 / 2$, has reference angle $arccos ⁡ \left(\right. 1 / 2 \left.\right) = \pi / 3$, and is satisfied on:

$$\left(\right. \pi / 3 + 2 k \pi , 5 \pi / 3 + 2 k \pi \left.\right)$$

To find the intersection, it suffices to work within a single period, say $\left[\right. 0 , 2 \pi \left.\right)$. The first condition restricts attention to $\left[\right. 0 , \pi \left]\right.$. The second condition on this interval is satisfied where $x > \pi / 3$. The intersection within one period is therefore $\left(\right. \pi / 3 , \pi \left]\right.$, and the general solution is the following.

$$\frac{\pi}{3} + 2 k \pi < x \leq \pi + 2 k \pi$$
$$k \in \mathbb{Z}$$
