---
layout: chapter
title: "Geometric Mean"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 3
permalink: /materi-algebrica/probability-and-statistics/geometric-mean/
---

## What is the geometric mean?

The **geometric mean** belongs to the family of power means. Unlike the simple [arithmetic mean](https://algebrica.org/arithmetic-mean/), it is based on the product of the elements rather than their sum, making it especially useful for measuring average rates of growth, returns over time, or quantities that vary multiplicatively. It captures the central tendency of data that evolves through proportional or percentage changes, offering a more accurate representation than the arithmetic mean when dealing with ratios, indices, or compound phenomena.

---

In general form, the geometric mean is expressed as:

$$M_{g} = \left(\left(\right. \prod_{i = 1}^{n} x_{i} \left.\right)\right)^{\frac{1}{n}}$$

where $x_{1} , x_{2} , \ldots , x_{n}$ are positive values and $n$ is the total number of elements.

- The geometric mean can only be applied to a set of values whose overall product is positive, since the calculation involves both multiplication and the extraction of a [root](https://algebrica.org/radicals/).
- Because it operates on products, the geometric mean is closely related to [exponential growth](https://algebrica.org/exponential-function/).
- The geometric mean is always less than or equal to the arithmetic mean.

## Geometric mean logarithmic form

Another useful way to express the geometric mean is through its [logarithmic](https://algebrica.org/logarithms/) form. In this representation, the geometric mean of a set of positive values $x_{1} , x_{2} , \ldots , x_{n}$ can be written as:

$$M_{g} = exp ⁡ \left(\right. \frac{1}{n} \sum_{i = 1}^{n} ln ⁡ x_{i} \left.\right)$$

- By taking logarithms, products are transformed into sums and exponents into multipliers, which greatly simplifies both computation and interpretation.
- This formula shows that the geometric mean is the exponential of [arithmetic mean](https://algebrica.org/arithmetic-mean) of the logarithms of the data values.
- The logarithmic form is especially convenient when dealing with numbers that span several orders of magnitude or when direct multiplication might cause computational issues.

## Example 1

Let’s consider the following data set of five positive values:

| $\mathbf{x}_{\mathbf{i}}$ | Values |
| --- | --- |
| $x_{1}$ | 2.0 |
| $x_{2}$ | 3.5 |
| $x_{3}$ | 4.0 |
| $x_{4}$ | 5.5 |
| $x_{5}$ | 6.0 |

In this case, $n = 5$. Substituting the values, we get:

$$M_{g} = \left(\right. 2.0 \times 3.5 \times 4.0 \times 5.5 \times 6.0 \left.\right)^{\frac{1}{5}}$$

$$M_{g} = \left(\right. 924 \left.\right)^{\frac{1}{5}} \approx 3.93$$

##### The geometric mean provides a sense of the typical multiplicative value within a dataset.While the arithmetic mean of these numbers is $\left(\right. 2.0 + 3.5 + 4.0 + 5.5 + 6.0 \left.\right) / 5 = 4.2$, the geometric mean is slightly lower ($3.93$) because it gives less weight to higher values and more to lower ones.

Hence, the geometric mean of the series is approximately:

$$M_{g} \approx 3.93$$

## Example 2

Let’s see how the geometric mean can be applied to determine the overall average return of a stock over a given period. In finance, investment returns combine multiplicatively rather than additively, each month’s performance compounds with the previous ones, influencing the total outcome in a nonlinear way. The geometric mean naturally reflects this compounding effect, offering a more accurate measure of an asset’s true average growth rate than the arithmetic mean.

---

In the following example, we’ll calculate the geometric mean of Tesla’s monthly returns for the first five months of 2025 to estimate its average monthly performance across the period.

| Month (2025) | Return |
| --- | --- |
| January | +12.4% |
| February | –3.8% |
| March | +7.6% |
| April | +2.1% |
| May | +4.5% |

When dealing with percentage returns, direct multiplication can quickly lead to very small or misleading values, especially when negative returns are involved. To handle this correctly, each percentage return $x_{i}$ is first converted into a growth factor by adding $1$ (that is, $1 + x_{i}$). These factors are then multiplied together, the $n$-th root is taken, and finally, 1 is subtracted to bring the result back to percentage form.

$$M_{g} = \left(\left[\right. \prod_{i = 1}^{n} \left(\right. 1 + x_{i} \left.\right) \left]\right.\right)^{\frac{1}{n}} - 1$$

---

By considering the values for the five periods, we obtain:

$$M_{g} & = \left(\left[\right. \left(\right. 1.124 \left.\right) \times \left(\right. 0.962 \left.\right) \times \left(\right. 1.076 \left.\right) \times \left(\right. 1.021 \left.\right) \times \left(\right. 1.045 \left.\right) \left]\right.\right)^{\frac{1}{5}} - 1 \\ & = 1.0442 - 1 \\ & = 0.0442 \\ & = 4.42 \%$$

Therefore, the average monthly return of Tesla’s stock over the first five months of 2025 was approximately $4.4 \%$.

## Weighted geometric mean

In some cases, not all data points contribute equally to the overall result. The weighted geometric mean extends the idea of the standard geometric mean by assigning a weight $w_{i}$ to each observation $x_{i}$, reflecting its relative importance or frequency within the dataset. It is defined as:

$$M_{g w} = \left(\left(\right. \prod_{i = 1}^{n} x_{i}^{w_{i}} \left.\right)\right)^{\frac{1}{\sum_{i = 1}^{n} w_{i}}}$$

where $x_{i} > 0$ are the observed values and $w_{i} > 0$ are their associated weights.

- The weighted geometric mean generalizes the simple geometric mean by introducing importance factors $w_{i}$.
- It ensures that larger or more relevant observations have a stronger influence on the final result.
- When all weights are equal, the weighted geometric mean reduces to the standard geometric mean.

## Example 3

Let’s consider the same Tesla example as above, this time applying a set of arbitrary weights chosen according to the rationale shown in the note.

| Month | Return | Weight |
| --- | --- | --- |
| January | +12.4% | 3 |
| February | –3.8% | 1 |
| March | +7.6% | 2 |
| April | +2.1% | 1 |
| May | +4.5% | 3 |

##### January, strong growth period, higher importance. February, Negative month, lower importance. March, partial recovery, medium weight. April, stable month, limited impact. May, positive performance, higher importance.

---

We now calculate the weighted geometric mean, taking into account the growth factors $\left(\right. 1 + x_{i} \left.\right)$ and the corresponding weights $w_{i}$ assigned to each observation. We obtain:

$$M_{g w} & = \left(\left[\right. \left(\right. 1.124 \left.\right)^{3} \times \left(\right. 0.962 \left.\right)^{1} \times \left(\right. 1.076 \left.\right)^{2} \times \left(\right. 1.021 \left.\right)^{1} \times \left(\right. 1.045 \left.\right)^{3} \left]\right.\right)^{\frac{1}{10}} - 1 \\ & = \left(\right. 1.5566 \left.\right)^{0.1} - 1 \\ & = 1.0455 - 1 \\ & = 0.0455 \\ & = 4.55 \%$$

##### In this case, the exponent $\frac{1}{10}$ is obtained as the reciprocal of the sum of all weights.Since the weights assigned to each month are $w_{i} = 3 , 1 , 2 , 1 , 3$, their total is $\sum w_{i} = 10$.

Therefore, after applying the chosen weights, Tesla’s weighted average monthly return for the first five months of 2025 was approximately $4.55 \%$ slightly higher than the unweighted value due to the greater influence of months with positive performance.
