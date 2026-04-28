---
layout: chapter
title: "Squeeze Theorem"
chapter: "Limits"
chapter_order: 15
section_order: 3
permalink: /materi-algebrica/limits/squeeze-theorem/
---

## What is the Squeeze Theorem

The **Squeeze Theorem**, also referred to as the Sandwich Theorem, provides a method for determining the [limit](https://algebrica.org/limits/) of a [function](https://algebrica.org/functions/) when direct evaluation is challenging or when the function displays complex oscillatory behaviour near a specific point. This theorem is frequently applied to functions involving [sine and cosine](https://algebrica.org/sine-and-cosine/), particularly when these trigonometric terms exhibit oscillatory behaviour that precludes straightforward limit evaluation, such as:

$$sin ⁡ \left(\right. \frac{1}{x} \left.\right) \text{or} cos ⁡ \left(\right. \frac{1}{x} \left.\right)$$

In these situations, the function is constrained between two other functions with known and equal limits, which facilitates the evaluation of the target limit.

## Statement

Let $x_{0} \in \mathbb{R} \cup \pm \infty$ be a limit point, meaning that every neighborhood of $x_{0}$ contains at least one point of the [domain](https://algebrica.org/determining-the-domain-of-a-function/) different from $x_{0}$. Let $f$, $g$, and $h$ be real-valued functions defined on a neighborhood $I$ of $x_{0}$. Assume that for every $x \in I$, the following [inequality](https://algebrica.org/linear-inequalities/) holds:

$$g \left(\right. x \left.\right) \leq f \left(\right. x \left.\right) \leq h \left(\right. x \left.\right)$$

Also assume that the limits of $f \left(\right. x \left.\right)$ and $h \left(\right. x \left.\right)$ as $x \rightarrow x_{0}$ exist and are equal to some real number $ℓ$:
$$\underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) = \underset{x \rightarrow x_{0}}{lim} h \left(\right. x \left.\right) = ℓ$$

Then, under these hypotheses, the function $g \left(\right. x \left.\right)$ also admits a limit as $x \rightarrow x_{0}$, and that limit is:
$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = ℓ$$

---

In the graph, the black curve representing $f \left(\right. x \left.\right)$ lies entirely between the lower bound $g \left(\right. x \left.\right)$ and the upper bound $h \left(\right. x \left.\right)$. As both bounding functions tend to $ℓ$, the function $f \left(\right. x \left.\right)$ is forced to approach the same limit.

![](https://algebrica.org/wp-content/uploads/resources/images/squeeze-theorem.png)

This demonstrates the geometric intuition underlying the theorem: if a function is bounded above and below by two functions that both converge to the same value, then it must converge to that value.

## Proof of the Squeeze Theorem

Let $\epsilon > 0$ be arbitrary. Our objective is to prove that the function $f \left(\right. x \left.\right)$, which is bounded between $g \left(\right. x \left.\right)$ and $h \left(\right. x \left.\right)$, tends to the same limit $ℓ$ as $x \rightarrow x_{0}$. By assumption, we know that $\underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) = ℓ$. This means that there exists a positive number $\delta_{1}$ such that for every $x$ sufficiently close to $x_{0}$ (specifically, for all $x$ with $0 < \left|\right. x - x_{0} \left|\right. < \delta_{1}$), we have:

$$\left|\right. g \left(\right. x \left.\right) - ℓ \left|\right. < \epsilon \rightarrow ℓ - \epsilon < g \left(\right. x \left.\right) < ℓ + \epsilon$$

Similarly, since $\underset{x \rightarrow x_{0}}{lim} h \left(\right. x \left.\right) = ℓ$, there exists another positive number $\delta_{2}$ such that:

$$\left|\right. h \left(\right. x \left.\right) - ℓ \left|\right. < \epsilon \rightarrow ℓ - \epsilon < h \left(\right. x \left.\right) < ℓ + \epsilon$$

Now let $\delta = min \left(\right. \delta_{1} , \delta_{2} \left.\right)$. Then for every $x$ such that $0 < \left|\right. x - x_{0} \left|\right. < \delta$, both inequalities above are satisfied. But $f \left(\right. x \left.\right)$ is squeezed between $g \left(\right. x \left.\right)$ and $h \left(\right. x \left.\right)$, so:

$$g \left(\right. x \left.\right) \leq f \left(\right. x \left.\right) \leq h \left(\right. x \left.\right)$$

Combining this with the bounds on $g \left(\right. x \left.\right)$ and $h \left(\right. x \left.\right)$, we obtain:

$$ℓ - \epsilon < f \left(\right. x \left.\right) < ℓ + \epsilon \rightarrow \left|\right. f \left(\right. x \left.\right) - ℓ \left|\right. < \epsilon$$

Since this inequality holds for every $\epsilon > 0$, we conclude that:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = ℓ$$

## Example

The subsequent example demonstrates how the theorem is applied to compute the following limit:

$$\underset{x \rightarrow 0}{lim} x \cdot sin ⁡ \left(\right. \frac{1}{x} \left.\right)$$

---

The term $sin ⁡ \left(\right. \frac{1}{x} \left.\right)$ does not admit a limit as $x \rightarrow 0$, since it oscillates indefinitely between $- 1$ and $1$. However, for every [real number](https://algebrica.org/types-of-numbers) $x \neq 0$, the following inequality holds:

$$- 1 \leq sin ⁡ \left(\right. \frac{1}{x} \left.\right) \leq 1$$

Multiplying the entire inequality by $x$, we obtain:

$$- \left|\right. x \left|\right. \leq x \cdot sin ⁡ \left(\right. \frac{1}{x} \left.\right) \leq \left|\right. x \left|\right.$$

---

Indeed, when $x > 0$, the inequality is preserved, while for $x < 0$, the inequality is reversed, but the [absolute value](https://algebrica.org/absolute-value) ensures that the comparison remains symmetric with respect to zero. Now observe that both bounding functions $- \left|\right. x \left|\right.$ and $\left|\right. x \left|\right.$ tend to zero as $x \rightarrow 0$:

$$\underset{x \rightarrow 0}{lim} - \left|\right. x \left|\right. = 0 \underset{x \rightarrow 0}{lim} \left|\right. x \left|\right. = 0$$

Since $f \left(\right. x \left.\right)$ is squeezed between two functions that both approach zero, we can apply the squeeze theorem and conclude that:

$$\underset{x \rightarrow 0}{lim} x \cdot sin ⁡ \left(\right. \frac{1}{x} \left.\right) = 0$$

In many instances, when an oscillating function is multiplied by a power of $x$ that approaches zero, the overall limit is zero. This result arises because the oscillation remains bounded, as demonstrated by sine and cosine functions, which are always confined between $- 1$ and $1$. Conversely, the factor $x^{n}$ approaches zero rapidly enough to dominate the oscillation, causing the entire product to converge to zero.

## Exercises: compute the following limits using the Squeeze Theorem

- $$\text{1}. \underset{x \rightarrow + \infty}{lim} \frac{ln ⁡ \left(\right. 3 + sin ⁡ x \left.\right)}{x^{3}}$$ [solution](https://algebrica.org/#e1)
- $$\text{2}. \underset{x \rightarrow 0}{lim} x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) + 2$$ [solution](https://algebrica.org/#e2)

## Exercise 1

Evaluate the following limit:

$$\underset{x \rightarrow + \infty}{lim} \frac{ln ⁡ \left(\right. 3 + sin ⁡ x \left.\right)}{x^{3}}$$

---

To begin, observe that the sine function is always bounded between $- 1$ and $1$ for all real $x$, so we can write:

$$- 1 \leq sin ⁡ x \leq 1$$

From the previous inequality, we can write:

$$2 \leq 3 + sin ⁡ x \leq 4 \text{for all} x \in \mathbb{R}$$

---

Now, since the [logarithmic function](https://algebrica.org/logarithmic-function/) is strictly [increasing](https://algebrica.org/increasing-and-decreasing-functions/), we have:

$$log ⁡ 2 \leq log ⁡ \left(\right. 3 + sin ⁡ x \left.\right) \leq log ⁡ 4$$

We now divide all parts of the inequality by $x^{3}$ obtaining:

$$\frac{log ⁡ 2}{x^{3}} \leq \frac{ln ⁡ \left(\right. 3 + sin ⁡ x \left.\right)}{x^{3}} \leq \frac{log ⁡ 4}{x^{3}} \forall x > 0$$

Since both bounding functions tend to zero as $x \rightarrow + \infty$, we apply the Squeeze Theorem and obtain:

$$\underset{x \rightarrow + \infty}{lim} \frac{ln ⁡ \left(\right. 3 + sin ⁡ x \left.\right)}{x^{3}} = 0$$

## Exercise 2

Evaluate the following limit:

$$\underset{x \rightarrow 0}{lim} x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) + 2$$

To do so, we start by analyzing the behavior of the function $x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right)$. We know that the cosine function is bounded between $- 1$ and $1$ for all real values:

$$- 1 \leq cos ⁡ \left(\right. \frac{2}{x} \left.\right) \leq 1$$

Multiplying all parts of this inequality by $x^{4}$, which is always non-negative, we get:

$$- x^{4} \leq x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) \leq x^{4}$$

---

Now we take the limit of the left and right bounds as $x \rightarrow 0$:

$$\underset{x \rightarrow 0}{lim} \left(\right. - x^{4} \left.\right) = 0 \underset{x \rightarrow 0}{lim} x^{4} = 0$$

Therefore, by the Squeeze Theorem, we conclude:

$$\underset{x \rightarrow 0}{lim} x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) = 0$$

Now we return to the original expression:

$$\underset{x \rightarrow 0}{lim} \left(\right. x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) + 2 \left.\right)$$

Since:

$$\underset{x \rightarrow 0}{lim} x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) = 0$$

we obtain

$$\underset{x \rightarrow 0}{lim} x^{4} \cdot cos ⁡ \left(\right. \frac{2}{x} \left.\right) + 2 = 0 + 2 = 2$$

## Selected references

- **MIT OpenCourseWare, C. Rodriguez**. [The Squeeze Theorem](https://ocw.mit.edu/courses/18-100a-real-analysis-fall-2020/mit18_100af20_lec8.pdf)
- **University of California, Berkeley, A. Vizeff**. [Limit Laws and the Squeeze Theorem](https://math.berkeley.edu/~avizeff/calculus-I-F22/lecture-4.pdf)
