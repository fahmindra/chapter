---
layout: chapter
title: "Logarithmic Inequalities"
chapter: "Inequalities"
chapter_order: 8
section_order: 7
permalink: /materi-algebrica/inequalities/logarithmic-inequalities/
---

## Introduction

Logarithmic inequalities are inequalities that involve one or more [logarithmic](https://algebrica.org/logarithms) expressions, in which the unknown $x$ appears either in the argument of the logarithm or, in some cases, in the base itself. Before tackling logarithmic inequalities, it is essential to have a solid understanding of logarithms, their fundamental properties, and the standard methods used to solve [logarithmic equations](https://algebrica.org/logarithmic-inequalities/), as these tools are crucial for approaching and resolving such inequalities correctly.

---

Logarithmic inequalities may have the general form:

$$log_{a} ⁡ f \left(\right. x \left.\right) \underset{<}{\geq} log_{a} ⁡ g \left(\right. x \left.\right)$$

- $a$ is the base of the logarithm, with (a > 0) and $a \neq 1.$
- $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are algebraic expressions depending on the variable $x .$
- The symbol $\underset{<}{\geq}$ denotes one of the relations $\leq$, $=$, or $\geq .$

Moreover, for the inequality to be well defined, the following conditions must be satisfied:

$$\left{\right. f \left(\right. x \left.\right) > 0 \\ g \left(\right. x \left.\right) > 0$$

---

An inequality that contains a logarithmic expression in which the unknown variable does not appear in either the argument or the base of the logarithm is not a logarithmic inequality. In other words, an inequality such as:
$$log_{3} ⁡ \left(\right. 9 \left.\right) - 3 x > 0$$
is not a logarithmic inequality, since the logarithmic term is a constant. By contrast,
 $$log_{3} ⁡ \left(\right. 9 x \left.\right) - 3 x > 0$$
is a logarithmic inequality, because the variable $x$ appears inside the argument of the logarithm and directly affects its domain and behavior.

## How to solve logarithmic inequalities

The solution process for logarithmic inequalities is general, however, for explanatory convenience, let us consider the following inequality:
$$log_{a} ⁡ f \left(\right. x \left.\right) \geq log_{a} ⁡ g \left(\right. x \left.\right)$$

The procedure can be structured into four fundamental steps:

- Determine the [domain](https://algebrica.org/determining-the-domain-of-a-function/) of the inequality by imposing the admissibility conditions. The arguments of all logarithmic expressions must be strictly positive, and the base must satisfy:
  $$\left{\right. f \left(\right. x \left.\right) > 0 \\ g \left(\right. x \left.\right) > 0$$
- The base must satisfy:
  $$\left{\right. a > 0 \\ a \neq 1$$
- If $a > 1$, the logarithmic function is [increasing](https://algebrica.org/increasing-and-decreasing-functions/) and the inequality preserves its direction when the logarithms are removed.
- If $0 < a < 1$, the logarithmic function is decreasing and the direction of the inequality must be reversed when eliminating the logarithms.
- Use the monotonicity of the logarithmic function to remove the logarithms and reduce the problem to an equivalent algebraic inequality involving $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$.
- Solve the resulting algebraic inequality and intersect the solution set with the domain previously determined, discarding any values that do not satisfy the original logarithmic conditions.

---

To explain the role played by the base of the logarithm, let us recall the behavior of the [logarithmic function](https://algebrica.org/logarithmic-function/) when $0 < a < 1$. From its graph, we observe that the function is strictly decreasing over its entire domain, with a vertical asymptote along the $y$-axis:

![Graph of the logarithmic function with base between zero and one.](https://algebrica.org/wp-content/uploads/resources/images/logharithm-5-1.png "Graph of the logarithmic function with base between zero and one.")

##### The dashed curve represents the logarithmic function with base $a > 1$. In this case, the function is strictly increasing. In both cases, when $x = 1$, the value of the logarithmic function is $0$, and the graphs intersect at the point $\left(\right. 1 , 0 \left.\right)$.

## Example 1

Consider the logarithmic inequality:
$$log_{\frac{1}{2}} ⁡ \left(\right. x + 3 \left.\right) \geq log_{\frac{1}{2}} ⁡ \left(\right. 2 x - 1 \left.\right)$$

We begin by determining the domain of the inequality. The arguments of the logarithms must be strictly positive:
$$\left{\right. x + 3 > 0 \\ 2 x - 1 > 0$$

Using a graphical representation and considering the solution intervals of the [linear inequalities](https://algebrica.org/linear-inequalities/) in the previous system, we find that their intersection, which determines the domain of the logarithmic inequality, is precisely given by $x > 1 / 2$.

|  | $$- 3$$ | $$\frac{1}{2}$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Therefore, the domain $D$ of the original inequality is given by the following interval:
$$\left(\right. - \frac{1}{2} , + \infty \left.\right)$$

---

Next, we analyze the base of the logarithm. Since the base satisfies
$$0 < \frac{1}{2} < 1$$
the logarithmic function is strictly decreasing. As a consequence, when the logarithms are removed, the direction of the inequality must be reversed. Therefore, the given inequality:
$$log_{\frac{1}{2}} ⁡ \left(\right. x + 3 \left.\right) \geq log_{\frac{1}{2}} ⁡ \left(\right. 2 x - 1 \left.\right)$$
is equivalent to:
$$x + 3 \leq 2 x - 1$$

---

We now solve the resulting algebraic inequality:
$$x + 3 \leq 2 x - 1 \rightarrow x \geq 4$$

Finally, we intersect this result with the domain previously determined. Since the domain requires $x > \frac{1}{2}$, the condition $x \geq 4$ is admissible.

Hence, the solution set of the logarithmic inequality is:
$$x \geq 4$$

## Example 2

Consider the logarithmic inequality:

$$log_{\frac{1}{2}} ⁡ \left(\right. x + 1 \left.\right) > log_{2} ⁡ \left(\right. 2 - x \left.\right)$$

We begin by determining the [domain](https://algebrica.org/determining-the-domain-of-a-function/). The arguments of the logarithms must be strictly positive, hence:

$$\left{\right. x + 1 > 0 \\ 2 - x > 0$$

Using a graphical representation and considering the solution intervals of the linear inequalities in the previous system, we find that their intersection is given by $- 1 < x < 2$.

|  | $$- 1$$ | $$2$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Therefore, the domain $D$ of the original inequality is given by the following interval:
$$\left(\right. - 1 , 2 \left.\right)$$

---

Next, we rewrite the logarithm with base $\frac{1}{2}$ in terms of base $2$. Since $\frac{1}{2} = 2^{- 1}$, we have
$$log_{\frac{1}{2}} ⁡ \left(\right. x + 1 \left.\right) = \frac{log_{2} ⁡ \left(\right. x + 1 \left.\right)}{log_{2} ⁡ \left(\right. \frac{1}{2} \left.\right)} = - log_{2} ⁡ \left(\right. x + 1 \left.\right)$$

Substituting into the original inequality, we obtain:

$$log_{2} ⁡ \left(\right. x + 1 \left.\right) < - log_{2} ⁡ \left(\right. 2 - x \left.\right)$$

Bringing all logarithmic terms to the same side and applying the properties of logarithms, we get:
$$log_{2} ⁡ \left(\right. x + 1 \left.\right) + log_{2} ⁡ \left(\right. 2 - x \left.\right) < 0$$

which, by the sum property of logarithms, stating that the [sum of two logarithms](https://algebrica.org/logarithms) equals the logarithm of their product, allows us to rewrite the expression as follows:

$$log_{2} ! \left(\right. \left(\right. x + 1 \left.\right) \left(\right. 2 - x \left.\right) \left.\right) < 0$$

Since the logarithmic function with base $2 > 1$ is strictly increasing, this inequality is equivalent to
$$0 < \left(\right. x + 1 \left.\right) \left(\right. 2 - x \left.\right) < 1$$

Within the domain $\left(\right. - 1 , 2 \left.\right)$, the product $\left(\right. x + 1 \left.\right) \left(\right. 2 - x \left.\right)$ is always positive, so it suffices to solve:

$$\left(\right. x + 1 \left.\right) \left(\right. 2 - x \left.\right) < 1$$

Expanding and simplifying, we obtain
$$x^{2} - x - 1 > 0$$

The associated [quadratic equation](https://algebrica.org/quadratic-equations) has roots:
$$x = \frac{1 \pm \sqrt{5}}{2}$$

The inequality is satisfied outside the interval determined by these roots. Intersecting this result with the domain $\left(\right. - 1 , 2 \left.\right)$, we finally obtain the solution set: $$- 1 < x < \frac{1 - \sqrt{5}}{2}$$
