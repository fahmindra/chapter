---
layout: chapter
title: "Absolute Value Equations"
chapter: "Equations"
chapter_order: 7
section_order: 15
permalink: /materi-algebrica/equations/absolute-value-equations/
---

## Introduction

Absolute value equations are a particular class of [equations](https://algebrica.org/equations) in which the variable $x$ appears within an [absolute value](https://algebrica.org/absolute-value) expression. The absolute value represents how far a [number](https://algebrica.org/types-of-numbers) is from zero on the number line, regardless of its sign. It transforms any real number into its non-negative counterpart according to the following rule:

$$\left|\right. x \left|\right. = \left{\right. + x & \text{if} x \geq 0 \forall x \in \mathbb{R} \\ - x & \text{if} x < 0 \forall x \in \mathbb{R}$$

When solving an equation that involves an absolute value, it is essential to consider both possible cases (positive and negative) since the sign of the expression inside the bars determines which definition must be applied. This process often leads to two separate linear equations that need to be examined individually.

## Properties

The [absolute value function](https://algebrica.org/absolute-value-function) $\left|\right. x \left|\right.$ obeys several essential algebraic properties that describe how it interacts with basic arithmetic operations and comparisons. Understanding these rules is fundamental when simplifying expressions or solving equations that include absolute values. The following list summarizes the key properties that characterize the behavior of absolute values in real numbers:

$$\left|\right. x \left|\right. = \left|\right. - x \left|\right. \forall x \in \mathbb{R}$$

---

$$\left|\right. x \cdot y \left|\right. = \left|\right. x \left|\right. \cdot \left|\right. y \left|\right. \forall x , y \in \mathbb{R}$$

---

$$\left|\right. x \left|\right. = \left|\right. y \left|\right. \Longleftrightarrow x = \pm y \forall x , y \in \mathbb{R}$$

---

$$\left|\right. x \left|\right. \leq \left|\right. y \left|\right. \Longleftrightarrow x^{2} \leq y^{2} \forall x , y \in \mathbb{R}$$

---

$$\left|\right. \frac{x}{y} \left|\right. = \frac{\left|\right. x \left|\right.}{\left|\right. y \left|\right.} \forall x , y \in \mathbb{R} , y \neq 0$$

---

$$\sqrt{x^{2}} = \left|\right. x \left|\right. \forall x \in \mathbb{R}$$

##### These properties are useful for manipulating expressions involving absolute values and for simplifying calculations when solving related equations.

## Solving absolute value equations

To solve equations involving absolute values, it is necessary to analyze the expression inside the bars and consider the possible signs it can assume. The general approach depends on the type of equation: whether the absolute value is equal to a constant or to another expression. In each case, the solution process involves separating the equation into distinct cases, reflecting the definition of the absolute value function.

Let’s consider the basic case:
$$\left|\right. A \left(\right. x \left.\right) \left|\right. = a$$

In general, if $a \geq 0$, the equation is equivalent to $A \left(\right. x \left.\right) = a$ or $A \left(\right. x \left.\right) = - a$. If $a < 0$, the equation has no solution. For example, the equation $\left|\right. 3 + 2 x \left|\right. = - 2$ has no solution because the absolute value of an expression can never be negative.

---

Let’s now consider the case:

$$\left|\right. A \left(\right. x \left.\right) \left|\right. = B \left(\right. x \left.\right)$$

and solving it requires taking into account the sign of the absolute value when performing the calculations.

## Example 1

Let’s solve the equation:
$$\left|\right. 2 x - 4 \left|\right. = x + 1$$

---

First, we analyze the sign of the expression inside the absolute value. We have $2 x - 4 \geq 0$, which leads to $x \geq 2$.

According to (1), the equation becomes:

$$\left|\right. 2 x - 4 \left|\right. = \left{\right. 2 x - 4 & \text{if} x \geq 2 \\ - 2 x + 4 & \text{if} x < 2$$

---

Let’s now solve the first system given by:

$$\left{\right. x \geq 2 \\ 2 x - 4 = x + 1$$

$$\left{\right. x \geq 2 \\ 2 x - x = + 1 + 4 \rightarrow x = 5$$

This solution is acceptable because it satisfies the condition $x \geq 2$.

##### What we have just seen is a [system of inequalities](https://algebrica.org/systems-of-inequalities) with one variable and two inequalities. Explore the related entry to learn more about the solving process and how to handle more complex cases.

---

Let’s now solve the second system given by:

$$\left{\right. x < 2 \\ - 2 x + 4 = x + 1$$

$$\left{\right. x < 2 \\ - 2 x - x = + 1 - 4 \rightarrow - 3 x = - 3 \rightarrow x = 1$$

This solution is acceptable because it satisfies the condition $x < 2$.

The solution to the equation is:

$$x = 1 x = 5$$

## Example 2

Let’s solve the equation:
$$\frac{\left|\right. 3 x \left|\right.}{\left|\right. x + 1 \left|\right.} = \left|\right. x \left|\right.$$

We are dealing with a rational equation for which it is necessary to determine the conditions of existence, which in this case correspond to the values of $x$ that make the denominator zero. The denominator becomes zero when $x = - 1$, so this value must be excluded from the set of solutions.

---

Using the properties of absolute value, we can rewrite the equation as:

$$3 \left|\right. \frac{x}{x + 1} \left|\right. = \left|\right. x \left|\right.$$

---

We must therefore analyze the signs of the expressions. Let’s start by considering the following case:

$$\frac{3 x}{x + 1} = x \rightarrow 3 x = x^{2} + x \rightarrow x^{2} - 2 x \rightarrow x \left(\right. x - 2 \left.\right)$$

We have obtained a straightforward [quadratic equation](https://algebrica.org/quadratic-equations) whose solutions are:

$$x = 0 x = 2$$

Both solutions are acceptable because they are different from $- 1$.

##### We solved the quadratic equation without using the [quadratic formula](https://algebrica.org/quadratic-formula), by [factoring](https://algebrica.org/factoring-quadratic-equations/) the corresponding [polynomial](https://algebrica.org/polynomials) and finding the values of $x$ that make each linear factor equal to zero.

---

Let’s now consider the case:

$$\frac{3 x}{x + 1} = - x \rightarrow 3 x = - x^{2} - x \rightarrow x^{2} + 4 x \rightarrow x \left(\right. x + 4 \left.\right)$$

Proceeding as above we have obtained a straightforward quadratic equation whose solutions are:

$$x = 0 x = - 4$$

Both solutions are acceptable because they are different from $- 1$.

The solution to the equation is:

$$x = - 4 x = 0 x = 2$$
