---
layout: chapter
title: "Analyzing the Graphs of Functions"
chapter: "Functions"
chapter_order: 14
section_order: 11
permalink: /materi-algebrica/functions/analyzing-the-graphs-of-functions/
---

## Introduction

Analyzing the graph of a [function](https://algebrica.org/functions) $y = f \left(\right. x \left.\right)$ allows us to analyze its behavior and key characteristics, providing valuable insights into its mathematical properties. It is a structured process that can be efficiently carried out by following a precise analytical framework, which consists of the following steps.

- Determine the [domain](https://algebrica.org/determining-the-domain-of-a-function/) by identifying the set of real numbers where the function is defined.
- Check for symmetry to see if the function is [even or odd](https://algebrica.org/even-and-odd-functions/).
- Find intercepts by locating points where the graph crosses the $x$-axis and $y$-axis.
- Analyze the sign of the function to determine where it is positive or negative.
- Identify [asymptotes](https://algebrica.org/asymptotes), including horizontal, vertical, or oblique boundaries.
- Use the first derivative to find increasing and decreasing intervals.
- Apply the second derivative to study concavity and detect [inflection points](https://algebrica.org/https:/algebrica.org/maximum-minimum-and-inflection-points/).
- Provide a qualitative representation of the function’s graph.

## Domain

The first step in analyzing a function is to determine its [domain](https://algebrica.org/determining-the-domain-of-a-function/), the set of all real numbers for which the function is well-defined. The domain depends on the type of function being analyzed. Identifying the domain is crucial because it establishes the input values for which the function can be evaluated and graphed. To find the domain, we examine the function’s expression and identify any mathematical constraints that may restrict certain values of $x$.

Let us consider the function $y = x^{3} - 2 x$ as an example. This is a polynomial function of the form:
$$y = a_{n} x^{n} + a_{n - 1} x^{n - 1} + \hdots + a_{1} x + a_{0}$$
where $a_{n} , a_{n - 1} , \ldots , a_{0}$ are real coefficients, and $n$ is the degree of the [polynomial](https://algebrica.org/polynomials).

Since polynomial functions are defined for all real numbers, the domain of this function is $\mathbb{R}$.

## Symmetry

The following step is determining whether the function exhibits [symmetry](https://algebrica.org/even-and-odd-functions/) with respect to the $y$-axis or the origin.

- A function $y = f \left(\right. x \left.\right)$ is classified as [even](https://algebrica.org/even-and-odd-functions/) if it satisfies the condition $f \left(\right. - x \left.\right) = f \left(\right. x \left.\right) \forall x \in D .$ This implies that the graph is symmetric with respect to the $y$-axis.
- A function $y = f \left(\right. x \left.\right)$ is classified as [odd](https://algebrica.org/even-and-odd-functions/) if it satisfies the condition $f \left(\right. - x \left.\right) = - f \left(\right. x \left.\right) \forall x \in D .$ This implies that the graph is symmetric with respect to the origin.

To determine whether the function $f \left(\right. x \left.\right) = x^{3} - 2 x$ is even or odd, we compute $f \left(\right. - x \left.\right)$. Substituting ( -x ) in place of ( x ) we have:
$$f \left(\right. - x \left.\right) & = \left(\right. - x \left.\right)^{3} - 2 \left(\right. - x \left.\right) \\ & = - x^{3} + 2 x$$

---

Calculating $- f \left(\right. x \left.\right)$ we obtain:
 $$- f \left(\right. x \left.\right) & = - \left(\right. x^{3} - 2 x \left.\right) \\ & = - x^{3} + 2 x$$

Since $f \left(\right. - x \left.\right) = - f \left(\right. x \left.\right)$, the function is odd, meaning it is symmetric with respect to the origin.

## Intersections with the cartesian axes

Once the symmetry has been studied, the next step is to determine the points where the function intersects the Cartesian axes. These include:

- $x$-intercepts, obtained by solving $f \left(\right. x \left.\right) = 0$.
- $y$-intercept, given by $f \left(\right. 0 \left.\right)$ when the function is defined at $x = 0$.

To determine the intersection points with the $y$-axis, we set $x = 0$ in the function $f \left(\right. x \left.\right)$. We have:
$$f \left(\right. 0 \left.\right) = 0^{3} - 2 \left(\right. 0 \left.\right) = 0$$

Thus, the function intersects the $y$-axis at the point:
$$\left(\right. 0 , 0 \left.\right)$$

---

Next, to find the intersection points with the $x$-axis, we set $f \left(\right. x \left.\right) = 0$:

$$x^{3} - 2 x = 0$$
$$x \left(\right. x^{2} - 2 \left.\right) = 0$$

Solving for $x$ we have:
$$x = 0 \text{or} x^{2} - 2 = 0$$

From $x^{2} - 2 = 0$, we obtain:
 $$x = \pm \sqrt{2}$$

Thus, the function intersects the $x$-axis at the points:

$$\left(\right. 0 , 0 \left.\right) , \left(\right. \sqrt{2} , 0 \left.\right) , \left(\right. - \sqrt{2} , 0 \left.\right)$$

Therefore, the intersections with the Cartesian axes are:

$y$-axis: $\left(\right. 0 , 0 \left.\right)$
 $x$-axis: $\left(\right. 0 , 0 \left.\right)$, $\left(\right. \sqrt{2} , 0 \left.\right)$, $\left(\right. - \sqrt{2} , 0 \left.\right)$

## Sign analysis

Next, we analyze the sign of the function, identifying the intervals where it is positive and negative. This is done by solving the inequality $f \left(\right. x \left.\right) > 0$ which determines where the function takes positive values. The complementary intervals where $f \left(\right. x \left.\right) < 0$ indicate where the function is negative.

##### In this context, since we will be dealing with inequalities, it is useful to recall how to perform [sign analysis](https://algebrica.org/sign-analysis-in-inequalities/) in inequalities.

To analyze the sign of the function, we determine where $f \left(\right. x \left.\right)$ is positive, negative, or zero by solving the inequality:
 $$x^{3} - 2 x > 0$$

---

Factoring the expression, we have:
$$x \left(\right. x^{2} - 2 \left.\right) > 0$$

From the first factor we obtain:
$$x > 0$$

From the second factor we obtain:
$$x^{2} - 2 > 0 \Rightarrow x > \sqrt{2} x < - \sqrt{2}$$

---

By multiplying the signs of the first and second factors, we obtain (in black) the intervals where the function is positive.

|  | $$- \sqrt{2}$$ | $$0$$ | $$+ \sqrt{2}$$ |  |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

Therefore, the function $x \left(\right. x^{2} - 2 \left.\right)$ is positive for:

$$x \in \left(\right. - \sqrt{2} , 0 \left.\right) \cup \left(\right. + \sqrt{2} , + \infty \left.\right)$$

##### For the sake of completeness, we recall that the sign analysis of a function, as in the given example, requires examining the signs of its individual factors and determining the overall sign for each interval by computing the product of these signs.

---

We then represent on the Cartesian plane the intervals where the function must be located, excluding those in gray.

![](https://algebrica.org/wp-content/uploads/resources/images/graph-functions-1-2.png)

## Asymptotes

Another important step in function analysis is examining its behavior at the boundaries of the domain. This involves computing [limits](https://algebrica.org/limits/) to determine how the function behaves as $x$ approaches the endpoints of its domain or extends toward infinity. By evaluating these limits, we can identify the presence of asymptotes.

- A function $f \left(\right. x \left.\right)$ has a horizontal asymptote if:
  $$\underset{x \rightarrow \pm \infty}{lim} f \left(\right. x \left.\right) = L$$
  where $L$ is a finite real number. In this case, the line $y = L$ represents the asymptote, describing the function’s end behavior.
- A function $f \left(\right. x \left.\right)$ has a vertical asymptote at $x = x_{0}$ if
   $$\underset{x \rightarrow x_{0}^{\pm}}{lim} f \left(\right. x \left.\right) = \pm \infty$$
  In this case, the line $x = a$ represents the asymptote, indicating that the function grows unbounded near $x = a$.
- A function $f \left(\right. x \left.\right)$ has an oblique asymptote of the form $y = m x + q$ if the following limits exist and are finite:
   $$m = \underset{x \rightarrow \pm \infty}{lim} \frac{f \left(\right. x \left.\right)}{x}$$
  $$q = \underset{x \rightarrow \pm \infty}{lim} \left[\right. f \left(\right. x \left.\right) - m x \left]\right.$$

To determine whether horizontal asymptotes exist, we verify whether the following limit exists and is finite:
$$\underset{x \rightarrow \pm \infty}{lim} f \left(\right. x \left.\right)$$

We have:
 $$\underset{x \rightarrow \pm \infty}{lim} \left(\right. x^{3} - 2 x \left.\right) = \pm \infty$$

The function tends to infinity in both directions thus, there are no horizontal asymptotes.

---

Vertical asymptotes occur at points where a function is undefined and its values grow unbounded. The given function, $y = x^{3} - 2 x$ is a polynomial, which is defined for all $x \in \mathbb{R}$. Since polynomials do not have points of discontinuity or infinite limits at finite values of $x$, we conclude that no vertical asymptotes exist.

---

To determine the existence of oblique asymptotes, we compute the slope $m$ using the following limit:

$$m = \underset{x \rightarrow \pm \infty}{lim} \frac{x^{3} - 2 x}{x} = + \infty$$

Since the limit is not finite, oblique asymptotes do not exist.

Therefore, there are no horizontal, vertical, or oblique asymptotes.

## Maximum and minimum points

Now, by analyzing the first derivative, we first identify its domain and zeros, determining where $f^{′} \left(\right. x \left.\right) = 0$. By studying its sign, we establish the intervals where the function is increasing $f^{′} \left(\right. x \left.\right) > 0$ and consequently those where it is decreasing $f^{′} \left(\right. x \left.\right) < 0$.

Next, we identify possible [local maxima and minima](https://algebrica.org/maximum-minimum-and-inflection-points/) by evaluating the critical points of $f \left(\right. x \left.\right)$. Additionally, we examine the function for points of inflection, where the concavity changes, and for points where $f \left(\right. x \left.\right)$ is [not differentiable](https://algebrica.org/points-of-non-differentiability/).

We calculate the first derivative of $f \left(\right. x \left.\right)$ and analyze its sign.
$$f^{′} \left(\right. x \left.\right) = 3 x^{2} - 2$$

For
$$3 x^{2} - 2 > 0 \Rightarrow x < - \sqrt{\frac{2}{3}} x > \sqrt{\frac{2}{3}}$$

---

From this, it follows that $f \left(\right. x \left.\right)$ is increasing for:

$$x < - \sqrt{\frac{2}{3}} \text{or} x > \sqrt{\frac{2}{3}}$$

and decreasing for:

$$- \sqrt{\frac{2}{3}} < x < \sqrt{\frac{2}{3}}$$

---

From the sign analysis, it follows that there is a local minimum at $\sqrt{\frac{2}{3}}$. We now compute the function value at this point:

$$f \left(\right. \sqrt{\frac{2}{3}} \left.\right) & = \left(\left(\right. \sqrt{\frac{2}{3}} \left.\right)\right)^{3} - 2 \left(\right. \sqrt{\frac{2}{3}} \left.\right) \\ & = \frac{2 \sqrt{2}}{3 \sqrt{3}} - 2 \sqrt{\frac{2}{3}} \\ & = \frac{2 \sqrt{6}}{9} - \frac{6 \sqrt{6}}{9} \\ & = \frac{- 4 \sqrt{6}}{9}$$

---

From the sign analysis, it also follows that there is a local maximum at ( -\sqrt{\frac{2}{3}} ). We now compute the function value at this point:

$$f \left(\right. - \sqrt{\frac{2}{3}} \left.\right) & = \left(\left(\right. - \sqrt{\frac{2}{3}} \left.\right)\right)^{3} - 2 \left(\right. - \sqrt{\frac{2}{3}} \left.\right) \\ & = - \frac{2 \sqrt{2}}{3 \sqrt{3}} + 2 \sqrt{\frac{2}{3}} \\ & = - \frac{2 \sqrt{6}}{9} + \frac{6 \sqrt{6}}{9} \\ & = \frac{4 \sqrt{6}}{9}$$

The function has:

- A local maximum at:
   $$x = - \sqrt{\frac{2}{3}} , y = \frac{4 \sqrt{6}}{9}$$
- A local minimum at:
   $$x = \sqrt{\frac{2}{3}} , y = \frac{- 4 \sqrt{6}}{9}$$

## Inflection points

Finally, by analyzing the second derivative $f^{′ ′} \left(\right. x \left.\right)$, we determine the intervals where the graph is concave up $f^{′ ′} \left(\right. x \left.\right) > 0$ or concave down $f^{′ ′} \left(\right. x \left.\right) < 0$.

Now, we identify the [inflection points](https://algebrica.org/maximum-minimum-and-inflection-points/) by analyzing the sign of the second derivative. The second derivative of f(x) is:

$$f^{′ ′} \left(\right. x \left.\right) = 6 x$$

Setting $f^{''} \left(\right. x \left.\right) = 0$, we find the inflection point at $x = 0$. Evaluating $f \left(\right. 0 \left.\right)$, we obtain $y = 0$.

Thus, the inflection point is: $$\left(\right. 0 , 0 \left.\right)$$

## The final graph

At this point, we have all the necessary information to construct a qualitative-quantitative graph of our function, considering its behavior, possible asymptotes, local maxima and minima, and inflection points.

In the given example, we obtain the following graph:

![](https://algebrica.org/wp-content/uploads/resources/images/graph-functions-2.png)

In conclusion, studying the graph of a function requires a structured approach that involves identifying key properties such as domain, symmetry, intercepts, sign analysis, asymptotes, monotonicity, concavity, and critical points. Following these steps systematically ensures a precise and thorough understanding of the function’s behavior.
