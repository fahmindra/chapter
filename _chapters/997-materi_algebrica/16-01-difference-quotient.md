---
layout: chapter
title: "Difference Quotient"
chapter: "Derivatives"
chapter_order: 16
section_order: 1
permalink: /materi-algebrica/derivatives/difference-quotient/
---

## What is the difference quotient

Consider a function $y = f \left(\right. x \left.\right)$ defined on the interval $\left[\right. a , b \left]\right.$, and two real numbers $c$ and $c + h$ with $h \neq 0$, both lying within the interval $\left[\right. a , b \left]\right.$. The difference quotient of $f$ at the point $c$ is defined as the ratio:

$$\frac{\Delta y}{\Delta x} = \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$

The condition $h \neq 0$ is necessary: for $h = 0$ the points $A$ and $B$ coincide, the secant line is not defined, and the ratio reduces to $\frac{0}{0}$. Consider the points $A$ and $B$ with:

- $A \left(\right. c , f \left(\right. c \left.\right) \left.\right)$
- $B \left(\right. c + h , f \left(\right. c + h \left.\right) \left.\right)$

the **difference quotient** of $f$ at the point $c$ is the slope of the line passing through $A$ and $B$.

![](https://algebrica.org/wp-content/uploads/resources/images/difference-quotient-2.png)

The difference quotient is fundamental to the definition of the [derivative](https://algebrica.org/derivatives). The derivative of a function at a point is the [limit](https://algebrica.org/limits/) of the difference quotient as $h$ approaches zero.

$$f^{'} \left(\right. c \left.\right) = \underset{h \rightarrow 0}{lim} \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$

This process, known as the limit of the difference quotient, provides the instantaneous rate of change of the function at that point, or equivalently, the slope of the tangent line to the graph of the function.

---

In general, the difference quotient measures how a function changes over a finite displacement. As the interval shrinks, it transitions from a global measure of variation to a local one.

- The difference quotient provides an approximation of the rate of change. It is calculated over a finite interval $\left[\right. x , x + \Delta x \left]\right.$ and represents the average rate of change.
- The derivative provides the exact rate of change. It is calculated by taking the limit as $\Delta x \rightarrow 0$ and represents the instantaneous rate of change.

It is worth noting that the difference quotient and the [derivative](https://algebrica.org/derivatives) measure the same geometric quantity at different scales.

- The difference quotient measures the slope of a [secant](https://algebrica.org/secant-and-cosecant/) line over a finite interval.
- The derivative measures the slope of the [tangent](https://algebrica.org/tangent-and-cotangent/) line at a point.

## Alternative forms

- $$\text{1}. \frac{f \left(\right. c + h \left.\right) - f \left(\right. c \left.\right)}{h}$$
- $$\text{2}. \frac{f \left(\right. x_{1} \left.\right) - f \left(\right. x_{0} \left.\right)}{x_{1} - x_{0}}$$
- $$\text{3}. \frac{f \left(\right. x + \Delta x \left.\right) - f \left(\right. x \left.\right)}{\Delta x}$$
- $$\text{4}. \frac{f \left(\right. x + d x \left.\right) - f \left(\right. x \left.\right)}{d x}$$

###### The expressions above represent the same quantity and differ only in how the two points are labeled, depending on the notation in use.

## Example 1

Let us calculate the difference quotient of the function $y = f \left(\right. x \left.\right) = 3 x^{2} - x$ at the point $c = 1$ for a generic $h$.

Determine $f \left(\right. c + h \left.\right) = f \left(\right. 1 + h \left.\right)$:

$$f \left(\right. 1 + h \left.\right) & = 3 \left(\right. 1 + h \left.\right)^{2} - \left(\right. 1 + h \left.\right) \\ & = 3 \left(\right. 1 + h^{2} + 2 h \left.\right) - 1 - h \\ & = 3 + 3 h^{2} + 6 h - 1 - h \\ & = 3 h^{2} + 5 h + 2$$

---

Determine $f \left(\right. c \left.\right) = f \left(\right. 1 \left.\right)$:
 $$f \left(\right. 1 \left.\right) = 3 \left(\right. 1 \left.\right)^{2} - 1 = 3 - 1 = 2$$

---

Calculate the difference quotient:
$$\frac{f \left(\right. 1 + h \left.\right) - f \left(\right. 1 \left.\right)}{h} & = \frac{\left(\right. 3 h^{2} + 5 h + 2 \left.\right) - 2}{h} \\ & = \frac{3 h^{2} + 5 h + 2 - 2}{h} \\ & = \frac{3 h^{2} + 5 h}{h} \\ & = 3 h + 5$$

The expression $3 h + 5$ represents, as $h$ varies, the slope of a secant line passing through point $A$ on the graph with an abscissa of 1.

## Example 2

Let us now consider a function that is not polynomial: $f \left(\right. x \left.\right) = \sqrt{x}$,calculated at the point $c = 4$. The procedure is the same as before, but the simplification of the difference quotient requires an additional step. Determine $f \left(\right. 4 + h \left.\right)$:

$$f \left(\right. 4 + h \left.\right) = \sqrt{4 + h}$$

Determine $f \left(\right. 4 \left.\right)$:

$$f \left(\right. 4 \left.\right) = \sqrt{4} = 2$$

The difference quotient takes the form:

$$\frac{f \left(\right. 4 + h \left.\right) - f \left(\right. 4 \left.\right)}{h} = \frac{\sqrt{4 + h} - 2}{h}$$

As it stands, this expression cannot be simplified directly since numerator and denominator
share no obvious common factor. The standard approach is to rationalize the numerator
by multiplying both numerator and denominator by the conjugate expression
$\sqrt{4 + h} + 2$:

$$\frac{\sqrt{4 + h} - 2}{h} \cdot \frac{\sqrt{4 + h} + 2}{\sqrt{4 + h} + 2} & = \frac{\left(\right. 4 + h \left.\right) - 4}{h \left(\right. \sqrt{4 + h} + 2 \left.\right)} \\ & = \frac{h}{h \left(\right. \sqrt{4 + h} + 2 \left.\right)} \\ & = \frac{1}{\sqrt{4 + h} + 2}$$

The factor $h$ cancels and the result is well-defined for every $h \neq 0$.

The expression $\frac{1}{\sqrt{4 + h} + 2}$ represents the slope of the secant through $A = \left(\right. 4 , 2 \left.\right)$ and $B = \left(\right. 4 + h , \sqrt{4 + h} \left.\right)$ as $h$ varies.

As $h \rightarrow 0$, this slope approaches $\frac{1}{4}$ which is precisely the derivative of $\sqrt{x}$ at $x = 4$.

## Selected references

- **Purdue University, N. Egbert**. [The Difference Quotient](https://www.math.purdue.edu/~egbertn/fa2016/notes/lesson8.pdf)
- **Dartmouth College**. [The Difference Quotient and the Derivative](https://math.dartmouth.edu/opencalc2/cole/lecture21.pdf)
- **Princeton University**. [Differential and Integral Calculus](https://imai.fas.harvard.edu/teaching/files/calculus.pdf)
- **Harvard University, O. Knill**. [Introduction to Calculus](https://people.math.harvard.edu/~knill/teaching/math1a_2012/handouts/math1a_2012.pdf)
- **California State University San Marcos**. [Difference Quotient](https://www.csusm.edu/mathlab/documents/differencequotient-r6.pdf)
