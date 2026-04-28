---
layout: chapter
title: "Equations with Parameters"
chapter: "Equations"
chapter_order: 7
section_order: 20
permalink: /materi-algebrica/equations/equations-with-parameters/
---

no solutioninfinitely many solutionsdegenerate casesunique solutiondeterminant conditioncoefficient matrixclassification of rootsdiscriminant functionparameter dependent coefficientsdegenerate equationvanishing coefficient caseunique solution casecoefficient function a(k)dependence of solutionsparameters in coefficientsfamily of equationsparameter vs unknownsystems with parametersquadratic equationslinear equationsconcept of parameters

## Introduction

A parametric equation refers to a family of [equations](https://algebrica.org/equations/) indexed by a real quantity that is allowed to vary freely. This quantity, known as a parameter, appears among the coefficients of the equation and is regarded as a constant during the process of solving for the unknown, despite its value not being specified in advance.

A parameter differs from an ordinary unknown in that its value is fixed temporarily to solve the equation for the remaining variable. Subsequently, the behaviour of the solutions is analysed as the parameter varies. This distinction is significant from the outset. For example, in the following equation, both the structure and the solution are completely determined:

$$2 x + 3 = 7$$

The situation changes when the equation is written as follows:

$$k x + 3 = 7$$

More generally we have:

$$k x + m = 0$$

In this context, $k$ and $m$ are real parameters, and the equation defines not a single algebraic problem but an entire family of problems, one for each admissible pair $\left(\right. k , m \left.\right)$.

Solving an equation with parameters involves determining, for each parameter configuration, the values of the unknowns that satisfy the equation, and analysing how these values depend on the parameter.

---

A parameter is defined as a real number that remains fixed within a single instance of an equation, whereas the unknown refers to the variable being solved for. The same symbol may assume different roles depending on the problem’s framing.

For example, in the equation $a x + b = 0$, if the objective is to find the value of $x$ that satisfies the equation, then $a$ and $b$ serve as parameters and $x$ is the unknown. Conversely, if the question concerns which pairs $\left(\right. a , b \left.\right)$ yield a solution equal to $1$, then $a$ and $b$ become the unknowns.

The term parametric equations commonly appears in calculus and analytic geometry to describe curves whose coordinates are expressed as functions of a common variable, such as $x \left(\right. t \left.\right)$ and $y \left(\right. t \left.\right)$. In this context, however, the term refers to equations whose coefficients depend on one or more real parameters, with solutions analysed as those parameters vary.

## Linear equations with parameters

The most basic context in which parameters arise is the [first-degree equation](https://algebrica.org/linear-equations-with-parameters/). A general linear equation with one unknown $x$ and a real parameter $k$ can be expressed as:
$$a \left(\right. k \left.\right) \cdot x + b \left(\right. k \left.\right) = 0$$
Here, $a \left(\right. k \left.\right)$ and $b \left(\right. k \left.\right)$ represent expressions involving $k$. The analysis of this equation divides into two cases, determined by whether the coefficient of $x$ is zero. If $a \left(\right. k \left.\right) \neq 0$, the equation admits a unique solution, given by:
$$x = - \frac{b \left(\right. k \left.\right)}{a \left(\right. k \left.\right)}$$

This solution defines a [function](https://algebrica.org/functions/) of the parameter.

- If $a \left(\right. k \left.\right) = 0$, the equation is no longer linear.
- If $b \left(\right. k \left.\right)$ also equals zero, every real number is a solution, and the equation is satisfied identically.
- If $b \left(\right. k \left.\right) \neq 0$, no solution exists and the equation is inconsistent.

## Example 1

Consider the following linear equation involving the parameter $k$:
$$\left(\right. k - 1 \left.\right) x = k^{2} - 1$$
The coefficient of $x$ is $a \left(\right. k \left.\right) = k - 1$, and the right-hand side is $b \left(\right. k \left.\right) = k^{2} - 1$. Since the right-hand side factors as $\left(\right. k - 1 \left.\right) \left(\right. k + 1 \left.\right)$, the case $k = 1$ requires separate consideration.

For $k \neq 1$, both sides can be divided by $k - 1$ without ambiguity, as the divisor is nonzero. This yields
$$x = \frac{\left(\right. k - 1 \left.\right) \left(\right. k + 1 \left.\right)}{k - 1} = k + 1$$
Thus, the equation has the unique solution $x = k + 1$ for every real value of $k$ except $1$. When $k = 1$, both sides become zero, and the equation reduces to $0 \cdot x = 0$. This identity is satisfied by every real $x$, so the solution set is $\mathbb{R}$.

In summary, the solution is:
$$k = 1 & \Rightarrow x \in \mathbb{R} \\ k \neq 1 & \Rightarrow x = k + 1$$

## Quadratic equations with parameters

Introducing a parameter into the coefficients of a [quadratic equation](https://algebrica.org/quadratic-equations-with-parameters/) increases the complexity of the analysis. The structure of the solution set depends both on the potential vanishing of a coefficient and on the sign of the discriminant, which itself varies with the parameter. A general parametric quadratic equation can be expressed as follows:
$$a \left(\right. k \left.\right) x^{2} + b \left(\right. k \left.\right) x + c \left(\right. k \left.\right) = 0 a \left(\right. k \left.\right) \neq 0$$
The condition $a \left(\right. k \left.\right) \neq 0$ must be verified for each value of the parameter or the equation reduces to a linear form. The [discriminant](https://algebrica.org/quadratic-formula/) becomes a real-valued function of $k$:
$$\Delta \left(\right. k \left.\right) = b \left(\right. k \left.\right)^{2} - 4 a \left(\right. k \left.\right) c \left(\right. k \left.\right)$$

Analysing the sign of the discriminant enables classification of the solutions:

- Two distinct real roots occur when $\Delta \left(\right. k \left.\right) > 0$.
- A repeated real root arises when $\Delta \left(\right. k \left.\right) = 0$.
- Two [complex conjugate roots](https://algebrica.org/quadratic-equations-with-complex-solutions/) exist when $\Delta \left(\right. k \left.\right) < 0$.

The parameter values at which the discriminant changes sign represent critical thresholds, marking transitions between qualitatively different solution structures.

## Higher-degree and transcendental equations with parameters

This reasoning extends beyond quadratic equations. Consider a general [polynomial equation](https://algebrica.org/polynomial-equations/) of degree $n$:
$$a_{n} \left(\right. k \left.\right) x^{n} + a_{n - 1} \left(\right. k \left.\right) x^{n - 1} + \hdots + a_{1} \left(\right. k \left.\right) x + a_{0} \left(\right. k \left.\right) = 0$$
The number and nature of the solutions depend on the parameter in ways that are often more complex to characterise. For $n \geq 3$, closed-form solution formulas become highly intricate or are unavailable in the classical sense.

Parameters may also appear in non-polynomial equations, including [exponential equations](https://algebrica.org/exponential-equations/) of the form $a^{x} = f \left(\right. k \left.\right)$, [logarithmic equations](https://algebrica.org/logarithmic-equations/) involving $log_{a} ⁡ \left(\right. x + k \left.\right)$, and trigonometric equations such as $sin ⁡ x = k$.

For example, the equation $sin ⁡ x = k$ has solutions only when $\left|\right. k \left|\right. \leq 1$, and within this interval, there are infinitely many solutions distributed periodically along the real line. When $k$ lies outside the interval $\left[\right. - 1 , 1 \left]\right.$, the equation has no solutions. In such cases, the parameter determines not only the form of the solutions but also their existence.

## Example 2

The following example illustrates a case where the existence of solutions cannot be determined by algebraic manipulation alone, but requires an analytic argument based on the behaviour of a derived function. Consider the equation

$$sin ⁡ x = k x k \in \mathbb{R}$$

The solution $x = 0$ exists for every value of $k$, since $sin ⁡ 0 = 0$. The question of interest is whether non-trivial solutions exist. Defining $f \left(\right. x \left.\right) = sin ⁡ x - k x$, the solutions correspond to the zeros of $f$. Since $f$ is an odd function, it suffices to study the case $x > 0$.

For $x > 0$, the condition $sin ⁡ x = k x$ can be rewritten as

$$k = \frac{sin ⁡ x}{x}$$

The function $g \left(\right. x \left.\right) = \frac{sin ⁡ x}{x}$ is [continuous](https://algebrica.org/continuous-functions/) for $x > 0$, tends to $1$ as $x \rightarrow 0^{+}$, and oscillates with decreasing amplitude toward $0$.

Its [local maxima](https://algebrica.org/maximum-minimum-and-inflection-points/) form a strictly decreasing [sequence](https://algebrica.org/sequences/), all below $1$.

- For $k \geq 1$, the line $y = k x$ is too steep to intersect the sinusoid outside the origin, and no non-trivial solution exists.
- For $0 < k < 1$, the line intersects the curve $y = sin ⁡ x$ on each arc where $\left|\right. sin ⁡ x / x \left|\right. > k$, producing infinitely many non-trivial solutions, distributed symmetrically about the origin.

As $k \rightarrow 0^{+}$, the number of intersections grows without bound. For $k \leq 0$, the right-hand side $k x$ is non-positive for $x > 0$, while $sin ⁡ x$ changes sign, so solutions still exist but their distribution depends on the specific value of $k$.

In summary, the solution set is:

- If $k \geq 1$: $x = 0$ is the only solution.
- If $0 < k < 1$: $x = 0$ and infinitely many symmetric non-trivial solutions.
- If $k \leq 0$: $x = 0$ and additional solutions depending on $k$.

## Systems of equations with parameters

Parameters appear naturally in systems as well. A [linear system](https://algebrica.org/systems-of-linear-equations/) of two equations in two unknowns takes the general form:

$$a_{11} \left(\right. k \left.\right) x + a_{12} \left(\right. k \left.\right) y & = b_{1} \left(\right. k \left.\right) \\ a_{21} \left(\right. k \left.\right) x + a_{22} \left(\right. k \left.\right) y & = b_{2} \left(\right. k \left.\right)$$

The system has a unique solution when the coefficient [matrix](https://algebrica.org/matrices/) is invertible, that is, when its determinant $D \left(\right. k \left.\right)$is nonzero:

$$D \left(\right. k \left.\right) = a_{11} \left(\right. k \left.\right) a_{22} \left(\right. k \left.\right) - a_{12} \left(\right. k \left.\right) a_{21} \left(\right. k \left.\right)$$

When $D \left(\right. k \left.\right) = 0$ for some value of the parameter, the system either becomes inconsistent or admits infinitely many solutions, depending on whether the right-hand side [vector](https://algebrica.org/vectors/) is compatible with the structure of the coefficient matrix at that value.

## Example 3

Let us examine the following system:

$$k x + y & = 1 \\ x + k y & = 1$$

The determinant of the coefficient matrix is:

$$D \left(\right. k \left.\right) = k \cdot k - 1 \cdot 1 = k^{2} - 1 = \left(\right. k - 1 \left.\right) \left(\right. k + 1 \left.\right)$$

When $k \neq \pm 1$, the determinant is nonzero and [Cramer’s rule](https://algebrica.org/cramers-rule/) applies directly, yielding a unique solution. Applying it, we find:

$$x = \frac{k - 1}{k^{2} - 1} = \frac{1}{k + 1}$$

$$y = \frac{k - 1}{k^{2} - 1} = \frac{1}{k + 1}$$

We obtain:

$$x = y = \frac{1}{k + 1} \forall k \neq \pm 1$$

At $k = 1$, both equations become $x + y = 1$, so the system reduces to a single equation. The two lines are coincident, and every point on the line $x + y = 1$ is a solution. The solution set is infinite and can be parametrised as $x = t$, $y = 1 - t$ for $t \in \mathbb{R}$.

At $k = - 1$, the first equation gives $- x + y = 1$ and the second gives $x - y = 1$. These two relations are inconsistent: adding them yields $0 = 2$, which is a contradiction. The lines are parallel and distinct, and the system has no solution.

The two values $k = \pm 1$ are therefore not merely special but structurally opposite: one leads to underdetermination and the other to incompatibility.

In summary, the solution is:

- If $k = 1$: infinitely many solutions, $x = t$, $y = 1 - t$ for $t \in \mathbb{R}$.
- If $k = - 1$: no solution.
- If $k \neq \pm 1$: unique solution $x = y = \frac{1}{k + 1}$.
