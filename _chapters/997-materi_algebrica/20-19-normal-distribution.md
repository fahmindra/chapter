---
layout: chapter
title: "Normal Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 19
permalink: /materi-algebrica/probability-and-statistics/normal-distribution/
---

## Definition of the normal distribution

The **normal distribution**, also known as the Gaussian distribution, is one of the most important continuous probability distributions in both probability and statistics. It plays a central role in modeling real-world phenomena where values tend to cluster around a mean, following a characteristic bell-shaped curve. Mathematically, the normal distribution is defined by two parameters: the [mean](https://algebrica.org/introduction-to-the-mean/) $\mu$, which determines the center of the distribution, and the [standard deviation](https://algebrica.org/variance/) $\sigma$, which controls its spread. It is usually denoted as:

$$\mathcal{N} \left(\right. x ; \mu , \sigma \left.\right)$$

As previously introduced, the normal distribution has a distinctive bell-shaped form and follows a set of well-defined mathematical properties that make it unique among continuous probability distributions.

![](https://algebrica.org/wp-content/uploads/resources/images/normal-distribution-1.png)

- The total area under the curve equals $1$. This means that the integral of its probability density function over the entire real line, from $- \infty$ to $+ \infty$, is equal to $1$.
- The curve is symmetric around the mean $\mu$. In other words, it looks the same on both sides of the mean, with half of the total probability lying to the left and the other half to the right.
- The curve has two [inflection points](https://algebrica.org/maximum-minimum-and-inflection-points/), located at $x = \mu + \sigma$ and $x = \mu - \sigma$. At these points, the curvature of the graph [changes sign](https://algebrica.org/sign-analysis-in-inequalities/), marking the transition between the concave and convex regions of the distribution.
- The curve is asymptotic to the x-axis for values of $x$ that move farther away from the mean.

## Key features

- $$\text{1}. \mathcal{N} \left(\right. x ; \mu , \sigma \left.\right) = \frac{1}{\sigma \sqrt{2 \pi}} exp \left(\right. - \frac{\left(\right. x - \mu \left.\right)^{2}}{2 \sigma^{2}} \left.\right)$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = \mu$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = \sigma^{2}$$
- $$\text{4}. \sigma = \sigma$$

##### Each expression highlights a key property of the normal distribution, showing how its bell shape is fully determined by the mean $\mu$ and the standard deviation $\sigma$, which control its center and spread.

## Probability density function of the normal distribution

The random variable $X$ that follows a normal distribution is known as a normal random variable. It represents a [continuous random variable](https://algebrica.org/continuous-random-variables/) whose probabilities are described by the normal probability density [function](https://algebrica.org/functions), defined as:

$$\mathcal{N} \left(\right. x ; \mu , \sigma \left.\right) = \frac{1}{\sqrt{2 \pi} \sigma} e^{- \frac{1}{2 \sigma^{2}} \left(\right. x - \mu \left.\right)^{2}}$$

$$- \infty < x < + \infty$$

This function describes how probability is distributed over the possible values of the continuous random variable $X$, depending on the mean $\mu$ and the standard deviation $\sigma$. To explore in greater depth the concepts of the mean (or expected value), variance, and standard deviation of a random variable ([discrete](https://algebrica.org/discrete-random-variables/) or [continuous](https://algebrica.org/continuous-random-variables/)), refer to the following related topics:

- 1k [Mean or Expected Value of a Random Variable](https://algebrica.org/mean-or-expected-value-of-a-random-variable/)
- 981 [Variance and Covariance of a Random Variable](https://algebrica.org/variance-and-covariance-of-a-random-variable/)

---

As discussed above, the integral of the normal density function over the entire real line, from $- \infty$ to $+ \infty$, is equal to 1:

$$\frac{1}{\sqrt{2 \pi} \sigma} \int_{- \infty}^{+ \infty} e^{- \frac{1}{2 \sigma^{2}} \left(\right. x - \mu \left.\right)^{2}} d x = 1$$

From the integral it follows that, if we want to compute the area under the curve between two points $x_{0}$ and $x_{1}$, we must evaluate the [definite integral](https://algebrica.org/definite-integrals/) of the normal density function within that [interval](https://algebrica.org/intervals/).

![](https://algebrica.org/wp-content/uploads/resources/images/normal-distribution-2.png)

It follows intuitively that the shaded area under the curve represents the probability that the random variable $X$ assumes a value within the interval $\left[\right. x_{0} , x_{1} \left]\right.$. In other words, the integral of the normal density function over this range quantifies the likelihood of observing $X$ between those two limits. Formally, the probability that the random variable $X$ takes a value between $x_{0}$ and $x_{1}$ is given by:

$$P \left(\right. x_{0} < X < x_{1} \left.\right) & = \int_{x_{0}}^{x_{1}} n \left(\right. x ; \mu , \sigma \left.\right) d x \\ & = \frac{1}{\sqrt{2 \pi} \sigma} \int_{x_{0}}^{x_{1}} e^{- \frac{1}{2 \sigma^{2}} \left(\right. x - \mu \left.\right)^{2}} d x$$

## Standard normal distribution

To make probability calculations easier and more general, the normal distribution is often rewritten in a standardized form. In this process, the original variable $X$ is transformed into a new variable $Z$, defined as:

$$Z = \frac{X - \mu}{\sigma}$$

This new variable $Z$ follows what is called the **standard normal distribution**, a special case where the mean is $0$ and the standard deviation is $1$. By standardizing, we can work with a single universal curve and use [the standard normal Z table](https://algebrica.org/standard-normal-z-table/) to find probabilities, instead of computing the integral for each specific distribution. In practice, every normal distribution can be converted into the standard one, making comparisons and calculations much simpler.

##### The values reported in Z-tables represent the cumulative area under the standard normal curve to the left of a given $Z$ value.

---

Let us reconsider the case of the probability defined over a generic interval $\left[\right. x_{0} , x_{1} \left]\right.$. It can be expressed as:

$$P \left(\right. x_{0} < X < x_{1} \left.\right) & = \frac{1}{\sqrt{2 \pi} \sigma} \int_{x_{0}}^{x_{1}} e^{- \frac{1}{2 \sigma^{2}} \left(\right. x - \mu \left.\right)^{2}} d x$$

If we transform the variable $X$ into its standardized form, the interval $P \left(\right. x_{0} < X < x_{1} \left.\right)$ can be rewritten in terms of the standard variable $Z$ as:

$$P \left(\right. x_{0} < X < x_{1} \left.\right) = P \left(\right. \frac{x_{0} - \mu}{\sigma} < Z < \frac{x_{1} - \mu}{\sigma} \left.\right)$$

where the variable $X$ has been replaced by its standardized form $Z$, and the limits $x_{0}$ and $x_{1}$ have been replaced by their corresponding standardized values. This transformation allows us to express the probability in the standard normal framework, where $Z$ follows a distribution with mean $0$ and standard deviation $1$. Starting from the general form of the probability over an interval $\left[\right. x_{0} , x_{1} \left]\right.$ we have:

$$P \left(\right. x_{0} < X < x_{1} \left.\right) & = \frac{1}{\sqrt{2 \pi} \sigma} \int_{x_{0}}^{x_{1}} e^{- \frac{1}{2 \sigma^{2}} \left(\right. x - \mu \left.\right)^{2}} d x \\ & = \frac{1}{\sqrt{2 \pi} \sigma} \int_{z_{0}}^{z_{1}} e^{- \frac{1}{2} \left(\right. z \left.\right)^{2}} d x = P \left(\right. z_{0} < Z < z_{1} \left.\right)$$

This formulation highlights how the process of standardization provides a direct link between any normal distribution and the standard normal curve, enabling probabilities to be determined through universal reference values of $Z$.

## Three-sigma rule

In a normal distribution, probabilities are symmetrically arranged around the mean.
 There exists a fundamental relationship between these probabilities and their distance from the mean, known as the 68–95–99.7 rule or three-sigma rule, which describes how most of the probability mass is concentrated near the center of the distribution.

![](https://algebrica.org/wp-content/uploads/resources/images/normal-distribution-3.png)

- Approximately 68% of all values fall within one standard deviation of the mean, with about 34.1% on each side.
- Expanding the range to two standard deviations includes roughly 95% of the data
- Expanding the range to three standard deviations cover about 99.7% of all possible values.

## Central limit theorem

Let $X_{1} , X_{2} , \ldots , X_{n}$ be a sequence of independent and identically distributed random variables, each having an expected value $E \left[\right. X_{i} \left]\right. = \mu$ and a finite variance $Var \left(\right. X_{i} \left.\right) = \sigma^{2} > 0$. We define their sample mean as:

$$\bar{X}_{n} = \frac{1}{n} \sum_{i = 1}^{n} X_{i}$$

As the number of observations $n$ grows larger, the distribution of the standardized variable $Z$

$$Z = \frac{\bar{X}_{n} - \mu}{\sigma / \sqrt{n}}$$

gradually approaches the standard normal distribution in law, according to the relation:

$$\frac{\bar{X}_{n} - \mu}{\sigma / \sqrt{n}} \overset{d }{\rightarrow} \mathcal{N} \left(\right. x ; 0 , 1 \left.\right) \text{as} n \rightarrow \infty$$

In other words, regardless of the original distribution of the random variables the distribution of their mean tends to become approximately normal as the sample size increases. This result explains why the normal distribution appears so frequently in statistics: it acts as a limiting model for the behavior of averages when the number of observations is sufficiently large.

##### The notation $\overset{d }{\rightarrow}$ denotes “convergence in distribution”, meaning that the probability distribution of the standardized variable gradually approaches the standard normal distribution as $n$ increases.

## Selected references

- **L. Wasserman**. [All of Statistics (free PDF draft)](https://www.stat.cmu.edu/~larry/all-of-statistics/)
- **J. Blitzstein, J. Hwang**. [Introduction to Probability](https://projects.iq.harvard.edu/stat110/home)
- **MIT OpenCourseWare**. [Introduction to Probability and Statistics](https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2014/)
- **OpenStax**. [Introductory Statistics 2e](https://openstax.org/details/books/introductory-statistics-2e)
- **Penn State (STAT 414)**. [Probability Theory – Normal Distribution](https://online.stat.psu.edu/stat414/)
- **University of Berkeley**. [Statistics](https://www.stat.berkeley.edu/~stark/SticiGui/)
- **University of Oxford**. [Statistics Lecture Notes – Normal Distribution](https://www.stats.ox.ac.uk/~reinert/time/notesht10short.pdf)
- **NIST/SEMATECH**. [Engineering Statistics Handbook – Normal Distribution](https://www.itl.nist.gov/div898/handbook/eda/section3/eda3661.htm)
