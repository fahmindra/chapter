---
layout: chapter
title: "Derivatives"
chapter: "Derivatives"
chapter_order: 16
section_order: 2
permalink: /materi-algebrica/derivatives/derivatives/
---

## Introduction to derivatives

Consider a function $y = f \left(\right. x \left.\right)$ defined on an interval $\left[\right. a , b \left]\right.$. The derivative of $f$ at a point $c \in \left(\right. a , b \left.\right)$, denoted by $f^{'} \left(\right. c \left.\right)$, is defined, if the limit exists and is finite, as the limit of the [difference quotient](https://algebrica.org/difference-quotient/) as $h \rightarrow 0$:

$$f^{'} \left(\right. c \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$

If this limit exists for every $x$ in an interval, then the derivative defines a new function $f^{'} \left(\right. x \left.\right)$, called the derivative of $f$. The value $f^{'} \left(\right. x \left.\right)$ represents the slope of the tangent line to the graph of $f$ at the point $x$.

---

When $h \rightarrow 0$, the point $B$ approaches the point $A$, and the [line](https://algebrica.org/lines/) $A B$ becomes the tangent line to the curve at point $A$. The slope of the tangent line at $A$ is called the derivative of the function at point $c$.

![](https://algebrica.org/wp-content/uploads/resources/images/derivatives-1.png)

With reference to the tangent at point $A$ of the function $y = m x + q$, the derivative $f^{'} \left(\right. x \left.\right)$ represents the value of the slope coefficient $m$.

---

A function is differentiable at a point $c$ if the derivative $f^{'} \left(\right. c \left.\right)$ exists. If a function is differentiable:

- The function is defined in a neighborhood of the point $c$.
- The limit of the [difference quotient](https://algebrica.org/difference-quotient), with respect to $c$, exists and is finite as $h \rightarrow 0$.
- The right-hand and left-hand limits of the difference quotient exist and are equal.

---

The inverse operation of differentiation is [integration](https://algebrica.org/indefinite-integrals/). This deep connection between derivatives and integrals is formalized by the [Fundamental Theorem of Calculus](https://algebrica.org/fundamental-theorem-of-calculus/), which establishes that differentiation and integration are inverse processes.

##### Derivatives play a fundamental role in physics as well. A classic example is [velocity](https://algebrica.org/velocity), which is defined as the derivative of position with respect to time. This simple concept forms the basis for understanding motion and change in the physical world.

If a function $f \left(\right. x \left.\right)$ is differentiable at a point $c$, then the function is also [continuous](https://algebrica.org/continuous-functions/) at that point. However, not all functions that are continuous at a point $c$ are differentiable. In other words, differentiable functions form a subset of continuous functions.

## Example 1

Let’s calculate the derivative of the function $f \left(\right. x \left.\right) = 2 x^{2} - 3 x$ at $c = 2$ using the definition of the derivative.

$$f^{'} \left(\right. 2 \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. 2 + h \left.\right) - f \left(\right. 2 \left.\right)}{h}$$

---

Let’s calculate the value of $f \left(\right. 2 + h \left.\right)$:

$$f \left(\right. 2 + h \left.\right) & = 2 \left(\right. 2 + h \left.\right)^{2} - 3 \left(\right. 2 + h \left.\right) \\ & = 2 \left(\right. 4 + 4 h + h^{2} \left.\right) - 3 \left(\right. 2 + h \left.\right) \\ & = 8 + 8 h + 2 h^{2} - 6 - 3 h \\ & = 2 + 5 h + 2 h^{2}$$

---

Now, calculate the value of $f \left(\right. 2 \left.\right)$:

$$f \left(\right. 2 \left.\right) = 2 \left(\right. 2^{2} \left.\right) - 3 \left(\right. 2 \left.\right) = 8 - 6 = 2$$

---

Next, calculate the difference $f \left(\right. 2 + h \left.\right) - f \left(\right. 2 \left.\right)$:

$$f \left(\right. 2 + h \left.\right) - f \left(\right. 2 \left.\right) = \left(\right. 2 + 5 h + 2 h^{2} \left.\right) - 2 = 5 h + 2 h^{2}$$

Now, calculate the difference quotient:

$$\frac{f \left(\right. 2 + h \left.\right) - f \left(\right. 2 \left.\right)}{h} = \frac{5 h + 2 h^{2}}{h} = 5 + 2 h$$

---

Finally, calculate the limit:

$$\underset{h \rightarrow 0}{lim} \left(\right. 5 + 2 h \left.\right) = 5$$

Thus, the derivative of $f \left(\right. x \left.\right) = 2 x^{2} - 3 x$ at $c = 2$ is: $$f^{'} \left(\right. 2 \left.\right) = 5$$

## Right-hand and left-hand derivatives

Since the derivative is the limit of the difference quotient, as in the case of limits, it is possible to define the **right-hand** and **left-hand derivatives** of a function $y = f \left(\right. x \left.\right)$.

The right-hand derivative is:
$$f_{+}^{′} \left(\right. c \left.\right) = \underset{h \rightarrow 0^{+}}{lim} \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$

The left-hand derivative is:
$$f_{-}^{′} \left(\right. c \left.\right) = \underset{h \rightarrow 0^{-}}{lim} \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$

A function is differentiable at a point $c$ if the right-hand derivative and the left-hand derivative at the point exist and are equal to each other. More generally, a function $y = f \left(\right. x \left.\right)$ is differentiable on an interval $\left[\right. A , B \left]\right.$ if it is differentiable at all interior points of the interval and if the right-hand derivative at point $A$ and the left-hand derivative at point $B$ exist and are finite.

## Fundamental derivatives

- $$f \left(\right. x \left.\right) = c f^{'} \left(\right. x \left.\right) = 0$$
- $$f \left(\right. x \left.\right) = x f^{'} \left(\right. x \left.\right) = 1$$
- $$f \left(\right. x \left.\right) = x^{a} a \in \mathbb{R} , x > 0 f^{'} \left(\right. x \left.\right) = a x^{a - 1}$$
- $$f \left(\right. x \left.\right) = \sqrt{x} x > 0 f^{'} \left(\right. x \left.\right) = \frac{1}{2 \sqrt{x}}$$
- $$f \left(\right. x \left.\right) = a^{x} f^{'} \left(\right. x \left.\right) = a^{x} ln ⁡ \left(\right. a \left.\right)$$
- $$f \left(\right. x \left.\right) = log_{a} ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = \frac{1}{x log ⁡ \left(\right. a \left.\right)}$$
- $$f \left(\right. x \left.\right) = ln ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = \frac{1}{x}$$
- $$f \left(\right. x \left.\right) = e^{x} f^{'} \left(\right. x \left.\right) = e^{x}$$
- $$f \left(\right. x \left.\right) = sin ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = cos ⁡ \left(\right. x \left.\right)$$
- $$f \left(\right. x \left.\right) = cos ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = - sin ⁡ \left(\right. x \left.\right)$$
- $$f \left(\right. x \left.\right) = tan ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = 1 + tan^{2} ⁡ \left(\right. x \left.\right)$$
- $$f \left(\right. x \left.\right) = cot ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = - \left(\right. 1 + cot^{2} ⁡ \left(\right. x \left.\right) \left.\right)$$
- $$f \left(\right. x \left.\right) = arcsin ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = \frac{1}{\sqrt{1 - x^{2}}}$$
- $$f \left(\right. x \left.\right) = arccos ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = \frac{- 1}{\sqrt{1 - x^{2}}}$$
- $$f \left(\right. x \left.\right) = arctan ⁡ \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = \frac{1}{1 + x^{2}}$$
- $$f \left(\right. x \left.\right) = \text{arccot} \left(\right. x \left.\right) f^{'} \left(\right. x \left.\right) = \frac{- 1}{1 + x^{2}}$$

##### $f \left(\right. x \left.\right) = c$; Derivative: $f^{'} \left(\right. x \left.\right) = 0$, since a line $y = c$ is parallel to the x-axis, its slope $m$ is equal to 0.

##### $f \left(\right. x \left.\right) = x$; Derivative: $f^{'} \left(\right. x \left.\right) = 1$. The function $y = x$ is the bisector of the first and third quadrants, and its slope $m$ is equal to 1.

##### $f \left(\right. x \left.\right) = x^{a}$, $a \in \mathbb{R} , x > 0$; Derivative: $f^{'} \left(\right. x \left.\right) = a x^{a - 1}$

## Operations with derivatives

The derivative of the product of a constant $c$ and a differentiable function $f \left(\right. x \left.\right)$ is equal to the product of the constant and the derivative of the function. This is expressed as:

$$D \left[\right. c \cdot f \left(\right. x \left.\right) \left]\right. = c \cdot f^{'} \left(\right. x \left.\right)$$

For example, if $c = 3$ and $f \left(\right. x \left.\right) = x^{2}$, then:

$$D \left[\right. 3 \cdot x^{2} \left]\right. = 3 \cdot f^{'} \left[\right. x^{2} \left]\right. = 3 \cdot 2 x = 6 x$$

---

The derivative of the sum of two functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ is equal to the sum of their derivatives. This is expressed as:

$$D \left[\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left]\right. = f^{'} \left(\right. x \left.\right) + g^{'} \left(\right. x \left.\right)$$

For example, if $f \left(\right. x \left.\right) = x^{2}$ and $g \left(\right. x \left.\right) = 3 x$, then:

$$D \left[\right. x^{2} + 3 x \left]\right. = f^{'} \left(\right. x^{2} \left.\right) + g^{'} \left(\right. 3 x \left.\right) = 2 x + 3$$

---

The derivative of the product of two functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ is given by the product rule. This is expressed as:

$$D \left[\right. f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) \left]\right. = f^{'} \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) + f \left(\right. x \left.\right) \cdot g^{'} \left(\right. x \left.\right)$$

For example, if $f \left(\right. x \left.\right) = x^{2}$ and $g \left(\right. x \left.\right) = 3 x$, then:

$$D \left[\right. x^{2} \cdot 3 x \left]\right. & = f^{'} \left(\right. x^{2} \left.\right) \cdot g \left(\right. 3 x \left.\right) + f \left(\right. x^{2} \left.\right) \cdot g^{'} \left(\right. 3 x \left.\right) \\ & = 2 x \cdot 3 x + x^{2} \cdot 3 \\ & = 6 x^{2} + 3 x^{2} = 9 x^{2}$$

---

The derivative of the quotient of two functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$, where $g \left(\right. x \left.\right) \neq 0$, is given by the quotient rule. This is expressed as:

$$D \left[\right. \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} \left]\right. = \frac{f^{'} \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) - f \left(\right. x \left.\right) \cdot g^{'} \left(\right. x \left.\right)}{g^{2} \left(\right. x \left.\right)}$$

For example, if $f \left(\right. x \left.\right) = x^{2}$ and $g \left(\right. x \left.\right) = 3 x + 1$, then:

$$D \left[\right. \frac{x^{2}}{3 x + 1} \left]\right. & = \frac{2 x \cdot \left(\right. 3 x + 1 \left.\right) - x^{2} \cdot 3}{\left(\right. 3 x + 1 \left.\right)^{2}} \\ & = \frac{6 x^{2} + 2 x - 3 x^{2}}{\left(\right. 3 x + 1 \left.\right)^{2}} \\ & = \frac{3 x^{2} + 2 x}{\left(\right. 3 x + 1 \left.\right)^{2}}$$

---

The derivative of the reciprocal of a function $f \left(\right. x \left.\right)$, where $f \left(\right. x \left.\right) \neq 0$, is given by:

$$D \left[\right. \frac{1}{f \left(\right. x \left.\right)} \left]\right. = - \frac{f^{'} \left(\right. x \left.\right)}{f^{2} \left(\right. x \left.\right)}$$

For example, if $f \left(\right. x \left.\right) = 3 x + 1$, then:

$$D \left[\right. \frac{1}{3 x + 1} \left]\right. = - \frac{3}{\left(\right. 3 x + 1 \left.\right)^{2}}$$

---

When differentiating a composition of two functions, these rules are not sufficient. In that case, it is necessary to apply the [derivative of a composite function](https://algebrica.org/the-derivative-of-a-composite-function/), also known as the chain rule.

## Higher-order derivatives

In general, the derivatives we have discussed so far are the first derivatives of a function $y = f \left(\right. x \left.\right)$. The differentiation process can be iterated to compute the higher-order derivatives of a first derivative, such as the second derivative and the third derivative.

For example, let the function $y = f \left(\right. x \left.\right) = 3 x^{3} - 2 x^{2} + 1$.

- The first derivative of the function is: $$f^{'} \left(\right. x \left.\right) = 9 x^{2} - 4 x$$
- The second derivative is: $$f^{''} \left(\right. x \left.\right) = 18 x - 4$$
- The third derivative
  $$f^{′ ′ ′} \left(\right. x \left.\right) = 18$$

First and second derivatives play a fundamental role in analyzing the local behavior of functions, particularly in identifying [minimum and maximum points](https://algebrica.org/maximum-minimum-and-inflection-points/), as well as inflection points.

## Key theorems in differential calculus

Derivatives are also at the foundation of some of the most important theorems in differential calculus.

- [Weierstrass’s Theorem](https://algebrica.org/weierstrass-theorem/) guarantees that a continuous function on a closed and bounded interval attains both its maximum and minimum values.
- [Fermat’s Theorem](https://algebrica.org/fermats-theorem/) establishes a necessary condition for local extrema.
- [Rolle’s Theorem](https://algebrica.org/rolles-theorem/) and [Lagrange’s Theorem](https://algebrica.org/lagranges-theorem/), also known as the Mean Value Theorem, describe fundamental properties of differentiable functions on a closed interval.
- Further generalizations are provided by [Cauchy’s Theorem](https://algebrica.org/cauchy-theorem/) and [L’Hôpital’s Rule](https://algebrica.org/hopital-rule/), which extends the use of derivatives to the evaluation of [indeterminate forms](https://algebrica.org/indeterminate-forms/) of limits.

## Equation of the tangent line

The slope of the tangent line to the graph of a function $f \left(\right. x \left.\right)$ at a point $x_{0}$ is given by the derivative $f^{'} \left(\right. x_{0} \left.\right)$. This value represents the instantaneous rate of change of the function at that point and coincides with the limit of the slopes of the secant lines approaching $x_{0}$.

More precisely, if we consider a second point $x_{0} + h$, the slope of the secant line through the points $\left(\right. x_{0} , f \left(\right. x_{0} \left.\right) \left.\right)$ and $\left(\right. x_{0} + h , f \left(\right. x_{0} + h \left.\right) \left.\right)$ is:

$$\frac{f \left(\right. x_{0} + h \left.\right) - f \left(\right. x_{0} \left.\right)}{h}$$

If the limit of this expression exists as $h \rightarrow 0$, the function is differentiable at $x_{0}$, and this limit equals $f^{'} \left(\right. x_{0} \left.\right)$. The tangent line is therefore understood as the limiting position of the secant lines.

If the derivative exists and is finite, the tangent line is not vertical. In that case, its equation can be written in point–slope form. Since the line passes through the point $\left(\right. x_{0} , f \left(\right. x_{0} \left.\right) \left.\right)$ and has slope $f^{'} \left(\right. x_{0} \left.\right)$, its equation is:

$$y - f \left(\right. x_{0} \left.\right) = f^{'} \left(\right. x_{0} \left.\right) \left(\right. x - x_{0} \left.\right)$$

This linear function provides the best linear approximation of $f$ near $x_{0}$. In fact, for values of $x$ close to $x_{0}$, the increment of the function satisfies:

$$f \left(\right. x \left.\right) \approx f \left(\right. x_{0} \left.\right) + f^{'} \left(\right. x_{0} \left.\right) \left(\right. x - x_{0} \left.\right)$$

which expresses the idea that, at sufficiently small scales, a differentiable function behaves approximately like its tangent line.

## Example 2

Let us consider the [parabola](https://algebrica.org/parabola) defined by the equation $y = 2 x^{2} + 3 x$, and determine the tangent line at the point $P \left(\right. 1 , 5 \left.\right)$.

---

First, we compute the derivative $f^{'} \left(\right. x \left.\right)$, and we obtain:

$$2 x + 3$$

We compute the slope of the tangent line at $x = 1$:

$$f^{'} \left(\right. 1 \left.\right) = 2 \left(\right. 1 \left.\right) + 3 = 5$$

Therefore, the slope of the tangent line is $m = 5$. We have:

$$y - f \left(\right. 1 \left.\right) = f ′ \left(\right. 1 \left.\right) \left(\right. x - 1 \left.\right) \rightarrow y - 5 = 5 \left(\right. x - 1 \left.\right)$$

Completing the calculations, we obtain the equation of the tangent line:

$$y = 5 x$$

## Partial derivatives

Derivatives are fundamental in multivariable calculus. When a function depends on multiple variables, the rate of change with respect to a single variable, while keeping all other variables constant, is described by the partial derivative:

$$\frac{\partial f}{\partial x_{i}} \left(\right. x_{0} \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. x_{1}^{0} , \ldots , x_{i}^{0} + h , \ldots , x_{n}^{0} \left.\right) - f \left(\right. x_{0} \left.\right)}{h}$$

The [vector](https://algebrica.org/vectors/) of all partial derivatives forms the gradient $\nabla f$, which indicates the direction of the steepest increase of $f$. For a comprehensive discussion, including higher-order derivatives, Schwarz’s theorem, the Jacobian matrix, and the chain rule for functions of several variables, refer to the entry on [partial derivatives](https://algebrica.org/partial-derivatives).

## Selected references

- **MIT OpenCourseWare**. [Single Variable Calculus – Lecture Notes (Derivatives)](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/pages/lecture-notes/)
- **University of British Columbia**. [Differentiation – Lecture Notes](https://www.math.ubc.ca/~feldman/m101/clp/clp_notes_100.pdf)
- **University College London (UCL)**. [On Differentiation I](https://www.ucl.ac.uk/~uczlcfe/my%20website%20notes/_maths%20-%20diff%201%20-%2000%20-%20complete.pdf)
- **Simon Fraser University**. [Calculus III – Partial Derivatives](https://www.sfu.ca/~vjungic/Calculus%203/Calculus3.pdf)
- **Portland State University**. [Calculus Problems and Exercises](https://web.pdx.edu/~erdman/CALCULUS/CALCULUS_pdf.pdf)
- **Northwestern University**. [Real Analysis – Lecture Notes](https://sites.math.northwestern.edu/scg479/courses/notes/lecture-notes-320-3.pdf)
- **Penn State University**. [Calculus – Derivatives and Applications](https://www.math.psu.edu/lamy/misc/Calc_Notes.pdf)
