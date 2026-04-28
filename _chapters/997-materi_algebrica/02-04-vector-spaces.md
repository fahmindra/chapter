---
layout: chapter
title: "Vector Spaces"
chapter: "Algebraic Structures"
chapter_order: 2
section_order: 4
permalink: /materi-algebrica/algebraic-structures/vector-spaces/
---

## Definition

A vector space is an algebraic structure that formalises the idea of quantities that can be scaled and [combined linearly](https://algebrica.org/linear-combinations/). The concept arises wherever one encounters objects that can be added together and multiplied by numbers in a coherent way: geometric arrows in the plane, [polynomials](https://algebrica.org/polynomials/) with real coefficients, sequences of [real numbers](https://algebrica.org/properties-of-real-numbers/), and [continuous functions](https://algebrica.org/continuous-functions/) on an interval all share this common pattern.

Unlike a [group](https://algebrica.org/groups/) or a [ring](https://algebrica.org/rings/), which are defined on a single set, a vector space involves two distinct sets: a [field](https://algebrica.org/fields/) $F$, whose elements are called scalars, and a set $V$, whose elements are called [vectors](https://algebrica.org/vectors/). A vector space over $F$ is a set $V$ together with two operations, vector addition $+ : V \times V \rightarrow V$ and scalar multiplication $\cdot : F \times V \rightarrow V$, satisfying the following axioms:

- $\left(\right. V , + \left.\right)$ is an abelian group. In particular, there exists a zero vector $0 \in V$ such that $\mathbf{v} + 0 = \mathbf{v}$ for all $\mathbf{v} \in V$, and every vector $\mathbf{v}$ has an additive inverse $- \mathbf{v}$.
- Compatibility with field multiplication: for all $\alpha , \beta \in F$ and $\mathbf{v} \in V$, one has $\alpha \cdot \left(\right. \beta \cdot \mathbf{v} \left.\right) = \left(\right. \alpha \beta \left.\right) \cdot \mathbf{v}$.
- Identity element of scalar multiplication: for all $\mathbf{v} \in V$, the multiplicative identity $1 \in F$ satisfies $1 \cdot \mathbf{v} = \mathbf{v}$.
- Distributivity of scalar multiplication over vector addition: for all $\alpha \in F$ and $\mathbf{u} , \mathbf{v} \in V$, one has $\alpha \cdot \left(\right. \mathbf{u} + \mathbf{v} \left.\right) = \alpha \cdot \mathbf{u} + \alpha \cdot \mathbf{v}$.
- Distributivity of scalar multiplication over field addition: for all $\alpha , \beta \in F$ and $\mathbf{v} \in V$, one has $\left(\right. \alpha + \beta \left.\right) \cdot \mathbf{v} = \alpha \cdot \mathbf{v} + \beta \cdot \mathbf{v}$.

> The field $F$ over which $V$ is defined is called the scalar field of $V$. In most applications encountered at the undergraduate level, $F$ is either $\mathbb{R}$ or $\mathbb{C}$, and one speaks of a real vector space or a complex vector space accordingly.

## Properties

Several elementary consequences follow directly from the axioms. For any scalar $\alpha \in F$ and any vector $\mathbf{v} \in V$, multiplication by zero satisfies $0 \cdot \mathbf{v} = 0$. To see this, one writes $0 \cdot \mathbf{v} = \left(\right. 0 + 0 \left.\right) \cdot \mathbf{v} = 0 \cdot \mathbf{v} + 0 \cdot \mathbf{v}$ and cancels $0 \cdot \mathbf{v}$ from both sides using the group structure of $\left(\right. V , + \left.\right)$. Similarly, for any $\mathbf{v} \in V$ one has $\alpha \cdot 0 = 0$ and $\left(\right. - 1 \left.\right) \cdot \mathbf{v} = - \mathbf{v}$.

If $\alpha \cdot \mathbf{v} = 0$, then either $\alpha = 0$ or $\mathbf{v} = 0$. This is a direct consequence of the invertibility of nonzero scalars: if $\alpha \neq 0$, then $\mathbf{v} = 1 \cdot \mathbf{v} = \left(\right. \alpha^{- 1} \alpha \left.\right) \cdot \mathbf{v} = \alpha^{- 1} \cdot \left(\right. \alpha \cdot \mathbf{v} \left.\right) = \alpha^{- 1} \cdot 0 = 0$. This property is the vector space analogue of the absence of zero divisors in a field, and it plays a central role in the theory of linear independence.

## Algebraic hierarchy

Vector spaces occupy a position at the top of the standard hierarchy of algebraic structures, depending essentially on the presence of a field of scalars.

A [group](https://algebrica.org/groups/) consists of a set with a single operation admitting inverses. A [ring](https://algebrica.org/rings/) introduces a second operation that need not be invertible. A [field](https://algebrica.org/fields/) requires both operations to be fully invertible on nonzero elements. A vector space then takes a field as a given and builds a new structure on top of it, one in which the field acts on a separate set of vectors by scaling. The three structures form a chain of increasing rigidity:

- A group carries one operation with inverses.
- A ring carries two operations, with inverses guaranteed only for addition.
- A field carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> A vector space is not itself a further step in this chain but rather a structure that presupposes a field. Every vector space over $\mathbb{R}$ or $\mathbb{C}$ depends on the field axioms being in force for its scalar multiplication to be well-defined.

## Examples

The set $\mathbb{R}^{n}$ of all ordered $n$-tuples of real numbers is a vector space over $\mathbb{R}$ under componentwise addition and scalar multiplication. For $n = 2$, addition is defined by $\left(\right. a_{1} , a_{2} \left.\right) + \left(\right. b_{1} , b_{2} \left.\right) = \left(\right. a_{1} + b_{1} , a_{2} + b_{2} \left.\right)$ and scalar multiplication by $\alpha \cdot \left(\right. a_{1} , a_{2} \left.\right) = \left(\right. \alpha a_{1} , \alpha a_{2} \left.\right)$. The zero vector is $\left(\right. 0 , 0 \left.\right)$. This is the prototype of a finite-dimensional real vector space, and it provides the geometric intuition underlying the general theory.

The set $\mathbb{C}^{n}$ of all ordered $n$-tuples of complex numbers is a vector space over $\mathbb{C}$ under the analogous operations. It can also be regarded as a vector space over $\mathbb{R}$, though in that case its dimension doubles: $\mathbb{C}^{n}$ as a real vector space has dimension $2 n$.

---

The set $\mathbb{R} \left[\right. x \left]\right._{\leq n}$ of all [polynomials](https://algebrica.org/polynomials/) with real coefficients of degree at most $n$ is a vector space over $\mathbb{R}$ under the usual addition of polynomials and multiplication of a polynomial by a real constant. The zero vector is the zero polynomial. A natural basis for this space is $1 , x , x^{2} , \ldots , x^{n}$, which contains $n + 1$ elements, so the dimension of this space is $n + 1$.

The set $\mathcal{C} \left(\right. \left[\right. a , b \left]\right. \left.\right)$ of all continuous real-valued functions on a closed interval $\left[\right. a , b \left]\right.$ is a vector space over $\mathbb{R}$ under pointwise addition and scalar multiplication: $\left(\right. f + g \left.\right) \left(\right. x \left.\right) = f \left(\right. x \left.\right) + g \left(\right. x \left.\right)$ and $\left(\right. \alpha f \left.\right) \left(\right. x \left.\right) = \alpha f \left(\right. x \left.\right)$. This space is infinite-dimensional, since the polynomials of all degrees form a linearly independent subset with no finite spanning set.

## Subspaces

A nonempty subset $W \subseteq V$ is called a subspace of $V$ if $W$ is itself a vector space over $F$ under the operations inherited from $V$. Rather than verifying all axioms separately, it suffices to check two conditions: for all $\mathbf{u} , \mathbf{v} \in W$ and all $\alpha \in F$, one requires $\mathbf{u} + \mathbf{v} \in W$ and $\alpha \cdot \mathbf{v} \in W$. These two conditions together are called closure under linear combinations. The zero vector $0$ must belong to every subspace, since setting $\alpha = 0$ gives $0 \cdot \mathbf{v} = 0 \in W$.

As an example, the set $W = \left(\right. x , y \left.\right) \in \mathbb{R}^{2} : y = 2 x$ is a subspace of $\mathbb{R}^{2}$. For any two vectors $\left(\right. x_{1} , 2 x_{1} \left.\right)$ and $\left(\right. x_{2} , 2 x_{2} \left.\right)$ in $W$, their sum $\left(\right. x_{1} + x_{2} , 2 x_{1} + 2 x_{2} \left.\right) = \left(\right. x_{1} + x_{2} , 2 \left(\right. x_{1} + x_{2} \left.\right) \left.\right)$ belongs to $W$, and for any scalar $\alpha \in \mathbb{R}$ the vector $\alpha \left(\right. x_{1} , 2 x_{1} \left.\right) = \left(\right. \alpha x_{1} , 2 \alpha x_{1} \left.\right)$ also belongs to $W$. Both conditions are satisfied, so $W$ is a subspace of $\mathbb{R}^{2}$. Geometrically, $W$ is the line through the origin with slope $2$.

![](https://algebrica.org/wp-content/uploads/resources/images/subspace.png)

> The diagram illustrates the two closure conditions on the subspace $W = \left{\right. \left(\right. x , y \left.\right) \in \mathbb{R}^{2} : y = 2 x \left.\right}$. Any vector in $W$ lies on the line through the origin with slope $2$. Adding two such vectors or multiplying one by a scalar always produces a vector that remains on the same line, confirming that $W$ is closed under both operations.

## Basis and dimension

A set of vectors $\left{\right. \mathbf{v}_{1} , \mathbf{v}_{2} , \ldots , \mathbf{v}_{n} \left.\right}$ in $V$ is called linearly independent if the only solution to the equation

$$\alpha_{1} \mathbf{v}_{1} + \alpha_{2} \mathbf{v}_{2} + \hdots + \alpha_{n} \mathbf{v}_{n} = 0$$

is $\alpha_{1} = \alpha_{2} = \hdots = \alpha_{n} = 0$. A set of vectors that is not linearly independent is called linearly dependent, meaning that at least one vector in the set can be expressed as a [linear combination](https://algebrica.org/linear-combinations/) of the others. A basis of $V$ is a linearly independent set of vectors that spans $V$, meaning every vector in $V$ can be written as a linear combination of the basis vectors. The representation of any vector in terms of a given basis is unique. If
$$\mathbf{v} = \alpha_{1} \mathbf{v}_{1} + \hdots + \alpha_{n} \mathbf{v}_{n} = \beta_{1} \mathbf{v}_{1} + \hdots + \beta_{n} \mathbf{v}_{n}$$

then subtracting yields:
$$\left(\right. \alpha_{1} - \beta_{1} \left.\right) \mathbf{v}_{1} + \hdots + \left(\right. \alpha_{n} - \beta_{n} \left.\right) \mathbf{v}_{n} = 0$$

and linear independence forces $\alpha_{k} = \beta_{k}$ for all $k$.

---

One of the fundamental theorems of linear algebra states that any two bases of the same vector space contain the same number of elements. The argument rests on the observation that if a set of $m$ vectors spans $V$ and a set of $n$ vectors is linearly independent in $V$, then necessarily $n \leq m$. Applying this inequality twice, once in each direction, to any two bases forces their cardinalities to be equal. This common cardinality is called the dimension of $V$ and is denoted $dim ⁡ V$.

The standard basis of $\mathbb{R}^{n}$ consists of the $n$ vectors $\mathbf{e}_{1} , \mathbf{e}_{2} , \ldots , \mathbf{e}_{n}$, where $\mathbf{e}_{k}$ has a $1$ in position $k$ and $0$ everywhere else. For example, in $\mathbb{R}^{3}$ the standard basis is the following:

$$\mathbf{e}_{1} = \left(\right. 1 , 0 , 0 \left.\right) , \mathbf{e}_{2} = \left(\right. 0 , 1 , 0 \left.\right) , \mathbf{e}_{3} = \left(\right. 0 , 0 , 1 \left.\right)$$

Every [vector](https://algebrica.org/vectors/) $\left(\right. a , b , c \left.\right) \in \mathbb{R}^{3}$ can be written uniquely as $a \mathbf{e}_{1} + b \mathbf{e}_{2} + c \mathbf{e}_{3}$, confirming that these three vectors form a basis and that $dim ⁡ \mathbb{R}^{3} = 3$.

## Linear maps

A linear map, or linear transformation, is a function $\varphi : V \rightarrow W$ between two vector spaces over the same field $F$ that preserves the vector space structure. Explicitly, $\varphi$ is linear if for all $\mathbf{u} , \mathbf{v} \in V$ and all $\alpha \in F$ the following two conditions hold:

$$\varphi \left(\right. \mathbf{u} + \mathbf{v} \left.\right) = \varphi \left(\right. \mathbf{u} \left.\right) + \varphi \left(\right. \mathbf{v} \left.\right)$$
$$\varphi \left(\right. \alpha \cdot \mathbf{v} \left.\right) = \alpha \cdot \varphi \left(\right. \mathbf{v} \left.\right)$$

These two conditions can be combined into the single requirement that $\varphi \left(\right. \alpha \mathbf{u} + \beta \mathbf{v} \left.\right) = \alpha \varphi \left(\right. \mathbf{u} \left.\right) + \beta \varphi \left(\right. \mathbf{v} \left.\right)$ for all $\alpha , \beta \in F$ and $\mathbf{u} , \mathbf{v} \in V$. A linear map that is bijective is called a linear isomorphism, and two vector spaces are isomorphic if a linear isomorphism between them exists. A fundamental result states that every $n$-dimensional vector space over $F$ is isomorphic to $F^{n} ,$ so finite-dimensional vector spaces are completely classified by their dimension and their scalar field.

The kernel and image of a linear map $\varphi : V \rightarrow W$ are defined as follows:

$$ker ⁡ \left(\right. \varphi \left.\right) = \left{\right. \mathbf{v} \in V : \varphi \left(\right. \mathbf{v} \left.\right) = 0 \left.\right}$$
$$im \left(\right. \varphi \left.\right) = \left{\right. \varphi \left(\right. \mathbf{v} \left.\right) : \mathbf{v} \in V \left.\right}$$

Both $ker ⁡ \left(\right. \varphi \left.\right)$ and $im \left(\right. \varphi \left.\right)$ are subspaces of $V$ and $W$ respectively. The dimension theorem, also known as the rank-nullity theorem, states that for any linear map between finite-dimensional spaces the following identity holds:

$$dim ⁡ V = dim ⁡ ker ⁡ \left(\right. \varphi \left.\right) + dim ⁡ im \left(\right. \varphi \left.\right)$$

The dimension of $im \left(\right. \varphi \left.\right)$ is called the rank of $\varphi$ and the dimension of $ker ⁡ \left(\right. \varphi \left.\right)$ is called its nullity. The rank-nullity theorem is one of the central results of linear algebra and underlies the theory of [systems of linear equations](https://algebrica.org/systems-of-linear-equations/), the analysis of [matrices](https://algebrica.org/matrices/), and the classification of linear maps between finite-dimensional spaces.

## Example

Consider the linear map $\varphi : \mathbb{R}^{3} \rightarrow \mathbb{R}^{2}$ defined by the following assignment:

$$\varphi \left(\right. x , y , z \left.\right) = \left(\right. x + y , y + z \left.\right)$$

To verify linearity, one checks that:

$$\varphi \left(\right. \mathbf{u} + \mathbf{v} \left.\right) = \varphi \left(\right. \mathbf{u} \left.\right) + \varphi \left(\right. \mathbf{v} \left.\right)$$
$$\varphi \left(\right. \alpha \mathbf{v} \left.\right) = \alpha \varphi \left(\right. \mathbf{v} \left.\right)$$

hold for all vectors and scalars, which follows immediately from the linearity of addition and scalar multiplication in $\mathbb{R}^{3}$. The kernel consists of all vectors $\left(\right. x , y , z \left.\right)$ satisfying $x + y = 0$ and $y + z = 0$, that is, $x = - y$ and $z = - y$. Every element of $ker ⁡ \left(\right. \varphi \left.\right)$ therefore has the form:

$$\left(\right. - y , y , - y \left.\right) = y \left(\right. - 1 , 1 , - 1 \left.\right)$$

for some $y \in \mathbb{R}$, so the kernel is the one-dimensional subspace spanned by $\left(\right. - 1 , 1 , - 1 \left.\right)$. The image is all of $\mathbb{R}^{2}$, since for any $\left(\right. a , b \left.\right) \in \mathbb{R}^{2}$ the vector $\left(\right. a , 0 , b \left.\right)$ satisfies $\varphi \left(\right. a , 0 , b \left.\right) = \left(\right. a , b \left.\right)$, which shows that $\varphi$ is surjective and thus $dim ⁡ im \left(\right. \varphi \left.\right) = 2$. The rank-nullity theorem is verified:

$$dim ⁡ \mathbb{R}^{3} = dim ⁡ ker ⁡ \left(\right. \varphi \left.\right) + dim ⁡ im \left(\right. \varphi \left.\right) = 1 + 2 = 3$$

The solution to this example is therefore that $ker ⁡ \left(\right. \varphi \left.\right)$ is the line through the origin in direction $\left(\right. - 1 , 1 , - 1 \left.\right)$ and $im \left(\right. \varphi \left.\right) = \mathbb{R}^{2}$.

kernel and imagelinear mapsdimensionbasislinear combinationssubspacesconsistencyclosurelinearity rulesno zero divisorsadditive inversescalar zerozero multiplicationscalar fieldzero vectorscalar multiplicationvector additionvectors and scalarsdefinitiontheorypropertiesstructure
