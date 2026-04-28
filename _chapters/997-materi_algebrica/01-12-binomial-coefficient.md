---
layout: chapter
title: "Binomial Coefficient"
chapter: "Sets and Numbers"
chapter_order: 1
section_order: 12
permalink: /materi-algebrica/sets-and-numbers/binomial-coefficient/
---

## Introduction

The binomial coefficient denotes the number of ways to select a specific number of items $k$ from a more extensive set of $n$ elements, disregarding the selection order. In combinatorics, the binomial coefficient is denoted using the notation $n$ choose $k .$ The formula for the binomial coefficient is:

$$\left(\right. \frac{n}{k} \left.\right) = \left{\right. \frac{n !}{k ! \left(\right. n - k \left.\right) !} & \text{if} 0 \leq k \leq n \\ 0 & \text{if} k > n$$

- $n$ represents the total number of elements in the set.
- $k$ denotes the number of items to be selected.
- $n !$ and $\left(\right. n - k \left.\right) !$ point represents the [factorial](https://algebrica.org/factorial/) of the [natural numbers](https://algebrica.org/natural-numbers) $n$ and $\left(\right. n - k \left.\right) !$.

To determine the value of the binomial coefficient $\left(\right. \frac{4}{2} \left.\right)$, we count the number of pairs that can be created from a set of four elements. Consider a set $P = \left(\right. p , q , r , s \left.\right)$. The number of subsets formed by two elements is six. These subsets are:

$$\left(\right. p , q \left.\right) \left(\right. p , r \left.\right) \left(\right. p , s \left.\right) \left(\right. q , r \left.\right) \left(\right. q , s \left.\right) \left(\right. r , s \left.\right)$$

Order does not play a role here. The pair $\left(\right. p , q \left.\right)$ and the pair $\left(\right. q , p \left.\right)$ refer to the same selection, so they count as one. This is what separates a combination from a permutation — and it is precisely what the formula accounts for.

The numerator $\frac{n !}{\left(\right. n - k \left.\right) !}$ counts ordered sequences of $k$ elements drawn from a set of $n$: this is the number of permutations. Since order does not matter, each unordered subset appears $k !$ times in that count, once for each way its elements could have been arranged. Dividing by $k !$ removes the overcounting obtaining the expression introduced above:

$$\left(\right. \frac{n}{k} \left.\right) = \frac{n !}{\left(\right. n - k \left.\right) !} \cdot \frac{1}{k !} = \frac{n !}{k ! \left(\right. n - k \left.\right) !}$$

> The binomial coefficient appears in the [binomial theorem](https://algebrica.org/binomial-theorem/), where it represents the coefficients of each term in the expansion of $\left(\right. a + b \left.\right)^{n}$.

## Pascal’s triangle

Pascal’s triangle is a visual representation of binomial coefficients. In short, it is a geometric arrangement of binomial coefficients, which are the coefficients in the expansion of the [binomial](https://algebrica.org/binomials/) $\left(\right. a + b \left.\right)$ raised to any power $n$. The triangle is built using the following rules. The first row contains only 1. Each number in the subsequent rows is the sum of the two numbers directly above it. The outermost elements are always 1. Here are the first six rows:

$$1 \\ 1 1 \\ 1 2 1 \\ 1 3 3 1 \\ 1 4 6 4 1 \\ 1 5 10 10 5 1$$

---

Each element in row $n$ and column $k$ corresponds to the binomial coefficient. For example, the number at $n = 4 , k = 2$ is:

$$\left(\right. \frac{4}{2} \left.\right) = \frac{4 !}{2 ! \left(\right. 4 - 2 \left.\right) !} = \frac{4 !}{2 ! 2 !} = \frac{24}{4} = 6$$

And indeed, in the fourth row, the third number is 6.

---

Pascal’s Triangle satisfies the recurrence relation which directly follows from the triangle’s construction:

$$\left(\right. \frac{n}{k} \left.\right) = \left(\right. \frac{n - 1}{k - 1} \left.\right) + \left(\right. \frac{n - 1}{k} \left.\right)$$

## Fundamental properties of the binomial coefficient

The edge property of the binomial coefficient expresses a basic rule that appears along the borders of [Pascal’s triangle](https://algebrica.org/#pascal-triangle). It states that the coefficients located at the two ends of each row are always equal to one:

$$\left(\right. \frac{n}{0} \left.\right) = \left(\right. \frac{n}{n} \left.\right) = 1$$

For any natural number $n$, there is exactly one possible way to choose none of the available elements, and likewise only one way to choose all of them.

---

The symmetry property is observed when selecting a subset of $k$ elements from a set of $n$ elements, with the number of ways to do this always equal to the number of ways to select the remaining $n - k$ elements. This symmetry is reflected in the equivalence:

$$\left(\right. \frac{n}{k} \left.\right) = \left(\right. \frac{n}{n - k} \left.\right)$$

This principle of symmetric selection is not just a theoretical idea, but a practical tool used in various fields. It’s particularly useful in probability theory, combinatorics, and statistics, where it helps in calculating probabilities, counting possibilities, and analyzing data.

---

The additive property of the binomial coefficient establishes a relationship between consecutive binomial coefficients. If we consider the binomial coefficients $\left(\right. \frac{n}{k} \left.\right)$ and $\left(\right. \frac{n}{k + 1} \left.\right)$, then:

$$\left(\right. \frac{n}{k} \left.\right) + \left(\right. \frac{n}{k + 1} \left.\right) = \left(\right. \frac{n + 1}{k + 1} \left.\right)$$

This property is fundamental in practical applications, as it provides a way to quickly compute the value of the next binomial coefficient, knowing the previous ones. It relies on the definition of the binomial coefficient and its recursive relationship, which allows the expression of a binomial coefficient in terms of preceding binomial coefficients.

---

The [recursive property](https://algebrica.org/#recursion) describes how each binomial coefficient can be derived from those in the previous row of Pascal’s triangle. According to this relationship, every coefficient is obtained as the sum of the two elements positioned directly above it:

$$\left(\right. \frac{n}{k} \left.\right) = \left(\right. \frac{n - 1}{k - 1} \left.\right) + \left(\right. \frac{n - 1}{k} \left.\right)$$

This rule provides a recursive definition for the binomial coefficient and explains the additive structure underlying Pascal’s triangle.

## Notable identities of the binomial coefficient

Beyond the core properties, the binomial coefficient satisfies a number of deeper identities that appear repeatedly across combinatorics, probability, and analysis. Each of them reflects a structural truth about how counting works.

---

The row sum identity states that the sum of all binomial coefficients in
row $n$ of Pascal’s triangle equals $2^{n}$:

$$\sum_{k = 0}^{n} \left(\right. \frac{n}{k} \left.\right) = 2^{n}$$

One way to see why this is true: consider a set of $n$ elements. Each element can either be included in a subset or not, giving two independent choices per element. The total number of subsets is therefore $2^{n}$, and since $\left(\right. \frac{n}{k} \left.\right)$ counts the subsets of exactly $k$ elements, summing over all possible values of $k$ from $0$ to $n$ recovers the same count.

---

The alternating sum identity is a close relative of the row sum, but with alternating signs:

$$\sum_{k = 0}^{n} \left(\right. - 1 \left.\right)^{k} \left(\right. \frac{n}{k} \left.\right) = 0$$

This follows directly from evaluating the binomial theorem at $a = 1$ and $b = - 1$. The result reflects a symmetry between subsets of even and odd size: for any $n \geq 1$, there are exactly as many even-sized subsets of an $n$-element set as there are odd-sized ones.

---

The Vandermonde identity describes what happens when two independent selections are combined into a single one. Given two disjoint groups of $m$ and $n$ elements respectively, the number of ways to choose $r$ elements from the combined group equals:

$$\left(\right. \frac{m + n}{r} \left.\right) = \sum_{k = 0}^{r} \left(\right. \frac{m}{k} \left.\right) \left(\right. \frac{n}{r - k} \left.\right)$$

The reasoning is direct: any selection of $r$ elements from the combined group must draw exactly $k$ elements from the first group and $r - k$ from the second, for some value of $k$ between $0$ and $r$. Each such split contributes $\left(\right. \frac{m}{k} \left.\right) \cdot \left(\right. \frac{n}{r - k} \left.\right)$ combinations, and summing over all valid values of $k$ gives the total. A particularly useful special case arises when $m = n$ and $r = n$:

$$\left(\right. \frac{2 n}{n} \left.\right) = \sum_{k = 0}^{n} \left(\left(\right. \frac{n}{k} \left.\right)\right)^{2}$$

This tells us that the central binomial coefficient — the middle entry of row $2 n$ in Pascal’s triangle — counts the number of ways to select $n$ elements from a group of $2 n$, which can always be decomposed as choosing $k$ from one half and $n - k$ from the other.

---

The upper summation identity relates a binomial coefficient to a sum of coefficients from earlier rows:

$$\sum_{i = 0}^{r} \left(\right. \frac{n + i}{i} \left.\right) = \left(\right. \frac{n + r + 1}{r} \left.\right)$$

The name comes from the shape this identity traces in Pascal’s triangle: a diagonal run of entries whose sum equals a single entry one step to the right and one step down — resembling the blade and handle of a hockey stick. This identity is especially useful when computing cumulative counts that build row by row.

## Generalized binomial coefficient

The definition introduced at the start of this page requires $n$ and $k$ to be natural numbers. This constraint, however, is not as rigid as it appears. The factorial in the numerator can be replaced by a product that makes sense for any real number $\alpha$, leading to the generalized binomial coefficient:

$$\left(\right. \frac{\alpha}{k} \left.\right) = \frac{\alpha \left(\right. \alpha - 1 \left.\right) \left(\right. \alpha - 2 \left.\right) \hdots \left(\right. \alpha - k + 1 \left.\right)}{k !}$$

where $\alpha \in \mathbb{R}$ and $k$ remains a non-negative integer. When $\alpha$ is a natural number and $k \leq \alpha$, this expression reduces to the standard binomial coefficient. When $\alpha$ is not a natural number or when $k > \alpha$ it produces values that are no longer integers, but remain well-defined. This generalization is what allows the [binomial theorem](https://algebrica.org/binomial-theorem/) to extend beyond integer exponents. For $\left|\right. x \left|\right. < 1$, Newton showed that:

$$\left(\right. 1 + x \left.\right)^{\alpha} = \sum_{k = 0}^{\infty} \left(\right. \frac{\alpha}{k} \left.\right) x^{k}$$

Unlike the standard binomial theorem, this sum does not terminate and it is an infinite series. Two cases are worth noting. Taking $\alpha = - 1$ recovers the [geometric series](https://algebrica.org/geometric-series/):

$$\frac{1}{1 + x} = \sum_{k = 0}^{\infty} \left(\right. - 1 \left.\right)^{k} x^{k}$$

Taking $\alpha = \frac{1}{2}$ produces the expansion of $\sqrt{1 + x}$:

$$\sqrt{1 + x} = 1 + \frac{1}{2} x - \frac{1}{8} x^{2} + \frac{1}{16} x^{3} - \hdots$$

an approximation used routinely in physics and engineering when $x$ is small. In both cases, the coefficients are computed directly from the generalized binomial coefficient (the same formula, with $\alpha$ no longer restricted to a whole number).

## Example 1

A research team is made up of 7 scientists and 8 engineers. In how many ways can we form a working group consisting of 3 scientists and 4 engineers? To form the group, we must independently select 3 scientists from 7 and 4 engineers from 8. Since the two selections are independent, the total number of possible combinations is given by:

$$N = \left(\right. \frac{7}{3} \left.\right) \times \left(\right. \frac{8}{4} \left.\right)$$

Now, compute each term:

$$\left(\right. \frac{7}{3} \left.\right) = \frac{7 \times 6 \times 5}{3 \times 2 \times 1} = 35$$

$$\left(\right. \frac{8}{4} \left.\right) = \frac{8 \times 7 \times 6 \times 5}{4 \times 3 \times 2 \times 1} = 70$$

Therefore, by combining the possible selections of scientists and engineers, we obtain:

$$N = 35 \times 70 = 2450$$

> This means that, based on our group of scientists and engineers, we can form 2,450 distinct working teams composed of 3 scientists and 4 engineers.

## Example 2

Let’s now consider the same situation described in Example 1, but with an additional condition: if 2 engineers have a disagreement and cannot be assigned to the same group, how many valid combinations can be formed? We already know that the total number of possible groups, without any restriction, is 2450.

Now, we must exclude the groups that include both of the two engineers who cannot work together. If both conflicting engineers are included in the same group, we have already chosen 2 specific engineers, so we only need to select the remaining 2 engineers from the other 6:

$$\left(\right. \frac{6}{2} \left.\right)$$

At the same time, we still need to select 3 scientists from the 7 available:

$$\left(\right. \frac{7}{3} \left.\right)$$

The number of invalid groups that contain both conflicting engineers is therefore:

$$N_{\text{invalid}} = \left(\right. \frac{7}{3} \left.\right) \times \left(\right. \frac{6}{2} \left.\right)$$

Substituting the values we have:

$$\left(\right. \frac{7}{3} \left.\right) = 35 \left(\right. \frac{6}{2} \left.\right) = 15$$

$$N_{\text{invalid}} = 35 \times 15 = 525$$

Finally, subtract these invalid cases from the total to find the number of valid combinations:

$$N_{\text{valid}} = N_{\text{total}} - N_{\text{invalid}} = 2450 - 525 = 1925$$

There are 1,925 valid combinations if the two conflicting engineers cannot be assigned to the same group.

## Recursion

The binomial coefficient has a natural recursive structure: to count the ways to choose $k$ elements from $n$, it is enough to know the answers to two smaller versions of the same problem.

$$\left(\right. \frac{n}{k} \left.\right) = \left(\right. \frac{n - 1}{k - 1} \left.\right) + \left(\right. \frac{n - 1}{k} \left.\right)$$

The reasoning is combinatorial. Fix one element from the set — call it $x$. Every subset of size $k$ either contains $x$ or it does not. If it does, the remaining $k - 1$ elements must be chosen from the other $n - 1$, giving $\left(\right. \frac{n - 1}{k - 1} \left.\right)$. If it does not, all $k$ elements come from the remaining $n - 1$, giving $\left(\right. \frac{n - 1}{k} \left.\right)$. The two cases are mutually exclusive and together cover all possibilities. For example:

$$\left(\right. \frac{3}{2} \left.\right) = \left(\right. \frac{2}{1} \left.\right) + \left(\right. \frac{2}{2} \left.\right) = 2 + 1 = 3$$

What makes this identity particularly useful in computing is that the recursion is not imposed on the problem from the outside: it is already there in the mathematics. A recursive function does nothing more than follow that structure directly, reducing each call to two smaller ones until it reaches the base cases:

$$\left(\right. \frac{n}{0} \left.\right) = \left(\right. \frac{n}{n} \left.\right) = 1$$

> Note that recursion recalculates the same values multiple times. The computational cost grows quickly with $n ,$ a problem that memoization solves by storing intermediate results as they are computed. This trade-off between simplicity and efficiency is explored in depth in the analysis of [Big O notation](https://algebrica.org/big-o-notation/).

## Foundation of the binomial distribution

The binomial coefficient provides the foundation for the [binomial distribution](https://algebrica.org/binomial-distribution/), which describes the probability of obtaining a specific number of successes in a fixed number of independent trials. If each trial has only two possible outcomes, success with probability $p$ and failure with probability $q = 1 - p$, the probability of observing exactly $x$ successes in $n$ trials is given by:

$$b \left(\right. x ; n , p \left.\right) = \left(\right. \frac{n}{x} \left.\right) p^{x} q^{n - x}$$

This expression combines the binomial coefficient, which counts the number of ways $x$ successes can be arranged across $n$ trials, and the factor $p^{x} q^{n - x}$, which measures the probability of any one such arrangement. Fixing $n$ and $p$, and letting $x$ vary from $0$ to $n$, gives the full distribution, with each outcome weighted by the number of ways it can occur.

central binomial coefficientbinomial theoremupper summationvandermondealternating sumrow sumboundary valuespascal trianglerecursiveadditivesymmetryedgenotation n choose kpermutations relationselection without orderfactorial formulacombinationsidentitiespropertiesdefinition
