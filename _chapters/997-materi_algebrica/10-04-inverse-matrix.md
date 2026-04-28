---
layout: chapter
title: "Inverse Matrix"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 4
permalink: /materi-algebrica/vectors-and-matrices/inverse-matrix/
---

lu decompositiongaussian eliminationadjugateminorcofactorrank conditionexistence conditionnon commutativitydeterminant relationtranspose inverseproduct inverseinverse of inverseuniquenessdeterminant conditionsingular matrixinvertible matrixidentity matrixdefinitioninverse matrixcomputationpropertiesfoundations

## Definition

Given a square [matrix](https://algebrica.org/matrices/) of order $n$, the inverse of $A$, denoted $A^{- 1}$, is the matrix such that:

$$A \cdot A^{- 1} = A^{- 1} \cdot A = I$$

where $I$ is the identity matrix of order $n$. When such a matrix exists, it is unique. A square matrix that admits an inverse is called invertible or nonsingular. A matrix that does not admit an inverse is called singular.

The inverse matrix represents the linear transformation that reverses the effect of the original transformation. If $A$ maps a vector $\mathbf{x}$ to $\mathbf{b}$, that is $A \mathbf{x} = \mathbf{b}$, then $A^{- 1}$ maps $\mathbf{b}$ back to $\mathbf{x}$:

$$A \mathbf{x} = \mathbf{b} \Longrightarrow \mathbf{x} = A^{- 1} \mathbf{b}$$

This is precisely the principle underlying the solution of [systems of linear equations](https://algebrica.org/systems-of-linear-equations/) via the inverse matrix.

A square matrix $A$ is invertible if and only if its [determinant](https://algebrica.org/determinant/) is nonzero:

$$A \text{is invertible} \Longleftrightarrow det \left(\right. A \left.\right) \neq 0$$

> The condition $det \left(\right. A \left.\right) \neq 0$ is both necessary and sufficient for invertibility. It is equivalent to requiring that the rows (or columns) of $A$ are linearly independent, and that the [rank](https://algebrica.org/rank-of-a-matrix/) of $A$ equals $n$. The set of all invertible matrices of order $n$ forms a group under matrix multiplication, known as the general linear group $G L \left(\right. n , \mathbb{R} \left.\right)$, discussed in the entry on [groups](https://algebrica.org/groups/).

## Properties of the inverse

The inverse matrix satisfies the following properties, for square matrices $A$ and $B$ of order $n$:

- $\left(\right. A^{- 1} \left.\right)^{- 1} = A$. The inverse of the inverse is the original matrix.
- $\left(\right. A B \left.\right)^{- 1} = B^{- 1} A^{- 1}$. The inverse of a product reverses the order of the factors.
- $\left(\right. A^{T} \left.\right)^{- 1} = \left(\right. A^{- 1} \left.\right)^{T}$. The inverse of the transpose equals the transpose of the inverse.
- $det \left(\right. A^{- 1} \left.\right) = \frac{1}{det \left(\right. A \left.\right)}$. The determinant of the inverse is the reciprocal of the determinant of $A$.

> The reversal of order in $\left(\right. A B \left.\right)^{- 1} = B^{- 1} A^{- 1}$ is necessary for the same reason as in the transpose: matrix multiplication is not commutative, so inverting a product requires inverting each factor and reversing their order.

## Computing the inverse: the cofactor method

The inverse of a square matrix $A$ of order $n$, when it exists, can be computed using the cofactor method. Given a square matrix $A = \left(\right. a_{i j} \left.\right)$, the minor $M_{i j}$ is the determinant of the $\left(\right. n - 1 \left.\right) \times \left(\right. n - 1 \left.\right)$ submatrix obtained by deleting the $i$-th row and $j$-th column of $A$. The cofactor $C_{i j}$ is defined as:

$$C_{i j} = \left(\right. - 1 \left.\right)^{i + j} \cdot M_{i j}$$

The cofactor matrix $C$ is the matrix whose entry in position $\left(\right. i , j \left.\right)$ is the cofactor $C_{i j}$. The transpose of the cofactor matrix, denoted $C^{T}$, is called the adjugate of $A$ and written $adj \left(\right. A \left.\right)$. The inverse is then given by:

$$A^{- 1} = \frac{1}{det \left(\right. A \left.\right)} C^{T} = \frac{1}{det \left(\right. A \left.\right)} adj \left(\right. A \left.\right)$$

The computation proceeds as follows: calculate the cofactor $C_{i j}$ for every entry of $A$, assemble the cofactor matrix $C$, take its transpose to obtain $adj \left(\right. A \left.\right)$, and divide every entry by $det \left(\right. A \left.\right)$.

## Example

Consider the following matrix:

$$A = \left(\right. 3 & 0 & 0 \\ 2 & 1 & 0 \\ - 1 & 4 & 2 \left.\right)$$

This is a lower triangular matrix. Its determinant is the product of the diagonal entries:

$$C_{11} & = \left(\right. + 1 \left.\right) det \left(\right. \begin{matrix}1 & 0 \\ 4 & 2\end{matrix} \left.\right) & 2 \\ C_{12} & = \left(\right. - 1 \left.\right) det \left(\right. \begin{matrix}2 & 0 \\ - 1 & 2\end{matrix} \left.\right) & - 4 \\ C_{13} & = \left(\right. + 1 \left.\right) det \left(\right. \begin{matrix}2 & 1 \\ - 1 & 4\end{matrix} \left.\right) & 9 \\ C_{21} & = \left(\right. - 1 \left.\right) det \left(\right. \begin{matrix}0 & 0 \\ 4 & 2\end{matrix} \left.\right) & 0 \\ C_{22} & = \left(\right. + 1 \left.\right) det \left(\right. \begin{matrix}3 & 0 \\ - 1 & 2\end{matrix} \left.\right) & 6 \\ C_{23} & = \left(\right. - 1 \left.\right) det \left(\right. \begin{matrix}3 & 0 \\ - 1 & 4\end{matrix} \left.\right) & - 12 \\ C_{31} & = \left(\right. + 1 \left.\right) det \left(\right. \begin{matrix}0 & 0 \\ 1 & 0\end{matrix} \left.\right) & 0 \\ C_{32} & = \left(\right. - 1 \left.\right) det \left(\right. \begin{matrix}3 & 0 \\ 2 & 0\end{matrix} \left.\right) & 0 \\ C_{33} & = \left(\right. + 1 \left.\right) det \left(\right. \begin{matrix}3 & 0 \\ 2 & 1\end{matrix} \left.\right) & 3$$

The cofactor matrix $C$ is assembled from the nine cofactors computed above:

$$C = \left(\right. 2 & - 4 & 9 \\ 0 & 6 & - 12 \\ 0 & 0 & 3 \left.\right)$$

Taking the transpose of $C$ gives the adjugate of $A$:

$$adj \left(\right. A \left.\right) = C^{T} = \left(\right. 2 & 0 & 0 \\ - 4 & 6 & 0 \\ 9 & - 12 & 3 \left.\right)$$

Dividing by $det \left(\right. A \left.\right) = 6$:

$$A^{- 1} = \frac{1}{6} \left(\right. 2 & 0 & 0 \\ - 4 & 6 & 0 \\ 9 & - 12 & 3 \left.\right) = \left(\right. \frac{1}{3} & 0 & 0 \\ - \frac{2}{3} & 1 & 0 \\ \frac{3}{2} & - 2 & \frac{1}{2} \left.\right)$$

> The cofactor method is exact but computationally expensive for large matrices, with complexity $O \left(\right. n ! \left.\right)$ due to the determinant evaluations involved. In numerical practice, the inverse is typically computed via [Gaussian elimination](https://algebrica.org/solving-linear-systems-using-gaussian-elimination/) or LU decomposition, which achieve $O \left(\right. n^{3} \left.\right)$ complexity.
