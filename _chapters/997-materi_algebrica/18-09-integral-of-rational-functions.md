---
layout: chapter
title: "Integral of Rational Functions"
chapter: "Integrals"
chapter_order: 18
section_order: 9
permalink: /materi-algebrica/integrals/integral-of-rational-functions/
---

## Integration of rational functions with polynomial division

Let’s see how we can proceed to calculate the [integral](https://algebrica.org/indefinite-integral) of rational functions of the form:

$$\int \frac{N \left(\right. x \left.\right)}{D \left(\right. x \left.\right)} d x$$

where $N \left(\right. x \left.\right)$ and $D \left(\right. x \left.\right)$ are [polynomials](https://algebrica.org/polynomials/). When solving this type of integrals, we may encounter different scenarios. Let’s examine the case where the degree of $N \left(\right. x \left.\right)$ is greater than the degree of $D \left(\right. x \left.\right)$.

---

From the properties of polynomials, we know that it is always possible to perform the [division of a polynomial](https://algebrica.org/polynomial-division/) $P \left(\right. x \left.\right)$ by another polynomial $D \left(\right. x \left.\right)$. This division yields:

- A quotient polynomial $Q \left(\right. x \left.\right)$.
- A remainder polynomial $R \left(\right. x \left.\right)$, where the degree of $R \left(\right. x \left.\right)$ is strictly less than the degree of $D \left(\right. x \left.\right)$.

This process leads us to obtain a polynomial in the form:
$$N \left(\right. x \left.\right) = Q \left(\right. x \left.\right) D \left(\right. x \left.\right) + R \left(\right. x \left.\right)$$

Dividing both sides by $D \left(\right. x \left.\right)$, we obtain:
$$\frac{N \left(\right. x \left.\right)}{D \left(\right. x \left.\right)} = Q \left(\right. x \left.\right) + \frac{R \left(\right. x \left.\right)}{D \left(\right. x \left.\right)}$$

If we compute the integral, we obtain:
$$\int \frac{N \left(\right. x \left.\right)}{D \left(\right. x \left.\right)} d x = \int Q \left(\right. x \left.\right) d x + \int \frac{R \left(\right. x \left.\right)}{D \left(\right. x \left.\right)} d x$$

---

What guides the choice of method is the comparison between the degrees of the numerator and
the denominator. If $deg ⁡ N \left(\right. x \left.\right) \geq deg ⁡ D \left(\right. x \left.\right)$, the rational function is improper and
must first be reduced by polynomial long division. Only after this preliminary step does the
integral take a manageable form.

If instead $deg ⁡ N \left(\right. x \left.\right) < deg ⁡ D \left(\right. x \left.\right)$, the rational function is already proper, and
attention shifts to the factorization of the denominator. Its algebraic structure dictates
the technique:

- when the denominator is a single linear factor, a simple substitution typically settles the integral immediately;
- when it splits into distinct linear factors, decomposing into partial fractions converts the expression into a sum of elementary terms;
- when a linear factor is repeated, each power of that factor generates its own term in the decomposition, forming a small hierarchy of fractions;
- when an irreducible quadratic factor is present, the path runs through completing the square and naturally leads to an inverse tangent term.

Once the rational function has been reduced to the proper case, the denominator governs the entire strategy. Its factorization over the real numbers determines the structure of the partial fraction decomposition. Integration then becomes a systematic reduction to logarithmic and inverse trigonometric primitives.

## Example 1

Let’s compute the integral of the rational function:

$$\int \frac{x^{3} + x + 1}{x^{2} + 1} d x$$

First, we proceed with the division between the numerator and the denominator, obtaining:

$$+ x^{3} & + x & + 1 & + x^{2} & + 1 \\ - x^{3} & - x & & + x & \\ // & // & + 1$$

From the division, we obtain:
$$Q \left(\right. x \left.\right) = x R \left(\right. x \left.\right) = 1$$

##### To learn more about the method of dividing two polynomials, refer to the relevant section on [polynomials](https://algebrica.org/polynomials).

---

We can rewrite our integral as:

$$\int \frac{x^{3} + x + 1}{x^{2} + 1} d x = \int x d x + \int \frac{1}{x^{2} + 1} d x$$

Solving the integral, we obtain:

$$\frac{x^{2}}{2} + arctan ⁡ \left(\right. x \left.\right) + c$$

## Integrals with linear denominators

In the case where the degree of $N \left(\right. x \left.\right)$ is less than the degree of $D \left(\right. x \left.\right)$, and the denominator is of first degree, we have integrals of the form:

$$\int \frac{c}{a x + b} d x$$

These integrals can be solved by [substitution](https://algebrica.org/integration-by-substitution/).

## Example 2

Let’s compute the integral of the rational function:

$$\int \frac{2}{6 x + 1} d x$$

---

Let’s apply the substitution $t = 6 x + 1$. Then, we have:

$$\frac{d t}{d x} = 6 \rightarrow d x = \frac{d t}{6}$$

Replacing these into the integral, we obtain:

$$\int \frac{2}{6 x + 1} d x = \int \frac{2}{t} \cdot \frac{d t}{6} = \frac{2}{6} \int \frac{1}{t} d t = \frac{1}{3} \int \frac{1}{t} d t$$

Now, we can proceed to integrate with respect to $t$. We have:

$$\frac{1}{3} \int \frac{1}{t} d t = \frac{1}{3} \cdot ln ⁡ \left|\right. t \left|\right. + c$$

By substituting the original value of $t$, we obtain:
$$\frac{1}{3} ln ⁡ \left|\right. 6 x + 1 \left|\right. + c$$

## Partial fraction decomposition

In many situations, the integral of a rational function cannot be computed directly by inspection. Even when the expression appears relatively simple, algebraic manipulations may not reveal an immediate antiderivative. In such cases, the method of [partial fraction decomposition](https://algebrica.org/partial-fraction-decomposition/) provides a systematic way to rewrite the function as a sum of elementary terms whose integrals are well known. By decomposing the rational function into simpler components, we obtain a representation that is far more suitable for integration. To illustrate the idea in a setting different from the earlier examples, consider the integral:

$$\int \frac{7 x + 5}{\left(\right. x - 1 \left.\right) \left(\right. 3 x + 2 \left.\right)} d x$$

At first glance, the structure of this expression does not suggest an obvious primitive. However, once we decompose the integrand into partial fractions, the computation becomes straightforward. We begin by writing

$$(\text{1}) \frac{7 x + 5}{\left(\right. x - 1 \left.\right) \left(\right. 3 x + 2 \left.\right)} = \frac{A}{x - 1} + \frac{B}{3 x + 2}$$

Multiplying both sides by $\left(\right. x - 1 \left.\right) \left(\right. 3 x + 2 \left.\right)$ yields the identity:

$$7 x + 5 = A \left(\right. 3 x + 2 \left.\right) + B \left(\right. x - 1 \left.\right)$$

which allows us to determine the coefficients $A$ and $B$. Evaluating at the convenient values $x = 1$ and $x = - 2 / 3$, we obtain:

$$A = 4 B = - 5$$

Thus, by substituting the values obtained into identity $1$, we obtain:

$$\frac{7 x + 5}{\left(\right. x - 1 \left.\right) \left(\right. 3 x + 2 \left.\right)} = \frac{4}{x - 1} - \frac{5}{3 x + 2}$$

At this point the integral becomes:

$$\int \left(\right. \frac{4}{x - 1} - \frac{5}{3 x + 2} \left.\right) d x$$

and by the [linearity of the integral](https://algebrica.org/indefinite-integrals/) we may treat each term separately:

$$4 \int \frac{1}{x - 1} d x$$
$$5 \int \frac{1}{3 x + 2} d x$$

Both integrals reduce to elementary [logarithmic](https://algebrica.org/logarithms/) forms:

$$4 ln ⁡ \left|\right. x - 1 \left|\right. + c_{1}$$
$$\frac{5}{3} ln ⁡ \left|\right. 3 x + 2 \left|\right. + c_{2}$$

Combining the constants and simplifying, we obtain the antiderivative:

$$4 ln ⁡ \left|\right. x - 1 \left|\right. - \frac{5}{3} ln ⁡ \left|\right. 3 x + 2 \left|\right. + c$$

##### This example shows how a rational function that initially presents no clear path to integration becomes entirely tractable once rewritten in partial fractions. The method transforms the integral into a collection of standard forms, making the computation both systematic and transparent.

## Irreducible quadratic factors in the denominator

Not every polynomial splits into linear factors over the real numbers. A quadratic expression $a x^{2} + b x + c$ whose [discriminant](https://algebrica.org/quadratic-formula) satisfies $b^{2} - 4 a c < 0$ has no real roots. In concrete terms, this means it cannot be written as $\left(\right. x - r_{1} \left.\right) \left(\right. x - r_{2} \left.\right)$ with $r_{1} , r_{2} \in \mathbb{R}$.

Over the real field, such a quadratic is said to be irreducible. When a factor of this type appears in the denominator of a [rational function](https://algebrica.org/rational-functions/), the strategy for partial fraction decomposition changes slightly. In the linear case, each factor $\left(\right. x - r \left.\right)$ gives rise to a term of the form:

$$\frac{A}{x - r}$$

Here there are no real roots to attach such terms to. The quadratic must therefore remain intact in the denominator. For this reason, an irreducible quadratic factor $a x^{2} + b x + c$ contributes a term of the form:

$$\frac{A x + B}{a x^{2} + b x + c}$$

The numerator must have degree strictly smaller than the denominator, and in the quadratic case that means degree one. Using only a constant would not provide enough flexibility to match the original rational function. Once the decomposition is complete, integration typically proceeds by rewriting the quadratic denominator through [completing the square](https://algebrica.org/completing-the-square/). After an appropriate change of variable, one arrives at an expression of the type:

$$\int \frac{1}{u^{2} + a^{2}} d u$$

whose antiderivative is

$$\frac{1}{a} arctan \left(\right. \frac{u}{a} \left.\right) + c$$

The appearance of the [arctangent](https://algebrica.org/arctangent-and-arccotangent/) reflects the geometric structure encoded in the expression $u^{2} + a^{2}$, which cannot vanish over the real numbers and corresponds, analytically, to the derivative of the inverse [tangent function](https://algebrica.org/tangent-function/).

## Example 3

Consider the following integral:

$$\int \frac{5 x^{2} + 3 x - 2}{\left(\right. x + 1 \left.\right) \left(\right. x^{2} + 2 x + 3 \left.\right)} d x$$

The denominator is already written as a product. One factor, $x + 1$, is linear. The other, $x^{2} + 2 x + 3$, deserves a closer look. Its discriminant is:

$$\Delta = 2^{2} - 4 \cdot 1 \cdot 3 = 4 - 12 = - 8 < 0$$

so it has no real zeros and is irreducible over $\mathbb{R}$. This immediately determines the shape of the partial fraction decomposition:

$$\frac{5 x^{2} + 3 x - 2}{\left(\right. x + 1 \left.\right) \left(\right. x^{2} + 2 x + 3 \left.\right)} = \frac{A}{x + 1} + \frac{B x + C}{x^{2} + 2 x + 3}$$

We now clear denominators by multiplying both sides by $\left(\right. x + 1 \left.\right) \left(\right. x^{2} + 2 x + 3 \left.\right)$. This produces the identity:

$$5 x^{2} + 3 x - 2 = A \left(\right. x^{2} + 2 x + 3 \left.\right) + \left(\right. B x + C \left.\right) \left(\right. x + 1 \left.\right)$$

A convenient first step is to evaluate at $x = - 1$. At that value the second term vanishes, and we obtain:

$$5 \left(\right. - 1 \left.\right)^{2} + 3 \left(\right. - 1 \left.\right) - 2 = A \left(\right. \left(\right. - 1 \left.\right)^{2} + 2 \left(\right. - 1 \left.\right) + 3 \left.\right)$$

The left-hand side simplifies to $5 - 3 - 2 = 0$, while the right-hand side becomes $A \left(\right. 1 - 2 + 3 \left.\right) = 2 A$. Hence $0 = 2 A$, so:

$$A = 0$$

With $A = 0$, the identity reduces to:

$$5 x^{2} + 3 x - 2 = \left(\right. B x + C \left.\right) \left(\right. x + 1 \left.\right)$$

Expanding the right-hand side gives:

$$\left(\right. B x + C \left.\right) \left(\right. x + 1 \left.\right) = B x^{2} + \left(\right. B + C \left.\right) x + C$$

Matching coefficients term by term, we find:

$$B = 5 B + C = 3$$

From the second relation, $C = - 2$. The decomposition therefore collapses to:

$$\frac{5 x^{2} + 3 x - 2}{\left(\right. x + 1 \left.\right) \left(\right. x^{2} + 2 x + 3 \left.\right)} = \frac{5 x - 2}{x^{2} + 2 x + 3}$$

The integral has simplified considerably:

$$\int \frac{5 x - 2}{x^{2} + 2 x + 3} d x$$

At this point, the standard strategy is to relate the numerator to the derivative of the denominator. Since:

$$\frac{d}{d x} \left(\right. x^{2} + 2 x + 3 \left.\right) = 2 x + 2$$

we rewrite the numerator as a combination of this derivative and a constant:

$$5 x - 2 = \frac{5}{2} \left(\right. 2 x + 2 \left.\right) - 7$$

The integral splits accordingly:

$$\frac{5}{2} \int \frac{2 x + 2}{x^{2} + 2 x + 3} d x - 7 \int \frac{1}{x^{2} + 2 x + 3} d x$$

---

First part: here the numerator is exactly the derivative of the denominator. This produces a [logarithm](https://algebrica.org/logarithms/):

$$\frac{5}{2} ln ⁡ \left|\right. x^{2} + 2 x + 3 \left|\right.$$

Because the quadratic has negative discriminant, it is always positive, so the [absolute value](https://algebrica.org/absolute-value/) is not strictly necessary, though keeping it causes no harm.

---

Second part: we complete the square $x^{2} + 2 x + 3 = \left(\right. x + 1 \left.\right)^{2} + 2$ thus:

$$- 7 \int \frac{1}{\left(\right. x + 1 \left.\right)^{2} + 2} d x$$

With the substitution $u = x + 1$ and $a^{2} = 2$, we obtain

$$- \frac{7}{\sqrt{2}} arctan \left(\right. \frac{x + 1}{\sqrt{2}} \left.\right)$$

Putting everything together, an antiderivative is:

$$\frac{5}{2} ln ⁡ \left(\right. x^{2} + 2 x + 3 \left.\right) - \frac{7}{\sqrt{2}} arctan \left(\right. \frac{x + 1}{\sqrt{2}} \left.\right) + c$$

##### The factor $x + 1$ initially appears to require its own term in the decomposition. Yet, once the coefficients are computed, that contribution disappears entirely. For this reason, the full decomposition must always be written down: what seems essential at first may ultimately cancel.

## Selected references

- **MIT H. Miller, J. Orloff**. [Partial Fractions and the Coverup Method](https://math.mit.edu/~hrm/18.031/pf-coverup.pdf)
- **Harvard University, O. Knill**. [Partial Fractions](https://people.math.harvard.edu/~knill/teaching/math1a2024/handouts/lecture30.pdf)
- **UC Davis, D. Kouba**. [Integration by Partial Fractions](https://www.math.ucdavis.edu/~kouba/CalcTwoDIRECTORY/partialfracdirectory/PartialFrac.html)
