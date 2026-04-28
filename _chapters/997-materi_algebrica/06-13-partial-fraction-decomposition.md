---
layout: chapter
title: "Partial Fraction Decomposition"
chapter: "Polynomials"
chapter_order: 6
section_order: 13
permalink: /materi-algebrica/polynomials/partial-fraction-decomposition/
---

## Introduction

Partial fraction decomposition is a practical and widely used method for rewriting a [rational function](https://algebrica.org/rational-functions/) (a quotient of two [polynomials](https://algebrica.org/polynomials/)) as a sum of simpler elementary fractions. The key idea is that, once the denominator is factored into its irreducible components, the original [function](https://algebrica.org/functions/) can be expressed as a combination of basic terms whose structure directly reflects the factors of the denominator.

This method becomes especially valuable when a rational function is easier to analyze once it has been broken into its elementary components, as in the [integration of rational functions](https://algebrica.org/integral-of-rational-functions/), where each partial fraction corresponds to a standard form. Before turning to practical applications, it is useful to understand the underlying mechanism that makes this decomposition possible.

---

Suppose we are given a rational function of the form:

$$\frac{P \left(\right. x \left.\right)}{Q \left(\right. x \left.\right)}$$

- $P \left(\right. x \left.\right)$ and $Q \left(\right. x \left.\right)$ are polynomials.
- The degree of $P \left(\right. x \left.\right)$ is strictly less than the degree of $Q \left(\right. x \left.\right)$.

Our goal is to factor $Q \left(\right. x \left.\right)$ into its irreducible components and to express $P \left(\right. x \left.\right)$ as a linear combination of terms whose denominators correspond to those factors. In this way, the original rational function is rewritten as a sum of elementary fractions, each associated with a specific linear or irreducible quadratic factor of $Q \left(\right. x \left.\right)$. This decomposition provides a canonical representation of the function and forms the basis of the partial fraction method.

##### An example of a reduction into irreducible factors is the case of $Q \left(\right. x \left.\right) = x^{2} - 9$, which can be written as $Q \left(\right. x \left.\right) = \left(\right. x - 3 \left.\right) \left(\right. x + 3 \left.\right)$. Both factors are linear and therefore irreducible over the real numbers.

## Example 1

To illustrate the mechanism of the method, it is helpful to begin with a concrete example.
 Consider the rational function:

$$\frac{5 x + 4}{\left(\right. x - 2 \left.\right) \left(\right. 2 x + 3 \left.\right)}$$

We first observe that both the numerator and the denominator are polynomials, and that the degree of $P \left(\right. x \left.\right)$ is strictly less than the degree of $Q \left(\right. x \left.\right)$. Hence the expression is already a proper rational function, and the conditions required for applying the partial fraction method are satisfied. We may therefore proceed with the decomposition.

---

As a first step, we rewrite the given rational function as a sum of two simpler terms, each having one of the linear factors of the denominator as its own denominator. In other words, we seek constants $A$ and $B$ such that the expression can be represented as

$$(\text{1}) \frac{5 x + 4}{\left(\right. x - 2 \left.\right) \left(\right. 2 x + 3 \left.\right)} = \frac{A}{x - 2} + \frac{B}{2 x + 3}$$

At this point, our objective is to determine the constants $A$ and $B$ so that the identity above holds for all real values of $x$. In other words, we must find $A$ and $B$ such that the following relation is satisfied:

$$(\text{2}) 5 x + 4 = A \left(\right. 2 x + 3 \left.\right) + B \left(\right. x - 2 \left.\right)$$

In this final step, we clear the denominators by multiplying both sides of the equation by $\left(\right. x - 2 \left.\right) \left(\right. 2 x + 3 \left.\right)$. This yields the polynomial identity above which must hold for every value of $x$. The advantage of this transformation is that it converts the original rational expression into an equation involving only polynomials, allowing us to determine the unknown coefficients $A$ and $B$ through direct algebraic comparison.

---

To determine the values of $A$ and $B$, we apply a simple and effective procedure often referred to as the **cover-up rule**. The idea is to assign strategic values to $x$ so as to eliminate one coefficient at a time. Specifically, by choosing values of $x$ that annul one of the linear factors in the denominator, we remove the corresponding term from the equation and can solve directly for the remaining coefficient. This allows us to compute $A$ and $B$ efficiently without expanding or comparing all polynomial coefficients.

For example, by choosing $x = 2$ we eliminate the term involving $B$, since the factor $\left(\right. x - 2 \left.\right)$ becomes zero. Substituting $x = 2$ into the identity $2$ we obtain:

$$5 \left(\right. 2 \left.\right) + 4 = A \left(\right. 2 \cdot 2 + 3 \left.\right) + B \left(\right. 0 \left.\right)$$

This simplifies to:

$$10 + 4 = A \left(\right. 7 \left.\right)$$

and therefore:

$$A = \frac{14}{7} = 2$$

---

To determine $B$, we choose the value of $x$ that annuls the factor $2 x + 3$. Setting $x = - \frac{3}{2}$ eliminates the term involving $A$. Substituting this value into the identity $2$ we obtain

$$5 \left(\right. - \frac{3}{2} \left.\right) + 4 = A \left(\right. 0 \left.\right) + B \left(\right. - \frac{3}{2} - 2 \left.\right)$$

Simplifying each term gives:

$$- \frac{15}{2} + 4 = B \left(\right. - \frac{7}{2} \left.\right)$$

We obtain:

$$- \frac{7}{2} = - \frac{7}{2} B$$

and therefore

$$B = 1$$

By substituting the values of $A$ and $B$ into equation $1$, we obtain the following representation of the original rational function:

$$\frac{5 x + 4}{\left(\right. x - 2 \left.\right) \left(\right. 2 x + 3 \left.\right)} = \frac{2}{x - 2} + \frac{1}{2 x + 3}$$

This expresses the given rational function as the sum of its partial fractions.

## Application to the computation of integrals

As mentioned at the beginning, partial fraction decomposition is particularly valuable in practical settings, especially when [integrating rational functions](https://algebrica.org/integral-of-rational-functions/). Returning to the function from Example 1, the integral:

$$\int \frac{5 x + 4}{\left(\right. x - 2 \left.\right) \left(\right. 2 x + 3 \left.\right)} d x$$

is not immediately straightforward to evaluate in its original form. However, once the expression is rewritten as a sum of simpler terms we have:

$$\int \frac{5 x + 4}{\left(\right. x - 2 \left.\right) \left(\right. 2 x + 3 \left.\right)} d x = \int \left(\right. \frac{2}{x - 2} + \frac{1}{2 x + 3} \left.\right) d x$$

In this form the computation becomes significantly more manageable. By the [linearity property of integrals](https://algebrica.org/indefinite-integrals/), the integral of a sum is equal to the sum of the integrals of each term. Therefore, after performing the partial fraction decomposition, we obtain:

$$2 \int \frac{1}{x - 2} d x + \int \frac{1}{2 x + 3} d x$$

which can be evaluated term by term using standard [logarithmic](https://algebrica.org/logarithms) formulas. In particular:

$$\int \frac{2}{x - 2} d x = 2 ln ⁡ \left|\right. x - 2 \left|\right. + c_{1}$$
$$\int \frac{1}{2 x + 3} d x = \frac{1}{2} ln ⁡ \left|\right. 2 x + 3 \left|\right. + c_{2}$$

Combining the results yields the antiderivative of the original rational function. This illustrates how partial fraction decomposition transforms an integral that is difficult to approach directly into the sum of elementary integrals with known solutions.

## General structure of partial fraction decomposition

The decomposition of a rational function into partial fractions follows a systematic rule that depends exclusively on the factorization of the denominator. Once the denominator has been expressed as a product of linear and irreducible quadratic factors, possibly raised to higher powers, the rational function can be rewritten as a sum of elementary terms associated with each factor.

Specifically, for every linear factor of the form $x + a$, the decomposition includes a term of the form:

$$\frac{A}{\left(\right. x + a \left.\right)}$$

If the linear factor appears with multiplicity $k$, then a sequence of terms must be added, namely:

$$\frac{A_{1}}{x + a} + \frac{A_{2}}{\left(\right. x + a \left.\right)^{2}} + \hdots + \frac{A_{k}}{\left(\right. x + a \left.\right)^{k}}$$

Similarly, for each irreducible quadratic factor $x^{2} + a x + b$, a term of the form:

$$\left(\right. A + B x \left.\right) / \left(\right. x^{2} + a x + b \left.\right)$$

must be included. If this factor is repeated $k$ times, the decomposition requires the full sequence:

$$\frac{A_{1} + B_{1} x}{x^{2} + a x + b} + \frac{A_{2} + B_{2} x}{\left(\right. x^{2} + a x + b \left.\right)^{2}} + \hdots + \frac{A_{k} + B_{k} x}{\left(\right. x^{2} + a x + b \left.\right)^{k}}$$

##### These rules guarantee that every rational function with denominator fully factored over the reals admits a unique partial fraction representation once the coefficients are determined.

## Example 2

Let us now consider a slightly more complicated example than the previous one. We want to find the partial fraction decomposition of the rational function:

$$\frac{1}{x^{3} - 6 x^{2} + 11 x - 6}$$

Although the numerator is already as simple as possible, the denominator is a cubic polynomial, and its factorization will guide the entire decomposition process. Our first step is therefore to factor the denominator into irreducible components. Testing possible rational [roots](https://algebrica.org/roots-of-a-polynomial/), we find that $x = 1$ satisfies:

$$1 - 6 + 11 - 6 = 0$$

so $\left(\right. x - 1 \left.\right)$ is a factor. Dividing the polynomial by $\left(\right. x - 1 \left.\right)$ using [synthetic division](https://algebrica.org/synthetic-division/) we have:

$$1 & 1 & - 6 & 11 & - 6 \\ & & 1 & - 5 & 6 \\ & 1 & - 5 & 6 & 0$$

In this way we obtain the quotient $x^{2} - 5 x + 6$, which further factorizes as

$$x^{2} - 5 x + 6 = \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)$$

The complete factorization of the denominator is thus:

$$\left(\right. x - 1 \left.\right) \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)$$

and since all factors are linear and distinct, we may express the rational function as

$$\frac{1}{\left(\right. x - 1 \left.\right) \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)} = \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{x - 3}$$

---

To determine the constants $A$, $B$, and $C$, we multiply both sides by the denominator, obtaining the identity:

$$1 = A \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right) + B \left(\right. x - 1 \left.\right) \left(\right. x - 3 \left.\right) + C \left(\right. x - 1 \left.\right) \left(\right. x - 2 \left.\right)$$

which holds for all real $x$. By substituting convenient values, we can eliminate terms and solve for each constant.

---

Setting $x = 1$ gives:

$$1 = A \left(\right. 1 - 2 \left.\right) \left(\right. 1 - 3 \left.\right) = 2 A , A = \frac{1}{2}$$

Setting $x = 2$ gives:

$$1 = B \left(\right. 2 - 1 \left.\right) \left(\right. 2 - 3 \left.\right) = - B , B = - 1$$

Setting $x = 3$ gives:

$$1 = C \left(\right. 3 - 1 \left.\right) \left(\right. 3 - 2 \left.\right) = 2 C , C = \frac{1}{2}$$

Substituting these values into the decomposition yields

$$\frac{1}{x^{3} - 6 x^{2} + 11 x - 6} = \frac{1}{2 \left(\right. x - 1 \left.\right)} - \frac{1}{x - 2} + \frac{1}{2 \left(\right. x - 3 \left.\right)}$$

##### This decomposition expresses the original rational function as a sum of elementary fractions, each associated with one of the linear factors of the denominator. The example shows how the partial fraction method extends naturally to higher-degree denominators once they are properly factorized.
