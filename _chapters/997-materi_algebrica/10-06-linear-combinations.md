---
layout: chapter
title: "Linear Combinations"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 6
permalink: /materi-algebrica/vectors-and-matrices/linear-combinations/
---

other structuresuniquenesssolution setdimensionlinear independencesubspacespanother operationssolvabilitysystem Ax=bmatrix-vector productlinear combinationvector additionscalar multiplicationother conceptsvector spacesgeometric meaningcoordinate formnotationscalars and vectorsdefinitionstructuresoperationsfoundations

## Definition

In linear algebra, a linear combination is the fundamental operation that relates [vectors](https://algebrica.org/vectors/) to one another within a given collection. Each vector is scaled by a real coefficient, and the scaled vectors are then summed to produce a new vector. Simple as this construction is, it generates the core concepts of the subject: span, linear independence, [rank](https://algebrica.org/rank-of-a-matrix/), and dimension. It also gives rise to the geometric objects that structure $\mathbb{R}^{n}$, including [lines](https://algebrica.org/lines/), planes, and higher-dimensional subspaces. Let $V = \mathbb{R}^{n}$ and consider a finite collection of vectors:

$$v_{1} , v_{2} , \ldots , v_{k} \in \mathbb{R}^{n}$$

A linear combination of these vectors is any vector of the form:

$$c_{1} v_{1} + c_{2} v_{2} + \hdots + c_{k} v_{k}$$

where $c_{1} , c_{2} , \ldots , c_{k} \in \mathbb{R}$ are real scalars. Each vector $v_{i}$ is multiplied by a scalar coefficient $c_{i}$, and the resulting scaled vectors are then added. The scalars determine how strongly each vector contributes to the final result. Although the definition is elementary, it captures the fundamental mechanism through which vectors interact inside $\mathbb{R}^{n}$.

---

A linear combination should not be viewed merely as a symbolic algebraic expression. Beyond the formal manipulation of symbols, it carries a clear and concrete geometric meaning. Consider two vectors $v , w \in \mathbb{R}^{n}$. By forming expressions of the type:

$$a v + b w$$

with $a , b \in \mathbb{R}$, we allow each vector to be independently scaled and then combined through vector addition. Varying the coefficients $a$ and $b$ produces an entire collection of vectors, all obtained from the same two building blocks.

- If the vectors $v$ and $w$ are not scalar multiples of one another, these combinations sweep out a plane passing through the origin. Every point of that plane can be reached by a suitable choice of the coefficients.
- If, on the other hand, the two vectors are collinear, all linear combinations collapse onto a single line through the origin, since one vector can already be expressed in terms of the other.

> In this way, linear combinations naturally generate geometric objects such as lines and planes, and more generally subsets of $\mathbb{R}^{n}$ that exhibit a linear structure. The dimension of the object obtained depends entirely on how the vectors relate to one another and on whether they contribute genuinely independent directions.

A vector $b \in \mathbb{R}^{n}$ is said to be a linear combination of the vectors $v_{1} , v_{2} , \ldots , v_{k} \in \mathbb{R}^{n}$ if and only if there exist scalars $c_{1} , c_{2} , \ldots , c_{k} \in \mathbb{R}$ such that:

$$b = c_{1} v_{1} + c_{2} v_{2} + \hdots + c_{k} v_{k}$$

## Coordinate representation

To understand more concretely how linear combinations operate, it is helpful to express everything in coordinates. Since vectors in $\mathbb{R}^{n}$ are represented as ordered $n$-tuples of real numbers, every operation on vectors can be described component by component. Suppose each vector $v_{i} \in \mathbb{R}^{n}$ has components:

$$v_{i} = \left(\right. v_{i 1} \\ v_{i 2} \\ \vdots \\ v_{i n} \left.\right)$$

When we form a linear combination of these vectors, the operation unfolds coordinatewise. Indeed, we obtain:

$$c_{1} v_{1} + \hdots + c_{k} v_{k} = \left(\right. c_{1} v_{11} + \hdots + c_{k} v_{k 1} \\ c_{1} v_{12} + \hdots + c_{k} v_{k 2} \\ \vdots \\ c_{1} v_{1 n} + \hdots + c_{k} v_{k n} \left.\right)$$

Each entry of the resulting vector is therefore a linear combination of [real numbers](https://algebrica.org/types-of-numbers/) drawn from the corresponding entries of the original vectors. In other words, scalar multiplication and vector addition are performed independently in each coordinate. This explicit description confirms that the concept of linear combination is fully compatible with the coordinate structure of $\mathbb{R}^{n}$. The global operation of combining vectors reduces to familiar arithmetic carried out entry by entry.

## Matrix–Vector interpretation

The relationship between linear combinations and [matrices](https://algebrica.org/matrices/) becomes especially clear when we look at matrix–vector multiplication more closely. Consider a matrix whose columns are the vectors $v_{1} , \ldots , v_{k}$:

$$A = \left(\right. \left|\right. & \left|\right. & & \left|\right. \\ v_{1} & v_{2} & \ldots & v_{k} \\ \left|\right. & \left|\right. & & \left|\right. \left.\right)$$

Now take a vector of scalars:

$$c = \left(\right. c_{1} \\ c_{2} \\ \vdots \\ c_{k} \left.\right)$$

When we compute the product $A c$ what happens is remarkably simple: each column of $A$ is multiplied by the corresponding entry of $c$, and the resulting vectors are added together. Writing this explicitly, we obtain:

$$A c = c_{1} v_{1} + c_{2} v_{2} + \hdots + c_{k} v_{k}$$

In other words, multiplying a matrix by a vector is nothing more than forming a linear combination of its columns. The entries of the vector $c$ play the role of coefficients that determine how strongly each column contributes to the result.

> Seen from this perspective, matrix multiplication is not just a computational rule involving rows and columns. It is a structured way of assembling vectors from simpler building blocks, and every matrix–vector product can be understood as a controlled linear combination of the columns of the matrix.

## Linear systems and solvability

Let us now return to one of the central objects of linear algebra: a [linear system](https://algebrica.org/systems-of-linear-equations/) written in matrix form:

$$A x = b$$

This equation represents a compact way of writing several linear [equations](https://algebrica.org/equations/) at once. However, once we interpret matrix–vector multiplication as a linear combination of columns, the meaning of the system becomes much clearer. Suppose the columns of $A$ are the vectors $v_{1} , \ldots , v_{k}$. Expanding the product $A x$ according to the definition of matrix multiplication, we obtain:

$$x_{1} v_{1} + x_{2} v_{2} + \hdots + x_{k} v_{k} = b$$

Seen in this way, solving the system does not primarily mean manipulating equations. It means searching for scalars $x_{1} , \ldots , x_{k}$ that combine the columns of $A$ to produce the vector $b$. The problem of solvability therefore acquires a geometric interpretation. The question is no longer only algebraic. It becomes: can the vector $b$ be assembled from the columns of $A$? In other words, does $b$ belong to the set of all linear combinations generated by those vectors?

- If such scalars exist, the system has at least one solution.
- If no such combination is possible, the system is inconsistent.

The structure of the solution set is thus determined entirely by how the vector $b$ relates to the space generated by the columns of $A$.

## Span

Once the notion of linear combination is in place, a natural question arises: given a finite collection of vectors, what is the totality of vectors that can be produced by scaling and summing them in all possible ways? The set of all linear combinations of $v_{1} , \ldots , v_{k}$ is called their span:

$$span \left(\right. v_{1} , \ldots , v_{k} \left.\right) = \sum_{i = 1}^{k} c_{i} v_{i} \mid c_{i} \in \mathbb{R}$$

In other words, the span consists of every vector that can be built from $v_{1} , \ldots , v_{k}$ using the operations of scalar multiplication and vector addition. It represents the entire region of $\mathbb{R}^{n}$ that becomes accessible once those vectors are taken as building blocks.

---

By construction, the span is closed under addition and scalar multiplication. If two vectors belong to the span, any linear combination of them also belongs to the span. For this reason, the span is not just a subset of $\mathbb{R}^{n}$, but a subspace of $\mathbb{R}^{n}$. From a geometric point of view we have:

- A single nonzero vector spans a line through the origin.
- Two vectors that are not collinear span a plane through the origin.
- Three vectors, provided they introduce independent directions, may span a three-dimensional subspace.

---

The geometric description above suggests that the span behaves like a flat region passing through the origin. This intuition can be made precise by verifying that the span satisfies the defining properties of a subspace of $\mathbb{R}^{n}$. First, the zero vector belongs to the span. Indeed, by choosing all coefficients equal to zero, we obtain:

$$0 = 0 v_{1} + 0 v_{2} + \hdots + 0 v_{k}$$

Hence:

$$0 \in span \left(\right. v_{1} , \ldots , v_{k} \left.\right)$$

Second, the span is closed under linear combinations. Let:

$$u = \sum_{i = 1}^{k} a_{i} v_{i} w = \sum_{i = 1}^{k} b_{i} v_{i}$$

be two arbitrary vectors in $span \left(\right. v_{1} , \ldots , v_{k} \left.\right)$, and let $\alpha , \beta \in \mathbb{R}$. Then:

$$\alpha u + \beta w & = \alpha \sum_{i = 1}^{k} a_{i} v_{i} + \beta \sum_{i = 1}^{k} b_{i} v_{i} \\ & = \sum_{i = 1}^{k} \left(\right. \alpha a_{i} + \beta b_{i} \left.\right) v_{i}$$

Since the coefficients $\alpha a_{i} + \beta b_{i}$ are real numbers, the resulting vector is again a linear combination of $v_{1} , \ldots , v_{k}$. Therefore:

$$\alpha u + \beta w \in span \left(\right. v_{1} , \ldots , v_{k} \left.\right)$$

These properties show that the span is not merely a subset of $\mathbb{R}^{n}$, but a subspace: it contains the zero vector and is closed under addition and scalar multiplication.

## Example

Let us now see how the concept of span works in practice. When we say that a vector belongs to the span of other vectors, we are claiming that it can be constructed as a linear combination of them. In concrete terms, this means that there must exist suitable scalar coefficients that, when applied to the given vectors and added together, reproduce the target vector. Testing whether a vector lies in a span therefore amounts to solving a [linear system](https://algebrica.org/systems-of-linear-equations/). We will make this idea explicit through a direct computation.

Consider the vectors in $\mathbb{R}^{3}$:

$$v_{1} = \left(\right. 1 2 1 \left.\right) v_{2} = \left(\right. 0 1 1 \left.\right)$$

We ask whether the vector:

$$b = \left(\right. 3 \\ 7 \\ 5 \left.\right)$$

belongs to $span \left(\right. v_{1} , v_{2} \left.\right)$. To answer this question, we must determine whether there exist scalars $c_{1} , c_{2} \in \mathbb{R}$ such that:

$$c_{1} v_{1} + c_{2} v_{2} = b$$

Writing the linear combination explicitly, we obtain:

$$c_{1} \left(\right. 1 \\ 2 \\ 1 \left.\right) + c_{2} \left(\right. 0 \\ 1 \\ 1 \left.\right) = \left(\right. 3 \\ 7 \\ 5 \left.\right)$$

Equating the components yields the system:

$$\left{\right. c_{1} = 3 \\ 2 c_{1} + c_{2} = 7 \\ c_{1} + c_{2} = 5$$

From the first equation we obtain $c_{1} = 3$. Substituting into the second equation gives:

$$2 \left(\right. 3 \left.\right) + c_{2} = 7 \rightarrow c_{2} = 1$$

However, checking the third equation:

$$3 + 1 = 4 \neq 5$$

The system is inconsistent. Therefore, no scalars $c_{1} , c_{2}$ produce the vector $b$, and we conclude that $b \notin span \left(\right. v_{1} , v_{2} \left.\right)$.

---

Now consider instead:

$$b = \left(\right. 3 \\ 7 \\ 4 \left.\right)$$

Repeating the same computation, we obtain:

$$\left{\right. c_{1} = 3 \\ 2 c_{1} + c_{2} = 7 \\ c_{1} + c_{2} = 4$$

Substituting $c_{1} = 3$ into the second equation gives $c_{2} = 1$, and the third equation becomes:

$$3 + 1 = 4$$

which is satisfied. Hence:

$$b = 3 v_{1} + 1 v_{2}$$

and therefore $b \in span \left(\right. v_{1} , v_{2} \left.\right)$

This simple example shows concretely that belonging to a span is not an abstract property but a solvability condition: a vector lies in the span of given vectors if and only if a corresponding linear system admits a solution.

## Uniqueness of representation

Suppose that a vector $b$ can be written as a linear combination of the vectors $v_{1} , \ldots , v_{k}$, namely:

$$b = c_{1} v_{1} + \hdots + c_{k} v_{k}$$

At this point, a natural question arises. Once such a representation has been found, are the coefficients $c_{1} , \ldots , c_{k}$ uniquely determined? Or could there exist different choices of scalars producing the same vector $b$? To investigate this, imagine that two distinct families of scalars lead to the same vector. Subtracting the two representations would produce an expression of the form

$$c_{1} v_{1} + \hdots + c_{k} v_{k} = 0$$

where not all the coefficients are zero. The existence of such a relation means that the zero vector itself can be obtained as a nontrivial linear combination of the vectors $v_{1} , \ldots , v_{k}$ This situation has an important structural consequence. If a nontrivial combination of the vectors yields the zero vector, then at least one of the vectors can be expressed as a linear combination of the others. In that case, the original representation of $b$ need not be unique: different choices of coefficients may lead to the same vector.

> The question of uniqueness is therefore connected with the existence of nontrivial linear relations among the vectors. When no such relation exists, that is, when the only way to obtain the zero vector is by setting all coefficients to zero, the representation of any vector in the span is necessarily unique. This property defines what it means for a collection of vectors to be linearly independent, a concept that will be examined in detail in the dedicated entry.

## General vector spaces

The definition of linear combination given above is stated for [vectors](https://algebrica.org/vectors/) in $\mathbb{R}^{n}$, but the concept extends without modification to any vector space over a field. Let $V$ be a vector space over a field $\mathbb{F}$, and let $v_{1} , v_{2} , \ldots , v_{k} \in V$. A linear combination of these vectors is any element of $V$ of the form:

$$c_{1} v_{1} + c_{2} v_{2} + \hdots + c_{k} v_{k}$$

where $c_{1} , c_{2} , \ldots , c_{k} \in \mathbb{F}$. The field $\mathbb{F}$ may be taken to be $\mathbb{R}$ or $\mathbb{C}$, and the vector space $V$ may be a space of polynomials, of matrices, or of continuous functions, among many others. In each of these settings, the notions of span and linear independence carry over directly, and the structural results of linear algebra remain valid in full generality.
