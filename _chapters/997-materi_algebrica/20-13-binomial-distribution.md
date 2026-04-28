---
layout: chapter
title: "Binomial Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 13
permalink: /materi-algebrica/probability-and-statistics/binomial-distribution/
---

## Introduction to the binomial distribution

The **binomial distribution** is a discrete probability distribution that models the number of successes in a sequence of independent experiments, each one following a [Bernoulli distribution](https://algebrica.org/bernoulli-distribution/) with the same probability of success. In this sense, the binomial model is derived directly from repeated Bernoulli trials. In each trial, only two outcomes are possible: success or failure. The binomial model therefore quantifies, for every possible value of $x$, the probability of observing exactly $x$ successes in a total of $n$ trials, assuming that the probability of success in each trial remains constant and equal to $p$. This type of experiment must satisfy a series of properties:

- There are only two possible outcomes for each trial: success, with probability $p$, and failure, with probability $1 - p$.
- The trials are independent.
- The probability of success $p$ remains constant across all trials.
- The total number of trials $n$ is fixed in advance.
- The random variable $X$ represents the number of successes obtained in the sequence of trials.
- Each trial produces a single, mutually exclusive outcome, either success or failure.

---

Formally, the binomial distribution is expressed as

$$P \left(\right. X = x \left.\right) = b \left(\right. x ; n , p \left.\right) = \left(\right. \frac{n}{x} \left.\right) p^{x} q^{n - x}$$

where:

- $q = 1 - p$.
- $n$ represents the total number of independent trials.
- $x$ is the number of observed successes.
- $p$ is the probability of success in each individual trial.
- $q$ is the probability of failure, equal to ( 1 - p ).
- $\left(\right. \frac{n}{x} \left.\right)$ is the [binomial coefficient](https://algebrica.org/binomial-coefficient), which counts the number of distinct ways to obtain $x$ successes out of $n$ trials.

---

Considering that $p + q = 1$, the binomial model satisfies the fundamental condition required of any probability distribution:

$$\sum_{x = 0}^{n} b \left(\right. x ; n , p \left.\right) = 1$$

This relationship ensures that the total probability across all possible outcomes is equal to one, meaning that the distribution fully describes every potential result of the $n$ Bernoulli trials.

##### The binomial distribution is directly related to the [binomial theorem](https://algebrica.org/binomial-theorem), which states that the expansion of $\left(\right. p + q \left.\right)^{n}$ yields all possible combinations of successes and failures across $n$ trials. Each term in this expansion corresponds to a possible number of successes $x$, with its associated probability given precisely by the binomial formula above.

## Key features

- $$\text{1}. P \left(\right. X = x \left.\right) = b \left(\right. x ; n , p \left.\right) = \left(\right. \frac{n}{x} \left.\right) p^{x} q^{ n - x} x = 0 , 1 , \ldots , n$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = n p$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = n p \left(\right. 1 - p \left.\right)$$
- $$\text{4}. \sigma = \sqrt{ n p \left(\right. 1 - p \left.\right) }$$

##### Each expression highlights a key property of the binomial distribution, summarizing how it models the number of successes, where its average behavior lies, and how its variability increases with the number of trials.

## Mean of the binomial distribution

The [mean](https://algebrica.org/introduction-to-the-mean/), or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/), of a binomial distribution represents the average number of successes that can be expected over a large number of identical experiments. To compute the mean formally, we start from the definition of the expected value:

$$\mu = E \left(\right. X \left.\right) = \sum_{x = 0}^{n} x P \left(\right. X = x \left.\right) = n p$$

Substituting the probability mass function of the binomial distribution we have:

$$E \left(\right. X \left.\right) = \sum_{x = 0}^{n} x \left(\right. \frac{n}{x} \left.\right) p^{x} \left(\right. 1 - p \left.\right)^{n - x}$$

Using the identity, which connects two related binomial coefficients by reducing both $n$ and $x$ by one:

$$x \left(\right. \frac{n}{x} \left.\right) = n \left(\right. \frac{n - 1}{x - 1} \left.\right)$$

the expression becomes:

$$E \left(\right. X \left.\right) = n p \sum_{x = 1}^{n} \left(\right. \frac{n - 1}{x - 1} \left.\right) p^{x - 1} \left(\right. 1 - p \left.\right)^{\left(\right. n - 1 \left.\right) - \left(\right. x - 1 \left.\right)}$$

The summation term equals 1, because it corresponds to the total probability of a binomial distribution with parameters $n - 1$ and $p$. Therefore, we obtain:

$$\mu = E \left(\right. X \left.\right) = n p$$

This shows that the mean of a binomial distribution depends linearly on both the number of trials and the probability of success in each trial. On average, we expect $n p$ of the $n$ experiments to produce a successful outcome.

---

This result can also be derived by noting that the binomial random variable $X$ can be expressed as the sum of ( n ) independent Bernoulli random variables $X_{1} , X_{2} , \ldots , X_{n}$, each taking the value 1 (success) with probability $p$ and 0 (failure) with probability $1 - p$:

$$X = X_{1} + X_{2} + \hdots + X_{n}$$

By the linearity of expectation:

$$E \left(\right. X \left.\right) = E \left(\right. X_{1} \left.\right) + E \left(\right. X_{2} \left.\right) + \hdots + E \left(\right. X_{n} \left.\right) = n p$$

## Variance of the binomial distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of a binomial distribution measures how much the number of observed successes is expected to vary around the mean value $\mu = n p$. While the mean describes the central tendency of the distribution, the variance quantifies its spread that is, how concentrated or dispersed the outcomes are across repeated experiments. Formally, the variance is defined as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2} = n p q$$

To compute it, we recall that the binomial variable $X$ can be expressed as the sum of $n$ independent Bernoulli variables $X_{1} , X_{2} , \ldots , X_{n}$, where each trial has probability of success $p$:

$$X = X_{1} + X_{2} + \hdots + X_{n}$$

Since the variance of a Bernoulli variable is $Var \left(\right. X_{i} \left.\right) = p \left(\right. 1 - p \left.\right)$, and the trials are independent, the variance of their sum is simply the sum of the individual variances:

$$Var \left(\right. X \left.\right) = Var \left(\right. X_{1} \left.\right) + Var \left(\right. X_{2} \left.\right) + \hdots + Var \left(\right. X_{n} \left.\right)$$

Therefore, the variance of the binomial distribution is:

$$\sigma^{2} = n p q$$

##### This result shows that the variability of the distribution increases linearly with the number of trials $n$, and depends on both the probability of success $p$ and the probability of failure $\left(\right. 1 - p \left.\right)$.

## Example 1

Consider a factory that produces electronic sensors. Each sensor is tested to verify whether it operates correctly under specific temperature conditions. Suppose 6 sensors are selected at random from a production batch, and the probability that a single sensor passes the test is ( p = 0.7 ). We want to find the probability that exactly 4 of the 6 sensors will function properly during the test.

---

Assuming that each test is independent, the probability is given by:

$$b \left(\right. 4 ; 6 , 0.7 \left.\right) & = \left(\right. \frac{6}{4} \left.\right) \left(\right. 0.7 \left.\right)^{4} \left(\right. 0.3 \left.\right)^{2} \\ & = \frac{6 !}{4 ! 2 !} \left(\right. 0.7 \left.\right)^{4} \left(\right. 0.3 \left.\right)^{2} \\ & = 15 \times 0.2401 \times 0.09 = 0.324135$$

##### The [factorial](https://algebrica.org/factorial) symbol $\left(\right. ! \left.\right)$ indicates the product of all positive integers up to a given number.

Therefore, the probability that exactly four sensors out of six will pass the test is approximately $0.324$, or 32.4%.

## Cumulative binomial distribution

In some contexts, the goal is not to find the probability of getting exactly $x$ successes, but rather the probability of getting no more than a certain number of successes $r$ in $n$ Bernoulli trials. This type of probability is obtained by summing all individual terms of the binomial distribution from $x = 0$ up to $x = r$:

$$B \left(\right. r ; n , p \left.\right) = \sum_{x = 0}^{r} b \left(\right. x ; n , p \left.\right)$$

where $b \left(\right. x ; n , p \left.\right)$ represents the probability mass function of the binomial distribution. The values of the cumulative binomial distribution are often provided in dedicated tables, similar in purpose to the [standard normal Z table](https://algebrica.org/standard-normal-z-table/). Each entry in these tables corresponds to the cumulative probability of obtaining up to a given number of successes, for specific combinations of $n$ and $p$.

In more formal terms, the cumulative probability of the binomial distribution can be expressed as:

$$P \left[\right. X \leq c \left]\right. = \sum_{x = 0}^{c} \left(\right. \frac{n}{x} \left.\right) p^{x} \left(\right. 1 - p \left.\right)^{n - x}$$

This probability is often computed using cumulative binomial tables, which list pre-calculated values of $P \left[\right. X \leq c \left]\right.$ for selected values of $n$ and $p$. A simplified portion of such a table is shown below.

| n | c | p = 0.05 | p = 0.10 | p = 0.20 | p = 0.30 | p = 0.40 | p = 0.50 | … |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 0 | 0.950 | 0.900 | 0.800 | 0.700 | 0.600 | 0.500 | … |
| 1 | 1 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | … |
| 2 | 0 | 0.903 | 0.810 | 0.640 | 0.490 | 0.360 | 0.250 | … |
| 2 | 1 | 0.998 | 0.990 | 0.960 | 0.910 | 0.840 | 0.750 | … |
| 2 | 2 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | … |
| … | … | … | … | … | … | … | … | … |

These tables allow users to quickly find cumulative probabilities without computing each term of the summation, in the same way that the [standard normal Z table](https://algebrica.org/standard-normal-z-table/) is used to determine cumulative probabilities under the normal distribution. The intersection between a row and a column gives the cumulative probability $P \left[\right. X \leq c \left]\right.$, that is, the probability of obtaining up to $c$ successes for the corresponding value of $n$ and $p$.

##### Such tabulated values allow for quick estimation of binomial probabilities without performing the full summation manually, just as the Z table simplifies the computation of probabilities under the [normal distribution](https://algebrica.org/normal-distribution).

## Normal approximation of the binomial distribution

In certain cases, the binomial distribution, which is inherently discrete, can be effectively approximated by a continuous [normal distribution](https://algebrica.org/normal-distribution). This approximation is appropriate when the binomial distribution exhibits a roughly symmetric and bell-shaped form, closely resembling the profile of a normal curve. Such situations typically occur when the number of trials $n$ is large and the probability of success $p$ is not too close to 0 or 1.

In these conditions, the random variable $X$, distributed as $Bin \left(\right. n , p \left.\right)$, can be approximated by a normal distribution with the same mean and variance:

$$X \approx \mathcal{N} \left(\right. x ; n p , n p q \left.\right)$$

This method simplifies calculations and allows binomial probabilities to be estimated using the tools and [Z tables](https://algebrica.org/standard-normal-z-table/) associated with the normal distribution, providing accurate results in most practical applications.

---

If $X$ is a binomial random variable with mean $\mu = n p$ and variance $\sigma^{2} = n p q$, then the limiting distribution of the standardized variable $Z$, defined as:

$$\frac{X - n p}{\sqrt{n p q}} \overset{d }{\rightarrow} \mathcal{N} \left(\right. x ; 0 , 1 \left.\right) \text{as} n \rightarrow \infty$$

is the [standard normal distribution](https://algebrica.org/normal-distribution/):

$$Z sim \mathcal{N} \left(\right. x ; 0 , 1 \left.\right)$$

##### The notation $\overset{d }{\rightarrow}$ denotes convergence in distribution, meaning that the probability distribution of the standardized variable gradually approaches the standard normal distribution as $n$ increases.

## Example 2

To better illustrate the normal approximation to the binomial distribution, consider a company that produces small electronic components. During quality control, each item is tested to check whether it meets the required electrical specifications. Suppose that 100 components are tested and that the probability a single component passes the test is $p = 0.9$. We want to find the probability that between 85 and 92 components pass the inspection successfully.

---

Let $X$ be the discrete random variable representing the number of components that pass the test. Then the probability of interest can be written as:

$$P \left(\right. 85 \leq X \leq 92 \left.\right) = \sum_{x = 85}^{92} b \left(\right. x ; 100 , 0.9 \left.\right)$$

Since $n$ is large and $p$ is not too close to 0 or 1, we can use the normal approximation with:

$$\mu = n p = 100 \times 0.9 = 90$$
$$\sigma = \sqrt{n p q} = \sqrt{100 \times 0.9 \times 0.1} = 3$$

Because the binomial variable $X$ is discrete (it only takes [integer](https://algebrica.org/integers/) values) and the normal distribution is continuous, the probability of $X$ lying between 85 and 92 is better approximated by the area under the normal curve from half a unit below 85 to half a unit above 92. For this reason, we replace the discrete bounds with

$$x_{1} = 84.5 \text{and} x_{2} = 92.5$$

---

We then compute the corresponding standardized values using the [transformation](https://algebrica.org/normal-distribution):

$$z = \frac{x - \mu}{\sigma}$$

which gives:

$$z_{1} = \frac{84.5 - 90}{3} = - 1.83 , z_{2} = \frac{92.5 - 90}{3} = 0.83$$

We can write:

$$P \left(\right. 85 \leq X \leq 92 \left.\right) = \sum_{x = 85}^{92} b \left(\right. x ; 100 , 0.9 \left.\right) \approx P \left(\right. - 1.83 \leq Z \leq 0.83 \left.\right)$$

---

According to the standard normal distribution, we have:

$$P \left(\right. - 1.83 \leq Z \leq 0.83 \left.\right) = P \left(\right. Z \leq 0.83 \left.\right) - P \left(\right. Z \leq - 1.83 \left.\right)$$

From the [standard normal Z table](https://algebrica.org/standard-normal-z-table/):

$$P \left(\right. Z \leq 0.83 \left.\right) = 0.7967 , P \left(\right. Z \leq - 1.83 \left.\right) = 0.0336$$

---

Thus we obtain:

$$P \left(\right. - 1.83 \leq Z \leq 0.83 \left.\right) = 0.7967 - 0.0336 = 0.7631$$

Therefore, the probability that between 85 and 92 components pass the quality test is approximately 0.763, or 76.3%:

## Comparison between the binomial and hypergeometric distributions

The binomial distribution applies when each trial has the same probability of success and when one trial does not influence the next. This setting is appropriate for sampling with replacement or for situations in which the population is large enough that removing a single item does not change its overall composition. In many real-world problems, however (such as quality control), the selected items are not replaced. In these cases, the composition of the population changes after each draw, and the binomial assumptions are no longer valid. The correct model becomes the [hypergeometric distribution](https://algebrica.org/hypergeometric-distribution).

When the population size $N$ is not large compared with the sample size $n$, the probability of success can no longer be treated as constant across trials. The binomial model must then be replaced by its finite-population counterpart:

$$X sim \text{Hyp} \left(\right. N , K , n \left.\right)$$

where $K$ is the number of successes in the population. Moving from the binomial to the hypergeometric distribution reflects the shift from independent trials with fixed probabilities to the more realistic setting of sampling without replacement.

## Connection between the binomial and the Poisson distribution

When the number of trials $n$ is large and the probability of success $p$ is small, while keeping $n p = \lambda$ constant, the binomial distribution converges to the [Poisson Distribution](https://algebrica.org/poisson-distribution/):

$$P \left(\right. X = x \left.\right) = \frac{e^{- \lambda} \lambda^{x}}{x !}$$

##### The binomial distribution thus serves as the foundation from which the Poisson model arises in the limit, offering a simplified representation of rare and independent events occurring over time or space.
