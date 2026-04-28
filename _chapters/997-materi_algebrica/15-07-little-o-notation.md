---
layout: chapter
title: "Little-o Notation"
chapter: "Limits"
chapter_order: 15
section_order: 7
permalink: /materi-algebrica/limits/little-o-notation/
---

## What is little-o notation

The symbol $o \left(\right. x \left.\right)$, referred to as little-o of $x$, belongs to the Landau symbol family, which is used to characterise asymptotic relationships between functions. This notation indicates that one function is negligible compared to another as the input approaches a given limit. Thus, $o \left(\right. x \left.\right)$ formalises [asymptotic](https://algebrica.org/asymptotes/) control by signifying that the growth rate of one function is insignificant relative to the other in the [limit](https://algebrica.org/limits/).

Let $f , g : A \rightarrow \mathbb{R}$ (or $\mathbb{C}$) be two [functions](https://algebrica.org/functions/), and let $x_{0}$ be a limit point of $A$. We say that $f \left(\right. x \left.\right)$ is little-o of $g \left(\right. x \left.\right)$ as $x \rightarrow x_{0}$ if $g \left(\right. x \left.\right) \neq 0$ in a neighborhood of $x_{0}$ (except possibly at $x_{0}$ itself) and:

$$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = 0$$

Equivalently, for every $\epsilon > 0$ there exists $\delta > 0$ such that whenever $0 < \left|\right. x - x_{0} \left|\right. < \delta$, we have $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq \epsilon \cdot \left|\right. g \left(\right. x \left.\right) \left|\right.$. This definition means that $f \left(\right. x \left.\right)$ grows asymptotically slower than $g \left(\right. x \left.\right)$ near $x_{0}$.

> This notation applies to limits at infinity by replacing $x \rightarrow x_{0}$ with $x \rightarrow \infty$. It also applies to [sequences](https://algebrica.org/sequences/), where the independent variable $x$ is replaced by $n \rightarrow \infty$.

## Example 1

To make the concept clearer, let us consider a simple example given by the following limit:

$$\underset{x \rightarrow 0}{lim} \frac{x^{2}}{x} = \underset{x \rightarrow 0}{lim} x = 0$$

This limit demonstrates that $x^{2}$ grows asymptotically slower than $x$ as $x$ approaches 0. Therefore, we can write:

$$x^{2} = o \left(\right. x \left.\right) \text{as} x \rightarrow 0$$

Let’s explore why this is the case. If we compare $x$ and $x^{2}$ as $x$ approaches zero, we observe that both functions tend to zero, but at different rates. The graph clearly shows that, near zero, $x^{2}$ is much smaller than $x$.

![](https://algebrica.org/wp-content/uploads/resources/images/little-o-1.png)

Here are a few examples:

- If $x = 0.1$, then $x = 0.1$ and $x^{2} = 0.01$.
- If $x = 0.01$, then $x = 0.01$ and $x^{2} = 0.0001$.
- If $x = 0.001$, then $x = 0.001$ and $x^{2} = 0.000001$.

As these examples show, $x^{2}$ becomes much smaller than $x$ as $x$ approaches zero. This is the key idea behind the little-o notation: it captures the fact that one function can become asymptotically negligible compared to another as the input approaches a particular value.

## Example 2

Little-o notation remains applicable when the input increases without bound. The following limit illustrates this as $x \rightarrow \infty$:

$$\underset{x \rightarrow \infty}{lim} \frac{x}{x^{2}} = \underset{x \rightarrow \infty}{lim} \frac{1}{x} = 0$$

Because the ratio approaches zero, the following expression holds:

$$x = o \left(\right. x^{2} \left.\right) \text{as} x \rightarrow \infty$$

This result indicates that $x$ grows asymptotically more slowly than $x^{2}$ as $x$ increases without bound. More generally, for any two polynomials $x^{a}$ and $x^{b}$ with $a < b$, the following relationship holds:

$$x^{a} = o \left(\right. x^{b} \left.\right) \text{as} x \rightarrow \infty$$

Another example compares a logarithmic function with a power function. Since:

$$\underset{x \rightarrow \infty}{lim} \frac{log ⁡ x}{x} = 0$$

it follows that $log ⁡ x = o \left(\right. x \left.\right)$ as $x \rightarrow \infty$. This result is particularly relevant in algorithm analysis, as it confirms that logarithmic growth is strictly dominated by linear growth.

> The little-o condition at infinity parallels the condition at a finite point: the ratio of the two functions must approach zero as the input increases without bound, rather than as it approaches a fixed value.

## The meaning of $o \left(\right. 1 \left.\right)$

The symbol $o \left(\right. 1 \left.\right)$ represents the class of functions that tend to zero as $x$ approaches a specific point $x_{0}$. In other words, a function $f \left(\right. x \left.\right)$ is said to belong to $o \left(\right. 1 \left.\right)$ when it becomes infinitesimally small compared to a constant, specifically 1, in the limit $x \rightarrow x_{0}$. Formally, we write $f \left(\right. x \left.\right) = o \left(\right. 1 \left.\right)$ as $x \rightarrow x_{0}$ if and only if:

$$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{1} = \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = 0$$

The set of all functions that belong to $o \left(\right. 1 \left.\right)$ can be described as follows:

$$o_{x_{0}} \left(\right. 1 \left.\right) = \left{\right. f : B \left(\right. x_{0} , \delta \left.\right) \backslash \left{\right. x_{0} \left.\right} \rightarrow \mathbb{R} \left|\right. \underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = 0 \left.\right}$$

In practice, this expression is used to describe the concept of $o \left(\right. 1 \left.\right)$ by specifying that:

- The functions considered must be defined on a neighborhood of $x_{0}$, excluding the point $x_{0}$ itself.
- The function must tend to zero as $x$ approaches $x_{0}$.
- The notation $o \left(\right. 1 \left.\right)$ represents the set of all functions that are infinitesimal compared to a constant, specifically to $1$.
- The symbol $B \left(\right. x_{0} , \delta \left.\right)$ denotes an open neighborhood of $x_{0}$ with radius $\delta$, where the function is defined and the limit is taken.

## Example 3

Let us consider the limit:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ \left(\right. x \left.\right)}{x}$$

Using the Taylor expansion of $sin ⁡ \left(\right. x \left.\right)$ near zero, we have:

$$sin ⁡ \left(\right. x \left.\right) = x - \frac{x^{3}}{6} + o \left(\right. x^{3} \left.\right) \text{as} x \rightarrow 0$$

---

Dividing both sides by $x$, we get:

$$\frac{sin ⁡ \left(\right. x \left.\right)}{x} = 1 - \frac{x^{2}}{6} + o \left(\right. x^{2} \left.\right) \text{as} x \rightarrow 0$$

Now observe that both the term $\frac{x^{2}}{6}$ and the remainder $o \left(\right. x^{2} \left.\right)$ tend to zero as $x \rightarrow 0$.

Therefore, as $x \rightarrow 0$ we can write:

$$\frac{sin ⁡ \left(\right. x \left.\right)}{x} = 1 + o \left(\right. 1 \left.\right)$$

> This expression shows that the difference between $\frac{sin ⁡ \left(\right. x \left.\right)}{x}$ and the constant $1$ tends to zero in the limit, and the correction terms are asymptotically smaller than 1.

## Properties

One fundamental property of the little-o notation is that, by definition, if $g \left(\right. x \left.\right) = o \left(\right. f \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$, then the ratio of the two functions tends to zero. In formal terms:

$$\underset{x \rightarrow x_{0}}{lim} \frac{o \left(\right. f \left(\right. x \left.\right) \left.\right)}{f \left(\right. x \left.\right)} = 0$$

---

Multiplying a function by a nonzero constant does not change its asymptotic behavior in little-o notation. For any constant $c \in \mathbb{R}$ and function $g \left(\right. x \left.\right)$, as $x \rightarrow x_{0}$, we have:

$$o \left(\right. c \cdot g \left(\right. x \left.\right) \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$$

$$c \cdot o \left(\right. g \left(\right. x \left.\right) \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$$

> This shows that little-o notation is about relative growth: scaling by a constant factor does not affect the asymptotic behavior near $x_{0}$.

---

Little-o terms also behave predictably under addition. The sum of two little-o terms of the same function remains a little-o term of that function. Formally as $x \rightarrow x_{0}$:

$$o \left(\right. f \left(\right. x \left.\right) \left.\right) + o \left(\right. f \left(\right. x \left.\right) \left.\right) = o \left(\right. f \left(\right. x \left.\right) \left.\right)$$

> This means that adding two functions that are each asymptotically smaller than $f \left(\right. x \left.\right)$ does not affect the fact that the sum is still asymptotically smaller than $f \left(\right. x \left.\right)$.

---

When multiplying a little-o term by a function, the result is a new little-o term where the asymptotic behavior scales accordingly. Specifically, for functions $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$, as $x \rightarrow x_{0}$:

$$f \left(\right. x \left.\right) o \left(\right. g \left(\right. x \left.\right) \left.\right) = o \left(\right. f \left(\right. x \left.\right) g \left(\right. x \left.\right) \left.\right)$$

For example, if $g \left(\right. x \left.\right) = x$ and $o \left(\right. g \left(\right. x \left.\right) \left.\right) = o \left(\right. x \left.\right)$, then multiplying by $f \left(\right. x \left.\right) = x^{2}$ gives:

$$x^{2} \cdot o \left(\right. x \left.\right) = o \left(\right. x^{3} \left.\right)$$

---

Another important property of the little-o notation involves powers of functions. If a function $f \left(\right. x \left.\right)$ is asymptotically smaller than $g \left(\right. x \left.\right)$ as $x \rightarrow x_{0}$, then raising both functions to the same positive power preserves the little-o relationship. Formally, for $a > 0$ if $f \left(\right. x \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$ then $\left[\right. f \left(\right. x \left.\right) \left]\right.^{a} = o \left(\right. \left[\right. g \left(\right. x \left.\right) \left]\right.^{a} \left.\right)$ as $x \rightarrow x_{0}$.

This property demonstrates that the asymptotic behaviour remains consistent when scaled by positive powers. if $f \left(\right. x \left.\right)$ becomes negligible compared to $g \left(\right. x \left.\right)$, then $\left[\right. f \left(\right. x \left.\right) \left]\right.^{a}$ is also negligible compared to $\left[\right. g \left(\right. x \left.\right) \left]\right.^{a}$ as $x \rightarrow x_{0}$. For example, if $f \left(\right. x \left.\right) = o \left(\right. x \left.\right)$ as $x \rightarrow 0$, then as $x \rightarrow x_{0}$ we have:

$$\left[\right. f \left(\right. x \left.\right) \left]\right.^{2} = o \left(\right. x^{2} \left.\right)$$

---

Little-o notation exhibits transitivity. Specifically, if $f \left(\right. x \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$ and $g \left(\right. x \left.\right) = o \left(\right. h \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$, then:

$$f \left(\right. x \left.\right) = o \left(\right. h \left(\right. x \left.\right) \left.\right) \text{as} x \rightarrow x_{0}$$

This result follows directly from the definition. Since both ratios approach zero, their product also approaches zero, and therefore $f \left(\right. x \left.\right) / h \left(\right. x \left.\right) \rightarrow 0$. For example, since $x^{3} = o \left(\right. x^{2} \left.\right)$ and $x^{2} = o \left(\right. x \left.\right)$ as $x \rightarrow 0$, it follows that $x^{3} = o \left(\right. x \left.\right)$ as $x \rightarrow 0$.

> This property enables the composition of chains of asymptotic comparisons: if $f$ grows more slowly than $g$, and $g$ grows more slowly than $h$, then $f$ also grows more slowly than $h$.

---

The composition of two little-o terms reduces to a single term. Specifically, if $h \left(\right. x \left.\right) = o \left(\right. g \left(\right. x \left.\right) \left.\right)$ and $g \left(\right. x \left.\right) = o \left(\right. f \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$, then any function that is little-o of $g$ is also little-o of $f$. In compact notation:

$$o \left(\right. o \left(\right. f \left(\right. x \left.\right) \left.\right) \left.\right) = o \left(\right. f \left(\right. x \left.\right) \left.\right) \text{as} x \rightarrow x_{0}$$

This result follows directly from the transitivity property: if $h = o \left(\right. g \left.\right)$ and $g = o \left(\right. f \left.\right)$, then $h = o \left(\right. f \left.\right)$. For example, since $x^{2} = o \left(\right. x \left.\right)$ as $x \rightarrow 0$, any function that is $o \left(\right. x^{2} \left.\right)$ is also $o \left(\right. x \left.\right)$.

> This property is especially useful for simplifying nested asymptotic expressions, as it ensures that iterated little-o terms can be represented by a single term.

## Distinction Between Little-o and Big-O Notation

Little-o and [Big-O notation](https://algebrica.org/big-o-notation/) are both members of the Landau symbol family, but they describe distinct asymptotic behaviours. Big-O notation provides an upper bound for a function up to a constant multiple, whereas little-o notation imposes a stricter requirement: the ratio of the two functions must approach zero in the limit.

Formally, $f \left(\right. x \left.\right) = O \left(\right. g \left(\right. x \left.\right) \left.\right)$ as $x \rightarrow x_{0}$ if there exist constants $M > 0$ and $\delta > 0$ such that: $\left|\right. f \left(\right. x \left.\right) \left|\right. \leq M \left|\right. g \left(\right. x \left.\right) \left|\right.$ whenever $0 < \left|\right. x - x_{0} \left|\right. < \delta$. This distinction is illustrated by the following example.

As $x \rightarrow 0$, $x^{2} = o \left(\right. x \left.\right)$, which also implies $x^{2} = O \left(\right. x \left.\right)$. However, $x = O \left(\right. x \left.\right)$ does not imply $x = o \left(\right. x \left.\right)$, as demonstrated below:

$$\underset{x \rightarrow 0}{lim} \frac{x}{x} = 1 \neq 0$$

The limit fails to vanish, so the little-o condition is not satisfied. This asymmetry is the heart of the distinction: little-o requires the ratio to go to zero, while Big-O only requires it to stay bounded.

This relationship can be visualised in terms of set inclusion: the set of functions satisfying $f = o \left(\right. g \left.\right)$ is strictly contained within the set of functions satisfying $f = O \left(\right. g \left.\right)$. Every little-o relationship is also a Big-O relationship, but the converse does not hold.

> Little-o notation excludes functions that merely keep pace with $g$, admitting only those that fall strictly behind in the limit.

## Little-o Notation in Taylor Expansions

In [Taylor expansions](https://algebrica.org/taylor-series/), little-o notation provides a rigorous framework for quantifying the error introduced by truncating an infinite series at a finite order. Instead of enumerating each remaining term, the remainder is represented by a single symbol that specifies its precise asymptotic order. Given a function $f \left(\right. x \left.\right)$ that is $n$ times differentiable at $x_{0}$, its Taylor expansion to order $n$ takes the form:

$$f \left(\right. x \left.\right) = f \left(\right. x_{0} \left.\right) + f^{'} \left(\right. x_{0} \left.\right) \left(\right. x - x_{0} \left.\right) + \frac{f^{''} \left(\right. x_{0} \left.\right)}{2 !} \left(\right. x - x_{0} \left.\right)^{2} + \hdots + \frac{f^{\left(\right. n \left.\right)} \left(\right. x_{0} \left.\right)}{n !} \left(\right. x - x_{0} \left.\right)^{n} + o \left(\right. \left(\right. x - x_{0} \left.\right)^{n} \left.\right)$$

The remainder $o \left(\right. \left(\right. x - x_{0} \left.\right)^{n} \left.\right)$ conveys precise asymptotic information. Specifically, the error decreases more rapidly than $\left(\right. x - x_{0} \left.\right)^{n}$ as $x \rightarrow x_{0}$, rendering it negligible compared to the last explicit term in the expansion.

---

The following table presents the Taylor expansions of commonly encountered functions near $x = 0$, each expressed with an explicit little-o remainder:

|  |  |
| --- | --- |
| $$e^{x}$$ | $$1 + x + \frac{x^{2}}{2 !} + \frac{x^{3}}{3 !} + o \left(\right. x^{3} \left.\right)$$ |
| $$sin ⁡ x$$ | $$x - \frac{x^{3}}{6} + o \left(\right. x^{3} \left.\right)$$ |
| $$cos ⁡ x$$ | $$1 - \frac{x^{2}}{2} + \frac{x^{4}}{24} + o \left(\right. x^{4} \left.\right)$$ |
| $$ln ⁡ \left(\right. 1 + x \left.\right)$$ | $$x - \frac{x^{2}}{2} + \frac{x^{3}}{3} + o \left(\right. x^{3} \left.\right)$$ |
| $$\left(\right. 1 + x \left.\right)^{\alpha}$$ | $$1 + \alpha x + \frac{\alpha \left(\right. \alpha - 1 \left.\right)}{2} x^{2} + o \left(\right. x^{2} \left.\right)$$ |

These expansions are particularly effective for evaluating limits involving indeterminate forms. Replacing the original function with its Taylor expansion transforms the problem into an algebraic manipulation, where the little-o remainder vanishes in the limit. The following example demonstrates this approach:

$$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1 - x}{x^{2}} = \underset{x \rightarrow 0}{lim} \frac{\frac{x^{2}}{2} + o \left(\right. x^{2} \left.\right)}{x^{2}} = \frac{1}{2}$$

As $x \rightarrow 0$, the little-o term becomes negligible, allowing the limit to be determined by the leading coefficient.

> In a [Taylor expansion](https://algebrica.org/taylor-series/), the little-o remainder does not simply indicate omitted terms; it specifies the rate at which the approximation improves, thereby anchoring the truncation to a precise asymptotic scale.

taylor remainderasymptotic hierarchynested little-ocompositiontransitivityaddition rulescaling invariancedivergent behaviorinfinitesimalsrelative growthsequenceslimit at infinitylimit at pointbig-O relationlittle-o notationlandau symbolsnegligible growthlimit ratioasymptotic comparisonpropertiescontextsdefinition
