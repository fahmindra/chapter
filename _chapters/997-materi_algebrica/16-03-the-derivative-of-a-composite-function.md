---
layout: chapter
title: "Derivative of a Composite Function"
chapter: "Derivatives"
chapter_order: 16
section_order: 3
permalink: /materi-algebrica/derivatives/derivative-of-a-composite-function/
---

## The chain rule

Let $g$ be differentiable at $x$, and let $f$ be differentiable at $z = g \left(\right. x \left.\right)$. Then the composite function $y = f \left(\right. g \left(\right. x \left.\right) \left.\right)$ is differentiable at $x$, and its [derivative](https://algebrica.org/derivative/) is the product of the derivative of $f$ evaluated at $g \left(\right. x \left.\right)$ and the derivative of $g$ at $x$:

$$D \left[\right. f \left(\right. g \left(\right. x \left.\right) \left.\right) \left]\right. = f^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) \cdot g^{'} \left(\right. x \left.\right)$$

This result is known as the chain rule. It states that to differentiate a composite function, one multiplies the derivative of the outer function, evaluated at the inner function, by the derivative of the inner function.

In Leibniz notation, if $y = f \left(\right. u \left.\right)$ and $u = g \left(\right. x \left.\right)$, the chain rule takes the form:

$$\frac{d y}{d x} = \frac{d y}{d u} \cdot \frac{d u}{d x}$$

## Proof

To prove that $D \left[\right. f \left(\right. g \left(\right. x \left.\right) \left.\right) \left]\right. = f^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) \cdot g^{'} \left(\right. x \left.\right)$ we calculate the following [limit](https://algebrica.org/limits/):

$$D \left[\right. f \left(\right. g \left(\right. x \left.\right) \left.\right) \left]\right. = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. g \left(\right. x + h \left.\right) \left.\right) - f \left(\right. g \left(\right. x \left.\right) \left.\right)}{h}$$

---

Let $z = g \left(\right. x \left.\right)$, then $g \left(\right. x + h \left.\right) - g \left(\right. x \left.\right) = \Delta z .$ This implies that $g \left(\right. x + h \left.\right) = g \left(\right. x \left.\right) + \Delta z .$ The limit becomes:

$$D \left[\right. f \left(\right. g \left(\right. x \left.\right) \left.\right) \left]\right. = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. z + \Delta z \left.\right) - f \left(\right. z \left.\right)}{h}$$

---

Multiplying both the numerator and the denominator by $\Delta z$, we get:

$$D \left[\right. f \left(\right. g \left(\right. x \left.\right) \left.\right) \left]\right. & = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. z + \Delta z \left.\right) - f \left(\right. z \left.\right)}{\Delta z} \cdot \frac{\Delta z}{h} \\ & = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. z + \Delta z \left.\right) - f \left(\right. z \left.\right)}{\Delta z} \cdot \frac{g \left(\right. x + h \left.\right) - g \left(\right. x \left.\right)}{h} \\ & = f^{'} \left(\right. z \left.\right) \cdot g^{'} \left(\right. x \left.\right) \\ & = f^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) \cdot g^{'} \left(\right. x \left.\right)$$

This argument assumes $\Delta z \neq 0$ for $h$ sufficiently small. A complete proof handles the case $\Delta z = 0$ separately via an auxiliary function; the conclusion is the same.

---

In the case of powers of a function, the rule generalizes as follows:

$$D \left[\right. f \left(\right. x \left.\right)^{a} \left]\right. = a \left[\right. f \left(\right. x \left.\right) \left]\right.^{a - 1} f^{'} \left(\right. x \left.\right)$$

## Example 1

Let’s compute the derivative of the following composite function:

$$y = f \left(\right. g \left(\right. x \left.\right) \left.\right) = sin ⁡ \left(\right. 3 x^{2} + 2 x \left.\right)$$

In this case, we have:

- The inner function $g \left(\right. x \left.\right) = 3 x^{2} + 2 x$
- The outer function $f \left(\right. t \left.\right) = sin ⁡ \left(\right. t \left.\right)$, where $t = g \left(\right. x \left.\right) = 3 x^{2} + 2 x$

---

The outer function is $f \left(\right. t \left.\right) = sin ⁡ \left(\right. t \left.\right)$. Its derivative is:

$$f^{'} \left(\right. t \left.\right) = cos ⁡ \left(\right. t \left.\right)$$

Substituting $t = g \left(\right. x \left.\right)$:

$$f^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) = cos ⁡ \left(\right. 3 x^{2} + 2 x \left.\right)$$

---

The inner function is $g \left(\right. x \left.\right) = 3 x^{2} + 2 x$. Its derivative is:

$$g^{'} \left(\right. x \left.\right) = 6 x + 2$$

Applying the chain rule we obtain:

$$D \left[\right. f \left(\right. g \left(\right. x \left.\right) \left.\right) \left]\right. = f^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) \cdot g^{'} \left(\right. x \left.\right)$$

The result is:

$$\left(\right. 6 x + 2 \left.\right) cos ⁡ \left(\right. 3 x^{2} + 2 x \left.\right)$$

###### Explore the case of [composite power functions](https://algebrica.org/derivative-of-composite-power-functions/), specifically the calculation of the derivative of functions of the type: $$D \left[\right. f \left(\right. x \left.\right)^{g \left(\right. x \left.\right)} \left]\right.$$

## Extension to multiple compositions

The chain rule can be extended to compositions involving three or more functions. For example, given $y = f \left(\right. g \left(\right. h \left(\right. x \left.\right) \left.\right) \left.\right)$, the derivative is:

$$D \left[\right. f \left(\right. g \left(\right. h \left(\right. x \left.\right) \left.\right) \left.\right) \left]\right. = f^{'} \left(\right. g \left(\right. h \left(\right. x \left.\right) \left.\right) \left.\right) \cdot g^{'} \left(\right. h \left(\right. x \left.\right) \left.\right) \cdot h^{'} \left(\right. x \left.\right)$$

Each factor represents the derivative of a function in the composition, evaluated at the composition of all subsequent functions. This pattern generalises to any finite number of nested functions. For $y = f_{1} \left(\right. f_{2} \left(\right. \hdots f_{n} \left(\right. x \left.\right) \hdots \left.\right) \left.\right)$, the derivative is given by the product:

$$f_{1}^{'} \left(\right. f_{2} \left(\right. \hdots f_{n} \left(\right. x \left.\right) \hdots \left.\right) \left.\right) \cdot f_{2}^{'} \left(\right. f_{3} \left(\right. \hdots f_{n} \left(\right. x \left.\right) \hdots \left.\right) \left.\right) \hdots f_{n - 1}^{'} \left(\right. f_{n} \left(\right. x \left.\right) \left.\right) \cdot f_{n}^{'} \left(\right. x \left.\right)$$

In practical applications, differentiation proceeds from the outermost function inward, with each derivative computed in sequence and the results multiplied together.

---

As an example, consider $y = sin ⁡ \left(\right. e^{3 x} \left.\right)$. The composition involves three functions:

$$h \left(\right. x \left.\right) & = 3 x \\ g \left(\right. t \left.\right) & = e^{t} \\ f \left(\right. s \left.\right) & = sin ⁡ \left(\right. s \left.\right)$$

Applying the chain rule from the outside inward we obtain:

$$D \left[\right. sin ⁡ \left(\right. e^{3 x} \left.\right) \left]\right. & = cos ⁡ \left(\right. e^{3 x} \left.\right) \cdot e^{3 x} \cdot 3 \\ & = 3 e^{3 x} cos ⁡ \left(\right. e^{3 x} \left.\right)$$

## Example 2

Consider the following function:

$$y = ln ⁡ \left(\right. e^{x^{2}} + 1 \left.\right)$$

The composition involves three functions:

$$h \left(\right. x \left.\right) & = x^{2} \\ g \left(\right. t \left.\right) & = e^{t} + 1 \\ f \left(\right. s \left.\right) & = ln ⁡ \left(\right. s \left.\right)$$

---

The derivative of the outer function $f \left(\right. s \left.\right) = ln ⁡ \left(\right. s \left.\right)$ is $f^{'} \left(\right. s \left.\right) = \frac{1}{s}$, evaluated at $s = g \left(\right. h \left(\right. x \left.\right) \left.\right) = e^{x^{2}} + 1$:

$$f^{'} \left(\right. g \left(\right. h \left(\right. x \left.\right) \left.\right) \left.\right) = \frac{1}{e^{x^{2}} + 1}$$

The derivative of the middle function $g \left(\right. t \left.\right) = e^{t} + 1$ is $g^{'} \left(\right. t \left.\right) = e^{t}$, evaluated at $t = h \left(\right. x \left.\right) = x^{2}$:

$$g^{'} \left(\right. h \left(\right. x \left.\right) \left.\right) = e^{x^{2}}$$

The derivative of the inner function $h \left(\right. x \left.\right) = x^{2}$ is:

$$h^{'} \left(\right. x \left.\right) = 2 x$$

---

Applying the chain rule from the outside inward:

$$D \left[\right. ln ⁡ \left(\right. e^{x^{2}} + 1 \left.\right) \left]\right. & = \frac{1}{e^{x^{2}} + 1} \cdot e^{x^{2}} \cdot 2 x \\ & = \frac{2 x e^{x^{2}}}{e^{x^{2}} + 1}$$

The result is:

$$\frac{2 x e^{x^{2}}}{e^{x^{2}} + 1}$$

## Selected references

- **Harvard University, O. Knill**. [Chain Rule](https://people.math.harvard.edu/~knill/teaching/math1a2020/handouts/lecture10.pdf)
- **MIT OpenCourseWare, G. Strang**. [Derivatives by the Chain Rule](https://ocw.mit.edu/courses/res-18-001-calculus-fall-2023/mitres_18_001_f17_ch04.pdf)
- **University of Toronto, J. Campesato**. [Differentiability and the Chain Rule](https://www.math.toronto.edu/campesat/ens/1920/1114.pdf)
