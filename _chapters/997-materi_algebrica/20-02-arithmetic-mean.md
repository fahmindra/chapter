---
layout: chapter
title: "Arithmetic Mean"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 2
permalink: /materi-algebrica/probability-and-statistics/arithmetic-mean/
---

## What is the arithmetic mean?

The **arithmetic mean** is the most common and intuitive form of average. As a special case within the broader family of power means it expresses the representative value of a data set by dividing the total sum of all observations by their [number](https://algebrica.org/types-of-numbers/). Since it is grounded on additive aggregation, the arithmetic mean is ideal for describing quantities that combine linearly (for example, raw measurements or values that do not evolve proportionally or [exponentially](https://algebrica.org/exponential-function/)). In essence, it identifies the equilibrium point of the distribution, the value around which the data tend to balance.

---

In general form, the arithmetic mean is expressed as:

$$M_{a} = \frac{1}{n} \sum_{i = 1}^{n} x_{i}$$

where $x_{1} , x_{2} , \ldots , x_{n}$ are the observed values and $n$ is the total number of elements.

- The arithmetic mean can be applied to any set of [real numbers](https://algebrica.org/types-of-numbers/), including negative and zero values.
- Because it is sensitive to extreme values, the arithmetic mean can be distorted by outliers, making other means, like the median or [geometric mean](https://algebrica.org/geometric-mean), more appropriate in some cases.
- The arithmetic mean is always greater than or equal to the geometric mean.

## Example 1

Let’s consider the following data set of five numerical values and let’s calculate the arithmetic mean:

| $\mathbf{x} \mathbf{ᵢ}$ | **Values** |
| --- | --- |
| x₁ | 7.2 |
| x₂ | 4.8 |
| x₃ | 9.1 |
| x₄ | 5.5 |
| x₅ | 6.4 |

In this case, $n = 5$. Substituting the values, we get:

$$M_{a} = \frac{7.2 + 4.8 + 9.1 + 5.5 + 6.4}{5} = \frac{33.0}{5} = 6.6$$

Hence, the arithmetic mean of the series is approximately:
$$M_{a} = 6.6$$

## Weighted arithmetic mean

In some cases, not all data points contribute equally to the overall result. The weighted arithmetic mean extends the idea of the simple arithmetic mean by assigning a weight $w_{i}$ to each observation $x_{i}$, reflecting its relative importance or frequency within the dataset. It is defined as:

$$M_{a w} = \frac{\sum_{i = 1}^{n} w_{i} x_{i}}{\sum_{i = 1}^{n} w_{i}}$$

where $x_{i}$ are the observed values and $w_{i} > 0$ are their associated weights.

- The weighted arithmetic mean generalizes the simple arithmetic mean by introducing importance factors $w_{i}$.
- It ensures that larger or more relevant observations have a stronger influence on the final result.
- When all weights are equal, the weighted arithmetic mean reduces to the standard arithmetic mean.

## Example 2

Let’s consider a business case where a company wants to calculate the weighted arithmetic mean of its monthly sales. Each month has a different number of working days, which serve as the weights for the calculation.

| **Month** | $x_{i}$ **= daily sales in $** | $w_{i}$ **= working days** |
| --- | --- | --- |
| January | 420 | 20 |
| February | 380 | 22 |
| March | 460 | 18 |
| April | 400 | 21 |
| May | 440 | 19 |

By applying the formula of the weighted arithmetic mean, we obtain:

$$M_{a w} & = \frac{\left(\right. 420 \times 20 \left.\right) + \left(\right. 380 \times 22 \left.\right) + \left(\right. 460 \times 18 \left.\right) + \left(\right. 400 \times 21 \left.\right) + \left(\right. 440 \times 19 \left.\right)}{20 + 22 + 18 + 21 + 19} \\ & = \frac{8400 + 8360 + 8280 + 8400 + 8360}{100} \\ & = \frac{41800}{100} \\ & = 418$$

Hence, the weighted arithmetic mean of the company’s sales is $M_{a w} = 418$ $ per day.
