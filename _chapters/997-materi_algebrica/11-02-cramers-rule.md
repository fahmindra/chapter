---
layout: chapter
title: "Cramer’s Rule"
chapter: "Linear Systems"
chapter_order: 11
section_order: 2
permalink: /materi-algebrica/linear-systems/cramers-rule/
---

## What is Cramer’s rule?

Cramer’s Rule provides a method for solving [systems](https://algebrica.org/systems-of-linear-equations) of $n$ [linear equations](https://algebrica.org/linear-equations) in $n$ unknowns, by using the determinant of the system’s coefficient [matrix](https://algebrica.org/matrices). This rule applies only when the coefficient matrix is square and its determinant is non-zero, ensuring that the system has a unique solution.

## Applying Cramer’s Rule

Let us consider a general system of $n$ equations in $n$ unknowns:

$$\left{\right. a_{11} x_{1} + a_{12} x_{2} + \hdots + a_{1 n} x_{n} = b_{1} \\ a_{21} x_{1} + a_{22} x_{2} + \hdots + a_{2 n} x_{n} = b_{2} \\ \vdots \\ a_{n 1} x_{1} + a_{n 2} x_{2} + \hdots + a_{n n} x_{n} = b_{n}$$

We can rewrite the system using matrix notation as $A \cdot \mathbf{X} = \mathbf{B}$. The system becomes:

$$A = \left[\right. a_{11} & a_{12} & \hdots & a_{1 n} \\ a_{21} & a_{22} & \hdots & a_{2 n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m 1} & a_{n 2} & \hdots & a_{n n} \left]\right.$$

The constant terms and variables can be organized into two column [vectors](https://algebrica.org/vectors/):

$$X = \left[\right. x_{1} \\ x_{2} \\ \vdots \\ x_{n} \left]\right. B = \left[\right. b_{1} \\ b_{2} \\ \vdots \\ b_{m} \left]\right.$$

---

Suppose that the coefficient matrix $A$ is invertible, which means that its determinant is non-zero ($det \left(\right. A \left.\right) \neq 0$). Under this condition, the system has a unique solution, and it can be expressed using the inverse of $A$ as:

$$\left[\right. x_{1} \\ x_{2} \\ \vdots \\ x_{n} \left]\right. = \frac{1}{det \left(\right. A \left.\right)} \left[\right. A_{11} & A_{21} & \hdots & A_{n 1} \\ A_{12} & A_{22} & \hdots & A_{n 2} \\ \vdots & \vdots & \ddots & \vdots \\ A_{1 n} & A_{2 n} & \hdots & A_{n n} \left]\right. \left[\right. b_{1} \\ b_{2} \\ \vdots \\ b_{n} \left]\right.$$

This is the general form of Cramer’s Rule, where each $A_{i j}$ is the cofactor of the element $a_{j i}$ in the original matrix $A$.

##### In this context, $A_{i j}$ refers to the cofactor of the element $a_{j i}$ from the original matrix $A$, not to the entry of the matrix itself. The matrix used here is the adjugate of $A$, denoted as $\text{adj} \left(\right. A \left.\right)$.

---

The value of the unknown in position $k$ is given by a fraction. Its denominator is $det \left(\right. A \left.\right)$ and its numerator is the determinant of the matrix obtained by replacing the $k$-th column of $A$ with the column of constants:

$$x_{k} = \frac{det \left(\right. A_{k} \left.\right)}{det \left(\right. A \left.\right)}$$

##### For a clearer understanding of this step, see the detailed explanation in Example 2.

## Solutions of homogeneous systems

A [homogeneous system](https://algebrica.org/systems-of-linear-equations) is a system of linear equations where all the constant terms are zero. These systems always have at least one solution: the trivial solution, where all the variables are zero. But something interesting happens when we look at the determinant of the coefficient matrix:

- If $det \left(\right. A \left.\right) \neq 0$, the system has only the trivial solution.
- If $det \left(\right. A \left.\right) = 0$, the system admits infinitely many solutions, including non-trivial ones, where at least one variable is not zero.

##### Homogeneous systems never have no solution. They’re always consistent, but the number of solutions depends entirely on the determinant.

## Example 1

Let’s consider the following homogeneous system of three equations in three unknowns:

$$\left{\right. x + y + z = 0 \\ 2 x - y + z = 0 \\ 3 x + y + 2 z = 0$$

---

This system can be written in matrix form as $A \cdot \mathbf{x} = 0$, where the coefficient matrix is:

$$A = \left[\right. 1 & 1 & 1 \\ 2 & - 1 & 1 \\ 3 & 1 & 2 \left]\right.$$

---

To understand the nature of the solutions, we compute the determinant of the matrix $A$:

$$det \left(\right. A \left.\right) & = 1 \cdot \left(\right. - 1 \cdot 2 - 1 \cdot 1 \left.\right) - 1 \cdot \left(\right. 2 \cdot 2 - 1 \cdot 3 \left.\right) + 1 \cdot \left(\right. 2 \cdot 1 - \left(\right. - 1 \left.\right) \cdot 3 \left.\right) \\ & = 1 \left(\right. - 2 - 1 \left.\right) - 1 \left(\right. 4 - 3 \left.\right) + 1 \left(\right. 2 + 3 \left.\right) \\ & = - 3 - 1 + 5 \\ & = 1$$

Since the determinant is non-zero, the system admits only the trivial solution:

$$x = 0 y = 0 z = 0$$

##### This outcome aligns with Cramer’s Rule: when $det \left(\right. A \left.\right) \neq 0$, the only possible solution to a homogeneous system is the trivial one, since all the determinants in the numerators of Cramer’s formula become zero.

## Example 2

Let’s solve the following system of two linear equations in two unknowns:

$$\left{\right. 2 x + 3 y = 8 \\ 4 x - y = 2$$

---

We identify the coefficient matrix $A$, the vector of unknowns $\mathbf{x}$, and the constants vector $\mathbf{b}$:

$$A = \left[\right. 2 & 3 \\ 4 & - 1 \left]\right. \mathbf{x} = \left[\right. x \\ y \left]\right. \mathbf{b} = \left[\right. 8 \\ 2 \left]\right.$$

---

We compute the determinant of the coefficient matrix $A$:

$$det \left(\right. A \left.\right) = 2 \cdot \left(\right. - 1 \left.\right) - 3 \cdot 4 = - 2 - 12 = - 14$$

Since the determinant is non-zero, the system has exactly one solution, and we can apply Cramer’s rule.

---

We build the matrix $A_{1}$ by replacing the first column of $A$ with the constants:

$$A_{1} = \left[\right. 8 & 3 \\ 2 & - 1 \left]\right. \rightarrow det \left(\right. A_{1} \left.\right) = 8 \cdot \left(\right. - 1 \left.\right) - 3 \cdot 2 = - 8 - 6 = - 14$$

---

We now build $A_{2}$ by replacing the second column of $A$ with the constants:

$$A_{2} = \left[\right. 2 & 8 \\ 4 & 2 \left]\right. \rightarrow det \left(\right. A_{2} \left.\right) = 2 \cdot 2 - 8 \cdot 4 = 4 - 32 = - 28$$

---

Now we compute the values of the unknowns using the formula:

$$x & = \frac{det \left(\right. A_{1} \left.\right)}{det \left(\right. A \left.\right)} = \frac{- 14}{- 14} = 1 \\ y & = \frac{det \left(\right. A_{2} \left.\right)}{det \left(\right. A \left.\right)} = \frac{- 28}{- 14} = 2$$

The solution to the system is:

$$x = 1 y = 2$$

##### Remember that the solution to a system of linear equations refers to the $n$-tuple of values that satisfies all equations in the system simultaneously. In this case, the pair $\left(\right. x , y \left.\right) = \left(\right. 1 , 2 \left.\right)$ is the only combination of values that makes both equations true at the same time.
