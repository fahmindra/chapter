---
layout: chapter
title: "Determinant of a Square Matrix"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 3
permalink: /materi-algebrica/vectors-and-matrices/determinant-of-a-square-matrix/
---

invertible matrixsingular matrixscaling factorzero determinanttranspose invariancemultiplicativitylinearitysarrus rulelaplace expansiondiagonal matricestriangular matrices2x2 determinant1x1 determinantvolume scalinginvertibilityfunctionnotationsquare matrixdeterminantpropertiescomputationfoundations

## Definition

To every square [matrix](https://algebrica.org/matrices/) of order $n$ one can associate a [real number](https://algebrica.org/types-of-numbers/) called the determinant of the matrix, denoted $det \left(\right. A \left.\right)$ or $\left|\right. A \left|\right.$. The determinant is a scalar-valued function that encodes both algebraic and geometric properties of the associated linear transformation:

$$det : M_{n} \left(\right. \mathbb{R} \left.\right) \rightarrow \mathbb{R}$$

It determines whether the matrix is invertible and measures the factor by which the transformation scales volumes. It appears in the explicit solution of [systems of linear equations](https://algebrica.org/systems-of-linear-equations/) via [Cramer’s rule](https://algebrica.org/cramers-rule/), and plays a central role in the study of [eigenvalues](https://algebrica.org/eigenvalues-and-eigenvectors/) and linear transformations.

The determinant of a matrix of order 1 is the element itself:

$$A = \left(\right. a_{11} \left.\right) \Longrightarrow det \left(\right. A \left.\right) = a_{11}$$

For a square matrix of order 2, the determinant is the difference between the product of the elements on the main diagonal and the product of the elements on the secondary diagonal:

$$A = \left(\right. a_{11} & a_{12} \\ a_{21} & a_{22} \left.\right) \Longrightarrow det \left(\right. A \left.\right) = a_{11} \cdot a_{22} - a_{21} \cdot a_{12}$$

For example:

$$A = \left(\right. 3 & 2 \\ 1 & 4 \left.\right) \Longrightarrow det \left(\right. A \left.\right) = 3 \cdot 4 - 1 \cdot 2 = 10$$

## Diagonal and triangular matrices

For a diagonal matrix, that is a square matrix in which all off-diagonal elements are zero, the determinant equals the product of the elements on the main diagonal:

$$A = \left(\right. a_{11} & 0 & \hdots & 0 \\ 0 & a_{22} & \hdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \hdots & a_{n n} \left.\right) \Longrightarrow det \left(\right. A \left.\right) = a_{11} \cdot a_{22} \cdot \ldots \cdot a_{n n}$$

The same result holds for upper and lower triangular matrices. In both cases, the determinant is the product of the diagonal entries, since all the additional terms in the expansion vanish.

## Laplace expansion

The determinant of a square matrix of order $n \geq 3$ can be computed recursively using the cofactor expansion, also known as Laplace expansion. Given a square matrix $A = \left(\right. a_{i j} \left.\right)$ of order $n$, the minor $M_{i j}$ is the determinant of the $\left(\right. n - 1 \left.\right) \times \left(\right. n - 1 \left.\right)$ submatrix obtained by deleting the $i$-th row and $j$-th column of $A$. The cofactor $C_{i j}$ is defined as:

$$C_{i j} = \left(\right. - 1 \left.\right)^{i + j} \cdot M_{i j}$$

The sign factor $\left(\right. - 1 \left.\right)^{i + j}$ is positive when $i + j$ is even and negative when $i + j$ is odd. The determinant of $A$ is then obtained by expanding along any row $i$:

$$det \left(\right. A \left.\right) = \sum_{k = 1}^{n} a_{i k} \cdot C_{i k} = \sum_{k = 1}^{n} a_{i k} \cdot \left(\right. - 1 \left.\right)^{i + k} \cdot M_{i k}$$

The same result is obtained by expanding along any column $j$:

$$det \left(\right. A \left.\right) = \sum_{k = 1}^{n} a_{k j} \cdot C_{k j}$$

The following example illustrates the computation for a matrix of order 3. Consider:

$$A = \left(\right. 2 & 0 & - 1 \\ 3 & - 2 & 0 \\ 1 & 4 & 1 \left.\right)$$

Expanding along the first row, we compute the cofactor contribution of each element.

---

For $a_{11} = 2$, the minor is the determinant of the submatrix obtained by deleting row 1 and column 1:

$$C_{11} = \left(\right. - 1 \left.\right)^{1 + 1} \cdot det \left(\right. - 2 & 0 \\ 4 & 1 \left.\right) = \left(\right. + 1 \left.\right) \cdot \left(\right. - 2 - 0 \left.\right) = - 2$$

The contribution is $a_{11} \cdot C_{11} = 2 \cdot \left(\right. - 2 \left.\right) = - 4$.

---

For $a_{12} = 0$, the minor is:

$$C_{12} = \left(\right. - 1 \left.\right)^{1 + 2} \cdot det \left(\right. 3 & 0 \\ 1 & 1 \left.\right) = \left(\right. - 1 \left.\right) \cdot \left(\right. 3 - 0 \left.\right) = - 3$$

The contribution is $a_{12} \cdot C_{12} = 0 \cdot \left(\right. - 3 \left.\right) = 0$.

---

For $a_{13} = - 1$, the minor is:

$$C_{13} = \left(\right. - 1 \left.\right)^{1 + 3} \cdot det \left(\right. 3 & - 2 \\ 1 & 4 \left.\right) = \left(\right. + 1 \left.\right) \cdot \left(\right. 12 + 2 \left.\right) = 14$$

The contribution is $a_{13} \cdot C_{13} = \left(\right. - 1 \left.\right) \cdot 14 = - 14$.

---

Summing the three contributions we obtain:

$$det \left(\right. A \left.\right) = - 4 + 0 + \left(\right. - 14 \left.\right) = - 18$$

> The computational cost of Laplace expansion grows factorially with the order of the matrix, resulting in a time complexity of $O \left(\right. n ! \left.\right)$. For this reason, the method is impractical for large matrices in numerical applications, where more efficient algorithms such as LU decomposition are preferred.

## Sarrus’ rule

For matrices of order 3, the determinant can be computed using Sarrus’ rule, a direct mnemonic method equivalent to the Laplace expansion. Given the matrix:

$$A = \left(\right. a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \left.\right)$$

the determinant is:

$$det \left(\right. A \left.\right) & = a_{11} a_{22} a_{33} + a_{12} a_{23} a_{31} + a_{13} a_{21} a_{32} \\ & - a_{13} a_{22} a_{31} - a_{11} a_{23} a_{32} - a_{12} a_{21} a_{33}$$

The three positive terms correspond to the products along the three main diagonals (top-left to bottom-right), and the three negative terms correspond to the products along the three secondary diagonals (top-right to bottom-left). A convenient way to visualize this is to append the first two columns of $A$ to its right:

$$\left(\right. a_{11} & a_{12} & a_{13} & a_{11} & a_{12} \\ a_{21} & a_{22} & a_{23} & a_{21} & a_{22} \\ a_{31} & a_{32} & a_{33} & a_{31} & a_{32} \left.\right)$$

The following example applies Sarrus’ rule to a concrete matrix. Consider:

$$A = \left(\right. 1 & - 2 & 3 \\ 0 & 4 & - 1 \\ 2 & 1 & 0 \left.\right)$$

We obtain:

$$det \left(\right. A \left.\right) & = \left(\right. 1 \left.\right) \left(\right. 4 \left.\right) \left(\right. 0 \left.\right) + \left(\right. - 2 \left.\right) \left(\right. - 1 \left.\right) \left(\right. 2 \left.\right) + \left(\right. 3 \left.\right) \left(\right. 0 \left.\right) \left(\right. 1 \left.\right) \\ & - \left(\right. 3 \left.\right) \left(\right. 4 \left.\right) \left(\right. 2 \left.\right) - \left(\right. 1 \left.\right) \left(\right. - 1 \left.\right) \left(\right. 1 \left.\right) - \left(\right. - 2 \left.\right) \left(\right. 0 \left.\right) \left(\right. 0 \left.\right) \\ & = 0 + 4 + 0 - 24 + 1 + 0 \\ & = - 19$$

> Sarrus’ rule applies exclusively to matrices of order 3. It does not generalize to higher orders.

## Properties of the determinant

The following are the fundamental properties of the determinant.

- If $A$ has an entire row or column of zeros, then $det \left(\right. A \left.\right) = 0$.
- If two rows or two columns of $A$ are proportional, then $det \left(\right. A \left.\right) = 0$. More generally, if one row or column is a [linear combination](https://algebrica.org/linear-combinations/) of others, then $det \left(\right. A \left.\right) = 0$.
- If all elements of a row or column are multiplied by a scalar $k$, the determinant is multiplied by $k$. Equivalently, a scalar factor can be extracted from any row or column: $det \left(\right. k A \left.\right) = k^{n} det \left(\right. A \left.\right)$ for a matrix of order $n$.
- The determinant of a product equals the product of the determinants: $det \left(\right. A B \left.\right) = det \left(\right. A \left.\right) \cdot det \left(\right. B \left.\right)$.
- The determinant of the transpose equals the determinant of the original matrix: $det \left(\right. A^{T} \left.\right) = det \left(\right. A \left.\right)$.
- A square matrix $A$ is invertible if and only if $det \left(\right. A \left.\right) \neq 0$. When $det \left(\right. A \left.\right) = 0$, the matrix is called singular, as discussed in the entry on the [inverse matrix](https://algebrica.org/inverse-matrix/).
