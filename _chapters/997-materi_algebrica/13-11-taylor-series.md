---
layout: chapter
title: "Taylor Series"
chapter: "Series"
chapter_order: 13
section_order: 11
permalink: /materi-algebrica/series/taylor-series/
---

## Introduction

The idea behind a Taylor series is to replace a function with an infinite [polynomial](https://algebrica.org/polynomials/) whose coefficients are entirely determined by the local behaviour of the function at a single point. This perspective reduces the study of a wide class of [functions](https://algebrica.org/functions/) to the algebraic manipulation of [power series](https://algebrica.org/power-series/) and at the same time it provides a constructive way to approximate values that would otherwise be inaccessible by elementary means.

Throughout this page we shall assume familiarity with the notion of [derivative](https://algebrica.org/derivatives/) of arbitrary order and with the basic theory of power series, in particular with the notion of radius of convergence.

## Analytic functions and the motivating problem

Let $f$ be a real function defined on an open interval containing the point $a$. The question we want to address is whether it is possible to represent $f$ on a neighbourhood of $a$ by means of an expression of the form:

$$f \left(\right. x \left.\right) = \sum_{n = 0}^{\infty} c_{n} \left(\right. x - a \left.\right)^{n}$$

The coefficients $c_{n}$ are [real numbers](https://algebrica.org/real-numbers/) and the series converges in some [interval](https://algebrica.org/intervals/) centred at $a$. When such a representation exists with positive radius of convergence, the function is said to be analytic at $a$.

---

The class of analytic functions is nevertheless extremely rich and includes essentially every elementary function on its [domain](https://algebrica.org/determining-the-domain-of-a-function/): polynomials, [exponentials](https://algebrica.org/exponential-function/), [logarithms](https://algebrica.org/logarithmic-function/) on the positive half-line, trigonometric and hyperbolic functions, [rational functions](https://algebrica.org/rational-functions/) away from their poles, and roots away from branch points. The functions that fail to be analytic at a given point are those that exhibit a singular behaviour there, such as a vertical tangent, an infinite value, or some form of irregular oscillation.

## Determination of the coefficients

The main observation is that, if a representation of the form written above exists, then the coefficients $c_{n}$ are determined by $f$ and its derivatives at $a$. To see this, recall that within the radius of convergence a power series can be differentiated term by term, and the resulting series has the same radius of convergence as the original one. Setting $x = a$ in the original series leaves only the term with $n = 0$, so we obtain:

$$c_{0} = f \left(\right. a \left.\right)$$

Differentiating once and then evaluating at $a$ again eliminates all term except for the one corresponding to $n = 1$, yielding:

$$c_{1} = f^{'} \left(\right. a \left.\right)$$

Differentiating twice produces a factor $2 \cdot 1$ in front of $c_{2}$, so that:

$$c_{2} = \frac{f^{''} \left(\right. a \left.\right)}{2 !}$$

Iterating this procedure, the $N$-th derivative of the series evaluated at $a$ yields a single non-vanishing term, which carries the [factorial](https://algebrica.org/factorial/) $N !$ and the coefficient $c_{N}$. The general formula is therefore:

$$c_{n} = \frac{f^{\left(\right. n \left.\right)} \left(\right. a \left.\right)}{n !}$$

This computation, which is essentially algebraic once term-by-term differentiation has been justified, is the content of the following statement.

## The Taylor series theorem

Let $f$ be analytic at $a$, so that there exist coefficients $c_{n}$ and a positive radius $R$ for which, for $\left|\right. x - a \left|\right. < R$ holds:

$$f \left(\right. x \left.\right) = \sum_{n = 0}^{\infty} c_{n} \left(\right. x - a \left.\right)^{n}$$

Then the coefficients are given by:

$$c_{n} = \frac{f^{\left(\right. n \left.\right)} \left(\right. a \left.\right)}{n !} n = 0 , 1 , 2 , \ldots$$

The representation takes the explicit form:

$$f \left(\right. x \left.\right) = \sum_{n = 0}^{\infty} \frac{f^{\left(\right. n \left.\right)} \left(\right. a \left.\right)}{n !} \left(\right. x - a \left.\right)^{n}$$

This expression is called the Taylor series of $f$ centred at $a$. When the centre is chosen at the origin (when $a = 0$), the series is referred to as the Maclaurin series of $f$.

> A common source of confusion concerns the meaning of the symbols $f^{\left(\right. n \left.\right)} \left(\right. a \left.\right)$. These are real numbers, obtained by computing the $n$-th derivative as a function of $x$ and then evaluating at the centre $a$. They are not functions of $x$ and the variable $x$ appears only through the factors $\left(\right. x - a \left.\right)^{n}$.

## Taylor polynomials and the formula with remainder

In practice the infinite series cannot be summed exactly and one truncates it after a finite number of terms. The following polynomial is called the Taylor polynomial of $f$ of order $N$ centred at $a$:

$$T_{N} \left(\right. x \left.\right) = \sum_{n = 0}^{N} \frac{f^{\left(\right. n \left.\right)} \left(\right. a \left.\right)}{n !} \left(\right. x - a \left.\right)^{n}$$

The first non-trivial case, corresponding to $N = 1$, recovers the linear approximation:

$$T_{1} \left(\right. x \left.\right) = f \left(\right. a \left.\right) + f^{'} \left(\right. a \left.\right) \left(\right. x - a \left.\right)$$

whose graph is the tangent line to $f$ at $a$. Higher-order Taylor polynomials provide successively better local approximations, in the sense that they share with $f$ an increasing number of [derivatives](https://algebrica.org/derivatives/) at the centre. The discrepancy between the function and its $N$-th Taylor polynomial is called the remainder of order $N$ and is denoted as:

$$R_{N} \left(\right. x \left.\right) = f \left(\right. x \left.\right) - T_{N} \left(\right. x \left.\right)$$

If $f$ is of class $C^{N + 1}$ on an interval containing both $a$ and $x$, then there exists a point $\xi$ strictly between $a$ and $x$ such that:

$$R_{N} \left(\right. x \left.\right) = \frac{f^{\left(\right. N + 1 \left.\right)} \left(\right. \xi \left.\right)}{\left(\right. N + 1 \left.\right) !} \left(\right. x - a \left.\right)^{N + 1}$$

Saying that the Taylor series of $f$ converges to $f$ on an interval is therefore equivalent to saying that $R_{N} \left(\right. x \left.\right) \rightarrow 0$ as $N \rightarrow \infty$ for every $x$ in that interval.

> The mere existence of all derivatives of $f$ at $a$ is sufficient to write down the Taylor series formally, but it does not guarantee that the series converges to $f$. The convergence must be checked separately, and this is precisely the role of the remainder.

## Maclaurin series of the exponential function

Consider the function $f \left(\right. x \left.\right) = e^{x}$, which satisfies the elementary differential identity $f^{'} \left(\right. x \left.\right) = f \left(\right. x \left.\right)$. Every derivative of $f$ coincides with $f$ itself and evaluating at the origin, for every $n \geq 0$, yields:

$$f^{\left(\right. n \left.\right)} \left(\right. 0 \left.\right) = e^{0} = 1$$

The Maclaurin coefficients are therefore $c_{n} = 1 / n !$, and the resulting series is:

$$e^{x} = \sum_{n = 0}^{\infty} \frac{x^{n}}{n !} = 1 + x + \frac{x^{2}}{2 !} + \frac{x^{3}}{3 !} + \hdots$$

To establish convergence for every real $x$ it suffices to apply the ratio test to the absolute values of the terms:

$$\underset{n \rightarrow \infty}{lim} \left|\right. \frac{x^{n + 1} / \left(\right. n + 1 \left.\right) !}{x^{n} / n !} \left|\right. = \underset{n \rightarrow \infty}{lim} \frac{\left|\right. x \left|\right.}{n + 1} = 0$$

Since the limit is zero regardless of $x$, the series converges absolutely on the whole real line, and one can verify through the Lagrange remainder that its sum is precisely $e^{x}$.

## Maclaurin series of sine and cosine

The functions [sine](https://algebrica.org/sine-function/) and [cosine](https://algebrica.org/cosine-function/) are perhaps the most instructive example because their derivatives cycle through a period of length four. For $f \left(\right. x \left.\right) = sin ⁡ x$ we have:

$$f \left(\right. x \left.\right) & = sin ⁡ x \\ f^{'} \left(\right. x \left.\right) & = cos ⁡ x \\ f^{''} \left(\right. x \left.\right) & = - sin ⁡ x \\ f^{′^{''}} \left(\right. x \left.\right) & = - cos ⁡ x$$

From the fourth derivative onwards the pattern repeats. Evaluating at the origin we obtain the following sequence:

$$0 , 1 , 0 , - 1 , 0 , 1 , 0 , - 1 , \ldots$$

So that all even-indexed coefficients vanish and the odd-indexed ones alternate in sign. Substituting into the general formula gives:

$$sin ⁡ x = \sum_{n = 0}^{\infty} \left(\right. - 1 \left.\right)^{n} \frac{x^{2 n + 1}}{\left(\right. 2 n + 1 \left.\right) !} = x - \frac{x^{3}}{3 !} + \frac{x^{5}}{5 !} - \frac{x^{7}}{7 !} + \hdots$$

An analogous computation, starting from $f \left(\right. x \left.\right) = cos ⁡ x$, yields:

$$cos ⁡ x = \sum_{n = 0}^{\infty} \left(\right. - 1 \left.\right)^{n} \frac{x^{2 n}}{\left(\right. 2 n \left.\right) !} = 1 - \frac{x^{2}}{2 !} + \frac{x^{4}}{4 !} - \frac{x^{6}}{6 !} + \hdots$$

The ratio test, applied as in the case of the exponential, shows that both series converge for every real $x$. Note that the same series interpreted with [complex arguments](https://algebrica.org/complex-numbers-introduction/) are the foundation of Euler’s identity $e^{i x} = cos ⁡ x + i sin ⁡ x$, but this connection lies beyond the scope of the present discussion.

> The fact that the Maclaurin series of $sin ⁡ x$ contains only odd powers, and that of $cos ⁡ x$ only even powers, is a manifestation of the [parity](https://algebrica.org/even-and-odd-functions/) of these functions: $sin$ is odd and $cos$ is even.

## Maclaurin series of the logarithm

The [logarithmic function](https://algebrica.org/logarithmic-function/) presents an additional subtlety, because $ln ⁡ x$ is not defined at the origin. To obtain a Maclaurin series we therefore consider the shifted function $f \left(\right. x \left.\right) = ln ⁡ \left(\right. 1 + x \left.\right)$, which is well defined and infinitely differentiable on the interval $\left(\right. - 1 , + \infty \left.\right)$. Computing successive derivatives we find:

$$f^{\left(\right. n \left.\right)} \left(\right. x \left.\right) = \left(\right. - 1 \left.\right)^{n - 1} \frac{\left(\right. n - 1 \left.\right) !}{\left(\right. 1 + x \left.\right)^{n}} \text{for} n \geq 1$$

Evaluating at the origin yields $f^{\left(\right. n \left.\right)} \left(\right. 0 \left.\right) = \left(\right. - 1 \left.\right)^{n - 1} \left(\right. n - 1 \left.\right) !$. The corresponding coefficients are $c_{n} = \left(\right. - 1 \left.\right)^{n - 1} / n$, and the Maclaurin series reads:

$$ln ⁡ \left(\right. 1 + x \left.\right) = \sum_{n = 1}^{\infty} \left(\right. - 1 \left.\right)^{n - 1} \frac{x^{n}}{n} = x - \frac{x^{2}}{2} + \frac{x^{3}}{3} - \frac{x^{4}}{4} + \hdots$$

The ratio test shows that the radius of convergence is exactly equal to $1$, and a more delicate analysis at the boundary establishes convergence at $x = 1$, with the celebrated identity:

$$ln ⁡ 2 = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \hdots$$

## The binomial series

A further fundamental example is provided by the function $f \left(\right. x \left.\right) = \left(\right. 1 + x \left.\right)^{\alpha}$, where $\alpha$ is an arbitrary real exponent. When $\alpha$ is a non-negative [integer](https://algebrica.org/integers/) the function is a polynomial and the Maclaurin series reduces to the binomial expansion of Newton. For a general real exponent the situation is more interesting, since the series is infinite and its convergence depends on the magnitude of $x$. Successive differentiation gives:

$$f^{\left(\right. n \left.\right)} \left(\right. x \left.\right) = \alpha \left(\right. \alpha - 1 \left.\right) \hdots \left(\right. \alpha - n + 1 \left.\right) \left(\right. 1 + x \left.\right)^{\alpha - n}$$

Evaluation at the origin yields the generalised [binomial coefficients](https://algebrica.org/binomial-coefficient/):

$$\left(\right. \frac{\alpha}{n} \left.\right) = \frac{\alpha \left(\right. \alpha - 1 \left.\right) \hdots \left(\right. \alpha - n + 1 \left.\right)}{n !}$$

The Maclaurin series therefore takes the form:

$$\left(\right. 1 + x \left.\right)^{\alpha} = \sum_{n = 0}^{\infty} \left(\right. \frac{\alpha}{n} \left.\right) x^{n}$$

> Note that one can show that it converges to $\left(\right. 1 + x \left.\right)^{\alpha}$ on the open interval $\left|\right. x \left|\right. < 1$.

## Example

To appreciate the practical strength of the method we compute an approximation of $sin ⁡ \left(\right. 10^{\circ} \left.\right)$. Trigonometric arguments must first be expressed in radians, so we write

$$10^{\circ} = \frac{\pi}{180} \cdot 10 = \frac{\pi}{18}$$

The value $\pi / 18$ is approximately $0.1745$, which is small enough to expect rapid convergence of the Maclaurin series. Truncating after the cubic term we obtain:

$$sin ! \left(\right. \frac{\pi}{18} \left.\right) \approx \frac{\pi}{18} - \frac{1}{3 !} \left(\left(\right. \frac{\pi}{18} \left.\right)\right)^{3}$$

Substituting a sufficiently accurate value of $\pi$ and performing the arithmetic, the Taylor polynomial of order three already yields $sin ⁡ \left(\right. 10^{\circ} \left.\right) \approx 0.173648$, in agreement with the true value to five decimal places.

## Choice of the centre

An essential aspect of the method concerns the choice of the centre $a$ of the expansion. The choice is constrained by three requirements that must be balanced against one another:

- the function must be analytic at $a .$
- the value $f \left(\right. a \left.\right)$ and the derivatives $f^{\left(\right. n \left.\right)} \left(\right. a \left.\right)$ must be computable in closed form.
- the distance $\left|\right. x - a \left|\right.$ must be small enough to fall within the radius of convergence and to ensure rapid decay of the terms.

To illustrate this point, suppose we wish to compute $\sqrt{2}$ by means of the Taylor series of $f \left(\right. x \left.\right) = \sqrt{x}$. The candidate $a = 0$ is excluded, because $\sqrt{x}$ is not analytic at the origin: a series in non-negative powers of $x$ would force the function to be defined for negative arguments, which is impossible.

The choice $a = 1$ gives convergent derivatives, but the distance $\left|\right. 2 - 1 \left|\right. = 1$ coincides with the radius of convergence and the series converges extremely slowly. The choice $a = 2$ is circular, since computing $f \left(\right. 2 \left.\right)$ is exactly the problem we wish to solve. A compromise is $a = 9 / 4$, because $\sqrt{9 / 4} = 3 / 2$ is rational, the distance $\left|\right. 2 - 9 / 4 \left|\right. = 1 / 4$ is small, and the derivatives can be evaluated explicitly. With this choice the partial sums of the Taylor series converge to $\sqrt{2}$ at a satisfactory rate, and a few terms suffice to obtain five-digit accuracy.

The result of this construction is that $\sqrt{2} \approx 1.41421$, already attained by the Taylor polynomial of order four centred at $9 / 4$.

## Smooth functions that are not analytic

It is natural to wonder whether infinite differentiability alone is enough to guarantee that a function coincides with the sum of its Taylor series. The answer is negative, and the standard counterexample is the function:

$$f \left(\right. x \left.\right) = \left{\right. e^{- 1 / x^{2}} & \text{if} x \neq 0 \\ 0 & \text{if} x = 0$$

A direct computation, based on the fact that exponentials decay faster than any polynomial growth, shows that all derivatives of $f$ at the origin are equal to zero. Consequently the Maclaurin series of $f$ is identically zero,

$$\sum_{n = 0}^{\infty} \frac{f^{\left(\right. n \left.\right)} \left(\right. 0 \left.\right)}{n !} x^{n} = 0$$

Yet the function itself takes strictly positive values for every $x \neq 0$. The Taylor series exists, converges everywhere, but does not represent the function except at the single point $x = 0$. This phenomenon clarifies once more that analyticity is a stronger property than $C^{\infty}$ regularity, and that the Lagrange remainder cannot be ignored.

## Applications

The range of applications of Taylor series extends far beyond the numerical evaluation of functions. Three classes of problems deserve to be mentioned at least briefly.

The first concerns the computation of [limits of indeterminate form](https://algebrica.org/indeterminate-forms/). Replacing each factor of an expression by a Taylor polynomial of suitable order often reveals the dominant behaviour and resolves indeterminacies of type $0 / 0$ without recourse to repeated applications of de l’Hôpital’s rule. For instance, the well-known limit $\underset{x \rightarrow 0}{lim} \left(\right. sin ⁡ x \left.\right) / x = 1$ follows immediately from the Maclaurin series of the sine, since $\left(\right. sin ⁡ x \left.\right) / x = 1 - x^{2} / 6 + O \left(\right. x^{4} \left.\right)$ tends to $1$ as $x \rightarrow 0$.

The second class concerns the integration of functions whose antiderivatives cannot be expressed in elementary terms. The following [integrals](https://algebrica.org/integrals/) have no representation in closed form:

$$\int e^{- x^{2}} d x \text{and} \int \frac{sin ⁡ x}{x} d x$$

Their integrands admit Maclaurin series that can be integrated term by term, producing series representations of the antiderivatives that are perfectly suited for numerical evaluation.

The third class concerns the resolution of differential equations by series methods. Seeking a solution in the form of a power series and substituting into the equation produces a recurrence relation for the coefficients, which in many cases can be solved explicitly. Several special functions of mathematical physics, including the Bessel and Legendre functions, are most naturally defined in this way.

> We close with a remark of a more conceptual nature. The Taylor series construction shows that the entire global behaviour of an analytic function is encoded in the sequence of its derivatives at a single point. This rigidity is one of the defining features of the analytic category and has no counterpart among smooth functions, where local data and global behaviour are to a large extent independent. The same rigidity reappears, in an even more striking form, in the theory of holomorphic functions of a complex variable, where it leads to the principle of analytic continuation and to the celebrated identity theorem. The real-variable Taylor series presented here is the elementary face of a phenomenon that pervades large portions of modern analysis.

non analyticchoice centreexamplesconvergenceremaindertaylor polynomialsterm differentiationuniquenessmaclaurin casetaylor theoremcoeff formuladerivativescoefficientsradius convergencecentre alocal representationpower seriesanalytic functionsapplicationsconstructionfoundations
