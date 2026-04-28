---
layout: chapter
title: "Sign Analysis in Inequalities"
chapter: "Inequalities"
chapter_order: 8
section_order: 3
permalink: /materi-algebrica/inequalities/sign-analysis-in-inequalities/
---

## What is sign analysis

Sign analysis of inequalities is a method for determining the intervals in which a given expression is positive, negative, or zero. This approach is especially valuable for solving [polynomial](https://algebrica.org/polynomials) and [rational inequalities](https://algebrica.org/rational-inequalities/) and for analysing the behaviour of functions within specified[domains](https://algebrica.org/determining-the-domain-of-a-function/).

---

The sign of a product is determined by whether the number of negative factors is even or odd. A product is positive if the number of negative factors is even, and negative if the number of negative factors is odd. We have:

$$+ \times + & = + \\ + \times - & = - \\ - \times - & = + \\ - \times + & = -$$

## Example 1

Let’s consider a simple [quadratic inequality](https://algebrica.org/quadratic-inequalities/):

$$x^{2} + x - 2 > 0$$

We need to determine the range of x values that satisfy the inequality. First, we can [factor the polynomial](https://algebrica.org/factoring-ac-method/) in the form:

$$\left(\right. x - 1 \left.\right) \left(\right. x + 2 \left.\right) > 0$$

According to the sign product rule, this polynomial factored into the product of two factors is positive when the following condition is met:

$$& x - 1 > 0 \rightarrow x > 1 \\ & x + 2 > 0 \rightarrow x > - 2$$

The values $x = 1$ and $x = - 2$ divide the real line into disjoint intervals. Since the expression is [continuous](https://algebrica.org/continuous-functions/) and can change sign only at its zeros, its sign remains constant within each interval. These values are then marked on a number line, with $+$ and $-$ indicating the sign on each interval.

|  |  | $$- 2$$ | $$1$$ |
| --- | --- | --- | --- |
| $x - 1 > 0$ | $-$ | $-$ | $+$ |
| $x + 2 > 0$ | $-$ | $+$ | $+$ |
| $\left(\right. x - 1 \left.\right) \left(\right. x + 2 \left.\right) > 0$ | $+$ | $-$ | $+$ |

---

In the last row, we insert the result of the product of the signs between the sign from row 1 and that from row 2, for each interval. The intervals that satisfy our initial inequality $\left(\right. x - 1 \left.\right) \left(\right. x + 2 \left.\right) > 0$ are:

$$x < - 2 \text{and} x > 1$$

In interval notation, the solution set is:

$\left(\right. - \infty , - 2 \left.\right) \cup \left(\right. 1 , + \infty \left.\right)$

###### If the inequality is non-strict, the zeros of the expression belong to the solution. For the inequality: $x^{2} + x - 2 \geq 0$ the procedure is identical, but since the inequality is satisfied also when $f \left(\right. x \left.\right) = 0$, the zeros $x = - 2$ and $x = 1$ are included in the solution set $\left(\right. - \infty , - 2 \left]\right. \cup \left[\right. 1 , + \infty \left.\right)$.

## Systematic procedure for sign analysis

In general, sign analysis of inequalities follows a systematic procedure that applies consistently to any polynomial or rational expression.

- Rewrite the inequality in the form $f \left(\right. x \left.\right) > 0$ (or $< 0$, $\geq 0$, $\leq 0$), with zero on the right-hand side.
- Factor $f \left(\right. x \left.\right)$ into a product or quotient of linear or irreducible factors. For rational inequalities, analyse the numerator and denominator independently.
- Find the zeros of each factor. Zeros of the denominator never belong to the solution and must be marked on the number line with an open circle.
- Arrange the zeros in ascending order along the real line, thereby partitioning $\mathbb{R}$ into disjoint intervals. For each interval, determine the sign of each factor.
- Combine the signs for each interval using the product rule: the overall sign is positive if the number of negative factors is even and negative if it is odd. Factors with even multiplicity do not produce a sign change at their corresponding zero.
- Identify the intervals where the overall sign fulfils the original inequality. For strict inequalities, exclude zeros from the solution; for non-strict inequalities, include them. Always exclude zeros of the denominator.
- Present the solution using set notation, combining disjoint intervals with $\cup$.

## Geometric representation

Plotting the curve on the axes, we obtain:

![](https://algebrica.org/wp-content/uploads/resources/images/sign-analysis-1.png)

In this way, we have solved the inequality using the sign table without resorting to solving the associated quadratic equation using the [quadratic formula](https://algebrica.org/quadratic-formula), which would have led to the same result.

In fact, when the inequality is of the form $a x^{2} + b x + c \geq 0$ or $a x^{2} + b x + c > 0$, and the corresponding [quadratic equation](https://algebrica.org/quadratic-equations/) $a x^{2} + b x + c = 0$ has two distinct real solutions $x_{1} < x_{2}$, we have:

$$& x \leq x_{1} \lor x \geq x_{2} & & \text{for} a x^{2} + b x + c \geq 0 \\ & x < x_{1} \lor x > x_{2} & & \text{for} a x^{2} + b x + c > 0$$

If a function $f \left(\right. x \left.\right)$ is [continuous](https://algebrica.org/continuous-functions/) on an interval $\left[\right. a , b \left]\right.$ and $f \left(\right. a \left.\right)$ and $f \left(\right. b \left.\right)$ have opposite signs, then by the Intermediate Value Theorem there exists at least one point $c \in \left(\right. a , b \left.\right)$ such that $f \left(\right. c \left.\right) = 0.$

##### In other words, for a [continuous function](https://algebrica.org/continuous-functions/), a change of sign occurs only by crossing a zero of the function, which is a point where $f \left(\right. x \left.\right) = 0$. In the example shown above, the change of sign occurs precisely near the solutions of the equation associated with the inequality, namely $- 2$ and $1$.

## Example 2

The same approach discussed above can be applied to solving rational inequalities of the type:

$$\frac{N \left(\right. x \left.\right)}{D \left(\right. x \left.\right)}$$

To [analyse the sign](https://algebrica.org/sign-analysis-in-inequalities/) of an inequality of this type, we need to separately study the sign of the numerator and the sign of the denominator. Then, we verify the intervals where the signs are concordant (both positive or both negative) or discordant (one positive, the other negative).

---

Let’s consider the following rational inequality:

$$\frac{2 x - 3}{1 - x} > 0$$

Let’s analyse the numerator and the denominator separately by setting: $N \left(\right. x \left.\right) > 0$ and $D \left(\right. x \left.\right) > 0$. We obtain:

$$& 2 x - 3 > 0 \rightarrow x > \frac{3}{2} \\ & 1 - x > 0 \rightarrow x < 1$$

By representing the signs on the number line, we have:

|  |  | $$1$$ | $$\frac{3}{2}$$ |
| --- | --- | --- | --- |
| $N \left(\right. x \left.\right) > 0$ | $+$ | $-$ | $-$ |
| $D \left(\right. x \left.\right) > 0$ | $-$ | $-$ | $+$ |
| $\frac{N \left(\right. x \left.\right)}{D \left(\right. x \left.\right)} > 0$ | $-$ | $+$ | $-$ |

The interval of positivity that satisfies our initial inequality is therefore:

$x \in \left(\right. 1 , \frac{3}{2} \left.\right)$

## Example 3

Consider the following inequality, which involves a factor with even multiplicity:

$$\left(\right. x - 1 \left.\right)^{2} \left(\right. x + 3 \left.\right) > 0$$

The zeros are $x = 1$ (with multiplicity $2$) and $x = - 3$ (with multiplicity $1$). They partition the real line into three intervals:

|  |  | $$- 3$$ | $$1$$ |
| --- | --- | --- | --- |
| $\left(\right. x - 1 \left.\right)^{2} > 0$ | $+$ | $+$ | $+$ |
| $x + 3 > 0$ | $-$ | $+$ | $+$ |
| $\left(\right. x - 1 \left.\right)^{2} \left(\right. x + 3 \left.\right) > 0$ | $-$ | $+$ | $+$ |

---

Notice that $\left(\right. x - 1 \left.\right)^{2}$ is always non-negative and equals zero only at $x = 1$. As a result, the sign of the product is determined entirely by the factor $\left(\right. x + 3 \left.\right)$, and no sign change occurs at $x = 1.$ The overall sign transitions from $-$ to $+$ only at $x = - 3$, where the factor $\left(\right. x + 3 \left.\right)$ changes sign.

The solution to the inequality is therefore:

$$x \in \left(\right. - 3 , 1 \left.\right) \cup \left(\right. 1 , + \infty \left.\right)$$

###### The point $x = 1$ is excluded because the inequality is strict and $f \left(\right. 1 \left.\right) = 0$, even though no sign change occurs there.

## Selected references

- **City University of New York, N. Apostolakis**. [Handout About the Table of Signs Method](https://fsw01.bcc.cuny.edu/nikolaos.apostolakis/teaching/sp08/Math30/30sp08table-of-signs-hand.pdf)
- **Florida State University, P. Kirby**. [Solving Polynomial and Rational Inequalities](https://www.math.fsu.edu/~pkirby/mac1140/5_4Inequalities.pdf)
- **University of North Carolina Charlotte, H. Breiter**. [Sign Charts and the Test Interval Technique](https://webpages.charlotte.edu/~hbreiter/m1120/testinterval.pdf)
