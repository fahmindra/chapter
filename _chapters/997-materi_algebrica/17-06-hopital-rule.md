---
layout: chapter
title: "L’Hôpital’s Rule"
chapter: "Differential Calculus Theorems"
chapter_order: 17
section_order: 6
permalink: /materi-algebrica/differential-calculus-theorems/lhôpitals-rule/
---

## Indeterminate forms

L’Hôpital’s rule is a method for evaluating certain [limits](https://algebrica.org/limits) that result in [indeterminate forms](https://algebrica.org/indeterminate-forms/). The theorem establishes a criterion for resolving the indeterminate form of the limit of one or more functions by utilizing their [derivatives](https://algebrica.org/derivatives). By indeterminate forms, we refer to expressions of uncertainty such as:
$$\frac{0}{0} \text{and} \frac{\infty}{\infty}$$

These forms prevent the direct evaluation of a limit, as they signify cases where standard limit theorems alone are insufficient to determine the result and require additional analytical techniques.

## Statement

According to l’Hôpital’s rule, if two [functions](https://algebrica.org/functions/), $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$, are defined on a punctured neighbourhood $I$ of a point $x_{0}$, the following conditions must be satisfied:

- $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are differentiable in $I$, except possibly at $x_{0}$.
- $g^{'} \left(\right. x \left.\right) \neq 0$ for all $x \in I$, with $x \neq x_{0}$.
- $\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) = 0$.
- The following limit exists (finite or infinite):
  $$\underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. x \left.\right)}{g^{'} \left(\right. x \left.\right)}$$

If the above conditions hold, then the following limit exists:
$$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = \underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. x \left.\right)}{g^{'} \left(\right. x \left.\right)}$$

##### In simpler terms, if the quotient of two functions results in an indeterminate form, its limit can be determined by evaluating the limit of their derivatives as $x \rightarrow x_{0}$, provided that this latter limit exists.

---

The rule similarly applies to the indeterminate form $\infty / \infty$. Assume that $f \left(\right. x \left.\right) \rightarrow \infty$ and $g \left(\right. x \left.\right) \rightarrow \infty$ as $x \rightarrow x_{0}$, and that both functions are differentiable in a neighbourhood of $x_{0}$ with $g^{'} \left(\right. x \left.\right) \neq 0$. If the limit of the quotient of the derivatives exists, then the original limit is equal to this value, as follows:

$$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = \underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. x \left.\right)}{g^{'} \left(\right. x \left.\right)}$$

## Proof

To prove the theorem, let us consider an arbitrary point $x \in I$ with $x > x_{0}$. We apply [Cauchy’s theorem](https://algebrica.org/cauchy-theorem/) to $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$. The theorem states that under certain conditions, there exists a point $c \in \left]\right. x_{0} , x \left[\right.$ such that:
 $$\frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \frac{f \left(\right. x \left.\right) - f \left(\right. x_{0} \left.\right)}{g \left(\right. x \left.\right) - g \left(\right. x_{0} \left.\right)}$$

---

By hypothesis, we have $f \left(\right. x_{0} \left.\right) = g \left(\right. x_{0} \left.\right) = 0$. Therefore, $\left(\right. 1 \left.\right)$ becomes:
 $$\frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)}$$

---

At this stage, the point $c$ is not fixed: it depends on $x$. More precisely, for each $x \neq x_{0}$, Cauchy’s Theorem guarantees the existence of a point $c = c \left(\right. x \left.\right)$ such that:
$$x_{0} < c \left(\right. x \left.\right) < x \text{if} x > x_{0}$$
$$x < c \left(\right. x \left.\right) < x_{0} \text{if} x < x_{0}$$
Assume for instance that $x \rightarrow x_{0}^{+}$. Then, we have $0 < c \left(\right. x \left.\right) - x_{0} < x - x_{0} .$ Since $x - x_{0} \rightarrow 0$, by the [Squeeze Theorem](https://algebrica.org/squeeze-theorem/) it follows that $c \left(\right. x \left.\right) - x_{0} \rightarrow 0$ and therefore $c \left(\right. x \left.\right) \rightarrow x_{0}$. An analogous argument holds when $x \rightarrow x_{0}^{-}$. Hence, we conclude that:
$$\underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. c \left(\right. x \left.\right) \left.\right)}{g^{'} \left(\right. c \left(\right. x \left.\right) \left.\right)} = \underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)}$$

---

If $f^{'} \left(\right. x \left.\right)$ and $g^{'} \left(\right. x \left.\right)$ are continuous at $x_{0}$, then their limits at the points $c$ and $x$ coincide. Therefore, the following equality holds:
$$\underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. c \left.\right)}{g^{'} \left(\right. c \left.\right)} = \underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. x \left.\right)}{g^{'} \left(\right. x \left.\right)}$$

---

Then we obtain what we wanted to prove:
$$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = \underset{x \rightarrow x_{0}}{lim} \frac{f^{'} \left(\right. x \left.\right)}{g^{'} \left(\right. x \left.\right)}$$

## Example 1

Let’s compute the following limit involving the [sine function](https://algebrica.org/sine-function).

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x}$$

---

This is a fairly simple limit, but at first glance, it leads to an indeterminate form. Indeed, substituting $0$ for $x$, we get:

$$\frac{sin ⁡ 0}{0} = \frac{0}{0}$$

Because the functions meet the necessary conditions for l’Hôpital’s Rule, the limit of the quotient may be replaced with the limit of the ratio of their derivatives:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x} = \underset{x \rightarrow 0}{lim} \frac{\left(\right. sin ⁡ x \left.\right)^{'}}{\left(\right. x \left.\right)^{'}} = \underset{x \rightarrow 0}{lim} \frac{cos ⁡ x}{1}$$

##### The conditions of the theorem are satisfied. Indeed, we have that $sin ⁡ \left(\right. x \left.\right)$ and $x$ are [continuous functions](https://algebrica.org/continuous-functions/) at $x_{0} = 0$, and $sin ⁡ \left(\right. 0 \left.\right) = 0 , x \left|\right._{x = 0} = 0$. Moreover, both functions are differentiable in an interval $I$ containing $0$, and the derivative of the denominator $g^{'} \left(\right. x \left.\right)$, which in this case is simply $1$, is different from zero.

---

In this case, by evaluating the limit and computing $cos ⁡ \left(\right. x \left.\right)$, we find that the limit is equal to (1):

$$\underset{x \rightarrow 0}{lim} \frac{cos ⁡ x}{1} = \frac{cos ⁡ \left(\right. 0 \left.\right)}{1} = \frac{1}{1} = 1$$

We can therefore conclude that:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x} = \underset{x \rightarrow 0}{lim} \frac{cos ⁡ x}{1} = 1$$

## Example 2

Let us now consider a more complex scenario in which the expression results in an indeterminate form of the type $- \infty + \infty$. In these situations, the recommended approach is to rewrite the difference between the two functions as either a product or a quotient. This transformation allows the expression to be converted into one of the standard indeterminate forms to which L’Hôpital’s Rule applies, namely:

$$\frac{0}{0} \text{or} \frac{\infty}{\infty}$$

---

Let’s consider the following limit:

$$\underset{x \rightarrow 0}{lim} \left(\right. \frac{1}{sin ⁡ x} - \frac{2}{x} \left.\right)$$

This limit leads to an indeterminate form of type $- \infty + \infty$. To apply L’Hôpital’s Rule$^{*}$, we must first rewrite it as a single fraction, thus obtaining an indeterminate form of type $\frac{0}{0}$ or $\frac{\infty}{\infty}$. We have:

$$\underset{x \rightarrow 0}{lim} \left(\right. \frac{1}{sin ⁡ x} - \frac{2}{x} \left.\right) = \underset{x \rightarrow 0}{lim} \frac{x - 2 sin ⁡ x}{x sin ⁡ x}$$

##### Before applying the theorem, it is always necessary to verify that the initial conditions are satisfied.

---

Computing the derivative, the limit becomes:
$$\underset{x \rightarrow 0}{lim} \frac{1 - 2 cos ⁡ x}{sin ⁡ x + x cos ⁡ x}$$

Substituting $x = 0$ in the resulting expression yields $- 1 / 0$, which means the limit diverges.

The result is:

$$\underset{x \rightarrow 0}{lim} \frac{1 – 2 cos ⁡ x}{sin ⁡ x + x cos ⁡ x} = - \infty$$

Generally, if the application of L’Hôpital’s Rule yields a limit that remains an [indeterminate form](https://algebrica.org/indeterminate-forms/), the rule may be applied repeatedly, provided the necessary conditions are met at each stage. At every iteration, it is essential to confirm that both the new numerator and denominator approach either $0$ or $\infty$.

## Indeterminate products

The same principle illustrated in Example 2 can be applied when encountering indeterminate forms of the type $0 \cdot \infty$, arising from the product of two functions $f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right)$. In this case, to rewrite the expression in a form suitable for applying L’Hôpital’s Rule, it is sufficient to express the product as follows:

$$f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) = \frac{f \left(\right. x \left.\right)}{\frac{1}{g \left(\right. x \left.\right)}} \text{or} f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) = \frac{g \left(\right. x \left.\right)}{\frac{1}{f \left(\right. x \left.\right)}}$$

---

For example, consider the following limit:

$$\underset{x \rightarrow 0^{+}}{lim} x ln ⁡ x$$

This expression represents an indeterminate form of type $0 \cdot \infty$. The product can be rewritten as a quotient:

$$\underset{x \rightarrow 0^{+}}{lim} x ln ⁡ x = \underset{x \rightarrow 0^{+}}{lim} \frac{ln ⁡ x}{\frac{1}{x}}$$

The resulting expression is now an indeterminate form of type $\frac{\infty}{\infty}$, which is suitable for the application of L’Hôpital’s Rule:

$$\underset{x \rightarrow 0^{+}}{lim} \frac{ln ⁡ x}{\frac{1}{x}} = \underset{x \rightarrow 0^{+}}{lim} \frac{\left(\right. ln ⁡ x \left.\right)^{'}}{\left(\left(\right. \frac{1}{x} \left.\right)\right)^{'}} = \underset{x \rightarrow 0^{+}}{lim} \frac{\frac{1}{x}}{- \frac{1}{x^{2}}} = \underset{x \rightarrow 0^{+}}{lim} \left(\right. - x \left.\right) = 0$$

## Selected references

- **MIT, E. Herman**. [Calculus Vol. 1 — 4.8 L’Hôpital’s Rule](https://openstax.org/books/calculus-volume-1/pages/4-8-lhopitals-rule-introduction-to-improper-integrals)
- **University of British Columbia (Feldman, Rechnitzer, Yeager)**. [L’Hôpital’s Rule](https://personal.math.ubc.ca/~CLP/CLP1/clp_1_dc/sec_4_7.html)
- **MAA Convergence, (D. E. Otero, Xavier University)**. [L’Hôpital’s Rule](https://old.maa.org/press/periodicals/convergence/l-h-pital-s-rule-a-mini-primary-source-project-for-calculus-1-students)
