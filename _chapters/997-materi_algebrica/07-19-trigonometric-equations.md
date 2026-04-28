---
layout: chapter
title: "Trigonometric Equations: Part 1"
chapter: "Equations"
chapter_order: 7
section_order: 19
permalink: /materi-algebrica/equations/trigonometric-equations-part-1/
---

Trigonometric equations are [equations](https://algebrica.org/equations) in which the unknown appears as the argument of trigonometric functions. There are various types of such equations, each with its corresponding solution method, as outlined below. In this first part, we will explore how to solve simple trigonometric equations of the form:

$$sin ⁡ \left(\right. x \left.\right) = m , cos ⁡ \left(\right. x \left.\right) = m , tan ⁡ \left(\right. x \left.\right) = m , \ldots$$

as well as equations of the type:

$$sin ⁡ \left[\right. f \left(\right. x \left.\right) \left]\right. , cos ⁡ \left[\right. f \left(\right. x \left.\right) \left]\right. , tan ⁡ \left[\right. f \left(\right. x \left.\right) \left]\right. , \ldots$$

and so on.

---

## Simple Trigonometric Equations

Let’s start with the simplest cases. Consider, for example, equations involving a single trigonometric function of the form:

$$(\text{1}) sin ⁡ \left(\right. x \left.\right) = m$$

To solve this equation, we need to determine all angles $x$ whose [sine](https://algebrica.org/sine-and-cosine) equals $m$. Since the sine function is defined in the range $- 1 \leq m \leq 1$, this constraint must be satisfied; otherwise, the equation has no real solutions and is considered impossible. On the [unit circle](https://algebrica.org/unit-circle), we can visualize this equation by drawing a horizontal line at $y = m$ which intersects the circle at two points in the first and second quadrants, provided that $- 1 \leq m \leq 1$.

![](https://algebrica.org/wp-content/uploads/resources/images/trigonometric-equations-1.png)

These intersection points correspond to two angles:

$$x = \alpha \text{and} x = \pi - \alpha$$

where $\alpha$ is the reference angle satisfying $sin ⁡ \left(\right. \alpha \left.\right) = m$ in the principal range $\left[\right. 0 , \pi \left]\right.$. Since the sine function is periodic with period $2 \pi$, the general solution can be written as:

$$x = \alpha + 2 k \pi , x = \pi - \alpha + 2 k \pi , k \in \mathbb{Z}$$

where $k$ is any [integer](https://algebrica.org/integers/), accounting for the periodic nature of the [sine function](https://algebrica.org/sine-function).

---

For example, we want to solve the equation $cos ⁡ x = 1 / 2$ within the interval $\left[\right. 0 , 2 \pi \left]\right.$. Let’s plot a line at the value $1 / 2$ on the graph of the [cosine function](https://algebrica.org/cosine-function).

![](https://algebrica.org/wp-content/uploads/resources/images/trigonometric-equations-2.png)

From known [cosine](https://algebrica.org/sine-and-cosine) values, we recall that:

$$cos ⁡ \left(\right. \frac{\pi}{3} \left.\right) = \frac{1}{2}$$

Since cosine is positive in the first and fourth quadrants, the two solutions within the given interval are:

$$x_{1} = \frac{\pi}{3} , x_{2} = \frac{5 \pi}{3}$$

---

Let’s now try to solve the equation $tan ⁡ x = 2$. Let’s plot a line at the value $2$ on the graph of the [tangent function](https://algebrica.org/tangent-function).

![](https://algebrica.org/wp-content/uploads/resources/images/trigonometric-equations-3.png)

To determine the solutions, we first identify the principal angle $x$ such that:

$$tan ⁡ x = 2$$

Since the tangent function is periodic with period $\pi$ the general solution is:

$$x = arctan ⁡ \left(\right. 2 \left.\right) + k \pi , k \in \mathbb{Z}$$

where $k$ is any integer, representing all possible solutions.

When the tangent value isn’t one of the commonly used ones, we can apply the arctangent—the inverse of the tangent—to determine the principal angle. This approach allows us to compute the corresponding angle directly without relying on standard tangent values. The same principle applies to other inverse trigonometric functions, such as [arcsin](https://algebrica.org/arcsine-and-arccosine) e and [arccosine](https://algebrica.org/arcsine-and-arccosine), which enable us to find the respective angles for any given sine or cosine values.

---

## Trigonometric Equations Solvable by Substitution

Another example of trigonometric equations are those that are generally solved by substitution and are of the form:

$$(\text{2}) sin ⁡ \left[\right. f \left(\right. x \left.\right) \left]\right. = m$$

To solve such an equation, first ensure that $m$ is within the interval $\left[\right. - 1 , 1 \left]\right.$, which is the valid range for the sine function. Then, apply a substitution to $f \left(\right. x \left.\right)$ to simplify the equation and solve it more easily. For example, consider the equation

$$sin ⁡ \left(\right. 2 x \left.\right) = \frac{1}{2}$$

Since $1 / 2$ is within the valid range, we set $2 x$ equal to the angles whose sine is $1 / 2$. We know that if $sin ⁡ \left(\right. u \left.\right) = 1 / 2$, then:

$$u = \frac{\pi}{6} + 2 \pi k \text{or} u = \frac{5 \pi}{6} + 2 \pi k , k \in \mathbb{Z}$$

Substituting $u = 2 x$ into these expressions, we obtain:

$$2 x = \frac{\pi}{6} + 2 \pi k \text{or} 2 x = \frac{5 \pi}{6} + 2 \pi k$$

Dividing both equations by 2, the solutions for $x$ are:

$$x = \frac{\pi}{12} + \pi k \text{or} x = \frac{5 \pi}{12} + \pi k , k \in \mathbb{Z}$$

---

## Example

Solve the equation:

$$cos ⁡ \left(\right. 3 x + 2 \left.\right) = \frac{1}{\sqrt{2}}$$

---

We first recall that $cos ⁡ u = \frac{1}{\sqrt{2}}$ has solutions at

$$u = \frac{\pi}{4} + 2 k \pi \text{or} u = - \frac{\pi}{4} + 2 k \pi , k \in \mathbb{Z} .$$

Setting $3 x + 2$ equal to these solutions, we obtain the two equations:

$$3 x + 2 = \frac{\pi}{4} + 2 k \pi$$

$$3 x + 2 = - \frac{\pi}{4} + 2 k \pi$$

---

Subtracting $2$ from both sides:

$$3 x = \frac{\pi}{4} - 2 + 2 k \pi$$

$$3 x = - \frac{\pi}{4} - 2 + 2 k \pi$$

Dividing everything by 3, we find:

$$x = \frac{\pi}{12} - \frac{2}{3} + \frac{2 k \pi}{3}$$

$$x = - \frac{\pi}{12} - \frac{2}{3} + \frac{2 k \pi}{3} , k \in \mathbb{Z}$$

Thus, the general solutions can be written as:

$$x = \frac{\pi - 8}{12} + \frac{2 k \pi}{3}$$

$$x = \frac{- \pi - 8}{12} + \frac{2 k \pi}{3} , k \in \mathbb{Z}$$

These represent all possible values of $x$ that satisfy the given equation.
