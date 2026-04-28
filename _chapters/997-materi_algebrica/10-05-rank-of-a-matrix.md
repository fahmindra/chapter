---
layout: chapter
title: "Rank of a Matrix"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 5
permalink: /materi-algebrica/vectors-and-matrices/rank-of-a-matrix/
---

rouche-capellilinear systemsdeterminant relationinvertibilitydimensioncolumn spacerow spaceother methodscomputational approachnonzero rowsrow echelon formgaussian eliminationsubmatricesminorsrank-nullitykernel and imagelinear independencerank boundsdefinitionstructuresmethodsfoundations

## Definition

The rank of a matrix $A$, denoted $r \left(\right. A \left.\right)$ or $rank \left(\right. A \left.\right)$, is the maximum number of linearly independent rows (or equivalently, columns) of $A$. For an $m \times n$ matrix $A$, the rank satisfies:

$$0 \leq r \left(\right. A \left.\right) \leq min \left(\right. m , n \left.\right)$$

The rank of a matrix $A$ equals the dimension of the image of the associated linear transformation $T_{A} : \mathbb{R}^{n} \rightarrow \mathbb{R}^{m}$, defined by $T_{A} \left(\right. \mathbf{x} \left.\right) = A \mathbf{x}$. The complementary quantity $n - r \left(\right. A \left.\right)$ is the dimension of the kernel of $T_{A}$, the subspace of [vectors](https://algebrica.org/vectors/) mapped to zero. These two quantities are related by the rank-nullity theorem: for any $A \in M_{m , n} \left(\right. \mathbb{R} \left.\right)$ we have:

$$rank \left(\right. A \left.\right) + nullity \left(\right. A \left.\right) = n$$

> The rank is one of the most fundamental invariants of a matrix. It determines the solvability of [systems of linear equations](https://algebrica.org/systems-of-linear-equations/) via the Rouché-Capelli theorem, and it coincides with the condition $r \left(\right. A \left.\right) = n$ for a square matrix to be [invertible](https://algebrica.org/inverse-matrix/).

## Submatrices and minors

A submatrix of a matrix $A \in M_{m , n} \left(\right. \mathbb{R} \left.\right)$ is any matrix obtained by selecting $k$ rows and $h$ columns from $A$, preserving the original order of elements, with $k \leq m$ and $h \leq n$. For example, selecting rows 1 and 3 and columns 1, 2, and 4 from a $3 \times 4$ matrix $A$ yields the $2 \times 3$ submatrix:

$$B = \left(\right. a_{11} & a_{12} & a_{14} \\ a_{31} & a_{32} & a_{34} \left.\right)$$

A minor of order $p$ of a matrix $A$ is the [determinant](https://algebrica.org/determinant/) of a square submatrix of size $p \times p$ extracted from $A$. Since the determinant is defined only for square matrices, only square submatrices give rise to minors.

## Definition via minors

The rank of a matrix $A$ is the largest integer $r$ such that at least one minor of order $r$ is nonzero. Equivalently, all minors of order $r + 1$ are zero.

The following example computes the rank of a $3 \times 4$ matrix. Consider:

$$A = \left(\right. 1 & 2 & 3 & 4 \\ 2 & 4 & 6 & 8 \\ 1 & 0 & 1 & 2 \left.\right)$$

The second row is exactly twice the first, so any $3 \times 3$ minor involving both rows will have two proportional rows and therefore vanish. One can verify that all minors of order 3 are zero. However, the $2 \times 2$ submatrix extracted from rows 1 and 3 and columns 1 and 2 gives:

$$det \left(\right. 1 & 2 \\ 1 & 0 \left.\right) = 0 - 2 = - 2 \neq 0$$

Since there exists a nonzero minor of order 2 and all minors of order 3 are zero, the rank of $A$ is:

$$r \left(\right. A \left.\right) = 2$$

## Definition via vector spaces

The rank of a matrix $A = \left(\right. a_{i j} \left.\right) \in M_{m , n} \left(\right. \mathbb{R} \left.\right)$ can also be defined as the common dimension of the row space and the column space of $A$. The rows of $A$, viewed as vectors $R_{1} , R_{2} , \ldots , R_{m} \in \mathbb{R}^{n}$, span a subspace of $\mathbb{R}^{n}$ called the row space of $A$. The columns of $A$, viewed as vectors $C_{1} , C_{2} , \ldots , C_{n} \in \mathbb{R}^{m}$, span a subspace of $\mathbb{R}^{m}$ called the column space of $A$. A fundamental result of linear algebra states that these two subspaces always have the same dimension, which equals the rank of $A$. Consider the matrix:

$$A = \left(\right. 1 & 0 & 2 \\ - 1 & 3 & 1 \left.\right)$$

The rows $\left(\right. 1 , 0 , 2 \left.\right)$ and $\left(\right. - 1 , 3 , 1 \left.\right)$ are not proportional, so they are linearly independent and span a subspace of dimension 2 in $\mathbb{R}^{3}$. Therefore $r \left(\right. A \left.\right) = 2$.

> The two definitions — via minors and via vector spaces — are equivalent. The minor-based definition is more direct for computation, while the vector space definition connects the rank to the theory of [linear combinations](https://algebrica.org/linear-combinations/) and dimension.

## Computing the rank via Gaussian elimination

For matrices of large order, computing all minors is impractical. The standard computational method is [Gaussian elimination](https://algebrica.org/solving-linear-systems-using-gaussian-elimination/): reduce $A$ to row echelon form by applying elementary row operations, which do not change the rank. The rank equals the number of nonzero rows in the reduced matrix. Consider the matrix from the previous example:

$$A = \left(\right. 1 & 2 & 3 & 4 \\ 2 & 4 & 6 & 8 \\ 1 & 0 & 1 & 2 \left.\right)$$

Subtracting twice the first row from the second, and the first row from the third:

$$\left(\right. 1 & 2 & 3 & 4 \\ 0 & 0 & 0 & 0 \\ 0 & - 2 & - 2 & - 2 \left.\right)$$

Swapping the second and third rows:

$$\left(\right. 1 & 2 & 3 & 4 \\ 0 & - 2 & - 2 & - 2 \\ 0 & 0 & 0 & 0 \left.\right)$$

The row echelon form has 2 nonzero rows, confirming $r \left(\right. A \left.\right) = 2$.

## Properties of the rank

- $r \left(\right. A \left.\right) = 0$ if and only if $A$ is the zero matrix.
- For a square matrix $A$ of order $n$, $r \left(\right. A \left.\right) = n$ if and only if $A$ is nonsingular, that is $det \left(\right. A \left.\right) \neq 0$.
- $r \left(\right. A \left.\right) = r \left(\right. A^{T} \left.\right)$. The rank is unchanged by transposition.
- $r \left(\right. A + B \left.\right) \leq r \left(\right. A \left.\right) + r \left(\right. B \left.\right)$.
- $r \left(\right. A B \left.\right) \leq min \left(\right. r \left(\right. A \left.\right) , r \left(\right. B \left.\right) \left.\right)$.

> The rank appears in the Rouché-Capelli theorem, which characterizes the compatibility of a system of linear equations $A \mathbf{x} = \mathbf{b}$: the system is consistent if and only if $r \left(\right. A \left.\right) = r \left(\right. A \left|\right. \mathbf{b} \left.\right)$, where $A \left|\right. \mathbf{b}$ denotes the augmented matrix. When consistent, the solution space has dimension $n - r \left(\right. A \left.\right)$.
