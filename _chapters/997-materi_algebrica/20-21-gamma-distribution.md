---
layout: chapter
title: "Gamma Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 21
permalink: /materi-algebrica/probability-and-statistics/gamma-distribution/
---

## Introduction to the gamma distribution

The gamma distribution is a continuous probability distribution defined on the positive half-line. It is used to model waiting times, event durations, and phenomena where independent contributions accumulate over time. It originates from the gamma function, defined as

$$\Gamma \left(\right. \alpha \left.\right) = \int_{0}^{\infty} x^{ \alpha - 1} e^{- x} d x$$

which extends the [factorial](https://algebrica.org/factorial/) to the real [domain](https://algebrica.org/determining-the-domain-of-a-function/) through the identity $\Gamma \left(\right. n \left.\right) = \left(\right. n - 1 \left.\right) !$ for every positive [integer](https://algebrica.org/integers/) $n$. In general, a [continuous random variable](https://algebrica.org/continuous-random-variables/) $X$ is said to follow a gamma distribution with parameters $\alpha$ and $\beta$ when its probability density function is given by

$$G \left(\right. x ; \alpha , \beta \left.\right) = \left{\right. \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} & x > 0 \\ 0 & x \leq 0$$

- $\alpha$ is the shape parameter: it controls how quickly the density rises near the origin and determines the degree of skewness. Larger values make the distribution more symmetric and shift the peak to the right.
- $\beta$ is the scale parameter: it stretches the distribution horizontally. Increasing $\beta$ produces longer average waiting times and a broader spread.

The support of the distribution is the positive half-line, reflecting the fact that it models durations, waiting times, or other quantities that cannot take negative values. The interaction between $\alpha$ and $\beta$ shapes the overall behavior: $\alpha$ governs the internal structure, while $\beta$ sets the scale.

![Plot of the gamma distribution for different parameter values.](https://algebrica.org/wp-content/uploads/resources/images/gamma-distribution.png "Plot of the gamma distribution for different parameter values.")

When $\alpha$ grows beyond $1$, the gamma density no longer peaks at zero but forms a maximum at a positive value of $x$. As $\alpha$ increases, this peak moves to the right and the overall shape becomes smoother and less skewed.

---

As with any continuous distribution, the total area under the density curve must equal 1. This is the same principle that holds for the [normal distribution](https://algebrica.org/normal-distribution/), whose density [integrates](https://algebrica.org/definite-integrals/) to $1$ over the entire real line. The gamma distribution follows the same requirement: its density is defined so that the integral over the positive half-line is exactly equal to $1$. Formally, we have

$$\int_{0}^{+ \infty} \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} d x = 1$$

Solving the integral by applying the [substitution](https://algebrica.org/integration-by-substitution/) $x = \beta t$, which gives $d x = \beta d t$, we can rewrite the expression as:

$$\int_{0}^{+ \infty} \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \left(\right. \beta t \left.\right)^{\alpha - 1} e^{- t} \beta d t$$

After collecting the powers of $\beta$, this becomes:

$$\frac{1}{\Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} t^{\alpha - 1} e^{- t} d t$$

The integral on the right-hand side is exactly the definition of the gamma function, so we obtain

$$\frac{1}{\Gamma \left(\right. \alpha \left.\right)} \cdot \Gamma \left(\right. \alpha \left.\right) = 1$$

## Key features

- $$\text{1}. f \left(\right. x \left.\right) = \frac{1}{\Gamma \left(\right. \alpha \left.\right) \beta^{\alpha}} x^{\alpha - 1} e^{- x / \beta} x > 0$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \alpha \beta$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \alpha \beta^{2}$$
- $$\text{4}. \sigma = \beta \sqrt{\alpha}$$

##### Each expression highlights a key property of the Gamma distribution, whose density is defined through the Gamma function $\Gamma \left(\right. \alpha \left.\right)$. Its mean and variability depend jointly on the shape parameter $\alpha$ and the scale parameter $\beta$, determining how the distribution models waiting times and positively skewed processes.

## Expected value of the gamma distribution

As introduced in the section on continuous random variables, the [expected value of a continuous random variable](https://algebrica.org/mean-or-expected-value-of-a-random-variable/) describes the central tendency of its distribution and is defined as

$$\mu = E \left(\right. X \left.\right) = \int_{- \infty}^{+ \infty} x f \left(\right. x \left.\right) d x$$

This general formula applies to any continuous distribution, where $f \left(\right. x \left.\right)$ denotes the probability density function of the random variable $X$. For the gamma distribution with shape parameter $\alpha$ and scale parameter $\beta$, the density is:

$$f \left(\right. x ; \alpha , \beta \left.\right) = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} x > 0$$

so the expected value is computed as:

$$\mu = E \left(\right. X \left.\right) = \int_{0}^{+ \infty} x \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} d x$$

Combining the powers of $x$, we obtain:

$$E \left(\right. X \left.\right) = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} x^{\alpha} e^{- x / \beta} d x$$

To simplify the integral, we apply the change of variable $x = \beta t$, which gives $d x = \beta d t$. Substituting, we have:

$$E \left(\right. X \left.\right) = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} \left(\right. \beta t \left.\right)^{\alpha} e^{- t} \beta d t$$

Collecting the powers of $\beta$:

$$E \left(\right. X \left.\right) & = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} \left(\right. \beta t \left.\right)^{\alpha} e^{- t} , \beta , d t \\ & = \frac{\beta^{\alpha} \beta}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} t^{\alpha} e^{- t} d t \\ & = \frac{\beta}{\Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} t^{\alpha} e^{- t} d t$$

The remaining integral is recognized as the gamma function evaluated at $\alpha + 1$:

$$\int_{0}^{+ \infty} t^{\alpha} e^{- t} d t = \Gamma \left(\right. \alpha + 1 \left.\right)$$

Using the identity $\Gamma \left(\right. \alpha + 1 \left.\right) = \alpha \Gamma \left(\right. \alpha \left.\right)$, we find

$$\mu = \alpha \beta$$

This shows that the mean of the gamma distribution depends on both parameters: $\alpha$ shapes how the mass is distributed along the positive axis, while $\beta$ stretches the distribution horizontally, and their product gives the average value of the variable.

---

The gamma distribution is sometimes written in an alternative form that uses a rate parameter instead of a scale parameter. In that case, the density is expressed as:

$$f \left(\right. x ; \alpha , \beta \left.\right) = \frac{\beta^{\alpha}}{\Gamma \left(\right. \alpha \left.\right)} , x^{\alpha - 1} e^{- \beta x} x > 0$$

where $\beta$ now plays the role of the rate which is the inverse of the scale. Under this parametrization, the expected value becomes:

$$E \left(\right. X \left.\right) = \frac{\alpha}{\beta}$$

##### The two expressions for the mean are completely consistent: with a scale parameter the mean is $\alpha \beta$, while with a rate parameter it is $\alpha / \beta$. The difference comes solely from the choice of parametrization, not from the distribution itself.

## Variance of the gamma distribution

The variance of the gamma distribution can be obtained from the general definition of [variance for continuous random variables](https://algebrica.org/variance-and-covariance-of-a-random-variable/):

$$\sigma^{2} = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

Using the corresponding integral expression and substituting the gamma density, we have:

$$E \left(\right. X^{2} \left.\right) = \int_{0}^{+ \infty} x^{2} \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} d x$$

Combining the powers of $x$, this becomes:

$$E \left(\right. X^{2} \left.\right) = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} x^{\alpha + 1} e^{- x / \beta} d x$$

Applying the change of variable $x = \beta t$, we may rewrite the integral as:

$$E \left(\right. X^{2} \left.\right) & = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} \left(\right. \beta t \left.\right)^{\alpha + 1} e^{- t} \beta d t \\ & = \frac{\beta^{\alpha + 2}}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} \int_{0}^{+ \infty} t^{\alpha + 1} e^{- t} d t \\ & = \frac{\beta^{2}}{\Gamma \left(\right. \alpha \left.\right)} \Gamma \left(\right. \alpha + 2 \left.\right)$$

Using the identity:

$$\Gamma \left(\right. \alpha + 2 \left.\right) = \left(\right. \alpha + 1 \left.\right) \alpha \Gamma \left(\right. \alpha \left.\right)$$

we obtain:

$$E \left(\right. X^{2} \left.\right) = \beta^{2} \alpha \left(\right. \alpha + 1 \left.\right)$$

Since the mean of the gamma distribution is

$$E \left(\right. X \left.\right) = \alpha \beta$$

the variance becomes:

$$\sigma^{2} = \beta^{2} \alpha \left(\right. \alpha + 1 \left.\right) - \left(\right. \alpha \beta \left.\right)^{2} = \alpha \beta^{2}$$

---

As with the expected value, when the gamma distribution is written using a rate parameter instead of a scale parameter, the expression for the variance also changes. Under this form, the variance of the gamma distribution becomes:

$$Var \left(\right. X \left.\right) = \frac{\alpha}{\beta^{2}}$$

##### This result is fully consistent with the scale–parameter version. It is simply a different way of writing the same distribution.

## Special cases of the gamma distribution

The gamma distribution includes several important special cases, each obtained by choosing specific values for its parameters. One of the most notable is the [exponential distribution](https://algebrica.org/exponential-distribution/), which arises when $\alpha = 1$. In this situation, the density takes the simpler form

$$f \left(\right. x ; \lambda \left.\right) = \left{\right. \lambda e^{- \lambda x} & x > 0 \\ 0 & x \leq 0$$

where $\lambda$ is the rate parameter that determines how quickly the distribution decays. The exponential distribution is often used to model waiting times between successive events that occur independently and at a constant average rate, such as the time between arrivals in a [Poisson process](https://algebrica.org/poisson-distribution/).
