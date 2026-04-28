---
layout: chapter
title: "Factoring Quadratic Equations"
chapter: "Equations"
chapter_order: 7
section_order: 6
permalink: /materi-algebrica/equations/factoring-quadratic-equations/
---

## Introduction

A [quadratic equation](https://algebrica.org/quadratic-equations/) is a type of [polynomial](https://algebrica.org/polynomials/) expression that consists of one or more terms, where each term is a product of a constant coefficient, a variable raised to a [power](https://algebrica.org/powers), and a possible constant term. Factoring a polynomial involves expressing it as a multiplication of irreducible factors, usually of lower degree.

A quadratic equation in the form $a x^{2} + b x + c = 0$ can be factored into an equivalent equation if its [discriminant](https://algebrica.org/quadratic-formula/) is not negative:

$$a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right) = 0$$

where $x_{1}$ and $x_{2}$ are the roots of the equation.

## Demonstration

The proof of the expression above is straightforward. We include it here for completeness.

$$P \left(\right. x \left.\right) = a x^{2} + b x + c$$

---

We can factor out the coefficient $a$ and rewrite the expression:

$$P \left(\right. x \left.\right) = a \left(\right. x^{2} + \frac{b}{a} x + \frac{c}{a} \left.\right)$$

---

The expression becomes clearer due to the relationships between the solutions of a second-degree equation and its coefficients, in particular, from what are defined as [Viète’s relations](https://algebrica.org/quadratic-formula):

$$x_{1} \cdot x_{2} = \frac{c}{a}$$
$$x_{1} + x_{2} = - \frac{b}{a}$$

Replacing the values, we obtain:

$$P \left(\right. x \left.\right) & = a \left[\right. x^{2} - \left(\right. x_{1} + x_{2} \left.\right) x + x_{1} x_{2} \left]\right. \\ & = a \left(\right. x^{2} - x_{1} x - x_{2} x + x_{1} x_{2} \left.\right) \\ & = a \left[\right. x \left(\right. x - x_{1} \left.\right) - x_{2} \left(\right. x - x_{1} \left.\right) \left]\right. \\ & = a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$$

This demonstrates the expression $\left(\right. 1 \left.\right)$.

$$P \left(\right. x \left.\right) = a x^{2} + b x + c = a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$$

This method of factoring polynomials is known as the [AC method](https://algebrica.org/factoring-ac-method/). The solutions to the equation can be found by setting each factor equal to zero:

$$\left(\right. x - x_{1} \left.\right) = 0 \rightarrow x = x_{1}$$
$$\left(\right. x - x_{2} \left.\right) = 0 \rightarrow x = x_{2}$$

This method is effective for simple [polynomial equations](https://algebrica.org/polynomial-equations/). However, it becomes impractical for more complex equations. In these cases, it is better to use the [quadratic formula](https://algebrica.org/quadratic-formula/).

## Example

The polynomial $x^{2} - 4 x + 3$ can be factorized in the form $\left(\right. x - 1 \left.\right) \left(\right. x - 3 \left.\right)$. We have to find two numbers, $m , n$ whose product $P$ is $3$ $\left(\right. a \cdot c = 1 \cdot 3 \left.\right)$ and sum $S$ is $- 4$ $\left(\right. b \left.\right)$.

---

We can use this simple scheme to find the numbers that satisfy our constraints. $$& m & n & P & S \\ & 1 & 3 & 3 & 4 \\ & - 1 & - 3 & 3 & - 4$$

---

The second row satisfies our constraints, so the equation associated with the polynomial becomes:
$$x^{2} - 4 x + 3 = \left(\right. x - 1 \left.\right) \left(\right. x - 3 \left.\right) = 0$$

The solutions to the associated equation are:
$$x - 1 = 0 \rightarrow x = 1$$
$$x - 3 = 0 \rightarrow x = 3$$

The solution to the equation is:
$$x_{1} = 1 \text{and} x_{2} = 3$$
