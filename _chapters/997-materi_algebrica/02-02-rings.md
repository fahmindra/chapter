---
layout: chapter
title: "Rings"
chapter: "Algebraic Structures"
chapter_order: 2
section_order: 2
permalink: /materi-algebrica/algebraic-structures/rings/
---

## Definition

A ring is an algebraic structure that extends the notion of a [group](https://algebrica.org/groups/) by introducing a second binary operation. The concept arises from the observation that several fundamental objects, such as the [integers](https://algebrica.org/integers/), the [polynomials](https://algebrica.org/polynomials/) with real coefficients, and the [square matrices](https://algebrica.org/matrices/) of a given size, share a common pattern. They admit both an addition and a multiplication, the two operations interact in a predictable way, and yet multiplication need not be commutative and need not admit inverses. A ring is a set $R$ together with two binary operations $+$ and $\cdot$ (addition and multiplication), satisfying the following axioms:

- $\left(\right. R , + \left.\right)$ is an abelian group. In particular, there exists an element $0 \in R$ such that $a + 0 = a$ for all $a \in R$, and for every $a \in R$ there exists $- a \in R$ with $a + \left(\right. - a \left.\right) = 0$.
- Associativity of multiplication: for all $a , b , c \in R$, one has $\left(\right. a \cdot b \left.\right) \cdot c = a \cdot \left(\right. b \cdot c \left.\right)$.
- Distributivity: for all $a , b , c \in R$, one has $a \cdot \left(\right. b + c \left.\right) = a \cdot b + a \cdot c$ and $\left(\right. a + b \left.\right) \cdot c = a \cdot c + b \cdot c$.

A ring $\left(\right. R , + , \cdot \left.\right)$ is called commutative if $a \cdot b = b \cdot a$ for all $a , b \in R$. It is called a ring with unity, or unital ring, if there exists a multiplicative identity element $1 \in R$ such that $1 \cdot a = a \cdot 1 = a$ for all $a \in R$.

## Properties

Several consequences follow directly from the axioms. For any $a \in R$, multiplication by the additive identity satisfies $a \cdot 0 = 0 \cdot a = 0$. This is a consequence of distributivity. One writes:

$$a \cdot 0 = a \cdot \left(\right. 0 + 0 \left.\right) = a \cdot 0 + a \cdot 0$$

and then cancels $a \cdot 0$ from both sides using the group structure of $\left(\right. R , + \left.\right)$. Similarly, for all $a , b \in R$ one has the following identity:

$$\left(\right. - a \left.\right) \cdot b = a \cdot \left(\right. - b \left.\right) = - \left(\right. a \cdot b \left.\right)$$

In particular, $\left(\right. - 1 \left.\right) \cdot a = - a$ whenever $R$ has a unity. These sign rules hold in any ring.

- A nonzero element $a \in R$ is called a zero divisor if there exists a nonzero element $b \in R$ such that $a \cdot b = 0$ or $b \cdot a = 0$.
- Zero divisors are a feature that distinguishes rings from fields: in a field, no nonzero element can be a zero divisor.
- A commutative ring with unity that contains no zero divisors is called an integral domain.

## Algebraic hierarchy

A [group](https://algebrica.org/groups/) is the most elementary of these structures. It consists of a set equipped with a single binary operation satisfying closure, associativity, the existence of an identity element, and the existence of inverses.

A ring extends this framework by introducing a second operation, multiplication, required to be associative and to distribute over addition, but not necessarily commutative and not required to admit inverses.

When the additional requirement that every nonzero element possess a multiplicative inverse is imposed on a commutative ring with unity, the structure becomes a [field](https://algebrica.org/fields/). The three structures thus form a chain of increasing rigidity:

- A group carries one operation with inverses.
- A ring carries two operations, with inverses guaranteed only for addition.
- A field carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> The integers $\mathbb{Z}$ are the most natural example of a ring that is not a field: every integer has an additive inverse, yet $2^{- 1}$ does not belong to $\mathbb{Z} .$ The rational numbers $\mathbb{Q}$, by contrast, form a field.

## Examples

The set $\mathbb{Z}$ of integers, equipped with ordinary addition and multiplication, is the most simple example of a commutative ring with unity. The additive identity is $0$, the multiplicative identity is $1$, and every integer has an additive inverse. The integers form an integral domain, since the product of two nonzero integers is always nonzero.

The set of polynomials with real coefficients, denoted $\mathbb{R} \left[\right. x \left]\right.$, forms a commutative ring with unity under the usual addition and multiplication of polynomials. The additive identity is the zero polynomial, and the multiplicative identity is the constant polynomial $1$. This ring is also an integral domain.

---

Let $n$ be a positive integer. The set $\mathbb{Z} / n \mathbb{Z} = 0 , 1 , \ldots , n - 1$, equipped with addition and multiplication [modulo](https://algebrica.org/modulo-operator/) $n$, forms a commutative ring with unity. For example, in $\mathbb{Z} / 6 \mathbb{Z}$ one has $2 \cdot 3 = 0$, so $2$ and $3$ are zero divisors and $\mathbb{Z} / 6 \mathbb{Z}$ is not an integral domain. When $n$ is prime, however, $\mathbb{Z} / n \mathbb{Z}$ contains no zero divisors and is in fact a field.

Let $F$ be a field and let $n$ be a positive integer. The set $M_{n} \left(\right. F \left.\right)$ of all $n \times n$ [matrices](https://algebrica.org/matrices/) with entries in $F$ forms a ring under matrix addition and multiplication. The additive identity is the zero matrix, and the multiplicative identity is the identity matrix $I_{n}$. For $n \geq 2$, this ring is not commutative, since matrix multiplication does not commute in general, and it contains zero divisors.

## Subrings

A subset $S$ of a ring $R$ is called a subring if $S$ is itself a ring under the operations inherited from $R$. A nonempty subset $S \subseteq R$ is a subring of $R$ if and only if it is closed under subtraction and under multiplication, that is, for all $a , b \in S$ one has $a - b \in S$ and $a \cdot b \in S$. Closure under subtraction is equivalent to requiring that $S$ be a subgroup of $\left(\right. R , + \left.\right)$, and closure under multiplication then ensures that the second operation is also well-defined on $S$. Every ring $R$ contains at least two subrings:

- the trivial subring $0$
- $R$ itself.

Any subring other than $R$ is called a proper subring.

As an example, the set of even integers $2 \mathbb{Z} = \left{\right. \ldots , - 4 , - 2 , 0 , 2 , 4 , \ldots \left.\right}$ is a subring of $\left(\right. \mathbb{Z} , + , \cdot \left.\right)$. For any two even integers $a = 2 m$ and $b = 2 k$, one has $a - b = 2 \left(\right. m - k \left.\right) \in 2 \mathbb{Z}$ and $a \cdot b = 4 m k \in 2 \mathbb{Z}$, so both conditions are satisfied. Note that $2 \mathbb{Z}$ does not contain the multiplicative identity $1$ of $\mathbb{Z}$, which illustrates that a subring of a unital ring need not itself be unital.

## Ideals

Ideals are the subsets that allow the construction of quotient rings, playing a role analogous to normal subgroups in group theory. A nonempty subset $I \subseteq R$
is called a left ideal of $R$ if it is closed under addition and under left multiplication by elements of $R$, that is, for all $a \in I$ and $r \in R$
one has $r \cdot a \in I$. A right ideal is defined analogously with right multiplication. A subset that is simultaneously a left and a right ideal is called a
two-sided ideal, or simply an ideal.

The set $n \mathbb{Z}$ of all multiples of a fixed integer $n$ is an ideal of
$\mathbb{Z}$: for any $a = n k \in n \mathbb{Z}$ and any $r \in \mathbb{Z}$
one has:

$$r \cdot a = n \left(\right. r k \left.\right) \in n \mathbb{Z}$$

> Ideals are precisely the kernels of ring homomorphisms, a fact that makes them the natural tool for constructing quotient rings and studying the structure of rings through their homomorphic images.

## Ring homomorphisms and isomorphisms

A ring homomorphism is a [function](https://algebrica.org/functions/) between two rings that preserves both operations. Given two rings $\left(\right. R , + , \cdot \left.\right)$ and $\left(\right. S , \oplus , \bigodot \left.\right)$, a function $\varphi : R \rightarrow S$ is a ring homomorphism if for all $a , b \in R$:

$$\varphi \left(\right. a + b \left.\right) = \varphi \left(\right. a \left.\right) \oplus \varphi \left(\right. b \left.\right)$$
$$\varphi \left(\right. a \cdot b \left.\right) = \varphi \left(\right. a \left.\right) \bigodot \varphi \left(\right. b \left.\right)$$

The first condition requires that $\varphi$ be a group homomorphism between the additive groups, and the second that it preserve multiplication. As a consequence, $\varphi$ maps the additive identity of $R$ to the additive identity of $S$. If both rings are unital, one often additionally requires that $\varphi \left(\right. 1_{R} \left.\right) = 1_{S}$. The kernel and image of a ring homomorphism $\varphi : R \rightarrow S$ are defined as in the case of groups:

$$ker ⁡ \left(\right. \varphi \left.\right) = \left{\right. a \in R : \varphi \left(\right. a \left.\right) = 0_{S} \left.\right}$$
$$im \left(\right. \varphi \left.\right) = \left{\right. \varphi \left(\right. a \left.\right) : a \in R \left.\right}$$

The kernel is always an ideal of $R$, and the image is always a subring of $S$. A homomorphism is injective if and only if its kernel contains only the additive identity of $R .$

---

A ring homomorphism that is injective and surjective is called a ring isomorphism. Two rings are isomorphic, written $R \cong S$, if an isomorphism between them exists. Isomorphic rings are structurally identical and share all properties that are intrinsic to their ring structure.

As an example, consider the map $\varphi : \mathbb{Z} \rightarrow \mathbb{Z} / n \mathbb{Z}$ defined by $\varphi \left(\right. a \left.\right) = a mod n$. This map preserves addition and multiplication, since $\left(\right. a + b \left.\right) mod n = \left(\right. a mod n \left.\right) + \left(\right. b mod n \left.\right)$ and analogously for multiplication. It is therefore a ring homomorphism, and its kernel is precisely $n \mathbb{Z}$, the ideal of multiples of $n$.

isomorphismshomomorphismstwo-sided idealidealssubringscancellationsign identitieszero divisorsmultiplication rulesadditive inversezero elementintegral domainring with unitycommutative ringdistributivitymultiplicative structureadditive structuredefinitionsubstructurespropertiesstructure
