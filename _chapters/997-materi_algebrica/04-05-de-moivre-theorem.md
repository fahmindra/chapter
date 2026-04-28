---
layout: chapter
title: "De Moivre’s Theorem"
chapter: "Complex Numbers"
chapter_order: 4
section_order: 5
permalink: /materi-algebrica/complex-numbers/de-moivres-theorem/
---

## Motivation for De Moivre’s Theorem

Suppose we want to compute the power of a complex number $z \in \mathbb{C}$. The most straightforward approach is to start from its [algebraic form](https://algebrica.org/complex-numbers-introduction/) and expand the expression directly. For example, given $z = a + i b$ we may want to calculate its square. We have:

$$z^{2} & = \left(\right. a + i b \left.\right)^{2} \\ & = a^{2} + i 2 a b - b^{2}$$

While this method is valid, as the exponent increases beyond three, the calculations become increasingly tedious and impractical. Expanding higher powers algebraically yields lengthy expressions and more terms, reducing the practicality of this approach. In these situations, [De Moivre’s Theorem](https://algebrica.org/de-moivre-theorem/) provides a more efficient and elegant solution.

## De Moivre’s theorem and exponential notation for complex numbers

De Moivre’s theorem provides a method for computing powers and roots of complex numbers, whether written in [trigonometric](https://algebrica.org/complex-numbers-trigonometric-form/) or [exponential form](https://algebrica.org/complex-numbers-exponential-form/). Consider a complex number $z$ raised to an integer power $n \in \mathbb{Z}$. That is,

$$z^{n} n \in \mathbb{Z}$$

Rewrite the number $z$ in trigonometric form:

$$z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$$

For any [integer](https://algebrica.org/integers/) $n$, the power $z^{n}$ can be computed by raising the modulus to the $n$-th power and multiplying the angle by $n$. The result is a new complex number in polar form. We have:

$$z^{n} = r^{n} \left(\right. cos ⁡ \left(\right. n \theta \left.\right) + i sin ⁡ \left(\right. n \theta \left.\right) \left.\right)$$

This identity holds for all integers $n$, including negative ones. When $n$ is a rational number $n = p / q$, the formula still applies but yields one of the $q$ distinct roots; the full set of roots requires considering all values of the argument of the form $\theta + 2 k \pi$ for $k = 0 , 1 , \ldots , q - 1$.

---

Now rewrite the complex number $z$ using Euler’s identity, in exponential form:

$$e^{i \theta} = cos ⁡ \theta + i sin ⁡ \theta$$

We obtain:

$$z = r e^{i \theta}$$

This formulation allows us to interpret complex numbers in a way that’s deeply aligned with the structure of exponentiation. It also turns De Moivre’s Theorem into something almost automatic. When we raise $z$ to an integer power, we simply apply the usual exponent laws:

$$z^{n} = \left(\right. r e^{i \theta} \left.\right)^{n} = r^{n} e^{i n \theta}$$

There’s no algebra to expand, no trigonometric identities to manipulate. The modulus is raised to the power $n$, and the argument is multiplied by $n$.

## A proof by induction

De Moivre’s Theorem states that for any integer $n$ and any complex number $z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$:

$$z^{n} = r^{n} \left(\right. cos ⁡ \left(\right. n \theta \left.\right) + i sin ⁡ \left(\right. n \theta \left.\right) \left.\right)$$

The formula can be established by [induction](https://algebrica.org/principle-of-mathematical-induction/) on $n$. The argument has two parts:

- Verifying the base case.
- Showing that validity at step $n$ forces validity at step $n + 1$.

---

For the base case, setting $n = 1$ reduces the formula to $z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$, which is the trigonometric form of $z$ by definition. For the inductive step, suppose the formula holds for some integer $n \geq 1$:

$$z^{n} = r^{n} \left(\right. cos ⁡ \left(\right. n \theta \left.\right) + i sin ⁡ \left(\right. n \theta \left.\right) \left.\right)$$

Multiplying both sides by $z = r \left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)$ and expanding the product we obtain:

$$z^{n + 1} = r^{n + 1} \left[\right. \left(\right. cos ⁡ \left(\right. n \theta \left.\right) cos ⁡ \theta - sin ⁡ \left(\right. n \theta \left.\right) sin ⁡ \theta \left.\right) + i \left(\right. sin ⁡ \left(\right. n \theta \left.\right) cos ⁡ \theta + cos ⁡ \left(\right. n \theta \left.\right) sin ⁡ \theta \left.\right) \left]\right.$$

The two expressions in brackets are the addition formulas for [cosine and sine](https://algebrica.org/sine-and-cosine/) respectively and applying them yields:

$$z^{n + 1} = r^{n + 1} \left(\right. cos ⁡ \left(\right. \left(\right. n + 1 \left.\right) \theta \left.\right) + i sin ⁡ \left(\right. \left(\right. n + 1 \left.\right) \theta \left.\right) \left.\right)$$

The identity holds at step $n + 1$, which completes the induction.

## Example 1

For example, squaring the complex number $z = r e^{i \theta}$ gives:

$$z^{2} = \left(\right. r e^{i \theta} \left.\right)^{2} = r^{2} e^{i 2 \theta}$$

![](https://algebrica.org/wp-content/uploads/resources/images/exponent-form-2-1.png)

The result is a new complex number whose modulus is $r^{2}$ and whose argument is $2 \theta .$ In geometric terms, this means the [vector](https://algebrica.org/vectors/) is stretched by a factor of $r^{2}$ and rotated to double its original angle.

## Example 2

Let’s try to compute $z^{4}$ for the complex number $z = 2 + 2 i$.
First, we determine the modulus of $z$:

$$\left|\right. z \left|\right. = \sqrt{2^{2} + 2^{2}} = \sqrt{8} = 2 \sqrt{2}$$

> The modulus of a complex number represents its distance from the origin in the complex plane. It is calculated using the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/).

---

Next, we determine the argument of $z$:

$$\theta = arg ⁡ \left(\right. z \left.\right) = arctan ⁡ \left(\right. \frac{2}{2} \left.\right) = \frac{\pi}{4}$$

##### The argument of a complex number is the angle it makes with the positive real axis, measured counterclockwise. In this case, since both the real and imaginary parts are equal, the angle is exactly $45^{\circ}$, or $\frac{\pi}{4}$ radians.

---

We can now express $z$ in exponential form:

$$z = 2 \sqrt{2} \cdot e^{i \frac{\pi}{4}}$$

This compact form makes it much easier to raise $z$ to a power, since we can apply the rules of exponents directly. Applying De Moivre’s Theorem, we compute:

$$z^{4} = \left(\right. 2 \sqrt{2} \left.\right)^{4} \cdot e^{i \cdot 4 \cdot \frac{\pi}{4}} = \left(\right. 2 \sqrt{2} \left.\right)^{4} \cdot e^{i \pi}$$

Let’s simplify:

$$\left(\right. 2 \sqrt{2} \left.\right)^{4} = \left(\right. 2^{1} \cdot 2^{1 / 2} \left.\right)^{4} = 2^{6} = 64$$

---

Since $e^{i \pi} = - 1$ we find:

$$z^{4} = 64 \cdot \left(\right. - 1 \left.\right) = - 64$$

##### The same result can also be obtained by expanding the expression algebraically.

So the fourth power of $z = 2 + 2 i$ is the real number $- 64$.

## Deriving trigonometric identities

One of the most practical applications of De Moivre’s Theorem is the derivation of explicit formulas for [sine and cosine](https://algebrica.org/sine-and-cosine/), in particular for $cos ⁡ \left(\right. n \theta \left.\right)$ and $sin ⁡ \left(\right. n \theta \left.\right)$ in terms of powers of $cos ⁡ \theta$ and $sin ⁡ \theta$. The idea is straightforward: expand the left-hand side of the theorem using the [binomial formula](https://algebrica.org/binomial-coefficient/), then separate real and imaginary parts.

For $n = 3$, the theorem gives:

$$\left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)^{3} = cos ⁡ \left(\right. 3 \theta \left.\right) + i sin ⁡ \left(\right. 3 \theta \left.\right)$$

Expanding the left-hand side with the binomial formula:

$$\left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)^{3} = cos^{3} ⁡ \theta + 3 i cos^{2} ⁡ \theta sin ⁡ \theta + 3 i^{2} cos ⁡ \theta sin^{2} ⁡ \theta + i^{3} sin^{3} ⁡ \theta$$

Using $i^{2} = - 1$ and $i^{3} = - i$:

$$= \left(\right. cos^{3} ⁡ \theta - 3 cos ⁡ \theta sin^{2} ⁡ \theta \left.\right) + i \left(\right. 3 cos^{2} ⁡ \theta sin ⁡ \theta - sin^{3} ⁡ \theta \left.\right)$$

Equating real and imaginary parts with the right-hand side:

$$cos ⁡ \left(\right. 3 \theta \left.\right) = cos^{3} ⁡ \theta - 3 cos ⁡ \theta sin^{2} ⁡ \theta$$

$$sin ⁡ \left(\right. 3 \theta \left.\right) = 3 cos^{2} ⁡ \theta sin ⁡ \theta - sin^{3} ⁡ \theta$$

These are the triple angle formulas for cosine and sine. Both follow directly from a single application of the binomial expansion, with no need for repeated use of [addition formulas](https://algebrica.org/reduction-formulas-and-reference-angles/) or any other intermediate result. The same procedure extends to any integer $n$: the binomial expansion of $\left(\right. cos ⁡ \theta + i sin ⁡ \theta \left.\right)^{n}$ always yields $cos ⁡ \left(\right. n \theta \left.\right)$ as its real part and $sin ⁡ \left(\right. n \theta \left.\right)$ as its imaginary part.

## Finding complex roots with De Moivre’s theorem

De Moivre’s Theorem isn’t just useful for powers. It also gives us a clean and elegant way to find the roots of a complex number. Suppose we want to solve:

$$z^{n} = w$$

where $w \in \mathbb{C}$. This means we’re looking for all the complex numbers $z$ such that raising them to the $n$-th power gives $w$. First, we write $w$ in exponential form. Since the argument of a complex number is defined up to multiples of $2 \pi$, we write:

$$w = r e^{i \left(\right. \theta + 2 k \pi \left.\right)} , k \in \mathbb{Z}$$

Applying De Moivre’s Theorem to $z^{n} = w$ and taking the $n$-th root of both sides, we obtain the general formula for the $n$-th roots:

$$z_{k} = \sqrt[n]{r} \cdot e^{i \left(\right. \frac{\theta + 2 k \pi}{n} \left.\right)} , \text{for} k = 0 , 1 , \ldots , n - 1$$

This gives all the $n$ distinct complex roots. They lie on a circle of radius $\sqrt[n]{r}$, equally spaced by an angle of $\frac{2 \pi}{n}$. This means the roots are arranged like the vertices of a regular polygon with $n$ sides inscribed in a circle of radius $\sqrt[n]{r}$. In the case of cube roots, we get three points on a circle, each separated by an angle of $\frac{2 \pi}{3}$, forming an equilateral triangle in the complex plane.

## Example 3

Let’s find all the complex solutions to the equation:

$$z^{3} = 1$$

At first glance, it seems obvious that $z = 1$ is a solution. But since we’re working in the complex plane, we know there are three cube roots in total, equally spaced around the [unit circle](https://algebrica.org/unit-circle).

---

Since the argument of a complex number is defined up to multiples of $2 \pi$, we write $1$ in exponential form as:

$$1 = e^{i \cdot 2 k \pi} , k \in \mathbb{Z}$$

Applying the general root formula with $r = 1$ and $\theta = 0$, we obtain:

$$z_{k} = \sqrt[3]{1} \cdot e^{i \left(\right. \frac{0 + 2 k \pi}{3} \left.\right)} = e^{i \cdot \frac{2 k \pi}{3}} , \text{for} k = 0 , 1 , 2$$

---

Let’s now evaluate the three roots explicitly.

For $k = 0$:

$$z_{0} = e^{i \cdot 0} = cos ⁡ \left(\right. 0 \left.\right) + i sin ⁡ \left(\right. 0 \left.\right) = 1$$

---

For $k = 1$:

$$z_{1} = e^{i \cdot \frac{2 \pi}{3}} = cos ⁡ \left(\right. \frac{2 \pi}{3} \left.\right) + i sin ⁡ \left(\right. \frac{2 \pi}{3} \left.\right) = - \frac{1}{2} + \frac{\sqrt{3}}{2} i$$

---

For $k = 2$:

$$z_{2} = e^{i \cdot \frac{4 \pi}{3}} = cos ⁡ \left(\right. \frac{4 \pi}{3} \left.\right) + i sin ⁡ \left(\right. \frac{4 \pi}{3} \left.\right) = - \frac{1}{2} - \frac{\sqrt{3}}{2} i$$

---

![](https://algebrica.org/wp-content/uploads/resources/images/roots-of-unit.png "De Moivre's Theorem.")

These are the three cube roots of 1, arranged in the complex plane like the vertices of an equilateral triangle. Together, they form what are known as the [cube roots of unity](https://algebrica.org/roots-of-unity/).

nth rootscomplex rootsroots of unitypowers of complex numberstrigonometric identitiesinduction proofperiodicityangle multiplicationtrigonometric linkgeometric meaningpower formulastatementprincipal argumentargumentmodulusexponential formtrigonometric formalgebraic formproof and usesde moivre theoremforms
