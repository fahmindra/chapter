---
layout: chapter
title: "Integration by Parts"
chapter: "Integrals"
chapter_order: 18
section_order: 5
permalink: /materi-algebrica/integrals/integration-by-parts/
---

## The method of integration by parts

The method of integration by parts allows us to rewrite the integral of the product of two [functions](https://algebrica.org/functions/) in a more convenient form. For [indefinite integrals](https://algebrica.org/indefinite-integrals), the formula is:

$$\int f \left(\right. x \left.\right) g^{'} \left(\right. x \left.\right) d x = f \left(\right. x \left.\right) g \left(\right. x \left.\right) - \int f^{'} \left(\right. x \left.\right) g \left(\right. x \left.\right) d x + c$$

For [definite integrals](https://algebrica.org/definite-integrals), the formula extends as:

$$\int_{a}^{b} f \left(\right. x \left.\right) g^{'} \left(\right. x \left.\right) d x = \left[\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left]\right._{a}^{b} - \int_{a}^{b} f^{'} \left(\right. x \left.\right) g \left(\right. x \left.\right) d x$$

where $\left[\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left]\right._{a}^{b} = f \left(\right. b \left.\right) g \left(\right. b \left.\right) - f \left(\right. a \left.\right) g \left(\right. a \left.\right)$ is the boundary term, which must be evaluated.

In both cases, $f$ and $g$ are assumed to be differentiable on the [interval](https://algebrica.org/intervals/) of integration. The method is conceptually simple, but it requires practice to identify which function should be differentiated and which should be integrated in order to simplify the expression.

##### In some cases, integration by parts must be applied more than once to completely evaluate the integral. One should proceed carefully, since repeated applications may increase the length of the computation and make sign errors more likely.

## Derivation of the formula

The integration by parts formula follows directly from the product rule for [derivatives](https://algebrica.org/derivatives). Start from:

$$\frac{d}{d x} \left(\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left.\right) = f^{'} \left(\right. x \left.\right) g \left(\right. x \left.\right) + f \left(\right. x \left.\right) g^{'} \left(\right. x \left.\right)$$

Integrating both sides with respect to $x$:

$$\int \frac{d}{d x} \left(\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left.\right) d x = \int f^{'} \left(\right. x \left.\right) g \left(\right. x \left.\right) d x + \int f \left(\right. x \left.\right) g^{'} \left(\right. x \left.\right) d x$$

The left-hand side is the integral of a derivative, which returns the original function
up to a constant:

$$f \left(\right. x \left.\right) g \left(\right. x \left.\right) = \int f^{'} \left(\right. x \left.\right) g \left(\right. x \left.\right) d x + \int f \left(\right. x \left.\right) g^{'} \left(\right. x \left.\right) d x$$

Rearranging to isolate the second integral on the left:

$$\int f \left(\right. x \left.\right) g^{'} \left(\right. x \left.\right) d x = f \left(\right. x \left.\right) g \left(\right. x \left.\right) - \int f^{'} \left(\right. x \left.\right) g \left(\right. x \left.\right) d x + c$$

This is the integration by parts formula. In the compact notation $u = f \left(\right. x \left.\right)$, $d v = g^{'} \left(\right. x \left.\right) d x$, it takes the familiar form:

$$\int u d v = u v - \int v d u$$

###### In practice, integration by parts is useful when differentiating one factor makes it simpler, while the other can still be integrated without difficulty. The method often turns a complicated expression into something more manageable, and in many problems it can be applied repeatedly until the integral is reduced to a standard form.

## How to choose $u$ and $d v$

The method is effective only if the new integral $\int v d u$ is simpler than
the original one. This depends entirely on how $u$ and $d v$ are assigned,
so the choice is not arbitrary. A practical strategy is:

- Choose $u$ as the factor that becomes simpler when differentiated.
- Choose $d v$ as the remaining factor, so that $v = \int d v$ is easy to compute.

---

A useful order for selecting $u$ is the hierarchy known by the acronym LIATE:

- Logarithmic functions
- Inverse trigonometric functions
- Algebraic expressions
- Trigonometric functions
- Exponential functions

The ordering reflects how these functions behave under differentiation. [Logarithmic](https://algebrica.org/logarithmic-function/) and inverse trigonometric functions simplify considerably when differentiated, making them natural candidates for $u$. [Exponential functions](https://algebrica.org/exponential-function/), by contrast, remain essentially unchanged after differentiation and are generally better assigned to $d v$.

##### Choosing $u$ according to this hierarchy often reduces the complexity of the remaining integral after a single application of the formula

## Most common mistakes

A few recurring mistakes are worth keeping in mind when applying integration by parts.

Choosing $d v$ carelessly, in particular assigning to $d v$ a factor whose integral $v$ is harder to compute than the original integral, often makes the problem worse rather than better. If the resulting $\int v , d u$ is more complex than what you started with, it is worth reconsidering the assignment before proceeding.

In the [definite integral](https://algebrica.org/definite-integrals/) version of the formula, the boundary term $u v \left|\right._{a}^{b}$ must be evaluated explicitly. Omitting it is one of the most common sources of incorrect results, particularly when the computation spans several lines and attention drifts toward the integral that follows.

Sign errors during differentiation are especially insidious in cyclic cases, where $sin ⁡ \left(\right. x \left.\right)$ and $cos ⁡ \left(\right. x \left.\right)$ alternate and a misplaced minus sign propagates through the entire calculation. Keeping track of signs at each step, rather than reconstructing them at the end, saves considerable time.

Finally, in the indefinite case, the constant of integration $C$ must appear in the final result. After repeated applications of the formula it is easy to lose track of it, particularly when intermediate integrals are written without it. A reliable habit is to carry $C$ explicitly only in the last step and to confirm its presence before writing the answer.

## Example 1

Let’s consider an example by solving the following integral:

$$\int x^{2} ln ⁡ \left(\right. x \left.\right) d x$$

The integrand is a product of a logarithmic function and a [power](https://algebrica.org/powers) of $x$. Following the LIATE hierarchy, $ln ⁡ \left(\right. x \left.\right)$ takes priority and is assigned to $f$, while $x^{2}$ is assigned to $g^{'}$:

$$f \left(\right. x \left.\right) = ln ⁡ \left(\right. x \left.\right) \rightarrow f^{'} \left(\right. x \left.\right) = \frac{1}{x}$$

$$g^{'} \left(\right. x \left.\right) = x^{2} \rightarrow g \left(\right. x \left.\right) = \frac{x^{3}}{3}$$

Applying the formula, we obtain:

$$\int x^{2} ln ⁡ \left(\right. x \left.\right) , d x & = ln ⁡ \left(\right. x \left.\right) \cdot \frac{x^{3}}{3} - \int \frac{1}{x} \cdot \frac{x^{3}}{3} d x + c \\ & = ln ⁡ \left(\right. x \left.\right) \cdot \frac{x^{3}}{3} - \int \frac{x^{2}}{3} d x + c$$

The remaining integral is a straightforward power rule application, considerably simpler than the original. Completing the calculation we have:

$$ln ⁡ \left(\right. x \left.\right) \cdot \frac{x^{3}}{3} - \frac{x^{3}}{9} + c$$

Factoring out $\frac{x^{3}}{3}$ gives the final result in compact form:

$$\frac{x^{3}}{3} \left(\right. ln ⁡ \left(\right. x \left.\right) - \frac{1}{3} \left.\right) + c$$

## Example 2

Some integrals do not resolve after a single application of integration by parts. Instead, repeated application leads back to the original integral, a situation that, rather than signaling failure, opens the door to an algebraic resolution. The following example illustrates this technique. Solve the following integral:

$$\int e^{x} sin ⁡ \left(\right. x \left.\right) d x$$

Denote the integral by $I$:

$$I = \int e^{x} sin ⁡ \left(\right. x \left.\right) d x$$

Following the LIATE hierarchy, the trigonometric function $sin ⁡ \left(\right. x \left.\right)$ takes priority over the exponential, so we assign $u = sin ⁡ \left(\right. x \left.\right)$, $d v = e^{x} d x$ from which:

$$d u = cos ⁡ \left(\right. x \left.\right) d x$$
$$v = e^{x}$$

Applying the formula, we obtain:

$$I = e^{x} sin ⁡ \left(\right. x \left.\right) - \int e^{x} cos ⁡ \left(\right. x \left.\right) d x$$

The new integral is no simpler in structure than the original. It still involves the product of $e^{x}$ and a trigonometric function. We apply integration by parts a second time, denoting:

$$J = \int e^{x} cos ⁡ \left(\right. x \left.\right) d x$$

and assigning with the previous choice $u = cos ⁡ \left(\right. x \left.\right)$ and $d v = e^{x} d x$. We obtain:

$$d u = - sin ⁡ \left(\right. x \left.\right) d x$$
$$v = e^{x}$$

This gives:

$$J = e^{x} cos ⁡ \left(\right. x \left.\right) + \int e^{x} sin ⁡ \left(\right. x \left.\right) d x = e^{x} cos ⁡ \left(\right. x \left.\right) + I$$

The original integral $I$ has reappeared. Substituting back into the expression
for $I$:

$$I = e^{x} sin ⁡ \left(\right. x \left.\right) - \left(\right. e^{x} cos ⁡ \left(\right. x \left.\right) + I \left.\right)$$

Both occurrences of $I$ now appear on the same equation. Collecting them on
the left-hand side:

$$2 I = e^{x} sin ⁡ \left(\right. x \left.\right) - e^{x} cos ⁡ \left(\right. x \left.\right)$$

Dividing through by $2$ and adding the constant of integration:

$$I = \frac{e^{x}}{2} \left(\right. sin ⁡ \left(\right. x \left.\right) - cos ⁡ \left(\right. x \left.\right) \left.\right) + c$$

###### The key observation is that the cyclic structure transforms an apparently endless recursion into a [linear equation](https://algebrica.org/linear-equations/) in $I$, which can be solved directly. This technique applies whenever repeated integration by parts returns the original integral with a nonzero coefficient.

## Example 3

The following example illustrates the definite integral version of the formula. Compute:

$$\int_{0}^{1} x ln ⁡ \left(\right. x \left.\right) d x$$

The integrand is a product of a logarithmic function and a power of $x$. Following the LIATE hierarchy, $ln ⁡ \left(\right. x \left.\right)$ takes priority and is assigned to $f$, while $x$ is assigned to $g^{'}$:

$$f \left(\right. x \left.\right) = ln ⁡ \left(\right. x \left.\right) \rightarrow f^{'} \left(\right. x \left.\right) = \frac{1}{x}$$

$$g^{'} \left(\right. x \left.\right) = x \rightarrow g \left(\right. x \left.\right) = \frac{x^{2}}{2}$$

Applying the definite integral form of the formula:

$$\int_{0}^{1} x ln ⁡ \left(\right. x \left.\right) d x & = \left(\left[\right. \frac{x^{2}}{2} ln ⁡ \left(\right. x \left.\right) \left]\right.\right)_{0}^{1} - \int_{0}^{1} \frac{x^{2}}{2} \cdot \frac{1}{x} d x \\ & = \left(\left[\right. \frac{x^{2}}{2} ln ⁡ \left(\right. x \left.\right) \left]\right.\right)_{0}^{1} - \frac{1}{2} \int_{0}^{1} x d x$$

The boundary term requires care at $x = 0$. Since $ln ⁡ \left(\right. 1 \left.\right) = 0$ and $x^{2} ln ⁡ \left(\right. x \left.\right) \rightarrow 0$ as $x \rightarrow 0^{+}$, both endpoints vanish:

$$\left(\left[\right. \frac{x^{2}}{2} ln ⁡ \left(\right. x \left.\right) \left]\right.\right)_{0}^{1} = 0$$

The remaining integral is a standard power rule application:

$$\frac{1}{2} \int_{0}^{1} x d x = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}$$

Therefore:

$$\int_{0}^{1} x ln ⁡ \left(\right. x \left.\right) d x = - \frac{1}{4}$$

###### The [limit](https://algebrica.org/limits) $\underset{x \rightarrow 0^{+}}{lim} x^{2} ln ⁡ \left(\right. x \left.\right) = 0$ follows from the fact that [polynomial](https://algebrica.org/polynomials/) growth dominates [logarithmic](https://algebrica.org/logarithms/) decay near zero. This kind of boundary analysis is essential whenever the integrand is not defined at one of the endpoints.

## Selected references

- **Harvard University, O. Knill** . [Lecture 29: Integration by Parts](https://people.math.harvard.edu/~knill/teaching/math1a_2011/handouts/39-parts.pdf)
- **UC Berkeley, A. Vizeff**. [Lecture 3: Integration by Parts – Calculus II](https://math.berkeley.edu/~avizeff/calculus-II/lecture-3.pdf)
- **MIT, David Jerison**. [Integration by Parts](https://ocw.mit.edu/courses/18-01-single-variable-calculus-fall-2006/resources/lec30/)
- **UC Davis, D. Kouba**. [Integration by Parts – Problems and Solutions](https://www.math.ucdavis.edu/~kouba/CalcTwoDIRECTORY/intbypartsdirectory/IntByParts.html)
