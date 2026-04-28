---
layout: chapter
title: "Gaussian Elimination"
chapter: "Linear Systems"
chapter_order: 11
section_order: 3
permalink: /materi-algebrica/linear-systems/gaussian-elimination/
---

## What is Gaussian elimination

The Gauss method, or **Gaussian elimination**, is a technique used to solve [systems](https://algebrica.org/systems-of-linear-equations/) of $n$ linear equations in $n$ unknowns. The process involves applying a sequence of operations iteratively to eliminate one variable at a time, transforming the system into a form that is easy to solve. Let us consider the following system of equations:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + a_{13} x_{3} = b_{1} \\ a_{21} x_{1} + a_{22} x_{2} + a_{23} x_{3} = b_{2} \\ a_{31} x_{1} + a_{32} x_{2} + a_{33} x_{3} = b_{3}$$

##### To apply the method, it is essential that the system is square, that is, it must have the same number of equations and unknowns, like the $3 \times 3$ system shown above.

## The process involves the following steps:

- Eliminate the variable $x_{1}$ from all equations except the first one.
- Eliminate the variable $x_{2}$ from the third equation.
- Solve the third equation to find the value of $x_{3}$.
- Work backwards to find the values of the remaining variables.

##### When the algorithm produces an inconsistent or indeterminate equation, the system cannot proceed further: this signals either no solution or an infinite set of solutions.

## Connection with Matrices

The Gaussian elimination method transforms a [matrix](https://algebrica.org/matrices) into its row-echelon form. The objective is to rewrite the matrix so that each pivot position (on the main diagonal) contains a 1, and all entries below each pivot are 0. For example, starting from a generic matrix:

$$A = \left[\right. a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \left]\right. \overset{\text{to} }{\rightarrow} \left[\right. 1 & b_{12} & b_{13} \\ 0 & 1 & b_{23} \\ 0 & 0 & 1 \left]\right.$$

## Let’s start by eliminating the variable $x_{1}$ from all equations except the first one.

To eliminate $x_{1}$ from the second equation, we multiply the first equation by $a_{21}$ and the second by $a_{11}$. We then subtract the two resulting equations and replace the second equation with the result. We obtain:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + a_{13} x_{3} = b_{1} \\ \left(\right. a_{11} a_{22} - a_{21} a_{12} \left.\right) x_{2} + \left(\right. a_{11} a_{23} - a_{21} a_{13} \left.\right) x_{3} = a_{11} b_{2} - a_{21} b_{1} \\ a_{31} x_{1} + a_{32} x_{2} + a_{33} x_{3} = b_{3}$$

To simplify the calculations, we rewrite the second equation as:

$$a_{22}^{′} x_{2} + a_{23}^{′} x_{3} = b_{2}^{′}$$

The system becomes:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + a_{13} x_{3} = b_{1} \\ a_{22}^{′} x_{2} + a_{23}^{′} x_{3} = b_{2}^{′} \\ a_{31} x_{1} + a_{32} x_{2} + a_{33} x_{3} = b_{3}$$

---

Now, we multiply the first equation by $a_{31}$ and the third equation by $a_{11}$. We then subtract the two resulting equations and replace the third equation with the result.

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + a_{13} x_{3} = b_{1} \\ a_{22}^{′} x_{2} + a_{23}^{′} x_{3} = b_{2}^{′} \\ \left(\right. a_{11} a_{32} - a_{31} a_{12} \left.\right) x_{2} + \left(\right. a_{11} a_{33} - a_{31} a_{13} \left.\right) x_{3} = a_{11} b_{3} - a_{31} b_{1}$$

We rewrite the third equation as:

$$a_{32}^{′} x_{2} + a_{33}^{′} x_{3} = b_{3}^{'}$$

We obtain:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + a_{13} x_{3} = b_{1} \\ a_{22}^{′} x_{2} + a_{23}^{′} x_{3} = b_{2}^{′} \\ a_{32}^{′} x_{2} + a_{33}^{′} x_{3} = b_{3}^{'}$$

## We proceed with the second step and eliminate the variable $x_{2}$ from the third equation.

We multiply the second equation by $a_{32}^{′}$ and the third equation by $a_{22}^{′}$. We then subtract the two resulting equations and replace the third equation with the result. By completing the calculations as in the first step, the system reduces to the following:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + a_{13} x_{3} = b_{1} \\ a_{22}^{′} x_{2} + a_{23}^{′} x_{3} = b_{2}^{′} \\ a_{33}^{′ ′} x_{3} = b_{3}^{′ ′}$$

We have obtained a triangular system. At this point, we can solve for $x_{3}$ from the third equation, obtaining:
$$x_{3} = \frac{b^{′ ′_{3}}}{a^{′ ′_{33}}}$$

We can now determine each variable, starting from the known value of $x_{3}$.

## Example

Let’s walk through a concrete example of Gaussian elimination applied to a 3×3 system. Consider the following system of linear equations:

$$\left{\right. x + y + z = 6 \\ 2 x + 3 y + z = 14 \\ x + 2 y + 3 z = 14$$

To eliminate $x$ from the second equation, subtract $2 \times$ equation 1 from equation 2:

$$\left(\right. 2 x + 3 y + z \left.\right) - 2 \left(\right. x + y + z \left.\right) = 0 x + y - z = 2$$

---

Now eliminate $x$ from the third equation by subtracting equation 1 from equation 3:

$$\left(\right. x + 2 y + 3 z \left.\right) - \left(\right. x + y + z \left.\right) = 0 x + y + 2 z = 8$$

The system becomes:

$$\left{\right. x + y + z = 6 \\ y - z = 2 \\ y + 2 z = 8$$

---

Now use the second equation as the new pivot. To eliminate $y$ from the third equation, subtract equation 2 from equation 3:

$$\left(\right. y + 2 z \left.\right) - \left(\right. y - z \left.\right) = 3 z = 6 \Rightarrow z = 2$$

Substituting back to find the remaining variables. From equation 2:
$$y - z = 2 \rightarrow y = 2 + z = 2 + 2 = 4$$

From equation 1:
$$x + y + z = 6 \Rightarrow x = 6 - y - z = 6 - 4 - 2 = 0$$

The solution is

$$x = 0 y = 4 z = 2$$
