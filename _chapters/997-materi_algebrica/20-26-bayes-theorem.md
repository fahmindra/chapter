---
layout: chapter
title: "Bayes’ Theorem"
chapter: "Probability and Statistics"
chapter_order: 20
section_order: 26
permalink: /materi-algebrica/probability-and-statistics/bayes-theorem/
---

## What it is and what Bayes’ Theorem is used for

Bayes’ Theorem is a fundamental result in probability theory that describes how to compute the conditional probability of a hypothesis given observed evidence. It provides a formal mechanism for updating prior beliefs in light of new data, by relating the posterior probability to the prior probability and the likelihood of the observed evidence.

---

In formal terms, given two events $A$ and $B$, Bayes’ Theorem states that the posterior probability of event $A$ given event $B$ is equal to the likelihood of event $B$ given event $A$ multiplied by the prior probability of event $A$, all divided by the marginal probability (or evidence) of event $B$.

$$P \left(\right. A \left|\right. B \left.\right) = \frac{P \left(\right. B \left|\right. A \left.\right) P \left(\right. A \left.\right)}{P \left(\right. B \left.\right)}$$

- $P \left(\right. A \left|\right. B \left.\right)$, posterior probability: the probability of event $A$ occurring given that event $B$ has already occurred. It represents our updated belief about $A$ after observing $B$.
- $P \left(\right. B \left|\right. A \left.\right)$, likelihood: the probability of observing event $B$ if event $A$ were true. It measures how compatible the observed data ($B$) is with the hypothesis ($A$).
- $P \left(\right. A \left.\right)$, prior probability, the initial probability of event $A$ occurring before observing any evidence ($B$). It represents our initial belief about $A$.
- $P \left(\right. B \left.\right)$, marginal probability, or evidence: the overall probability of event $B$ occurring. It can be calculated as the sum (or integral in the continuous case) of the probabilities of $B$ conditioned on all possible states of $A$, weighted by their prior probabilities.

Formally, the marginal probability of an event $B$ is calculated using the law of total probability, which expresses $P \left(\right. B \left.\right)$ as the sum of the probabilities of $B$ conditioned on all possible events of another complete and exclusive set of events (such as $A$ and its complement $\neg A$, weighted by the probabilities of these events:

$$P \left(\right. B \left.\right) = P \left(\right. B \left|\right. A \left.\right) P \left(\right. A \left.\right) + P \left(\right. B \left|\right. \neg A \left.\right) P \left(\right. \neg A \left.\right)$$

##### This formula is crucial because it has significant practical implications for calculating the marginal probability of an event (B) when solving problems that utilize Bayes’ Theorem.

## How to derive Bayes’ Theorem

To derive the Bayes’ Theorem, we consider the joint probability of the two events $A$ and $B$, which can be expressed as:

$$\left(\right. A \cap B \left.\right) = P \left(\right. A \left|\right. B \left.\right) P \left(\right. B \left.\right)$$

Since the intersection of two sets is commutative, the order does not change the result, we also have that the joint probability of $B$ and $A$ can be expressed as:

$$\left(\right. B \cap A \left.\right) = P \left(\right. B \left|\right. A \left.\right) P \left(\right. A \left.\right)$$

From this, it follows that:

$$\left(\right. A \cap B \left.\right) = P \left(\right. A \left|\right. B \left.\right) P \left(\right. B \left.\right) = P \left(\right. B \left|\right. A \left.\right) P \left(\right. A \left.\right) = \left(\right. B \cap A \left.\right)$$

Therefore, we obtain:

$$\left(\right. P \left(\right. A \left|\right. B \left.\right) = \frac{P \left(\right. B \left|\right. A \left.\right) P \left(\right. A \left.\right)}{P \left(\right. B \left.\right)}$$

## Example

An email filtering system tries to classify emails into two categories: spam and not spam. The filter uses the presence of certain keywords to make this decision. Let’s consider the word “discount”.

First, let’s define the events that occur in this problem:

- $S$: the email is spam.
- $\neg S$: the email is not spam.
- $D$: the email contains the word “discount”.

Now, let’s consider the following probabilities, assuming that the word “discount” is present in 95% of spam emails, while it is present in only 2% of non-spam emails.

- Prior probability of spam: $P \left(\right. S \left.\right) = 0.40$.
- Prior probability of not spam: $P \left(\right. \neg S \left.\right) = 0.60$.
- Likelihood of “discount” given spam: $P \left(\right. D \left|\right. S \left.\right) = 0.95$.
- Likelihood of “discount” given not spam: $P \left(\right. D \left|\right. \neg S \left.\right) = 0.02$.

We want to find the probability that the email is spam given that it contains the word “discount”, which is $P \left(\right. S \left|\right. D \left.\right)$.

---

Let’s apply Bayes’ Theorem to our problem, and we get

$$P \left(\right. S \left|\right. D \left.\right) = \frac{P \left(\right. D \left|\right. S \left.\right) P \left(\right. S \left.\right)}{P \left(\right. D \left.\right)}$$

We are missing the marginal probability of finding the word “discount” in any email, $P \left(\right. D \left.\right)$. We can calculate it using the law of total probability:

$$P \left(\right. D \left.\right) = P \left(\right. D \left|\right. S \left.\right) P \left(\right. S \left.\right) + P \left(\right. D \left|\right. \neg S \left.\right) P \left(\right. \neg S \left.\right)$$

Calculating $P \left(\right. D \left.\right)$ gives us:

$$P \left(\right. D \left.\right) & = \left(\right. 0.95 \times 0.40 \left.\right) + \left(\right. 0.02 \times 0.60 \left.\right) \\ P \left(\right. D \left.\right) & = 0.38 + 0.012 \\ P \left(\right. D \left.\right) & = 0.392$$

Substituting the value $P \left(\right. B \left.\right)$ into Bayes’ Theorem formula, we get:

$$P \left(\right. S \left|\right. D \left.\right) & = \frac{0.95 \times 0.40}{0.392} \\ P \left(\right. S \left|\right. D \left.\right) & = \frac{0.38}{0.392} \\ P \left(\right. S \left|\right. D \left.\right) & \approx 0.969$$

Therefore, it is concluded that given that the email contains the word “discount”, the probability that it is spam is approximately 96.94%.

## Glossary

- Bayes’ Theorem: a fundamental result in probability theory that describes how to compute the conditional probability of a hypothesis given observed evidence, providing a framework for updating prior beliefs.
- Posterior probability $P \left(\right. A \left|\right. B \left.\right)$: the updated probability of an event $A$ occurring after observing new evidence $B$.
- Prior probability $P \left(\right. A \left.\right)$: the initial probability of an event $A$ occurring before any evidence is observed.
- Likelihood $P \left(\right. B \left|\right. A \left.\right)$: the probability of observing the evidence $B$ if the hypothesis $A$ were true.
- Marginal probability $P \left(\right. B \left.\right)$: the overall probability of the evidence $B$ occurring, regardless of the truth of the hypothesis $A$. Also referred to as the evidence.
- Conditional probability: the probability of an event occurring given that another event has already occurred.
- Joint probability $P \left(\right. A \cap B \left.\right)$: the probability that two events $A$ and $B$ both occur.
