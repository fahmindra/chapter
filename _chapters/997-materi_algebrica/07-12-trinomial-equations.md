---
layout: chapter
title: "Trinomial Equations"
chapter: "Equations"
chapter_order: 7
section_order: 12
permalink: /materi-algebrica/equations/trinomial-equations/
---

## What are trinomial equations

Trinomial equations are a specific type of [polynomial equation](https://algebrica.org/polynomial-equations/) that consist of three terms involving constants and [powers](https://algebrica.org/powers) of a variable.

$$a x^{2 n} + b x^{n} + c = 0$$

This form is especially useful because it allows for substitution strategies such as setting $x^{n} = y$ to transform the equation into a standard quadratic.

- $a$, $b$, and $c$ are numerical coefficients.
- $x$ is the unknown variable.

It is worth noting that if $n = 1$, the equation becomes a [quadratic equation](https://algebrica.org/quadratic-equations), often written in the form:

$$a x^{2} + b x + c = 0$$

## How to solve trinomial equations

A general set of steps can be followed to solve a trinomial equation of the form $a x^{2 n} + b x^{n} + c = 0$. The first step is to make a substitution that transforms the equation into a quadratic equation in $y$, which is easier to solve. For example, we let:

$$x^{n} = y$$

and obtain:

$$a y^{2} + b y + c = 0$$

We can use techniques such as [factoring](https://algebrica.org/factoring-quadratic-equations), [completing the square](https://algebrica.org/completing-the-square), or the [quadratic formula](https://algebrica.org/quadratic-formula) to solve the resulting quadratic equation in $y$. Once we find the solutions for $y$, we substitute them back using the original substitution $y = x^{n}$ to determine the corresponding values of $x$. In short:

- Let $y = x^{n}$, so the equation becomes $a y^{2} + b y + c = 0$.
- Solve the quadratic equation in $y$.
- For each solution $y_{i}$, solve $x^{n} = y_{i}$ to find the corresponding $x$-values.
- Check all solutions in the original equation to ensure they are valid.

##### It is important to verify each solution by substituting it into the original equation to ensure its validity. The process may seem complex, but it’s actually practical and straightforward to implement.

When solving equations through substitution, extra solutions, called extraneous solutions, can sometimes appear. These might satisfy the transformed equation but not the original one. By substituting each solution back into the original equation, we ensure that it truly works and doesn’t violate any implicit conditions.

## Example

Solve the equation $3 x^{4} - 7 x^{2} + 2 = 0$.

Let’s substitute $y = x^{2}$ to transform the equation into a quadratic equation:

$$3 y^{2} - 7 y + 2 = 0$$

---

We can use the [quadratic formula](https://algebrica.org/quadratic-formula) to find the value of $y$. We obtain:

$$y & = \frac{- \left(\right. - 7 \left.\right) \pm \sqrt{\left(\right. - 7 \left.\right)^{2} - 4 \cdot 3 \cdot 2}}{2 \cdot 3} \\ & = \frac{7 \pm \sqrt{49 - 24}}{6} \\ & = \frac{7 \pm \sqrt{25}}{6} \\ & = \frac{7 \pm 5}{6}$$

So, we found:

$$y_{1} = \frac{12}{6} = 2$$
$$y_{2} = \frac{2}{6} = \frac{1}{3}$$

---

Once the solution for $y$ are found, they can be substituted back into the original equation with $x^{2} = y$ to find the corresponding values of $x$.

For $y = 2$ we have:
$$x^{2} = 2 \rightarrow x = \pm \sqrt{2}$$

For $y = \frac{1}{3}$ we have
$$x^{2} = \frac{1}{3} \rightarrow \pm \sqrt{\frac{1}{3}}$$

---

It’s essential to verify that the solutions are correct by substituting them back into the original equation to ensure accuracy. To check if the given values are solutions to the equation $3 x^{4} - 7 x^{2} + 2 = 0$, we must plug them into the equation and verify if they satisfy it.

For $x = \sqrt{2}$:

$$3 \left(\right. \sqrt{2} \left.\right)^{4} - 7 \left(\right. \sqrt{2} \left.\right)^{2} + 2 = 3 \cdot 2^{2} - 7 \cdot 2 + 2$$
$$= 12 - 14 + 2 = 0$$

---

For $x = - \sqrt{2}$:
$$3 \left(\right. - \sqrt{2} \left.\right)^{4} - 7 \left(\right. - \sqrt{2} \left.\right)^{2} + 2 = 3 \cdot 2^{2} - 7 \cdot 2 + 2$$
$$= 12 - 14 + 2 = 0$$

---

For $x = \sqrt{\frac{1}{3}}$:
$$3 \left(\left(\right. \sqrt{\frac{1}{3}} \left.\right)\right)^{4} - 7 \left(\left(\right. \sqrt{\frac{1}{3}} \left.\right)\right)^{2} + 2 = 3 \cdot \left(\left(\right. \frac{1}{3} \left.\right)\right)^{2} - 7 \cdot \frac{1}{3} + 2$$
$$= \frac{3}{9} - \frac{7}{3} + 2 = 0$$

---

For $x = - \sqrt{\frac{1}{3}}$:
$$3 \left(\left(\right. - \sqrt{\frac{1}{3}} \left.\right)\right)^{4} - 7 \left(\left(\right. - \sqrt{\frac{1}{3}} \left.\right)\right)^{2} + 2 = 3 \cdot \left(\left(\right. \frac{1}{3} \left.\right)\right)^{2} - 7 \cdot \frac{1}{3} + 2$$
$$= \frac{3}{9} - \frac{7}{3} + 2 = 0$$

All solutions satisfy the original equation.

The solution to the equation is:
$$x = \pm \sqrt{2} \text{and} \pm \sqrt{\frac{1}{3}}$$
