---
layout: chapter
title: "Systems of Linear Equations"
chapter: "Linear Systems"
chapter_order: 11
section_order: 1
permalink: /materi-algebrica/linear-systems/systems-of-linear-equations/
---

## What is a linear system?

Linear systems model problems where multiple conditions must be satisfied at the same time. They form the basis of many solution methods in algebra and applied mathematics. Given $n$ variables $x_{1} , x_{2} , \ldots , x_{n}$, a system is called linear if all the equations are [linear equations](https://algebrica.org/linear-equations), meaning each variable appears to the first power, with no products between variables. The standard form of a linear system with $m$ equations and $n$ unknowns is written as:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + \hdots + a_{1 n} x_{n} = b_{1} \\ a_{21} x_{1} + a_{22} x_{2} + \hdots + a_{2 n} x_{n} = b_{2} \\ \vdots \\ a_{m 1} x_{1} + a_{m 2} x_{2} + \hdots + a_{m n} x_{n} = b_{m}$$

In a linear system written in standard form, the coefficients $a_{i j}$ represent the value multiplying the variable $x_{j}$ in the $i$-th equation.

## Omogeneous systems

Each $b_{i}$ denotes the constant term (also called the known term) on the right-hand side of the $i$-th equation. If all constant terms are zero, that is, $\forall i , b_{i} = 0$, the system is called **homogeneous**.

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + \hdots + a_{1 n} x_{n} = 0 \\ a_{21} x_{1} + a_{22} x_{2} + \hdots + a_{2 n} x_{n} = 0 \\ \vdots \\ a_{m 1} x_{1} + a_{m 2} x_{2} + \hdots + a_{m n} x_{n} = 0$$

## Solutions

Solving a linear system means finding an ordered $n$-tuple of values denoted as $\left(\right. s_{1} , s_{2} , \ldots , s_{n} \left.\right)$, that satisfies all the equations in the system.

- A system is said to be **consistent** (or possible) if at least one solution exists, and its equations are compatible.
- If no solution exists, the system is called **inconsistent** (or impossible), and its equations are incompatible.
- If there is only one solution, the system is called **determined**.
- If there are infinitely many solutions, it is called **undetermined**.

Linear systems are defined by their coefficients and constants, which can be naturally organized into [matrices](https://algebrica.org/matrices). This connection allows us to represent the system compactly and apply matrix methods to analyze and solve it.

Any linear system in standard form can be represented by an $m \times n$ matrix, where $m$ is the number of equations and $n$ is the number of variables. The matrix formed by the coefficients of the variables is called the **coefficient matrix**:

$$A = \left[\right. a_{11} & a_{12} & \hdots & a_{1 n} \\ a_{21} & a_{22} & \hdots & a_{2 n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m 1} & a_{m 2} & \hdots & a_{m n} \left]\right.$$

The constant terms and variables can be organized into two column [vectors](https://algebrica.org/vectors/):

$$X = \left[\right. x_{1} \\ x_{2} \\ \vdots \\ x_{n} \left]\right. B = \left[\right. b_{1} \\ b_{2} \\ \vdots \\ b_{m} \left]\right.$$

Therefore, the system can be rewritten in matrix form as:

$$A \cdot X = B$$

##### This compact form summarizes the entire system, where $A$ is the coefficient matrix, $X$ is the vector of variables, and $B$ is the vector of constants.

## Why is the matrix form important?

Solving systems of linear equations can become challenging, especially as the number of equations and variables increases. While we’ll explore various solution methods, it’s worth noting that rewriting a system in matrix form is particularly useful. It provides a more compact representation and often simplifies the process of finding solutions.

## How to solve a linear system with the same number of equations and unknowns ($n = m$)

A linear system with $n$ equations and $n$ unknowns can be solved using the [inverse matrix](https://algebrica.org/inverse-matrix/) method. If the coefficient matrix $A$ is non-singular, that is, if its determinant is nonzero the system $A \cdot X = B$ has a unique solution, given by:

$$X = A^{- 1} B$$

## Example

Let’s solve a relatively simple example: a linear system with 3 equations in 3 unknowns, where $n = m$.

$$\left{\right. x_{1} + x_{2} + x_{3} = 3 \\ 2 x_{1} + x_{2} + x_{3} = 4 \\ 2 x_{1} + x_{2} + 3 x_{3} = 8$$

---

First, let’s determine the coefficient matrix $A$ and compute the determinant:

$$A = \left[\right. 1 & 1 & 1 \\ 2 & 1 & 1 \\ 2 & 1 & 3 \left]\right. det \left(\right. A \left.\right) = - 2$$

##### Refer to the section on [computing the determinant](https://algebrica.org/determinant/) of a square matrix for a clearer understanding of the method.

---

Since the determinant of the matrix is nonzero, the matrix is non-singular and its inverse can be computed.

$$A^{- 1} = \left[\right. - \frac{1}{2} & - \frac{1}{2} & \frac{1}{2} \\ 0 & - \frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & 1 & - \frac{1}{2} \left]\right.$$

##### Refer to the section on computing the [inverse matrix](https://algebrica.org/inverse-matrix) for all the steps.

---

We now express the system as $X = A^{- 1} B$ in order to determine the unknown variables:

$$\left[\right. x_{1} \\ x_{2} \\ x_{3} \left]\right. = \left[\right. - \frac{1}{2} & - \frac{1}{2} & \frac{1}{2} \\ 0 & - \frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & 1 & - \frac{1}{2} \left]\right. \cdot \left[\right. 3 \\ 4 \\ 8 \left]\right.$$

---

We now compute the values of $x_{1}$, $x_{2}$, and $x_{3}$ from the matrix equation.

$$x_{1} & = - \frac{1}{2} \cdot 3 - \frac{1}{2} \cdot 4 + \frac{1}{2} \cdot 8 = \frac{1}{2} \\ x_{2} & = 0 \cdot 3 - \frac{1}{2} \cdot 4 + \frac{1}{2} \cdot 8 = 2 \\ x_{3} & = \frac{1}{2} \cdot 3 + 1 \cdot 4 - \frac{1}{2} \cdot 8 = \frac{3}{2}$$

Therefore, the solutions of the system are:

$$x_{1} = \frac{1}{2} x_{2} = 2 x_{3} = \frac{3}{2}$$
