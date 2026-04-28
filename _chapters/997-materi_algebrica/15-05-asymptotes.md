---
layout: chapter
title: "Asymptotes"
chapter: "Limits"
chapter_order: 15
section_order: 5
permalink: /materi-algebrica/limits/asymptotes/
---

## Horizontal asymptotes

Asymptotes are a fundamental concept in mathematical analysis. They are [lines](https://algebrica.org/lines) that a [function](https://algebrica.org/functions) approaches indefinitely without ever reaching, which helps to characterise the function’s behaviour, particularly near infinity or at points of discontinuity. Asymptotes play a fundamental role in the [analysis of functions](https://algebrica.org/analyzing-the-graphs-of-functions/), as their definition inherently relies on the concept of [limits](https://algebrica.org/limits/).

###### In general terms, an asymptote describes the limiting behaviour of a function through a straight line.

---

Consider a real-valued function $y = f \left(\right. x \left.\right)$ defined on an interval $\left[\right. a , + \infty \left[\right.$, $\left]\right. - \infty , b \left]\right.$, or on $\mathbb{R}$. The line with equation $y = L$ is defined as a **horizontal asymptote** of ( f ) if:

$$\underset{x \rightarrow + \infty}{lim} f \left(\right. x \left.\right) = L \text{or} \underset{x \rightarrow - \infty}{lim} f \left(\right. x \left.\right) = L$$

In other words, the function approaches the horizontal line $y = L$ as $x$ tends to positive or negative infinity. Let us consider, for example, the function:

$$y = \frac{x + 1}{x}$$

![](https://algebrica.org/wp-content/uploads/resources/images/asymptotes-1.png)

By computing the limit as $x \rightarrow \pm \infty$, we obtain:

$$\underset{x \rightarrow \pm \infty}{lim} \frac{x + 1}{x} = \underset{x \rightarrow \pm \infty}{lim} \left(\right. 1 + \frac{1}{x} \left.\right) = 1$$

Therefore, the function has a horizontal asymptote along the line $y = 1$. As we can see from the graph of the function, both branches get closer and closer to the line $y = 1$ as $x$ tends to positive or negative infinity. This behavior confirms that $y = 1$ is a horizontal asymptote.

## Vertical asymptotes

Let $y = f \left(\right. x \left.\right)$ be a real-valued function defined on an interval $\left[\right. a , b \left]\right. \backslash x_{0}$, where $x_{0} \in \left[\right. a , b \left]\right.$. We say that the line with equation $x = x_{0}$ is a **vertical asymptote** of $f$ if:

$$\underset{x \rightarrow x_{0}^{-}}{lim} f \left(\right. x \left.\right) = \pm \infty \text{or} \underset{x \rightarrow x_{0}^{+}}{lim} f \left(\right. x \left.\right) = \pm \infty$$

In other words, the function diverges as $x$ approaches $x_{0}$ from the left or the right, getting arbitrarily large in [absolute value](https://algebrica.org/absolute-value). Let us consider, for example, the function:

$$y = \frac{1}{x - 1}$$

![](https://algebrica.org/wp-content/uploads/resources/images/asymptotes-2.png)

We observe that the [rational function](https://algebrica.org/rational-functions) is undefined at $x = 1$, since the denominator becomes zero. To analyze the behavior of $f \left(\right. x \left.\right)$ near $x = 1$, we compute the one-sided limits:

$$\underset{x \rightarrow 1^{-}}{lim} \frac{1}{x - 1} = - \infty \underset{x \rightarrow 1^{+}}{lim} \frac{1}{x - 1} = + \infty$$

This means that the function diverges to $- \infty$ when approaching $1$ from the left, and to $+ \infty$ when approaching from the right. Therefore, the line $x = 1$ is a vertical asymptote of the function.

###### [Rational functions](https://algebrica.org/rational-functions) often have vertical asymptotes at points where the denominator is zero, and the function is undefined. These points correspond to non-removable discontinuities, which are typical of this type of function.

## Oblique asymptotes

Let $y = f \left(\right. x \left.\right)$ be a real-valued function defined on the half-line $\left]\right. - \infty , a \left]\right.$ or $\left[\right. a , + \infty \left[\right.$. We say that the line with equation $y = p x + q$ is an **oblique asymptote** of $f$ if the following condition holds:

$$\underset{x \rightarrow - \infty}{lim} \left[\right. f \left(\right. x \left.\right) - \left(\right. p x + q \left.\right) \left]\right. & = 0 \\ \underset{x \rightarrow + \infty}{lim} \left[\right. f \left(\right. x \left.\right) - \left(\right. p x + q \left.\right) \left]\right. & = 0$$

In other words, the difference between the function and the line $y = p x + q$ tends to zero as $x$ tends to infinity or negative infinity. This means that the function behaves more and more like the line $y = p x + q$ for large values of $x$.

---

The equation of the oblique asymptote $y = p x + q$ for a function $f \left(\right. x \left.\right)$ can be determined by computing two specific limits. The slope $p$ of the asymptote is found by evaluating the following limit:

$$p = \underset{x \rightarrow \pm \infty}{lim} \frac{f \left(\right. x \left.\right)}{x}$$

Once the slope is known, we find the vertical offset $q$ by computing:

$$q = \underset{x \rightarrow \pm \infty}{lim} \left[\right. f \left(\right. x \left.\right) - p x \left]\right.$$

If both limits exist and are finite, the line $y = p x + q$ is the oblique asymptote of the function.

---

Let us consider the function:

$$f \left(\right. x \left.\right) = \frac{x^{2} + 1}{x}$$

![](https://algebrica.org/wp-content/uploads/resources/images/asymptotes-3-1.png)

To determine whether this function has an oblique asymptote as $x \rightarrow \pm \infty$, we begin by analyzing its behavior for large values of $x$. We start by computing the limit:

$$\frac{f \left(\right. x \left.\right)}{x} = \frac{x^{2} + 1}{x^{2}} = 1 + \frac{1}{x^{2}}$$

As $x \rightarrow \pm \infty$, the term $\frac{1}{x^{2}}$ tends to zero, so:

$$\underset{x \rightarrow \pm \infty}{lim} \frac{f \left(\right. x \left.\right)}{x} = 1$$

This tells us that the slope of the asymptote is $p = 1$. Next, we compute the limit of the difference between the function and the linear term $p x$, to find the vertical offset:

$$f \left(\right. x \left.\right) - x = \frac{x^{2} + 1}{x} - x = \frac{x^{2} + 1 - x^{2}}{x} = \frac{1}{x}$$

And again, since $\frac{1}{x} \rightarrow 0$ as $x \rightarrow \pm \infty$, we find:

$$\underset{x \rightarrow \pm \infty}{lim} \left[\right. f \left(\right. x \left.\right) - x \left]\right. = 0$$

Therefore, the function has an oblique asymptote with equation:

$$y = x$$

###### In this example, the oblique asymptote passes through the origin, resulting in $q = 0$, which represents a degenerate case. Generally, the vertical offset $q$ does not need to be zero.

## Example 1

Consider the following function as an additional example, which extends the discussion beyond the degenerate case presented previously:

$$f \left(\right. x \left.\right) = \frac{2 x^{2} - x + 3}{2 x}$$

To determine the oblique asymptote, first compute the slope $p$:

$$p & = \underset{x \rightarrow \pm \infty}{lim} \frac{f \left(\right. x \left.\right)}{x} \\ & = \underset{x \rightarrow \pm \infty}{lim} \frac{2 x^{2} - x + 3}{2 x^{2}} \\ & = 1$$

Next, evaluate the vertical offset $q$:

$$q & = \underset{x \rightarrow \pm \infty}{lim} \left(\right. f \left(\right. x \left.\right) - x \left.\right) \\ & = \underset{x \rightarrow \pm \infty}{lim} \frac{2 x^{2} - x + 3 - 2 x^{2}}{2 x} \\ & = \underset{x \rightarrow \pm \infty}{lim} \frac{- x + 3}{2 x} \\ & = - \frac{1}{2}$$

Therefore, the equation of the oblique asymptote is given by:

$$y = x - \frac{1}{2}$$

## Summary

|  |  |
| --- | --- |
| Horizontal | $$\underset{x \rightarrow \pm \infty}{lim} f \left(\right. x \left.\right) = L$$ |
| Vertical | $$\underset{x \rightarrow x_{0}^{\pm}}{lim} f \left(\right. x \left.\right) = \pm \infty$$ |
| Oblique | $$\underset{x \rightarrow \pm \infty}{lim} \left[\right. f \left(\right. x \left.\right) - \left(\right. p x + q \left.\right) \left]\right. = 0$$ |

## Key properties of asymptotes

Asymptotes come in different forms and follow specific rules that are worth keeping in mind. Some of these properties are immediately intuitive, while others become clear only after working through a few examples. The following points summarize the most important facts about asymptotes and how they relate to a function’s behavior.

- Not all functions possess asymptotes.
- With respect to horizontal asymptotes, several configurations are possible: a function may have none, it may approach the same horizontal line as $x \rightarrow + \infty$ and $x \rightarrow - \infty$, or it may approach two different horizontal lines in the two directions.
- Different types of asymptotes can also occur together. A function may simultaneously exhibit horizontal, vertical, and oblique asymptotes, depending on its behaviour near discontinuities and as the variable tends to infinity.
- Vertical asymptotes typically occur at points where the function is undefined as a result of division by zero. These asymptotes correspond to non-removable discontinuities.
- Horizontal asymptotes characterise the end behaviour of a function as it approaches a constant value when $x$ becomes very large or very small.
- Oblique asymptotes occur when the degree of the numerator exceeds that of the denominator by exactly one, causing the function to approach a slanted line as $x$ approaches infinity.
