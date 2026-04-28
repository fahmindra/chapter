---
layout: chapter
title: "Sampling Distributions"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 25
permalink: /materi-algebrica/probability-and-statistics/sampling-distributions/
---

## From Populations to samples

A **sampling distribution** represents the distribution of a statistic obtained from all possible samples of a given size drawn from a population. In statistics, some problems, due to the size or complexity of the observable data, do not allow for a direct analysis of every element in a population.

For this reason, it becomes necessary to select a sample, that is, a smaller set of observations drawn from the population. A sample is a representative subset of the population, chosen randomly to minimize potential distortions or bias arising from other selection criteria. The process of selecting a sample is called sampling.

Inferential statistics uses samples to infer, from their observed characteristics, the properties or parameters of the entire population. A statistic is the value of a variable computed from the data of a sample. Examples of statistics include the sample mean, the sample variance, and the sample proportion. Sampling distributions describe how these values vary from one sample to another when the sampling process is repeated from the same population.

## Mean, mode, and median of a sampling distribution

Also for sampling distributions, it is possible to define the mean, mode, and median, each describing in a different way the central tendency of the distribution. The sample mean differs from the [simple arithmetic mean](https://algebrica.org/introduction-to-the-mean/) in that it represents the average of the observed values in a sample drawn from a population and is used as an estimate of the population mean. Unlike the arithmetic mean, which describes a fixed set of known data, the sample mean plays an inferential role, as it varies from one sample to another and follows its own sampling distribution.

---

In formal terms, the sample mean is defined as

$$\overset{―}{X} = \frac{1}{n} \sum_{i = 1}^{n} X_{i}$$

- $\overset{―}{X}$ represents the sample mean.
- $n$ is the sample size.
- $X_{i}$ denotes the value of the $i$-th observation in the sample.

For example, consider a sample $X$ consisting of $5$ observed values:

| $i$ | 1 | 2 | 3 | 4 | 5 |
| --- | --- | --- | --- | --- | --- |
| $X_{i}$ | 4 | 6 | 5 | 7 | 8 |

The sample mean is computed as

$$\overset{―}{X} = \frac{1}{n} \sum_{i = 1}^{n} X_{i} = \frac{1}{5} \left(\right. 4 + 6 + 5 + 7 + 8 \left.\right)$$

$$\overset{―}{X} = \frac{30}{5} = 6$$

Therefore, the sample mean is $\overset{―}{X} = 6$.

##### It is worth noting that this mean is representative only of the specific sample considered and not of all the possible samples that could be drawn from the population, nor of the population itself.

---

The sample mode, on the other hand, is the value that occurs most frequently within the sample. It represents the most common observation and provides an indication of where the sample values tend to cluster. Formally, the sample mode can be expressed as

$$Mode \left(\right. X \left.\right) = x_{k} : f \left(\right. x_{k} \left.\right) = \underset{x_{i}}{max} f \left(\right. x_{i} \left.\right)$$

- $X$ denotes the random variable representing the sample data.
- $f \left(\right. x_{i} \left.\right)$ denotes the frequency of the value $x_{i}$ in the sample
- $x_{k}$ is the observation that occurs most frequently.

Consider a sample $X$ consisting of 7 observed values:

| $i$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| $X_{i}$ | 4 | 6 | 5 | 6 | 8 | 6 | 7 |

The sample mode is the value that occurs most frequently within the sample. In this case, the value $6$ appears three times, more than any other observation. Therefore, the sample mode is $6$.

It is important to note that the mode is sensitive to the frequency of individual observations and may not be unique — multiple modes can exist if two or more values occur with the same highest frequency. In such cases, the distribution is referred to as multimodal.

---

The sample median, on the other hand, is defined as the middle value of the ordered sample.
 It divides the data set into two equal parts, with 50% of the observations below and 50% above this value. Formally, the sample median can be expressed as

$$\overset{\sim}{x} = \left{\right. x_{\frac{n + 1}{2}} , & \text{if} n \text{is odd} \\ \frac{1}{2} \left(\right. x_{\frac{n}{2}} + x_{\frac{n}{2} + 1} \left.\right) , & \text{if} n \text{is even}$$

- $x_{i}$ are the ordered observations of the sample.
- $n$ is the sample size.

Consider a sample $X$ consisting of 6 observed values:

| $i$ | 1 | 2 | 3 | 4 | 5 | 6 |
| --- | --- | --- | --- | --- | --- | --- |
| $X_{i}$ | 4 | 5 | 6 | 8 | 9 | 10 |

To find the sample median, the observations must first be ordered from smallest to largest (which they already are in this case). When the sample size $n$ is even, the median is calculated as the average of the two central values:

$$\overset{\sim}{x} = \frac{1}{2} \left(\right. x_{\frac{n}{2}} + x_{\frac{n}{2} + 1} \left.\right)$$

Substituting the corresponding values we have:

$$\overset{\sim}{x} = \frac{1}{2} \left(\right. x_{3} + x_{4} \left.\right) = \frac{1}{2} \left(\right. 6 + 8 \left.\right) = 7$$

Therefore, the sample median is $\overset{\sim}{x} = 7$.

##### The median is less sensitive to extreme values (outliers) compared to the mean, making it a more robust measure of central tendency in samples that contain skewed or non-symmetric data.

## Sample variance and sample standard deviation

The sample variance measures how the observations in a sample are distributed with respect to the sample mean. Larger values of variance indicate that the observations are spread out more widely around the mean, while smaller values indicate that they are more tightly clustered.
 Formally, given $X_{1} , X_{2} , \ldots , X_{n}$ [random variables](https://algebrica.org/discrete-random-variables/), the sample variance is defined as

$$S^{2} = \frac{1}{n - 1} \sum_{i = 1}^{n} \left(\right. X_{i} - \overset{―}{X} \left.\right)^{2}$$

- $S^{2}$ denotes the sample variance
- $\overset{―}{X}$ is the sample mean
- $n$ is the sample size.

The sample variance differs from the [simple variance](https://algebrica.org/variance/) because it divides by $n - 1$ instead of $n$, where $n - 1$ represents the degrees of freedom. This adjustment accounts for the fact that the sample mean, being used in the calculation, constrains one observation and leaves only $n - 1$ values free to vary. Dividing by $n - 1$ compensates for this constraint and ensures that the sample variance is an unbiased estimator of the population variance.

---

The sample variance can also be written in an equivalent computational form that avoids explicitly calculating the sample mean. This alternative expression is obtained by [expanding the squared differences](https://algebrica.org/notable-products/) and simplifying the terms of the variance formula:

$$S^{2} = \frac{1}{n \left(\right. n - 1 \left.\right)} \left[\right. n \sum_{i = 1}^{n} X_{i}^{2} - \left(\left(\right. \sum_{i = 1}^{n} X_{i} \left.\right)\right)^{2} \left]\right.$$

This formulation is particularly useful for manual calculations or when working with large data sets, as it reduces the need for repeated subtraction of the mean and minimizes rounding errors.

---

The sample standard deviation is defined as the [square root](https://algebrica.org/radicals/) of the sample variance $S^{2}$. It provides a measure of dispersion expressed in the same units as the data, indicating how much, on average, the observations deviate from the sample mean.
 Formally, it is expressed as

$$S = \sqrt{S^{2}} = \sqrt{\frac{1}{n - 1} \sum_{i = 1}^{n} \left(\right. X_{i} - \overset{―}{X} \left.\right)^{2}}$$

A smaller value of ( S ) indicates that the data points are closely clustered around the mean, whereas a larger value suggests greater variability within the sample.

## Sample range

The sample range is defined as the difference between the largest and smallest observed values within a sample. It provides a simple measure of dispersion that indicates the total spread of the data, though it is highly sensitive to extreme values. Formally, it can be expressed as

$$R = X_{\text{max}} - X_{\text{min}}$$

where $X_{\text{max}}$ and $X_{\text{min}}$ represent, respectively, the maximum and minimum observations in the sample.

## Connection with the normal distribution

As a consequence of the [Central Limit Theorem](https://algebrica.org/normal-distribution/), when the sample size $n$ becomes large, the distribution of the sample mean $\overset{―}{X}$ approaches a normal distribution with mean $\mu$ and variance $\frac{\sigma^{2}}{n}$. This can be expressed through the standardized variable

$$Z = \frac{\overset{―}{X} - \mu}{\sigma / \sqrt{n}}$$

which, for sufficiently large $n$, follows approximately the [standard normal distribution](https://algebrica.org/standard-normal-z-table/)

$$Z sim \mathcal{N} \left(\right. x ; 0 , 1 \left.\right)$$

regardless of the shape of the population distribution. There is no exact value of $n$ that guarantees normality, since the Central Limit Theorem describes an asymptotic behavior.
 However, in practice, the sample mean tends to be approximately normal when:

- $n \geq 30$ for most population distributions with finite variance.
- $n < 30$ if the population is already close to normal.
- $n > 50$ or $n > 100$ if the population is highly skewed or contains outliers.

##### In general, the larger the sample size, the closer the sampling distribution of the mean is to the normal distribution.

## Example 1

To show in practice how sampling distributions are connected to the normal distribution, consider a company that manufactures industrial machines whose operating lifespan follows a normal distribution with a mean of 5,000 hours and a standard deviation of 200 hours.
 We want to calculate the probability that a random sample of 25 machines has an average lifespan of less than 4,950 hours.

---

According to the Central Limit Theorem, the sampling distribution of $\overset{―}{X}$ will be approximately normal, with mean

$$\mu_{\overset{―}{X}} = 5000$$

and standard deviation

$$\sigma_{\overset{―}{X}} = \frac{\sigma}{\sqrt{n}} = \frac{200}{\sqrt{25}} = 40$$

For the observed sample mean $\overset{―}{X} = 4950$, we can apply the standardization formula to convert it into a corresponding $z$-score. The transformation from a sample mean to a standard normal variable is given by:

$$Z = \frac{\overset{―}{X} - \mu_{\overset{―}{X}}}{\sigma_{\overset{―}{X}}}$$

Substituting the known values, we obtain

$$z = \frac{4,950 - 5,000}{40} = \frac{- 50}{40} = - 1.25$$

This means that the sample mean of 4950 hours is 1.25 standard deviations below the expected population mean. We can therefore express the probability associated with the sample mean in terms of the standardized variable $Z$. By substituting the corresponding $z$-score, the probability becomes

$$P \left(\right. \overset{―}{X} < 4,950 \left.\right) = P \left(\right. Z < - 1.25 \left.\right)$$

Using the [standard normal Z table](https://algebrica.org/standard-normal-z-table/), we find that

$$P \left(\right. Z < - 1.25 \left.\right) = 0.1056$$

##### This means there is approximately a 10.56% probability that the sample of 25 machines will have an average lifespan shorter than 4,950 hours.
