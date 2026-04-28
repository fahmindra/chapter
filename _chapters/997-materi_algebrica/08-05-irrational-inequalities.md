---
layout: chapter
title: "Irrational Inequalities"
chapter: "Inequalities"
chapter_order: 8
section_order: 5
permalink: /materi-algebrica/inequalities/irrational-inequalities/
---

extraneous solutionsintersection solutionsmultiple radicalstwo radicalsnested radicalsparameter casessquare root inequalitiessolution checksquaring stepodd index caseeven index casesign analysisdomain determinationadmissible valuesdomain restrictionsfractional exponentsradicalsirrational inequalitycasesmethodsfoundation

## Definition

An irrational inequality is an inequality in which the unknown appears under a [radical](https://algebrica.org/radicals/) sign or is raised to a fractional [exponent](https://algebrica.org/powers/). More precisely, it is an inequality of the form $F \left(\right. x \left.\right) \geq 0$ or $F \left(\right. x \left.\right) > 0$ in which at least one term contains an expression of the type $\sqrt[n]{f \left(\right. x \left.\right)}$ or equivalently $f \left(\right. x \left.\right)^{p / q}$ with $q > 1$. As with [irrational equations](https://algebrica.org/irrational-equations/), the presence of radicals imposes constraints on the [domain](https://algebrica.org/determining-the-domain-of-a-function/), and these constraints interact non-trivially with the direction of the inequality.

The central difficulty that distinguishes irrational inequalities from their equation counterparts is that raising both sides to a power is a monotone operation only under specific sign conditions:

- When both sides are non-negative, the inequality is preserved under even-power exponentiation.
- When the sign of one side is indeterminate, the direction of the inequality may be reversed or the operation may not be justified at all.

###### In practice, solving irrational inequalities requires careful control of admissible values, since algebraic transformations may introduce extraneous solutions that must be checked against the original inequality.

## Even-index radicals versus odd-index radicals

The behaviour of an irrational inequality depends fundamentally on whether the index $n$ of the radical is even or odd, and this distinction shapes the entire solution strategy. When the index is odd, the function $\sqrt[n]{x}$ is defined and strictly increasing on the whole real line, provided one adopts the real-valued convention which uses the [sign function](https://algebrica.org/sign-function/):

$$\sqrt[n]{x} = \text{sign} \left(\right. x \left.\right) \cdot \left|\right. x \left|\right.^{1 / n}$$

which extends the odd root to negative arguments. Under this convention, $\sqrt[3]{- 8} = - 2$ and more generally the odd-index radical is the inverse of the odd-power function $t \rightarrowtail t^{n}$. As a consequence we have:

$$\sqrt[n]{f \left(\right. x \left.\right)} \leq \sqrt[n]{g \left(\right. x \left.\right)} \Longleftrightarrow f \left(\right. x \left.\right) \leq g \left(\right. x \left.\right)$$

without any additional domain conditions, since the function is monotone on all of $\mathbb{R}$. The odd-index case is therefore the simpler one, and it mirrors the treatment of odd-index irrational equations.

---

When the index is even, the situation is more delicate. The function $\sqrt[n]{x}$ is defined only for non-negative arguments, and its range is restricted to non-negative values. This means that any inequality of the form $\sqrt[n]{f \left(\right. x \left.\right)} \leq g \left(\right. x \left.\right)$ with $n$ even carries implicit constraints.

![](https://algebrica.org/wp-content/uploads/resources/images/irr-ineq-1.png)

The radicand must be non-negative, and, depending on the sign of $g \left(\right. x \left.\right)$, the inequality may be satisfied trivially or may need to be squared. The even-index case therefore splits naturally into sub-cases depending on the sign of the right-hand side.

## General forms and solution strategies

The most frequently encountered irrational inequalities involving a square root are outlined below. Each type necessitates a specific method of solution. For the inequality of the form:

$$\sqrt{f \left(\right. x \left.\right)} \leq g \left(\right. x \left.\right)$$

the solution proceeds as follows. If $g \left(\right. x \left.\right) < 0$, the inequality has no solution at that point, since a square root is always non-negative. If $g \left(\right. x \left.\right) \geq 0$, the inequality is equivalent to squaring both sides, which is admissible because both sides are non-negative. The full condition is therefore the following system.

$$\left{\right. f \left(\right. x \left.\right) \geq 0 \\ g \left(\right. x \left.\right) \geq 0 \\ f \left(\right. x \left.\right) \leq \left(\right. g \left(\right. x \left.\right) \left.\right)^{2}$$

---

For the following case one must distinguish two sub-cases:

$$\sqrt{f \left(\right. x \left.\right)} \geq g \left(\right. x \left.\right)$$

- When $g \left(\right. x \left.\right) < 0$, the inequality is automatically satisfied for every $x$ in the domain of $\sqrt{f \left(\right. x \left.\right)}$, since the left-hand side is non-negative and therefore always greater than a negative quantity.
- When $g \left(\right. x \left.\right) \geq 0$, both sides are non-negative and one may square, obtaining the following system.

$$\left{\right. f \left(\right. x \left.\right) \geq 0 \\ g \left(\right. x \left.\right) \geq 0 \\ f \left(\right. x \left.\right) \geq \left(\right. g \left(\right. x \left.\right) \left.\right)^{2}$$

The complete solution is then the union of the two sub-cases.

---

For the inequality of the form:

$$\sqrt{f \left(\right. x \left.\right)} \leq \sqrt{g \left(\right. x \left.\right)}$$

since both sides are non-negative wherever they are defined, squaring is always admissible when both radicands are non-negative, and the system reduces to the following.

$$\left{\right. f \left(\right. x \left.\right) \geq 0 \\ g \left(\right. x \left.\right) \geq 0 \\ f \left(\right. x \left.\right) \leq g \left(\right. x \left.\right)$$

Solving an irrational inequality follows the same foundational principle as solving an irrational equation: one eliminates the radical by raising both sides to the appropriate power, and then analyses the resulting algebraic inequality together with the domain conditions imposed by the radical. The key difference is that the direction of the inequality must be monitored carefully at each step, since squaring is a monotone operation only on the non-negative reals.

## Typical solution steps

Regardless of the specific form of the inequality, the solution process follows a consistent sequence of steps.

- Determine the domain imposed by the radicals.
- Analyse the sign of the non-radical side.
- Square only when both sides are non-negative.
- Solve the resulting algebraic inequality.
- Intersect with the domain conditions.

###### Each step depends on the previous one: skipping the domain analysis or ignoring the sign of the right-hand side are the two most common sources of error in solving irrational inequalities.

## Example 1

Consider the following inequality:

$$\sqrt{2 x - 1} \leq x - 2$$

The left-hand side is defined only when the radicand is non-negative, so the first condition to impose is $2 x - 1 \geq 0$, that is $x \geq \frac{1}{2}$. Since the square root is always non-negative, the right-hand side must also be non-negative for the inequality to be satisfiable: one requires $x - 2 \geq 0$, that is $x \geq 2$.

Under these two conditions both sides are non-negative, and squaring both sides is a valid operation that preserves the direction of the inequality. The problem reduces to the following system.

$$\left{\right. x \geq \frac{1}{2} \\ x \geq 2 \\ 2 x - 1 \leq \left(\right. x - 2 \left.\right)^{2}$$

Expanding the right-hand side of the third inequality gives $\left(\right. x - 2 \left.\right)^{2} = x^{2} - 4 x + 4$, so the inequality becomes $2 x - 1 \leq x^{2} - 4 x + 4$, that is $x^{2} - 6 x + 5 \geq 0$. The [roots](https://algebrica.org/roots-of-a-polynomial/) of the associated [quadratic equation](https://algebrica.org/quadratic-equations/) $x^{2} - 6 x + 5 = 0$ are $x = 1$ and $x = 5$, so the quadratic is non-negative outside the interval $\left[\right. 1 , 5 \left]\right.$, giving $x \leq 1$ or $x \geq 5$.

Intersecting all three conditions: the first two require $x \geq 2$, and the third requires $x \leq 1$ or $x \geq 5$. Within the region $x \geq 2$, only the part $x \geq 5$ survives. Representing the conditions on the real line gives the following picture.

|  | $$\frac{1}{2}$$ | $$1$$ | $$2$$ | $$5$$ |  |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

The highlighted row represents the intersection of the conditions: the solution is the set of values of $x$ for which both inequalities are simultaneously satisfied.

The solution is therefore the interval $\left[\right. 5 , + \infty \left.\right)$.

## Example 2

Consider the following inequality:

$$\sqrt{x^{2} - 3 x} \geq x - 1$$

The [domain](https://algebrica.org/determining-the-domain-of-a-function/) requires $x^{2} - 3 x \geq 0$, that is $x \left(\right. x - 3 \left.\right) \geq 0$, which holds for $x \leq 0$ or $x \geq 3$. One now distinguishes two sub-cases according to the sign of the right-hand side.

The first case is $x - 1 < 0$, that is $x < 1$. In this region the right-hand side is negative and the left-hand side is non-negative, so the inequality is automatically satisfied. The contribution of this sub-case is the intersection of $x < 1$ with the domain $x \leq 0$ or $x \geq 3$, which gives $x \leq 0$.

The second case is $x - 1 \geq 0$, that is $x \geq 1$. Both sides are non-negative and squaring is admissible. The inequality becomes $x^{2} - 3 x \geq \left(\right. x - 1 \left.\right)^{2} = x^{2} - 2 x + 1$, that is $- 3 x \geq - 2 x + 1$, hence $- x \geq 1$, giving $x \leq - 1$. This must be intersected with $x \geq 1$ and with the domain: the intersection is empty.

Collecting the two sub-cases, the complete solution is $\left(\right. - \infty , 0 \left]\right.$. Representing the conditions on the real line gives the following picture.

|  | $$0$$ | $$1$$ | $$3$$ |  |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

The highlighted row represents the intersection of the conditions: the solution is the set of values of $x$ for which both inequalities are simultaneously satisfied.

The solution is therefore the interval $\left(\right. - \infty , 0 \left]\right.$.

## Example 3

Consider the following inequality:

$$\sqrt{x^{2} - x - 6} \leq \sqrt{2 x + 2}$$

Since both sides involve square roots, both radicands must be non-negative. The domain conditions are $x^{2} - x - 6 \geq 0$ and $2 x + 2 \geq 0$. The first factors as $\left(\right. x - 3 \left.\right) \left(\right. x + 2 \left.\right) \geq 0$, giving $x \leq - 2$ or $x \geq 3$. The second gives $x \geq - 1$. The intersection of these two conditions is $x \geq 3$.

Since both sides are non-negative on the domain, squaring is admissible and the inequality is equivalent to $x^{2} - x - 6 \leq 2 x + 2$, that is $x^{2} - 3 x - 8 \leq 0$. The roots of $x^{2} - 3 x - 8 = 0$ are as follows.

$$x = \frac{3 \pm \sqrt{9 + 32}}{2} = \frac{3 \pm \sqrt{41}}{2}$$

Since $\sqrt{41} \approx 6.40$, the roots are approximately $x \approx - 1.70$ and $x \approx 4.70$. The quadratic is non-positive between the roots, so the inequality holds for:

$$\frac{3 - \sqrt{41}}{2} \leq x \leq \frac{3 + \sqrt{41}}{2}$$

Representing the conditions on the real line gives the following picture.

|  | $$- 2$$ | $$\frac{3 - \sqrt{41}}{2}$$ | $$- 1$$ | $$3$$ | $$\frac{3 + \sqrt{41}}{2}$$ |  |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |

The highlighted row represents the intersection of the conditions: the solution is the set of values of $x$ for which both inequalities are simultaneously satisfied.

The solution is therefore the closed interval:

$$\left[\right. 3 , \frac{3 + \sqrt{41}}{2} \left]\right.$$

## Example 4

We now consider a more general situation in which the right-hand side contains a [real parameter](https://algebrica.org/equations-with-parameters/) $k$. The structure of the solution set depends on the value of $k$, and a complete discussion requires a case analysis. Consider the following inequality.

$$\sqrt{x + 4} \leq k$$

The domain requires $x + 4 \geq 0$, that is $x \geq - 4$. The behaviour of the solution then depends on the sign of $k$.

If $k < 0$, the right-hand side is negative while the left-hand side is always non-negative, so the inequality is never satisfied. There is no solution.

If $k = 0$, the inequality reduces to $\sqrt{x + 4} \leq 0$. Since the square root is always non-negative, the only possibility is $\sqrt{x + 4} = 0$, that is $x = - 4$. The solution is the single point $- 4$.

If $k > 0$, both sides are non-negative and squaring is admissible. The inequality becomes $x + 4 \leq k^{2}$, that is $x \leq k^{2} - 4$. Intersecting with the domain $x \geq - 4$, the solution is the following closed interval.

$$- 4 \leq x \leq k^{2} - 4$$

This interval is non-empty whenever $k^{2} - 4 \geq - 4$, that is whenever $k^{2} \geq 0$, which is always true. Representing the solution on the real line for the case $k > 0$ gives the following picture.

|  | $$- 4$$ | $$k^{2} - 4$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Note that as $k \rightarrow 0^{+}$ the right endpoint $k^{2} - 4$ approaches $- 4$ from the right, and the interval shrinks to the single point $- 4$, consistently with the case $k = 0$.

The solution is therefore the closed interval:

$$\left[\right. - 4 , k^{2} - 4 \left]\right.$$

## Nested radicals

A further level of complexity arises when radicals are nested, as in inequalities of the form:

$$\sqrt{a + \sqrt{f \left(\right. x \left.\right)}} \leq g \left(\right. x \left.\right)$$

In such cases the procedure described above must be applied iteratively: one first isolates the outer radical and squares, then addresses the inner radical by repeating the same analysis. At each step the domain conditions accumulate, and the intersection of all of them must be carried through to the final solution. The same monotonicity considerations apply at every level of nesting.
