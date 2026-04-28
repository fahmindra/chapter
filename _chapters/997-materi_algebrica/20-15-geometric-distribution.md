---
layout: chapter
title: "Geometric Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 15
permalink: /materi-algebrica/probability-and-statistics/geometric-distribution/
---

## Introduction to the geometric distribution

The **geometric distribution** describes the number of independent trials required to observe the first success in a repeated experiment. The setting involves a sequence of identical [Bernoulli trials](https://algebrica.org/bernoulli-distribution/), each with the same probability of success, so the distribution models a waiting time rather than a fixed number of successes. Unlike distributions based on sampling without replacement, for example the [hypergeometric distribution](https://algebrica.org/hypergeometric-distribution/) where the probability of success changes after each draw, the geometric distribution assumes that the success probability remains constant across all trials.

To formalize this context, consider a sequence of trials where each outcome can be classified as either a success or a failure. The probability of success is denoted by $p$, and the trials are assumed to be independent. The random variable $X$ represents the trial on which the first success occurs. This framework is based on the following assumptions:

- Each trial yields one of two outcomes: success or failure.
- The probability of success $p$ is constant across all trials.
- Trials are mutually independent.
- The variable $X$ counts how many trials are needed before the first success appears.

---

Formally, the geometric distribution is defined by the probability mass function:

$$P \left(\right. X = k \left.\right) = \left(\right. 1 - p \left.\right)^{ k - 1} p$$

where:

- $p$ is the probability of success in a single trial.
- $1 - p$ represents the probability of failure.
- $k$ denotes the index of the trial where the first success occurs, $k = 1 , 2 , 3 , \ldots$
- The term $\left(\right. 1 - p \left.\right)^{k - 1}$ corresponds to observing $k - 1$ consecutive failures.

##### This distribution is appropriate whenever one is interested in the waiting time until the first success under constant and independent probabilistic conditions. It is often used in reliability studies, communication processes, and scenarios involving repeated attempts until a favorable outcome is achieved.

## Key features

- $$\text{1}. P \left(\right. X = k \left.\right) = \left(\right. 1 - p \left.\right)^{ k - 1} p k = 1 , 2 , 3 , \ldots$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \frac{1}{p}$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \frac{1 - p}{p^{2}}$$
- $$\text{4}. \sigma = \sqrt{\frac{1 - p}{p^{2}}}$$

##### Each expression highlights a core aspect of the geometric distribution: the probability of observing the first success on the $k$-th trial, the average waiting time, and the variability associated with repeated independent Bernoulli experiments where the probability of success remains constant.

## Deriving the geometric distribution

To understand the probability law of the geometric distribution, consider a sequence of independent Bernoulli trials $Y_{1} , Y_{2} , \ldots$, each with success probability $p$. The random variable $X$ represents the index of the first trial in which a success occurs. To determine its distribution, we examine what it means for $X$ to take a specific value.

- If $X = 1$, the first trial must already be a success, which happens with probability $p .$
- If $X = 2$, the first trial must be a failure and the second a success, giving probability $\left(\right. 1 - p \left.\right) p .$
- Similarly, $X = 3$ requires two initial failures followed by a success: $\left(\right. 1 - p \left.\right)^{2} p$.
- In general, the event $X = k$ means that the first $k - 1$ trials produce no success and the $k$-th trial does. Because the trials are independent, the probability of observing this pattern is:

$$P \left(\right. X = k \left.\right) = \left(\right. 1 - p \left.\right)^{ k - 1} p$$

This reasoning shows that the geometric distribution arises naturally from repeating identical Bernoulli experiments until the first success occurs. The factor $\left(\right. 1 - p \left.\right)^{k - 1}$ accounts for the sequence of consecutive failures, while the final $p$ corresponds to the success that ends the waiting time.

##### Since observing the first success at a later trial requires a longer sequence of consecutive failures, the probability $P \left(\right. X = k \left.\right)$ becomes smaller as $k$ increases.

## Mean of the geometric distribution

The [mean](https://algebrica.org/introduction-to-the-mean/) or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/) of a geometric distribution represents the average number of independent trials required to observe the first success. Since each trial is a Bernoulli experiment with the same probability of success $p$, the geometric distribution models a waiting time under identical and independent probabilistic conditions. To compute the mean formally, we begin with the definition of the expected value for [random discrete variables](https://algebrica.org/discrete-random-variables/):

$$\mu = E \left(\right. X \left.\right) = \sum_{k = 1}^{\infty} k P \left(\right. X = k \left.\right)$$

Substituting the probability mass function of the geometric distribution gives:

$$E \left(\right. X \left.\right) = \sum_{k = 1}^{\infty} k \left(\right. 1 - p \left.\right)^{ k - 1} p$$

To simplify this expression, we recall a standard series identity involving the sum of a weighted [geometric progression](https://algebrica.org/geometric-sequence/):

$$\sum_{k = 1}^{\infty} k r^{ k - 1} = \frac{1}{\left(\right. 1 - r \left.\right)^{2}} \left|\right. r \left|\right. < 1$$

Setting $r = 1 - p$, we obtain:

$$\sum_{k = 1}^{\infty} k \left(\right. 1 - p \left.\right)^{ k - 1} = \frac{1}{p^{2}}$$

Multiplying this result by $p$ gives the expected value of the geometric distribution:

$$E \left(\right. X \left.\right) = p \cdot \frac{1}{p^{2}} = \frac{1}{p}$$

##### This result shows that the mean of a geometric distribution depends only on the probability of success $p$. On average, one expects to perform $1 / p$ independent trials before the first success occurs, reflecting the constant nature of the probability across all repetitions.

## Variance of the geometric distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of a geometric distribution quantifies how much the number of trials required to obtain the first success is expected to fluctuate around the mean value $\mu = 1 / p$. While the mean represents the average waiting time, the variance describes how widely the waiting times are spread when each trial is an independent Bernoulli experiment with the same probability of success. Formally, the variance for a discrete random variable is defined as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

To compute it, we begin by recalling the probability mass function of the geometric distribution:

$$P \left(\right. X = k \left.\right) = \left(\right. 1 - p \left.\right)^{ k - 1} p$$

The second moment $E \left(\right. X^{2} \left.\right)$ can be obtained using a known series identity for weighted geometric sums:

$$\sum_{k = 1}^{\infty} k^{2} r^{ k - 1} = \frac{1 + r}{\left(\right. 1 - r \left.\right)^{3}} \left|\right. r \left|\right. < 1$$

Setting $r = 1 - p$, we have:

$$E \left(\right. X^{2} \left.\right) = p \sum_{k = 1}^{\infty} k^{2} \left(\right. 1 - p \left.\right)^{, k - 1} = p \cdot \frac{1 + \left(\right. 1 - p \left.\right)}{p^{3}} = \frac{2 - p}{p^{3}}$$

Using this result together with the expression for the mean $E \left(\right. X \left.\right) = 1 / p$, the variance becomes:

$$Var \left(\right. X \left.\right) = \frac{2 - p}{p^{3}} - \left(\left(\right. \frac{1}{p} \left.\right)\right)^{2}$$

Simplifying the expression gives the standard closed-form formula for the geometric distribution:

$$\sigma^{2} = \frac{1 - p}{p^{2}}$$

##### This formula shows that the variability of the geometric distribution depends only on the probability of success ( p ). When ( p ) is small, successes are rare and the waiting time becomes more dispersed; when ( p ) is large, the outcomes concentrate around a smaller number of trials.

## Example 1

A technician is testing a digital sensor that occasionally fails to detect a signal. Each detection attempt is independent, and the probability that the sensor correctly registers the signal on a single attempt is $p = 0.2$. Let $X$ be the number of attempts required until the first successful detection occurs.

Write the probability mass function of $X$. Since $X$ counts the number of independent trials until the first success, it follows a geometric distribution with parameter $p = 0.2$. Therefore,
$$P \left(\right. X = k \left.\right) = \left(\right. 1 - p \left.\right)^{k - 1} p = \left(\right. 0.8 \left.\right)^{k - 1} \left(\right. 0.2 \left.\right) , k = 1 , 2 , 3 , \ldots$$

---

Compute the expected value $E \left(\right. X \left.\right)$. The mean of a geometric distribution is
$$E \left(\right. X \left.\right) = \frac{1}{p} = \frac{1}{0.2} = 5$$

---

Compute the variance $Var \left(\right. X \left.\right)$. Using the closed-form expression for the variance, we have:
$$Var \left(\right. X \left.\right) = \frac{1 - p}{p^{2}} = \frac{0.8}{\left(\right. 0.2 \left.\right)^{2}} = \frac{0.8}{0.04} = 20$$

For a geometric distribution with $p = 0.2$, the mean is $E \left(\right. X \left.\right) = 5$ and the variance is $Var \left(\right. X \left.\right) = 20$.

## Connection between the geometric and exponential distributions

The geometric distribution is commonly viewed as the discrete analogue of the [exponential distribution](https://algebrica.org/exponential-distribution/) because both describe how long one must wait before an event occurs for the first time. The difference lies in how time is represented. In the geometric setting, time progresses in discrete steps, each corresponding to a Bernoulli trial with constant success probability $p$. The random variable $X$ counts how many such trials take place before the first success.

In continuous time, this role is played by the exponential distribution, where events occur at a constant rate $\lambda$. The waiting time $T$ until the first event is a continuous random variable with density
$$f \left(\right. t ; \lambda \left.\right) = \left{\right. \lambda e^{- \lambda t} & t > 0 \\ 0 & t \leq 0$$

Even though one distribution is discrete and the other continuous, they share a distinctive structural property: memorylessness. For the geometric distribution,
$$P \left(\right. X > m + n \mid X > m \left.\right) = P \left(\right. X > n \left.\right)$$
and the exponential distribution satisfies the corresponding identity,
$$P \left(\right. T > s + t \mid T > s \left.\right) = P \left(\right. T > t \left.\right)$$

This property shows that the probability of waiting additional time does not depend on how long one has already waited. Among standard distributions, the geometric is the only discrete law with this feature, and the exponential is the only continuous one.
