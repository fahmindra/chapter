---
layout: chapter
title: "Functions"
chapter: "Functions"
chapter_order: 14
section_order: 1
permalink: /materi-algebrica/functions/functions/
---

## What is a function

A function is a mathematical rule that connects two non-empty [subsets](https://algebrica.org/sets/) of the [real numbers](https://algebrica.org/real-numbers/), typically denoted as $A \subseteq \mathbb{R}$ and $B \subseteq \mathbb{R}$. A function $f$ from $A$ to $B$ assigns exactly one real number in $B$ to each real number in $A$. This relationship is written as:
$$f : A \rightarrow B$$

- The set $A$ is called the [domain](https://algebrica.org/#domain) of the function.
- The set $B$ is the codomain.
- For every $x \in A$, the function produces a unique value $f \left(\right. x \left.\right) \in B$.
- The variable $x$ is called the independent variable, while $y$ is the dependent variable.

![](https://algebrica.org/wp-content/uploads/resources/images/functions-5.png "Illustration showing the concept of a function with its domain and codomain.")

> If such a rule holds, we say that the function is well-defined. Otherwise, the relation is not a function, since it either assigns no value or more than one value to an element of the domain.

---

A function from a set $A$ (domain) to a set $B$ (codomain), $f : A \rightarrow B ,$ can be classified as:

- Injective: if every element of $B$ is the image of at most one element of $A$, that is, if for any $x_{1} , x_{2} \in A$ with $x_{1} \neq x_{2}$, we have $f \left(\right. x_{1} \left.\right) \neq f \left(\right. x_{2} \left.\right)$; equivalently, if for every $y \in B$ there is at most one $x \in A$ such that $f \left(\right. x \left.\right) = y$.
- Surjective: if every element of $B$ is the image of at least one element of $A$, that is, if $\forall y \in B$ there exists at least one $x \in A$ such that $f \left(\right. x \left.\right) = y .$
- Bijective: if the function is both injective and surjective, that is, if for every $y \in B$ there exists a unique $x \in A$ such that $f \left(\right. x \left.\right) = y$.

---

An alternative definition states that a function $f : A \rightarrow B$ is bijective if and only if there exists a function $g : B \rightarrow A$ such that:
$$\left(\right. g \circ f \left.\right) \left(\right. x \left.\right) = x , \forall x \in A$$
$$\left(\right. f \circ g \left.\right) \left(\right. y \left.\right) = y , \forall y \in B$$
Whenever such a function $g$ exists, it is uniquely determined. In this case $g$ is called the [inverse](https://algebrica.org/inverse-function/) of $f$ and is denoted by $f^{- 1}$.

> An example of an inverse function is the [logarithmic function](https://algebrica.org/logarithmic-function/), which serves as the inverse of the [exponential function](https://algebrica.org/exponential-function/), and conversely.

## What is not a function

For greater clarity, let us illustrate the case in which we face a situation similar to the one shown in the previous figure, but where it is not possible to define a function. In formal terms, this occurs when there exist at least two distinct points $\left(\right. x , y_{1} \left.\right)$ and $\left(\right. x , y_{2} \left.\right)$ such that $y_{1} \neq y_{2}$. In this case, the relation does not satisfy the definition of a function, since a single value of $x$ is associated with more than one value of $y$.

![What is not a function.](https://algebrica.org/wp-content/uploads/resources/images/functions-4-1.png "What is not a function.")

In the image, a single element of the domain, denoted by $x_{0}$, corresponds to two distinct values in the codomain. This situation is not admissible according to the very definition of a function. Formally, a relation $R \subseteq A \times B$ is a function if and only if:

$$\forall x \in A , \exists ! y \in B : \left(\right. x , y \left.\right) \in R$$

In this case, there exist $y_{1} , y_{2} \in B$ with $y_{1} \neq y_{2}$ such that $\left(\right. x_{0} , y_{1} \left.\right) \in R$ and $\left(\right. x_{0} , y_{2} \left.\right) \in R$ which violates the condition of uniqueness required for $R$ to be a function. In simpler terms, imagine a situation where certain values of $x$ are associated with corresponding values of $y$, as shown in the following table.

| X | -3 | 1 | -3 | 5 | 2 |
| --- | --- | --- | --- | --- | --- |
| Y | 7 | 4 | 10 | -2 | 8 |

In this case, the relation does not represent a function because for the same value $x = - 3$, there are two different corresponding values of $y$, namely $y = 7$ and $y = 10$. This violates the fundamental definition of a function, which requires that each element of the domain be associated with one and only one element of the codomain.

---

A practical graphical criterion for deciding whether a curve in the plane represents a function is the vertical line test. Draw any vertical line and count how many times it intersects the curve. If every vertical line meets the curve in at most one point, then the curve represents a function.

- For each value of $x$ there is at most one corresponding value of $y$.
- If some vertical line crosses the curve in two or more points, the curve does not represent a function, because that value of $x$ would be associated with multiple outputs.

![](https://algebrica.org/wp-content/uploads/resources/images/functions-10-1.png)

The figure shows that the curve on the left (a [parabola](https://algebrica.org/parabola/)) is a function, since each $x \left.\right) c o r r e s p o n d s t o e x a c t l y o n e \backslash( y$, whereas the curve on the right is not, since for $x_{2}$ there are multiple possible values of $y$.

## Difference between codomain and range

- The codomain is the set that we declare as the potential target of the outputs of a function. It is explicitly stated in the function’s definition. For instance, in a function written as $f : A \rightarrow B$, the set $B$ is the codomain.
- The range (or image) is the actual set of outputs that the function attains when evaluated over its domain. It includes all values $f \left(\right. x \left.\right)$ for $x \in A$. The range is always a subset of the codomain.

## Function equality and zeros

Two functions $y = f \left(\right. x \left.\right)$ and $y = g \left(\right. x \left.\right)$ are considered equal if they share the same domain $D$ and satisfy the condition:

$$f \left(\right. x \left.\right) = g \left(\right. x \left.\right) \forall x \in D$$

---

A real number $a \in \mathbb{R}$ is called a zero of the function $y = f \left(\right. x \left.\right)$ if the function evaluates to zero at that point, that is:

$$f \left(\right. a \left.\right) = 0$$

This means that the graph of the function intersects the x-axis at the point $\left(\right. a , 0 \left.\right)$. Identifying the zeros of a function is crucial for analyzing its behavior, solving [equations](https://algebrica.org/equations/), and determining where the function changes sign.

## Symmetric functions

When studying real-valued functions, it is often useful to understand how a function behaves with respect to reflections around the origin. This leads to the distinction between [even and odd functions](https://algebrica.org/even-and-odd-functions/). Let $A \subseteq \mathbb{R}$ be a domain that is symmetric with respect to the origin, meaning that $x \in A \Rightarrow - x \in A$. A function $f : A \rightarrow \mathbb{R}$ is said to be:

- Even if $f \left(\right. - x \left.\right) = f \left(\right. x \left.\right) \forall x \in A .$
- Odd if $f \left(\right. - x \left.\right) = - f \left(\right. x \left.\right) \forall x \in A .$

More generally, for the function $f \left(\right. x \left.\right) = x^{n}$ with $n \in \mathbb{N}$, the function is even exactly when the exponent $n$ is even, and it is odd exactly when $n$ is odd.

## Bounded functions

Before introducing the formal definitions, it is useful to reflect on how a real-valued function behaves across its entire domain. In many situations we want to know whether the function stays within certain limits, never rising above a fixed threshold or never dropping below one. A function $f : A \subseteq \mathbb{R} \rightarrow \mathbb{R}$ is said to be:

- Upper bounded if there exists a real number $M \in \mathbb{R}$ such that $f \left(\right. x \left.\right) \leq M$ $\forall x \in A .$
- Lower bounded if there exists a real number $m \in \mathbb{R}$ such that $m \leq f \left(\right. x \left.\right) \forall x \in A .$
- Bounded if it satisfies both conditions above, meaning that there exist $m , M \in \mathbb{R}$ for which $m \leq f \left(\right. x \left.\right) \leq M$ holds $\forall x \in A$.

---

It is important to distinguish between the notion of a bounded function and the existence of a [maximum or minimum](https://algebrica.org/maximum-minimum-and-inflection-points/). Saying that a function is bounded does not imply that it actually attains a maximal or minimal value, either globally or locally. The requirement of boundedness simply means that the values of the function remain confined within a finite interval $\left[\right. m , M \left]\right.$.

Of course, if a function has a global maximum, then it is automatically bounded from above. Similarly, the presence of a global minimum ensures that it is bounded from below. However, the converse is not true: a function may be bounded without attaining any maxima or minima. A typical example is:

$$f \left(\right. x \left.\right) = sin \left(\right. \frac{1}{x} \left.\right) x \neq 0$$

This function always stays between $- 1$ and $1$, so it is indeed bounded. Nevertheless, it has neither a global maximum nor a global minimum, because as $x$ approaches $0$ the oscillations become arbitrarily rapid and the function never reaches its extreme values.

## Monotone functions

In the analysis of real-valued functions, understanding whether a function increases, decreases, or maintains a consistent directional behavior is essential. These ideas are captured by the concepts of [increasing, decreasing, and monotone functions](https://algebrica.org/increasing-and-decreasing-functions/), which describe how the output values evolve as the input grows. Let $A \subseteq \mathbb{R}$ and let $x_{1} , x_{2} \in A$ with $x_{1} < x_{2}$. A function $f : A \rightarrow \mathbb{R}$ is said to be:

- Increasing if $f \left(\right. x_{1} \left.\right) \leq f \left(\right. x_{2} \left.\right) .$
- Strictly increasing if $f \left(\right. x_{1} \left.\right) < f \left(\right. x_{2} \left.\right) .$
- Decreasing if $f \left(\right. x_{1} \left.\right) \geq f \left(\right. x_{2} \left.\right) .$
- Strictly decreasing if $f \left(\right. x_{1} \left.\right) > f \left(\right. x_{2} \left.\right) .$
- Monotone if it satisfies one of the conditions above throughout its domain.

## Periodic functions

A function is called periodic when its values repeat after a fixed horizontal shift. More formally, if $X \subseteq \mathbb{R}$ and $T > 0$ is such that $x + T \in X$ whenever $x \in X$, a function:
$$f : X \rightarrow \mathbb{R}$$
is periodic with period $T$ when $T$ is the smallest positive number for which
 $$f \left(\right. x + T \left.\right) = f \left(\right. x \left.\right)$$
holds $\forall x$ in the domain. As a simple illustration, the [sine](https://algebrica.org/sine-function/) and [cosine functions](https://algebrica.org/cosine-function/) are periodic: both repeat their entire pattern after an interval of length $2 \pi$.

## Classification of functions

Functions are classified as algebraic or transcendental. A function is said to be algebraic if its analytical expression $y = f \left(\right. x \left.\right)$ involves only a finite number of operations such as addition, subtraction, multiplication, division, exponentiation to a rational [power](https://algebrica.org/powers/), and [root extraction](https://algebrica.org/radicals/). Algebraic functions can be further categorized based on the structure of their expressions:

- [Polynomial functions](https://algebrica.org/polynomial-function/) are defined by a [polynomial](https://algebrica.org/polynomials/) expression involving powers of $x$ with constant coefficients.
- Rational functions are expressed as the [ratio of two polynomials](https://algebrica.org/rational-equations/).
- Irrational functions contain the variable $x$ under a [root symbol](https://algebrica.org/radicals/), such as $\sqrt{x}$.

Transcendental functions go beyond algebraic operations and include expressions that cannot be written using a finite combination of addition, subtraction, multiplication, division, and root extraction. Common examples are [exponential functions](https://algebrica.org/exponential-function/), [logarithmic functions](https://algebrica.org/logarithmic-function/), and [trigonometric functions](https://algebrica.org/sine-function/).

## Domain of the main functions

Below we will review the domains of the most common elementary functions. In practice, however, many functions encountered in real problems are considerably more intricate, and their domains cannot be identified at a glance. For all such situations in which the structure of the expression makes the analysis less immediate, we refer to [this method](https://algebrica.org/determining-the-domain-of-a-function/), which provides a systematic way to determine the domain of more complex functions.

---

[Polynomial functions](https://algebrica.org/polynomial-function/) are defined by expressions of the form:

$$y = a_{0} x^{n} + a_{1} x^{n - 1} + \hdots + a_{n}$$

where $a_{0} , a_{1} , \ldots , a_{n}$ are real coefficients and $n \in \mathbb{N}$. The domain of a polynomial function is the entire set of real numbers, $\mathbb{R}$, since it does not involve any operations that could restrict its definition. An example of a polynomial function is:

$$y = 2 x^{3} - 5 x^{2} + 3 x - 1$$

This expression can be viewed as a linear combination of powers of $x$, where each term $a_{i} x^{i}$ has a real coefficient $a_{i}$. Polynomial functions of this type are defined for every real number $x \in \mathbb{R}$, since no operation in their form imposes any restriction on the domain.

---

[Rational functions](https://algebrica.org/rational-functions/) are expressed in the form:

$$y = \frac{N \left(\right. x \left.\right)}{D \left(\right. x \left.\right)}$$

where $N \left(\right. x \left.\right)$ and $D \left(\right. x \left.\right)$ are polynomials. These functions are defined for all real numbers $x$ such that $D \left(\right. x \left.\right) \neq 0$. The domain is therefore $\mathbb{R}$ excluding the values that make the denominator zero. An example of a rational function is:

$$y = \frac{x^{2} - 4}{x - 2}$$

This expression represents the ratio of two polynomials and can be interpreted as a linear combination of powers of $x$ in both the numerator and denominator. Rational functions of this type are defined for all real values of $x$ except those that make the denominator equal to zero. In this example, the function is undefined at $x = 2$, since it would make the denominator vanish.

---

Irrational functions are expressions of the form:

$$y = \sqrt[n]{f \left(\right. x \left.\right)}$$

The domain depends on the parity of the index $n$. If $n$ is even, the function is defined only when $f \left(\right. x \left.\right) \geq 0$, so the domain is:

$$x \in \mathbb{R} \mid f \left(\right. x \left.\right) \geq 0$$

An example of an irrational function with an even index is:

$$y = \sqrt{x - 2}$$

In this case, the expression under the radical must be non-negative, so the domain is given by $x \geq 2$. The function is therefore defined only for values of $x$ that make the radicand $x - 2$ greater than or equal to zero. If $n$ is odd, the function is defined for every value in the domain of $f \left(\right. x \left.\right)$. An example with an odd index is:

$$y = \sqrt[3]{x - 2}$$

Here, the cube root is defined for every real value of $x$, since odd roots can also take negative arguments. Thus, the domain of the function is the entire set of real numbers, $\mathbb{R}$.

---

[Logarithmic functions](https://algebrica.org/logarithmic-function/) are defined as:

$$y = log_{a} ⁡ f \left(\right. x \left.\right) \text{with} a > 0 , a \neq 1$$

They are defined only when the argument of the [logarithm](https://algebrica.org/logarithms/) is strictly positive. Therefore, their domain is:

$$x \in \mathbb{R} \mid f \left(\right. x \left.\right) > 0$$

An example of a logarithmic function is:

$$y = log_{2} ⁡ \left(\right. x - 1 \left.\right)$$

This function is defined only when the argument of the logarithm, $x - 1$, is strictly positive. Therefore, the domain is $x > 1$. For any value of $x$ less than or equal to $1$, the expression becomes undefined because the [logarithm](https://algebrica.org/logarithms/) of a non-positive number does not exist in the real domain. Another example is:

$$y = ln ⁡ \left(\right. 3 x + 6 \left.\right)$$

In this case, the argument $3 x + 6$ must also be positive, so the domain is $x > - 2$. The same principle applies to all logarithmic functions: the argument of the logarithm must always be greater than zero for the function to be defined.

---

[Exponential functions](https://algebrica.org/exponential-function/) of the form:

$$y = a^{f \left(\right. x \left.\right)} \text{with} a > 0 , a \neq 1$$

are defined for all values in the domain of $f \left(\right. x \left.\right)$. An example of an exponential function is:

$$y = 2^{x}$$

This function is defined for every real value of $x$, since the base $a = 2$ is positive and different from $1$. Its domain is therefore the entire set of real numbers, $\mathbb{R}$, while the range is strictly positive, $y > 0$.

---

Exponential functions of the form:

$$y = \left[\right. f \left(\right. x \left.\right) \left]\right.^{g \left(\right. x \left.\right)}$$

are defined only when the base $f \left(\right. x \left.\right) > 0$, since real-valued exponentiation requires a positive base. Therefore, their domain is the intersection of:

$$\left{\right. x \in \mathbb{R} \mid f \left(\right. x \left.\right) > 0 \left.\right} \cap \text{domain of} g \left(\right. x \left.\right)$$

---

Exponential functions of the form:

$$f \left(\right. x \left.\right)^{\alpha}$$

where $\alpha \in \mathbb{R} \backslash \mathbb{Q}$ are defined under the following conditions:

$$\left{\right. x \in \mathbb{R} \mid f \left(\right. x \left.\right) \geq 0 \left.\right} , \text{if} \alpha > 0$$
$$\left{\right. x \in \mathbb{R} \mid f \left(\right. x \left.\right) > 0 \left.\right} , \text{if} \alpha < 0$$

This ensures that the result of the expression remains within the set of real numbers.

---

For trigonometric functions, the following domains apply:

$y = sin ⁡ x , y = cos ⁡ x$
 Domain: $\mathbb{R}$

$y = tan ⁡ x$
 Domain: $\mathbb{R} \backslash \left{\right. \frac{\pi}{2} + k \pi \left.\right} , k \in \mathbb{Z}$

$y = cot ⁡ x$
 Domain: $\mathbb{R} \backslash \left{\right. k \pi \left.\right} , k \in \mathbb{Z}$

$y = arcsin ⁡ x , y = arccos ⁡ x$
 Domain: $\left[\right. - 1 , 1 \left]\right.$

$y = arctan ⁡ x , y = \text{arccot} x$
 Domain: $\mathbb{R}$

> Understanding the domain of a function is a crucial step in solving equations, inequalities, and in [analyzing functions](https://algebrica.org/analyzing-the-graphs-of-functions/). In most cases, identifying the domain involves recognizing a few fundamental situations, summarized below.

## Operations between functions

When two real functions are defined on the same domain, it is possible to combine them through the usual algebraic operations, obtaining new functions derived from the original ones. This generalizes the basic arithmetic of real numbers to the context of functions, where each operation is applied point by point for every value of $x$ in the domain. In formal terms, if

$$f : X_{1} \subseteq \mathbb{R} \rightarrow \mathbb{R} \text{and} g : X_{2} \subseteq \mathbb{R} \rightarrow \mathbb{R}$$

are two functions, we define: $X = X_{1} \cap X_{2}$ as the common domain on which the following operations can be performed.

---

The sum of two functions $f$ and $g$ is defined by:

$$\left(\right. f + g \left.\right) \left(\right. x \left.\right) = f \left(\right. x \left.\right) + g \left(\right. x \left.\right)$$

The resulting function assigns to each $x \in X$ the sum of the corresponding values of $f$ and $g$.

---

The difference of two functions is given by:

$$\left(\right. f - g \left.\right) \left(\right. x \left.\right) = f \left(\right. x \left.\right) - g \left(\right. x \left.\right)$$

---

The product of two functions is defined as:

$$\left(\right. f \cdot g \left.\right) \left(\right. x \left.\right) = f \left(\right. x \left.\right) g \left(\right. x \left.\right)$$

The resulting function represents the pointwise multiplication of the two values.

---

The quotient of two functions is expressed by

$$\left(\right. \frac{f}{g} \left.\right) \left(\right. x \left.\right) = \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)}$$

but it is defined only for those values of $x \in X$ where $g \left(\right. x \left.\right) \neq 0$. The domain of this function is therefore obtained by excluding from $X$ all points that make the denominator vanish.

---

The composition of two functions, written $\left(\right. g \circ f \left.\right) \left(\right. x \left.\right) = g \left(\right. f \left(\right. x \left.\right) \left.\right)$, is another fundamental operation and is treated in detail on the dedicated page on [composite functions](https://algebrica.org/composite-functions/).

compositionquotientproductdifferencesumperiodicitymonotonicityboundednesssymmetryinversebijectivesurjectiveinjectivenot a functiongraphrangecodomaindomainmapping ruleoperationspropertiesdefinition
