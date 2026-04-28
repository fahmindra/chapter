---
layout: chapter
title: "Linear Inequalities"
chapter: "Inequalities"
chapter_order: 8
section_order: 1
permalink: /materi-algebrica/inequalities/linear-inequalities/
---

## Introduction to inequalities

An inequality is a mathematical statement involving algebraic expressions for which we seek the values of the variables that make the inequality true. In general, an inequality between two algebraic expressions $A \left(\right. x \left.\right)$ and $B \left(\right. x \left.\right)$ is defined as the relation:

$$A \left(\right. x \left.\right) > B \left(\right. x \left.\right)$$

Solving an inequality involves determining the solution set, that is, all the values of $x$ that satisfy the previous inequality. The solutions of inequalities are subsets of $\mathbb{R}$ defined as intervals.

---

Given two real numbers $a$ and $b$ with $a < b$, a bounded interval is defined as the set of real numbers between $a$ and $b$, where $a$ and $b$ are the lower and upper bounds, respectively. An unbounded interval is the set of numbers that either precede $a$ or follow $a$. If the endpoints of a bounded interval are included, the interval is called closed, otherwise, it is called open.

![](https://algebrica.org/wp-content/uploads/resources/images/inequalities-1.png)

The inequality sign determines whether the solution interval is open or closed at its boundary. A strict inequality, expressed with $>$ or $<$, excludes the boundary value, yielding an open interval. A non-strict inequality, expressed with $\geq$ or $\leq$, includes it, yielding a closed or half-open interval.

| Inequality | Interval |
| --- | --- |
| $x > a$ | $\left(\right. a , + \infty \left.\right)$ |
| $x \geq a$ | $\left[\right. a , + \infty \left.\right)$ |
| $x < a$ | $\left(\right. - \infty , a \left.\right)$ |
| $x \leq a$ | $\left(\right. - \infty , a \left]\right.$ |
| $a < x < b$ | $\left(\right. a , b \left.\right)$ |
| $a \leq x \leq b$ | $\left[\right. a , b \left]\right.$ |

###### The previous table summarizes the correspondence between the inequality sign and the resulting interval notation for a single-variable linear inequality.

---

The degree of an inequality corresponds to the degree of the [polynomial](https://algebrica.org/polynomials) $P \left(\right. x \left.\right)$ obtained by rewriting the inequality in the form $P \left(\right. x \left.\right) > 0$. A linear or first-degree inequality is defined in the general form:

$$a x > b$$

Every first-degree inequality with $a \neq 0$ always has an interval of values as its solution. The condition $a \neq 0$ is essential. When $a = 0$, the variable disappears entirely from the inequality, and the problem reduces to comparing two constants. Consider the general form with $a = 0$.

$$0 \cdot x > b$$

This simplifies to $0 > b$. If $b < 0$, the inequality holds regardless of the value of $x$, and the solution set is all of $\mathbb{R}$. If $b \geq 0$, the inequality is never satisfied, and the solution set is empty. In either case, there is no interval determined by a boundary point: the outcome is a global truth or a contradiction, not a proper first-degree inequality.

---

Given an inequality, an equivalent inequality can be obtained by adding the same number or expression to both sides, provided that the expression is well-defined within the same [domain](https://algebrica.org/determining-the-domain-of-a-function/). The inequality $5 x - 2 > x + 3$ is equivalent to the inequality $4 x - 2 > 3$, by subtracting $x$ from both sides.

An equivalent inequality can also be obtained by dividing or multiplying both sides by the same non-zero value. However, if the value is negative, the inequality sign must be reversed. It is always useful to rewrite a first-degree inequality like $- x + 5 < - 3$ in the form $x - 5 > 3$. Changing the signs requires reversing the direction of the inequality.

## Geometric interpretation

The solution set of a linear inequality always corresponds to a half-line on the real number line, that is, an unbounded interval extending indefinitely in one direction from a boundary point.

- When the inequality is strict, the boundary point is excluded and the half-line is open at that end.
- When the inequality is non-strict, the boundary point belongs to the solution set and the half-line is closed.

Consider, for instance, the simple inequality $x \geq 1$. Its solution set is the closed half-line $\left[\right. 1 , + \infty \left.\right)$, represented below.

|  | $$1$$ |  |
| --- | --- | --- |
|  |  |  |
|  |  |  |

This geometric reading clarifies why the solution of a first-degree inequality is never an isolated point or a bounded interval: the linear structure of the expression $a x - b$ ensures that its sign changes exactly once, at $x = b / a$, dividing the real line into precisely two regions, one of which constitutes the solution.

## Example 1

Consider the following inequality:

$$- \frac{x}{2} + 5 > 2 x - 5$$

The goal is to reduce it to the standard form $a x > b$. Since the left-hand side contains a fraction with denominator $2$, multiplying both sides by $2$ clears the denominator without altering the direction of the inequality, as the multiplier is positive.

$$- x + 10 > 4 x - 10$$

Collecting all terms involving $x$ on the left and moving the constant terms to the right yields the following.

$$- 5 x > - 20$$

Dividing both sides by $- 5$ isolates the variable. Since the divisor is negative, the direction of the inequality must be reversed.

$$x < 4$$

The solution set is the open interval $\left(\right. - \infty , 4 \left.\right)$.

## How to solve literal first-degree inequalities

In the case of literal first-degree inequalities, the coefficient of the variable is not a fixed constant but depends on one or more parameters. Consider the following inequality.

$$z \left(\right. x - 1 \left.\right) < 2 x + 1$$

The first step is to expand and collect terms so as to rewrite the expression in one of the standard forms $A x > B$, $A x < B$, $A x \geq B$, or $A x \leq B$. Expanding the left-hand side and moving all terms involving $x$ to the left yields the following.

$$& z x - z < 2 x + 1 \\ & z x - 2 x < z + 1 \\ & \left(\right. z - 2 \left.\right) x < z + 1$$

The inequality is now in the form $A x < B$ with $A = z - 2$ and $B = z + 1$. Since dividing both sides by $A$ requires knowing its sign, and the sign of $z - 2$ depends on the value of the parameter $z$, it is necessary to distinguish three separate cases.

---

When $z > 2$, the coefficient $z - 2$ is positive. Dividing both sides by a positive quantity preserves the direction of the inequality, giving the following.

$$x < \frac{z + 1}{z - 2}$$

---

When $z = 2$, the coefficient $z - 2$ vanishes. Substituting this value reduces the inequality to $0 \cdot x < 3$, which holds for every $x \in \mathbb{R}$. The solution set is all of $\mathbb{R}$.

---

When $z < 2$, the coefficient $z - 2$ is negative. Dividing both sides by a negative quantity reverses the direction of the inequality, giving the following.

$$x > \frac{z + 1}{z - 2}$$

## Absolute value inequalities

Absolute value inequalities are inequalities that follow the properties of [absolute value](https://algebrica.org/absolute-value) and are of the form:

$$\left|\right. x \left|\right. < z$$

In general, inequalities involving absolute values do not belong to the class of linear inequalities, since the presence of the absolute value function alters the behavior of the expression by introducing a discontinuity that breaks its linear structure. However, through an appropriate decomposition process, they can be transformed into one or more equivalent systems of linear inequalities, allowing them to be analyzed using the same methods applied to first-degree inequalities.

---

To solve them, we need to consider the sign of the absolute value by dividing it into two cases:

- $\left|\right. x \left|\right. < z$ if and only if $- z < x < z$.
- $\left|\right. x \left|\right. > z$ if and only if $x < - z \text{or} x > z$.

We must therefore solve a system of inequalities resulting from the possible cases considered in the analysis. The process is slightly more complicated than simple linear equations, and careful attention must be paid to the signs and the direction of the inequality during calculations.

## Example 2

Let’s try to solve the following absolute value inequality:

$$\left|\right. x - 1 \left|\right. < 2 x + 4$$

---

First, we study the sign of $\left|\right. x - 1 \left|\right.$. We have:

$$\left|\right. x - 1 \left|\right. = \left{\right. x - 1 & x \geq 1 \\ - x + 1 & x < 1$$

---

Substituting the first branch into the inequality and solving yields the following system.

$$\left{\right. x \geq 1 \\ x - 1 < 2 x + 4$$

|  | $$- 5$$ | $$1$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

The second inequality reduces to $x > - 5$. The solution of the system is the intersection of $x \geq 1$ and $x > - 5$, which is $x \geq 1$.

---

Substituting the second branch into the inequality and solving yields the following system:

$$\left{\right. x < 1 \\ - x + 1 < 2 x + 4$$

|  | $- 1$ | $1$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

The second inequality reduces to $x > - 1$. The solution of the system is the intersection of $x < 1$ and $x > - 1$, which is the open interval $\left(\right. - 1 , 1 \left.\right)$.

The complete solution is obtained by taking the union of the two partial solution sets. Since $x \geq 1$ and $\left(\right. - 1 , 1 \left.\right)$ are adjacent intervals that together cover all values greater than $- 1$, the solution to the inequality is the following.

$$x > - 1$$

## Selected references

- **Stony Brook University**. [Linear Inequalities](https://www.math.stonybrook.edu/Videos/MAP103Online/Handouts/Lecture-17-Handout.pdf)
- **Stony Brook University**. [Absolute Value Inequalities](https://www.math.stonybrook.edu/Videos/MAP103Online/Handouts/Lecture-18-Handout.pdf)
- **Harvard University**. [Appendix H: Interpreting and Working with Inequalities](https://abel.math.harvard.edu/archive/xb_spring_03/icearchive1/webAPPH.pdf)
- **University of Houston**. [Interval Notation and Linear Inequalities](https://online.math.uh.edu/Math1300-unpaid/ch1/s17/1300_Ch1_Section7.pdf)
