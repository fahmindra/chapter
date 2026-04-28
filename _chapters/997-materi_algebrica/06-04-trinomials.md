---
layout: chapter
title: "Trinomials"
chapter: "Polynomials"
chapter_order: 6
section_order: 4
permalink: /materi-algebrica/polynomials/trinomials/
---

## Definition

A trinomial is defined as a [polynomial](https://algebrica.org/polynomials/) consisting of exactly three non-zero, pairwise distinct terms. More generally, within a commutative ring with unity, a trinomial in the indeterminate $x$ is any expression of the form:

$$a_{n} x^{n} + a_{m} x^{m} + a_{k} x^{k}$$
$$n > m > k \geq 0$$

The coefficients $a_{n} , a_{m} , a_{k}$ are non-zero elements of the ring. When the underlying ring is $\mathbb{R}$, the coefficients are real numbers and the degree of the trinomial is $n$.

> A [ring](https://algebrica.org/rings/) is a set equipped with addition and multiplication satisfying the standard algebraic axioms: associativity, distributivity, and the existence of an additive identity and inverses. A commutative ring with unity additionally requires commutativity of multiplication and a multiplicative identity. Typical examples are $\mathbb{Z}$, $\mathbb{R}$, and $\mathbb{C} .$

---

The [quadratic trinomial](https://algebrica.org/quadratic-equations/) in one variable, which has degree two, is the most frequently studied case and takes the following canonical form where $a , b , c \in \mathbb{R}$ and $a \neq 0$:

$$(\text{1}) a x^{2} + b x + c$$

The requirement $a \neq 0$ is essential because, if omitted, the leading term vanishes and the expression ceases to be quadratic. The coefficient $a$ is referred to as the leading coefficient, $b$ as the linear coefficient, and $c$ as the constant term.

Not every polynomial with three terms is of the form (1). For example, expressions such as $x^{3} + 2 x + 1$, $x^{4} - x^{2} + 3$, and $x^{2} y + x y^{2} - 1$ are all trinomials, each representing a distinct class. The subsequent discussion primarily addresses the quadratic case, with a dedicated section for higher-degree trinomials that can be reduced to this form through substitution.

---

The quadratic trinomial (1) defines the quadratic function $f \left(\right. x \left.\right) = a x^{2} + b x + c$, whose graph is a [parabola](https://algebrica.org/parabola/). The vertex form indicates that the vertex of the parabola is located at

$$\left(\right. - \frac{b}{2 a} , - \frac{\Delta}{4 a} \left.\right)$$

The parabola opens upward if $a > 0$ and downward if $a < 0$.

![](https://algebrica.org/wp-content/uploads/resources/images/trinomials.png "Parabola.")

The number of intersections with the $x$-axis corresponds to the number of distinct real roots. The sign of $\Delta$ provides a geometric interpretation: $\Delta > 0$ indicates two $x$-intercepts, $\Delta = 0$ indicates tangency to the $x$-axis, and $\Delta < 0$ indicates no real intersection.

## Classification of trinomials

Trinomials are classified according to two primary criteria: degree and number of variables. With respect to degree, the simplest non-trivial trinomials in one variable are quadratic trinomials (degree 2). Cubic trinomials, such as $x^{3} + p x + q$, are significant in the theory of cubic equations, while degree-four trinomials arise in the study of biquadratic equations.

In the case of two variables, trinomials of the form $a x^{2} + b x y + c y^{2}$ represent homogeneous quadratic forms. Homogeneous trinomials deserve a brief mention: a trinomial $a x^{n} + b x^{n - 1} y + c y^{n - 2}$ is not homogeneous unless all three terms share the same total degree. The trinomial $x^{2} + x y + y^{2}$, for instance, is homogeneous of degree 2, while $x^{2} + x y + y$ is not.

## The discriminant

The algebraic properties of the quadratic trinomial $a x^{2} + b x + c$ are determined by a single quantity known as the discriminant, defined as follows:

$$(\text{2}) \Delta = b^{2} - 4 a c$$

The discriminant determines the nature of the [roots](https://algebrica.org/roots-of-a-polynomial/) of the quadratic equation $a x^{2} + b x + c = 0$ and, consequently, the factorisation structure of the trinomial over the real numbers $\mathbb{R}$ and the complex numbers $\mathbb{C}$. Three distinct cases arise based on the value of the discriminant.

If $\Delta > 0$, the trinomial possesses two distinct real roots, $x_{1}$ and $x_{2}$, which are given by the [quadratic formula](https://algebrica.org/quadratic-formula/):

$$(\text{3}) x_{1 , 2} = \frac{- b \pm \sqrt{\Delta}}{2 a}$$

If $\Delta = 0$, the two roots coincide, resulting in a single value $x_{0} = - b / \left(\right. 2 a \left.\right)$, referred to as a repeated root or a root of multiplicity two.

If $\Delta < 0$, the trinomial has no real roots and is irreducible over $\mathbb{R}$, as it cannot be expressed as a product of two linear factors with real coefficients. However, over the [complex numbers](https://algebrica.org/complex-numbers-introduction/) $\mathbb{C}$, formula (3) remains valid, with $\sqrt{\Delta}$ interpreted as $i \sqrt{\left|\right. \Delta \left|\right.}$, resulting in a conjugate pair of [complex roots](https://algebrica.org/quadratic-equations-with-complex-solutions/).

---

If $\Delta \geq 0$, the trinomial in equation (1) can be completely factorised over the real numbers:

$$(\text{4}) a x^{2} + b x + c = a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$$

$x_{1}$ and $x_{2}$ denote the roots specified in equation (3). In the case of a repeated root, this factorisation simplifies to

$$a x^{2} + b x + c = a \left(\right. x - x_{0} \left.\right)^{2}$$

The factorisation in equation (4) represents the product form of the trinomial. This form is fundamental for simplifying rational expressions, solving inequalities, and evaluating [limits](https://algebrica.org/limits/) and [integrals](https://algebrica.org/definite-integrals/) that involve quadratic denominators.

## Vieta’s formulas

An immediate consequence of equation (4) is that the roots satisfy the following relations, known as Vieta’s formulas:

$$(\text{5}) \begin{matrix}x_{1} + x_{2} & = - \frac{b}{a} \\ x_{1} x_{2} & = \frac{c}{a}\end{matrix}$$

These identities are derived by expanding $a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$ and equating coefficients with $a x^{2} + b x + c$. Vieta’s formulas are particularly useful because they enable verification of a factorisation without explicitly computing the roots and underpin several factorisation techniques. For example, to factor $x^{2} - 5 x + 6$, it is necessary to identify two numbers whose sum is 5 and whose product is 6. We can use this simple scheme to find the numbers that satisfy our constraints.

$$m & n & P & S \\ 1 & 6 & 6 & 7 \\ - 1 & - 6 & 6 & - 7 \\ 2 & 3 & 6 & 5 \\ - 2 & - 3 & 6 & - 5$$

The pair $\left(\right. 2 , 3 \left.\right)$ in row 3 satisfies both conditions, thus:

$$x^{2} - 5 x + 6 = \left(\right. x - 2 \left.\right) \left(\right. x - 3 \left.\right)$$

> This mental arithmetic approach is effective whenever the roots are rational.

## Example 1

Factor the trinomial $3 x^{2} - 7 x + 2$. The first step is to compute the discriminant: $\Delta = \left(\right. - 7 \left.\right)^{2} - 4 \cdot 3 \cdot 2 = 49 - 24 = 25 > 0$. Since $\Delta > 0$, the trinomial has two distinct real roots, which can be determined using the quadratic formula:

$$x_{1 , 2} = \frac{7 \pm \sqrt{25}}{6} = \frac{7 \pm 5}{6}$$

This calculation yields $x_{1} = 12 / 6 = 2$ and $x_{2} = 2 / 6 = 1 / 3$. The factorisation over $\mathbb{R}$ is therefore

$$3 x^{2} - 7 x + 2 & = 3 \left(\right. x - 2 \left.\right) \left(\right. x - \frac{1}{3} \left.\right) \\ & = \left(\right. x - 2 \left.\right) \left(\right. 3 x - 1 \left.\right)$$

As a consistency check, Vieta’s formulas (5) require that $x_{1} + x_{2} = - b / a$ and $x_{1} x_{2} = c / a$. Indeed, $x_{1} + x_{2} = 2 + 1 / 3 = 7 / 3$ and $x_{1} x_{2} = 2 \cdot 1 / 3 = 2 / 3$, both in agreement with $- b / a = 7 / 3$ and $c / a = 2 / 3$.

The factorisation therefore yields:
$$\left(\right. x - 2 \left.\right) \left(\right. 3 x - 1 \left.\right)$$

## Perfect square trinomials

A trinomial is defined as a perfect square if it can be expressed as the square of a binomial. The two fundamental identities are as follows:

$$\left(\right. a + b \left.\right)^{2} = a^{2} + 2 a b + b^{2}$$
$$\left(\right. a - b \left.\right)^{2} = a^{2} - 2 a b + b^{2}$$

To identify a perfect square trinomial, three conditions must be verified simultaneously: the first and last terms must be perfect squares (such as $a^{2}$ and $b^{2}$), and the middle term must be exactly $\pm 2 a b$. If any of these conditions is not satisfied, the trinomial is not a perfect square.

For instance, $9 x^{2} - 12 x + 4$ satisfies all conditions: $9 x^{2} = \left(\right. 3 x \left.\right)^{2}$, $4 = 2^{2}$, and $12 x = 2 \cdot 3 x \cdot 2$. Therefore

$$9 x^{2} - 12 x + 4 = \left(\right. 3 x - 2 \left.\right)^{2}$$

A frequent mistake is to assume that $x^{2} + 4 x + 8$ is a perfect square solely because the first term is a perfect square. This is incorrect, as $8 \neq \left(\right. 2 \left.\right)^{2} = 4$. Calculating the discriminant confirms this: $\Delta = 16 - 32 = - 16 < 0$ indicating that the trinomial is irreducible over $\mathbb{R}$.

A perfect square trinomial always has a discriminant $\Delta = 0$, as its two roots are identical. Conversely, any quadratic trinomial with $\Delta = 0$ is a perfect square.

---

For example, determine whether $4 x^{2} - 12 x + 9$ is a perfect square and factor it. To verify, note that $4 x^{2} = \left(\right. 2 x \left.\right)^{2}$, $9 = 3^{2}$, and $12 x = 2 \cdot 2 x \cdot 3$. Since all three conditions are satisfied we have:

$$4 x^{2} - 12 x + 9 = \left(\right. 2 x - 3 \left.\right)^{2}$$

The discriminant $\Delta = 144 - 144 = 0$ confirms the presence of a repeated root at $x_{0} = 3 / 2$.

## Example 2

Determine whether the polynomial $x^{2} + x + 1$ is reducible over $\mathbb{R}$, and identify its complex roots. The discriminant is $\Delta = 1 - 4 = - 3 < 0$. Because $\Delta < 0$, the polynomial has no real roots and is irreducible over $\mathbb{R}$. It cannot be expressed as a product of two linear factors with real coefficients.

Over $\mathbb{C}$, the quadratic formula applies with $\sqrt{\Delta} = i \sqrt{3}$, resulting in a pair of complex conjugate roots:

$$x_{1 , 2} = \frac{- 1 \pm i \sqrt{3}}{2}$$

These roots are primitive sixth roots of unity, as they satisfy $x^{6} = 1$ but $x^{k} \neq 1$ for $k = 1 , 2 , 3 , 4 , 5$. The factorisation over $\mathbb{C} \left[\right. x \left]\right.$ is therefore given by

$$x^{2} + x + 1 = \left(\right. x - \frac{- 1 + i \sqrt{3}}{2} \left.\right) \left(\right. x - \frac{- 1 - i \sqrt{3}}{2} \left.\right)$$

Thus, the trinomial is irreducible over $\mathbb{R}$, and its two complex roots are:
$$x_{1} = \frac{- 1 + i \sqrt{3}}{2} x_{2} = \frac{- 1 - i \sqrt{3}}{2}$$

## The method of completing the square

[Completing the square](https://algebrica.org/completing-the-square/) is a technique used to rewrite any quadratic trinomial of the form $a x^{2} + b x + c$ as an equivalent expression:

$$a \left(\right. x - h \left.\right)^{2} + k$$

$h$ and $k$ are constants determined by the original coefficients. This form allows for direct identification of the vertex of the corresponding [parabola](https://algebrica.org/parabola/) and serves as a fundamental step in deriving the quadratic formula. For a comprehensive discussion, refer to the dedicated page on completing the square.

## Trinomials reducible to quadratic form

Certain higher-degree trinomials may be reduced to quadratic form through an appropriate change of variable. Specifically, a trinomial of the form:

$$a x^{2 n} + b x^{n} + c$$

$n \geq 2$ is a positive [integer](https://algebrica.org/integers/), becomes quadratic when the substitution $t = x^{n}$ is applied:

$$a t^{2} + b t + c$$

The roots $t_{1} , t_{2}$ of the resulting quadratic equation correspond to the roots of the original trinomial, which are obtained by solving $x^{n} = t_{i}$ for each $i$. The number and type of solutions depend on the value of $n$ and the sign of each $t_{i}$. When $n = 2$, the trinomial is referred to as a biquadratic trinomial. For example, consider

$$x^{4} - 5 x^{2} + 4$$

Applying the substitution $t = x^{2}$ results in:

$$t^{2} - 5 t + 4 = \left(\right. t - 1 \left.\right) \left(\right. t - 4 \left.\right)$$

So $t = 1$ or $t = 4.$

Reverting to the original variable, $x^{2} = 1$ yields $x = \pm 1$, and $x^{2} = 4$ yields $x = \pm 2$. Thus, the complete factorisation over $\mathbb{R}$ is:

$$x^{4} - 5 x^{2} + 4 = \left(\right. x - 1 \left.\right) \left(\right. x + 1 \left.\right) \left(\right. x - 2 \left.\right) \left(\right. x + 2 \left.\right)$$

If any value $t_{i}$ is negative and $n$ is even, the equation $x^{n} = t_{i}$ admits no real solutions. In this case, the corresponding factor is irreducible over $\mathbb{R}$ but splits over $\mathbb{C}$.

The trinomial $x^{4} + x^{2} + 1$ serves as a less straightforward example. Substituting $t = x^{2}$ yields $t^{2} + t + 1$, which has discriminant $\Delta = 1 - 4 = - 3 < 0$ and is therefore irreducible over $\mathbb{R}$. However, the original trinomial can be factored over $\mathbb{R}$ by alternative methods, as shown below:

$$x^{4} + x^{2} + 1 & = \left(\right. x^{4} + 2 x^{2} + 1 \left.\right) - x^{2} \\ & = \left(\right. x^{2} + 1 \left.\right)^{2} - x^{2} \\ & = \left(\right. x^{2} + x + 1 \left.\right) \left(\right. x^{2} - x + 1 \left.\right)$$

Each factor is a quadratic trinomial with a negative discriminant, so the factorisation cannot be further refined over $\mathbb{R}$.

## Irreducibility and complex roots

A quadratic trinomial $a x^{2} + b x + c$ with $\Delta < 0$ cannot be decomposed into linear factors over $\mathbb{R}$. Over $\mathbb{C}$, every quadratic polynomial can be factored completely. The roots form a conjugate pair:

$$x_{1 , 2} = \frac{- b \pm i \sqrt{\left|\right. \Delta \left|\right.}}{2 a}$$

The corresponding factorisation is $a \left(\right. x - x_{1} \left.\right) \left(\right. x - x_{2} \left.\right)$, which holds in $\mathbb{C} \left[\right. x \left]\right.$. This result follows from the [Fundamental Theorem of Algebra](https://algebrica.org/roots-of-a-polynomial/), which states that every non-constant polynomial over $\mathbb{C}$ can be factored completely into linear factors.

> This irreducibility constitutes a property with significant implications in real analysis and integration theory. Specifically, integrals involving an irreducible quadratic in the denominator necessitate completing the square and substitution, rather than employing partial fractions with real linear factors.

applicationsfactoringbiquadraticsubstitutionreductioncompleting squarequadratic formulacomplex rootsirreducibilityperfect squarevieta formulasfactorizationrootsdiscriminantparabolaquadratic casecoefficientsdegreegeneral formmethodspropertiesfoundations
