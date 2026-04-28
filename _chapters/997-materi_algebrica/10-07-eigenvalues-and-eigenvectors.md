---
layout: chapter
title: "Eigenvalues and Eigenvectors"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 7
permalink: /materi-algebrica/vectors-and-matrices/eigenvalues-and-eigenvectors/
---

trace and determinantjordan formdiagonalizationlinear independencealgebraic multiplicitygeometric multiplicityeigenspacescomplex eigenvaluesroots and multiplicitydeterminant conditioncharacteristic polynomialcharacteristic equationeigen equationnon-zero conditionscaling factorinvariant directionseigenvalueeigenvectorlinear transformationstructureconstructionfoundations

## Definition

A linear transformation, represented by a square [matrix](https://algebrica.org/matrices/) $A$, acts on vectors by moving them in space. It can stretch, compress, rotate, or reflect them, and in general the image of a [vector](https://algebrica.org/vectors/) points in a different direction from the original. Among all vectors however there are those for which the action of $A$ is particularly simple. The transformation scales them by a constant factor, leaving their direction unchanged. Such vectors are called eigenvectors of $A$, and the corresponding scaling factors are called eigenvalues.

> Eigenvectors reveal the intrinsic geometry of a linear transformation, and the collection of eigenvalues encodes information about the matrix that is invariant under a wide class of coordinate changes.

---

Let $A$ be a square [matrix](https://algebrica.org/matrices/) of order $n$ with entries in $\mathbb{R}$ or $\mathbb{C}$. A non-zero [vector](https://algebrica.org/vectors/) $\mathbf{v}$ is called an eigenvector of $A$ if there exists a scalar $\lambda$ such that the following equation holds:

$$A \mathbf{v} = \lambda \mathbf{v}$$

The scalar $\lambda$ is called the eigenvalue of $A$ associated with $\mathbf{v}$. The condition requires that $A$ maps $\mathbf{v}$ to a scalar multiple of itself: the vector $\mathbf{v}$ may be stretched or compressed, and its orientation may be reversed if $\lambda$ is negative, but it remains on the same line through the origin. Eigenvectors are the invariant directions of the transformation and eigenvalues are the scaling factors along those directions.

> The zero vector is excluded by convention. The equation $A 0 = \lambda 0$ is satisfied for every $\lambda$ and carries no information about the matrix.

---

The following diagram illustrates this idea for the square matrix:

$$A = \left(\right. 2 & 1 \\ 1 & 2 \left.\right)$$

![Eigenvalues and eigenvectors.](https://algebrica.org/wp-content/uploads/resources/images/eigenvectors.png "Eigenvalues and eigenvectors.")

The [unit circle](https://algebrica.org/unit-circle/) is mapped to an [ellipse](https://algebrica.org/ellipse/): most vectors change direction under the transformation. The two eigenvectors $\mathbf{v}_{1}$ and $\mathbf{v}_{2}$ are the exception. They remain on the same line through the origin, scaled by $\lambda_{1} = 3$ and $\lambda_{2} = 1$ respectively.

## The characteristic equation

Rewriting the eigenvalue equation as $\left(\right. A - \lambda I \left.\right) \mathbf{v} = 0$, where $I$ is the identity matrix of order $n$, it is clear that a non-zero solution $\mathbf{v}$ exists precisely when the matrix $A - \lambda I$ is singular. The condition for singularity is that its determinant vanishes. The equation

$$det \left(\right. A - \lambda I \left.\right) = 0$$

is called the characteristic equation of $A$. Expanding the determinant yields a polynomial of degree $n$ in $\lambda$, known as the characteristic polynomial of $A$. The eigenvalues of $A$ are the roots of this polynomial, and by the fundamental theorem of algebra there are exactly $n$ of them, counted with multiplicity, in $\mathbb{C}$.

> A matrix with real entries has a characteristic polynomial with real coefficients, but this does not prevent complex roots. Complex eigenvalues of a real matrix always appear in conjugate pairs.

## Eigenspaces

For each eigenvalue $\lambda_{0}$, the [set](https://algebrica.org/sets/) of all vectors satisfying $A \mathbf{v} = \lambda_{0} \mathbf{v}$ is a subspace of $\mathbb{R}^{n}$ or $\mathbb{C}^{n}$. It coincides with the [kernel](https://algebrica.org/?s=kernel) of $A - \lambda_{0} I$ and is called the eigenspace of $A$ associated with $\lambda_{0}$:

$$E_{\lambda_{0}} = ker ⁡ \left(\right. A - \lambda_{0} I \left.\right) = \left{\right. \mathbf{v} : \left(\right. A - \lambda_{0} I \left.\right) \mathbf{v} = 0 \left.\right}$$

The dimension of $E_{\lambda_{0}}$ is called the geometric multiplicity of $\lambda_{0}$. Separately, the multiplicity of $\lambda_{0}$ as a root of the characteristic polynomial is called the algebraic multiplicity of $\lambda_{0}$. It can be shown that the geometric multiplicity never exceeds the algebraic one, and the two coincide in the most well-behaved cases.

## Example 1

Consider the following [matrix](https://algebrica.org/matrices/):

$$A = \left(\right. 3 & 1 \\ 0 & 2 \left.\right)$$

We compute the characteristic [polynomial](https://algebrica.org/polynomials/) by forming the matrix $A - \lambda I$ and computing its [determinant](https://algebrica.org/determinant/). Since $A - \lambda I$ is upper triangular, its determinant is the product of the diagonal entries:

$$det \left(\right. A - \lambda I \left.\right) = \left(\right. 3 - \lambda \left.\right) \left(\right. 2 - \lambda \left.\right)$$

Setting this expression equal to zero gives $\lambda_{1} = 2$ and $\lambda_{2} = 3$. For $\lambda_{1} = 2$, we solve $\left(\right. A - 2 I \left.\right) \mathbf{v} = 0$. The matrix $A - 2 I$ reduces to:

$$A - 2 I = \left(\right. 1 & 1 \\ 0 & 0 \left.\right)$$

The system yields the single condition $v_{1} + v_{2} = 0$, so $v_{1} = - v_{2}$. Taking $v_{2} = 1$, the eigenspace $E_{2}$ is spanned by:

$$\mathbf{v}_{1} = \left(\right. - 1 \\ 1 \left.\right)$$

For $\lambda_{2} = 3$, the matrix $A - 3 I$ is:

$$A - 3 I = \left(\right. 0 & 1 \\ 0 & - 1 \left.\right)$$

Both rows give the condition $v_{2} = 0$, leaving $v_{1}$ free. Taking $v_{1} = 1$, the eigenspace $E_{3}$ is spanned by:

$$\mathbf{v}_{2} = \left(\right. 1 \\ 0 \left.\right)$$

The matrix $A$ has therefore eigenvalue $\lambda_{1} = 2$ with eigenvector $\left(\right. - 1 , 1 \left.\right)^{T}$, and eigenvalue $\lambda_{2} = 3$ with eigenvector $\left(\right. 1 , 0 \left.\right)^{T}$.

## Example 2

Consider the matrix

$$A = \left(\right. 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3 \left.\right)$$

The matrix $A - \lambda I$ is block upper triangular, so its determinant is again the product of the diagonal entries. The characteristic polynomial is the following:

$$p \left(\right. \lambda \left.\right) = \left(\right. 2 - \lambda \left.\right)^{2} \left(\right. 3 - \lambda \left.\right)$$

Setting $p \left(\right. \lambda \left.\right) = 0$ gives two eigenvalues: $\lambda_{1} = 2$, with algebraic multiplicity two, and $\lambda_{2} = 3$, with algebraic multiplicity one.

For $\lambda_{2} = 3$, we solve $\left(\right. A - 3 I \left.\right) \mathbf{v} = 0$. The matrix $A - 3 I$ is:

$$A - 3 I = \left(\right. - 1 & 1 & 0 \\ 0 & - 1 & 0 \\ 0 & 0 & 0 \left.\right)$$

The second row gives $v_{2} = 0$, and the first row then gives $v_{1} = 0$, leaving $v_{3}$ free. Taking $v_{3} = 1$, the eigenspace $E_{3}$ is spanned by:

$$\mathbf{v}_{1} = \left(\right. 0 \\ 0 \\ 1 \left.\right)$$

For $\lambda_{1} = 2$, we solve $\left(\right. A - 2 I \left.\right) \mathbf{v} = 0$. The matrix $A - 2 I$ is:

$$A - 2 I = \left(\right. 0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \left.\right)$$

The first row gives $v_{2} = 0$ and the third row gives $v_{3} = 0$, while $v_{1}$ remains free. Taking $v_{1} = 1$, the eigenspace $E_{2}$ is one-dimensional, spanned by:

$$\mathbf{v}_{2} = \left(\right. 1 \\ 0 \\ 0 \left.\right)$$

The geometric multiplicity of $\lambda_{1} = 2$ is therefore one, while its algebraic multiplicity is two. Since these two values differ, the matrix $A$ is not diagonalizable. It possesses only two [linearly independent](https://algebrica.org/rank-of-a-matrix/) eigenvectors, which is insufficient to form a basis of $\mathbb{R}^{3}$.

## Linear independence of eigenvectors

Eigenvectors corresponding to distinct eigenvalues are always linearly independent. More precisely, if $\lambda_{1} , \ldots , \lambda_{k}$ are pairwise distinct eigenvalues of $A$ with associated eigenvectors $\mathbf{v}_{1} , \ldots , \mathbf{v}_{k}$, then $\mathbf{v}_{1} , \ldots , \mathbf{v}_{k}$ are linearly independent. The proof proceeds by induction on $k$ and uses the fact that each eigenvalue is distinct to derive a contradiction from any supposed linear dependence relation.

As a consequence, a square matrix of order $n$ with $n$ distinct eigenvalues always possesses $n$ linearly independent eigenvectors, and therefore admits a basis of eigenvectors.

## Diagonalization

A matrix $A$ of order $n$ is called diagonalizable if it can be written in the form

$$A = P D P^{- 1}$$

where $P$ is an invertible matrix and $D$ is diagonal. The columns of $P$ are eigenvectors of $A$, and the corresponding diagonal entries of $D$ are the associated eigenvalues. This decomposition, when it exists, simplifies many computations substantially. In particular, the $k$-th power of $A$ takes the form:

$$A^{k} = P D^{k} P^{- 1}$$

Since raising a diagonal matrix to a power amounts to raising each diagonal entry to that power, this avoids the need to perform $k$ successive matrix multiplications.

A matrix is diagonalizable if and only if, for every eigenvalue, its geometric multiplicity equals its algebraic multiplicity. When this condition fails, the matrix cannot be diagonalized but can be reduced to Jordan canonical form, which is the closest diagonal-like structure available in the general case.

## Trace, determinant and eigenvalues

Let $\lambda_{1} , \lambda_{2} , \ldots , \lambda_{n}$ be the eigenvalues of $A$ counted with algebraic multiplicity. Two classical identities relate them directly to entries of the matrix. The trace of $A$, defined as the sum of its diagonal entries, satisfies:

$$\text{tr} \left(\right. A \left.\right) = \lambda_{1} + \lambda_{2} + \hdots + \lambda_{n}$$

The determinant of $A$ satisfies:

$$det \left(\right. A \left.\right) = \lambda_{1} \cdot \lambda_{2} \hdots \lambda_{n}$$

Both identities follow from the structure of the characteristic polynomial. The second has a notable consequence: a matrix is singular if and only if zero is one of its eigenvalues. Together, these two relations offer a quick consistency check when eigenvalues are computed by hand, without requiring any additional verification.
