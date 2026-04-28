---
layout: chapter
title: "Median and Quantiles"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 6
permalink: /materi-algebrica/probability-and-statistics/median-and-quantiles/
---

## The central position in a data distribution

The median is a key measure of central tendency used to describe the typical value within a dataset. While the [mean](https://algebrica.org/introduction-to-the-mean) expresses the numerical balance of all values, the median focuses instead on position, it identifies the value that divides the ordered data into two equally sized groups. Half of the observations fall below the median, and half lie above it. Because it depends only on the relative ordering of the data, the median remains stable in the presence of extreme values. This makes it especially useful when the distribution is skewed or when outliers would otherwise distort the [arithmetic mean](https://algebrica.org/arithmetic-mean).

---

A formal definition of the median can be expressed as follows: Let $n$ numerical observations be arranged in ascending order:

$$x_{1} \leq x_{2} \leq \hdots \leq x_{n}$$

If $n$ is odd, the median corresponds to the central element of the sequence:

$$\overset{\sim}{M} = x_{\left(\right. \frac{n + 1}{2} \left.\right)}$$

If $n$ is even, it is defined as the average of the two middle values:

$$\overset{\sim}{M} = \frac{x_{\left(\right. \frac{n}{2} \left.\right)} + x_{\left(\right. \frac{n}{2} + 1 \left.\right)}}{2}$$

##### This definition ensures that the number of data points smaller than the median equals the number that are larger, providing a perfectly balanced partition of the dataset.

## Example 1

To illustrate how the median is calculated when the number of observations is odd, let’s look at a simple example showing the monthly salaries of seven employees working in the same company:

| Employee $x_{i}$ | Salary ($) |
| --- | --- |
| $x_{1}$ | 1,200 |
| $x_{2}$ | 1,300 |
| $x_{3}$ | 1,400 |
| $x_{4}$ | 1,500 |
| $x_{5}$ | 3,000 |
| $x_{6}$ | 3,200 |
| $x_{7}$ | 4,000 |

Since there are $n = 7$ observations, the median is the value that occupies the central position:

$$\overset{\sim}{M} = x_{\left(\right. \frac{n + 1}{2} \left.\right)} = x_{4}$$

The fourth value in the ordered list is 1,500, so the median is $\overset{\sim}{M} = 1 , 500$.

##### This means that half of the employees earn less than $ 1,500, and the other half earn more.

## A distance-based definition of the median

The median can be described as the point that minimizes the total absolute deviation of all observations:

$$\overset{\sim}{M} = arg ⁡ \underset{m}{min} \sum_{i = 1}^{n} \left|\right. x_{i} - m \left|\right.$$

where $\left|\right. x_{i} - m \left|\right.$ is the sum of absolute deviations. This property emphasizes that the median identifies the value that best captures the central location of a distribution when balance is defined in terms of distances instead of averages. Because it is less affected by extreme values, the median is often preferred when data are skewed or contain outliers.

---

Let’s apply this property to the data from Example 1, where the salaries (in dollars) are:

$$1200 , 1300 , 1400 , 1500 , 3000 , 3200 , 4000$$

We compute the total absolute deviation for several possible values of $m$.

For $m = 1200$ we have $\sum_{i = 1}^{n} \left|\right. x_{i} - m \left|\right.$:
$$& = \left|\right. 1200 - 1200 \left|\right. + \\ & + \left|\right. 1300 - 1200 \left|\right. \\ & + \left|\right. 1400 - 1200 \left|\right. \\ & + \left|\right. 1500 - 1200 \left|\right. \\ & + \left|\right. 3000 - 1200 \left|\right. \\ & + \left|\right. 3200 - 1200 \left|\right. \\ & + \left|\right. 4000 - 1200 \left|\right. \\ & = 7 , 100$$

For $m = 1300$ we have $\sum_{i = 1}^{n} \left|\right. x_{i} - m \left|\right.$:
$$& = \left|\right. 1200 - 1300 \left|\right. + \\ & + \left|\right. 1300 - 1300 \left|\right. \\ & + \left|\right. 1400 - 1300 \left|\right. \\ & + \left|\right. 1500 - 1300 \left|\right. \\ & + \left|\right. 3000 - 1300 \left|\right. \\ & + \left|\right. 3200 - 1300 \left|\right. \\ & + \left|\right. 4000 - 1300 \left|\right. \\ & = 6 , 700$$

Iterating the same procedure for each value of $m$ gives the following total results.

| $m$ | $S \left(\right. m \left.\right) = \sum \left|\right. x_{i} - m \left|\right.$ |
| --- | --- |
| 1200 | 7,100 |
| 1300 | 6,700 |
| 1400 | 6,400 |
| 1500 | 6,300 |
| 3000 | 7,800 |
| 3200 | 8,400 |
| 4000 | 12,400 |

The median is therefore $1500$, as this value minimizes the total sum of absolute deviations, with $S \left(\right. m \left.\right) = 6300$ being the smallest among all those computed.

## Example 2

Let’s now consider another example, this time with an even number of observations. The dataset shows the selling prices of six houses recently sold in the same neighborhood:

| House $x_{i}$ | Price $ |
| --- | --- |
| $x_{1}$ | 180,000 |
| $x_{2}$ | 190,000 |
| $x_{3}$ | 200,000 |
| $x_{4}$ | 220,000 |
| $x_{5}$ | 300,000 |
| $x_{6}$ | 450,000 |

Since there are $n = 6$ observations, the median is given by the average of the two central values:

$$\overset{\sim}{M} = \frac{x_{\left(\right. \frac{n}{2} \left.\right)} + x_{\left(\right. \frac{n}{2} + 1 \left.\right)}}{2} = \frac{x_{3} + x_{4}}{2}$$

Substituting the corresponding values:

$$\overset{\sim}{M} = \frac{200 , 000 + 220 , 000}{2} = 210 , 000$$

The median house price is $ 210,000.

##### This means that half of the houses were sold for less than $ 210,000 and the other half for more.

## Example 3

Let’s now consider a slightly more complex case, where data are organized into frequency classes. When data are grouped into classes, the median is obtained by interpolation within the median class, providing an estimated measure of the central tendency of the distribution. The following table shows the monthly household electricity consumption (in kWh) for a group of families, grouped into four classes:

| Class interval (kWh) | Frequency ($f_{i}$) |
| --- | --- |
| (100, 200] | 5 |
| (200, 300] | 8 |
| (300, 400] | 12 |
| (400, 500] | 5 |

The total number of observations is:

$$n = \sum f_{i} = 5 + 8 + 12 + 5 = 30$$

To find the median, we first determine the class that contains the middle observation. Since $n = 30$, the middle position is:

$$\frac{n}{2} = \frac{30}{2} = 15$$

We now determine the cumulative frequencies, which represent the progressive total of observations up to each class. In this example, the cumulative frequency allows us to locate the class that contains the middle observation (that is, the median class) from which the value of the median will be computed.

| Class interval (kWh) | Frequency ($f_{i}$) | Cumulative frequency |
| --- | --- | --- |
| (100, 200] | 5 | 5 |
| (200, 300] | 8 | 13 |
| (300, 400] | 12 | 25 |
| (400, 500] | 5 | 30 |

The 15th observation falls into the class (300, 400], which is therefore the median class. The median for grouped data is given by:

$$\overset{\sim}{M} = L + \left(\right. \frac{\frac{n}{2} - F}{f_{m}} \left.\right) \times c$$

where:

- $L$ = lower boundary of the median class
- $F$ = cumulative frequency before the median class
- $f_{m}$ = frequency of the median class
- $c$ = class width

Substituting the values we obtain:

$$L = 300 , F = 13 , f_{m} = 12 , c = 100$$

$$\overset{\sim}{M} = 300 + \left(\right. \frac{15 - 13}{12} \left.\right) \times 100 = 300 + \left(\right. \frac{2}{12} \times 100 \left.\right) = 316.7$$

The median electricity consumption is approximately 317 kWh.

##### This means that half of the families consume less than 317 kWh per month, and the other half consume more.

## Median and quantiles

The median is a particular case of the **quantiles**, statistical measures that divide a distribution into equal parts. Specifically, the median corresponds to the quantile that separates the lower 50% of observations from the upper 50%, and it is therefore denoted as the quantile $x_{0.5}$.

To introduce the concept of a quantile, we begin by considering a real number $p$ such that $0 < p < 1$. This parameter identifies the proportion of observations lying below a specific threshold within a distribution. The corresponding value, denoted by $x_{p}$, is called the quantile of order $p$ and represents the point that divides the data in such a way that a fraction $p$ of the observations are less than or equal to it, and the remaining $1 - p$ are greater.

From an analytical perspective, the quantile $x_{p}$ can also be defined as the value that minimizes a global loss function obtained from the sum of asymmetric deviations:

$$g \left(\right. x_{i} , \bar{x} \left.\right) = \left{\right. \left(\right. 1 - p \left.\right) \left|\right. x_{i} - \bar{x} \left|\right. & \text{if} x_{i} \leq \bar{x} \\ p \left|\right. x_{i} - \bar{x} \left|\right. & \text{if} x_{i} > \bar{x}$$

Commonly used quantiles include:

- $x_{0.25}$, first quartile, that identifies the value below which lies $1 / 4$ of the distribution.
- $x_{0.50}$, median, that divides the data into two equal halves $1 / 2$.
- $x_{0.75}$, third quartile, that marks the value below which lies $3 / 4$ of the observations.

---

The **interquantile range** is a measure of statistical dispersion that expresses the spread of the central portion of a distribution. It is defined as the difference between two quantiles of order $p_{1}$ and $p_{2}$ $\left(\right. 0 < p_{1} < p_{2} < 1 \left.\right)$:

$$I Q R = x_{p_{2}} - x_{p_{1}}$$

When the two quantiles correspond to the first and third quartiles, that is $p_{1} = 0.25$ and $p_{2} = 0.75$, the interquantile range becomes:

$$I Q R = x_{0.75} - x_{0.25}$$

This interval contains the central 50% of the observations and is particularly useful for describing the variability of a dataset in a way that is robust to outliers, since it ignores the extreme values located in the tails of the distribution.

## Example 4

Let’s consider a small dataset representing the monthly salaries of ten employees in a company:

| $i$ | $x_{i}$ (Salary in $) |
| --- | --- |
| 1 | 2,200 |
| 2 | 2,400 |
| 3 | 2,600 |
| 4 | 2,700 |
| 5 | 2,800 |
| 6 | 2,900 |
| 7 | 3,100 |
| 8 | 3,300 |
| 9 | 3,400 |
| 10 | 3,700 |

Since there are $n = 10$ observations, we can compute the positions of the first and third quartiles as:

$$Q_{1} = x_{0.25} = x_{\left(\right. n + 1 \left.\right) \times 0.25} = x_{2.75}$$
$$Q_{3} = x_{0.75} = x_{\left(\right. n + 1 \left.\right) \times 0.75} = x_{8.25}$$

These positions correspond to fractional ranks, so we interpolate between the nearest observations.

$x_{2.75}$ lies between the 2nd and 3rd values:
 $$x_{0.25} = 2400 + 0.75 \times \left(\right. 2600 - 2400 \left.\right) = 2400 + 150 = 2550$$

$x_{8.25}$ lies between the 8th and 9th values:
 $$x_{0.75} = 3300 + 0.25 \times \left(\right. 3400 - 3300 \left.\right) = 3300 + 25 = 3325$$

We now calculate the interquantile range between the third and the first quantile. We obtain:

$$I Q R = x_{0.75} - x_{0.25} = 3325 - 2550 = 775$$

The interquantile range is 775 dollars.

##### This means that the central 50% of the employees have salaries that fall within a range of 775 dollars.
