---
layout: chapter
title: "Poisson Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 16
permalink: /materi-algebrica/probability-and-statistics/poisson-distribution/
---

## Introduction to the Poisson distribution

The **Poisson distribution** is a discrete probability distribution that describes how many times a specific event may occur within a fixed period of time or space. It is applied when events occur randomly, independently of each other, and with a constant average rate over the observed [interval](https://algebrica.org/intervals/). This distribution is particularly useful for modeling rare or random occurrences, such as the number of customer arrivals per hour or the frequency of network failures in a day.

Formally, the Poisson distribution is expressed as

$$p \left(\right. x ; \lambda \left.\right) = P \left(\right. X = x \left.\right) = \frac{e^{- \lambda} \lambda^{x}}{x !}$$

where:

- $X$ represents the discrete random variable counting the number of events occurring in a given interval.
- $x$ is the specific number of occurrences being observed.
- $\lambda$ is the average rate of occurrence, that is, the expected number of events per interval.
- $e$ is [Euler’s number](https://algebrica.org/euler-number-limit-sequence/).
- $x !$ denotes the [factorial](https://algebrica.org/factorial) of $x$.

The parameter $\lambda$ fully characterizes the Poisson distribution and must be positive ($\lambda > 0$).

## The Poisson process

The Poisson distribution is closely related to the Poisson process, which models the random occurrence and accumulation of events over time or space, while the Poisson distribution expresses the probability of observing a specific number of such events within a fixed interval. A process can be defined as a Poisson process if it satisfies the following conditions:

- Events occur one at a time, never simultaneously.
- The events are independent, meaning that the occurrence of one does not influence the probability of another.
- The average rate of occurrence (λ) remains constant over time or space.
- The probability of more than one event occurring in an infinitesimally small interval is negligible.

Under these assumptions, the number of events observed in any fixed interval of duration $t$ follows a Poisson distribution with parameter $\lambda t$, which represents the expected number of occurrences during that interval. Formally, the probability that exactly $x$ events occur in time $t$ is given by:

$$p \left(\right. x ; \lambda t \left.\right) = P \left(\right. X = x \left.\right) = \frac{e^{- \lambda t} \left(\right. \lambda t \left.\right)^{x}}{x !}$$
$$x = 0 , 1 , 2 , \ldots$$

When $t = 1$, the expression reduces to the standard form of the Poisson distribution with parameter $\lambda$.

## Key features

- $$\text{1}. P \left(\right. X = x \left.\right) = \frac{\lambda^{x} e^{- \lambda}}{x !} x = 0 , 1 , 2 , \ldots$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \lambda$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \lambda$$
- $$\text{4}. \sigma = \sqrt{\lambda}$$

##### Each expression highlights a key property of the Poisson distribution, describing how it models the frequency of rare events, where its mean value lies, and how its variability is directly linked to the rate parameter $\lambda$.

## Mean of the Poisson distribution

The [mean](https://algebrica.org/introduction-to-the-mean/), or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/), of a Poisson distribution represents the average number of events that can be expected to occur in a fixed interval of time or space. It provides a direct measure of the central tendency of the distribution. Formally, the expected value is defined as:

$$\mu = E \left(\right. X \left.\right) = \sum_{x = 0}^{\infty} x P \left(\right. X = x \left.\right) = \lambda$$

Substituting the probability mass function of the Poisson distribution we have:

$$E \left(\right. X \left.\right) = \sum_{x = 0}^{\infty} x \frac{e^{- \lambda} \lambda^{x}}{x !}$$

Since the term with $x = 0$ equals zero, we can start the summation from $x = 1$:

$$E \left(\right. X \left.\right) = e^{- \lambda} \sum_{x = 1}^{\infty} \frac{x \lambda^{x}}{x !} .$$

Using the [factorial](https://algebrica.org/factorial) identity ( x/x! = 1/(x - 1)! ), the expression can be rewritten as:

$$E \left(\right. X \left.\right) = e^{- \lambda} \lambda \sum_{x = 1}^{\infty} \frac{\lambda^{x - 1}}{\left(\right. x - 1 \left.\right) !} .$$

By changing the index of summation $x - 1 = k$, we obtain:

$$E \left(\right. X \left.\right) = e^{- \lambda} \lambda \sum_{k = 0}^{\infty} \frac{\lambda^{k}}{k !} .$$

The infinite sum equals $e^{\lambda}$, which cancels out the $e^{- \lambda}$ term, giving:

$$\mu = E \left(\right. X \left.\right) = \lambda$$

This result shows that for a Poisson distribution, the mean value is equal to the parameter $\lambda$, which also represents the expected number of events occurring within the given interval. In other words, $\lambda$ characterizes both the average and the rate at which events occur.

## Variance of the Poisson distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of a Poisson distribution describes how much the number of observed events tends to fluctuate around the mean value $\mu = \lambda$. While the mean expresses the expected frequency of occurrence, the variance indicates how widely the actual counts may differ from this average when the experiment is repeated many times. By definition, the variance is written as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2} = \lambda$$

We can rewrite $x^{2}$ as $x \left[\right. \left(\right. x - 1 \left.\right) + 1 \left]\right.$, which gives:

$$E \left(\right. X^{2} \left.\right) = \lambda e^{- \lambda} \left[\right. \sum_{x = 1}^{\infty} \frac{\lambda^{x - 1}}{\left(\right. x - 1 \left.\right) !} + \sum_{x = 2}^{\infty} \frac{\lambda^{x - 2}}{\left(\right. x - 2 \left.\right) !} \left]\right.$$

Since these sums correspond to exponential series, the expression can be rewritten as:

$$E \left(\right. X^{2} \left.\right) = \lambda e^{- \lambda} \left(\right. \lambda e^{\lambda} + e^{\lambda} \left.\right) = \lambda \left(\right. \lambda + 1 \left.\right)$$

Since the mean of the Poisson distribution is $E \left(\right. X \left.\right) = \lambda$, the variance is obtained as:

$$Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2} = \lambda \left(\right. \lambda + 1 \left.\right) - \lambda^{2} = \lambda$$

Thus, the variance of a Poisson distribution is equal to its mean:

$$\sigma^{2} = \lambda$$

##### This equality between mean and variance is a defining property of the Poisson model, indicating that the expected frequency of events $\lambda$ also determines the variability observed within any fixed interval of time or space.

## Cumulative Poisson distribution

In many applications, the focus is not on finding the probability of observing exactly $x$ events, but rather on determining the probability of observing no more than a certain number of events within a fixed time or spatial interval. This concept is described by the cumulative Poisson distribution, obtained by adding together the probabilities of all outcomes from $x = 0$ up to a chosen value $x = r$:

$$F \left(\right. r ; \lambda \left.\right) = \sum_{x = 0}^{r} \frac{e^{- \lambda} \lambda^{x}}{x !} .$$

Hence, the cumulative probability that the [random variable](https://algebrica.org/discrete-random-variables/) $X$ takes a value less than or equal to $r$ is:

$$P \left(\right. X \leq r \left.\right) = e^{- \lambda} \sum_{x = 0}^{r} \frac{\lambda^{x}}{x !}$$

Each term in this summation represents the probability of exactly $x$ events occurring, while the total sum expresses the probability of observing at most $r$ events in the given interval. These probabilities are usually obtained from Poisson cumulative tables that provide pre-calculated values of $P \left(\right. X \leq r \left.\right)$ for different values of the parameter $\lambda$. Their structure is similar to that of the [standard normal Z table](https://algebrica.org/standard-normal-z-table/):

| λ | x = 0 | 1 | 2 | 3 | 4 | … |
| --- | --- | --- | --- | --- | --- | --- |
| 0.02 | 0.980 | 1.000 |  |  |  | … |
| 0.04 | 0.961 | 0.999 | 1.000 |  |  | … |
| 0.06 | 0.942 | 0.998 | 1.000 |  |  | … |
| 0.08 | 0.923 | 0.997 | 1.000 |  |  | … |
| 0.10 | 0.905 | 0.995 | 1.000 |  |  | … |
| 0.15 | 0.861 | 0.990 | 0.999 | 1.000 |  | … |
| … | … | … | … | … | … | … |

In this table, each value represents a cumulative probability of the Poisson distribution. To use it, locate the value of $\lambda$ along the rows, which indicates the average expected number of events, and find the value of x along the columns, which represents the maximum number of events considered. The cell at the intersection of these two values gives the cumulative probability $P \left(\right. X \leq x \left.\right)$, meaning the probability that the observed number of events is less than or equal to x for the chosen $\lambda$.

##### Where no numerical value is displayed, the probability is either extremely small or practically equal to one, and therefore omitted for clarity.

## Example 1

Consider a call center that receives customer service calls throughout the day. Historical data show that, on average, five calls are received every ten minutes. We want to determine the probability that exactly eight calls are received during a ten-minute interval.

---

Let $X$ be the random variable representing the number of calls received in ten minutes. Assuming that calls arrive independently and at a constant average rate, $X$ follows a Poisson distribution with parameter $\lambda = 5$. The probability mass function is:

$$P \left(\right. X = x \left.\right) = \frac{e^{- \lambda} \lambda^{x}}{x !}$$

Substituting $x = 8$ and $\lambda = 5$ we obtain:

$$P \left(\right. X = 8 \left.\right) = \frac{e^{- 5} 5^{8}}{8 !}$$

We have:

$$P \left(\right. X = 8 \left.\right) = \frac{e^{- 5} \cdot 390625}{40320} \approx 0.0653$$

Thus, the probability that exactly eight calls are received in ten minutes is approximately 0.065, or 6.5%.

---

However, the calculations are not always straightforward, and in such cases it is often more convenient to use cumulative Poisson tables. In these tables, each entry represents a cumulative probability up to a certain value of $x$. Therefore, to find the probability of exactly eight calls, we subtract the cumulative probability up to $x = 7$ from the cumulative probability up to $x = 8$, since both values include all outcomes up to their respective limits.

$$P \left(\right. X \leq 8 \left.\right) = 0.9319 , P \left(\right. X \leq 7 \left.\right) = 0.8666$$

The difference between them gives:

$$P \left(\right. X = 8 \left.\right) = 0.9319 - 0.8666 = 0.0653$$

Therefore, the probability that exactly eight calls are received during a ten-minute interval is approximately $0.0653$, meaning there is about a $6.5$ chance of observing this specific count of calls under the assumed conditions.

## From the binomial to the Poisson distribution

The Poisson distribution can be derived as a limiting form of the [binomial distribution](https://algebrica.org/binomial-distribution) when the number of trials becomes very large and the probability of success in each trial becomes very small. Imagine dividing a fixed time interval $T$ into $n$ smaller subintervals, each of length $T / n$. We assume that:

- In each subinterval at most one event may occur.
- The probability of occurrence in any subinterval is proportional to its length:
  $$P \left(\right. E_{k} \left.\right) = \frac{\lambda}{n} \left(\right. k = 1 , 2 , \ldots , n \left.\right)$$
  where $\lambda = c T$ represents the expected number of events in the whole interval.
- All events are independent of one another.

Under these conditions, the number of observed events $X$ follows a binomial distribution:
$$P \left(\right. X = x \left.\right) = \left(\right. \frac{n}{x} \left.\right) p^{x} \left(\right. 1 - p \left.\right)^{n - x} \text{with} p = \frac{\lambda}{n}$$

Now consider the [limit](https://algebrica.org/limits) as $n$ grows indefinitely large and $p$ becomes very small, while keeping their product $n p = \lambda$ constant. In this limit, the binomial expression approaches:

$$p \left(\right. x ; \lambda \left.\right) = P \left(\right. X = x \left.\right) = \frac{e^{- \lambda} \lambda^{x}}{x !}$$

which is exactly the Poisson distribution. Let’s see the derivation formally:

$$P \left(\right. X = x \left.\right) = \left(\right. \frac{n}{x} \left.\right) \left(\left(\right. \frac{\lambda}{n} \left.\right)\right)^{x} \left(\left(\right. 1 - \frac{\lambda}{n} \left.\right)\right)^{n - x}$$

$$= \frac{n !}{x ! \left(\right. n - x \left.\right) !} \frac{\lambda^{x}}{n^{x}} \left(\left(\right. 1 - \frac{\lambda}{n} \left.\right)\right)^{n} \left(\left(\right. 1 - \frac{\lambda}{n} \left.\right)\right)^{- x}$$

As $n$ increases:

$$\left(\left(\right. 1 - \frac{\lambda}{n} \left.\right)\right)^{n} \rightarrow e^{- \lambda} , \frac{n !}{\left(\right. n - x \left.\right) ! n^{x}} \rightarrow 1$$

and thus we obtain the limit:

$$p \left(\right. x ; \lambda \left.\right) = P \left(\right. X = x \left.\right) = \frac{e^{- \lambda} \lambda^{x}}{x !}$$

##### This limiting relationship shows that the Poisson distribution can be seen as an approximation of the binomial law for rare events that occur independently and infrequently over time or space.
