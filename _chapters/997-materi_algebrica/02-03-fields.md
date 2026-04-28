---
layout: chapter
title: "Fields"
chapter: "Algebraic Structures"
chapter_order: 2
section_order: 3
permalink: /materi-algebrica/algebraic-structures/fields/
---

## Definition

A field is an algebraic structure in which the operations of addition and multiplication are both fully invertible, subject to the sole exception that division by zero is excluded. The concept arises when one observes that certain number systems, such as the rational numbers, the [real numbers](https://algebrica.org/properties-of-real-numbers/), and the [complex numbers](https://algebrica.org/complex-numbers-introduction/), allow not only addition and subtraction but also multiplication and division by any nonzero element, with all the expected algebraic rules in force.

Formally, a field is a set $F$ together with two binary operations $+$ and $\cdot$ satisfying the following axioms:

- $\left(\right. F , + \left.\right)$ is an abelian group. The additive identity is denoted $0$, and the additive inverse of an element $a \in F$ is denoted $- a .$
- $\left(\right. F \backslash \left{\right. 0 \left.\right} , \cdot \left.\right)$ is an abelian group. The multiplicative identity is denoted $1$, and the multiplicative inverse of a nonzero element $a$ is denoted $a^{- 1} .$
- Multiplication distributes over addition: for all $a , b , c \in F$, one has $a \cdot \left(\right. b + c \left.\right) = a \cdot b + a \cdot c$.

> The requirement that $0 \neq 1$ is included implicitly by excluding $0$ from the multiplicative group, and it ensures that the trivial set $\left{\right. 0 \left.\right}$ does not qualify as a field. A field is therefore a commutative [ring](https://algebrica.org/rings) with unity in which every nonzero element is invertible. Every field is a ring, but a ring is generally not a field.

## Properties

Several properties follow directly from the previous axioms. For any $a \in F$, multiplication by zero satisfies $a \cdot 0 = 0$. This is not assumed but derived: one writes $a \cdot 0 = a \cdot \left(\right. 0 + 0 \left.\right) = a \cdot 0 + a \cdot 0$ and then cancels $a \cdot 0$ from both sides using the additive group structure.

A field contains no zero divisors. If $a \cdot b = 0$ and $a \neq 0$, then $a$ is invertible and one obtains $b = a^{- 1} \cdot \left(\right. a \cdot b \left.\right) = a^{- 1} \cdot 0 = 0$. This means that in a field the product of two nonzero elements is always nonzero, which is the property that makes cancellation possible throughout algebra. The additive and multiplicative structures interact through the identity:

$$\left(\right. - a \left.\right) \cdot b = a \cdot \left(\right. - b \left.\right) = - \left(\right. a \cdot b \left.\right)$$

The expression holds or all $a , b \in F$. In particular, the product of two negative elements is positive in the sense that:

$$\left(\right. - a \left.\right) \cdot \left(\right. - b \left.\right) = a \cdot b$$

a consequence of the axioms rather than a convention.

## Algebraic hierarchy

A [group](https://algebrica.org/groups/) is the most elementary of algebraic structures. It consists of a set equipped with a single binary operation satisfying closure, associativity, the existence of an identity element, and the existence of inverses.

When a second operation is introduced and required to distribute over the first, but without demanding that this second operation admit inverses, the result is a [ring](https://algebrica.org/rings/). The integers $\mathbb{Z}$ are the canonical example. Every [integer](https://algebrica.org/integers/) has an additive inverse, yet most integers lack a multiplicative inverse within $\mathbb{Z}$ itself, since $2^{- 1}$ does not belong to $\mathbb{Z}$.

A field is obtained by imposing one further requirement on a commutative ring with unity, namely that every nonzero element be invertible with respect to multiplication. The three structures thus form a chain of increasing rigidity:

- A group carries one operation with inverses.
- A ring carries two operations, with inverses guaranteed only for addition.
- A field carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> The rational numbers $\mathbb{Q}$, the real numbers $\mathbb{R}$, and the complex numbers $\mathbb{C}$ are all fields. The integers $\mathbb{Z}$, by contrast, form a ring but not a field, since division does not close within them.

## Examples

The set $\mathbb{Q}$ of rational numbers, equipped with ordinary addition and multiplication, is the smallest field containing the integers. Every nonzero rational number $p / q$ has a multiplicative inverse $q / p$, and all field axioms are satisfied.

The set $\mathbb{R}$ of real numbers is a field extending $\mathbb{Q}$. It admits an ordering compatible with its algebraic structure, a property that distinguishes it within the family of fields and that is responsible for many of the analytic concepts built upon it.

The set $\mathbb{C}$ of complex numbers is a field extending $\mathbb{R}$. Unlike $\mathbb{R}$, it is algebraically closed: every nonconstant polynomial with coefficients in $\mathbb{C}$ has at least one root in $\mathbb{C}$, a result known as the fundamental theorem of algebra.

---

For any prime $p$, the set $\mathbb{Z} / p \mathbb{Z} = \left{\right. 0 , 1 , \ldots , p - 1 \left.\right}$ equipped with addition and multiplication [modulo](https://algebrica.org/modulo-operator/) $p$ is a field, commonly denoted $\mathbb{F}_{p}$. This is a finite field: it contains exactly $p$ elements. The primality of $p$ is essential. In $\mathbb{Z} / 6 \mathbb{Z}$, for instance, the elements $2$ and $3$ satisfy $2 \cdot 3 = 0$, so neither is invertible, and the structure fails to be a field.

> Finite fields exist only when the number of elements is a prime power $p^{n}$, for some prime $p$ and positive integer $n$. For every such prime power there exists, up to isomorphism, exactly one finite field, denoted $\mathbb{F}_{p^{n}}$ or $\text{GF} \left(\right. p^{n} \left.\right)$.

## Subfields and field extensions

A subset $K \subseteq F$ is called a subfield of $F$ if $K$ is itself a field under the operations inherited from $F$. Equivalently, $K$ is a subfield of $F$ if it contains $0$ and $1$, and is closed under addition, negation, multiplication, and taking multiplicative inverses of nonzero elements. The rational numbers $\mathbb{Q}$ form a subfield of $\mathbb{R}$, which is itself a subfield of $\mathbb{C}$. These inclusions define a chain of fields:

$$\mathbb{Q} \subseteq \mathbb{R} \subseteq \mathbb{C}$$

When $K$ is a subfield of $F$, one says that $F$ is a field extension of $K$, written $F / K$. From this perspective, $\mathbb{C} / \mathbb{R}$ is a field extension, and $\mathbb{C}$ can be studied as a two-dimensional vector space over $\mathbb{R}$ with basis $\left{\right. 1 , i \left.\right}$. The dimension of $F$ regarded as a vector space over $K$ is called the degree of the extension and is denoted $\left[\right. F : K \left]\right.$. In this example, $\left[\right. \mathbb{C} : \mathbb{R} \left]\right. = 2$.

## Characteristic of a field

Every field $F$ has an associated non-negative integer called its characteristic, which measures how many times the multiplicative identity must be added to itself before reaching zero. Formally, the characteristic of $F$ is the smallest positive integer $n$ such that:

$$\underset{n}{\underbrace{1 + 1 + \hdots + 1}} = 0$$

If no such $n$ exists, the characteristic is defined to be $0$. The characteristic of a field is always either zero or a prime number. If the characteristic were a composite number $n = a b$ with $1 < a , b < n$, one could write:

$$0 = \underset{n}{\underbrace{1 + \hdots + 1}} = \left(\right. \underset{a}{\underbrace{1 + \hdots + 1}} \left.\right) \cdot \left(\right. \underset{b}{\underbrace{1 + \hdots + 1}} \left.\right)$$

Since a field has no zero divisors, one of the two factors would have to be zero, contradicting the minimality of $n$. The fields $\mathbb{Q}$, $\mathbb{R}$, and $\mathbb{C}$ all have characteristic zero. The finite field $\mathbb{F}_{p}$ has characteristic $p$.

## Field homomorphisms

A field homomorphism is a function $\varphi : F \rightarrow K$ between two fields that preserves both operations: for all $a , b \in F$ holds:

$$\varphi \left(\right. a + b \left.\right) = \varphi \left(\right. a \left.\right) + \varphi \left(\right. b \left.\right)$$
$$\varphi \left(\right. a \cdot b \left.\right) = \varphi \left(\right. a \left.\right) \cdot \varphi \left(\right. b \left.\right)$$

We have that $\varphi \left(\right. 1_{F} \left.\right) = 1_{K}$. Every field homomorphism is necessarily injective. To see this, note that its kernel is an [ideal](https://algebrica.org/.../rings/) of $F$:

$$ker ⁡ \left(\right. \varphi \left.\right) = \left{\right. a \in F : \varphi \left(\right. a \left.\right) = 0 \left.\right}$$

Since $F$ is a field, its only ideals are $\left{\right. 0 \left.\right}$ and $F$ itself, and the condition $\varphi \left(\right. 1 \left.\right) = 1 \neq 0$ rules out the second possibility. A bijective field homomorphism is called a field isomorphism. Two fields are isomorphic, written $F \cong K$, if an isomorphism between them exists. Isomorphic fields are algebraically indistinguishable: they share all properties that depend only on the field axioms.

> A function is injective, or one-to-one, if distinct elements of the domain are mapped to distinct elements of the codomain: $\varphi \left(\right. a \left.\right) = \varphi \left(\right. b \left.\right)$ implies $a = b$. A function is bijective if it is both injective and surjective, meaning it is one-to-one and every element of the codomain is the image of at least one element of the domain.

homomorphismscharacteristicfield extensionssubfieldsfinite fieldsexamplesconsistencyclosureinvertibilitysign rulescancellationno zero divisorszero multiplicationcommutative ringdistributive lawmultiplicative groupadditive groupfield axiomsdefinitiontheorypropertiesstructure
