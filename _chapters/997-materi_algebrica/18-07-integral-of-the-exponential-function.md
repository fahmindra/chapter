---
layout: chapter
title: "Integral of the Exponential Function"
chapter: "Integrals"
chapter_order: 18
section_order: 7
permalink: /materi-algebrica/integrals/integral-of-the-exponential-function/
---

## How the integral of the exponential function is calculated

An [exponential function](https://algebrica.org/exponential-function) is a function of the form $e^{x}$ or $\alpha^{x}$ (with $\alpha > 0$ and $\alpha \neq 1$). In general, the number $e$ occupies a central position in analysis because it is the only base for which the exponential function reproduces itself under differentiation. For a general exponential function $\alpha^{x}$ with $\alpha > 0$, differentiation introduces an unavoidable factor:

$$\frac{d}{d x} \alpha^{x} = \alpha^{x} ln ⁡ \alpha$$

That [logarithmic](https://algebrica.org/logarithms/) term reflects how the chosen base scales the growth of the function. There is exactly one case in which this extra factor disappears. If $ln ⁡ \alpha = 1$, we have:

$$\frac{d}{d x} \alpha^{x} = \alpha^{x}$$

The unique number satisfying this condition is $e \approx 2.718$. Thus $e^{x}$ is the only exponential function that remains unchanged by differentiation. The same simplicity extends to integration. This structural property explains why $e$ plays such a fundamental role.

---

Knowing how to compute the [integral](https://algebrica.org/indefinite-integrals/) of such functions is very useful in exercises involving exponential terms. We have two cases.

The integral of $e^{x}$ is given by:
$$(\text{1}) \int e^{x} d x = e^{x} + c$$
Indeed, it can be proven that the [derivative](https://algebrica.org/derivatives/) of $e^{x}$ is itself $e^{x}$.
By differentiating the integral result:
$$D \left[\right. e^{x} + c \left]\right. = D \left[\right. e^{x} \left]\right. + D \left[\right. c \left]\right. = e^{x} + 0 = e^{x}$$

##### Delve into how Euler’s number $e$ can be defined as the [limit of a known sequence](https://algebrica.org/euler-number-limit-sequence/).

---

The integral of $\alpha^{x}$ is given by:
$$(\text{2}) \int \alpha^{x} d x = \frac{1}{ln ⁡ \alpha} \cdot \alpha^{x} + c$$
In fact, we have:
$$D \left[\right. \frac{1}{ln ⁡ \alpha} \cdot \alpha^{x} + c \left]\right. = \frac{1}{ln ⁡ \alpha} \cdot \left(\right. ln ⁡ \alpha \cdot \alpha^{x} \left.\right) = \alpha^{x}$$

## Canonical forms of exponential integrals

###### Each row displays a standard exponential integrand on the left and its corresponding antiderivative on the right. These canonical patterns encompass the forms most commonly encountered in integration problems.

- $$\text{1}. \int e^{x} d x$$ $$e^{x} + c$$
- $$\text{2}. \int \alpha^{x} d x$$ $$\frac{1}{ln ⁡ \alpha} \alpha^{x} + c$$
- $$\text{3}. \int e^{a x + b} d x$$ $$\frac{1}{a} e^{a x + b} + c$$
- $$\text{4}. \int \alpha^{a x} d x$$ $$\frac{1}{a ln ⁡ \alpha} \alpha^{a x} + c$$
- $$\text{5}. \int e^{f \left(\right. x \left.\right)} f^{'} \left(\right. x \left.\right) d x$$ $$e^{f \left(\right. x \left.\right)} + c$$

Exponential functions preserve their structure under integration: the form remains unchanged, and only a multiplicative constant reflects the rate encoded in the exponent.

## Example 1

Let’s consider the following integral:
$$\int e^{x} + 3^{x} d x$$

---

By the [linearity property](https://algebrica.org/indefinite-integrals/) of the integral, the integral of a sum is equal to the sum of the integrals:

$$\int \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) d x = \int f \left(\right. x \left.\right) d x + \int g \left(\right. x \left.\right) d x$$

We have:

$$\int e^{x} + 3^{x} d x = \int e^{x} d x + \int 3^{x} d x$$

---

The first integral can be easily derived from $\left(\right. 1 \left.\right)$:
$$\int e^{x} d x = e^{x} + c$$

The second integral can be derived from $\left(\right. 2 \left.\right)$:
$$\int 3^{x} d x = \frac{1}{ln ⁡ 3} \cdot 3^{x} + c$$

Thus, our integral becomes:

$$e^{x} + \frac{1}{ln ⁡ 3} \cdot 3^{x} + c$$

## Exponential with a linear argument

In practice, the exponent is rarely just $x$. A very common situation is an exponential whose argument is a linear function $a x + b$, with $a \neq 0$. In that case we have:

$$\int e^{a x + b} d x = \frac{1}{a} e^{a x + b} + c$$

The factor $\frac{1}{a}$ compensates exactly for what the [chain rule](https://algebrica.org/the-derivative-of-a-composite-function/) introduces when differentiating. To verify:

$$D \left[\right. \frac{1}{a} e^{a x + b} + c \left]\right. = \frac{1}{a} \cdot a \cdot e^{a x + b} = e^{a x + b}$$

More generally, when the exponent is a differentiable function $f \left(\right. x \left.\right)$, [integration by substitution](https://algebrica.org/integration-by-substitution/) gives:

$$\int e^{f \left(\right. x \left.\right)} \cdot f^{'} \left(\right. x \left.\right) d x = e^{f \left(\right. x \left.\right)} + c$$

If the integrand contains an exponential $e^{f \left(\right. x \left.\right)}$ multiplied by the derivative of its own exponent, the integral collapses cleanly to $e^{f \left(\right. x \left.\right)} + c$. When $f^{'} \left(\right. x \left.\right)$ is not present, an algebraic manipulation or substitution is needed first.

---

The same reasoning based on the chain rule applies to exponential functions with an arbitrary base $\alpha$. If the exponent is $a x$ instead of just $x$, differentiation produces two factors: the coefficient $a$ from the exponent and $ln ⁡ \alpha$ from the base. For this reason we have:

$$\int \alpha^{a x} d x = \frac{1}{a ln ⁡ \alpha} \alpha^{a x} + c$$

A direct differentiation confirms the formula. This identity is useful in practice, since expressions of this type often appear in intermediate steps when simplifying more complicated integrals.

## Example 2

Let us now consider the following integral, which at first glance appears slightly more complex than the one presented in example 1.

$$\int 8^{x} \cdot 2^{\left(\right. - 3 x + 4 \left.\right)} d x$$

---

To solve it, we can take advantage of the [properties of powers](https://algebrica.org/powers/). We can rewrite:

$$2^{- 3 x + 4} = 2^{- 3 x} \cdot 2^{4} = 2^{- 3 x} \cdot 16$$

The integral then becomes:

$$16 \int 8^{x} \cdot 2^{- 3 x} d x & = 16 \int \left(\right. 2^{3} \left.\right)^{x} \cdot 2^{- 3 x} d x \\ & = 16 \int 2^{3 x} \cdot 2^{- 3 x} d x \\ & = 16 \int 2^{3 x - 3 x} d x \\ & = 16 \int 1 d x$$

We obtain:

$$16 x + c$$

## Example 3

Let’s consider the following integral:
$$\int 9^{x - 1} \cdot 3^{- x + 2} d x$$

---

We can rewrite the integral using the properties of powers:
$$\int 9^{x} \cdot 9^{- 1} \cdot 3^{- x} \cdot 3^{2} d x = \int 9^{x} \cdot 9^{- 1} \cdot 3^{- x} \cdot 9 d x$$

Simplifying the terms, we obtain:
$$\int 9^{x} \cdot 3^{- x} d x = \int 3^{2 x} \cdot 3^{- x} d x = \int 3^{x} d x$$

We have reduced the integral to the form:
$$\int \alpha^{x} d x$$

We obtain

$$\frac{1}{ln ⁡ 3} \cdot 3^{x} + c$$

## Example 4

Consider the following integral:

$$\int e^{3 x - 2} d x$$

The exponent is linear, so this is a direct application of the standard rule for exponential functions of the form $e^{a x + b}$. Since the derivative of $3 x - 2$ is $3$, we compensate by dividing by $3$.

$$\int e^{3 x - 2} d x = \frac{1}{3} e^{3 x - 2} + c$$

It is always worth checking the result. Differentiating $\frac{1}{3} e^{3 x - 2}$ gives:

$$\frac{1}{3} \cdot 3 e^{3 x - 2} = e^{3 x - 2}$$

so the computation is consistent.

The solution is:
$$\frac{1}{3} e^{3 x - 2} + c$$

## A common oversight

A frequent source of error arises when the exponent carries a coefficient. It is easy to write:

$$\int e^{3 x - 2} d x = e^{3 x - 2} + c$$

and overlook the factor $\frac{1}{3}$. The issue becomes clear as soon as one differentiates the result:

$$\frac{d}{d x} e^{3 x - 2} = 3 e^{3 x - 2}$$

which is not the original integrand but three times as large. The check takes only a moment and immediately reveals the inconsistency. Whenever the exponent has the form $a x + b$ with $a \neq 1$, the compensating factor $\frac{1}{a}$ is essential.

## Example 5

Consider now the following integral, in order to examine this new situation:

$$\int x e^{x^{2}} d x$$

Here the exponent is $x^{2}$, which is not linear, so the previous rule for $e^{a x + b}$ cannot be applied directly. However, the structure of the integrand suggests what to do. The derivative of $x^{2}$ is $2 x$, and a factor $x$ is already present. We rewrite the integral by introducing the constant:

$$\int x e^{x^{2}} d x = \frac{1}{2} \int 2 x e^{x^{2}} d x$$

Now the integrand has the form $e^{f \left(\right. x \left.\right)} f^{'} \left(\right. x \left.\right)$ with $f \left(\right. x \left.\right) = x^{2}$. In this situation, integration is immediate:

$$\frac{1}{2} e^{x^{2}} + c$$

A quick verification confirms the result. Differentiating $\frac{1}{2} e^{x^{2}}$ produces:

$$\frac{1}{2} \cdot 2 x e^{x^{2}} = x e^{x^{2}}$$

which matches the original integrand.

The solution is:
$$\frac{1}{2} e^{x^{2}} + c$$

## When the matching factor is missing

It is useful to notice what happens if the factor $x$ is removed. The integral:

$$\int e^{x^{2}} d x$$

does not have an antiderivative that can be written using elementary functions. Instead, it is expressed in terms of the error function $erf \left(\right. x \left.\right)$. It is defined by the integral:

$$erf \left(\right. x \left.\right) = \frac{2}{\sqrt{\pi}} \int_{0}^{x} e^{- t^{2}} d t$$

Unlike elementary functions such as polynomials, exponentials, or trigonometric functions, $erf \left(\right. x \left.\right)$ is defined directly through an integral. It was introduced precisely because integrals of the form $\int e^{- t^{2}} d t$ cannot be expressed in closed elementary form.

This shows that the factor $x$ in the previous example provided, up to a constant, the derivative of the exponent $x^{2}$. Without that match, the simple structure disappears and the integral can no longer be handled with the same elementary tools.

## Selected references

- **University of California, Davis – L. Kouba**. [Integration of Exponential Functions](https://www.math.ucdavis.edu/~kouba/CalcTwoDIRECTORY/expondirectory/Exponentials.html)
- **MIT, G. Strang**. [Calculus – Chapter 6: Exponentials and Logarithms](https://ocw.mit.edu/ans7870/textbooks/Strang/Edited/Calculus/6.pdf)
- **University of Wisconsin–Madison, S. Angenent**. [MATH 222 – Second Semester Calculus](https://people.math.wisc.edu/~angenent/222.2013s/UWMath222_2013s.pdf)
- **University of Chicago, V. Jayaram**. [Proving the Non-Existence of Elementary Anti-Derivatives](http://math.uchicago.edu/~may/REU2017/REUPapers/Jayaram.pdf)
