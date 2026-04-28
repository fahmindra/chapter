---
layout: chapter
title: "Irrational Equations"
chapter: "Equations"
chapter_order: 7
section_order: 14
permalink: /materi-algebrica/equations/irrational-equations/
---

extraneous solutionsrational equationsnon-negative valuesdomain restrictionodd rootseven rootsspurious rootssolution checkpower stepdomain checkrational rootconstant rootpolynomial rootprincipal rootradicandindex of rootroot notationfractional powersradicalspropertiesforms and methodsdefinition

## Definition of irrational equations

Irrational equations, also known as radical equations, are [equations](https://algebrica.org/equations/) in which the unknown variable $x$ appears within a [radical](https://algebrica.org/radicals/) or is represented by a fractional [exponent](https://algebrica.org/powers/). These equations form a distinct class of problems that cannot be addressed solely through standard algebraic manipulations. The inclusion of roots and non-integer exponents imposes additional constraints on the permissible values of $x$, making [domain analysis](https://algebrica.org/determining-the-domain-of-a-function/) an essential preliminary step before solving the equation.

---

An irrational equation is defined as an equation of the form $F \left(\right. x \left.\right) = 0$ in which at least one term contains a fractional power of a function, specifically a power with a denominator greater than one in the exponent. Equivalently, these equations include radical expressions. More precisely, the defining term takes the form:

$$f \left(\right. x \left.\right)^{\frac{p}{q}} \text{with} q > 1$$

In radical notation, we can express them as:

$$\sqrt[q]{ f \left(\right. x \left.\right)}$$

Typical forms include expressions where a [polynomial](https://algebrica.org/polynomials/) is placed under an $n$-th root or is raised to a reciprocal power:

$$\sqrt[n]{ f \left(\right. x \left.\right) } = g \left(\right. x \left.\right)$$$$f \left(\right. x \left.\right)^{ \frac{1}{n}} = g \left(\right. x \left.\right)$$

where $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ are [polynomials](https://algebrica.org/polynomials) of arbitrary degree with [real coefficients](https://algebrica.org/types-of-numbers).

###### Solving such equations typically involves eliminating the radical by raising both sides to the appropriate power. This process may introduce extraneous solutions; therefore, each candidate solution must be verified against the domain constraints determined by the original radical expression.

## General forms of irrational equations

- $$\text{1}. \sqrt[n]{ f \left(\right. x \left.\right) } = g \left(\right. x \left.\right)$$
- $$\text{2}. \sqrt[n]{ f \left(\right. x \left.\right) } = k$$
- $$\text{3}. f \left(\right. x \left.\right)^{1 / n} = g \left(\right. x \left.\right)$$

##### These conditions highlight what makes irrational equations unique. Roots set clear [limits](https://algebrica.org/limits/) on the [domain](https://algebrica.org/determining-the-domain-of-a-function/), and after removing radicals, you need to check your solutions. Algebraic steps may give possible answers, but each one should be checked carefully.

## How to solve irrational equations

When dealing with irrational equations, the strategy used to solve them depends heavily on the structure of the radical and on the position of the unknown within the expression. However, despite these variations, the overall approach follows a few essential steps that guide the solution process. The key stages can be summarised as follows:

- Determine the [domain](https://algebrica.org/determining-the-domain-of-a-function/) by considering whether the index of the roots is even or odd, and impose the relevant conditions discussed above.
- Eliminate the roots by raising both sides of the equation to the appropriate power.
- Perform the necessary calculations and determine the solutions. Check their admissibility by verifying if they belong to the original domain of existence and satisfy the initial equation.

## A closer look at the general forms

Irrational equations can appear in several structural patterns, and recognising these patterns is essential for understanding how to approach their solution. In this context, the position of the variable inside a radical and the value of the radical’s index play a central role, as they determine both the domain of definition and the type of algebraic manipulations that can be applied.

---

A first and very common case is that of irrational equations in which the index $n$ of the root is even. These equations have the general form:

$$\sqrt[n]{ f \left(\right. x \left.\right) } = g \left(\right. x \left.\right) n \in 2 \mathbb{Z}$$

where $2 \mathbb{Z}$ denotes the set of even [integers](https://algebrica.org/integers/). Because an even root is defined only for non-negative radicands, one must impose specific conditions of existence before attempting to solve the equation.

- Impose the domain:$f \left(\right. x \left.\right) \geq 0$ and $\left(\right. g \left(\right. x \left.\right) \geq 0.$
- Remove the radical: raise both sides to the power $n$.
- Solve the resulting algebraic equation.
- Check each solution in the original equation.
- Keep only the values that satisfy all domain conditions.

##### In this case, one must also verify that $g \left(\right. x \left.\right) \geq 0$, since an even-index root can only produce non-negative real values and cannot equal a negative quantity.

---

When the equation has the form

$$\sqrt[n]{ f \left(\right. x \left.\right) } = k$$

and $k$ is a non-negative real number, the domain of existence for the unknown $x$ is given by the values of the variable that satisfy:

$$f \left(\right. x \left.\right) \geq 0$$

Only for those values is the expression under the radical well defined. To solve the equation, follow these essential steps:

- Impose the domain condition: ensure that $f \left(\right. x \left.\right) \geq 0$.
- Remove the radical by raising both sides to the power $n$.
- Solve the resulting algebraic equation.
- Check each candidate solution in the original equation.
- Keep only the values that satisfy the domain and the original equality.

---

If instead the equation is of the form:

$$\sqrt[n]{ f \left(\right. x \left.\right) } = k$$

with $k$ a negative real number, then the equation has no solution. An even-index radical cannot yield a negative value, so the equality cannot be satisfied for any real value of the variable.

---

A more general situation arises when the equation is written as:

$$\sqrt[n]{ f \left(\right. x \left.\right) } = g \left(\right. x \left.\right)$$

where $g \left(\right. x \left.\right)$ is a rational function. In this case, determining the domain of existence requires analysing both sides of the equation. The allowed values of $x$ are those that satisfy the following [system of inequalities](https://algebrica.org/systems-of-inequalities/) defining the domain:

$$\left{\right. f \left(\right. x \left.\right) \geq 0 \\ g \left(\right. x \left.\right) \geq 0$$

After establishing the domain conditions, the equation may be transformed by raising both sides to the power $n$, resulting in the following equivalent algebraic equation:

$$f \left(\right. x \left.\right) = \left(\right. g \left(\right. x \left.\right) \left.\right)^{n}$$

Given these conditions, the radical is well-defined, the equality holds significance, and the resulting equation after eliminating the radical remains consistent with the original expression.

---

If the equation is written in the form:

$$f \left(\right. x \left.\right)^{1 / n} = g \left(\right. x \left.\right) n \in 2 \mathbb{Z}$$

and the expression $g \left(\right. x \left.\right)$ takes negative values for some real $x$, then the equation cannot have a solution at those points. When the index $n$ is even, the expression $f \left(\right. x \left.\right)^{1 / n}$ represents an even-index root, which can only produce non-negative real numbers. As a result, the equality cannot be satisfied whenever $g \left(\right. x \left.\right) < 0 ,$ since an even root cannot return a negative value. In other words, the equation

$$f \left(\right. x \left.\right)^{1 / n} = g \left(\right. x \left.\right)$$

has no solution for any $x$ such that $g \left(\right. x \left.\right) < 0.$ Possible solutions may exist only where $g \left(\right. x \left.\right) \geq 0 ,$ and these must also satisfy the condition that the radicand is defined, that is $f \left(\right. x \left.\right) \geq 0.$

## Distinction between irrational and rational equations

The difference between irrational and [rational equations](https://algebrica.org/rational-equations/) depends on the way the variable $x$ appears within the algebraic expression. Rational equations are built from ratios of polynomials, meaning that the unknown occurs only in the numerator or denominator of a fraction whose components are polynomial expressions. An example is

$$\frac{2 x}{2 x - 1}$$

which remains entirely within the framework of rational expressions.

Irrational equations, on the other hand, are characterised by the presence of the variable inside a root or raised to a fractional exponent. These equations involve [radical](https://algebrica.org/radicals/) notation, often with an explicit index defining the order of the root, and their structure introduces domain restrictions that must be considered before attempting a solution. A typical example is:

$$\frac{2 x}{\sqrt{2 x - 1}}$$

where the square root makes the equation irrational.

Recognising whether an equation is rational or irrational is an essential first step, as each class requires different solving techniques and comes with its own set of algebraic constraints.

## Roots with odd indexes

When the index $n$ of a radical is an odd integer, the behaviour of the equation becomes particularly manageable. Unlike even roots, which impose restrictions on the radicand, an odd root can be evaluated for any real input. This means that the expression remains meaningful over the entire real line, without the need to introduce conditions that limit the domain of the variable. In practice, the possibility of extracting the root of a negative number greatly simplifies the overall structure of the equation.

From a mathematical standpoint, if $n = 2 k + 1$ is odd, the function:

$$x \mapsto \sqrt[n]{x}$$

is defined for every $x \in \mathbb{R}$. This property stems from the fact that raising a real number to an odd power always gives a real value, regardless of whether the initial number is positive, negative, or zero. As a consequence, taking an odd root (the inverse operation) is always possible and never introduces inconsistencies related to sign constraints. A general irrational equation involving an odd root can be written as:

$$\sqrt[n]{ f \left(\right. x \left.\right) } = g \left(\right. x \left.\right) n \in 2 \mathbb{Z} + 1$$

and can be transformed into an equivalent algebraic equation simply by raising both sides to the power $n$:

$$f \left(\right. x \left.\right) = \left(\right. g \left(\right. x \left.\right) \left.\right)^{n}$$

In this setting, the radical does not impose additional inequalities such as $f \left(\right. x \left.\right) \geq 0$ or $g \left(\right. x \left.\right) \geq 0$; any restrictions arise solely from the expressions outside the radical, for instance when denominators or further roots appear elsewhere in the equation. A straightforward numerical example illustrates this behaviour:

$$\sqrt[3]{- 8} = - 2$$

because:

$$\left(\right. - 2 \left.\right)^{3} = - 8$$

More generally, for any real number $a$ and any odd index $n = 2 k + 1$:

$$\sqrt[n]{ a } = a^{1 / n}$$

and the result remains real. This correspondence between odd-index radicals and fractional powers explains why irrational equations of this type can often be handled through direct algebraic manipulation, without the preliminary domain checks required in the even-index case.

## Rationale for maintaining roots on opposite sides

When solving equations involving roots, it is important to keep the roots on either side of the equal sign separate. This practice helps prevent the introduction of extraneous solutions that may arise during exponentiation. For example, consider the following irrational equation:

$$\sqrt{2 x} - \sqrt{x + 1} = 0$$

---

Squaring a root can introduce additional roots, which may complicate the calculation:

$$& \left(\right. \sqrt{2 x} - \sqrt{x + 1} \left.\right)^{2} = 0 \\ & 2 x - \left(\right. x + 1 \left.\right) + 2 \sqrt{2 x} \cdot \sqrt{x + 1} = 0$$

---

To simplify calculations, it is preferable to isolate the roots on opposite sides of the equation whenever possible:

$$& \sqrt{2 x} = \sqrt{x + 1} \\ & \left(\right. \sqrt{2 x} \left.\right)^{2} = \left(\right. \sqrt{x + 1} \left.\right)^{2} \\ & 2 x = x + 1 \\ & 2 x - x = 1 \\ & x = 1$$

## Example 1

Solve the irrational equation:

$$\sqrt{x^{2} - 2} = \sqrt{4 x}$$

---

The equation is of the form:

$$\sqrt[n]{f \left(\right. x \left.\right)} = g \left(\right. x \left.\right)$$

where $n$, the index of the root is even. The admissible set of solutions is determined by solving the [system of inequalities](https://algebrica.org/systems-of-inequalities/):

$$\left{\right. f \left(\right. x \left.\right) \geq 0 \\ g \left(\right. x \left.\right) \geq 0$$

---

Substitute $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ for the polynomials under the roots to obtain: $$\left{\right. x^{2} - 2 \geq 0 \\ 4 x \geq 0$$

---

Solve the [second-degree](https://algebrica.org/quadratic-equations/) equation associated with the first inequality $x^{2} - 2 \geq 0$ and find its solutions. In this case, we have: $$x_{1 , 2} = \pm \sqrt{2}$$ therefore, the domain of existence of the [inequality](https://algebrica.org/inequalities) is given by the intervals: $$\left(\right. - \infty , - \sqrt{2} \left]\right. \cup \left[\right. \sqrt{2} , + \infty \left.\right)$$

For the second inequality we have $x \geq 0$. The intersection of the intervals found gives the admissible set of solutions. We can use the graphical method to determine it visually:

|  | $$- \sqrt{2}$$ | $$0$$ | $$+ \sqrt{2}$$ |  |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

The system admits solutions in the interval $\left[\right. \sqrt{2} , + \infty \left.\right)$.

---

To solve the original equation, isolate the radicals on each side of the equation and then square both sides as follows:

$$& \sqrt{x^{2} - 2} = \sqrt{4 x} \\ & x^{2} - 2 = 4 x \\ & x^{2} - 4 x - 2 = 0$$

This gives us a [quadratic equation](https://algebrica.org/quadratic-equations/) that we can solve using the [quadratic formula](https://algebrica.org/quadratic-formula/).

$$x_{1 , 2} & = \frac{- \left(\right. - 4 \left.\right) \pm \sqrt{\left(\right. - 4 \left.\right)^{2} - 4 \cdot 1 \cdot \left(\right. - 2 \left.\right)}}{2 \cdot 1} \\ & = \frac{4 \pm \sqrt{16 + 8}}{2} \\ & = \frac{4 \pm \sqrt{24}}{2} \\ & = \frac{4 \pm 2 \sqrt{6}}{2} \\ & = 2 \pm \sqrt{6}$$

---

Before verifying the solutions, it is necessary to determine whether they belong to the admissible set $\left[\right. \sqrt{2} , + \infty \left.\right)$:

- $x_{2} = 2 + \sqrt{6} \approx 4.449 \in \left[\right. \sqrt{2} , + \infty \left.\right)$
- $x_{1} = 2 - \sqrt{6} \approx - 0.449 \notin \left[\right. \sqrt{2} , + \infty \left.\right)$

$x_{1} = 2 - \sqrt{6}$ is an extraneous solution introduced during the squaring step and should be discarded. It is now necessary to verify that $x_{2} = 2 + \sqrt{6}$ satisfies the original equation:

$$& \sqrt{\left(\right. 2 + \sqrt{6} \left.\right)^{2} - 2} = \sqrt{4 \cdot \left(\right. 2 + \sqrt{6} \left.\right)} \\ & \sqrt{4 + 4 \sqrt{6} + 6 - 2} = \sqrt{8 + 4 \sqrt{6}} \\ & \sqrt{8 + 4 \sqrt{6}} = \sqrt{8 + 4 \sqrt{6}}$$

The equality holds. Thus, the solution to the equation is:

$$x = 2 + \sqrt{6}$$

## Exercises

- $$\text{1}. \sqrt{x^{2} - 2 x + 1} = \sqrt{3}$$ [solution](https://algebrica.org/tests/irrational-equation-a-1/)
- $$\text{2}. \sqrt{2 x - x^{2}} = x - 2$$ [solution](https://algebrica.org/tests/irrational-equation-a-2/)
- $$\text{3}. \sqrt{4 - x} = 3 - \sqrt{5 + x}$$[solution](https://algebrica.org/tests/irrational-equation-a-3/)
- $$\text{4}. \sqrt{3 x^{2} - 8 x} = - 5$$[solution](https://algebrica.org/tests/irrational-equation-a-4/)
- $$\text{5}. \sqrt[3]{2 x^{2} + x - 3} = \sqrt[3]{3}$$ [solution](https://algebrica.org/tests/irrational-equation-a-5/)
- $$\text{6}. \sqrt{x + 3} = 1 + \sqrt{2 - x}$$[solution](https://algebrica.org/tests/irrational-equation-a-6/)
- $$\text{7}. \sqrt[5]{4 x - 6} = 2$$ [solution](https://algebrica.org/tests/irrational-equation-a-7/)
- $$\text{8}. \sqrt{x + 100} - x = - 10$$ [solution](https://algebrica.org/tests/irrational-equation-a-8/)
- $$\text{9}. \frac{\sqrt{2 x - 1}}{x - 2} = 1$$ [solution](https://algebrica.org/tests/irrational-equation-a-9/)
- $$\text{10}. \sqrt{3 \sqrt{x - 1}} = 3$$ [solution](https://algebrica.org/tests/irrational-equation-a-10/)

##### The proposed equations are carefully designed to help you consolidate your understanding of irrational equations. Try solving them independently before checking the solutions provided.

## Selected references

- **OpenStax**. [Radical Equations](https://assets.openstax.org/oscms-prodcms/media/documents/Algebra-and-Trigonometry-2e-WEB.pdf)
- **City University of New York**. [College Algebra and Trigonometry](https://openlab.citytech.cuny.edu/shavermat1275cofall2019/files/2019/08/1566849743-AlgebraTrigBook.pdf)
- **University of British Columbia**. [Differentiation and Radical Equations Section](https://www.math.ubc.ca/~feldman/m101/clp/clp_notes_100.pdf)
