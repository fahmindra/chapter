---
layout: chapter
title: "Algebra of Limits"
chapter: "Limits"
chapter_order: 15
section_order: 2
permalink: /materi-algebrica/limits/algebra-of-limits/
---

## Introduction

The definition of a [limit](https://algebrica.org/limits/) offers a framework for describing how a function $f \left(\right. x \left.\right)$ approaches a specific value near a given point $x_{0}$. This definition by itself is not enough for practical calculations. In most cases, we deal with limits when [functions](https://algebrica.org/functions) are added, multiplied, composed, or divided.

The algebra of limits consists of operational rules derived directly from the formal definition of a limit. These rules illustrate the structural compatibility between limits and standard algebraic operations. To illustrate these rules, it is assumed that $L$ and $M$ are [real numbers](https://algebrica.org/properties-of-real-numbers/) such that:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = L \text{and} \underset{x \rightarrow x_{0}}{lim} g \left(\right. x \left.\right) = M$$

## Limit of a sum

When two functions approach finite values near a point, the sum of the functions approaches the sum of those values. Specifically, if $f \left(\right. x \left.\right)$ remains close to $L$ and $g \left(\right. x \left.\right)$ remains close to $M$, then their combined variation remains close to $L + M$. Formally we have:

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) = L + M$$

This property follows directly from the definition of a limit. For any tolerance around $L + M$, the deviations of $f \left(\right. x \left.\right)$ and $g \left(\right. x \left.\right)$ can be controlled independently to ensure that their combined deviation remains within the prescribed bound. Consider, for instance, the following expressions that involve [sine](https://algebrica.org/sine-function/) and [cosine functions](https://algebrica.org/cosine-function/):

$$f \left(\right. x \left.\right) = \frac{sin ⁡ x}{x} g \left(\right. x \left.\right) = \frac{1 - cos ⁡ x}{x^{2}}$$

and suppose we wish to compute the sum:

$$\underset{x \rightarrow 0}{lim} \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right)$$

Neither function is defined at $x = 0$, which prevents evaluating the limit by direct substitution. Nevertheless, two established results from the analysis provide:

$$\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x} = 1 \underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ x}{x^{2}} = \frac{1}{2}$$

By the sum rule for limits, we conclude:
$$\underset{x \rightarrow 0}{lim} \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) = 1 + \frac{1}{2} = \frac{3}{2}$$

###### This example demonstrates the utility of the sum rule. Instead of analysing the combined expression directly, which would require substantial algebraic manipulation, the rule permits decomposition of the problem into two independent limits, each of which can be addressed separately.

## Limit of a difference

A similar argument applies to subtraction. If two functions approach $L$ and $M$, then their difference approaches $L - M$. The algebraic properties of the real numbers ensure that subtraction is consistent with the limit process.

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left.\right) = L - M$$

The proof parallels that of the sum because subtraction can be interpreted as the addition of the additive inverse. For instance consider the functions:
$$f \left(\right. x \left.\right) = \frac{1 - cos ⁡ x}{x^{2}} g \left(\right. x \left.\right) = \frac{sin^{2} ⁡ x}{2 x^{2}}$$
Suppose we wish to compute the difference:
$$\underset{x \rightarrow 0}{lim} \left(\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left.\right)$$
Neither function is defined at $x = 0$, so direct substitution is not available. However, two known results give:

$$\underset{x \rightarrow 0}{lim} \frac{1 - cos ⁡ x}{x^{2}} = \frac{1}{2} \underset{x \rightarrow 0}{lim} \frac{sin^{2} ⁡ x}{2 x^{2}} = \frac{1}{2}$$

The second result comes from the fact that $\underset{x \rightarrow 0}{lim} \frac{sin ⁡ x}{x} = 1$. Using the difference rule for limits, we find:

$$\underset{x \rightarrow 0}{lim} \left(\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left.\right) = \frac{1}{2} - \frac{1}{2} = 0$$
At first, this result is not obvious from the combined expression:
$$\frac{1 - cos ⁡ x}{x^{2}} - \frac{sin^{2} ⁡ x}{2 x^{2}}$$

because each term approaches $\frac{1}{2}$, and finding their difference takes some careful work. The difference rule, like the sum rule, lets us break the problem into two simpler limits, which makes the calculation easier.

## Limit of a constant multiple

If a function gets closer to a value $L$, multiplying it by a constant will also multiply the limit by that constant. This shows that limits behave linearly. In general, for any real constant $c$, we have:

$$\underset{x \rightarrow x_{0}}{lim} c f \left(\right. x \left.\right) = c L$$

The constant does not affect the limit but just changes the final value by scaling it. To analyse this case, suppose we want to find:

$$\underset{x \rightarrow 0}{lim} 3 \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x}$$

The [logarithmic function](https://algebrica.org/logarithmic-function/) is not defined at $x = 0$, so we can’t use direct substitution. However, a well-known result from analysis tells us:

$$\underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x} = 1$$

Using the constant multiple rule for limits, we get:

$$\underset{x \rightarrow 0}{lim} 3 \cdot \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x} = 3 \cdot 1 = 3$$

## Limit of a product

If two functions get close to certain values near a point, their product also gets close to the product of those values. For example, if $f \left(\right. x \left.\right)$ stays near $L$ and $g \left(\right. x \left.\right)$ stays near $M$, then their product stays near $L \cdot M$:
$$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) \left.\right) = L \cdot M$$

The key idea behind this rule is that both factors can be controlled independently near $x_{0}$, and their combined effect remains bounded. To illustrate this, consider the following functions:
$$f \left(\right. x \left.\right) = \frac{e^{x} - 1}{x} g \left(\right. x \left.\right) = \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x}$$

Neither function is defined at $x = 0$, so direct substitution is not available. However, both are remarkable limits whose values are known:
$$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1}{x} = 1 \underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x} = 1$$

By the product rule, we can now compute the limit of their product:
$$\underset{x \rightarrow 0}{lim} \frac{\left(\right. e^{x} - 1 \left.\right) ln ⁡ \left(\right. 1 + x \left.\right)}{x^{2}} = 1 \cdot 1 = 1$$

## Limit of a quotient

When dividing two or more limits, there is an important restriction to keep in mind. If $g \left(\right. x \left.\right)$ gets close to a nonzero value $M \neq 0$, the quotient acts normally near $x_{0}$. But if the denominator’s limit is zero, the result can become unpredictable. Assuming $M \neq 0$, we have:

$$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = \frac{L}{M}$$

The main idea is that because $g \left(\right. x \left.\right)$ stays close to a nonzero number near $x_{0}$, it does not get close to zero there. This ensures the quotient does not give rise to any division-by-zero issues near $x_{0}$, and the limit behaves as expected. Let’s look at the following functions to analyse this case:

$$f \left(\right. x \left.\right) = \frac{e^{x} - 1}{x} g \left(\right. x \left.\right) = \frac{x^{2} + 1}{x + 1}$$

Suppose we want to find the quotient:
$$\underset{x \rightarrow 0}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)}$$

The function $f \left(\right. x \left.\right)$ is not defined at $x = 0$, so we cannot use direct substitution for the numerator. However we know that:
$$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1}{x} = 1$$

For the denominator, we can use direct substitution because $g \left(\right. x \left.\right)$ is defined at $x = 0$:
$$\underset{x \rightarrow 0}{lim} \frac{x^{2} + 1}{x + 1} = \frac{0 + 1}{0 + 1} = 1$$
Since the denominator’s limit is $M = 1$ and not zero, we can use the quotient rule and get:
$$\underset{x \rightarrow 0}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = \frac{1}{1} = 1$$

###### This example shows why it is important to check that the denominator’s limit is not zero before using the quotient rule. In this case, $g \left(\right. x \left.\right)$ stays close to $1$ near $x = 0$, so there is no risk of dividing by zero.

## Limits of powers and polynomials

When we have repeated multiplication, we encounter limits on powers. If $f \left(\right. x \left.\right)$ approaches $L$, then for any positive integer $n$ we have:

$$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) \left.\right)^{n} = L^{n}$$

This property means you can find the limit of a [polynomial](https://algebrica.org/polynomials/) by plugging the limiting value into the polynomial. Since polynomials use only sums and products, they follow the same rules for limits as these operations. Consider the following function limit:
$$\underset{x \rightarrow 0}{lim} \left(\left(\right. \frac{e^{x} - 1}{x} \left.\right)\right)^{4}$$

The function is not defined at $x = 0$, so direct substitution is not available. However, as a [remarkable limit](https://algebrica.org/remarkable-limits), we know that:

$$\underset{x \rightarrow 0}{lim} \frac{e^{x} - 1}{x} = 1$$

If we use the power rule with $n = 4$, we get:

$$\underset{x \rightarrow 0}{lim} \left(\left(\right. \frac{e^{x} - 1}{x} \left.\right)\right)^{4} = 1^{4} = 1$$

The power rule allows us to avoid expanding the expression directly, which would make the calculation much harder. Instead, once the limit of the base function is known, we just raise that value to the required power in a single step:
$$\left(\left(\right. \frac{e^{x} - 1}{x} \left.\right)\right)^{4} \rightarrow 1^{4} = 1$$

## Limit of a Composition

We now consider the case of function composition. Given two functions $\varphi$ and $f$, their composition $\varphi \left(\right. f \left(\right. x \left.\right) \left.\right)$ consists of applying $f$ first and then $\varphi$ to the result. Suppose that:

$$\underset{x \rightarrow x_{0}}{lim} f \left(\right. x \left.\right) = L$$

Now, if $\varphi$ is continuous at $L$, the limit can be taken through the function:
$$\underset{x \rightarrow x_{0}}{lim} \varphi \left(\right. f \left(\right. x \left.\right) \left.\right) = \varphi \left(\right. L \left.\right)$$

This property connects the algebra of limits with [continuity](https://algebrica.org/continuous-functions/). The continuity of $\varphi$ ensures that small variations in the input near $L$ produce small variations in the output. Without continuity, this rule cannot be guaranteed.

For instance, consider the following function:
$$f \left(\right. x \left.\right) = \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x} \varphi \left(\right. t \left.\right) = \sqrt{t}$$

Suppose we want to find the limit:
$$\underset{x \rightarrow 0}{lim} \sqrt{\frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x}}$$

The function $f \left(\right. x \left.\right)$ is not defined at $x = 0$, so direct substitution is not available. However, this is one of the remarkable limits, and its value is known to be:
$$\underset{x \rightarrow 0}{lim} \frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x} = 1$$

Since $\varphi \left(\right. t \left.\right) = \sqrt{t}$ is continuous at $t = 1$, the limit can be taken through the outer function:
$$\underset{x \rightarrow 0}{lim} \sqrt{\frac{ln ⁡ \left(\right. 1 + x \left.\right)}{x}} = \sqrt{1} = 1$$

###### This example shows that the composition rule reduces the problem to two separate steps: first identifying the limit of the inner function, and then evaluating the outer function at that value. This procedure is justified only if $\varphi$ is continuous at $L = 1$.

## Summary

|  |  |
| --- | --- |
| Sum | $$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) + g \left(\right. x \left.\right) \left.\right) = L + M$$ |
| Difference | $$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) - g \left(\right. x \left.\right) \left.\right) = L - M$$ |
| Constant multiple | $$\underset{x \rightarrow x_{0}}{lim} c f \left(\right. x \left.\right) = c L$$ |
| Product | $$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) \cdot g \left(\right. x \left.\right) \left.\right) = L \cdot M$$ |
| Quotient | $$\underset{x \rightarrow x_{0}}{lim} \frac{f \left(\right. x \left.\right)}{g \left(\right. x \left.\right)} = \frac{L}{M} M \neq 0$$ |
| Power | $$\underset{x \rightarrow x_{0}}{lim} \left(\right. f \left(\right. x \left.\right) \left.\right)^{n} = L^{n}$$ |
| Composition | $$\underset{x \rightarrow x_{0}}{lim} \varphi \left(\right. f \left(\right. x \left.\right) \left.\right) = \varphi \left(\right. L \left.\right) \varphi \text{continuous at} L$$ |

## Selected references

- **University of Washington, M. Greenberg**. [Basic Theorems About Limits](https://sites.math.washington.edu//~greenber/MATH327-LimitTheorems.pdf)
- **University of Wisconsin, J. Robbin**. [Calculus: Lecture Notes](https://people.math.wisc.edu/~angenent/Free-Lecture-Notes/free221.pdf)
- **University of California Davis, J. K. Hunter**. [Limits of Functions](https://www.math.ucdavis.edu/~hunter/m125a/intro_analysis_ch2.pdf)
