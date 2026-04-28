---
layout: chapter
title: "Propositional Logic"
chapter: "Other Topics"
chapter_order: 22
section_order: 2
permalink: /materi-algebrica/other-topics/propositional-logic/
---

CNF and DNFnormal formsequivalenceshypothetical syllogismmodus tollensmodus ponenslogical consequenceinconsistencytautologysatisfiabilitymodelsinterpretationstruth tablestruth valuespropositional languageformation ruleswell-formed formulasconnectivesatomic propositionsinferencesemanticssyntax

## Introduction

Propositional logic studies the inferential relationships among sentences, focusing on a class of logical operators known as propositional connectives. Inferential relationships are the logical connections that allow the truth of one proposition to be derived from the truth of others: they establish, according to the rules of logic, how the truth of a given proposition can follow necessarily from the truth of further propositions.

These relationships are fundamental in deductive reasoning and in the analysis of logical arguments. Propositional logic determines how the truth values of propositions relate to one another through logical operators, enabling automated reasoning and logical deduction in fields such as computer science, artificial intelligence, and formal verification.

## Propositional language

A propositional language $\text{Prop} \left[\right. P \left]\right.$ consists of a set of atomic propositions, logical connectives, and formation rules that define the syntax of the language.

- Atomic propositions are indivisible units of the language, represented by symbols such as $p , q , r$. A propositional language over a set $P$ is denoted as follows:
  $$\text{Prop} \left[\right. P \left]\right. , P = \left{\right. p , q , r \left.\right}$$
- Logical connectives include: $\neg$, $\land$, $\lor$, $\rightarrow$, $\leftrightarrow$, $\oplus$.
- Propositions built from atomic formulas using logical connectives, according to the formation rules, are called well-formed formulas (WFF).

These three elements constitute the syntax of a propositional language.

## Logical connectives

Propositional connectives are logical operators used in propositional logic to combine or modify atomic propositions, determining the truth conditions of the resulting compound proposition. An atomic proposition is a statement that cannot be broken down into simpler parts, such as “it is raining”. The main propositional connectives are the following.

- $\neg$, negation: inverts the truth value of a proposition. If $p$ is true, then $\neg p$ is false, and conversely.
- $\land$, conjunction: represents the logical AND. A conjunction $p \land q$ is true only if both $p$ and $q$ are true.
- $\lor$, disjunction: represents the logical OR. A disjunction $p \lor q$ is true if at least one of $p$ or $q$ is true.
- $\rightarrow$, implication: represents “if…then”. An implication $p \rightarrow q$ is false only when $p$ is true and $q$ is false, that is, when a true premise leads to a false conclusion.
- $\leftrightarrow$, biconditional: represents “if and only if”. A biconditional $p \leftrightarrow q$ is true precisely when $p$ and $q$ share the same truth value, that is, both are true or both are false.
- $\oplus$, exclusive disjunction (XOR): is true if and only if exactly one of $p$ or $q$ is true.

## Example

Consider a propositional language $\text{Prop} \left[\right. P \left]\right.$ defined over the following set of atomic propositions:

$$P = \left{\right. p , q \left.\right}$$

- $p =$ the door is open.
- $q =$ the window is open.

The following statements can be represented using the atomic propositions $p$ and $q$ together with the logical connectives introduced above.

- The door is closed, that is, the door is not open: $\neg p$
- The door and the window are both open: $p \land q$
- If the door is open, then the window is open: $p \rightarrow q$
- The door is open if and only if the window is open: $p \leftrightarrow q$
- Either the door is open or the window is open, but not both: $p \oplus q$
- It is not the case that if the door is open then the window is open: $\neg \left(\right. p \rightarrow q \left.\right)$

## Formation rules

Formation rules define how atomic propositions and logical connectives can be combined to produce well-formed formulas (WFFs). The rules are the following.

- If $p$ is an atomic proposition, then $p$ is a WFF.
- If $p$ is a WFF, then $\neg p$ is a WFF.
- If $p$ and $q$ are WFFs, then each of $p \land q$, $p \lor q$, $p \rightarrow q$, $p \leftrightarrow q$, and $p \oplus q$ is a WFF.

Any formula that cannot be obtained by a finite application of these rules is not considered a well-formed formula of the language.

## Semantics

The meaning of the syntactically correct expressions of $\text{Prop} \left[\right. P \left]\right.$ is provided by semantics. Defining the interpretation domain of the propositional language is essential to establishing its semantics. This domain comprises the set of objects that denote the possible meanings of the language’s expressions. In propositional logic, the interpretation domain consists of the two Boolean values true and false:

$$\text{Bool} = \left{\right. T , F \left.\right}$$

Given two formulas $p$ and $q$, the truth table illustrating their relationships under the propositional connectives is the following:

$$p & q & \neg p & p \land q & p \lor q & p \rightarrow q & p \leftrightarrow q & p \oplus q \\ T & T & F & T & T & T & T & F \\ T & F & F & F & T & F & F & T \\ F & T & T & F & T & T & F & T \\ F & F & T & F & F & T & T & F$$

The table covers all possible combinations of truth values for $p$ and $q$, making the effect of each connective explicit. Two notable equivalences that follow directly from the table are worth recording.

- An implication can be rewritten in disjunctive form as $p \rightarrow q \equiv \neg p \lor q$.
- A biconditional can be rewritten in disjunctive form as $p \leftrightarrow q \equiv \left(\right. \neg p \lor q \left.\right) \land \left(\right. \neg q \lor p \left.\right)$.

In both cases, the symbol $\equiv$ denotes logical equivalence.

## Interpretations

An interpretation $M$ is a function that assigns a Boolean value to each atomic proposition in $P$:

$$M : P \rightarrow \left{\right. T , F \left.\right}$$

Given a formula $\varphi$ built from the propositions in $P$, the truth value of $\varphi$ under $M$ is determined by the values assigned to its atomic components together with the semantics of the connectives.

- If $\varphi$ is true under $M$, we write $M \vDash \varphi$ and say that $M$ is a model of $\varphi$.
- If $\varphi$ is false under $M$, we write $M \nvDash \varphi$ and say that $M$ is a counter-model of $\varphi$.

Consider the following atomic propositions:

- $p =$ the door is open.
- $q =$ the window is open.

Let $M$ be the interpretation in which $p$ is true and $q$ is false. We want to verify whether $M$ satisfies the formula $p \rightarrow \neg q$. The relevant portion of the truth table is the following:

$$p & q & \neg q & p \rightarrow \neg q \\ T & F & T & T$$

Under this interpretation, $p$ is true, $q$ is false, and consequently $\neg q$ is true. Since both the premise and the conclusion of the implication are true, the formula $p \rightarrow \neg q$ evaluates to true, and we conclude that $M \vDash p \rightarrow \neg q$.

Three fundamental classifications of formulas arise from the notion of interpretation.

A formula $\varphi$ is inconsistent if no interpretation satisfies it, that is, if $\varphi$ is false under every possible interpretation:

$$\forall M , M \nvDash \varphi$$

A formula $\varphi$ is satisfiable if at least one interpretation satisfies it, that is, if $\varphi$ is true under some interpretation:

$$\exists M , M \vDash \varphi$$

A formula $\varphi$ is a tautology if it is true under every possible interpretation:

$$\forall M , M \vDash \varphi$$

## Logical consequence

A formula $p$ is a logical consequence of a set of formulas $S$ if and only if every interpretation $M$ that satisfies all formulas in $S$ also satisfies $p$:

$$S \vDash p$$

In other words, $p$ is a logical consequence of $S$ whenever $p$ must be true in every interpretation that makes all formulas in $S$ true simultaneously. Consider the following example. Let:

- $S = \left{\right. A , A \rightarrow B \left.\right}$
- $p = B$

We want to verify whether $B$ is a logical consequence of $S$. The truth table for the formulas in $S$ is the following:

$$A & B & A \rightarrow B \\ T & T & T \\ T & F & F \\ F & T & T \\ F & F & T$$

The only row in which both $A$ and $A \rightarrow B$ are true is the first, and in that row $B$ is also true. Therefore we conclude that $S \vDash B$, and $B$ is indeed a logical consequence of $S$.

This form of reasoning, known as modus ponens, is one of the most fundamental inference rules in propositional logic. The concept of logical consequence plays a central role not only in formal logic but also in artificial intelligence: it underpins the validity of arguments, the correctness of automated reasoning, and the reliability of conclusions drawn by AI systems from formalized knowledge.

## Inference rules

The notion of logical consequence, introduced in the previous section, establishes when a formula must be true given a set of premises. Inference rules are schematic patterns that license the derivation of a conclusion from one or more premises, provided those premises are true. Each rule is valid in the sense that its conclusion is a logical consequence of its premises. The three most fundamental inference rules of propositional logic are presented below.

Modus ponens states that if $p$ is true and the implication $p \rightarrow q$ is true, then $q$ must be true. In schematic form:

$$\frac{p p \rightarrow q}{q}$$

---

Modus tollens states that if $q$ is false and the implication $p \rightarrow q$ is true, then $p$ must be false. In schematic form:

$$\frac{\neg q p \rightarrow q}{\neg p}$$

---

The hypothetical syllogism states that if $p \rightarrow q$ and $q \rightarrow r$ are both true, then $p \rightarrow r$ is also true. In schematic form:

$$\frac{p \rightarrow q q \rightarrow r}{p \rightarrow r}$$

In each schema, the formulas above the horizontal line are the premises and the formula below is the conclusion.

> These three rules are not independent of one another. Modus tollens, for instance, can be derived from modus ponens together with the equivalence $\left(\right. p \rightarrow q \left.\right) \equiv \left(\right. \neg q \rightarrow \neg p \left.\right)$, known as contraposition. The hypothetical syllogism, similarly, follows from two successive applications of modus ponens.

As an illustration, consider the following premises:

- $p =$ it is raining.
- $q =$ the ground is wet.
- $r =$ the match is cancelled.

Suppose we know that $p \rightarrow q$ and $q \rightarrow r$. By the hypothetical syllogism, we may conclude that $p \rightarrow r$. If it is raining, then the match is cancelled. If we further know that $p$ is true, a single application of modus ponens yields $r$: the match is cancelled.

## Normal forms

Every propositional formula can be rewritten in a logically equivalent form that follows a regular syntactic structure. The two most important such structures are conjunctive normal form and disjunctive normal form.

- A literal is either an atomic proposition or its negation. Given an atomic proposition $p$, both $p$ and $\neg p$ are literals.
- A formula is in conjunctive normal form (CNF) if it is a conjunction of clauses, where each clause is a disjunction of literals:

$$\left(\right. l_{1 , 1} \lor \hdots \lor l_{1 , k} \left.\right) \land \left(\right. l_{2 , 1} \lor \hdots \lor l_{2 , m} \left.\right) \land \hdots$$

A formula is in disjunctive normal form (DNF) if it is a disjunction of terms, where each term is a conjunction of literals:

$$\left(\right. l_{1 , 1} \land \hdots \land l_{1 , k} \left.\right) \lor \left(\right. l_{2 , 1} \land \hdots \land l_{2 , m} \left.\right) \lor \hdots$$

It can be shown that every propositional formula is logically equivalent to some formula in CNF and to some formula in DNF. The conversion can always be carried out by applying the following standard equivalences: double negation elimination, De Morgan’s laws, and the distributivity of $\land$ over $\lor$ and of $\lor$ over $\land$.

> The most widely used equivalences in normal form conversion are the following: $\neg \neg p \equiv p$, $\neg \left(\right. p \land q \left.\right) \equiv \neg p \lor \neg q$, $\neg \left(\right. p \lor q \left.\right) \equiv \neg p \land \neg q$, and the distributive laws $p \land \left(\right. q \lor r \left.\right) \equiv \left(\right. p \land q \left.\right) \lor \left(\right. p \land r \left.\right)$ and $p \lor \left(\right. q \land r \left.\right) \equiv \left(\right. p \lor q \left.\right) \land \left(\right. p \lor r \left.\right) .$

---

As an example, consider the formula $\neg \left(\right. p \lor q \left.\right) \rightarrow r$. Using the equivalence $\varphi \rightarrow \psi \equiv \neg \varphi \lor \psi$, the formula can be rewritten as follows:

$$\neg \left(\right. p \lor q \left.\right) \rightarrow r \equiv \neg \neg \left(\right. p \lor q \left.\right) \lor r \equiv \left(\right. p \lor q \left.\right) \lor r$$

The resulting formula $\left(\right. p \lor q \left.\right) \lor r$ is a single clause and is therefore already in conjunctive normal form. The original formula is thus equivalent to the CNF formula $p \lor q \lor r$.

Normal forms play a central role in automated reasoning. Most satisfiability algorithms, including the widely used DPLL procedure, require the input formula to be expressed in CNF.
