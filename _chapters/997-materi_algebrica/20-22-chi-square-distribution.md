---
layout: chapter
title: "Chi-square Distribution"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 22
permalink: /materi-algebrica/probability-and-statistics/chi-square-distribution/
---

## From squared normals to the chi-square distribution

The **chi-square distribution** is a continuous probability distribution that arises from analyzing how the sum of squared observations behaves when those observations follow a standard normal distribution. More precisely, when we say that it comes from the sum of squares, we mean the following procedure:

- Consider a set of random variables that follow a [standard normal distribution](https://algebrica.org/normal-distribution), that is $Z_{1} , Z_{2} , \ldots , Z_{k}$ with distribution $\mathcal{N} \left(\right. x ; 0 , 1 \left.\right)$.
- Take the square of each observation: $Z_{1}^{2} , Z_{2}^{2} , \ldots , Z_{k}^{2}$. Squaring ensures that the values are always positive and reflects how far each observation is from zero.
- Sum all these squared values:
  $$X = \sum_{i = 1}^{k} Z_{i}^{, 2}$$
- The probability distribution that describes all the possible values of this sum is the chi-square distribution with $k$ degrees of freedom.

The parameter $k$ determines the shape of the distribution, influencing how much of the density is concentrated near zero and how much spreads toward larger values, as $k$ is the number of degrees of freedom.

## From the gamma to the chi-square distribution

Another way to derive the chi-square distribution is through the [gamma distribution](https://algebrica.org/gamma-distribution), of which it is a particular case. Recall that the gamma distribution with shape parameter $\alpha$ and scale parameter $\beta$ has density

$$G \left(\right. x ; \alpha , \beta \left.\right) = \left{\right. \frac{1}{\beta^{\alpha} \Gamma \left(\right. \alpha \left.\right)} x^{\alpha - 1} e^{- x / \beta} & x > 0 \\ 0 & x \leq 0$$

- The parameter $\alpha$ controls the shape of the distribution
- The parameter $\beta$ is the scale parameter and stretches the distribution horizontally.

If we set $\alpha = k / 2$ and $\beta = 2$, the gamma density reduces exactly to the form of the chi-square distribution with $k$ degrees of freedom. Therefore, the probability density function of the chi-square distribution is:

$$\chi^{2} \left(\right. x ; k \left.\right) = \left{\right. \frac{1}{2^{k / 2} \Gamma \left(\right. k / 2 \left.\right)} x^{ k / 2 - 1} e^{- x / 2} & x > 0 \\ 0 & x \leq 0$$

The behavior of the chi-square distribution is governed by the degrees of freedom $k$. As $k$ increases, the mode shifts to the right, the variance grows, and the distribution exhibits reduced skewness, gradually approaching a normal shape for large $k$.

![Chi-squared distribution.](https://algebrica.org/wp-content/uploads/resources/images/chi-squared-distribution.png "Chi-squared distribution.")

##### The chi-square distribution plays a central role in hypothesis testing and in the estimation of variance-related parameters, as it provides the theoretical foundation for many procedures that assess how well observed data agree with a statistical model and how much variability can be attributed to random fluctuations.

## Key features

- $$\text{1}. \chi^{2} \left(\right. x ; k \left.\right) = \frac{1}{2^{k / 2} \Gamma \left(\right. k / 2 \left.\right)} x^{ k / 2 - 1} e^{- x / 2} x > 0$$
- $$\text{2}. \mu = E \left(\right. X \left.\right) = k$$
- $$\text{3}. \sigma^{2} = Var \left(\right. X \left.\right) = 2 k$$
- $$\text{4}. \sigma = \sqrt{2 k}$$

##### Each expression summarizes a fundamental property of the chi-square distribution. The density describes how the distribution depends on the degrees of freedom $k$, the mean and variance quantify its location and spread, and the standard deviation highlights how dispersion grows as additional squared normal components are added.

## Sampling distribution of the sample variance

The [sampling distribution](https://algebrica.org/sampling-distributions/) of the sample variance describes the probabilistic behavior of the statistic $S^{2}$ when repeated samples are drawn from the same population. This concept is fundamental in statistical inference because it clarifies how the sample variance relates to the unknown population variance $\sigma^{2}$. Assume that:
$$X_{1} , X_{2} , \ldots , X_{n} sim N \left(\right. \mu , \sigma^{2} \left.\right)$$
are independent observations from a [normal distribution](https://algebrica.org/normal-distribution/). The sample variance is defined as
$$S^{2} = \frac{1}{n - 1} \sum_{i = 1}^{n} \left(\right. X_{i} - \bar{X} \left.\right)^{2}$$
where the divisor $n - 1$ accounts for the fact that the sample mean $\bar{X}$ is used as an estimate of $\mu$, reducing the degrees of freedom by one.

A result in mathematical statistics states that the standardized quantity:
$$\frac{\left(\right. n - 1 \left.\right) S^{2}}{\sigma^{2}}$$
follows a chi-square distribution with $n - 1$ degrees of freedom.
$$\frac{\left(\right. n - 1 \left.\right) S^{2}}{\sigma^{2}} sim \chi_{ n - 1}^{2}$$

This result arises from the structure of the normal model. When each observation is standardized, the deviations $\left(\right. X_{i} - \mu \left.\right) / \sigma$ behave like independent $\mathcal{N} \left(\right. x ; 0 , 1 \left.\right)$ variables. Squaring these deviations yields terms of the form $Z_{i}^{2}$, where $Z_{i} sim \mathcal{N} \left(\right. x ; 0 , 1 \left.\right)$, and the sum of such squared terms is precisely what defines a chi-square distribution.

---

In practice, the true mean $\mu$ is unknown and is replaced by the sample mean $\bar{X}$. This substitution introduces dependence among the deviations and reduces the number of independent squared terms from $n$ to $n - 1$, explaining the degrees of freedom of the resulting chi-square distribution. The identity:
$$\frac{\left(\right. n - 1 \left.\right) S^{2}}{\sigma^{2}} sim \chi_{, n - 1}^{2}$$
therefore characterizes the sampling distribution of the sample variance under normality.

##### The chi-square distribution provides the theoretical basis for inference about $\sigma^{2}$: it enables the construction of [confidence intervals](https://algebrica.org/confidence-intervals/) for the population variance and supports hypothesis tests that assess whether the observed sample variability is compatible with a hypothesized value of $\sigma^{2}$.

## Understanding chi-square critical values

Once we know that the statistic:
 $$\chi^{2} = \frac{\left(\right. n - 1 \left.\right) S^{2}}{\sigma^{2}}$$
follows a chi-square distribution with $k = n - 1$ degrees of freedom under normality, the next step is to determine whether the observed value of $\chi^{2}$ is compatible with a hypothesized population variance. To answer this, we need the critical values of the chi-square distribution, that is, the points $x$ satisfying:

$$P \left(\right. \chi_{k}^{2} \leq x \left.\right) = p$$

Because the chi-square distribution is asymmetric and lacks a simple closed-form inverse, its [quantiles](https://algebrica.org/median/) cannot be computed directly from an elementary formula. For this reason, just as one consults [z-tables](https://algebrica.org/standard-normal-z-table/) for the standard normal distribution, chi-square tables are used to look up the quantiles corresponding to specific probabilities and degrees of freedom.

When using these critical values, it is important to understand what they represent. In many statistical procedures, one is interested in the value $\chi_{\alpha}^{2}$ for which the area in the right tail of the chi-square distribution equals $\alpha$. This value satisfies:
$$P \left(\right. \chi_{k}^{2} > \chi_{\alpha}^{2} \left.\right) = \alpha$$
meaning that only a fraction $\alpha$ of the total probability lies to the right of the critical point.

![](https://algebrica.org/wp-content/uploads/resources/images/chi-squared-distribution-2.png)

The shaded region in the figure illustrates precisely this idea: the dark area corresponds to the probability $\alpha$, and the boundary between the shaded and unshaded regions marks the critical value $\chi_{\alpha}^{2}$.

---

An example of a chi-square table is shown below. The rows correspond to the degrees of freedom $k$, while the columns list several probability levels $p$, each associated with the corresponding chi-square quantile $\chi_{p}^{2}$. The entry at the intersection of a given row and column represents the real number $x$ such that $P \left(\right. \chi_{k}^{2} \leq x \left.\right) = p .$

These tables make it possible to locate the critical values required when constructing confidence intervals or performing hypothesis tests for a population variance. The fragment below illustrates the first few degrees of freedom together with commonly used probability levels; the ellipses indicate that both the rows and columns extend further.

| $k$ | $\chi_{.995}^{2}$ | $\chi_{.990}^{2}$ | $\chi_{.975}^{2}$ | $\chi_{.950}^{2}$ | $\chi_{.900}^{2}$ | … |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 0.000 | 0.000 | 0.001 | 0.004 | 0.016 | … |
| 2 | 0.010 | 0.020 | 0.051 | 0.103 | 0.211 | … |
| 3 | 0.072 | 0.115 | 0.216 | 0.352 | 0.584 | … |
| 4 | 0.207 | 0.297 | 0.484 | 0.711 | 1.064 | … |
| 5 | 0.412 | 0.554 | 0.831 | 1.145 | 1.610 | … |
| … | … | … | … | … | … | … |

##### Complete versions of chi-square tables are widely available online and in most statistical reference books, providing a full set of critical values for many degrees of freedom and probability levels.

These critical values are essential for constructing confidence intervals for the population variance. If we choose a confidence level of $1 - \alpha$, the parameter $\alpha$ represents the total probability excluded from the interval. In a two-tailed setting, this probability is split evenly between the two tails, so that each tail contains $\alpha / 2$. The central region of the chi-square distribution is therefore bounded by the two quantiles

$$\chi_{\alpha / 2 , k}^{2} \leq \chi^{2} \leq \chi_{1 - \alpha / 2 , k}^{2}$$

Here, $\chi_{p , k}^{2}$ denotes the $p$-th quantile of the chi-square distribution with $k$ degrees of freedom. If the computed statistic lies within these bounds, the sample variability is consistent with the hypothesized variance; if it falls outside, the data exhibit either too little or too much dispersion to be compatible with the assumed model.

## Example 1

A manufacturer of industrial pressure sensors reports that the output variability of its devices follows a normal distribution with a standard deviation of $\sigma = 0.8$ PSI (pounds per square inch). To verify whether the declared variability is plausible, an engineer decides to test four sensors selected at random (thus $n = 4$) and records their deviations from the nominal pressure. The measurements, together with the deviations from the sample mean, are summarized in the following table.

| Sensor | Measured deviation (PSI) | $X_{i} - \bar{X}$ | $\left(\right. X_{i} - \bar{X} \left.\right)^{2}$ |
| --- | --- | --- | --- |
| 1 | 0.5 | -0.075 | 0.0056 |
| 2 | 1.1 | 0.525 | 0.2756 |
| 3 | -0.2 | -0.775 | 0.6006 |
| 4 | 0.9 | 0.325 | 0.1056 |

To proceed with the analysis, the sample mean is first computed:

$$\bar{X} = \frac{0.5 + 1.1 - 0.2 + 0.9}{4} = 0.575$$

The next step is to compute the sample variance, which describes the dispersion of the observed deviations around the sample mean. Using the standard definition of the unbiased estimator of the variance, one obtains:

$$S^{2} = \frac{1}{n - 1} \sum_{i = 1}^{n} \left(\right. X_{i} - \bar{X} \left.\right)^{2} = \frac{1}{3} \left(\right. 0.9874 \left.\right) = 0.3291$$

The corresponding sample standard deviation is therefore

$$S = \sqrt{0.3291} \approx 0.574 \text{PSI}$$

which gives a first indication of the variability observed in this particular sample.

To formally assess whether these data are consistent with the manufacturer’s stated standard deviation of 0.8 PSI, the variability must be related to the chi-square distribution. Under the assumption that the population truly has variance $\sigma^{2} = 0.8^{2} = 0.64$, the statistic:

$$\chi^{2} = \frac{\left(\right. n - 1 \left.\right) S^{2}}{\sigma^{2}}$$

should follow a chi-square distribution with $n - 1 = 3$ degrees of freedom. Substituting the computed values gives:

$$\chi^{2} = \frac{3 \cdot 0.3291}{0.64} = 1.542$$

At this point, the observed value of the chi-square statistic must be compared with the [interval](https://algebrica.org/intervals/) that contains the central 95% of the $\chi_{3}^{2}$ distribution. The relevant bounds are:

$$0.215 \leq \chi^{2} \leq 7.815$$

Because the observed value $1.542$ falls inside this range, the sample does not exhibit unusual variability relative to what would be expected if the true standard deviation were indeed 0.8 PSI. In other words, the dispersion observed in the four tested sensors is entirely compatible with the manufacturer’s claim.
