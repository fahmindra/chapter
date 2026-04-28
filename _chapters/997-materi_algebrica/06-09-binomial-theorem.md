---
layout: chapter
title: "Binomial Theorem"
chapter: "Polynomials"
chapter_order: 6
section_order: 9
permalink: /materi-algebrica/polynomials/binomial-theorem/
---

## Statement

The binomial theorem asserts that for any positive integer $n$, the expression $\left(\right. a + b \left.\right)^{n}$ can be expanded as a finite sum of $n + 1$ terms. Each term consists of a binomial coefficient multiplied by a [power](https://algebrica.org/powers/) of $a$ and a power of $b$:
$$\left(\right. a + b \left.\right)^{n} = \left(\right. \frac{n}{0} \left.\right) a^{n} b^{0} + \left(\right. \frac{n}{1} \left.\right) a^{n - 1} b^{1} + \ldots + \left(\right. \frac{n}{n - 1} \left.\right) a^{1} b^{n - 1} + \left(\right. \frac{n}{n} \left.\right) a^{0} b^{n}$$

---

The formula is composed of the following elements:

- $n$, the exponent term, is a positive integer $n \in \mathbb{N}^{+}$.
- $a$ is raised to a decreasing power, from $n$ to $0$.
- $b$ is raised to an increasing power from $0$ to $n$.
- The term $\left(\right. \frac{n}{k} \left.\right)$ is the [binomial coefficient](https://algebrica.org/binomial-coefficient), where $k$ takes values between $0$ and $n$.

###### The coefficients $\left(\right. \frac{n}{k} \left.\right)$ appearing in the expansion correspond exactly to the entries of the $n$-th row of [Pascal’s Triangle](https://algebrica.org/binomial-coefficient/). The symmetry $\left(\right. \frac{n}{k} \left.\right) = \left(\right. \frac{n}{n - k} \left.\right)$ reflects the fact that choosing $k$ elements from $n$ is equivalent to leaving out $n - k$.

---

In its compact form, the binomial theorem can be expressed as the summation of $n + 1$ terms:

$$\left(\right. a + b \left.\right)^{n} = \sum_{k = 0}^{n} \left(\right. \frac{n}{k} \left.\right) a^{n - k} b^{k}$$

## Binomial coefficient

The [binomial coefficient](https://algebrica.org/binomial-coefficient/) represents the number of ways to choose $k$ items from a larger set of $n$ elements, ignoring the order of selection. In combinatorics, it is commonly referred to as n choose k, and is denoted by the notation:

$$\left(\right. \frac{n}{k} \left.\right) = \left{\right. \frac{n !}{k ! \left(\right. n - k \left.\right) !} & 0 \leq k \leq n \\ 0 & n < k$$

- $n , k \in \mathbb{N}$.
- $n$ is the total number of elements in the set.
- $k$ is the number of items to be selected.
- $n !$ and $\left(\right. n - k \left.\right) !$ are the [factorials](https://algebrica.org/factorial) of the [natural numbers](https://algebrica.org/natural-numbers) $n$ and $n - k$ respectively.

## Proof

There are two standard proofs of the theorem. The first is based on a combinatorial argument. The expansion of $\left(\right. a + b \left.\right)^{n}$ can be viewed as the product of $n$ identical factors:

$$\left(\right. a + b \left.\right)^{n} = \underset{n \text{factors}}{\underbrace{\left(\right. a + b \left.\right) \left(\right. a + b \left.\right) \hdots \left(\right. a + b \left.\right)}}$$

Each term in the expanded product results from selecting either $a$ or $b$ from each factor. A term of the form $a^{n - k} b^{k}$ occurs when $b$ is chosen from exactly $k$ of the $n$ factors, and $a$ from the remaining $n - k$. The number of such selections is $\left(\right. \frac{n}{k} \left.\right)$, which enumerates the $k$-element subsets of the $n$ factors. Summing over all possible values of $k$ from $0$ to $n$ establishes the theorem.

---

The second proof uses [mathematical induction](https://algebrica.org/principle-of-mathematical-induction/) on $n$. For $n = 1$, the identity becomes $\left(\right. a + b \left.\right)^{1} = a + b$, which is clearly valid. Assume the theorem holds for some integer $n \geq 1$. Multiplying both sides of the inductive hypothesis by $\left(\right. a + b \left.\right)$ yields:

$$\left(\right. a + b \left.\right)^{n + 1} & = \left(\right. a + b \left.\right) \sum_{k = 0}^{n} \left(\right. \frac{n}{k} \left.\right) a^{n - k} b^{k} \\ & = \sum_{k = 0}^{n} \left(\right. \frac{n}{k} \left.\right) a^{n - k + 1} b^{k} + \sum_{k = 0}^{n} \left(\right. \frac{n}{k} \left.\right) a^{n - k} b^{k + 1}$$

Re-index the second sum by letting $j = k + 1$ and separate the edge terms as follows:

$$= a^{n + 1} + \sum_{k = 1}^{n} \left[\right. \left(\right. \frac{n}{k} \left.\right) + \left(\right. \frac{n}{k - 1} \left.\right) \left]\right. a^{n + 1 - k} b^{k} + b^{n + 1}$$

Apply Pascal’s identity, $\left(\right. \frac{n}{k} \left.\right) + \left(\right. \frac{n}{k - 1} \left.\right) = \left(\right. \frac{n + 1}{k} \left.\right)$, to the interior terms to obtain:

$$\left(\right. a + b \left.\right)^{n + 1} = \sum_{k = 0}^{n + 1} \left(\right. \frac{n + 1}{k} \left.\right) a^{n + 1 - k} b^{k}$$

This expression is the binomial theorem for $n + 1$, which completes the induction.

## Example 1

Expand $\left(\right. x + 2 \left.\right)^{4}$ using the binomial theorem, with $a = x$, $b = 2$, and $n = 4$.

Applying the formula:

$$\left(\right. x + 2 \left.\right)^{4} = \sum_{k = 0}^{4} \left(\right. \frac{4}{k} \left.\right) x^{4 - k} \cdot 2^{k}$$

Computing each term:

$$k = 0 & \left(\right. \frac{4}{0} \left.\right) x^{4} \cdot 2^{0} = x^{4} \\ k = 1 & \left(\right. \frac{4}{1} \left.\right) x^{3} \cdot 2^{1} = 8 x^{3} \\ k = 2 & \left(\right. \frac{4}{2} \left.\right) x^{2} \cdot 2^{2} = 24 x^{2} \\ k = 3 & \left(\right. \frac{4}{3} \left.\right) x^{1} \cdot 2^{3} = 32 x \\ k = 4 & \left(\right. \frac{4}{4} \left.\right) x^{0} \cdot 2^{4} = 16$$

Summing all terms we obtain:
$$\left(\right. x + 2 \left.\right)^{4} = x^{4} + 8 x^{3} + 24 x^{2} + 32 x + 16$$

## Example 2

For a binomial involving subtraction, the binomial theorem applies with $b$ replaced by a negative value. The signs alternate in the expansion because $\left(\right. - 1 \left.\right)^{k}$ yields a positive value for even $k$ and a negative value for odd $k$. The expansion of $\left(\right. x - 1 \left.\right)^{5}$, where $a = x$, $b = - 1$, and $n = 5$, is as follows:

$$\left(\right. x - 1 \left.\right)^{5} = \sum_{k = 0}^{5} \left(\right. \frac{5}{k} \left.\right) x^{5 - k} \cdot \left(\right. - 1 \left.\right)^{k}$$

Each term in the expansion is computed as follows:

$$k = 0 & \left(\right. \frac{5}{0} \left.\right) x^{5} \cdot \left(\right. - 1 \left.\right)^{0} = x^{5} \\ k = 1 & \left(\right. \frac{5}{1} \left.\right) x^{4} \cdot \left(\right. - 1 \left.\right)^{1} = - 5 x^{4} \\ k = 2 & \left(\right. \frac{5}{2} \left.\right) x^{3} \cdot \left(\right. - 1 \left.\right)^{2} = 10 x^{3} \\ k = 3 & \left(\right. \frac{5}{3} \left.\right) x^{2} \cdot \left(\right. - 1 \left.\right)^{3} = - 10 x^{2} \\ k = 4 & \left(\right. \frac{5}{4} \left.\right) x^{1} \cdot \left(\right. - 1 \left.\right)^{4} = 5 x \\ k = 5 & \left(\right. \frac{5}{5} \left.\right) x^{0} \cdot \left(\right. - 1 \left.\right)^{5} = - 1$$

Summing all terms we have:

$$\left(\right. x - 1 \left.\right)^{5} = x^{5} - 5 x^{4} + 10 x^{3} - 10 x^{2} + 5 x - 1$$

## Selected resources

- **University of Connecticut, W. Abikoff**. [The Binomial Theorem](https://www2.math.uconn.edu/~abikoff/math2142s11/binomial.pdf)
- **University of California S. Barbara, H. McGahagan**. [Induction and the Binomial Theorem](https://web.math.ucsb.edu/~helena/teaching/math8/handouts/induction.pdf)
- **MIT,D. Karger, N. Lynch**. [Binomial Coefficients and Identities](https://courses.csail.mit.edu/6.042/past-devel/archive/spring00/archive/lectures/L16.pdf)
- **Harvard University, C. Wang**. [Binomial Theorem and Combinatorial Proofs](https://people.math.harvard.edu/~cmwang/teaching/55/3-5sol.pdf)
