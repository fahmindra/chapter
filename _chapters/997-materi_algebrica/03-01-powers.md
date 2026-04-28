---
layout: chapter
title: "Powers"
chapter: "Powers, Radicals and Logarithms"
chapter_order: 3
section_order: 1
permalink: /materi-algebrica/powers-radicals-and-logarithms/powers/
---

## Introduction to powers

Powers are mathematical operations that show how many times a [number](https://algebrica.org/types-of-numbers/) is to be multiplied by itself. The standard way of writing a power is $a^{n}$ where $a$ is the base and $n$ is the exponent:
$$(\text{1}) a^{n} = \underset{n \text{times}}{\underbrace{a \cdot a \cdot a \hdots a}} \text{with} a \in \mathbb{R} , n \in \mathbb{Z}^{+}$$

> From a geometric perspective, when considering a positive number $a$, it can be observed that the expressions $a^{2}$ and $a^{3}$ respectively denote the area of a square with its side length being $a$ and the volume of a cube with its edge length being $a$.

---

The value of the exponent $n$ can be positive, negative, or zero. When the exponent is negative, it indicates a reciprocal relationship between powers, expressed as follows:
$$a^{- n} = \frac{1}{a^{n}}$$
This means that raising a number to a negative exponent is equivalent to taking the reciprocal of the same number raised to the corresponding positive exponent. If the exponent is fractional, for instance $n = \frac{1}{m}$, the power can be rewritten in [radical](https://algebrica.org/radicals/) form as follows:
$$a^{\frac{1}{m}} = \sqrt[m]{a}$$
This expression represents the $m$-th root of $a$. By combining both concepts, a negative fractional exponent can be interpreted as the reciprocal of a root:
$$a^{- \frac{1}{m}} = \frac{1}{\sqrt[m]{a}}$$
This unified notation allows exponents to represent both powers and roots, simplifying many algebraic expressions and making exponent rules consistent across different cases.

---

The table below illustrates selected values of $a^{n}$. Each row corresponds to a fixed base $a$ and each column to a fixed exponent $n$.

|  | $a^{- 2}$ | $a^{- 1}$ | $a^{0}$ | $a^{1}$ | $a^{2}$ | … |
| --- | --- | --- | --- | --- | --- | --- |
| $- 2$ | $\frac{1}{4}$ | $- \frac{1}{2}$ | $1$ | $- 2$ | $4$ | … |
| $- 1$ | $1$ | $- 1$ | $1$ | $- 1$ | $1$ | … |
| $0$ | — | — | — | $0$ | $0$ | … |
| $1$ | $1$ | $1$ | $1$ | $1$ | $1$ | … |
| $2$ | $\frac{1}{4}$ | $\frac{1}{2}$ | $1$ | $2$ | $4$ | … |
| … | … | … | … | … | … | … |

> The symbol — indicates that the expression is undefined: negative exponents of zero involve division by zero, and $0^{0}$ is an [indeterminate form](https://algebrica.org/indeterminate-forms/).

If the base $a$ is negative, the sign of $a^{n}$ alternates according to the parity of $n$. For instance, $\left(\right. - 1 \left.\right)^{n} = 1$ when $n$ is even, and $\left(\right. - 1 \left.\right)^{n} = - 1$ when $n$ is odd. This alternating behaviour is particularly significant in the analysis of sequences and limits. Additionally, negative bases with fractional exponents must be treated carefully, since expressions such as $\left(\right. - 1 \left.\right)^{1 / 2}$ are not defined in $\mathbb{R}$.

## Powers with real exponents

The definition $a^{n}$ in $1$ is valid only for positive [integers](https://algebrica.org/integers/) $n$, but the idea of repeated multiplication does not work when the exponent is not an integer. Extending this concept to [real](https://algebrica.org/properties-of-real-numbers/) exponents necessitates a different approach, one based on the [exponential function](https://algebrica.org/exponential-function/) and the [natural logarithm](https://algebrica.org/logarithms/). For any positive base $a > 0$ and real exponent $x \in \mathbb{R}$, the power $a^{x}$ is defined as follows.
$$a^{x} = e^{x ln ⁡ a}$$
When $x$ is a positive integer, it yields repeated multiplication. For rational $x$, it aligns with the radical interpretation. To verify this, let $x = \frac{p}{q}$ with $p , q \in \mathbb{Z}$ and $q \neq 0$. Applying the definition yields the following:

$$e^{\frac{p}{q} ln ⁡ a} = \left(\left(\right. e^{ln ⁡ a} \left.\right)\right)^{\frac{p}{q}} = a^{\frac{p}{q}}$$

This confirms that the exponential definition reduces to the usual radical interpretation when the exponent is rational, and the two notations are fully consistent.The necessity of this extension can be illustrated by considering $2^{\sqrt{2}}$. Because $\sqrt{2}$ is irrational and cannot be written as a fraction $\frac{m}{n}$, the radical definition is inapplicable. Applying the real exponent definition yields the following:
$$2^{\sqrt{2}} = e^{\sqrt{2} ln ⁡ 2} \approx e^{0.9803} \approx 2.665$$
This value is well-defined and can be approximated to any specified degree of precision. This definition also explains why the base must satisfy $a > 0$. If $a \leq 0$, the expression $ln ⁡ a$ is undefined in $\mathbb{R}$, and the extension fails. This is consistent with the earlier observation that negative bases with fractional exponents do not yield real numbers. As a result, the function $f \left(\right. x \left.\right) = a^{x}$ is [continuous](https://algebrica.org/continuous-functions/) and [differentiable](https://algebrica.org/derivatives/) for all real numbers when $a > 0$.

## Fundamental rules of powers

The following rules govern the manipulation of expressions involving powers. They hold for real bases and exponents under the conditions specified in each case.

Raising any base not equal to zero to an exponent of zero always results in $1$. The value of $a$ is restricted because the operation $0^{0}$ is meaningless and considered an indeterminate form.
$$a^{0} = 1 \text{if} a \neq 0$$

---

Any power of zero always results in zero because it corresponds to the product of $n$ zeros, where $n$ is the exponent:
$$0^{n} = 0 \text{for} n > 0$$
The condition $n > 0$ is necessary because $0^{0}$ is an [indeterminate form](https://algebrica.org/indeterminate-forms/). Depending on the context, it can be approached as a [limit](https://algebrica.org/limits) in two ways:
$$\underset{x \rightarrow 0^{+}}{lim} 0^{x} = 0$$
$$\underset{x \rightarrow 0}{lim} x^{0} = 1$$
The form $0^{0}$ is therefore left undefined in the context of limits. More generally, the following expressions are indeterminate forms, meaning their value cannot be determined without further analysis of the specific limit: $0^{0}$, $1^{\infty}$, and $\infty^{0}$.

> In combinatorics and algebra, however, it is conventionally assigned the value $1$, since it arises naturally in expressions such as the [binomial theorem](https://algebrica.org/binomial-theorem/).

---

The product of two or more powers with the same base $a$ is a power with the same base and exponent equal to the sum of the exponents:
$$a^{n} \cdot a^{m} = a^{n + m}$$
To see why this holds, observe that $a^{n}$ represents the product of $n$ factors equal to $a$, and $a^{m}$ represents the product of $m$ such factors. Concatenating these two products gives a total of $n + m$ factors, which is precisely $a^{n + m}$. In formal terms, the argument reads as follows:
$$a^{n} \cdot a^{m} = \underset{n \text{times}}{\underbrace{a \cdot a \hdots a}} \cdot \underset{m \text{times}}{\underbrace{a \cdot a \hdots a}} = \underset{n + m \text{times}}{\underbrace{a \cdot a \hdots a}} = a^{n + m}$$
This reasoning applies directly to positive integer exponents, as it relies on counting factors. For integer, rational, or real exponents, the same result follows from the definition $a^{x} = e^{x ln ⁡ a}$. Since the exponential function satisfies $e^{u} \cdot e^{v} = e^{u + v}$, we have the following:
$$a^{n} \cdot a^{m} = e^{n ln ⁡ a} \cdot e^{m ln ⁡ a} = e^{\left(\right. n + m \left.\right) ln ⁡ a} = a^{n + m}$$

---

The product of powers with different bases $a$ and $b$ but the same exponent $n$ is a power whose base is the product of the original bases.
$$a^{n} \cdot b^{n} = \left(\right. a b \left.\right)^{n}$$

> Consider the expression $2^{3} \cdot 5^{3}$. Since both factors share the same exponent, they can be combined into a single power of the product of the bases, giving $2^{3} \cdot 5^{3} = \left(\right. 2 \cdot 5 \left.\right)^{3} = 10^{3}$.

---

The quotient of two powers with the same base $a$ is a power with the same base and exponent equal to the difference between the exponents.
$$\frac{a^{n}}{a^{m}} = a^{n - m}$$
This follows directly from the product rule already established. Dividing by $a^{m}$ is equivalent to multiplying by $a^{- m}$, so the quotient can be rewritten as follows.
$$\frac{a^{n}}{a^{m}} = a^{n} \cdot a^{- m} = a^{n + \left(\right. - m \left.\right)} = a^{n - m}$$
The condition $a \neq 0$ is required for $a^{- m}$ to be defined.

---

The quotient of powers with different bases $a$ and $b$ but the same exponent $n$ is a power whose base is the quotient of the original bases.
$$\frac{a^{n}}{b^{n}} = \left(\left(\right. \frac{a}{b} \left.\right)\right)^{n}$$

> Consider the expression $\frac{6^{3}}{2^{3}}$. Since both terms share the same exponent, the quotient can be rewritten as a single power of the ratio of the bases, giving $\frac{6^{3}}{2^{3}} = \left(\left(\right. \frac{6}{2} \left.\right)\right)^{3} = 3^{3} = 27$.

---

The power of a power is a power with the same base and exponent equal to the product of the two exponents.
$$\left(\right. a^{m} \left.\right)^{n} = a^{m \cdot n}$$

> Consider the expression $\left(\right. 2^{3} \left.\right)^{4}$. Applying the rule for the power of a power, the two exponents are multiplied, giving $\left(\right. 2^{3} \left.\right)^{4} = 2^{3 \cdot 4} = 2^{12}$.

---

When a base $a$ is raised to a negative exponent, the result is the reciprocal of the same base raised to the corresponding positive exponent.
$$a^{- n} = \frac{1}{a^{n}} \text{with} a \neq 0 \text{and} n > 0$$

---

When the exponent is a rational number of the form $\frac{m}{n}$, the power can be expressed as a radical.
$$a^{\frac{m}{n}} = \sqrt[n]{a^{m}} \text{where} m , n \in \mathbb{N} \text{and} n \neq 0$$

> The properties of powers transform multiplications and divisions of numbers raised to powers into simpler operations, making calculations faster and more manageable, especially in algebraic expressions.

## Summary

|  |  |  |
| --- | --- | --- |
| Zero exponent | $$a^{0} = 1$$ | $$a \neq 0$$ |
| Power of zero | $$0^{n} = 0$$ | $$n > 0$$ |
| Product (same base) | $$a^{n} \cdot a^{m} = a^{n + m}$$ | $$a \in \mathbb{R}$$ |
| Product (same exponent) | $$a^{n} \cdot b^{n} = \left(\right. a b \left.\right)^{n}$$ | $$a , b \in \mathbb{R}$$ |
| Quotient (same base) | $$\frac{a^{n}}{a^{m}} = a^{n - m}$$ | $$a \neq 0$$ |
| Quotient (same exponent) | $$\frac{a^{n}}{b^{n}} = \left(\left(\right. \frac{a}{b} \left.\right)\right)^{n}$$ | $$b \neq 0$$ |
| Power of a power | $$\left(\right. a^{m} \left.\right)^{n} = a^{m n}$$ | $$a \in \mathbb{R}$$ |
| Negative exponent | $$a^{- n} = \frac{1}{a^{n}}$$ | $$a \neq 0 , n > 0$$ |
| Rational exponent | $$a^{\frac{m}{n}} = \sqrt[n]{a^{m}}$$ | $$a > 0 , n \neq 0$$ |
| Real exponent | $$a^{x} = e^{x ln ⁡ a}$$ | $$a > 0 , x \in \mathbb{R}$$ |

## Why is $a^{0} = 1$?

Among the properties of exponents, the result $a^{0} = 1$ may initially seem counterintuitive, but this outcome follows directly from the quotient rule, which states that dividing any power by itself yields $1$.
$$\frac{a^{n}}{a^{n}} = 1$$
Applying the quotient rule to the left-hand side gives the following.
$$\frac{a^{n}}{a^{n}} = a^{n - n} = a^{0}$$
This reasoning establishes that $a^{0} = 1$. The condition $a \neq 0$ is a direct consequence of the argument, since the expression $\frac{a^{n}}{a^{n}}$ is defined only when $a \neq 0$.

## Power and exponential

Sometimes, people mistakenly mix up the concepts of power and exponential function. A power is an arithmetic operation in which a base $a$ is multiplied by itself $n$ times, with $n$ referred to as the exponent. The [exponential function](https://algebrica.org/exponential-function/), by contrast, is a function in which the variable appears in the exponent rather than the base, taking the form:
$$f \left(\right. x \left.\right) = e^{x} \text{or} f \left(\right. x \left.\right) = a^{x}$$
where $a > 0$ and $a \neq 1$.

## Powers with complex exponents

The definition $a^{x} = e^{x ln ⁡ a}$ extends naturally to cases where the exponent is complex. When the exponent is purely imaginary, that is, when $x = i \theta$ with $\theta \in \mathbb{R}$, the expression $e^{i \theta}$ is well-defined provided one interprets the exponential through its Taylor series expansion. Recalling that:
$$e^{z} = \sum_{n = 0}^{\infty} \frac{z^{n}}{n !}$$
and substituting $z = i \theta$, the series separates into real and imaginary parts by exploiting the periodicity of the powers of $i$, yielding Euler’s formula.
$$e^{i \theta} = cos ⁡ \theta + i sin ⁡ \theta$$
This result establishes a profound connection between the exponential function and trigonometry, showing that the two are in fact different expressions of the same underlying structure over the complex numbers. It enables any complex number to be represented in exponential form as $z = r e^{i \theta}$, where $r$ denotes the modulus and $\theta$ the argument. A notable consequence is one of the most celebrated identities in mathematics, obtained by setting $\theta = \pi$.
$$e^{i \pi} + 1 = 0$$
This equation, known as Euler’s identity, unites five fundamental mathematical constants in a single expression. A comprehensive discussion of complex exponents, including methods for computing powers and roots of complex numbers, is provided in the page [complex numbers in exponential form](https://algebrica.org/complex-numbers-exponential-form/).

indeterminate formspower rulespower of a powerproduct same exponentquotient same baseproduct same basecomplex exponentreal exponentrational exponentnegative exponentzero exponentsign and paritygeometric meaningrepeated multiplicationbase and exponentdefinitionoperationsextensionsfoundations
