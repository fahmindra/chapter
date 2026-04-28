---
layout: chapter
title: "Inverse Function"
chapter: "Functions"
chapter_order: 14
section_order: 7
permalink: /materi-algebrica/functions/inverse-function/
---

## What is an inverse function

In the introduction to [functions](https://algebrica.org/functions), we saw that a function $f : X \rightarrow Y$ is called bijective if it is both injective and surjective, that is, for every $y \in Y$, there exists a unique $x \in X$ such that $f \left(\right. x \left.\right) = y$.

- $X$ is the domain.
- $Y$ is the codomain.
- A function is called injective if for every $x_{1} , x_{2} \in X$, with $x_{1} \neq x_{2}$, we have $f \left(\right. x_{1} \left.\right) \neq f \left(\right. x_{2} \left.\right)$. In other words, for every $y \in Y$, there exists at most one $x \in X$ such that $f \left(\right. x \left.\right) = y$.
- A function is called surjective if for every $y \in Y$, there exists at least one $x \in X$ such that $f \left(\right. x \left.\right) = y$.

---

A function $f : X \rightarrow Y$ is bijective if and only if there exists a function $g : Y \rightarrow X$ such that:

- $\left(\right. g \circ f \left.\right) \left(\right. x \left.\right) = g \left(\right. f \left(\right. x \left.\right) \left.\right) = x$ for every $x \in X$
- $\left(\right. f \circ g \left.\right) \left(\right. y \left.\right) = f \left(\right. g \left(\right. y \left.\right) \left.\right) = y$ for every $y \in Y$

In this case, the function $g$ is unique and is called the **inverse function** of $f$, denoted by:
$$f^{- 1} = g$$

##### $\left(\right. g \circ f \left.\right) \left(\right. x \left.\right) = g \left(\right. f \left(\right. x \left.\right) \left.\right)$ is called the composite function, which means applying $f$ to $x$ first, and then applying $g$ to the result.

## Making a function invertible by restricting its domain

Consider the function $f \left(\right. x \left.\right) = x^{2}$, defined on $\mathbb{R}$. This is a quadratic function, represented by a [parabola](https://algebrica.org/parabola) with its vertex at the origin of the Cartesian plane. On its full [domain](https://algebrica.org/determining-the-domain-of-a-function/) $\mathbb{R}$, the function is not invertible, since it is not injective: distinct inputs can produce the same output, for example $f \left(\right. - 2 \left.\right) = f \left(\right. 2 \left.\right)$.

However, if we restrict the domain to $\left[\right. 0 , + \infty \left.\right)$, the function becomes bijective and therefore invertible. In this case, the inverse function is:

$$f \left(\right. x \left.\right) = x^{2} \rightarrow f^{- 1} \left(\right. x \left.\right) = \sqrt{x} \text{for} x \geq 0$$

![](https://algebrica.org/wp-content/uploads/resources/images/inverse-function-1.png)

The graph of a function and that of its inverse are symmetric with respect to the line $y = x$, which is the diagonal bisecting the first and third quadrants of the Cartesian plane.

If a function $f$ is [composed](https://algebrica.org/composite-functions/) with its inverse $f^{- 1}$, the result is the **identity function**, which maps each element of a set to itself:

$$f \left(\right. f^{- 1} \left(\right. x \left.\right) \left.\right) = f^{- 1} \left(\right. f \left(\right. x \left.\right) \left.\right) = x$$

## How to find the inverse of a general function

- Check whether the function is bijective, or determine a restriction of its domain that makes it bijective.
- Replace $f \left(\right. x \left.\right)$ with $y$, so that you work with the equation $y = f \left(\right. x \left.\right)$.
- Swap the variables $x$ and $y$: write $x = f \left(\right. y \left.\right)$. This reflects the idea of inverting input and output.
- Solve the equation for $y$, isolating it explicitly.
- Rewrite the result as $f^{- 1} \left(\right. x \left.\right) = \ldots$, using $x$ as the input variable for the inverse.

## Example

We want to find its inverse of the function $f \left(\right. x \left.\right) = \frac{2 x - 1}{x + 3}$.

##### The function $f$ is bijective on its domain $\mathbb{R} \backslash - 3$, because it is strictly increasing: its derivative is always positive. This ensures that $f$ is injective, and since the image of $f$ covers all real numbers except a single point, it is also surjective onto its codomain.

---

Write the function as an equation:
$$y = \frac{2 x - 1}{x + 3}$$

Swap $x$ and $y$
 $$x = \frac{2 y - 1}{y + 3}$$

---

Solve for $y$. Multiply both sides by $y + 3$:
 $$x \left(\right. y + 3 \left.\right) = 2 y - 1$$

Distribute the left-hand side:
 $$x y + 3 x = 2 y - 1$$

---

Bring all terms to one side and factor $y$ on the left-hand side:
 $$& x y - 2 y = - 1 - 3 x \\ & y \left(\right. x - 2 \left.\right) = - 1 - 3 x$$

Solve for $y$:
 $$y = \frac{- 1 - 3 x}{x - 2}$$

The inverse function is:
$$f^{- 1} \left(\right. x \left.\right) = \frac{- 1 - 3 x}{x - 2}$$

## Inverse function theorem

A useful result from basic analysis is the one–dimensional version of the inverse function theorem. The idea is quite intuitive: if a function behaves regularly on an interval, then it can be inverted without difficulty. More precisely, suppose a function $f$ is continuous and differentiable on an interval $I$, and its [derivative](https://algebrica.org/derivatives) never vanishes:

$$f^{'} \left(\right. x \left.\right) \neq 0 \forall x \in I$$

Under these conditions, the function is strictly monotonic on $I$, which guarantees that it is invertible on that interval. As a consequence, an inverse function $f^{- 1}$ exists on $f \left(\right. I \left.\right)$. This inverse is not only continuous but also differentiable, and its derivative is given by the relation:

$$\left(\right. f^{- 1} \left.\right)^{'} \left(\right. y \left.\right) = \frac{1}{f^{'} \left(\right. f^{- 1} \left(\right. y \left.\right) \left.\right)}$$

This result shows how a local condition (the derivative never becomes zero) ensures a global property such as invertibility.
