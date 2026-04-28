---
layout: chapter
title: "Hypergeometric Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 14
permalink: /materi-algebrica/probability-and-statistics/hypergeometric-distribution/
---

## Introduction to the hypergeometric distribution

The hypergeometric distribution is a discrete probability distribution that describes the number of successes drawn from a finite population without replacement. Unlike the [binomial distribution](https://algebrica.org/binomial-distribution/), where each trial is independent and the probability of success stays constant, the hypergeometric setting involves draws that change the composition of the population at every step. As a consequence, the probability of selecting a success varies after each extraction.

To formalize this scenario, we consider a finite population divided into two categories: successes and failures. A sample of fixed size is taken without replacement, and the random variable represents the number of successes observed in that sample. This model relies on the following assumptions:

- The population has a fixed size, with a known number of successes and failures.
- A sample of predetermined size is drawn from the population.
- The draws are made without replacement.
- Each draw results in selecting either a success or a failure.
- The [discrete random variable](https://algebrica.org/discrete-random-variables/) $X$ counts how many successes are observed in the sample.

---

Formally, the hypergeometric distribution is defined as:

$$P \left(\right. X = x \left.\right) = \frac{\left(\right. \frac{K}{x} \left.\right) \left(\right. \frac{N - K}{n - x} \left.\right)}{\left(\right. \frac{N}{n} \left.\right)}$$

where:

- $N$ is the total size of the population.
- $K$ is the number of successes in the population.
- $N - K$ is the number of failures in the population.
- $n$ is the sample size drawn without replacement.
- $x$ is the number of observed successes.
- $\left(\right. \frac{K}{x} \left.\right)$ is the [binomial coefficient](https://algebrica.org/binomial-coefficient/), which counts the number of ways to choose $x$ successes from the $K$ available.
- $\left(\right. \frac{N - K}{n - x} \left.\right)$ counts the number of ways to choose the remaining items from the failures.
- $\left(\right. \frac{N}{n} \left.\right)$ represents the total number of distinct samples of size $n$ that can be drawn from a population of size $N$.

##### This distribution is used when independence does not hold and the probability of success changes after each draw. It provides a reliable model for sampling from finite populations, as in quality control, where items are inspected without replacement from a batch with known numbers of defective and non-defective units.

## Key features

- $$\text{1}. P \left(\right. X = x \left.\right) = \frac{\left(\right. \frac{K}{x} \left.\right) \left(\right. \frac{N - K}{ n - x ,} \left.\right)}{\left(\right. \frac{N}{n} \left.\right)} x = 0 , 1 , \ldots , n$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = n \frac{K}{N}$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = n \frac{K}{N} \left(\right. 1 - \frac{K}{N} \left.\right) \frac{N - n}{N - 1}$$
- $$\text{4}. \sigma = \sqrt{ n \frac{K}{N} \left(\right. 1 - \frac{K}{N} \left.\right) \frac{N - n}{N - 1} }$$

##### Each expression summarizes a fundamental aspect of the hypergeometric distribution, capturing how it models the number of successes drawn without replacement, where its expected value lies, and how its variability is shaped by the sample size and the finite nature of the population.

## Mean of the hypergeometric distribution

The [mean](https://algebrica.org/introduction-to-the-mean/), or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/), of a hypergeometric distribution represents the average number of successes that can be expected when drawing a sample without replacement from a finite population. To compute the mean formally, we begin with the definition of the expected value:

$$\mu = E \left(\right. X \left.\right) = \sum_{x = 0}^{n} x P \left(\right. X = x \left.\right)$$

Substituting the probability mass function of the hypergeometric distribution gives:

$$E \left(\right. X \left.\right) = \sum_{x = 0}^{n} x \frac{\left(\right. \frac{K}{x} \left.\right) \left(\right. \frac{N - K}{ n - x } \left.\right)}{\left(\right. \frac{N}{n} \left.\right)}$$

To simplify this expression, we use a combinatorial identity that connects two related binomial coefficients by reducing both the number of available successes and the sample size by one:

$$x \left(\right. \frac{K}{x} \left.\right) = K \left(\right. \frac{K - 1}{ x - 1 } \left.\right)$$

Applying this identity to the summation yields:

$$E \left(\right. X \left.\right) = \frac{K}{\left(\right. \frac{N}{n} \left.\right)} \sum_{x = 1}^{n} \left(\right. \frac{K - 1}{ x - 1 } \left.\right) \left(\right. \frac{N - K}{ n - x } \left.\right)$$

We now recognize that the summation corresponds to the total probability of a hypergeometric distribution with parameters $N - 1$, $K - 1$, and sample size $n - 1$. Therefore, the summation equals:

$$\left(\right. \frac{N - 1}{ n - 1 } \left.\right)$$

Substituting this into the expression above gives:

$$E \left(\right. X \left.\right) = \frac{K}{\left(\right. \frac{N}{n} \left.\right)} \left(\right. \frac{N - 1}{ n - 1 } \left.\right)$$

Using the identity:

$$\frac{\left(\right. \frac{N - 1}{ n - 1 } \left.\right)}{\left(\right. \frac{N}{n} \left.\right)} = \frac{n}{N}$$

we obtain the final expression for the mean:

$$\mu = E \left(\right. X \left.\right) = n \frac{K}{N}$$

##### This result shows that the mean of a hypergeometric distribution depends on the sample size $n$ and on the proportion of successes in the population $K / N$. On average, we expect to observe a fraction $K / N$ of successes in any sample of size $n$, even though the draws are made without replacement.

## Variance of the hypergeometric distribution

The [variance](https://algebrica.org/variance-and-covariance-of-a-random-variable/) of a hypergeometric distribution measures how much the number of observed successes is expected to vary around the mean value $\mu = n K / N$. While the mean describes the central tendency of the distribution, the variance quantifies its spread, that is, how concentrated or dispersed the outcomes are when sampling without replacement from a finite population. Formally, the variance is defined as:

$$\sigma^{2} = Var \left(\right. X \left.\right) = E \left(\right. X^{2} \left.\right) - \left[\right. E \left(\right. X \left.\right) \left]\right.^{2}$$

To compute it, we recall that the hypergeometric experiment consists of drawing $n$ items without replacement from a finite population of size $N$ containing $K$ successes and $N - K$ failures. Although the draws are not independent, the variance can be derived by considering indicator variables for each draw. Let $X$ be the total number of successes in the sample, and let each draw be represented by an indicator variable:

$$X = X_{1} + X_{2} + \hdots + X_{n}$$

where $X_{i} = 1$ if the $I$-th draw is a success and $X_{i} = 0$ otherwise. Each indicator has expectation:

$$E \left(\right. X_{i} \left.\right) = \frac{K}{N}$$

and variance:

$$Var \left(\right. X_{i} \left.\right) = \frac{K}{N} \left(\right. 1 - \frac{K}{N} \left.\right)$$

However, because the sampling is done without replacement, each draw slightly changes the composition of the population. After a success is drawn, fewer successes remain, and after a failure is drawn, fewer failures remain. As a result, the draws influence one another, and the total variability is reduced compared with the binomial case. Taking this effect into account, the variance becomes:

$$Var \left(\right. X \left.\right) = n \frac{K}{N} \left(\right. 1 - \frac{K}{N} \left.\right) \frac{N - n}{ N - 1 }$$

Therefore, the variance of the hypergeometric distribution is:

$$\sigma^{2} = n \frac{K}{N} \left(\right. 1 - \frac{K}{N} \left.\right) \frac{N - n}{ N - 1 }$$

##### This expression shows how the spread of the distribution depends not only on the proportion of successes $K / N$, but also on the fact that sampling is done without replacement.

## Example 1

A batch contains 800 items, of which 12% are defective. An inspector selects a sample of 25 items for quality control. Determine the distribution of the random variable $X$ that counts the number of defective items found in the sample. Although this may look similar to a model with independent trials, the situation is different: once an item is selected, it is not placed back into the batch. The probability of drawing a defective item changes after each draw because the composition of the batch changes. For this reason, the draws are not independent.

The problem can be handled using basic combinatorial reasoning. The number of possible samples of 25 items that can be drawn from a batch of 800 is:

$$\left(\right. \frac{800}{25} \left.\right)$$

In the original batch, there are $0.12 \times 800 = 96$ defective items and $800 - 96 = 704$ non-defective items. The probability that the sample contains exactly $x$ defective items is:

$$P \left(\right. X = x \left.\right) = \frac{\left(\right. \frac{96}{x} \left.\right) \left(\right. \frac{704}{25 - x} \left.\right)}{\left(\right. \frac{800}{25} \left.\right)}$$

Thus, $X$ follows a hypergeometric distribution with parameters $N = 800$, $K = 96$, and $n = 25$.

## Comparison with the binomial distribution

The hypergeometric distribution is often compared to the [binomial distribution](https://algebrica.org/binomial-distribution/) because both describe the number of successes observed in a fixed number of trials. The essential difference lies in the sampling scheme.

- The binomial distribution assumes independent trials with a constant probability of success, as if each draw were taken from an infinite population or as if the sampled item were replaced before the next draw.
- The hypergeometric distribution, instead, models sampling without replacement from a finite population, so each draw slightly changes the composition of the remaining items. As a consequence, the probability of success varies across draws and the outcomes are not independent.

Despite these differences, the two distributions are closely related. When the population size $N$ is large compared with the sample size $n$, the effect of removing a few items becomes negligible. In this case, the hypergeometric distribution is well approximated by a binomial distribution with parameter $p = K / N$:

$$\text{Hyp} \left(\right. N , K , n \left.\right) \approx \text{Bin} \left(\right. n , \frac{K}{N} \left.\right)$$

##### This approximation highlights how the two models describe similar situations from different perspectives: the binomial focuses on idealized independent trials, while the hypergeometric captures the more realistic behavior of sampling from a finite population.

---

- **Sampling**
   Hypergeometric: without replacement
   Binomial: with replacement or independent trials
- **Probability of success**
   Hypergeometric: changes after each draw
   Binomial: remains constant
- **Independence**
   Hypergeometric: dependent draws
   Binomial: independent trials
- **Population**
   Hypergeometric: finite population explicitly matters
   Binomial: population treated as infinite or irrelevant
- **When it is used**
   Hypergeometric: batch sampling, quality control, card problems
   Binomial: repeated [Bernoulli experiments](https://algebrica.org/bernoulli-distribution/)
- **Conceptual idea**
   Hypergeometric: removing items alters future probabilities
   Binomial: each draw leaves probabilities unchanged
