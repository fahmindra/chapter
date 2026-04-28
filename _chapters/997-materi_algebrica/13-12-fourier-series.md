---
layout: chapter
title: "Fourier Series"
chapter: "Series"
chapter_order: 13
section_order: 12
permalink: /materi-algebrica/series/fourier-series/
---

## Definition

A Fourier series represents a periodic function as an infinite sum of [sine](https://algebrica.org/sine-function/) and [cosine functions](https://algebrica.org/cosine-function). More precisely, it shows that periodic behavior can be decomposed into elementary harmonic oscillations. This result expresses a structural property of periodic [functions](https://algebrica.org/functions): oscillatory components form a natural coordinate system for describing repetition.

---

Let $f : \mathbb{R} \rightarrow \mathbb{R}$ be a function that is periodic with period $2 \pi$, meaning:

$$f \left(\right. x + 2 \pi \left.\right) = f \left(\right. x \left.\right) \forall x \in \mathbb{R}$$

Assume that $f$ is [integrable](https://algebrica.org/definite-integrals/) on the [interval](https://algebrica.org/intervals/) $\left[\right. - \pi , \pi \left]\right.$. The Fourier series of $f$ is the formal trigonometric expansion:

$$f \left(\right. x \left.\right) sim \frac{a_{0}}{2} + \sum_{n = 1}^{\infty} a_{n} cos ⁡ \left(\right. n x \left.\right) + b_{n} sin ⁡ \left(\right. n x \left.\right)$$

- The symbol $sim$ emphasizes that we are not yet asserting equality (we are defining a trigonometric series associated with $f$).
- The question of whether the series converges to $f$ will be addressed later.
- Each term $cos ⁡ \left(\right. n x \left.\right)$ and $sin ⁡ \left(\right. n x \left.\right)$ represents an oscillation of frequency $n$.
- The expansion therefore decomposes $f$ into its harmonic components.

## Fourier Coefficients

The coefficients $a_{n}$ and $b_{n}$ are defined by the following integrals:

$$a_{0} & = \frac{1}{\pi} \int_{- \pi}^{\pi} f \left(\right. x \left.\right) d x \\ a_{n} & = \frac{1}{\pi} \int_{- \pi}^{\pi} f \left(\right. x \left.\right) cos ⁡ \left(\right. n x \left.\right) d x \\ b_{n} & = \frac{1}{\pi} \int_{- \pi}^{\pi} f \left(\right. x \left.\right) sin ⁡ \left(\right. n x \left.\right) d x n \geq 1$$

These expressions are not introduced by convention, and they are not chosen just because they work. They follow from a structural fact about [sines and cosines](https://algebrica.org/sine-and-cosine/): over a full period they are orthogonal to one another. On the interval $\left[\right. - \pi , \pi \left]\right.$, trigonometric waves with different frequencies remain independent under integration, which is exactly what lets us isolate one harmonic at a time and read off the corresponding coefficient.

$$\int_{- \pi}^{\pi} cos ⁡ \left(\right. n x \left.\right) cos ⁡ \left(\right. m x \left.\right) d x & = \left{\right. \begin{matrix}\pi & n = m \neq 0 \\ 0 & n \neq m\end{matrix} \\ \int_{- \pi}^{\pi} sin ⁡ \left(\right. n x \left.\right) sin ⁡ \left(\right. m x \left.\right) d x & = \left{\right. \begin{matrix}\pi & n = m \\ 0 & n \neq m\end{matrix} \\ \int_{- \pi}^{\pi} sin ⁡ \left(\right. n x \left.\right) cos ⁡ \left(\right. m x \left.\right) d x & = 0$$

These relations imply that the trigonometric system behaves like an orthogonal basis under the inner product:

$$\langle f , g \rangle = \int_{- \pi}^{\pi} f \left(\right. x \left.\right) g \left(\right. x \left.\right) d x$$

Each coefficient measures how much of a specific harmonic direction is present in the function. In this sense, the Fourier expansion is a projection process in an infinite-dimensional space.

## Example 1

This example illustrates how even a simple linear function acquires a rich harmonic structure when periodically extended. Consider the function $f \left(\right. x \left.\right) = x$, defined on $\left(\right. - \pi , \pi \left.\right)$ and extended periodically with period $2 \pi$. This function is odd. Therefore:

$$a_{0} = 0 a_{n} = 0$$

We compute the [sine](https://algebrica.org/sine-and-cosine/) coefficients:

$$b_{n} = \frac{1}{\pi} \int_{- \pi}^{\pi} x sin ⁡ \left(\right. n x \left.\right) d x$$

Using [integration by parts](https://algebrica.org/integration-by-parts/), we obtain:

$$b_{n} = \frac{2 \left(\right. - 1 \left.\right)^{n + 1}}{n}$$

Hence the Fourier series is:

$$x sim 2 \sum_{n = 1}^{\infty} \frac{\left(\right. - 1 \left.\right)^{n + 1}}{n} sin ⁡ \left(\right. n x \left.\right)$$

###### The coefficients decay like $\frac{1}{n}$. The slower decay reflects the fact that $f$ is continuous but not differentiable at the endpoints of the period. The periodic extension introduces jump discontinuities at multiples of $\pi$, which influences convergence behavior.

## Convergence of Fourier series

The definition of the Fourier series does not automatically guarantee convergence to the original function. A classical result states that if $f$ satisfies the following [Dirichlet conditions](https://algebrica.org/dirichlet-function/):

- $f$ is piecewise continuous
- $f$ has finitely many local extrema in $\left[\right. - \pi , \pi \left]\right.$
- $f$ has finitely many jump discontinuities

then the Fourier series converges at every point $x .$ More precisely consider the $N$-th partial sum:

$$S_{N} \left(\right. x \left.\right) = \frac{a_{0}}{2} + \sum_{n = 1}^{N} a_{n} cos ⁡ \left(\right. n x \left.\right) + b_{n} sin ⁡ \left(\right. n x \left.\right)$$

$$\underset{N \rightarrow \infty}{lim} S_{N} \left(\right. x \left.\right) = \frac{f \left(\right. x^{+} \left.\right) + f \left(\right. x^{-} \left.\right)}{2}$$

At points where $f$ is continuous, the series converges to $f \left(\right. x \left.\right)$. At jump discontinuities, it converges to the midpoint of the left and right [limits](https://algebrica.org/limits). This behavior reveals a fundamental property of Fourier approximation: it respects average local behavior rather than pointwise values at discontinuities.

- If $f$ is continuously differentiable, coefficients decay faster.
- If $f$ has discontinuities, decay is slower.
- The smoother the function, the more rapidly the harmonic amplitudes decrease.

## Selected references

- **E. M. Stein, R. Shakarchi**. [Fourier Analysis: An Introduction](https://kryakin.site/am2/Stein-Shakarchi-1-Fourier_Analysis.pdf)
- **L. Grafakos**. [Classical Fourier Analysis](https://www.math.stonybrook.edu/~bishop/classes/math638.F20/Grafakos_Classical_Fourier_Analysis.pdf)
- **G. P. Tolstov**. [Fourier Series](https://archive.org/embed/tolstov-fourier-series-1962)
- **G. B. Folland**. [Fourier Analysis and Its Applications](https://www-elec.inaoep.mx/~rogerio/Tres/FourierAnalysisUno.pdf)
- **A. Zygmund**. [Trigonometric Series](https://archive.org/details/trigonometricseries)
- **Y. Katznelson**. [An Introduction to Harmonic Analysis](https://archive.org/details/introductiontoha0000katz)
- **Stanford University**. [The Fourier Transform and Its Applications](https://see.stanford.edu/materials/lsoftaee261/book-fall-07.pdf)
- **Oxford University Press**. [Fourier Series and Fourier Transforms](https://academic.oup.com/book/54863/chapter/422699978)
- **R. Herman**. [An Introduction to Fourier and Complex Analysis](https://people.uncw.edu/hermanr/mat367/fcabook/FCA)
