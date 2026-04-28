---
layout: chapter
title: "Big O Notation"
chapter: "Limits"
chapter_order: 15
section_order: 8
permalink: /materi-algebrica/limits/big-o-notation/
---

## What is Big O notation

The symbol $O \left(\right. x \left.\right)$, commonly known as big O of $x$, is part of the Landau symbol family. It represents the concept of [asymptotic](https://algebrica.org/asymptotes/) upper bounds, signifying that a [function](https://algebrica.org/functions) does not grow faster than another function as the input approaches a specified [limit](https://algebrica.org/limits). Formally, it indicates that the ratio of the two functions remains bounded as the input approaches the limit.

Let $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ be two functions defined on a set $A$, and let $x_{0}$ be a limit point for $A$. If there exist positive constants $M$ and $\delta$ such that for all $x$ in a neighborhood of $x_{0}$ (excluding $x_{0}$ itself), $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq M \left|\right. g \left(\right. x \left.\right) \left|\right.$, then we say that $f \left(\right. x \left.\right)$ is big O of $g \left(\right. x \left.\right)$ as $x$ approaches $x_{0}$. In symbols:

$$\exists M > 0 , \delta > 0 : \left|\right. x - x_{0} \left|\right. < \delta \rightarrow \left|\right. f \left(\right. x \left.\right) \left|\right. \leq M \left|\right. g \left(\right. x \left.\right) \left|\right. \rightarrow f \left(\right. x \left.\right) = O_{x_{0}} \left(\right. g \left(\right. x \left.\right) \left.\right)$$

This notation indicates that $f \left(\right. x \left.\right)$ grows asymptotically no faster than $g \left(\right. x \left.\right)$ near $x_{0}$. To illustrate this definition, let $f \left(\right. x \left.\right) = 3 x^{2} + 2 x + 1$ and $g \left(\right. x \left.\right) = x^{2}$. The graph displays $f \left(\right. x \left.\right)$ together with $6 x^{2} = M \cdot g \left(\right. x \left.\right)$, which serves as the asymptotic upper bound.

![](https://algebrica.org/wp-content/uploads/resources/images/big-o-notation-1.png)

For all $x \geq 1$, the curve $f \left(\right. x \left.\right)$ remains entirely below $6 x^{2}$. Although both curves exhibit the same growth rate, $f \left(\right. x \left.\right)$ does not exceed its bound. This relationship represents the geometric interpretation of $f \left(\right. x \left.\right) = O \left(\right. x^{2} \left.\right)$.

## Example

To make the concept clearer, let us consider a simple example. Consider the function $f \left(\right. x \left.\right) = 3 x^{2} + 2 x + 1$ as $x \rightarrow \infty$. We want to show that $f \left(\right. x \left.\right) = O \left(\right. x^{2} \left.\right)$.

For large values of $x$, we can analyze:

$$\frac{3 x^{2} + 2 x + 1}{x^{2}} = 3 + \frac{2}{x} + \frac{1}{x^{2}}$$

As $x \rightarrow \infty$, this ratio approaches 3. More precisely, for $x \geq 1$:

$$\frac{3 x^{2} + 2 x + 1}{x^{2}} = 3 + \frac{2}{x} + \frac{1}{x^{2}} \leq 3 + 2 + 1 = 6$$

Therefore, we can choose $M = 6$ and conclude:

$$3 x^{2} + 2 x + 1 = O \left(\right. x^{2} \left.\right) \text{as} x \rightarrow \infty$$

Let’s explore why this is the case. If we compare $f \left(\right. x \left.\right) = 3 x^{2} + 2 x + 1$ and $g \left(\right. x \left.\right) = x^{2}$ as $x$ approaches infinity, we observe that $f \left(\right. x \left.\right)$ grows at most as fast as a constant multiple of $x^{2}$.

Here are a few examples:

- If $x = 10$, then $f \left(\right. x \left.\right) = 300 + 20 + 1 = 321$ and $6 x^{2} = 600$.
- If $x = 100$, then $f \left(\right. x \left.\right) = 30000 + 200 + 1 = 30201$ and $6 x^{2} = 60000$.
- If $x = 1000$, then $f \left(\right. x \left.\right) = 3000000 + 2000 + 1 = 3002001$ and $6 x^{2} = 6000000$.

As these examples show, $f \left(\right. x \left.\right)$ is always bounded above by $6 x^{2}$ for $x \geq 1$. This is the key idea behind the big O notation: it captures the fact that one function grows at most as fast as another (up to a constant factor) as the input approaches a particular value.

## The meaning of $O \left(\right. 1 \left.\right)$

The symbol $O \left(\right. 1 \left.\right)$ represents the class of functions that remain bounded as $x$ approaches a specific point $x_{0}$. In other words, a function $f \left(\right. x \left.\right)$ is said to belong to $O \left(\right. 1 \left.\right)$ when it remains bounded compared to a constant as $x \rightarrow x_{0}$. Formally, we write $f \left(\right. x \left.\right) = O \left(\right. 1 \left.\right)$ as $x \rightarrow x_{0}$ if and only if:

$$\exists M > 0 , \delta > 0 : \left|\right. x - x_{0} \left|\right. < \delta \Rightarrow \left|\right. f \left(\right. x \left.\right) \left|\right. \leq M$$

The set of all functions that belong to $O \left(\right. 1 \left.\right)$ can be described as follows:

$$O_{x_{0}} \left(\right. 1 \left.\right) = \left{\right. f : B \left(\right. x_{0} , \delta \left.\right) \backslash x_{0} \rightarrow \mathbb{R} , \left|\right. , \exists M > 0 : \left|\right. f \left(\right. x \left.\right) \left|\right. \leq M \text{for} x \text{near} x_{0} \left.\right}$$

In practice, this expression is used to describe the concept of $O \left(\right. 1 \left.\right)$ by specifying that:

- The functions considered must be defined on a neighborhood of $x_{0}$, excluding the point $x_{0}$ itself.
- The function must remain bounded as $x$ approaches $x_{0}$.
- The notation $O \left(\right. 1 \left.\right)$ represents the set of all functions that are bounded compared to a constant, specifically to 1.
- The symbol $B \left(\right. x_{0} , \delta \left.\right)$ denotes an open neighborhood of $x_{0}$ with radius $\delta$, where the function is defined.

## Example 1

Let us consider the function:

$$f \left(\right. x \left.\right) = \frac{sin ⁡ \left(\right. x \left.\right)}{x} \text{as} x \rightarrow 0$$

Using the Taylor expansion of $sin ⁡ \left(\right. x \left.\right)$ near zero, as $x \rightarrow 0$, we have:

$$sin ⁡ \left(\right. x \left.\right) = x - \frac{x^{3}}{6} + O \left(\right. x^{5} \left.\right)$$

Dividing both sides by $x$, as $x \rightarrow 0$, we get:

$$\frac{sin ⁡ \left(\right. x \left.\right)}{x} = 1 - \frac{x^{2}}{6} + O \left(\right. x^{4} \left.\right)$$

Now observe that the term $\frac{x^{2}}{6}$ and the remainder $O \left(\right. x^{4} \left.\right)$ both remain bounded as $x \rightarrow 0$. Therefore, as $x \rightarrow 0$ we can write:

$$\frac{sin ⁡ \left(\right. x \left.\right)}{x} = O \left(\right. 1 \left.\right)$$

This expression shows that the function remains bounded near $x = 0$, even though the function has a removable singularity at that point

## Example 2

Big O notation frequently arises in the context of Taylor expansions to characterise the remainder term. For example, consider the Taylor expansion of $cos ⁡ \left(\right. x \left.\right)$ near zero:

$$cos ⁡ \left(\right. x \left.\right) = 1 - \frac{x^{2}}{2} + \frac{x^{4}}{24} - \hdots$$

Truncating the series after the second term yields a remainder that is bounded by a constant multiple of $x^{4}$ for $x$ near zero. Therefore, it can be expressed as:

$$cos ⁡ \left(\right. x \left.\right) = 1 - \frac{x^{2}}{2} + O \left(\right. x^{4} \left.\right) \text{as} x \rightarrow 0$$

This means there exists a constant $M > 0$ such that:

$$\left|\right. cos ⁡ \left(\right. x \left.\right) - 1 + \frac{x^{2}}{2} \left|\right. \leq M x^{4}$$

for all $x$ in a neighborhood of zero. Since the next term in the series is $x^{4} / 24$, it follows that $M = 1 / 24$ is sufficient for sufficiently small $x$. This application of big O notation is common in analysis: instead of retaining the entire infinite series, only the terms of interest are kept, and all higher-order contributions are incorporated into a single remainder term $O \left(\right. x^{n} \left.\right)$.

## Properties

One fundamental property of the big O notation is that, by definition, if $g \left(\right. x \left.\right) = O \left(\right. f \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$, then the ratio of the two functions remains bounded. In formal terms:

$$\underset{x \rightarrow x_{0}}{lim sup} \left|\right. \frac{O \left(\right. f \left(\right. x \left.\right) \left.\right)}{f \left(\right. x \left.\right)} \left|\right. < \infty$$

---

Multiplying a function by a nonzero constant does not change its asymptotic behavior in big O notation. For any constant $c \neq 0$ and function $g \left(\right. x \left.\right)$, as $x \rightarrow x_{0}$, we have:

$$O \left(\right. c \cdot g \left(\right. x \left.\right) \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$$
$$c \cdot O \left(\right. g \left(\right. x \left.\right) \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$$

##### This shows that big O notation absorbs constant factors: scaling by a nonzero constant factor does not affect the asymptotic upper bound near $x_{0}$.

---

Big O terms also behave predictably under addition. The sum of two big O terms of the same function remains a big O term of that function. Formally as $x \rightarrow x_{0}$:

$$O \left(\right. f \left(\right. x \left.\right) \left.\right) + O \left(\right. f \left(\right. x \left.\right) \left.\right) = O \left(\right. f \left(\right. x \left.\right) \left.\right)$$

##### This means that adding two functions that are each asymptotically bounded by $f \left(\right. x \left.\right)$ results in a sum that is still asymptotically bounded by $f \left(\right. x \left.\right)$ (possibly with a larger constant).

---

When multiplying a big O term by a function, the result is a new big O term where the asymptotic behavior scales accordingly. Specifically, for functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$, as (x \to x_0):

$$f \left(\right. x \left.\right) , O \left(\right. g \left(\right. x \left.\right) \left.\right) = O \left(\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left.\right)$$

For example, if $g \left(\right. x \left.\right) = x$ and $O \left(\right. g \left(\right. x \left.\right) \left.\right) = O \left(\right. x \left.\right)$, then multiplying by $f \left(\right. x \left.\right) = x^{2}$ gives:

$$x^{2} \cdot O \left(\right. x \left.\right) = O \left(\right. x^{3} \left.\right)$$

---

Another important property of the big O notation involves powers of functions. If a function $f \left(\right. x \left.\right)$ is asymptotically bounded by $g \left(\right. x \left.\right)$ as $x \rightarrow x_{0}$, then raising both functions to the same positive power preserves the big O relationship. Formally, for $a > 0$, if $f \left(\right. x \left.\right) = O \left(\right. g \left(\right. x \left.\right)$ as $x \rightarrow x_{0}$, then:

$$\left[\right. f \left(\right. x \left.\right) \left]\right.^{a} = O \left(\right. \left[\right. g \left(\right. x \left.\right) \left]\right.^{a} \left.\right)$$

This property shows that the asymptotic upper bound scales consistently under positive powers: if $f \left(\right. x \left.\right)$ is bounded by a multiple of $g \left(\right. x \left.\right)$, then $\left[\right. f \left(\right. x \left.\right) \left]\right.^{a}$ is also bounded by a multiple of $\left[\right. g \left(\right. x \left.\right) \left]\right.^{a}$ as $x \rightarrow x_{0}$. For example, if $f \left(\right. x \left.\right) = O \left(\right. x \left.\right)$ as $x \rightarrow \infty$, then as $x \rightarrow \infty$ we have:

$$\left[\right. f \left(\right. x \left.\right) \left]\right.^{2} = O \left(\right. x^{2} \left.\right)$$

---

Big O notation demonstrates the property of transitivity. Specifically, if $f \left(\right. x \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$ and $g \left(\right. x \left.\right) = O \left(\right. h \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$, then:

$$f \left(\right. x \left.\right) = O \left(\right. h \left(\right. x \left.\right) \left.\right) \text{as} x \rightarrow x_{0}$$

The proof is straightforward. By assumption, there exist positive constants $M_{1}$ and $M_{2}$, as well as a neighborhood of $x_{0}$, such that $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq M_{1} \left|\right. g \left(\right. x \left.\right) \left|\right.$ and $\left|\right. g \left(\right. x \left.\right) \left|\right. \leq M_{2} \left|\right. h \left(\right. x \left.\right) \left|\right.$ both hold.

Combining these inequalities gives $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq M_{1} M_{2} \left|\right. h \left(\right. x \left.\right) \left|\right.$, so $f \left(\right. x \left.\right) = O \left(\right. h \left(\right. x \left.\right) \left.\right)$ with constant $M = M_{1} M_{2}$. For example, $x^{3} = O \left(\right. x^{4} \left.\right)$ and $x^{4} = O \left(\right. x^{5} \left.\right)$ as $x \rightarrow \infty$, so by transitivity, $x^{3} = O \left(\right. x^{5} \left.\right)$ as $x \rightarrow \infty$.

##### Transitivity enables chaining of asymptotic bounds: if $f$ is bounded by $g$ and $g$ is bounded by $h$, then $f$ is also bounded by $h$.

## Relationship with little-o notation

It’s important to note the relationship between big O and [little-o notation](https://algebrica.org/little-o-notation/).

- If $f \left(\right. x \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$, then $f \left(\right. x \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$: little-o implies big O.
- The converse is not necessarily true: $f \left(\right. x \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$ does not imply $f \left(\right. x \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$ For example, $f \left(\right. x \left.\right) = x$ and $g \left(\right. x \left.\right) = x$ satisfy $f \left(\right. x \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$ but not $f \left(\right. x \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow \infty$, since $\underset{x \rightarrow \infty}{lim} \frac{x}{x} = 1 \neq 0.$

## Selected references

- **MIT**. [Big O Notation](https://web.mit.edu/16.070/www/lecture/big_o.pdf)
- **University of Illinois, A. J. Hildebrand**. [Asymptotic Notations](https://faculty.math.illinois.edu/~hildebr/595ama/ama-ch2.pdf)
- **Rice University, J. A. Dobelman**. [Big O and Little o](https://www.stat.rice.edu/~dobelman/notes_papers/math/big_O.little_o.pdf)
- **Simon Fraser University, R. Lockhart**. [Landau Notation: Big O and Little o](https://www.sfu.ca/~lockhart/richard/830/20_3/lectures/Landau/web.pdf)
