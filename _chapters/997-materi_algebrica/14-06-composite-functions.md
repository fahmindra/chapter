---
layout: chapter
title: "Composite Functions"
chapter: "Functions"
chapter_order: 14
section_order: 6
permalink: /materi-algebrica/functions/composite-functions/
---

## What are composite functions

When we talk about composite functions, we refer to the process of applying one [function](https://algebrica.org/functions) to the result of another. In other words, given two functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$, a composite function is formed by evaluating $g$ at the output of $f$. This is denoted by:

$$g \circ f = g \left(\right. f \left(\right. x \left.\right) \left.\right)$$

This means that we first apply $f$ to the input $x$, and then apply $g$ to the result.

![](https://algebrica.org/wp-content/uploads/resources/images/composite-functions-1-1.png)

##### This diagram illustrates the concept of a composite function: the input $x$ from set $A$ is first mapped to $f \left(\right. x \left.\right)$ in set $B$, and then $f \left(\right. x \left.\right)$ is mapped to $g \left(\right. f \left(\right. x \left.\right) \left.\right)$ in set $C$, resulting in the composition $g \circ f$.

---

More formally, let two functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ be given such that:

- $f : A \rightarrow B$
- $g : B \rightarrow C$
- $f \left(\right. A \left.\right) \subseteq B$

The composite function is defined as follows:

$$g \circ f : x \in A \rightarrow g \left(\right. f \left(\right. x \left.\right) \left.\right) \in C$$

This means that the function $g \circ f$ maps each element $x$ in the [domain](https://algebrica.org/determining-the-domain-of-a-function/) $A$ to the value $g \left(\right. f \left(\right. x \left.\right) \left.\right)$, provided that the image of $f$ is contained in the domain of $g$.

## Example

Consider the following functions:

- $f \left(\right. x \left.\right) = 2 x + 3$
- $g \left(\right. x \left.\right) = x^{2}$

---

We wanto to define the composite function $g \circ f = g \left(\right. f \left(\right. x \left.\right) \left.\right)$. Let’s start by evaluating $f \left(\right. x \left.\right)$:

$$f \left(\right. x \left.\right) = 2 x + 3$$

Now plug that into $g \left(\right. x \left.\right)$:

$$g \left(\right. f \left(\right. x \left.\right) \left.\right) = g \left(\right. 2 x + 3 \left.\right) = \left(\right. 2 x + 3 \left.\right)^{2}$$

Therefore, the composite function is:
$$g \circ f = \left(\right. 2 x + 3 \left.\right)^{2}$$

## Composition with the inverse function

If a function $f$ is composed with its [inverse](https://algebrica.org/inverse-function) $f^{- 1}$, the result is the identity function, which maps each element of a set to itself:

$$f \left(\right. f^{- 1} \left(\right. x \left.\right) \left.\right) = f^{- 1} \left(\right. f \left(\right. x \left.\right) \left.\right) = x$$

##### This operation is valid only if the function $f$ is invertible, meaning that it is both one-to-one (injective) and onto (surjective) over its domain.

When the composition between two functions is well-defined, that is, when the output of the first function lies within the domain of the second, we can write:

$$g \left(\right. f \left(\right. x \left.\right) \left.\right) \equiv g \circ f \text{and} f \left(\right. g \left(\right. x \left.\right) \left.\right) \equiv f \circ g$$

This notation highlights that function composition is **not commutative**: in general, the order in which functions are composed affects the outcome, and the following holds:

$$g \circ f \neq f \circ g$$

## Example

Let’s demonstrate with a simple example that function composition is not a commutative operation, that is, in general, $g \circ f \neq f \circ g$. Consider the two functions:

- $f \left(\right. x \left.\right) = e^{x}$
- $g \left(\right. x \left.\right) = x + 1$

---

Compute $f \circ g$:
$$f \circ g = f \left(\right. g \left(\right. x \left.\right) \left.\right) = f \left(\right. x + 1 \left.\right) = e^{x + 1}$$

Compute $g \circ f$:
$$g \circ f = g \left(\right. f \left(\right. x \left.\right) \left.\right) = g \left(\right. e^{x} \left.\right) = e^{x} + 1$$

We have:

- $\left(\right. f \circ g \left.\right) \left(\right. x \left.\right) = e^{x + 1} = e \cdot e^{x}$
- $\left(\right. g \circ f \left.\right) \left(\right. x \left.\right) = e^{x} + 1$

These expressions are not equal and this proves that function composition is not commutative.
