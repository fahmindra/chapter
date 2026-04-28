---
layout: chapter
title: "Matrices"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 2
permalink: /materi-algebrica/vectors-and-matrices/matrices/
---

determinantdot productadditive inversematrix multiplicationscalar multiplicationmatrix subtractionmatrix additionidentity matrixtransposemain diagonalsymmetric matrixtriangular matrixdiagonal matrixsquare matrixzero matrixcolumn vectorrow vectornotationentriesdimensionsmatrixoperationstypesfoundations

## Introduction

A matrix is a rectangular array of [real numbers](https://algebrica.org/types-of-numbers) arranged in rows and columns. A matrix with $m$ rows and $n$ columns is said to have dimensions $m \times n$, and is called an $m \times n$ matrix. For example, a $3 \times 2$ matrix has 3 rows and 2 columns. Each number appearing in a matrix is called an element. Elements are identified by two subscript indices: the first indicates the row and the second the column. Thus $a_{2 , 3}$ denotes the element in the second row and third column. A matrix $A$ of dimensions $m \times n$ is written as follows:

$$A = \left(\right. a_{11} & a_{12} & \hdots & a_{1 n} \\ a_{21} & a_{22} & \hdots & a_{2 n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m 1} & a_{m 2} & \hdots & a_{m n} \left.\right)$$

This is also written in compact form as $A = \left(\right. a_{i j} \left.\right)$, where $a_{i j}$ denotes the element in the $i$-th row and $j$-th column, with $1 \leq i \leq m$ and $1 \leq j \leq n$.

> The set of all $m \times n$ matrices with real entries forms an abelian group under addition. When restricted to square matrices of order $n$, the additional structure of matrix multiplication makes $M_{n \times n} \left(\right. \mathbb{R} \left.\right)$ a ring. The subset of invertible matrices of order $n$ forms a [group](https://algebrica.org/groups/) under multiplication, known as the general linear group $G L \left(\right. n , \mathbb{R} \left.\right)$.

## Vectors and the zero matrix

A matrix consisting of a single row is called a row [vector](https://algebrica.org/vectors/), and a matrix consisting of a single column is called a column vector. The following are a row vector $A$ with 3 columns and a column vector $B$ with 3 rows:

$$A = \left(\right. a_{1} & a_{2} & a_{3} \left.\right) B = \left(\right. b_{1} \\ b_{2} \\ b_{3} \left.\right)$$

A matrix in which every element is equal to zero is called the zero matrix, denoted $O$. The zero matrix plays the role of the additive identity in matrix addition, as discussed below.

> Row and column vectors are matrices in the usual sense and obey all the same algebraic rules. They are treated as special cases here for clarity, but are studied more extensively in the context of [linear combinations](https://algebrica.org/linear-combinations/) and vector spaces.

## Square matrices and special types

A matrix is called square when its number of rows equals its number of columns, that is, when it has dimensions $n \times n$. The integer $n$ is called the order of the matrix. In a square matrix, the elements $a_{i j}$ for which $i = j$ form the main diagonal. The elements for which $i + j = n + 1$ form the secondary diagonal:

$$A = \left(\right. \mathbf{\mathit{a}}_{11} & a_{12} & a_{13} \\ a_{21} & \mathbf{\mathit{a}}_{22} & a_{23} \\ a_{31} & a_{32} & \mathbf{\mathit{a}}_{33} \left.\right)$$

A square matrix in which all elements outside the main diagonal are zero is called a diagonal matrix. The following is an example of a $3 \times 3$ diagonal matrix:

$$D = \left(\right. 4 & 0 & 0 \\ 0 & 5 & 0 \\ 0 & 0 & 6 \left.\right)$$

A square matrix is called upper triangular if all elements below the main diagonal are zero, and lower triangular if all elements above the main diagonal are zero:

$$U = \left(\right. 2 & - 1 & 3 \\ 0 & 5 & 4 \\ 0 & 0 & 7 \left.\right) L = \left(\right. 3 & 0 & 0 \\ - 2 & 6 & 0 \\ 5 & 1 & 4 \left.\right)$$

A square matrix $A$ is called symmetric if it equals its own transpose, that is, if $A = A^{T}$. This means that $a_{i j} = a_{j i}$ for all $i$ and $j$: the element in row $i$ and column $j$ equals the element in row $j$ and column $i$. The following is a $3 \times 3$ symmetric matrix:

$$S = \left(\right. 1 & 3 & - 2 \\ 3 & 0 & 5 \\ - 2 & 5 & 4 \left.\right)$$

> Symmetric matrices arise naturally in many areas of mathematics, including quadratic forms, inner product spaces, and spectral theory. Every real symmetric matrix has real [eigenvalues](https://algebrica.org/eigenvalues-and-eigenvectors/) and an orthogonal basis of eigenvectors, a result known as the spectral theorem.

## Transpose

The transpose of a matrix $A$ of dimensions $m \times n$, denoted $A^{T}$, is the matrix of dimensions $n \times m$ obtained by interchanging the rows and columns of $A$. Formally, the element in position $\left(\right. i , j \left.\right)$ of $A^{T}$ is the element in position $\left(\right. j , i \left.\right)$ of $A$. For example:

$$A = \left(\right. 2 & - 1 & 3 \\ 7 & 5 & 4 \\ 9 & 6 & 8 \left.\right) A^{T} = \left(\right. 2 & 7 & 9 \\ - 1 & 5 & 6 \\ 3 & 4 & 8 \left.\right)$$

The transpose satisfies the following properties, for matrices $A$ and $B$ of compatible dimensions and any scalar $k$:

- $\left(\right. A^{T} \left.\right)^{T} = A$
- $\left(\right. A + B \left.\right)^{T} = A^{T} + B^{T}$
- $\left(\right. k A \left.\right)^{T} = k A^{T}$
- $\left(\right. A B \left.\right)^{T} = B^{T} A^{T}$

> The identity $\left(\right. A B \left.\right)^{T} = B^{T} A^{T}$ reverses the order of the factors. This reversal is necessary because matrix multiplication is not commutative, and it recurs in several other contexts, including the inverse of a product.

## Additive inverse matrix

The additive inverse of a matrix $A$, denoted $- A$, is the matrix obtained by negating every element of $A$: each entry $a_{i j}$ becomes $- a_{i j}$. The matrices $A$ and $- A$ have the same dimensions, and their sum is the zero matrix:

$$A + \left(\right. - A \left.\right) = O$$

For example:

$$A = \left(\right. 2 & - 1 & 3 \\ 7 & 5 & 4 \\ 9 & 6 & 8 \left.\right) - A = \left(\right. - 2 & 1 & - 3 \\ - 7 & - 5 & - 4 \\ - 9 & - 6 & - 8 \left.\right)$$

## Matrix addition and subtraction

Two matrices can be added or subtracted only if they have the same dimensions. Given two $m \times n$ matrices $A = \left(\right. a_{i j} \left.\right)$ and $B = \left(\right. b_{i j} \left.\right)$, their sum $C = A + B$ is the $m \times n$ matrix defined by:

$$c_{i j} = a_{i j} + b_{i j}$$

That is, each element of $C$ is the sum of the corresponding elements of $A$ and $B$. The following example illustrates the computation for two $2 \times 3$ matrices:

$$A = \left(\right. 2 & - 1 & 3 \\ 7 & 5 & 4 \left.\right) B = \left(\right. 4 & 0 & - 2 \\ 1 & 3 & 6 \left.\right)$$

The sum is:

$$A + B & = \left(\right. \begin{matrix}2 + 4 & - 1 + 0 & 3 + \left(\right. - 2 \left.\right) \\ 7 + 1 & 5 + 3 & 4 + 6\end{matrix} \left.\right) \\ & = \left(\right. \begin{matrix}6 & - 1 & 1 \\ 8 & 8 & 10\end{matrix} \left.\right)$$

The difference $A - B$ is defined as $A + \left(\right. - B \left.\right)$, that is, the sum of $A$ and the additive inverse of $B$. Matrix addition satisfies the following properties, for any matrices $A$, $B$, $C$ of dimensions $m \times n$:

- Commutativity: $A + B = B + A$. The order in which two matrices are added does not affect the result.
- Associativity: $\left(\right. A + B \left.\right) + C = A + \left(\right. B + C \left.\right)$. Sums of three or more matrices can be computed in any grouping.
- Additive identity: $A + O = A$, where $O$ is the zero matrix of the same dimensions. Adding the zero matrix leaves $A$ unchanged.
- Additive inverse: $A + \left(\right. - A \left.\right) = O$. Every matrix has a unique additive inverse.

## Scalar multiplication

Given a matrix $A = \left(\right. a_{i j} \left.\right)$ of dimensions $m \times n$ and a real number $k$, the scalar multiple $k A$ is the $m \times n$ matrix whose element in position $\left(\right. i , j \left.\right)$ is $k \cdot a_{i j}$. Every entry of the matrix is multiplied by $k$. For example, with $k = 2$:

$$A = \left(\right. 1 & - 2 & 4 \\ 0 & 3 & - 1 \left.\right) 2 A = \left(\right. 2 & - 4 & 8 \\ 0 & 6 & - 2 \left.\right)$$

Scalar multiplication satisfies the following properties, for matrices $A$ and $B$ of the same dimensions and real numbers $k$ and $h :$

- Associativity: $k \left(\right. h A \left.\right) = \left(\right. k h \left.\right) A$. Successive scalar multiplications can be combined into one.
- Distributivity over matrix addition: $k \left(\right. A + B \left.\right) = k A + k B$. A scalar distributes over a sum of matrices.
- Distributivity over scalar addition: $\left(\right. k + h \left.\right) A = k A + h A$. A sum of scalars distributes over a single matrix.

## Matrix multiplication

Matrix multiplication is defined under a compatibility condition: the product $A B$ is defined only when the number of columns of $A$ equals the number of rows of $B$. If $A$ has dimensions $m \times n$ and $B$ has dimensions $n \times p$, the product $C = A B$ is a matrix of dimensions $m \times p$, whose element in position $\left(\right. i , j \left.\right)$ is defined by:

$$c_{i j} = \sum_{k = 1}^{n} a_{i k} b_{k j}$$

Each entry $c_{i j}$ is computed by taking the dot product of the $i$-th row of $A$ with the $j$-th column of $B$: multiply corresponding entries pairwise and sum the results. The following example computes the product of a $2 \times 3$ matrix $A$ and a $3 \times 2$ matrix $B$:

$$A = \left(\right. 1 & - 2 & 3 \\ 0 & 4 & - 1 \left.\right) B = \left(\right. 2 & 0 \\ - 1 & 5 \\ 4 & - 3 \left.\right)$$

The entries $c_{i j}$ of the product matrix $A B$ are obtained by multiplying each row of $A$ by each column of $B$:

$$c_{11} & = \left(\right. 1 \left.\right) \left(\right. 2 \left.\right) + \left(\right. - 2 \left.\right) \left(\right. - 1 \left.\right) + \left(\right. 3 \left.\right) \left(\right. 4 \left.\right) = 16 \\ c_{12} & = \left(\right. 1 \left.\right) \left(\right. 0 \left.\right) + \left(\right. - 2 \left.\right) \left(\right. 5 \left.\right) + \left(\right. 3 \left.\right) \left(\right. - 3 \left.\right) = - 19 \\ c_{21} & = \left(\right. 0 \left.\right) \left(\right. 2 \left.\right) + \left(\right. 4 \left.\right) \left(\right. - 1 \left.\right) + \left(\right. - 1 \left.\right) \left(\right. 4 \left.\right) = - 8 \\ c_{22} & = \left(\right. 0 \left.\right) \left(\right. 0 \left.\right) + \left(\right. 4 \left.\right) \left(\right. 5 \left.\right) + \left(\right. - 1 \left.\right) \left(\right. - 3 \left.\right) = 23$$

The result is a $2 \times 2$ matrix, consistent with the dimensions $m \times p = 2 \times 2$.

$$C = A B = \left(\right. 16 & - 19 \\ - 8 & 23 \left.\right)$$

> Matrix multiplication is not commutative in general: even when both $A B$ and $B A$ are defined, it is typically the case that $A B \neq B A$. This distinguishes matrix multiplication from multiplication of real numbers and is one of its most consequential properties.

---

The identity matrix of order $n$, denoted $I_{n}$, is the $n \times n$ square matrix with ones on the main diagonal and zeros elsewhere. It acts as the multiplicative identity: for any matrix $A$ of compatible dimensions,

$$A \cdot I = I \cdot A = A$$

For example:

$$\left(\right. 3 & 5 \\ 1 & - 2 \left.\right) \cdot \left(\right. 1 & 0 \\ 0 & 1 \left.\right) = \left(\right. 3 & 5 \\ 1 & - 2 \left.\right)$$

Matrix multiplication satisfies the following properties, for matrices of compatible dimensions:

- Associativity: $\left(\right. A B \left.\right) C = A \left(\right. B C \left.\right)$. The order in which successive products are computed does not affect the result.
- Left distributivity: $A \left(\right. B + C \left.\right) = A B + A C$. Multiplication distributes over addition from the left.
- Right distributivity: $\left(\right. B + C \left.\right) A = B A + C A$. Multiplication distributes over addition from the right.
- Non-commutativity: in general, $A B \neq B A$, even when both products are defined.

---

To every square matrix of order $n$ one associates a real number called the [determinant](https://algebrica.org/determinant/) of the matrix, denoted $det \left(\right. A \left.\right)$. The determinant encodes fundamental information about the matrix, including whether it is invertible, as discussed in the entry on the [inverse matrix](https://algebrica.org/inverse-matrix/).
