---
layout: chapter
title: "Uniform Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 17
permalink: /materi-algebrica/probability-and-statistics/uniform-distribution/
---

## Definition of the uniform distribution

The uniform distribution is one of the simplest continuous distributions to describe. It models a random variable that can take any value within a specified [interval](https://algebrica.org/intervals/), assigning the same probability to all subintervals of equal length. In other words, the possible outcomes are spread evenly across the interval, with no region being more likely than another.

In formal terms, a [continuous random variable](https://algebrica.org/continuous-random-variables/) $X$ is said to follow a uniform distribution on the interval $A = \left[\right. a , b \left]\right.$ if its probability density function is constant on that interval. Formally we have:

$$U \left(\right. x ; a , b \left.\right) = \left{\right. \frac{1}{ b - a } & x \in A \\ 0 & x \notin A$$

For any two subintervals $I_{1}$ and $I_{2}$ contained in $\left[\right. a , b \left]\right.$ and having the same length, the uniform distribution assigns them the same probability. If $w$ denotes the common width of these intervals, then:

$$P \left(\right. I_{1} \left.\right) = P \left(\right. I_{2} \left.\right) = \frac{w}{ b - a }$$

The image shows the density of the uniform distribution over the interval $\left[\right. a , b \left]\right.$. The flat horizontal line indicates that every value between $a$ and $b$ is assigned the same likelihood. The endpoints are drawn as open circles to highlight a key property of continuous distributions: individual points have zero probability and we have:

$$P \left(\right. X = x_{0} \left.\right) = 0$$

![The figure illustrates the density of the uniform distribution on the interval [a,b], showing its constant height and the equal likelihood assigned to all values within the range.](https://algebrica.org/wp-content/uploads/resources/images/uniform-distribution.png "The figure illustrates the density of the uniform distribution on the interval [a,b].")

## Key features

- $$\text{1}. U \left(\right. x ; a , b \left.\right) = \frac{1}{b - a} a \leq x \leq b$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \frac{a + b}{2}$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \frac{\left(\right. b - a \left.\right)^{2}}{12}$$
- $$\text{4}. \sigma = \frac{b - a}{2 \sqrt{3}}$$

##### Each expression highlights a key property of the uniform distribution, showing how probability is spread evenly across the interval and how its mean and variability depend solely on the endpoints $a$ and $b$.

## Mean of the uniform distribution

The [mean](https://algebrica.org/introduction-to-the-mean/), or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/), of a uniform distribution describes the average outcome we would expect from a random variable that can take any value between $a$ and $b$ with equal likelihood. Because the distribution is completely flat over this interval, computing the expected value is straightforward and follows directly from the general definition:

$$\mu = E \left(\right. X \left.\right) = \int_{a}^{b} x U \left(\right. x ; a , b \left.\right) d x$$

For the uniform distribution, the probability density function is constant:

$$f \left(\right. x \left.\right) = \frac{1}{b - a} \text{for} a \leq x \leq b$$

Substituting this expression into the [integral](https://algebrica.org/definite-integrals/) gives us:

$$E \left(\right. X \left.\right) = \int_{a}^{b} x \frac{1}{b - a} d x$$

Since the density does not vary across the interval, we can simply factor it out of the integral:

$$E \left(\right. X \left.\right) = \frac{1}{b - a} \int_{a}^{b} x d x$$

The remaining integral is elementary. The antiderivative of $x$ is $x^{2} / 2$, so evaluating it between $a$ and $b$ yields:

$$\int_{a}^{b} x d x = \frac{b^{2}}{2} - \frac{a^{2}}{2}$$

Plugging this back into the expression for the expected value, we obtain:

$$E \left(\right. X \left.\right) = \frac{1}{b - a} \left(\right. \frac{b^{2} - a^{2}}{2} \left.\right)$$

Noting that $b^{2} - a^{2} = \left(\right. b - a \left.\right) \left(\right. b + a \left.\right)$, the expression simplifies neatly to:

$$E \left(\right. X \left.\right) = \frac{b + a}{2}$$

##### This shows that the mean of the uniform distribution is exactly the midpoint of the interval $\left[\right. a , b \left]\right.$.

## Variance of the uniform distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of a uniform distribution describes how much the random variable is expected to spread out around its mean. While the mean identifies the central value of the interval, the variance quantifies how concentrated or dispersed the outcomes are across $\left[\right. a , b \left]\right.$. Because the uniform distribution assigns the same density to every point in the interval, its variability depends entirely on the length of that interval. Formally, the variance for a continuous random variable is defined as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

Starting from the probability density function of the uniform distribution we have:

$$E \left(\right. X^{2} \left.\right) = \int_{a}^{b} x^{2} U \left(\right. x ; a , b \left.\right) d x$$

For the uniform distribution, the density is:

$$U \left(\right. x ; a , b \left.\right) = \frac{1}{b - a}$$

Substituting this expression into the formula gives:

$$E \left(\right. X^{2} \left.\right) = \int_{a}^{b} x^{2} \frac{1}{b - a} d x = \frac{1}{b - a} \int_{a}^{b} x^{2} d x$$

The integral of $x^{2}$ is straightforward to evaluate:

$$\int_{a}^{b} x^{2} d x = \frac{b^{3}}{3} - \frac{a^{3}}{3}$$

Thus, we have:

$$E \left(\right. X^{2} \left.\right) = \frac{1}{b - a} \left(\right. \frac{b^{3} - a^{3}}{3} \left.\right)$$

Using the [factorization](https://algebrica.org/notable-products/) $b^{3} - a^{3} = \left(\right. b - a \left.\right) \left(\right. b^{2} + a b + a^{2} \left.\right)$, the expression simplifies to:

$$E \left(\right. X^{2} \left.\right) = \frac{b^{2} + a b + a^{2}}{3}$$

We now combine this with the mean of the uniform distribution,

$$E \left(\right. X \left.\right) = \frac{a + b}{2}$$

so that:

$$\left[\right. E \left(\right. X \left.\right) \left]\right.^{2} = \left(\left(\right. \frac{a + b}{2} \left.\right)\right)^{2} = \frac{a^{2} + 2 a b + b^{2}}{4}$$

Putting everything together, we obtain:

$$Var \left(\right. X \left.\right) = \frac{b^{2} + a b + a^{2}}{3} - \frac{a^{2} + 2 a b + b^{2}}{4}$$

After simplifying the expression, the variance reduces to the form:

$$\sigma^{2} = Var \left(\right. X \left.\right) = \frac{\left(\right. b - a \left.\right)^{2}}{12}$$

## Relationship between the uniform and the beta distribution

There is a connection between the uniform distribution and the [beta distribution](https://algebrica.org/beta-distribution) $B \left(\right. x \left.\right) , \alpha , \beta$. When the two shape parameters are both equal to one, that is $\alpha = 1$ and $\beta = 1$, the density of the beta distribution becomes perfectly flat over the interval $\left(\right. 0 , 1 \left.\right)$. The probability density function of a beta distribution is:

$$B \left(\right. x ; \alpha , \beta \left.\right) = \frac{x^{\alpha - 1} \left(\right. 1 - x \left.\right)^{\beta - 1}}{B \left(\right. \alpha , \beta \left.\right)}$$
$$0 < x < 1$$

Setting $\alpha = 1$ and $\beta = 1$ makes both exponents in the numerator equal to zero, and the beta function evaluates to $B \left(\right. 1 , 1 \left.\right) = 1$. As a result, the density simplifies to:

$$B \left(\right. x ; 1 , 1 \left.\right) = 1$$

which is exactly the density of a uniform random variable on $\left(\right. 0 , 1 \left.\right)$.

## Example 1

An industrial cutting machine completes a full cycle in a time that varies slightly due to mechanical tolerances and temperature fluctuations. Measurements show that the cycle time is equally likely to take any value between $4.8$ and $5.4$ seconds. Let $X$ denote the cycle time in seconds, and assume

$$X sim U \left(\right. x ; 4.8 , 5.4 \left.\right)$$

---

Compute the probability that a randomly selected cycle lasts less than 5 seconds. The density of a uniform distribution on $\left(\right. a , b \left.\right)$ is constant and equal to $1 / \left(\right. b - a \left.\right)$. Therefore,

$$P \left(\right. X < 5 \left.\right) = \frac{5 - 4.8}{5.4 - 4.8}$$

We obtain:

$$P \left(\right. X < 5 \left.\right) = \frac{0.2}{0.6} = \frac{1}{3}$$

So the probability is approximately $0.333$.

---

Determine the probability that the cycle time lies between 5.1 and 5.3 seconds. We have:

$$P \left(\right. 5.1 \leq X \leq 5.3 \left.\right) = \frac{5.3 - 5.1}{5.4 - 4.8}$$

This gives:

$$P \left(\right. 5.1 \leq X \leq 5.3 \left.\right) = \frac{0.2}{0.6} = \frac{1}{3}$$

So the probability is again approximately $0.333$.

---

Find the expected cycle time $E \left(\right. X \left.\right)$. For a uniform distribution on $\left(\right. a , b \left.\right)$ we have:

$$E \left(\right. X \left.\right) = \frac{a + b}{2}$$

Thus:

$$E \left(\right. X \left.\right) = \frac{4.8 + 5.4}{2} = \frac{10.2}{2} = 5.1$$

The expected cycle time is 5.1 seconds.

---

Calculate the variance $Var \left(\right. X \left.\right)$. The variance of a uniform distribution on $\left(\right. a , b \left.\right)$ is:

$$Var \left(\right. X \left.\right) = \frac{\left(\right. b - a \left.\right)^{2}}{12}$$

Substituting the values we obtain:

$$Var \left(\right. X \left.\right) = \frac{\left(\right. 5.4 - 4.8 \left.\right)^{2}}{12} = \frac{0.6^{2}}{12} = \frac{0.36}{12} = 0.03$$

So the variance is $0.03$.
