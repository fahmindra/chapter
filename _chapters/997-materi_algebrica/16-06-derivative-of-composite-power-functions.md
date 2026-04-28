---
layout: chapter
title: "Derivative of Composite Power Functions"
chapter: "Derivatives"
chapter_order: 16
section_order: 6
permalink: /materi-algebrica/derivatives/derivative-of-composite-power-functions/
---

## Composite Power Functions and Derivatives

We have previously introduced how to calculate the [derivative](https://algebrica.org/derivatives) of a function at a point using the definition of the [difference quotient](https://algebrica.org/difference-quotient). We also studied how to differentiate simple functions and [composite functions](https://algebrica.org/the-derivative-of-a-composite-function/). Now, let’s see how to differentiate power functions of the form:

$$D \left[\right. f \left(\right. x \left.\right) \left]\right.^{g \left(\right. x \left.\right)}$$

To calculate the derivative of such a function, a combination of the [logarithmic](https://algebrica.org/logarithms) rule and the derivative of [exponential functions](https://algebrica.org/exponential-function) is used. The general formula for the derivative of $f \left(\right. x \left.\right)^{g} \left(\right. x \left.\right)$, with $f$ and $g$ differentiable, is as follows:

$$D \left[\right. f \left(\right. x \left.\right) \left]\right.^{g \left(\right. x \left.\right)} = f \left(\right. x \left.\right)^{g \left(\right. x \left.\right)} \left[\right. g^{'} \left(\right. x \left.\right) ln ⁡ f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \frac{f^{'} \left(\right. x \left.\right)}{f \left(\right. x \left.\right)} \left]\right.$$

Where:

- $f \left(\right. x \left.\right)^{g \left(\right. x \left.\right)}$ is the original function.
- $f^{'} \left(\right. x \left.\right)$ is the derivative of $f \left(\right. x \left.\right)$.
- $ln ⁡ f \left(\right. x \left.\right)$ is the natural logarithm of $f \left(\right. x \left.\right)$.
- $g^{'} \left(\right. x \left.\right)$ is the derivative of $g \left(\right. x \left.\right)$.

## Example

Let’s consider the function $y = x^{2 x}$ as an example, and calculate its derivative.

---

First, let’s rewrite the function by applying the logarithm to both sides:

$$ln ⁡ y = ln ⁡ \left(\right. x^{2 x} \left.\right)$$

For the properties of logarithms $log_{a} ⁡ \left(\right. b^{c} \left.\right) = c \cdot log_{a} ⁡ \left(\right. b \left.\right)$

The equality can be rewritten as:

$$ln ⁡ y = 2 x \cdot ln ⁡ \left(\right. x \left.\right)$$

---

Since $ln ⁡ y$ is a composite function, its derivative is

$$\frac{1}{y} \cdot y^{'}$$

Let’s compute the derivative for the element on the right-hand side of the equality $2 x \cdot ln ⁡ \left(\right. x \left.\right)$:

$$2 \cdot ln ⁡ \left(\right. x \left.\right) + 2 x \cdot \frac{1}{x}$$

We obtain:

$$\frac{1}{y} \cdot y^{'} = 2 \cdot ln ⁡ \left(\right. x \left.\right) + 2 x \cdot \frac{1}{x}$$

---

The equality can be rewritten as:

$$y^{'} = y \cdot \left(\right. 2 \cdot ln ⁡ \left(\right. x \left.\right) + 2 \left.\right)$$

Since $y = x^{2 x}$, we have:

$$y^{'} = x^{2 x} \cdot \left(\right. 2 \cdot ln ⁡ \left(\right. x \left.\right) + 2 \left.\right)$$

Therefore, the derivative of $y = x^{2}$ is equal to:

$$x^{2 x} \cdot \left(\right. 2 \cdot ln ⁡ \left(\right. x \left.\right) + 2 \left.\right)$$

## Test yourself

- $$\text{1}. y = x^{2 cos ⁡ \left(\right. x \left.\right)}$$ [solution](https://algebrica.org/derivative-a-1)
- $$\text{2}. y = x^{ln ⁡ \left(\right. x \left.\right)}$$ [solution](https://algebrica.org/derivative-a-2)

##### The proposed functions are designed to help you consolidate your understanding of composite function derivatives. Try solving them independently before checking the solutions provided.
