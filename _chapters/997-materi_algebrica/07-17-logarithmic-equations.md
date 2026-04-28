---
layout: chapter
title: "Logarithmic Equations"
chapter: "Equations"
chapter_order: 7
section_order: 17
permalink: /materi-algebrica/equations/logarithmic-equations/
---

## Introduction

Logarithmic equations are [equations](https://algebrica.org/equations) in which the unknown appears inside a [logarithm](https://algebrica.org/logarithms). To solve them, it is crucial to understand the properties of logarithms and how these can be applied to isolate and determine the value of the unknown. A logarithmic equation takes the form:

$$log_{a} ⁡ f \left(\right. x \left.\right) = g \left(\right. x \left.\right)$$

- $a$ is the base of the logarithm and and it must meet the condition $a > 0 , a \neq 1$
- $f \left(\right. x \left.\right)$, the argument of the logarithm must be greater than zero. This is because the [logarithmic function](https://algebrica.org/logarithmic-function/) is only defined for positive [numbers](https://algebrica.org/types-of-numbers).

##### Solving logarithmic equations relies on a solid understanding of logarithmic properties, such as the product, quotient, and power rules, which allow complex expressions to be simplified and the variable to be isolated more easily.

## How to solve logarithmic equations

The resolution process for logarithmic equations can be structured into four fundamental steps:

- Determine the [domain](https://algebrica.org/determining-the-domain-of-a-function/) of the equations by ensuring the arguments of all logarithmic expressions are greater than 0 and remembering that the base must be greater than 0 and different from 1. $$log_{a} ⁡ f \left(\right. x \left.\right) = \left{\right. a > 0 \\ a \neq 1 \\ f \left(\right. x \left.\right) > 0$$
- Apply [logarithmic properties](https://algebrica.org/logarithms), such as the product, quotient, and power rules, to combine and simplify the logarithmic terms. This step aims to reduce the initial equation to a simpler form that allows for isolating the variable.
- Once the equation is simplified, solve for the variable by eliminating the logarithms. This often involves exponentiating both sides of the equation to remove the logarithmic functions.
- Substitute the solutions back into the original equation to ensure that they satisfy the equation. Check that all solutions are within the domain of the original logarithmic functions.

##### As a final remark, note that the domain restrictions identified in the first step often lead naturally to additional conditions on the variable. A systematic treatment of these cases can be found in the dedicated section on [logarithmic inequalities](https://algebrica.org/logarithmic-inequalities/), which complements the solution of logarithmic equations.

## Simplified forms of logarithmic equations

Once a logarithmic equation is simplified to a form suitable for solving the variable, the following strategies may occur. The equation is reduced to the form: $$log_{a} ⁡ f \left(\right. x \left.\right) = log_{a} ⁡ g \left(\right. x \left.\right)$$ In this case, we can use the fact that when two logarithms with the same base are equal, their arguments must also be equal. Therefore, it is sufficient to set the two arguments equal and solve the resulting equation for the variable $x$: $$f \left(\right. x \left.\right) = g \left(\right. x \left.\right)$$

##### This equivalence is valid only when both logarithmic expressions are defined. Always check that $f \left(\right. x \left.\right) > 0$, $g \left(\right. x \left.\right) > 0$ and that the base satisfies $a > 0$ and $a \neq 1$ before equating the arguments.

---

The equation is reduced to the form: $$log_{a} ⁡ f \left(\right. x \left.\right) = b$$ In this case, since no further simplifications can be made, the solution requires using the definition of the logarithm and converting to the exponential form, resulting in: $$f \left(\right. x \left.\right) = a^{b}$$

---

The equation is reduced to the form $$log_{a}^{2} ⁡ \left(\right. x + c \left.\right) + log_{a} ⁡ \left(\right. x + c \left.\right) + k = 0$$ where logarithms raised to a certain power $n$ appear, with the same base and the same argument. In this case, we can use a substitution of the type $z = log_{a} ⁡ \left(\right. x + c \left.\right)$, obtaining: $z^{2} + z + k$. The equation is thus transformed into a [quadratic equation](https://algebrica.org/quadratic-equation) or an equation of degree $n$, which can be solved using the quadratic formula or [Ruffini’s rule](https://algebrica.org/ruffinis-rule) for [polynomials](https://algebrica.org/polynomials) of degree $n > 2$.

## Example 1

Let’s solve the logarithmic equation:

$$log_{3} ⁡ \left(\right. 2 x + 1 \left.\right) = log_{3} ⁡ \left(\right. x^{2} \left.\right)$$

---

The first step is to determine the domain of valid solutions, ensuring that the arguments of the logarithms are positive. Therefore, we set the conditions:

$$2 x + 1 > 0 \rightarrow x > - \frac{1}{2}$$
$$x^{2} > 0 \rightarrow x \neq 0$$

|  | $$- \frac{1}{2}$$ | $$0$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

Therefore, the domain $D$ is given by the following intervals:

$$\left(\right. - \frac{1}{2} , 0 \left.\right) \cup \left(\right. 0 , + \infty \left.\right)$$

---

Since the logarithms have the same base and are in the form $log_{a} ⁡ f \left(\right. x \left.\right) = log_{a} ⁡ g \left(\right. x \left.\right)$ we can equate the arguments directly. Rearranging the terms to one side to form a standard [quadratic equation](https://algebrica.org/quadratic-equations), we get:

$$x^{2} - 2 x - 1 = 0$$

We can solve this using the quadratic formula:

$$x = \frac{- b \pm \sqrt{b^{2} - 4 a c}}{2 a}$$

where $a = 1$, $b = - 2$, and $c = - 1$. Substituting these values, we get:

$$x & = \frac{- \left(\right. - 2 \left.\right) \pm \sqrt{\left(\right. - 2 \left.\right)^{2} - 4 \cdot 1 \cdot \left(\right. - 1 \left.\right)}}{2 \cdot 1} \\ & = \frac{2 \pm \sqrt{4 + 4}}{2} \\ & = \frac{2 \pm \sqrt{8}}{2} \\ & = \frac{2 \pm 2 \sqrt{2}}{2} \\ & = 1 \pm \sqrt{2}$$

---

Now let’s verify that the solutions satisfy the domain:

- $x = 1 + \sqrt{2} \approx 2.414$ satisfies $x > - \frac{1}{2} \lor x \neq 0$
- $x = 1 - \sqrt{2} \approx - 0.414$ satisfies $x > - \frac{1}{2} \lor x \neq 0$

The solution to the equation is:

$$x = 1 \pm \sqrt{2}$$
