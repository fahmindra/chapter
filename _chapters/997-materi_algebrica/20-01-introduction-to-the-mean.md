---
layout: chapter
title: "Introduction to the Mean"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 1
permalink: /materi-algebrica/probability-and-statistics/introduction-to-the-mean/
---

## The central behavior of a data distribution

The mean is among the most fundamental tools in statistics for describing the central behavior of a data distribution. It condenses a collection of observations into a single, informative value that reflects the typical level around which the data are distributed.
By summarizing the balance point of a dataset, the mean helps reveal its general trend and supports many methods of descriptive and inferential analysis.

---

A general formulation of the mean was proposed by Oscar Chisini in 1929. According to his definition, the mean of a set of numerical values is the number $M$ that, when substituted for each observation in a symmetric [function](https://algebrica.org/functions) $F$, leaves the overall result unchanged:

$$F \left(\right. x_{1} , x_{2} , \ldots , x_{n} \left.\right) = F \left(\right. M , M , \ldots , M \left.\right)$$

##### A function is symmetric if the order of the data does not matter; the function depends only on the values themselves, not on how they are arranged.

This abstract definition unifies the different types of means, such as the [arithmetic](https://algebrica.org/arithmetic-mean), [geometric](https://algebrica.org/geometric-mean), and [harmonic mean](https://algebrica.org/harmonic-mean) within a single conceptual framework. Each specific mean can be obtained by choosing a particular function $F$ that represents the relationship among the data values. If the function $F$ iis chosen as the sum of all data values, that is:

$$F \left(\right. x_{1} , x_{2} , \ldots , x_{n} \left.\right) = x_{1} + x_{2} + \hdots + x_{n}$$

then the general expression becomes:

$$x_{1} + x_{2} + \hdots + x_{n} = n M$$

From this relation we obtain the formula of the [arithmetic mean](https://algebrica.org/arithmetic-mean):

$$M = \frac{x_{1} + x_{2} + \hdots + x_{n}}{n} = \frac{1}{n} \sum_{i = 1}^{n} x_{i}$$

## The mean as the minimum substitution error

Another influential definition of the mean was introduced by Abraham Wald, who associated the concept of the mean with the idea of the substitution error. According to this approach, the mean is the value that minimizes the total error produced when all data points in a set are replaced by a single representative number. In essence, it identifies the point that yields the smallest possible discrepancy between the observed values and their common substitute. Mathematically, this can be expressed as:

$$M = arg ⁡ \underset{\mu}{min} \sum_{i = 1}^{n} \left(\right. x_{i} - \mu \left.\right)^{2}$$

The value $\mu$ that minimizes this expression corresponds to the arithmetic mean, which balances the squared deviations of the data.

## Hölder Mean

The Hölder mean, also known as the power mean or generalized mean, defines a family of means that includes the arithmetic, geometric, and harmonic mean as special cases. It is defined for positive values $x_{1} , x_{2} , \ldots , x_{n}$ as:

$$M_{s} = \left(\left(\right. \frac{1}{n} \sum_{i = 1}^{n} x_{i}^{s} \left.\right)\right)^{\frac{1}{s}}$$

For different values of $s$, the Hölder mean reproduces the main classical means.

- For $s = 1$ it corresponds to the arithmetic mean.
- For $s = 0$ it becomes the geometric mean.
- For $s = - 1$ it yields the harmonic mean.
- For $s = 2$ it represents the quadratic mean.

## List of the main means

- $$\text{1}. M_{1} = \frac{1}{n} \sum_{i = 1}^{n} x_{i}$$ [more](https://algebrica.org/arithmetic-mean)
- $$\text{2}. M_{1} = \frac{\sum_{i = 1}^{n} w_{i} x_{i}}{\sum_{i = 1}^{n} w_{i}}$$ [more](https://algebrica.org/arithmetic-mean)
- $$\text{3}. M_{0} = \left(\left(\right. \prod_{i = 1}^{n} x_{i} \left.\right)\right)^{\frac{1}{n}}$$ [more](https://algebrica.org/geometric-mean)
- $$\text{4}. M_{0} = \left(\left(\right. \prod_{i = 1}^{n} x_{i}^{w_{i}} \left.\right)\right)^{\frac{1}{\sum_{i = 1}^{n} w_{i}}}$$ [more](https://algebrica.org/geometric-mean)
- $$\text{5}. M_{- 1} = \frac{n}{\sum_{i = 1}^{n} \frac{1}{x_{i}}}$$ [more](https://algebrica.org/harmonic-mean)
- $$\text{6}. M_{2} = \left(\left(\right. \frac{1}{n} \sum_{i = 1}^{n} x_{i}^{2} \left.\right)\right)^{\frac{1}{2}}$$ [more](https://algebrica.org/root-mean-square)

##### Each formula represents a specific way of summarizing a dataset, depending on how the individual values contribute to the final result. While all means describe central tendency, their interpretation varies with the mathematical operation that defines them.

## When to use each mean

- [Arithmetic mean](https://algebrica.org/arithmetic-mean) ($M_{1}$): used when values combine additively, such as totals of quantities like income, length, or temperature. It expresses the point of balance of a dataset, where each observation contributes equally to the result.
- [Weighted arithmetic mean](https://algebrica.org/arithmetic-mean) ($M_{1}$ weighted): applied when some data points have more relevance or occur more frequently than others. Each observation is multiplied by a weight that reflects its importance before computing the average.
- [Geometric mean](https://algebrica.org/geometric-mean) ($M_{0}$): suitable for quantities that combine multiplicatively, such as growth factors, returns, or indices. It describes the representative rate of change over time, showing how values scale proportionally.
- [Weighted geometric mean](https://algebrica.org/geometric-mean) ($M_{0}$ weighted): used when multiplicative data have different levels of importance. Common in finance or performance analysis, where certain elements influence the result more than others.
- [Harmonic mean](https://algebrica.org/harmonic-mean) ($M_{- 1}$): appropriate for averaging rates, speeds, or ratios where smaller values should weigh more. It reflects the true mean rate when the total distance, quantity, or workload remains constant.
- [Quadratic mean](https://algebrica.org/root-mean-square) ($M_{2}$): chosen when values combine quadratically, as in the case of voltages, accelerations, or power. It highlights the effective magnitude of the data by giving greater influence to larger variations.

## Mean or expected value of a random variable

In the case of [discrete random variables](https://algebrica.org/discrete-random-variables), the mean or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/) is calculated as the sum of all possible values of $X$ weighted by their probabilities:

$$\mu = E \left(\right. X \left.\right) = \underset{x}{\sum} x f \left(\right. x \left.\right)$$

In the case of [continuous random variables](https://algebrica.org/continuous-random-variables), the mean is obtained by integrating each possible value of $X$ weighted by its probability density over the entire range:

$$\mu = E \left(\right. X \left.\right) = \int_{- \infty}^{+ \infty} x f \left(\right. x \left.\right) d x$$

##### Both forms express the same underlying idea: the mean reflects where the values of a random variable tend to cluster. In the discrete case it is found by summing over all possible outcomes, while in the continuous case the same principle extends smoothly through integration.

## Mean of a sampling distribution

The [sample mean](https://algebrica.org/sampling-distributions/) represents the average value of observations in a sample drawn from a population and serves as an estimate of the population mean. It is defined as

$$\overset{―}{X} = \frac{1}{n} \sum_{i = 1}^{n} X_{i}$$

where $\overset{―}{X}$ is the sample mean, $n$ is the sample size, and $X_{i}$ represents the value of the $I$-th observation in the sample.
