---
layout: chapter
title: "Bernoulli Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 12
permalink: /materi-algebrica/probability-and-statistics/bernoulli-distribution/
---

## Introduction to the Bernoulli distribution

The Bernoulli distribution models the outcome of a single experiment that can result in only two mutually exclusive events: success or failure. Such an experiment is known as a Bernoulli trial. A [discrete random variable](https://algebrica.org/discrete-random-variables/) is said to follow a Bernoulli distribution when it takes the value $1$ if the trial results in success and the value $0$ if it results in failure. The uncertainty of the experiment is governed entirely by a single parameter $p$, which represents the probability of success in that trial. A Bernoulli trial must satisfy a few basic conditions:

- Only two outcomes are possible: success with probability $p$, and failure with probability $1 - p = q$.
- The probability structure of the trial is fixed and determined solely by the value of $p$.
- The outcome is represented by a random variable $X$ taking values in the set $0 , 1$.
- The result of the trial is single and mutually exclusive: either success or failure.

---

Formally, the Bernoulli distribution is defined by the probability mass function:

$$P \left(\right. X = x \left.\right) = b \left(\right. x ; p \left.\right) = p^{x} \left(\right. 1 - p \left.\right)^{ 1 - x}$$

where:

- $x \in 0 , 1$ is the observed outcome of the trial.
- $p$ is the probability of success.
- $1 - p = q$ is the probability of failure.

##### This simple model forms the basis for more complex discrete distributions, including the [binomial distribution](https://algebrica.org/binomial-distribution/), which extends the same structure to a fixed number of independent Bernoulli trials.

## Key features

- $$\text{1}. P \left(\right. X = x \left.\right) = b \left(\right. x ; p \left.\right) = p^{x} \left(\right. 1 - p \left.\right)^{ 1 - x} x \in 0 , 1$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = p$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = p \left(\right. 1 - p \left.\right)$$
- $$\text{4}. \sigma = \sqrt{ p \left(\right. 1 - p \left.\right) }$$

##### Each expression highlights a key property of the Bernoulli distribution, offering a quick overview of how it assigns probabilities, where its average outcome lies, and how its variability is determined.

## Mean of the Bernoulli distribution

The [mean](https://algebrica.org/introduction-to-the-mean/), or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/), of a Bernoulli distribution represents the long–run average outcome of a sequence of identical Bernoulli trials. Since the random variable can take only the values $0$ and $1$, the mean expresses the proportion of successes that would be observed over many repetitions of the same experiment. To compute the mean formally, we start from the definition of the expected value of a discrete random variable:

$$\mu = E \left(\right. X \left.\right) = \underset{x \in 0 , 1}{\sum} x b \left(\right. x ; p \left.\right)$$

For a Bernoulli distribution, the probability mass function, that is the rule assigning a probability to each possible value of the random variable, is given by:

$$b \left(\right. x ; p \left.\right) = p^{x} \left(\right. 1 - p \left.\right)^{ 1 - x}$$

so the expectation becomes:

$$E \left(\right. X \left.\right) = 0 \cdot \left(\right. 1 - p \left.\right) + 1 \cdot p$$

We obtain:

$$\mu = E \left(\right. X \left.\right) = p$$

##### The parameter $p$ of the Bernoulli distribution is itself the expected proportion of successes. If the experiment were repeated a large number of times, the average value of the observations would approach $p$.

## Variance of the Bernoulli distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of a Bernoulli distribution quantifies how much the outcomes of a single Bernoulli trial are expected to fluctuate around the mean value $\mu = p$. While the mean describes the long–run proportion of successes, the variance measures how dispersed the results are across repeated repetitions of the same experiment. Formally, the variance is defined as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

For a Bernoulli random variable $X$, only two outcomes are possible:
 $$X = 0 \text{or} X = 1$$
Because squaring does not change these values, we have $X^{2} = X$. Using this property, we can compute the expectation:

$$E \left(\right. X^{2} \left.\right) = 0^{2} \left(\right. 1 - p \left.\right) + 1^{2} p = p$$

We already know that:
 $$E \left(\right. X \left.\right) = p$$
so substituting into the variance formula yields:

$$Var \left(\right. X \left.\right) = p - p^{2} = p \left(\right. 1 - p \left.\right)$$

Therefore, the variance of a Bernoulli distribution is:

$$\sigma^{2} = p \left(\right. 1 - p \left.\right)$$

##### As $p$ moves closer to $0$ or $1$, the variance decreases, since the experiment becomes more and more predictable and the outcome tends to repeat itself with little fluctuation.

## Example 1

Consider a quality-control test performed on a single electronic component. During the inspection, the component is powered on and must reach a specific voltage level to be considered functional. Let $X$ be the random variable representing the outcome of the test, where:

- $X = 1$ if the component meets the required standard (success).
- $X = 0$ if it fails the test (failure).

Suppose that, based on historical data, the probability that a randomly selected component functions correctly is $p = 0.85$, so the random variable $X$ follows a Bernoulli distribution with parameter $p$. Since the distribution is Bernoulli, the probability mass function, that is, the rule assigning a probability to each possible value of the random variable, is given by:

$$P \left(\right. X = x \left.\right) = p^{x} \left(\right. 1 - p \left.\right)^{ 1 - x}$$

To compute the probability of success ($X = 1$):

$$P \left(\right. X = 1 \left.\right) = p^{1} \left(\right. 1 - p \left.\right)^{0} = 0.85$$

Similarly, the probability of failure is:

$$P \left(\right. X = 0 \left.\right) = p^{0} \left(\right. 1 - p \left.\right)^{1} = 0.15$$

Therefore, the probability that the component passes the test is ( 0.85 ), or 85%.

##### This example shows how past observations and the structure of the test work together in choosing a model. The historical success rate suggests the value of $p$, and the fact that the test has only two possible outcomes makes the Bernoulli distribution a natural way to describe the uncertainty of the experiment.

## The role of the Bernoulli distribution in the binomial model

The Bernoulli distribution is the foundation of the [binomial distribution](https://algebrica.org/binomial-distribution). A binomial random variable counts how many successes occur in $n$ independent Bernoulli trials, each with probability $p$. In this view, the binomial model simply summarizes the combined outcomes of repeated Bernoulli experiments. Its probability mass function,

$$P \left(\right. X = k \left.\right) = \left(\right. \frac{n}{k} \left.\right) p^{k} \left(\right. 1 - p \left.\right)^{ n - k}$$

describes all possible ways in which $k$ successes can arise from $n$ trials. From this structure follow the main properties of the binomial distribution, including its mean $n p$ and variance $n p \left(\right. 1 - p \left.\right)$, which derive directly from those of the Bernoulli model.

---

The following table offers a concise side-by-side comparison of the Bernoulli and Binomial distributions. Although the two models are closely related, they differ in scope and interpretation: As noted above, the Bernoulli distribution describes a single success–failure experiment, while the Binomial distribution extends this idea to a fixed number of independent and identical trials.

| Feature | Bernoulli | Binomial |
| --- | --- | --- |
| Number of trials | 1 | $n$ |
| Parameters | $p$ | $n , p$ |
| Support | $0 , 1$ | $0 , \ldots , n$ |
| Mean | $p$ | $n p$ |
| Variance | $p \left(\right. 1 - p \left.\right)$ | $n p \left(\right. 1 - p \left.\right)$ |
