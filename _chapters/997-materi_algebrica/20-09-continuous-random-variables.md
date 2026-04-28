---
layout: chapter
title: "Continuous Random Variables"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 9
permalink: /materi-algebrica/probability-and-statistics/continuous-random-variables/
---

## Definition of a continuous random variable

A **continuous random variable** is a function that assigns a real number to each element of a continuous sample space. Unlike [discrete random variables](https://algebrica.org/discrete-random-variables), it can take on infinitely many values within a given interval. Formally, a continuous random variable is a function:

$$X : \Omega \rightarrow \mathbb{R}$$

where $\Omega$ is a continuous sample space composed of infinitely many outcomes that can vary smoothly. In this case, probabilities are not assigned to individual values but to intervals of values, and they are determined through a probability density function.

---

A continuous random variable has the special property that the probability of it assuming any precise value is zero.

$$P \left(\right. X = x_{0} \left.\right) = 0$$

What matters instead is the probability of the variable falling within a given range of values. In general, therefore, when $X$ is a continuous random variable, the probability of it taking any specific value is zero, and we have:

$$P \left(\right. a < X \leq b \left.\right) = P \left(\right. a < X < b \left.\right) + P \left(\right. X = b \left.\right)$$

Since $P \left(\right. X = b \left.\right) = 0$ we have:

$$P \left(\right. a < X \leq b \left.\right) = P \left(\right. a < X < b \left.\right)$$

##### This means that, for continuous random variables, the exact endpoints of the interval are insignificant. The probability remains the same whether the bounds are included or not.

## Probability from the density function

To determine the probability distribution of a continuous random variable $X$ within a general interval $\left(\right. a , b \left.\right)$, it is necessary to compute the following [definite integral](https://algebrica.org/definite-integrals/):

$$P \left(\right. a < X < b \left.\right) = \int_{a}^{b} f \left(\right. x \left.\right) d x$$

The resulting probability corresponds to the area under the curve of the probability density function $f \left(\right. x \left.\right)$ between the limits $a$ and $b$.

![](https://algebrica.org/wp-content/uploads/resources/images/continuous-random-vars-1.png)

---

To describe a continuous probability distribution, we use a **probability density function** $f \left(\right. x \left.\right)$. This function defines how the probability is distributed across the possible values of the random variable $X$. A function $f \left(\right. x \left.\right)$ qualifies as a valid probability density if it satisfies the following conditions:

$$& f \left(\right. x \left.\right) \geq 0 , \text{for all} x \in \mathbb{R} \\ & \int_{- \infty}^{+ \infty} f \left(\right. x \left.\right) , d x = 1 \\ & P \left(\right. a < X < b \left.\right) = \int_{a}^{b} f \left(\right. x \left.\right) d x$$

These conditions ensure that the density function is always non-negative, that the total probability over the entire real line equals one, and that probabilities for any interval can be obtained by integration.

Unlike [discrete random variables](https://algebrica.org/discrete-random-variables), which assign probabilities to individual outcomes through a probability mass function (PMF), continuous random variables are described by a probability density function (PDF). In this case, probabilities are not tied to specific points but to areas under the curve, representing the likelihood of the variable falling within a given interval.

## Cumulative distribution function

As with discrete random variables, it is also possible to define a cumulative distribution function $F \left(\right. x \left.\right)$ for a continuous random variable $X$ with a probability density function $f \left(\right. x \left.\right)$. The cumulative distribution function represents the probability that the variable $X$ takes on a value less than or equal to $x$. Formally, for a variable $X$, the cumulative distribution function is defined as:

$$F \left(\right. x \left.\right) = P \left(\right. X \leq x \left.\right) = \int_{- \infty}^{x} f \left(\right. t \left.\right) d t$$

It describes how probability accumulates from the left tail of the distribution up to the point $x$. Considering a general interval $\left(\right. a , b \left.\right)$ like the one shown in the previous figure, the probability that the variable $X$ takes a value within that range is given by:

$$P \left(\right. a < X < b \left.\right) = F \left(\right. b \left.\right) - F \left(\right. a \left.\right)$$

where $F \left(\right. b \left.\right)$ and $F \left(\right. a \left.\right)$ represent the values of the cumulative distribution function that is the [antiderivative](https://algebrica.org/definite-integrals/) of the density function evaluated at the upper and lower limits of the interval.

## Joint probability density function

In the case of two continuous random variables $X$ and $Y$, we can describe how their probabilities are distributed together through a joint probability density function $f \left(\right. x , y \left.\right)$. The term joint indicates that the function represents the combined behavior of both variables that is, how the probability is shared across different pairs of values $\left(\right. x , y \left.\right)$ in the two-dimensional plane. It allows us to study the relationship between $X$ and $Y$, including whether they are independent or correlated.

A function $f \left(\right. x , y \left.\right)$ is a valid joint probability density function if it satisfies the following conditions:

$$& f \left(\right. x , y \left.\right) \geq 0 , \forall \left(\right. x , y \left.\right) \\ & \int_{- \infty}^{+ \infty} \int_{- \infty}^{+ \infty} f \left(\right. x , y \left.\right) d x d y = 1 \\ & P \left[\right. \left(\right. X , Y \left.\right) \in A \left]\right. = \int \int_{A} f \left(\right. x , y \left.\right) d x d y$$

---

Starting from the joint probability density function $f_{X , Y} \left(\right. x , y \left.\right)$, it is possible to define the marginal distributions of $X$ and $Y$. In the continuous case, these functions describe the probability behavior of each variable individually, regardless of the other. In other words, they represent the total probability obtained by integrating out the other variable. The marginal density functions are given by:

$$f_{X} \left(\right. x \left.\right) & = \int_{- \infty}^{+ \infty} f_{X , Y} \left(\right. x , y \left.\right) d y \\ f_{Y} \left(\right. y \left.\right) & = \int_{- \infty}^{+ \infty} f_{X , Y} \left(\right. x , y \left.\right) d x$$

where $f_{X} \left(\right. x \left.\right)$ is the marginal density of $X$, and $f_{Y} \left(\right. y \left.\right)$ is the marginal density of $Y$.

## Example 1

Consider a continuous random variable $X$ that represents the lifetime in years of a light bulb. Suppose its probability density function is given by:

$$f \left(\right. x \left.\right) = \left{\right. \lambda e^{- \lambda x} & x \geq 0 \\ 0 & x < 0$$

where $\lambda > 0$ is a constant that determines how quickly the probability decreases. This is known as the exponential distribution, commonly used to model waiting times or lifetimes of components.

##### The constant $e \approx 2.71828$ naturally appears in this context through the [exponential function](https://algebrica.org/exponential-function). Its origin can be traced back to the idea of a [limit of a sequence](https://algebrica.org/euler-number-limit-sequence/), where it first emerges as a fundamental mathematical constant.

---

The probability that the light bulb lasts between $a = 1$ and $b = 3$ years is obtained by integrating the density function:

$$P \left(\right. 1 < X < 3 \left.\right) = \int_{1}^{3} \lambda e^{- \lambda x} d x = e^{- \lambda} - e^{- 3 \lambda}$$

Graphically, this probability corresponds to the area under the curve of $f \left(\right. x \left.\right)$ between $x = 1$ and $x = 3$.

If, for instance, $\lambda = 0.5$ then:

$$P \left(\right. 1 < X < 3 \left.\right) = e^{- 0.5} - e^{- 1.5} \approx 0.383$$

meaning there is about a 38% chance that the bulb will last between one and three years.

## Mean of a continuous random variable

Also for continuous random variables, it is possible to define the concept of the mean or [expected value](https://algebrica.org/mean-or-expected-value-of-a-random-variable/). It represents the long-run average value that the variable would take if the experiment were repeated infinitely many times. For a continuous random variable $X$ with a probability density function $f \left(\right. x \left.\right)$, the mean is given by:

$$\mu = E \left(\right. X \left.\right) = \int_{- \infty}^{+ \infty} x f \left(\right. x \left.\right) d x$$
