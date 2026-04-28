---
layout: chapter
title: "Vectors"
chapter: "Vectors and Matrices"
chapter_order: 10
section_order: 1
permalink: /materi-algebrica/vectors-and-matrices/vectors/
---

vector spaceorthogonalityunit vectornormalgebraic propertiescross productdot productsubtractionscalar multiplicationadditiondimensioncoordinate formbasiscomponentsgeometric viewpropertiesoperationsrepresentation

## Geometric representation

A vector is a quantity characterised by both a magnitude and a direction, in contrast to a scalar, which is described by magnitude alone. This distinction arises naturally in geometry and physics, where quantities such as displacement, [velocity](https://algebrica.org/velocity), and force require directional information that a single real number cannot encode. The formal treatment developed here is algebraic and applies to vectors in the Euclidean spaces $\mathbb{R}^{2}$ and $\mathbb{R}^{3}$, which are sufficient for most basic applications in calculus, geometry, and mechanics. A vector in the plane or in three-dimensional space is represented as a directed line segment, that is, a segment with a specified initial point and a terminal point. The direction of the segment indicates the orientation of the vector, and its length represents the magnitude.

![Vector.](https://algebrica.org/wp-content/uploads/resources/images/vector-1.png "Vector.")

Two directed segments that have the same length and the same direction are considered to represent the same vector, regardless of their position in space. This equivalence is the basis for the notion of a free vector, which is entirely characterised by its direction and magnitude, independently of where it is drawn.

![Vectors.](https://algebrica.org/wp-content/uploads/resources/images/vector-2.png "Vectors.")

It is standard to denote vectors using boldface letters such as $\mathbf{v}$, or alternatively with an arrow notation $\overset{\rightarrow}{v}$. The zero vector, denoted $0$, has zero magnitude and no defined direction; it plays the role of the additive identity in vector arithmetic.

## Components and coordinate representation

In a Cartesian coordinate system, every vector in $\mathbb{R}^{n}$ can be expressed in terms of its components along the coordinate axes. A vector $\mathbf{v}$ in $\mathbb{R}^{2}$ is written as an ordered pair:

$$\mathbf{v} = \left(\right. v_{1} , v_{2} \left.\right) \in \mathbb{R}^{2}$$

![Vector components in ℝ².](https://algebrica.org/wp-content/uploads/resources/images/vector-3.png "Vector components in ℝ².")

A vector in $\mathbb{R}^{3}$ is written as an ordered triple.

$$\mathbf{v} = \left(\right. v_{1} , v_{2} , v_{3} \left.\right) \in \mathbb{R}^{3}$$

![Vector components in ℝ³.](https://algebrica.org/wp-content/uploads/resources/images/vector-4.png "Vector components in ℝ³.")

The [real numbers](https://algebrica.org/properties-of-real-numbers/) $v_{1} , v_{2} , v_{3}$ are called the components of $\mathbf{v}$ with respect to the chosen coordinate system. The standard basis vectors in $\mathbb{R}^{3}$ are defined as follows.

$$\mathbf{i} = \left(\right. 1 , 0 , 0 \left.\right) \mathbf{j} = \left(\right. 0 , 1 , 0 \left.\right) \mathbf{k} = \left(\right. 0 , 0 , 1 \left.\right)$$

Every vector in $\mathbb{R}^{3}$ can be expressed as a [linear combination](https://algebrica.org/linear-combinations/) of these basis vectors.

$$\mathbf{v} = v_{1} \mathbf{i} + v_{2} \mathbf{j} + v_{3} \mathbf{k}$$
In this expression, each scalar coefficient selects the contribution of the corresponding basis vector: $v_{1}$ scales $\mathbf{i}$ along the $x$-axis, $v_{2}$ scales $\mathbf{j}$ along the $y$-axis, and $v_{3}$ scales $\mathbf{k}$ along the $z$-axis. The sum of these three scaled basis vectors reconstructs $\mathbf{v}$ exactly. For example, the vector $\left(\right. 3 , - 1 , 2 \left.\right)$ is written as $3 \mathbf{i} - \mathbf{j} + 2 \mathbf{k}$, meaning a displacement of three units in the $x$-direction, one unit in the negative $y$-direction, and two units in the $z$-direction. This representation makes explicit the decomposition of $\mathbf{v}$ into contributions along each coordinate direction.

## Vector operations

The basic algebraic operations on vectors are addition, subtraction, and scalar multiplication. These operations are defined component-wise and admit clear geometric interpretations. Given two vectors $\mathbf{u} = \left(\right. u_{1} , u_{2} , u_{3} \left.\right)$ and $\mathbf{v} = \left(\right. v_{1} , v_{2} , v_{3} \left.\right)$ in $\mathbb{R}^{3}$, their sum is defined as follows.

$$\mathbf{u} + \mathbf{v} = \left(\right. u_{1} + v_{1} , u_{2} + v_{2} , u_{3} + v_{3} \left.\right)$$

Geometrically, vector addition corresponds to placing the initial point of $\mathbf{v}$ at the terminal point of $\mathbf{u}$. The resulting vector connects the initial point of $\mathbf{u}$ to the terminal point of $\mathbf{v}$. This construction is known as the triangle rule.

![](https://algebrica.org/wp-content/uploads/resources/images/vector-5-1.png "Triangle rule for vector addition.")

An equivalent formulation, the parallelogram rule, places both vectors at a common initial point and identifies their sum with the diagonal of the parallelogram they determine.

![Parallelogram rule for vectors.](https://algebrica.org/wp-content/uploads/resources/images/vector-6.png "Parallelogram rule for vectors.")

Scalar multiplication by a real number $\lambda \in \mathbb{R}$ scales each component uniformly.

$$\lambda \mathbf{v} = \left(\right. \lambda v_{1} , \lambda v_{2} , \lambda v_{3} \left.\right)$$

When $\lambda > 0$, the resulting vector has the same direction as $\mathbf{v}$ and magnitude scaled by $\lambda$. When $\lambda < 0$, the direction is reversed. When $\lambda = 0$, the result is the zero vector. Subtraction is defined by combining the two preceding operations: $\mathbf{u} - \mathbf{v} = \mathbf{u} + \left(\right. - 1 \left.\right) \mathbf{v}$, which yields $\left(\right. u_{1} - v_{1} , u_{2} - v_{2} , u_{3} - v_{3} \left.\right)$.

## Algebraic properties

The operations of vector addition and scalar multiplication satisfy a set of fundamental properties that hold for all vectors $\mathbf{u} , \mathbf{v} , \mathbf{w} \in \mathbb{R}^{n}$ and all scalars $\lambda , \mu \in \mathbb{R}$.

- Addition is commutative, meaning that $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$, and associative, so that $\left(\right. \mathbf{u} + \mathbf{v} \left.\right) + \mathbf{w} = \mathbf{u} + \left(\right. \mathbf{v} + \mathbf{w} \left.\right) .$
- The zero vector $0$ acts as the additive identity, satisfying $\mathbf{v} + 0 = \mathbf{v}$ for every $\mathbf{v}$, and each vector $\mathbf{v}$ has an additive inverse $- \mathbf{v} = \left(\right. - 1 \left.\right) \mathbf{v}$ such that $\mathbf{v} + \left(\right. - \mathbf{v} \left.\right) = 0 .$
- Scalar multiplication distributes over vector addition according to $\lambda \left(\right. \mathbf{u} + \mathbf{v} \left.\right) = \lambda \mathbf{u} + \lambda \mathbf{v}$, and over scalar addition according to $\left(\right. \lambda + \mu \left.\right) \mathbf{v} = \lambda \mathbf{v} + \mu \mathbf{v}$. Scalar multiplication is compatible with scalar product: $\left(\right. \lambda \mu \left.\right) \mathbf{v} = \lambda \left(\right. \mu \mathbf{v} \left.\right)$, and the scalar $1$ acts as the multiplicative identity, with $1 \cdot \mathbf{v} = \mathbf{v} .$

> These properties are not incidental: together they constitute the defining axioms of a vector space. The set $\mathbb{R}^{n}$ equipped with these two operations forms a vector space over the field $\mathbb{R}$, a structure that will be examined in greater generality in the entry on vector spaces.

## Norm of a vector

The norm, or magnitude, of a vector $\mathbf{v} = \left(\right. v_{1} , v_{2} , v_{3} \left.\right)$ is a non-negative real number that measures its length. It is defined by the following expression:

$$\parallel \mathbf{v} \parallel = \sqrt{v_{1}^{2} + v_{2}^{2} + v_{3}^{2}}$$

This formula is a direct consequence of the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/) applied iteratively along the coordinate axes. In $\mathbb{R}^{2}$, the analogous formula is:

$$\parallel \mathbf{v} \parallel = \sqrt{v_{1}^{2} + v_{2}^{2}}$$

As an example, consider the vector $\mathbf{v} = \left(\right. 2 , - 3 , 6 \left.\right)$ in $\mathbb{R}^{3}$. Its norm is computed by summing the squares of its components and taking the square root:

$$\parallel \mathbf{v} \parallel & = \sqrt{2^{2} + \left(\right. - 3 \left.\right)^{2} + 6^{2}} \\ & = \sqrt{4 + 9 + 36} \\ & = \sqrt{49} \\ & = 7$$

Each term under the radical corresponds to the squared contribution of one coordinate direction, and the result confirms that $\mathbf{v}$ has length $7$. A vector whose norm is equal to one is called a unit vector. Given any non-zero vector $\mathbf{v}$, it is always possible to construct a unit vector pointing in the same direction by dividing $\mathbf{v}$ by its norm. This operation is called normalisation.

$$\hat{\mathbf{v}} = \frac{\mathbf{v}}{\parallel \mathbf{v} \parallel}$$

The resulting vector $\hat{\mathbf{v}}$ satisfies $\parallel \hat{\mathbf{v}} \parallel = 1$ by construction.

## Dot product

The dot product, also called the scalar product or inner product, is a binary operation that takes two vectors and returns a real number. For $\mathbf{u} , \mathbf{v} \in \mathbb{R}^{n}$, it is defined algebraically as the sum of the products of corresponding components.

$$\mathbf{u} \cdot \mathbf{v} = \sum_{i = 1}^{n} u_{i} v_{i} = u_{1} v_{1} + u_{2} v_{2} + \hdots + u_{n} v_{n}$$

The dot product admits an equivalent geometric formulation in terms of the angle $\theta$ between the two vectors.

$$\mathbf{u} \cdot \mathbf{v} = \parallel \mathbf{u} \parallel \parallel \mathbf{v} \parallel cos ⁡ \theta$$

The factor $cos ⁡ \theta$ connects the dot product to the [cosine](https://algebrica.org/sine-and-cosine/) of the angle between the two vectors, and it is precisely this relationship that makes the dot product a powerful tool for measuring alignment and orthogonality. When $\mathbf{u} \cdot \mathbf{v} = 0$ and neither vector is zero, it follows that $cos ⁡ \theta = 0$, hence $\theta = \pi / 2$. Two vectors satisfying this condition are said to be orthogonal. Conversely, when the vectors are parallel, $\theta = 0$ or $\theta = \pi$, and the dot product equals $\pm \parallel \mathbf{u} \parallel , \parallel \mathbf{v} \parallel$. The dot product also provides a direct expression for the norm: $\left|\right. \mathbf{v} \left|\right.^{2} = \mathbf{v} \cdot \mathbf{v}$. As an application, consider $\mathbf{u} = \left(\right. 1 , 2 , - 1 \left.\right)$ and $\mathbf{v} = \left(\right. 3 , 0 , 3 \left.\right)$. The dot product is computed as follows.

$$\mathbf{u} \cdot \mathbf{v} & = \left(\right. 1 \left.\right) \left(\right. 3 \left.\right) + \left(\right. 2 \left.\right) \left(\right. 0 \left.\right) + \left(\right. - 1 \left.\right) \left(\right. 3 \left.\right) \\ & = 3 + 0 - 3 \\ & = 0$$

Since the result is zero, the two vectors are orthogonal. This conclusion can be verified geometrically by observing that neither vector is a scalar multiple of the other and their components satisfy the orthogonality condition exactly.

## Cross product

The cross product is an operation defined for vectors in $\mathbb{R}^{3}$ that takes two vectors and returns a third vector. Unlike the dot product, the result is not a scalar but a vector, and for this reason the operation is also called the vector product. Given $\mathbf{u} = \left(\right. u_{1} , u_{2} , u_{3} \left.\right)$ and $\mathbf{v} = \left(\right. v_{1} , v_{2} , v_{3} \left.\right)$, their cross product is defined by the following formula, expressed as the determinant of a [matrix](https://algebrica.org/matrices/).

$$\mathbf{u} \times \mathbf{v} = \left|\right. \mathbf{i} & \mathbf{j} & \mathbf{k} \\ u_{1} & u_{2} & u_{3} \\ v_{1} & v_{2} & v_{3} \left|\right.$$

Expanding along the first row yields the explicit component form.

$$\mathbf{u} \times \mathbf{v} = \left(\right. u_{2} v_{3} - u_{3} v_{2} , u_{3} v_{1} - u_{1} v_{3} , u_{1} v_{2} - u_{2} v_{1} \left.\right)$$

The resulting vector is orthogonal to both $\mathbf{u}$ and $\mathbf{v}$, as can be verified by computing the dot products $\left(\right. \mathbf{u} \times \mathbf{v} \left.\right) \cdot \mathbf{u}$ and $\left(\right. \mathbf{u} \times \mathbf{v} \left.\right) \cdot \mathbf{v}$, both of which equal zero. The direction of $\mathbf{u} \times \mathbf{v}$ is determined by the right-hand rule: if the fingers of the right hand curl from $\mathbf{u}$ toward $\mathbf{v}$, the thumb points in the direction of $\mathbf{u} \times \mathbf{v}$. The magnitude of the cross product has a natural geometric interpretation:
$$\parallel \mathbf{u} \times \mathbf{v} \parallel = \parallel \mathbf{u} \parallel \parallel \mathbf{v} \parallel sin ⁡ \theta$$

This quantity equals the area of the parallelogram spanned by $\mathbf{u}$ and $\mathbf{v}$. In particular, $\mathbf{u} \times \mathbf{v} = 0$ if and only if $sin ⁡ \theta = 0$, that is, if and only if the vectors are parallel. The cross product is anti-commutative: $\mathbf{v} \times \mathbf{u} = - \left(\right. \mathbf{u} \times \mathbf{v} \left.\right)$, which reflects the reversal of orientation when the order of the operands is exchanged.

---

As a concrete example, consider $\mathbf{u} = \left(\right. 1 , 2 , 3 \left.\right)$ and $\mathbf{v} = \left(\right. 4 , 5 , 6 \left.\right)$. Applying the component formula yields the following.
$$\mathbf{u} \times \mathbf{v} & = \left(\right. u_{2} v_{3} - u_{3} v_{2} , u_{3} v_{1} - u_{1} v_{3} , u_{1} v_{2} - u_{2} v_{1} \left.\right) \\ & = \left(\right. 2 \cdot 6 - 3 \cdot 5 , 3 \cdot 4 - 1 \cdot 6 , 1 \cdot 5 - 2 \cdot 4 \left.\right) \\ & = \left(\right. 12 - 15 , 12 - 6 , 5 - 8 \left.\right) \\ & = \left(\right. - 3 , 6 , - 3 \left.\right)$$
One can verify that the result is orthogonal to both $\mathbf{u}$ and $\mathbf{v}$ by computing the two dot products. For the first:
$$\left(\right. - 3 , 6 , - 3 \left.\right) \cdot \left(\right. 1 , 2 , 3 \left.\right) = - 3 + 12 - 9 = 0$$
and for the second:

$$\left(\right. - 3 , 6 , - 3 \left.\right) \cdot \left(\right. 4 , 5 , 6 \left.\right) = - 12 + 30 - 18 = 0$$

Both results are zero, confirming that $\mathbf{u} \times \mathbf{v}$ is perpendicular to both factors.
