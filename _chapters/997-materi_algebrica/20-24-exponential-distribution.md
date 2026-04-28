---
layout: chapter
title: "Exponential Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 24
permalink: /materi-algebrica/probability-and-statistics/exponential-distribution/
---

## What is the exponential probability distribution

The **exponential distribution** characterizes the time elapsed between random, independent events occurring at a constant average rate. It is often applied to model waiting times, such as the [interval](https://algebrica.org/intervals/) before the next customer arrives or a machine experiences a failure, providing a simple and intuitive way to describe processes governed by randomness and continuity over time. In formal terms, given a random variable $X$ and a positive real parameter $\lambda$, the exponential distribution is defined by the following probability density function:

$$f \left(\right. x ; \lambda \left.\right) = \left{\right. \lambda e^{- \lambda x} & \text{for} x > 0 \\ 0 & \text{for} x \leq 0$$

- $\lambda$ is the rate parameter, which determines how frequently events occur.
- A larger value of $\lambda$ corresponds to events happening more often.
- A smaller value indicates longer expected waiting times between events.

This function represents a continuous probability model that quantifies the likelihood of waiting a certain amount of time before an event occurs in a process with a constant rate of occurrence.

![](https://algebrica.org/wp-content/uploads/resources/images/exponential-distribution-1.png "Exponential distribution")

From the definition of the exponential distribution, and as illustrated in the figure above, we can observe that the total area under the curve of $f \left(\right. x ; \lambda \left.\right)$ equals one. In other words, the probability density function is normalized, satisfying the fundamental property

$$\int_{- \infty}^{+ \infty} f \left(\right. x ; \lambda \left.\right) d x = 1$$

Since $f \left(\right. x ; \lambda \left.\right) = 0$ for $x \leq 0$, the [definite integral](https://algebrica.org/definite-integrals/) effectively reduces to

$$\int_{0}^{+ \infty} \lambda e^{- \lambda x} d x = \left[\right. - e^{- \lambda x} \left]\right._{0}^{+ \infty} = 1$$

Therefore, the probability density function of the exponential distribution satisfies the normalization condition

$$\int_{- \infty}^{+ \infty} f \left(\right. x ; \lambda \left.\right) d x = 1$$

which ensures that the total probability over the entire [domain](https://algebrica.org/determining-the-domain-of-a-function/) is equal to one, as required for any valid continuous probability distribution.

##### The sum of many independent exponential random variables approaches the [normal distribution](https://algebrica.org/normal-distribution), as stated by the Central Limit Theorem.

The exponential distribution derives its name from the [exponential function](https://algebrica.org/exponential-function/) that shapes its probability density. The decreasing pattern of the curve $\lambda e^{- \lambda x}$ shows how the probability of observing longer waiting times diminishes exponentially, highlighting the intrinsic link between the concept of probability and the mathematical properties of the exponential function.

## Key features

- $$\text{1}. f \left(\right. x \left.\right) = \lambda e^{- \lambda x} x \geq 0$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \frac{1}{\lambda}$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \frac{1}{\lambda^{2}}$$
- $$\text{4}. \sigma = \frac{1}{\lambda}$$

##### Each expression highlights a key property of the exponential distribution, showing how it models waiting times between events, how its mean and variability depend on the rate parameter $\lambda$, and how its memoryless nature distinguishes it from other continuous distributions.

## Expected value and variance of the exponential distribution

As introduced in the section on continuous random variables, the [expected value of a continuous random variable](https://algebrica.org/mean-or-expected-value-of-a-random-variable/) provides a measure of the central tendency of the distribution and is defined as:

$$\mu = E \left(\right. X \left.\right) = \int_{- \infty}^{+ \infty} x f \left(\right. x \left.\right) d x$$

This expression is general and applies to any continuous distribution, where $f \left(\right. x \left.\right)$ denotes the probability density function of the random variable $X$. In the specific case of the exponential distribution, the expected value is obtained as

$$\mu = E \left(\right. X \left.\right) = \int_{0}^{+ \infty} x \lambda e^{- \lambda x} d x = \frac{1}{\lambda}$$

This result represents the average waiting time between two consecutive events in a process that occurs at a constant rate $\lambda$.

---

The variance of the exponential distribution can be obtained from the general definition of [variance for continuous random variables](https://algebrica.org/variance-and-covariance-of-a-random-variable/):

$$\sigma^{2} = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

Using the corresponding integral expression and substituting the exponential density function, we have:

$$E \left(\right. X^{2} \left.\right) = \int_{0}^{+ \infty} x^{2} \lambda e^{- \lambda x} d x = \frac{2}{\lambda^{2}}$$

Therefore, the variance is

$$\sigma^{2} = \frac{2}{\lambda^{2}} - \left(\left(\right. \frac{1}{\lambda} \left.\right)\right)^{2} = \frac{1}{\lambda^{2}}$$

This shows that the variability of the exponential distribution decreases as the rate parameter $\lambda$ increases, meaning that higher event frequencies correspond to shorter and more consistent waiting times.

## The survival function of the exponential distribution

The survival function of the exponential distribution expresses the probability that the random variable $X$ takes on a value greater than a given threshold $x$. It is defined as the complement of the cumulative distribution function:

$$S \left(\right. x \left.\right) = P \left(\right. X > x \left.\right) = 1 - F \left(\right. x \left.\right)$$

For the exponential distribution with rate parameter $\lambda > 0$, the survival function takes the form

$$S \left(\right. x \left.\right) = e^{- \lambda x} x \geq 0$$

This function shows that the probability of “surviving” beyond a certain time decreases exponentially as $x$ increases. In other words, the longer we wait, the smaller the chance that the event has not yet occurred.

## The memoryless property

An important property of a random variable $X$ that follows an exponential distribution is the so-called memoryless property. This characteristic can be expressed by the equality

$$P \left(\right. X > s + t \mid X > s \left.\right) = P \left(\right. X > t \left.\right)$$

which means that the probability of waiting an additional time $t$ does not depend on how much time $s$ has already elapsed. In other words, the exponential distribution “forgets” past events, making it unique among continuous probability distributions.

Starting from the definition of conditional probability, we can write:

$$P \left(\right. X > s + t \mid X > s \left.\right) = \frac{P \left(\right. X > s + t \left.\right)}{P \left(\right. X > s \left.\right)}$$

By substituting the survival function of the exponential distribution, we obtain:

$$P \left(\right. X > s + t \mid X > s \left.\right) & = \frac{\int_{s + t}^{+ \infty} \lambda e^{- \lambda x} d x}{\int_{s}^{+ \infty} \lambda e^{- \lambda x} d x} \\ & = \frac{e^{- \lambda \left(\right. s + t \left.\right)}}{e^{- \lambda s}} \\ & = e^{- \lambda t}$$

Finally, observing that $e^{- \lambda t} = P \left(\right. X > t \left.\right)$, we can conclude that

$$P \left(\right. X > s + t \mid X > s \left.\right) = P \left(\right. X > t \left.\right)$$

This confirms that the exponential distribution has no memory of past events. The probability of waiting an additional time $t$ remains the same, regardless of how long $s$ has already elapsed.

## Example 1

A certain type of light bulb has a lifetime that follows an exponential distribution with a rate parameter $\lambda = 0.002$ failures per hour.

- Find the probability that a bulb lasts more than 400 hours.
- Determine the probability that a bulb lasts between 200 and 600 hours.
- Compute the expected lifetime and the variance of the bulb’s duration.

---

To find the probability that the bulb operates for more than 400 hours, we use the survival function of the exponential distribution:

$$P \left(\right. X > x \left.\right) = e^{- \lambda x}$$

Substituting the given value of $\lambda = 0.002$ and $x = 400$, we obtain

$$P \left(\right. X > 400 \left.\right) = e^{- 0.002 \times 400} = e^{- 0.8} \approx 0.4493$$

This means there is approximately a 44.9% probability that the bulb will last beyond 400 hours.

---

To determine the probability that the bulb’s lifetime falls between 200 and 600 hours, we calculate the difference between the probabilities of lasting more than 200 hours and more than 600 hours:

$$P \left(\right. 200 < X < 600 \left.\right) & = P \left(\right. X > 200 \left.\right) - P \left(\right. X > 600 \left.\right) \\ & = e^{- 0.002 \times 200} - e^{- 0.002 \times 600} \\ & = e^{- 0.4} - e^{- 1.2} \approx 0.6703 - 0.3010 = 0.3693$$

Thus, there is approximately a 36.9% probability that the bulb operates between 200 and 600 hours.

---

The expected lifetime of a bulb that follows an exponential distribution is given by the inverse of the rate parameter:

$$E \left(\right. X \left.\right) = \frac{1}{\lambda} = \frac{1}{0.002} = 500 \text{hours}$$

This means that, on average, a bulb is expected to last 500 hours before failing.

The variance, which measures the spread of the distribution, is obtained as the square of the mean lifetime:

$$\sigma^{2} = \frac{1}{\lambda^{2}} = \frac{1}{\left(\right. 0.002 \left.\right)^{2}} = 250000$$

Consequently, the standard deviation is:

$$\sigma = \sqrt{\sigma^{2}} = 500 \text{hours}$$

Recapping the results of the exercise, we have:

$$& P \left(\right. X > 400 \left.\right) = 0.4493 \\ & P \left(\right. 200 < X < 600 \left.\right) = 0.3693 \\ & E \left(\right. X \left.\right) = 500 \text{hours} \\ & \sigma^{2} = Var \left(\right. X \left.\right) = 250000 \\ & \sigma = 500 \text{hours}$$

## Connection to the gamma distribution

The exponential distribution can be viewed as one of the simplest special cases of the [gamma distribution](https://algebrica.org/gamma-distribution). In particular, by setting the shape parameter of the gamma distribution to $\alpha = 1$, the gamma density:

$$G \left(\right. x ; \alpha , \beta \left.\right) = \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} x > 0$$

simplifies considerably. When $\alpha = 1$, we have $\Gamma \left(\right. 1 \left.\right) = 1$ and the term $x^{\alpha - 1}$ becomes $x^{0} = 1$. The density therefore reduces to

$$G \left(\right. x ; 1 , \beta \left.\right) = \frac{1}{\beta} e^{- x / \beta} x > 0$$

which is exactly the exponential distribution with scale parameter $\beta$. If we switch to the rate parametrization by setting $\lambda = 1 / \beta$, the same expression becomes
$$G \left(\right. x ; \lambda \left.\right) = \lambda e^{- \lambda x} x > 0$$

This shows that the exponential distribution is simply the gamma distribution with shape equal to one.
