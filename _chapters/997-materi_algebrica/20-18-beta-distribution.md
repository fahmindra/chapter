---
layout: chapter
title: "Beta Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 18
permalink: /materi-algebrica/probability-and-statistics/beta-distribution/
---

## Introduction to the beta distribution

The **beta distribution** is a continuous probability distribution defined over the open [interval](https://algebrica.org/intervals/) $\left(\right. 0 , 1 \left.\right)$. It depends on two positive numbers, $\alpha$ and $\beta$, which determine how the curve bends and how its mass is distributed along the interval. Because it only takes values between $0$ and $1$, it is often used to describe random quantities that represent proportions, ratios, or probabilities, situations where the outcomes are naturally limited within these bounds. In formal terms, the beta distribution is defined by the following probability density function:

$$B \left(\right. x ; \alpha , \beta \left.\right) = \frac{x^{\alpha - 1} \left(\right. 1 - x \left.\right)^{\beta - 1}}{B \left(\right. \alpha , \beta \left.\right)} 0 < x < 1$$

where $B \left(\right. \alpha , \beta \left.\right)$ is the beta function, related to the Gamma function by:

$$B \left(\right. \alpha , \beta \left.\right) = \frac{\Gamma \left(\right. \alpha \left.\right) \Gamma \left(\right. \beta \left.\right)}{\Gamma \left(\right. \alpha + \beta \left.\right)}$$

Therefore, the probability density function can also be written explicitly in terms of the Gamma function as:

$$B \left(\right. x ; \alpha , \beta \left.\right) = \frac{\Gamma \left(\right. \alpha + \beta \left.\right)}{\Gamma \left(\right. \alpha \left.\right) \Gamma \left(\right. \beta \left.\right)} x^{\alpha - 1} \left(\right. 1 - x \left.\right)^{\beta - 1}$$

with $B \left(\right. x ; \alpha , \beta \left.\right) = 0$ for $x \notin \left(\right. 0 , 1 \left.\right)$. The gamma function $\Gamma \left(\right. c \left.\right)$ itself is defined, for every $c \in \mathbb{R}^{+} ,$ by the following [integral](https://algebrica.org/definite-integrals/) representation:

$$\Gamma \left(\right. c \left.\right) = \int_{0}^{+ \infty} x^{c - 1} e^{- x} d x$$

The gamma function can be regarded as a continuous extension of the [factorial](https://algebrica.org/factorial/), which is defined only for [natural numbers](https://algebrica.org/natural-numbers), to all positive real values.

## The shape of the beta distribution

The shape of the beta distribution depends on the values of its parameters $\alpha$ and $\beta$. Depending on their magnitude, the distribution can take various forms: unimodal, U-shaped, or [monotonic](https://algebrica.org/increasing-and-decreasing-functions/). The distribution reaches its mode at the point

$$x_{0} = \frac{\alpha - 1}{\alpha + \beta - 2}$$

- If $\alpha > 1$ and $\beta > 1$, the distribution has a mode at $x_{0}$, corresponding to a maximum point of the density function.
- If $\alpha < 1$ and $\beta < 1$, the function has a [minimum](https://algebrica.org/maximum-minimum-and-inflection-points/) at the same point.
- In all other parameter combinations, the distribution is monotonic.
- When $\alpha = \beta$, the distribution is [symmetric](https://algebrica.org/even-and-odd-functions/) with respect to the vertical line $x = x_{0} = \frac{1}{2}$.

---

The figure illustrates one of the possible shapes of the beta distribution when both parameters $\alpha$ and $\beta$ are less than 1 and equal to each other. In this configuration, the distribution takes on a characteristic U-shaped form, with the density approaching infinity near the boundaries of the interval $\left(\right. 0 , 1 \left.\right)$. It is possible to observe a minimum point located at $x = x_{0}$, corresponding to the lowest value of the probability density within the [domain](https://algebrica.org/determining-the-domain-of-a-function/).

![Typical U-shaped form of the Beta distribution with α < 1, β < 1, and α = β.
](https://algebrica.org/wp-content/uploads/resources/images/beta-distribution-1.png "Typical U-shaped form of the Beta distribution with α < 1, β < 1, and α = β.")

An interesting case occurs when the two parameters are equal, that is $\alpha = \beta$, and both are greater than $1$. In this situation, the beta distribution becomes symmetric with respect to the vertical line $x = \frac{1}{2}$ and takes on a unimodal (that is, a single-peaked curve), bell-shaped form with a single central peak. As the values of $\alpha$ and $\beta$ increase, the curve becomes progressively narrower and increasingly similar to a [normal distribution](https://algebrica.org/normal-distribution) centered around $x = 0.5$.

![As α and β increase, the Beta distribution approaches a normal curve centered at 0.5.](https://algebrica.org/wp-content/uploads/resources/images/beta-distribution-2.png "As α and β increase, the Beta distribution approaches a normal curve centered at 0.5.")

To be more precise, this is an [asymptotic](https://algebrica.org/asymptotes/) approximation that holds for large values of $\alpha$ and $\beta$. For sufficiently large parameters, the Beta distribution can be approximated by a normal distribution with:

$$\mu = \frac{\alpha}{\alpha + \beta}$$
$$\sigma^{2} = \frac{\alpha \beta}{\left(\right. \alpha + \beta \left.\right)^{2} \left(\right. \alpha + \beta + 1 \left.\right)}$$

In the symmetric case, where $\alpha = \beta = k$ we have:

$$\mu = \frac{1}{2} \sigma^{2} = \frac{1}{8 \left(\right. 2 k + 1 \left.\right)} \approx \frac{1}{16 k}$$

Therefore, as $k \rightarrow \infty$:

$$B \left(\right. x ; k , k \left.\right) \approx \mathcal{N} \left(\right. \frac{1}{2} , \frac{1}{8 \left(\right. k + 1 \left.\right)} \left.\right)$$

## Key features

- $$\text{1}. f \left(\right. x \left.\right) = \frac{x^{\alpha - 1} \left(\right. 1 - x \left.\right)^{\beta - 1}}{B \left(\right. \alpha , \beta \left.\right)} 0 \leq x \leq 1$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \frac{\alpha}{\alpha + \beta}$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \frac{\alpha \beta}{\left(\right. \alpha + \beta \left.\right)^{2} \left(\right. \alpha + \beta + 1 \left.\right)}$$
- $$\text{4}. \sigma = \sqrt{\frac{\alpha \beta}{\left(\right. \alpha + \beta \left.\right)^{2} \left(\right. \alpha + \beta + 1 \left.\right)}}$$

##### Each expression highlights a key property of the Beta distribution, showing how its shape depends on the parameters $\alpha$ and $\beta$, and how its mean and variability reflect the balance between these two shape parameters.

## Mean of the beta distribution

The [mean](https://algebrica.org/introduction-to-the-mean/), or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/), of a beta distribution represents the average value of a random variable defined on the interval $\left(\right. 0 , 1 \left.\right)$, depending on the shape parameters $\alpha$ and $\beta$. Formally, the mean is obtained from the general definition of the expected value:

$$\mu = E \left(\right. X \left.\right) = \int_{0}^{1} x B \left(\right. x ; \alpha , \beta \left.\right) d x$$

Substituting the probability density function of the Beta distribution we have:

$$E \left(\right. X \left.\right) = \int_{0}^{1} x \frac{x^{\alpha - 1} \left(\right. 1 - x \left.\right)^{\beta - 1}}{B \left(\right. \alpha , \beta \left.\right)} d x$$

which simplifies to:

$$E \left(\right. X \left.\right) = \frac{1}{B \left(\right. \alpha , \beta \left.\right)} \int_{0}^{1} x^{\alpha} \left(\right. 1 - x \left.\right)^{\beta - 1} d x$$

Recognizing that the integral on the right-hand side is itself the Beta function
$B \left(\right. \alpha + 1 , \beta \left.\right)$, we obtain:

$$E \left(\right. X \left.\right) = \frac{B \left(\right. \alpha + 1 , \beta \left.\right)}{B \left(\right. \alpha , \beta \left.\right)}$$

Using the identity that relates the Beta and Gamma functions we obtain:

$$B \left(\right. \alpha , \beta \left.\right) = \frac{\Gamma \left(\right. \alpha \left.\right) \Gamma \left(\right. \beta \left.\right)}{\Gamma \left(\right. \alpha + \beta \left.\right)}$$

Therefore, the mean can be expressed as:

$$E \left(\right. X \left.\right) = \frac{\alpha}{\alpha + \beta}$$

##### Hence, the mean of the Beta distribution depends only on the two shape parameters and expresses the balance between them.

## Variance of the beta distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of the beta distribution measures how much the random variable is expected to vary around its mean value. While the mean describes the central tendency of the distribution, the variance quantifies its spread — that is, how concentrated or dispersed the possible outcomes are within the interval $\left(\right. 0 , 1 \left.\right)$. Formally, the variance is defined as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

Starting from the probability density function of the beta distribution:

$$B \left(\right. x ; \alpha , \beta \left.\right) = \frac{x^{\alpha - 1} \left(\right. 1 - x \left.\right)^{\beta - 1}}{B \left(\right. \alpha , \beta \left.\right)}$$

the expression can be rewritten as:

$$E \left(\right. X^{2} \left.\right) & = \int_{0}^{1} x^{2} f \left(\right. x ; \alpha , \beta \left.\right) d x \\ & = \frac{1}{B \left(\right. \alpha , \beta \left.\right)} \int_{0}^{1} x^{\alpha + 1} \left(\right. 1 - x \left.\right)^{\beta - 1} d x \\ & = \frac{B \left(\right. \alpha + 2 , \beta \left.\right)}{B \left(\right. \alpha , \beta \left.\right)}$$

Substituting this expression and the mean into the formula gives:

$$\sigma^{2} = \frac{B \left(\right. \alpha + 2 , \beta \left.\right)}{B \left(\right. \alpha , \beta \left.\right)} - \left(\left(\right. \frac{\alpha}{\alpha + \beta} \left.\right)\right)^{2}$$

Using the relationship between the beta and gamma functions:

$$B \left(\right. \alpha , \beta \left.\right) = \frac{\Gamma \left(\right. \alpha \left.\right) \Gamma \left(\right. \beta \left.\right)}{\Gamma \left(\right. \alpha + \beta \left.\right)}$$

we obtain the simplified expression for the variance:

$$\sigma^{2} = \frac{\alpha \beta}{\left(\right. \alpha + \beta \left.\right)^{2} \left(\right. \alpha + \beta + 1 \left.\right)}$$

##### When $\alpha$ and $\beta$ increase together, the variance decreases, causing the distribution to become more concentrated around its mean.

## Relationship between the beta and uniform distribution

The [uniform distribution](https://algebrica.org/uniform-distribution/) can be regarded as a special case of the beta distribution. When both parameters are equal to one, that is $\alpha = \beta = 1$, the probability density function of the beta distribution becomes constant over the interval $\left(\right. 0 , 1 \left.\right)$. In the general case, the continuous uniform distribution defined over an interval $\left(\right. a , b \left.\right)$ is given by:

$$f \left(\right. x \left.\right) = \left{\right. \frac{1}{b - a} & a < x < b \\ 0 & \text{otherwise}$$

For $a = 0$ and $b = 1$, this expression reduces to $f \left(\right. x \left.\right) = 1$, which corresponds exactly to the $B \left(\right. 1 , 1 \left.\right)$ distribution. In this case, the two parameters of the beta distribution take the values $\alpha = 1$ and $\beta = 1$, producing a constant probability density across the interval $0 , 1$.
