---
layout: chapter
title: "Discrete Random Variables"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 8
permalink: /materi-algebrica/probability-and-statistics/discrete-random-variables/
---

## Definition of a discrete random variable

A **discrete random variable** is a function that assigns a real number to each element of a discrete sample space. In other words, it maps the possible outcomes of a random experiment to numerical values that can be analyzed statistically. Formally, a discrete random variable is a function:

$$X : \Omega \rightarrow \mathbb{R}$$

where $\Omega$ is a discrete sample space.

##### When the sample space is continuous, composed of infinitely many infinitesimally close outcomes, we speak of [continuous random variables](https://algebrica.org/continuous-random-variables/).

---

To illustrate the concept in a simple way, consider an experiment where a single die is rolled twice, and let the random variable $X$ represent the number of sixes obtained. The possible values of $X$ are 0, 1, and 2 where $0$ means that no six appears in the two rolls, $1$ means that exactly one six appears, and $2$ means that both rolls show a six.

| $x$ | 0 | 1 | 2 |
| --- | --- | --- | --- |
| $$f \left(\right. x \left.\right)$$ | $$\frac{25}{36}$$ | $$\frac{10}{36}$$ | $$\frac{1}{36}$$ |

where $x$ represents the possible outcomes of the random variable $X$ and $f \left(\right. x \left.\right)$ represents the probability associated with each outcome. The probabilities satisfy:

$$\sum f \left(\right. x \left.\right) = 1$$

This is consistent with the law of total probability, which states that the sum of the probabilities of all mutually exclusive outcomes of a random variable must equal $1$. It ensures that the probability distribution accounts for every possible event in the experiment.

---

Since probability calculations can be tricky at first, the following shows how the values of $f \left(\right. x \left.\right)$ for 0, 1, and 2 are obtained.

$$P \left(\right. X = 0 \left.\right) & = \left(\left(\right. \frac{5}{6} \left.\right)\right)^{2} = \frac{25}{36} \\ P \left(\right. X = 1 \left.\right) & = 2 \cdot \frac{1}{6} \cdot \frac{5}{6} = \frac{10}{36} \\ P \left(\right. X = 2 \left.\right) & = \left(\left(\right. \frac{1}{6} \left.\right)\right)^{2} = \frac{1}{36}$$

- In the case of $x = 0$, both dice show numbers other than six. Since the probability of not getting a six on a single roll is $\frac{5}{6}$, the probability that this happens twice in a row is $\left(\left(\right. \frac{5}{6} \left.\right)\right)^{2}$.
- In the case of $x = 1$, exactly one six appears in the two rolls. There are two possible ways this can happen: the first die shows a six and the second does not,
   or the first does not show a six and the second does. Each event has a probability of $\frac{1}{6} \cdot \frac{5}{6}$, so the total probability is $2 \cdot \frac{1}{6} \cdot \frac{5}{6}$.
- Finally, in the case of $x = 2$, both dice show a six. Since the probability of rolling a six on a single die is $\frac{1}{6}$, the probability that this occurs twice in a row is $\left(\left(\right. \frac{1}{6} \left.\right)\right)^{2}$.

## Discrete probability distribution

A discrete random variable has a certain probability of taking each of its possible values.
 This probability is described by a function $f \left(\right. x \left.\right)$, called the probability mass function or **discrete probability distribution**. For such a distribution, the following conditions must hold:

$$& f \left(\right. x \left.\right) \geq 0 \\ & \underset{x}{\sum} f \left(\right. x \left.\right) = 1 \\ & P \left(\right. X = x \left.\right) = f \left(\right. x \left.\right)$$

These conditions ensure that all probabilities are non-negative, that their total equals one,
 and that the probability of a specific value $x$ is exactly given by its corresponding $f \left(\right. x \left.\right)$.

---

When dealing with a discrete random variable $X$, it is often useful to describe the probability that $X$ takes a value up to a certain threshold (x). This leads to the definition of the **cumulative distribution function**, denoted by $F \left(\right. x \left.\right)$:

$$F \left(\right. x \left.\right) = P \left(\right. X \leq x \left.\right) = \underset{t \leq x}{\sum} f \left(\right. t \left.\right)$$

The function $F \left(\right. x \left.\right)$ expresses the total probability accumulated up to $x$. It is defined for all real values of $x$ and increases step by step as new probability mass is added. Being cumulative by nature, $F \left(\right. x \left.\right)$ is always non-decreasing and never exceeds $1$. To better illustrate the concept, let us return to the example of rolling two dice and show how the cumulative distribution function is constructed. The random variable $X$ represents the number of sixes obtained. Its probability mass function is:

| $x$ | 0 | 1 | 2 |
| --- | --- | --- | --- |
| $$f \left(\right. x \left.\right)$$ | $$\frac{25}{36}$$ | $$\frac{10}{36}$$ | $$\frac{1}{36}$$ |

The cumulative distribution function (F(x)) is obtained by adding the probabilities
 up to each value of $x$:

| $x$ | 0 | 1 | 2 |
| --- | --- | --- | --- |
| $$F \left(\right. x \left.\right)$$ | $$\frac{25}{36}$$ | $$\frac{35}{36}$$ | $$1$$ |

In fact, we have:

$$F \left(\right. 0 \left.\right) & = P \left(\right. X \leq 0 \left.\right) = f \left(\right. 0 \left.\right) = \frac{25}{36} \\ F \left(\right. 1 \left.\right) & = P \left(\right. X \leq 1 \left.\right) = f \left(\right. 0 \left.\right) + f \left(\right. 1 \left.\right) = \frac{25}{36} + \frac{10}{36} = \frac{35}{36} \\ F \left(\right. 2 \left.\right) & = P \left(\right. X \leq 2 \left.\right) = f \left(\right. 0 \left.\right) + f \left(\right. 1 \left.\right) + f \left(\right. 2 \left.\right) = 1$$

The function $F \left(\right. x \left.\right)$ shows how probability accumulates as $x$ increases. It starts at $\frac{25}{36}$ when no sixes are obtained and reaches 1 when all possible outcomes have been included.

## Joint probability distributions

In cases where the sample space is multidimensional, meaning that each outcome depends on two or more random variables, the corresponding probabilities are described by **joint probability distributions** for discrete random variables. In some experiments, two discrete random variables can occur together, each taking specific values within the same outcome. The probability of this combined occurrence is described by a function $f \left(\right. x , y \left.\right)$, which assigns a probability to every possible pair $\left(\right. x , y \left.\right)$. We have:

$$f \left(\right. x , y \left.\right) = P \left(\right. X = x ; Y = y \left.\right)$$

This function expresses how likely it is that $X$ takes the value $x$ while, at the same time, $Y$ takes the value $y$. For joint probability distributions, the following conditions must hold:

$$& f \left(\right. x , y \left.\right) \geq 0 \forall \left(\right. x , y \left.\right) \\ & \underset{x}{\sum} \underset{y}{\sum} f \left(\right. x , y \left.\right) = 1 \\ & P \left(\right. X = x ; Y = y \left.\right) = f \left(\right. x , y \left.\right)$$

These conditions state that all probabilities are non-negative, that their total sum over all possible pairs $\left(\right. x , y \left.\right)$ equals one, and that each joint probability $P \left(\right. X = x , Y = y \left.\right)$ is represented by the value of $f \left(\right. x , y \left.\right)$.

## Example 1

To better illustrate the concept of a joint probability distribution for discrete random variables, consider the following simple example.Consider a small box containing 4 balls, 2 white and 2 black. Two balls are drawn at random without replacement. Let:

- $X$ = the number of black balls drawn
- $Y$ = the number of white balls drawn

The possible pairs $\left(\right. x , y \left.\right)$ represent all combinations of black and white balls that can be drawn. Since only two balls are extracted, $x + y = 2$, and the possible pairs are:

$$\left(\right. 0 , 2 \left.\right) , \left(\right. 1 , 1 \left.\right) , \left(\right. 2 , 0 \left.\right)$$

The joint probability distribution $f \left(\right. x , y \left.\right)$ is given by:

$$f \left(\right. x , y \left.\right) = \frac{\left(\right. \frac{2}{x} \left.\right) \left(\right. \frac{2}{y} \left.\right)}{\left(\right. \frac{4}{2} \left.\right)}$$

By representing the values assumed by each pair $\left(\right. x , y \left.\right)$, we obtain the following table showing the joint probability distribution $f \left(\right. x , y \left.\right)$:

$$f \left(\right. x , y \left.\right) & 0 & 1 & 2 & \text{Totals} \\ 0 & \frac{0}{6} & \frac{0}{6} & \frac{1}{6} & \frac{1}{6} \\ 1 & \frac{0}{6} & \frac{4}{6} & \frac{0}{6} & \frac{4}{6} \\ 2 & \frac{1}{6} & \frac{0}{6} & \frac{0}{6} & \frac{1}{6} \\ \text{Totals} & \frac{1}{6} & \frac{4}{6} & \frac{1}{6} & 1$$

This example helps visualize how probabilities can be distributed across two discrete random variables. Each cell in the table represents the likelihood of a specific combination of black and white balls being drawn. By summing across rows and columns, we obtain the marginal probabilities of $X$ and $Y$, confirming that the total probability of all possible outcomes equals one.

##### It’s a simple yet effective way to understand how joint distributions organize and relate probabilities in a two-variable system.
