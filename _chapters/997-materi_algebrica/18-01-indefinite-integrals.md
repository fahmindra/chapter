---
layout: chapter
title: "Indefinite Integrals"
chapter: "Integrals"
chapter_order: 18
section_order: 1
permalink: /materi-algebrica/integrals/indefinite-integrals/
---

## Primitives

Differentiation assigns to each function a unique [derivative](https://algebrica.org/derivatives) by definition. The inverse process seeks to determine whether, for a given function $f \left(\right. x \left.\right)$, there exists a function $F \left(\right. x \left.\right)$ whose derivative is exactly $f \left(\right. x \left.\right)$. Such a function is called a **primitive**. Formally, a function $F \left(\right. x \left.\right)$ is said to be a primitive of the function $f \left(\right. x \left.\right)$ defined on the [interval](https://algebrica.org/intervals/) $\left[\right. a , b \left]\right.$ if $F \left(\right. x \left.\right)$ is differentiable throughout $\left[\right. a , b \left]\right.$ and its derivative is $f \left(\right. x \left.\right)$, that is:

$$F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right) , \forall x \in \left[\right. a , b \left]\right.$$

Not every function admits a primitive on a given interval. A sufficient condition is [continuity](https://algebrica.org/continuous-functions/): every continuous function on a closed interval $\left[\right. a , b \left]\right.$ admits a primitive there. The converse does not hold in general.

If we seek a function $F \left(\right. x \left.\right)$ whose derivative is $f \left(\right. x \left.\right) = 3 x^{2}$, differentiation rules allow us to determine that such a function is $x^{3}$. Indeed, the derivative of $x^{3}$ is:
$$\frac{d}{d x} x^{3} = 3 x^{2}$$

which confirms that $x^{3}$ is a primitive of $f \left(\right. x \left.\right) = 3 x^{2}$.

---

We have seen that if a function $f \left(\right. x \left.\right)$ is differentiable, it has a unique derivative $f^{'} \left(\right. x \left.\right)$. However, in the case of primitives, the primitive of a function is not unique. Given a function $f \left(\right. x \left.\right)$, any two primitives $F_{1} \left(\right. x \left.\right)$ and $F_{2} \left(\right. x \left.\right)$ differ by a constant, meaning that:

$$F_{2} \left(\right. x \left.\right) = F_{1} \left(\right. x \left.\right) + c$$

where $c$ is an arbitrary constant. This follows from the fact that the derivative of a constant is zero: $$\frac{d}{d x} c = 0$$

In the previous example, $3 x^{2}$ is a derivative of $x^{3}$, but it is also the derivative of $x^{3} + 5$ and $x^{3} - 1 / 2$. This implies that there are infinitely many primitives $F \left(\right. x \left.\right)$ for our function.

---

If a function $f \left(\right. x \left.\right)$ admits a primitive $F \left(\right. x \left.\right)$, then it has infinitely many primitives of the form $F \left(\right. x \left.\right) + c$, where $c$ is any real number $c \in \mathbb{R}$:
$$D \left[\right. F \left(\right. x \left.\right) + C \left]\right. = F^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right) , \forall C \in \mathbb{R}$$

---

Conversely, if two functions $F_{1} \left(\right. x \left.\right)$ and $F_{2} \left(\right. x \left.\right)$ are both primitives of the same function $f \left(\right. x \left.\right)$, then they differ by a constant.
$$D \left[\right. F_{1} \left(\right. x \left.\right) - F_{2} \left(\right. x \left.\right) \left]\right. = F_{1}^{'} \left(\right. x \left.\right) - F_{2}^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right) - f \left(\right. x \left.\right) = 0$$

## What is the indefinite integral

The **indefinite integral** of a function $f \left(\right. x \left.\right)$ is defined as the set of all its primitives, expressed as $F \left(\right. x \left.\right) + c$, where $c$ is an arbitrary real number. It is denoted as:

$$\int f \left(\right. x \left.\right) d x = F \left(\right. x \left.\right) + c c \in \mathbb{R}$$

---

From the previous definition, it follows that:

$$D \left[\right. \int f \left(\right. x \left.\right) d x \left]\right. = f \left(\right. x \left.\right)$$

This result reflects a fundamental property of the indefinite integral: the operator
$D \left[\right. \int \cdot d x \left]\right.$ acts as the identity on integrable functions,
returning the original function $f \left(\right. x \left.\right)$. This relationship is made precise by the [Fundamental Theorem of Calculus](https://algebrica.org/fundamental-theorem-of-calculus/), which establishes
the formal connection between differentiation and integration.

## Example 1

Find the primitive of $3 x$ that passes through the point $\left(\right. 2 , 1 \left.\right)$. The first step is to find the general form of the primitive of $f \left(\right. x \left.\right) = 3 x$, which we obtain by integrating:

$$F \left(\right. x \left.\right) = \int 3 x d x = \frac{3}{2} x^{2} + c$$

To find the specific primitive that passes through the point $\left(\right. 2 , 1 \left.\right)$, we impose the condition $F \left(\right. 2 \left.\right) = 1$. Substituting $x = 2$ into the equation we obtain:

$$\frac{3}{2} \left(\right. 2 \left.\right)^{2} + c & = 1 \\ \frac{3}{2} \cdot 4 + c & = 1 \\ 6 + c & = 1 \\ c & = - 5$$

Thus, the unique primitive satisfying the given condition is:
$$F \left(\right. x \left.\right) = \frac{3}{2} x^{2} - 5.$$

## Linearity Properties

The integral is a linear operator, meaning that it satisfies the following linearity properties. The indefinite integral of a sum of integrable functions is equal to the sum of the indefinite integrals of the individual functions. In fact, we have:
$$(\text{1}) \int \left[\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left]\right. d x = \int f \left(\right. x \left.\right) d x + \int g \left(\right. x \left.\right) d x$$

The integral of the product of a constant and an integrable function is equal to the product of the constant and the integral of the function. We have:
$$(\text{2}) \int k f \left(\right. x \left.\right) d x = k \int f \left(\right. x \left.\right) d x , \forall k \in \mathbb{R}$$

## Example 2

Consider the function: $f \left(\right. x \left.\right) = 3 x^{2} + 2 x$. Applying equation $1$, we split the integral:

$$\int \left(\right. 3 x^{2} + 2 x \left.\right) d x = \int 3 x^{2} d x + \int 2 x d x$$

Now, we compute each integral separately:

$$\int 3 x^{2} d x = x^{3} + c_{1}$$
$$\int 2 x d x = x^{2} + c_{2}$$

We obtain $x^{3} + x^{2} + c$ where $c = c_{1} + c_{2}$ is an arbitrary constant.

## Example 3

Consider the function: $f \left(\right. x \left.\right) = 5 sin ⁡ \left(\right. x \left.\right)$. Applying equation $2$, we have:

$$\int 5 sin ⁡ \left(\right. x \left.\right) d x = 5 \int sin ⁡ \left(\right. x \left.\right) d x$$

Thus, we obtain $- 5 cos ⁡ \left(\right. x \left.\right) + c$.

## Integral of a power function

Let’s now see how to compute the integral of a power function of the form $x^{a}$ with $a \in \mathbb{R}$. In general, the following formula can be used:
$$\int x^{a} d x = \frac{x^{a + 1}}{a + 1} + c , \text{for} a \in \mathbb{R} , a \neq - 1$$

## Example 4

Let’s solve the following integral:

$$\int \left(\right. 3 x^{4} + 5 x^{2} \left.\right) d x$$

Using the properties mentioned above, we obtain:
$$3 \int x^{4} d x + 5 \int x^{2} d x$$

We have split the integral of the sum into the sum of two integrals and factored out the constants from the integral sign. Now, we compute the integral of the power function. We obtain:

$$\int x^{4} d x = \frac{x^{5}}{5} + c 1 , \int x^{2} d x = \frac{x^{3}}{3} + c 2$$

Multiplying by the constants:

$$3 \cdot \frac{x^{5}}{5} + 5 \cdot \frac{x^{3}}{3} + c$$

Thus, we obtain the final result:
$$\frac{3}{5} x^{5} + \frac{5}{3} x^{3} + c$$

## Example 5

Compute the following integral:

$$\int \left(\right. 4 x^{3} - \frac{3}{\sqrt{x}} + 2 cos ⁡ x \left.\right) d x$$

The integrand brings together three terms of genuinely different character: a polynomial
term, a term involving a fractional power of $x$, and a trigonometric term. Rather
than searching for a single rule that covers all three at once, we apply linearity to
decompose the problem into three independent integrals, each of which falls within a
known pattern:

$$\int 4 x^{3} d x - \int 3 x^{- 1 / 2} d x + \int 2 cos ⁡ x d x$$

---

The first term presents no difficulty. The power rule applied to $x^{3}$ gives:

$$\int 4 x^{3} , d x = 4 \cdot \frac{x^{4}}{4} = x^{4}$$

---

The second term is less immediate, but becomes straightforward once we rewrite $\frac{1}{\sqrt{x}}$ as $x^{- 1 / 2}$. With $a = - \frac{1}{2}$, the power rule yields:

$$\int 3 x^{- 1 / 2} d x = 3 \cdot \frac{x^{1 / 2}}{1 / 2} = 6 \sqrt{x}$$

Note that $a = - \frac{1}{2} \neq - 1$, so the logarithmic case does not arise and the power rule applies without exception.

---

For the third term, the standard integral of the cosine gives directly:

$$\int 2 cos ⁡ x d x = 2 sin ⁡ x$$

Assembling the three contributions:

$$\int \left(\right. 4 x^{3} - \frac{3}{\sqrt{x}} + 2 cos ⁡ x \left.\right) d x = x^{4} - 6 \sqrt{x} + 2 sin ⁡ x + c$$

###### The three separate integration constants collapse into a single arbitrary real number $c \in \mathbb{R}$, as expected from the general theory of primitives. The result can be verified by differentiating: applying $\frac{d}{d x}$ to $x^{4} - 6 \sqrt{x} + 2 sin ⁡ x + c$ returns the original integrand term by term, confirming that the computation is correct.

## The logarithmic integral

When the exponent of $x$ is $- 1$, the integral takes a different form. Instead of applying the power rule, we use the [logarithmic](https://algebrica.org/logarithms/) integral:
$$\int x^{- 1} d x = \int \frac{1}{x} d x = ln ⁡ \left|\right. x \left|\right. + c$$
In fact, the standard formula for integrating a power function is:
$$\int x^{a} d x = \frac{x^{a + 1}}{a + 1} + c$$
However, when $a = - 1$, the denominator in the fraction becomes zero:
$$\frac{x^{0}}{0} = \frac{1}{0}$$
Since division by zero is undefined, this approach does not apply. Instead, for $a = - 1$, the correct integral is $ln ⁡ \left|\right. x \left|\right. + c$. This result follows from the fact that the derivative of $ln ⁡ \left|\right. x \left|\right.$ is precisely $1 / x$, making it the appropriate antiderivative in this special case.

## Fundamental integration rules

|  |  |
| --- | --- |
| Linearity | $$\int \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) d x = \int f \left(\right. x \left.\right) d x + \int g \left(\right. x \left.\right) d x$$ |
| Linearity | $$\int k f \left(\right. x \left.\right) d x = k \int f \left(\right. x \left.\right) d x$$ |
| Power rule | $$\int x^{a} d x = \frac{x^{a + 1}}{a + 1} + c a \neq - 1$$ |
| Logarithmic case | $$\int \frac{1}{x} d x = ln ⁡ \left|\right. x \left|\right. + c$$ |

## Common Integrals

Below is a summary of the most common basic integrals, useful in calculus and for transforming complex expressions into simpler, well-known forms.

- $$\int \frac{1}{x} d x = ln ⁡ \left|\right. x \left|\right. + c$$ [Dive deeper](https://algebrica.org/integral-of-rational-functions/)
- $$\int a^{x} d x = \frac{1}{ln ⁡ a} \cdot a^{x} + c$$ [Dive deeper](https://algebrica.org/integral-of-the-exponential-function)
- $$\int sin ⁡ x d x = - cos ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int cos ⁡ x d x = sin ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int \frac{1}{sin^{2} ⁡ x} d x = cot ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int \frac{1}{cos^{2} ⁡ x} d x = tan ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int sec^{2} ⁡ x d x = tan ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int sec ⁡ x tan ⁡ x d x = sec ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int csc^{2} ⁡ x d x = - cot ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int csc ⁡ x cot ⁡ x d x = - csc ⁡ x + c$$ [Dive deeper](https://algebrica.org/integral-of-trigonometric-functions/)
- $$\int \frac{d x}{1 + x^{2}} = arctan ⁡ x + c$$
- $$\int \frac{d x}{\sqrt{1 - x^{2}}} = arcsin ⁡ x + c$$

##### These identities hold on any interval where the integrand is defined and continuous.

## Selected references

- **Stony Brook University**. [Antiderivative and Indefinite Integral](https://www.math.stonybrook.edu/Videos/MAT131Online/Handouts/Lecture-25-Handout.pdf)
- **University of Kentucky**. [Integrals, Antiderivatives, and the Fundamental Theorem of Calculus](https://www.ms.uky.edu/~123/lecturenotes/Chapter10.pdf)
- **Purdue University**. [Antiderivatives and Indefinite Integration](https://www.math.purdue.edu/~kyochman/MA16010/Lesson27_Notes-IndefiniteIntegration.pdf)
- **Binghamton University**. [Antiderivatives and Indefinite Integrals](https://www2.math.binghamton.edu/lib/exe/fetch.php/people/mckenzie/antiderivatives_with_examples_and_extra_problems.pdf)
