---
layout: chapter
title: "Integral of Trigonometric Functions"
chapter: "Integrals"
chapter_order: 18
section_order: 8
permalink: /materi-algebrica/integrals/integral-of-trigonometric-functions/
---

## Integrals of the fundamental trigonometric functions

In the section on [functions](https://algebrica.org/functions/), you’ll find the integrals of the main trigonometric functions (for example [sine](https://algebrica.org/sine-function/), [cosine](https://algebrica.org/cosine-function/), [tangent](https://algebrica.org/tangent-function/), [cotangent](https://algebrica.org/cotangent-function/), and the others. These integrals are easy to compute and worth keeping in mind, as they often appear when solving problems. Below is a summary list of the integrals of all the main trigonometric functions, offering an immediate overall view of the essential results.

- $$\text{1}. \int sin ⁡ x d x = - cos ⁡ x + c$$
- $$\text{2}. \int cos ⁡ x d x = sin ⁡ x + c$$
- $$\text{3}. \int tan ⁡ x d x = - ln ⁡ \left|\right. cos ⁡ x \left|\right. + c$$
- $$\text{4}. \int cot ⁡ x d x = ln ⁡ \left|\right. sin ⁡ x \left|\right. + c$$
- $$\text{5}. \int sec ⁡ x d x = ln ⁡ \left|\right. sec ⁡ x + tan ⁡ x \left|\right. + c$$
- $$\text{6}. \int csc ⁡ x d x = ln ⁡ \left|\right. csc ⁡ x - cot ⁡ x \left|\right. + c$$
- $$\text{7}. \int sinh ⁡ x d x = cosh ⁡ x + c$$
- $$\text{8}. \int cosh ⁡ x d x = sinh ⁡ x + c$$
- $$\text{9}. \int tanh ⁡ x d x = ln ⁡ \left|\right. cosh ⁡ x \left|\right. + c$$
- $$\text{10}. \int coth ⁡ x d x = ln ⁡ \left|\right. sinh ⁡ x \left|\right. + c$$
- $$\text{11}. \int sech x d x = 2 arctan \left(\right. tanh ⁡ \frac{x}{2} \left.\right) + c$$
- $$\text{12}. \int csch x d x = ln ⁡ \left|\right. tanh ⁡ \frac{x}{2} \left|\right. + c$$

##### Remember that $c$ denotes the constant of integration, which is included to represent the entire family of antiderivatives associated with an [indefinite integral](https://algebrica.org/indefinite-integrals/). Each value of $c$ corresponds to a different primitive, all of which share the same derivative.

## Integrals of trigonometric powers with $n$ even

There are, however, some important cases in which the antiderivative is not immediately accessible and requires a simple strategy to be handled effectively. Situations of this kind occur frequently in exercises and problem-solving. A classic example arises when sine or cosine appears raised to an integer power, namely:

$$\int sin^{n} ⁡ x d x$$
$$\int cos^{n} ⁡ x d x$$

In these situations, the integral can be greatly simplified by applying appropriate substitutions. When the exponent $n$ is even, one typically rewrites the squared trigonometric terms using the double-angle identities. In particular, we have:

$$sin^{2} ⁡ x = \frac{1 - cos ⁡ 2 x}{2}$$
$$cos^{2} ⁡ x = \frac{1 + cos ⁡ 2 x}{2}$$

These expressions reduce the power of the function and allow the integral to be computed more easily, and follow directly from following relationships. Starting from the [Pythagorean identity](https://algebrica.org/pythagorean-identity/):
$$sin^{2} ⁡ x + cos^{2} ⁡ x = 1$$
and combining it with the [double–angle formula](https://algebrica.org/trigonometric-identities/):
$$cos ⁡ 2 x = cos^{2} ⁡ x - sin^{2} ⁡ x$$
we can express $cos ⁡ 2 x$ entirely in terms of either $cos^{2} ⁡ x$ or $sin^{2} ⁡ x$.

---

Indeed, replacing $sin^{2} ⁡ x$ with $1 - cos^{2} ⁡ x$ we obtain:
$$cos ⁡ 2 x = cos^{2} ⁡ x - \left(\right. 1 - cos^{2} ⁡ x \left.\right) = 2 cos^{2} ⁡ x - 1$$
Solving this expression for $cos^{2} ⁡ x$ yields:
$$cos^{2} ⁡ x = \frac{1 + cos ⁡ 2 x}{2}$$

---

A similar argument holds for $sin^{2} ⁡ x$. If we substitute $cos^{2} ⁡ x = 1 - sin^{2} ⁡ x$ into the double–angle formula, we get:
$$cos ⁡ 2 x = \left(\right. 1 - sin^{2} ⁡ x \left.\right) - sin^{2} ⁡ x = 1 - 2 sin^{2} ⁡ x$$
Solving for $sin^{2} ⁡ x$ gives:
$$sin^{2} ⁡ x = \frac{1 - cos ⁡ 2 x}{2}$$

## Example 1

As an illustration of the method, let us consider the following integral:
$$\int 2 cos^{4} ⁡ x d x$$

---

To handle the fourth power of the cosine, we start by recalling the power-reducing identity:
$$cos^{2} ⁡ x = \frac{1 + cos ⁡ 2 x}{2}$$

Applying this identity allows us to rewrite the expression in a more manageable form:
$$cos^{4} ⁡ x & = \left(\left(\right. \frac{1 + cos ⁡ 2 x}{2} \left.\right)\right)^{2} \\ & = \frac{1}{4} \left(\right. 1 + 2 cos ⁡ 2 x + cos^{2} ⁡ 2 x \left.\right)$$

---

At this point, one power of cosine still remains. We therefore reduce it using the identity:
$$cos^{2} ⁡ 2 x = \frac{1 + cos ⁡ 4 x}{2}$$

Substituting this expression back into the formula and multiplying by 2 (as required by the original integral), we obtain the simplified form:
$$2 cos^{4} ⁡ x = \frac{3}{4} + cos ⁡ 2 x + \frac{1}{4} cos ⁡ 4 x$$

Finally, by integrating each term separately, we obtain the solution:

$$\frac{3}{4} x + \frac{1}{2} sin ⁡ 2 x + \frac{1}{16} sin ⁡ 4 x + c$$

## Integrals of trigonometric powers with $n$ odd

When the exponent $n$ is odd, the method becomes straightforward. In this case we can separate one factor of the trigonometric function whose power is odd and rewrite the remaining even power using the Pythagorean identity. For sine, this gives:
$$\int sin^{n} ⁡ x d x & = \int sin ⁡ x \left(\right. sin^{2} ⁡ x \left.\right)^{k} , d x \\ & = \int sin ⁡ x \left(\right. 1 - cos^{2} ⁡ x \left.\right)^{k} d x$$

The following [substitution](https://algebrica.org/integration-by-substitution/):
$$u = cos ⁡ x$$
$$d u = - sin ⁡ x d x$$

transforms the integral into a [polynomial](https://algebrica.org/polynomials) in $u$, which can then be integrated without difficulty. The procedure for an odd power of cosine is entirely analogous: one extracts a single $cos ⁡ x$ and rewrites the remaining even power using
$$cos^{2} ⁡ x = 1 - sin^{2} ⁡ x$$
leading to the substitution $u = sin ⁡ x$. In both cases, isolating one factor reduces the integral to a much simpler form.

## Example 2

Consider the following integral:

$$\int cos^{5} ⁡ x d x$$

The exponent is odd, so the strategy is to isolate one factor of cosine and rewrite the remaining even [power](https://algebrica.org/powers/) using the Pythagorean identity. We write:

$$\int cos^{5} ⁡ x , d x = \int cos^{4} ⁡ x \cdot cos ⁡ x d x$$

The factor $cos^{4} ⁡ x$ is an even power, so we can express it in terms of $sin^{2} ⁡ x$:

$$cos^{4} ⁡ x = \left(\right. cos^{2} ⁡ x \left.\right)^{2} = \left(\right. 1 - sin^{2} ⁡ x \left.\right)^{2}$$

The integral becomes:

$$\int \left(\right. 1 - sin^{2} ⁡ x \left.\right)^{2} \cdot cos ⁡ x d x$$

At this point the factor $cos ⁡ x d x$ is exactly the differential of $sin ⁡ x$, so we set:

$$u = sin ⁡ x d u = cos ⁡ x d x$$

and the integral transforms into a [polynomial](https://algebrica.org/polynomials/) in $u$:

$$\int \left(\right. 1 - u^{2} \left.\right)^{2} d u$$

Expanding the square we obtain:

$$\int \left(\right. 1 - 2 u^{2} + u^{4} \left.\right) d u$$

Each term integrates immediately:

$$u - \frac{2}{3} u^{3} + \frac{1}{5} u^{5} + c$$

Substituting back $u = sin ⁡ x$ we have::

$$sin ⁡ x - \frac{2}{3} sin^{3} ⁡ x + \frac{1}{5} sin^{5} ⁡ x + c$$

###### The substitution worked cleanly because the isolated factor $cos ⁡ x$ was precisely the derivative of $u = sin ⁡ x$. Recognising this pattern is what makes the odd-exponent case straightforward once the logic is in place.

## Reciprocals of sine and cosine

Other frequently encountered cases involve the integrals of the reciprocals of sine and cosine. Although these expressions may seem less straightforward at first glance, both can be derived with a single algebraic trick. For the secant, the key idea is to multiply the integrand by a fraction equal to 1:

$$\int sec ⁡ x d x & = \int sec ⁡ x \cdot \frac{sec ⁡ x + tan ⁡ x}{sec ⁡ x + tan ⁡ x} d x \\ & = \int \frac{sec^{2} ⁡ x + sec ⁡ x tan ⁡ x}{sec ⁡ x + tan ⁡ x} d x$$

The numerator is now exactly the derivative of the denominator, since:

$$\frac{d}{d x} \left(\right. sec ⁡ x + tan ⁡ x \left.\right) = sec ⁡ x tan ⁡ x + sec^{2} ⁡ x$$

This means the integral has the form $\int \frac{f^{'} \left(\right. x \left.\right)}{f \left(\right. x \left.\right)} d x$, which integrates directly to $ln ⁡ \left|\right. f \left(\right. x \left.\right) \left|\right.$. We obtain:

$$\int \frac{1}{cos ⁡ x} d x = \int sec ⁡ x , d x = ln ⁡ \left|\right. sec ⁡ x + tan ⁡ x \left|\right. + c$$

---

The same structure applies to the cosecant. Multiplying by $\frac{csc ⁡ x - cot ⁡ x}{csc ⁡ x - cot ⁡ x}$ gives a numerator that is the derivative of the denominator, since:

$$\frac{d}{d x} \left(\right. csc ⁡ x - cot ⁡ x \left.\right) = - csc ⁡ x cot ⁡ x + csc^{2} ⁡ x$$

and the integral of $csc ⁡ x$ produces:

$$\int \frac{1}{sin ⁡ x} d x = \int csc ⁡ x d x = ln ⁡ \left|\right. csc ⁡ x - cot ⁡ x \left|\right. + c$$

In both cases the result is [logarithmic](https://algebrica.org/logarithms/), and the sign inside the [absolute value](https://algebrica.org/absolute-value/) is easy to mix up. It is worth memorising the two forms together: $sec ⁡ x + tan ⁡ x$ for the cosine reciprocal, $csc ⁡ x - cot ⁡ x$ for the sine reciprocal.

## Selected references

- **University of British Columbia, J. Feldman**. [Trigonometric Integrals](https://personal.math.ubc.ca/~feldman/m105/intTrig.pdf)
- **University of British Columbia, L. Silberman**. [Integrating the Secant Function](https://personal.math.ubc.ca/~lior/teaching/1516/101_W16/Notes/IntSecant.pdf)
- **University of Toronto, I. Khatchatourian**. [Trigonometric Integrals](https://www.math.utoronto.ca/ivan/mat137/docs_1617/ivan_lecture205_student.pdf)
- **Columbia University, P. Woit**. [Euler’s Formula and Trigonometry](https://www.math.columbia.edu/~woit/eulerformula.pdf)
