---
layout: chapter
title: "Types of Numbers"
chapter: "Sets and Numbers"
chapter_order: 1
section_order: 2
permalink: /materi-algebrica/sets-and-numbers/types-of-numbers/
---

## Introduction

Numbers organized into nested families, each extending the previous one to accommodate quantities that the smaller family cannot represent. The main numerical sets, listed in order of inclusion, are the natural numbers $\mathbb{N} ,$ the [integers](https://algebrica.org/integers/) $\mathbb{Z} ,$ the rational numbers $\mathbb{Q} ,$ the real numbers $\mathbb{R} ,$ and the [complex numbers](https://algebrica.org/complex-numbers-introduction/) $\mathbb{C}$. The irrational numbers $\mathbb{I}$ occupy a complementary position within $\mathbb{R}$ rather than forming a separate step in the hierarchy. The inclusion relationships among these [sets](https://algebrica.org/sets/) are the following.

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C} , \mathbb{I} \subset \mathbb{R}$$

![](https://algebrica.org/wp-content/uploads/resources/images/numbers.png)

The structure of these sets reflects how each extension resolves a limitation of the previous one, until $\mathbb{C}$ is reached, within which every [polynomial equation](https://algebrica.org/polynomial-equations/) has a solution.

## Natural numbers

The set of [natural numbers](https://algebrica.org/natural-numbers), denoted by $\mathbb{N}$, is the collection of non-negative integers used to count discrete quantities.

$$\mathbb{N} = \left{\right. 0 , 1 , 2 , 3 , 4 , \ldots \left.\right}$$

Each element is obtained by adding one to the previous, starting from $0$. Because natural numbers express how many elements a collection contains, they are also called cardinal numbers. Whether zero belongs to $\mathbb{N}$ is a matter of convention that varies across traditions; the two most common choices are recorded below:

$$\mathbb{N}_{0} = \left{\right. 0 , 1 , 2 , 3 , \ldots \left.\right}$$
$$\mathbb{N}^{+} = \left{\right. 1 , 2 , 3 , \ldots \left.\right}$$

From a foundational point of view, $\mathbb{N}$ is the smallest inductive set contained in $\mathbb{R}$: it contains $0$ and, whenever it contains an element $n$, it also contains $n + 1$. This property is the basis of the [principle of mathematical induction](https://algebrica.org/principle-of-mathematical-induction/).

## Integer numbers

The set of integers, denoted by $\mathbb{Z}$, extends $\mathbb{N}$ by adjoining a negative counterpart to every positive natural number:

$$\mathbb{Z} = \left{\right. \ldots , - 3 , - 2 , - 1 , 0 , 1 , 2 , 3 , \ldots \left.\right}$$

Every integer is either positive, negative, or zero. The set $\mathbb{Z}$ can be expressed as the union of the natural numbers and their negatives:

$$\mathbb{Z} = \mathbb{N} \cup \left{\right. - n : n \in \mathbb{N}^{+} \left.\right}$$

The passage from $\mathbb{N}$ to $\mathbb{Z}$ makes subtraction always well-defined: for any $a , b \in \mathbb{Z}$ the difference $a - b$ is again an integer. A dedicated entry covers the properties of [integers](https://algebrica.org/integers/) in detail.

## Rational numbers

The set of rational numbers, denoted by $\mathbb{Q}$, consists of all numbers that can be expressed as a ratio of two integers with a nonzero denominator:

$$\mathbb{Q} = \left{\right. \frac{p}{q} : p , q \in \mathbb{Z} , q \neq 0 \left.\right}$$

Every integer is rational, since any $n \in \mathbb{Z}$ can be written as $n / 1$. The decimal expansion of a rational number is either terminating or eventually periodic: for example, $1 / 4 = 0.25$ and $1 / 3 = 0.333 \ldots$ The following are further examples of rational numbers.

$$\frac{- 5}{4} , \frac{12}{7} , - 8 , \frac{25}{19}$$

The passage from $\mathbb{Z}$ to $\mathbb{Q}$ makes division by any nonzero integer always well-defined.

## Irrational numbers

A real number is called irrational if it cannot be expressed as a ratio of two integers. The set of irrational numbers is denoted by $\mathbb{I}$, and it satisfies $\mathbb{R} = \mathbb{Q} \cup \mathbb{I}$ with $\mathbb{Q} \cap \mathbb{I} = \emptyset$. The decimal expansion of an irrational number is non-terminating and non-periodic. Familiar examples include the following.

$$\sqrt{2} , \sqrt{3} , \pi , e , - \sqrt[3]{5}$$

The irrationality of $\sqrt{2}$ is one of the oldest results in mathematics and admits a concise proof by contradiction. Assuming $\sqrt{2} = p / q$ in lowest terms leads to the conclusion that both $p$ and $q$ are even, contradicting the assumption. The numbers $\pi$ and $e$ are irrational but belong to a further distinguished class: they are transcendental, meaning they are not roots of any nonzero polynomial with rational coefficients.

## Real numbers

The set of [real numbers](https://algebrica.org/real-numbers/), denoted by $\mathbb{R}$, is the union of the rational and irrational numbers.

$$\mathbb{R} = \mathbb{Q} \cup \mathbb{I}$$

The passage from $\mathbb{Q}$ to $\mathbb{R}$ fills the gaps left by the rationals,
ensuring that every convergent [sequence](https://algebrica.org/sequences/) has a [limit](https://algebrica.org/limits/) within the set. Every real number admits a decimal representation of the following form.

$$\left{\right. p , \alpha_{0} \alpha_{1} \alpha_{2} \alpha_{3} \ldots : p \in \mathbb{Z} , \alpha_{k} \in \left{\right. 0 , 1 , 2 , \ldots , 9 \left.\right} , \forall k \in \mathbb{N} \left.\right}$$

In this representation, the components are interpreted as follows:

- $p \in \mathbb{Z}$ is the integer part, which may be positive, negative, or zero.
- $\alpha_{0} , \alpha_{1} , \alpha_{2} , \ldots$ are the decimal digits, each belonging to $0 , 1 , \ldots , 9$.
- The index $k \in \mathbb{N}$ ranges over all natural numbers, so the decimal expansion continues indefinitely.

For rational numbers the decimal expansion is eventually periodic. For irrational numbers it is non-terminating and non-periodic.

---

Geometrically, $\mathbb{R}$ corresponds to the points of a continuous straight line, the real number line, with no gaps.

![](https://algebrica.org/wp-content/uploads/resources/images/numbers-2-2.png)

Completeness is what distinguishes $\mathbb{R}$ from $\mathbb{Q}$: the sequence of rational approximations to $\sqrt{2}$, for instance, has no limit within $\mathbb{Q}$, but its limit exists in $\mathbb{R}$. The topic of least upper bounds is treated in the entry on [supremum and infimum](https://algebrica.org/supremum-and-infimum/).

The set $\mathbb{R}$ is also totally ordered: for any two real numbers $x$ and $y$, exactly one of the relations $x < y$, $x = y$, or $x > y$ holds. Moreover, $\mathbb{R}$ satisfies the Archimedean property: for every real number $x$ there exists a natural number $n$ such that $n > x$. This rules out the existence of infinitely large or infinitely small elements within $\mathbb{R}$.

A further structural distinction separates $\mathbb{Q}$ from $\mathbb{R}$ at the level of cardinality. The rational numbers form a countable set, meaning their elements can be put in one-to-one correspondence with $\mathbb{N}$. The real numbers, by contrast, are uncountable: no such correspondence exists, as shown by Cantor’s diagonal argument. In this precise sense, the irrational numbers constitute the vast majority of the real line. The properties of the real number system are discussed further in the entry on [properties of real numbers](https://algebrica.org/properties-of-real-numbers/).

Since zero carries no sign, it does not belong to either the positive or negative reals. For this reason the following terminology is standard: a non-negative real number satisfies $x \geq 0$, while a non-positive real number satisfies $x \leq 0$.

## Complex numbers

The set of complex numbers, denoted by $\mathbb{C}$, extends $\mathbb{R}$ by introducing an element $i$ satisfying $i^{2} = - 1$. Every complex number takes the form

$$z = a + b i$$

where $a$ and $b$ are real numbers, called respectively the real part and the imaginary part of $z$. When $b = 0$ the number reduces to a real number, so $\mathbb{R} \subset \mathbb{C}$. When $a = 0$ and $b \neq 0$ the number is called purely imaginary.

The passage to $\mathbb{C}$ makes it possible to take square roots of negative numbers and, more generally, to factor every polynomial completely: by the fundamental theorem of algebra, every non-constant polynomial with complex coefficients has at least one root in $\mathbb{C}$. This closure property is not shared by $\mathbb{R}$: the polynomial $x^{2} + 1$, for instance, has no real roots. A full treatment of complex numbers is given in the entry on [complex numbers](https://algebrica.org/complex-numbers-introduction/).

complex planealgebraic formnumber linedecimal expansiondensitycardinalitycompletenessorderingclosurecomplex numbersreal numbersirrational numbersrational numbersintegersnatural numbersrepresentationspropertieshierarchy
