---
layout: chapter
title: "Integration by Substitution"
chapter: "Integrals"
chapter_order: 18
section_order: 4
permalink: /materi-algebrica/integrals/integration-by-substitution/
---

## How substitution simplifies integration

**Integration by substitution** is a technique used to simplify an integral by introducing a suitable substitution. When the [integral](https://algebrica.org/indefinite-integrals/) is not straightforward to compute, this method proves highly useful as it allows rewriting the integral of a function $f \left(\right. x \left.\right)$ in terms of a new variable $u$, simplifying the computation:

$$\int f \left(\right. g \left(\right. x \left.\right) \left.\right) g^{'} \left(\right. x \left.\right) d x = \int f \left(\right. u \left.\right) d u$$

The process involves the following steps:

- Introduce a change of variable by defining $u = g \left(\right. x \left.\right)$, where $g \left(\right. x \left.\right)$ is an appropriately chosen function.
- Compute the differential transformation, given by $d u = g^{'} \left(\right. x \left.\right) d x .$
- Rewrite the integral in terms of $u$, replacing $x$ and $d x$ accordingly, to obtain an equivalent expression that is often more straightforward to solve.
- Once the integral is evaluated, revert to the original variable $x$ to express the final result in its initial form.

###### The key insight is that substitution reverses the chain rule: recognizing this connection makes it easier to identify when and how to apply the technique.

The method of substitution is a direct consequence of the [chain rule](https://algebrica.org/the-derivative-of-a-composite-function/) for derivatives. If $F \left(\right. x \left.\right) = H \left(\right. g \left(\right. x \left.\right) \left.\right)$, then by the chain rule:

$$F^{'} \left(\right. x \left.\right) = H^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) g^{'} \left(\right. x \left.\right) .$$

Therefore, whenever an integrand has the form $H^{'} \left(\right. g \left(\right. x \left.\right) \left.\right) g^{'} \left(\right. x \left.\right)$ it is the derivative of the composite function $H \left(\right. g \left(\right. x \left.\right) \left.\right)$. Integration by substitution simply reverses this process by introducing $u = g \left(\right. x \left.\right)$, reducing the integral to:

$$\int H^{'} \left(\right. u \left.\right) d u = H \left(\right. u \left.\right) + c .$$

## Recognizing when to use substitution

Before proceeding to concrete examples, it is useful to understand when a substitution is likely to be effective. The technique is most natural when the integrand contains a [composite function](https://algebrica.org/composite-functions/). In many cases, the integral has the general form:

$$f \left(\right. g \left(\right. x \left.\right) \left.\right) g^{'} \left(\right. x \left.\right)$$

or differs from it only by a constant factor. When this pattern appears, choosing $u = g \left(\right. x \left.\right)$ simplifies the expression by reducing the composite structure to a single variable. A common signal is the presence of expressions such as $\left(\right. a x + b \left.\right)^{n}$, $\sqrt{a x + b}$, $ln ⁡ \left(\right. a x + b \left.\right)$ or $e^{a x + b}$. In these cases, the inner linear function $a x + b$ is often a natural candidate for substitution. Similarly, in rational expressions of the form:

$$\frac{g^{'} \left(\right. x \left.\right)}{g \left(\right. x \left.\right)}$$

the [derivative](https://algebrica.org/derivatives) of the denominator suggests the substitution $u = g \left(\right. x \left.\right)$.

##### In practice, the key idea is to look for an inner expression whose derivative also appears, exactly or up to a multiplicative constant, elsewhere in the integrand. When such a relationship is present, substitution typically transforms the integral into a simpler and more manageable form.

## Substitution patterns

|  |  |
| --- | --- |
| $$\int f \left(\right. g \left(\right. x \left.\right) \left.\right) g^{'} \left(\right. x \left.\right) d x$$ | $$u = g \left(\right. x \left.\right)$$ |
| $$\int \left(\right. a x + b \left.\right)^{n} d x$$ | $$u = a x + b$$ |
| $$\int e^{a x + b}$$ | $$u = a x + b$$ |
| $$\int ln ⁡ \left(\right. a x + b \left.\right) d x$$ | $$u = a x + b$$ |
| $$\int \frac{g^{'} \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} d x$$ | $$u = g \left(\right. x \left.\right)$$ |

## Example 1

Let’s consider the following integral:

$$\int \left(\right. 2 x + 1 \left.\right)^{3} d x$$

---

Let $u = 2 x + 1$, which simplifies the [exponentiation](https://algebrica.org/exponential-function). Differentiating both sides with respect to $x$ we have:
$$d u = 2 d x$$

Solving for $d x$ we obtain:
$$d x = \frac{d u}{2}$$

---

Expressing the integral entirely in terms of $u$:

$$\int u^{3} \cdot \frac{d u}{2} = \frac{1}{2} \int u^{3} d u$$

We now proceed to solve the integral in $u$, which has been reduced to a basic integral of the form $x^{a}$. We obtain:

$$\frac{1}{2} \cdot \frac{u^{4}}{4} + c = \frac{1}{8} u^{4} + c$$

Substituting back $u = 2 x + 1$, we get the final solution:

$$\frac{1}{8} \left(\right. 2 x + 1 \left.\right)^{4} + c$$

## Example 2

Let’s consider another example by evaluating the following integral.

$$\int \frac{1}{3 x - 5} d x$$

---

Let $u = 3 x - 5$, which simplifies the denominator. Differentiating both sides with respect to $x$, we have:
$$d u = 3 d x$$

Solving for $d x$, we obtain:
$$d x = \frac{d u}{3}$$

---

Expressing the integral entirely in terms of $u$:

$$\int \frac{1}{u} \cdot \frac{d u}{3} = \frac{1}{3} \int \frac{d u}{u}$$

We now proceed to solve the integral in $u$, which has been reduced to a basic integral of the form $1 / x$. We obtain:

$$\frac{1}{3} ln ⁡ \left|\right. u \left|\right. + c$$

Substituting back $u = 3 x - 5$, we get the final result:

$$\frac{1}{3} ln ⁡ \left|\right. 3 x - 5 \left|\right. + c$$

##### As shown in the examples above, integration by substitution is an effective technique, but selecting the right substitution requires practice and the ability to recognize the structure of the integrand.

## Example 3

Let’s consider another example by evaluating the following integral:
$$\int x sin ⁡ \left(\right. x^{2} \left.\right) d x$$

---

At first, identifying an appropriate substitution to facilitate the evaluation of the integral may not be straightforward. However, we will proceed systematically to transform the given integral into a more manageable form and obtain the desired result. Let $u = x^{2}$, which simplifies the argument of the sine function. Differentiating both sides with respect to $x$, we get:
$$d u = 2 x d x$$

Solving for $d x$ we obtain:
$$d x = \frac{d u}{2 x}$$

---

Rewriting everything in terms of $u$, and since $d u = 2 x d x$, we have:

$$\int x sin ⁡ \left(\right. u \left.\right) \cdot \frac{d u}{2 x} = \frac{1}{2} \int sin ⁡ \left(\right. u \left.\right) d u$$

---

We now proceed to solve the integral in $u$, which has been reduced to a basic integral of the form $sin ⁡ u$:

$$\int sin ⁡ u d u = - cos ⁡ u$$

Thus:

$$\frac{1}{2} \left(\right. - cos ⁡ u \left.\right) + c = - \frac{1}{2} cos ⁡ u + c$$

Substituting back $u = x^{2}$, we obtain the final result:

$$- \frac{1}{2} cos ⁡ \left(\right. x^{2} \left.\right) + c$$

## Example 4

Let’s consider the following integral:
$$\int cos ⁡ x \sqrt{sin ⁡ x} d x$$

---

Let $u = sin ⁡ x$, which simplifies the square root term. Differentiating both sides with respect to $x$, we get:

$$d u = cos ⁡ x d x$$

Since $d u = cos ⁡ x d x$, we can directly substitute into the integral.

---

Substituting $u = sin ⁡ x$ and $d u = cos ⁡ x d x$ directly into the integral, we obtain:

$$\int \sqrt{u} d u = \int u^{1 / 2} d u$$

We have thus transformed the integral into a simple form of the type $x^{a}$.

---

We now proceed to compute the integral:

$$\int u^{1 / 2} d u = \frac{u^{3 / 2}}{\frac{3}{2}} = \frac{2}{3} u^{3 / 2} + c$$

Substituting back $u = sin ⁡ x$, we obtain the final result:

$$\frac{2}{3} \left(\right. sin ⁡ x \left.\right)^{3 / 2} + c$$

## Trigonometric substitutions

Let’s make things a bit more challenging and analyze the case where it is convenient to perform a [trigonometric substitution](https://algebrica.org/trigonometric-substitution-for-integrals/) to simplify an integral involving [polynomial](https://algebrica.org/polynomials), [rational](https://algebrica.org/rational-functions/), or algebraic expressions. This step is less intuitive; however, understanding it allows us to reduce seemingly more complex integrals to a simplified form. In general, this type of substitution is particularly useful when the integral contains a polynomial expression that can be rewritten using the [fundamental trigonometric identity](https://algebrica.org/pythagorean-identity/):

$$sin^{2} ⁡ x + cos^{2} ⁡ x = 1$$

which can be expressed in the following forms:

$$cos^{2} ⁡ x & = 1 - sin^{2} ⁡ x \\ sec^{2} ⁡ x & = 1 + tan^{2} ⁡ x \\ tan^{2} ⁡ x & = sec^{2} ⁡ x - 1$$

To simplify an integral, choose an appropriate substitution based on the expression present in the function:

- If the function contains $1 - x^{2}$, use $x = sin ⁡ u$.
- If the function contains $1 + x^{2}$, use $x = tan ⁡ u$.
- If the function contains $x^{2} - 1$, use $x = sec ⁡ u$.

##### A complete and systematic discussion of trigonometric substitution, including the geometric rationale and fully worked examples, is presented in the dedicated section [Trigonometric Substitution for Integrals](https://algebrica.org/trigonometric-substitution-for-integrals/).

## Example 5

Let’s consider the following integral:

$$\int \frac{1}{\sqrt{9 - x^{2}}} d x$$

---

A common substitution for expressions of the form $a^{2} - x^{2}$ is in this case:

$$x = 3 sin ⁡ u$$

Differentiating both sides:

$$d x = 3 cos ⁡ u d u$$

---

Substituting $x = 3 sin ⁡ u$ in the denominator:

$$\sqrt{9 - x^{2}} = \sqrt{9 - 9 sin^{2} ⁡ u} = \sqrt{9 \left(\right. 1 - sin^{2} ⁡ u \left.\right)}$$

By the fundamental property of trigonometry, we have:

$$sin^{2} ⁡ x + cos^{2} ⁡ x = 1$$

We obtain:

$$\sqrt{9 \left(\right. 1 - sin^{2} ⁡ u \left.\right)} = \sqrt{9 cos^{2} ⁡ u} = 3 cos ⁡ u$$

Thus, the integral transforms into:

$$\int \frac{3 cos ⁡ u d u}{3 cos ⁡ u} = \int d u = u + c$$

###### Note that this step assumes $cos ⁡ u \geq 0$, which holds since the substitution $x = 3 sin ⁡ u$ implies $u \in \left[\right. - \pi / 2 , \pi / 2 \left]\right.$.

---

From our substitution $x = 3 sin ⁡ u$, we solve for $u$. By applying the inverse [sine](https://algebrica.org/sine-and-cosine) function [arcsin](https://algebrica.org/arcsine-and-arccosine/), we obtain:

$$u = arcsin ⁡ \left(\right. \frac{x}{3} \left.\right)$$

Thus, the final result is:

$$arcsin ⁡ \left(\right. \frac{x}{3} \left.\right) + c$$

## Substitution rule for definite integrals

When applying the substitution rule to evaluate [definite integrals](https://algebrica.org/definite-integrals), it is crucial to adjust the limits of integration accordingly. The new limits must correspond to the substituted variable rather than the original one. If the limits are not changed, the evaluation of the definite integral will yield an incorrect result. We have:

$$\int_{a}^{b} f \left(\right. g \left(\right. x \left.\right) \left.\right) g^{'} \left(\right. x \left.\right) d x = \int_{g \left(\right. a \left.\right)}^{g \left(\right. b \left.\right)} f \left(\right. u \left.\right) d u$$

## Example 6

Evaluate the definite integral:

$$\int_{0}^{1} x cos ⁡ \left(\right. x^{2} \left.\right) d x$$

---

Using the substitution $u = x^{2}$, we get:
$$d u = 2 x d x d x = \frac{d u}{2 x}$$

---

The next step is to determine the transformed limits of integration. This is done by substituting the original limits into the chosen substitution equation to express them in terms of the new variable. When $x = 0$, then $u = 0^{2} = 0$. When $x = 1$, then $u = 1^{2} = 1$. Note that in this case the limits happen to coincide with the original ones, but this is not generally the case. We obtain:

$$\int_{0}^{1} x cos ⁡ \left(\right. x^{2} \left.\right) d x = \int_{0}^{1} cos ⁡ u \cdot \frac{d u}{2}$$

---

We have:
$$\frac{1}{2} \int_{0}^{1} cos ⁡ u d u$$

Next, we proceed with solving the integral by computing its exact value.
$$\frac{1}{2} sin ⁡ u \left|\right._{0}^{1}$$
$$\frac{1}{2} \left(\right. sin ⁡ 1 - sin ⁡ 0 \left.\right) = \frac{1}{2} \left(\right. sin ⁡ 1 \left.\right)$$

Thus, the final result is:

$$\frac{sin ⁡ \left(\right. 1 \left.\right)}{2}$$

## Selected references

- **MIT OpenCourseWare**. [Integration by Substitution](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/pages/unit-2-applications-of-differentiation/part-c-mean-value-theorem-antiderivatives-and-differential-equations/session-38-integration-by-substitution/)
- **Stanford University**. [Calculus Refresher — Integrals](https://web.stanford.edu/~shervine/teaching/cme-102/calculus)
- **University of California, Davis**. [U-Substitution](https://www.math.ucdavis.edu/~kouba/CalcTwoDIRECTORY/usubdirectory/USubstitution.html)
