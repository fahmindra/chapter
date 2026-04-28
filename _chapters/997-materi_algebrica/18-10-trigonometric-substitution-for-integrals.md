---
layout: chapter
title: "Trigonometric Substitution for Integrals"
chapter: "Integrals"
chapter_order: 18
section_order: 10
permalink: /materi-algebrica/integrals/trigonometric-substitution-for-integrals/
---

## How trigonometric substitution works

Trigonometric substitution is a method for evaluating [integrals](https://algebrica.org/indefinite-integrals/) that contain [square roots](https://algebrica.org/radicals/) of quadratic expressions. It is based on a simple idea: certain algebraic forms become much easier to handle once they are rewritten using the [Pythagorean identities](https://algebrica.org/pythagorean-identity/) of trigonometry. The method consists of a change of variables $x = \phi \left(\right. \theta \left.\right)$ chosen so that the quadratic expression under the radical is transformed into the square of a trigonometric function in the new variable.

---

After an appropriate algebraic manipulation, many integrals in elementary calculus can be reduced to one of the following canonical forms, with $a > 0$:

$$\sqrt{a^{2} - x^{2}}$$
$$\sqrt{x^{2} + a^{2}}$$
$$\sqrt{x^{2} - a^{2}}$$

For the radical to be real-valued, the variable $x$ must lie in the corresponding domain:

- $\sqrt{a^{2} - x^{2}}$ requires $x \in \left[\right. - a , a \left]\right.$
- $\sqrt{x^{2} + a^{2}}$ is defined $\forall x \in \mathbb{R}$
- $\sqrt{x^{2} - a^{2}}$ requires $x \in \left(\right. - \infty , - a \left]\right. \cup \left[\right. a , \infty \left.\right)$

These restrictions are essential, since they determine not only where the integrand is defined, but also the admissible range of the auxiliary angle $\theta$ introduced in the substitution. In particular, the choice of the [interval](https://algebrica.org/intervals/) for $\theta$ ensures that inverse trigonometric functions are well defined and that absolute values arising from square roots can be handled consistently. Each of these expressions is naturally linked to a [Pythagorean identity](https://algebrica.org/pythagorean-identity/):

$$1 - sin^{2} ⁡ \theta = cos^{2} ⁡ \theta$$
$$1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$$
$$sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$$

###### The substitutions are chosen so that the term inside the square root matches the left-hand side of one of these identities, turning the radical into an expression without radicals. The three standard cases are shown below, each illustrating how a suitable trigonometric substitution transforms the radical expression into a perfect square and simplifies the integral.

In practice, the expression under the square root is rarely presented in one of the three canonical forms straight away. A common preliminary step is to rewrite a general quadratic $a x^{2} + b x + c$ in a form that matches one of the standard patterns, by [completing the square](https://algebrica.org/completing-the-square/).

For instance, $x^{2} + 4 x + 5$ becomes $\left(\right. x + 2 \left.\right)^{2} + 1$ after completing the square, which is of the form $u^{2} + a^{2}$ with $u = x + 2$ and $a = 1$.
Once the quadratic has been rewritten in this way, a simple substitution $u = x + k$ reduces the integral to one of the three cases described below, and the appropriate trigonometric substitution can then be applied.

###### Recognizing this preliminary step is often the key to seeing which substitution is needed, and skipping it is a frequent source of confusion when the integrand does not immediately match a familiar pattern.

## From substitutions to geometry

From a geometric point of view, these substitutions can be interpreted as parametrizations of conic sections.

- The identity $sin^{2} ⁡ \theta + cos^{2} ⁡ \theta = 1$ corresponds to the [unit circle](https://algebrica.org/unit-circle/) and underlies the case $\sqrt{a^{2} - x^{2}}$.
- The identities $1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$ and $sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$ are related to the geometry of the [hyperbola](https://algebrica.org/hyperbola/) $x^{2} - y^{2} = a^{2}$, and underlie the forms $\sqrt{x^{2} + a^{2}}$ and $\sqrt{x^{2} - a^{2}}$.

In this sense, trigonometric substitution is not merely an algebraic trick, but a geometric reparametrization of quadratic curves.

## The form $\sqrt{a^{2} - x^{2}}$

When the integrand contains an expression of the form $\sqrt{a^{2} - x^{2}}$, it is appropriate to introduce a trigonometric substitution that reflects the [Pythagorean identity](https://algebrica.org/pythagorean-identity/) $1 - sin^{2} ⁡ \theta = cos^{2} ⁡ \theta$ which itself follows from the fundamental relation between [sine and cosine](https://algebrica.org/sine-and-cosine/). For this reason, we set:

$$x = a sin ⁡ \theta$$

so that the algebraic quantity under the square root can be rewritten in terms of a trigonometric [function](https://algebrica.org/functions). Differentiating both sides of the substitution with respect to $\theta$, we obtain:

$$d x = a cos ⁡ \theta d \theta$$

Substituting $x = a sin ⁡ \theta$ into the radical expression, we can rewrite the square root as follows:

$$\sqrt{a^{2} - x^{2}} = \sqrt{a^{2} - a^{2} sin^{2} ⁡ \theta}$$

Factoring out $a^{2}$ from the expression inside the radical yields:

$$\sqrt{a^{2} \left(\right. 1 - sin^{2} ⁡ \theta \left.\right)}$$

Using the identity $1 - sin^{2} ⁡ \theta = cos^{2} ⁡ \theta$, this becomes:

$$\sqrt{a^{2} cos^{2} ⁡ \theta} = a \sqrt{cos^{2} ⁡ \theta} = a \left|\right. cos ⁡ \theta \left|\right.$$

To avoid ambiguity related to the absolute value, it is customary to restrict the angle $\theta$ to the interval:

$$\theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$$

since on this interval we have $cos ⁡ \theta \geq 0$. Under this restriction, the absolute value is no longer necessary, and the radical simplifies to:

$$\sqrt{a^{2} - x^{2}} = a cos ⁡ \theta$$

Finally, returning to the original variable $x$, the relationships implied by the substitution can be written explicitly as:

$$sin ⁡ \theta = \frac{x}{a}$$

$$cos ⁡ \theta = \frac{\sqrt{a^{2} - x^{2}}}{a}$$

and therefore the angle can be expressed through the [arcsine](https://algebrica.org/arcsine-and-arccosine/):

$$\theta = arcsin ⁡ \left(\right. \frac{x}{a} \left.\right)$$

These relations allow us to express the final result of the integration entirely in terms of the original variable.

###### A geometric interpretation is often helpful: if $sin ⁡ \theta = x / a$, one may use a [right triangle](https://algebrica.org/right-triangle-trigonometry/) with hypotenuse $a$, opposite side $x$, and adjacent side $\sqrt{a^{2} - x^{2}}$.

The standard correspondences for $\sqrt{a^{2} - x^{2}}$ can be memorized as follows:

- Radical form: $\sqrt{a^{2} - x^{2}}$
- Substitution: $x = a sin ⁡ \theta$
- Identity used: $1 - sin^{2} ⁡ \theta = cos^{2} ⁡ \theta$

## Geometric interpretation

When working with trigonometric substitutions, it is often useful to visualize the relationship between $\theta$ and $x$ through a right triangle. Rather than relying on algebraic identities alone, one can read off the values of all trigonometric functions directly from the sides of the triangle, without needing to solve for $\theta$ explicitly.

![Right triangle for the substitution with sine: the three sides correspond to the hypotenuse, the opposite, and the adjacent as labeled.](https://algebrica.org/wp-content/uploads/resources/images/trigonometrix-substitution.png)

From $x = a sin ⁡ \theta$, we construct a right triangle where:

- the hypotenuse is $a$
- the opposite side is $x$
- the adjacent side is $\sqrt{a^{2} - x^{2}}$

Since $sin ⁡ \theta = \frac{x}{a}$ it follows that $cos ⁡ \theta = \frac{\sqrt{a^{2} - x^{2}}}{a} .$ This geometric representation allows all trigonometric functions of $\theta$ to be rewritten directly in terms of $x$.

###### The same construction applies to the other two standard forms: for $\sqrt{x^{2} + a^{2}}$ one draws a triangle with opposite side $x$, adjacent side $a$, and hypotenuse $\sqrt{x^{2} + a^{2}}$; for $\sqrt{x^{2} - a^{2}}$ the hypotenuse becomes $x$, the adjacent side $a$, and the opposite side $\sqrt{x^{2} - a^{2}}$. In each case the triangle is built directly from the substitution and serves as a reliable guide for the back-substitution step.

## Example 1

Let us evaluate the following integral:

$$\int \sqrt{a^{2} - x^{2}} d x \left(\right. a > 0 \left.\right)$$

Since the integrand contains the expression $\sqrt{a^{2} - x^{2}}$, we introduce the trigonometric substitution:

$$x = a sin ⁡ \theta \theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$$

so that we can use the identity $1 - sin^{2} ⁡ \theta = cos^{2} ⁡ \theta$ with $cos ⁡ \theta \geq 0$ on this interval. Differentiating the substitution gives:

$$d x = a cos ⁡ \theta d \theta$$

---

We now rewrite the radical:

$$\sqrt{a^{2} - x^{2}} = \sqrt{a^{2} - a^{2} sin^{2} ⁡ \theta} = a \sqrt{1 - sin^{2} ⁡ \theta} = a cos ⁡ \theta$$

Substituting everything into the integral we obtain:

$$\int \sqrt{a^{2} - x^{2}} d x = \int \left(\right. a cos ⁡ \theta \left.\right) \left(\right. a cos ⁡ \theta d \theta \left.\right) = a^{2} \int cos^{2} ⁡ \theta d \theta$$

To integrate $cos^{2} ⁡ \theta$, we use the [double-angle identity](https://algebrica.org/reduction-formulas-and-reference-angles/):

$$cos^{2} ⁡ \theta = \frac{1 + cos ⁡ 2 \theta}{2}$$

Therefore:

$$a^{2} \int cos^{2} ⁡ \theta d \theta = \frac{a^{2}}{2} \int \left(\right. 1 + cos ⁡ 2 \theta \left.\right) d \theta$$

Integrating term by term we have:

$$\frac{a^{2}}{2} \theta + \frac{a^{2}}{4} sin ⁡ 2 \theta + c$$

---

Returning to the variable $x$, from the substitution $x = a sin ⁡ \theta$, we have:

$$\theta = arcsin ⁡ \left(\right. \frac{x}{a} \left.\right)$$

To rewrite $sin ⁡ 2 \theta$, we use:

$$sin ⁡ 2 \theta = 2 sin ⁡ \theta cos ⁡ \theta$$

And since:

$$sin ⁡ \theta = \frac{x}{a} cos ⁡ \theta = \frac{\sqrt{a^{2} - x^{2}}}{a}$$

we obtain:

$$sin ⁡ 2 \theta = 2 \cdot \frac{x}{a} \cdot \frac{\sqrt{a^{2} - x^{2}}}{a} = \frac{2 x \sqrt{a^{2} - x^{2}}}{a^{2}}$$

Substituting back:

$$\frac{a^{2}}{2} \theta + \frac{a^{2}}{4} sin ⁡ 2 \theta = \frac{a^{2}}{2} arcsin ⁡ \left(\right. \frac{x}{a} \left.\right) + \frac{x}{2} \sqrt{a^{2} - x^{2}}$$

The result is:

$$\int \sqrt{a^{2} - x^{2}} d x = \frac{x}{2} \sqrt{a^{2} - x^{2}} + \frac{a^{2}}{2} arcsin ⁡ \left(\right. \frac{x}{a} \left.\right) + c$$

###### This completes the computation. The integral has been reduced to a trigonometric form, evaluated using standard identities, and finally rewritten entirely in terms of the original variable $x$.

## The form $\sqrt{x^{2} + a^{2}}$

When the integrand contains an expression of the form $\sqrt{x^{2} + a^{2}}$, it is convenient to introduce a substitution based on the [Pythagorean identity](https://algebrica.org/pythagorean-identity/):

$$1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$$

which relates the [tangent](https://algebrica.org/tangent-and-cotangent/) and the [secant](https://algebrica.org/secant-and-cosecant/). For this reason, we set $x = a tan ⁡ \theta$ so that the quadratic expression inside the square root can be rewritten in terms of a trigonometric function. Differentiating both sides with respect to $\theta$, we obtain:

$$d x = a sec^{2} ⁡ \theta d \theta$$

Substituting $x = a tan ⁡ \theta$ into the radical expression gives:

$$\sqrt{x^{2} + a^{2}} = \sqrt{a^{2} tan^{2} ⁡ \theta + a^{2}}$$

Factoring out $a^{2}$ from the expression inside the square root, we obtain:

$$\sqrt{a^{2} \left(\right. tan^{2} ⁡ \theta + 1 \left.\right)}$$

Using the identity $1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$, this becomes:

$$\sqrt{a^{2} sec^{2} ⁡ \theta} = a \sqrt{sec^{2} ⁡ \theta} = a \left|\right. sec ⁡ \theta \left|\right.$$

To eliminate the ambiguity introduced by the absolute value, it is standard to restrict the angle $\theta$ to the following interval:

$$\theta \in \left(\right. - \frac{\pi}{2} , \frac{\pi}{2} \left.\right)$$

since on this interval $cos ⁡ \theta > 0$ and therefore $sec ⁡ \theta > 0$. Under this restriction, the radical simplifies to:

$$\sqrt{x^{2} + a^{2}} = a sec ⁡ \theta$$

Returning to the original variable $x$, the relationships implied by the substitution can be written explicitly as:

$$tan ⁡ \theta = \frac{x}{a}$$
$$sec ⁡ \theta = \frac{\sqrt{x^{2} + a^{2}}}{a}$$
$$\theta = arctan ⁡ \left(\right. \frac{x}{a} \left.\right)$$

##### The corresponding geometric interpretation is immediate: from the relation $tan ⁡ \theta = \frac{x}{a}$, one may construct a right triangle in which the adjacent side has length $a$, the opposite side has length $x$, and the hypotenuse, by the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/), has length $\sqrt{x^{2} + a^{2}}$. This triangle provides a clear geometric picture of the substitution and helps visualize why the radical expression becomes a trigonometric function.

The standard correspondences for $\sqrt{x^{2} + a^{2}}$ can be memorized as follows:

- Radical form: $\sqrt{x^{2} + a^{2}}$
- Substitution: $x = a tan ⁡ \theta$
- Identity used: $1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$

## Example 2

Let us evaluate the following integral:

$$\int \frac{d x}{\sqrt{x^{2} + a^{2}}} \left(\right. a > 0 \left.\right)$$

Since the integrand contains the expression $\sqrt{x^{2} + a^{2}}$, we introduce the trigonometric substitution:

$$x = a tan ⁡ \theta \theta \in \left(\right. - \frac{\pi}{2} , \frac{\pi}{2} \left.\right)$$

so that we can use the identity $1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$ with $sec ⁡ \theta > 0$ on this interval. Differentiating the substitution gives:

$$d x = a sec^{2} ⁡ \theta d \theta$$

---

We now rewrite the radical:

$$\sqrt{x^{2} + a^{2}} & = \sqrt{a^{2} tan^{2} ⁡ \theta + a^{2}} \\ & = a \sqrt{tan^{2} ⁡ \theta + 1} \\ & = a sec ⁡ \theta$$

Substituting everything into the integral we obtain:

$$\int \frac{d x}{\sqrt{x^{2} + a^{2}}} = \int \frac{a sec^{2} ⁡ \theta}{a sec ⁡ \theta} d \theta = \int sec ⁡ \theta d \theta$$

To evaluate $\int sec ⁡ \theta d \theta$, we multiply numerator and denominator by $sec ⁡ \theta + tan ⁡ \theta$:

$$\int sec ⁡ \theta d \theta & = \int \frac{sec ⁡ \theta \left(\right. sec ⁡ \theta + tan ⁡ \theta \left.\right)}{sec ⁡ \theta + tan ⁡ \theta} d \theta \\ & = \int \frac{sec^{2} ⁡ \theta + sec ⁡ \theta tan ⁡ \theta}{sec ⁡ \theta + tan ⁡ \theta} d \theta$$

Setting $u = sec ⁡ \theta + tan ⁡ \theta$, we have $d u = \left(\right. sec^{2} ⁡ \theta + sec ⁡ \theta tan ⁡ \theta \left.\right) , d \theta$, so the numerator is exactly $d u$ and the integral reduces to:

$$\int \frac{d u}{u} = ln ⁡ \left|\right. u \left|\right. + c = ln ⁡ \left|\right. sec ⁡ \theta + tan ⁡ \theta \left|\right. + c$$

---

Returning to the variable $x$, since:

$$tan ⁡ \theta = \frac{x}{a} sec ⁡ \theta = \frac{\sqrt{x^{2} + a^{2}}}{a}$$

we obtain:

$$ln ⁡ \left|\right. sec ⁡ \theta + tan ⁡ \theta \left|\right. + c = ln ⁡ \left|\right. \frac{\sqrt{x^{2} + a^{2}} + x}{a} \left|\right. + c$$

Since $\sqrt{x^{2} + a^{2}} > \left|\right. x \left|\right.$ for all $x \in \mathbb{R}$, the quantity $\sqrt{x^{2} + a^{2}} + x$ is strictly positive, and the absolute value can be dropped. Moreover:

$$ln ⁡ \left|\right. \frac{\sqrt{x^{2} + a^{2}} + x}{a} \left|\right. = ln \left(\right. \sqrt{x^{2} + a^{2}} + x \left.\right) - ln ⁡ a$$

and $ln ⁡ a$ is a constant that can be absorbed into $c$.

The result is:

$$\int \frac{d x}{\sqrt{x^{2} + a^{2}}} = ln \left(\right. \sqrt{x^{2} + a^{2}} + x \left.\right) + c$$

###### This completes the computation. The integral has been reduced to a trigonometric form, evaluated by a standard manipulation of the secant, and finally rewritten entirely in terms of the original variable $x$.

## The form $\sqrt{x^{2} - a^{2}}$

When the integrand contains an expression of the form $\sqrt{x^{2} - a^{2}}$, it is natural to introduce a substitution based on the Pythagorean identity:

$$sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$$

which is equivalent to the fundamental relation $1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$. For this reason, we set:

$$x = a sec ⁡ \theta$$

so that the quadratic expression inside the square root can be rewritten in terms of trigonometric functions. Differentiating both sides with respect to $\theta$, we obtain:

$$d x = a sec ⁡ \theta tan ⁡ \theta d \theta$$

Substituting $x = a sec ⁡ \theta$ into the radical expression gives:

$$\sqrt{x^{2} - a^{2}} = \sqrt{a^{2} sec^{2} ⁡ \theta - a^{2}}$$

Factoring out $a^{2}$ inside the square root, we obtain

$$\sqrt{a^{2} \left(\right. sec^{2} ⁡ \theta - 1 \left.\right)}$$

Using the identity $sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$, this becomes:

$$\sqrt{a^{2} tan^{2} ⁡ \theta} = a \sqrt{tan^{2} ⁡ \theta} = a \left|\right. tan ⁡ \theta \left|\right.$$

The presence of the absolute value reflects the fact that the sign of $tan ⁡ \theta$ depends on the chosen domain for $\theta$. For example, if we are working under the assumption $x \geq a$, a convenient restriction is:

$$\theta \in \left[\right. 0 , \frac{\pi}{2} \left.\right)$$

since on this interval we have $sec ⁡ \theta \geq 1$ and $tan ⁡ \theta \geq 0$. Under this restriction, the radical simplifies to:

$$\sqrt{x^{2} - a^{2}} = a tan ⁡ \theta$$

###### When $x \leq - a$, one instead restricts $\theta \in \left(\right. \frac{\pi}{2} , \pi \left]\right.$, so that $sec ⁡ \theta \leq - 1$ and $tan ⁡ \theta \leq 0$; in that case $\left|\right. tan ⁡ \theta \left|\right. = - tan ⁡ \theta .$ For most textbook problems it suffices to assume $x \geq a$ and work with the interval $\left[\right. 0 , \frac{\pi}{2} \left.\right)$.

---

Returning to the original variable $x$, the relationships implied by the substitution can be written explicitly as:

$$sec ⁡ \theta = \frac{x}{a}$$
$$tan ⁡ \theta = \frac{\sqrt{x^{2} - a^{2}}}{a}$$

Equivalently, one may express the angle itself through an inverse trigonometric function, writing:

$$\theta = arcsec \left(\right. \frac{x}{a} \left.\right)$$

on a suitable domain. In many practical situations, however, it is sufficient to rewrite $tan ⁡ \theta$ and $sec ⁡ \theta$ directly in terms of $x$ and $\sqrt{x^{2} - a^{2}}$, without explicitly solving for $\theta$.

###### The corresponding geometric interpretation follows directly from the relation $sec ⁡ \theta = x / a$: one may construct a [right triangle](https://algebrica.org/right-triangle-trigonometry/) in which the hypotenuse has length $x$, the adjacent side has length $a$, and the opposite side, by the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/), has length $\sqrt{x^{2} - a^{2}}$. This triangle makes the substitution geometrically transparent and provides a reliable way to read off the values of $sec ⁡ \theta$ and $tan ⁡ \theta$ directly from the sides, without solving for $\theta$ explicitly.

The standard correspondences for $\sqrt{x^{2} - a^{2}}$ can be memorized as follows:

- Radical form:$\sqrt{x^{2} - a^{2}}$
- Substitution: $x = a sec ⁡ \theta$
- Identity used: $sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$

## Example 3

Let us evaluate the following integral:

$$\int \frac{d x}{\sqrt{x^{2} - a^{2}}} \left(\right. a > 0 , x > a \left.\right)$$

Since the integrand contains the expression $\sqrt{x^{2} - a^{2}}$, we introduce the trigonometric substitution:

$$x = a sec ⁡ \theta \theta \in \left[\right. 0 , \frac{\pi}{2} \left.\right)$$

so that we can use the identity $sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$ with $tan ⁡ \theta \geq 0$ on this interval. Differentiating the substitution gives:

$$d x = a sec ⁡ \theta tan ⁡ \theta d \theta$$

---

We now rewrite the radical:

$$\sqrt{x^{2} - a^{2}} & = \sqrt{a^{2} sec^{2} ⁡ \theta - a^{2}} \\ & = a \sqrt{sec^{2} ⁡ \theta - 1} \\ & = a tan ⁡ \theta$$

Substituting everything into the integral we obtain:

$$\int \frac{d x}{\sqrt{x^{2} - a^{2}}} = \int \frac{a sec ⁡ \theta tan ⁡ \theta}{a tan ⁡ \theta} d \theta = \int sec ⁡ \theta d \theta$$

To evaluate $\int sec ⁡ \theta , d \theta$, we multiply numerator and denominator by $sec ⁡ \theta + tan ⁡ \theta$:

$$\int sec ⁡ \theta , d \theta & = \int \frac{sec ⁡ \theta \left(\right. sec ⁡ \theta + tan ⁡ \theta \left.\right)}{sec ⁡ \theta + tan ⁡ \theta} d \theta \\ & = \int \frac{sec^{2} ⁡ \theta + sec ⁡ \theta tan ⁡ \theta}{sec ⁡ \theta + tan ⁡ \theta} d \theta$$

Setting $u = sec ⁡ \theta + tan ⁡ \theta$, we have $d u = \left(\right. sec^{2} ⁡ \theta + sec ⁡ \theta tan ⁡ \theta \left.\right) , d \theta$, so the numerator is exactly $d u$ and the integral reduces to:

$$\int \frac{d u}{u} = ln ⁡ \left|\right. u \left|\right. + c = ln ⁡ \left|\right. sec ⁡ \theta + tan ⁡ \theta \left|\right. + c$$

---

Returning to the variable $x$, since:

$$sec ⁡ \theta = \frac{x}{a} tan ⁡ \theta = \frac{\sqrt{x^{2} - a^{2}}}{a}$$

we obtain:

$$ln ⁡ \left|\right. sec ⁡ \theta + tan ⁡ \theta \left|\right. + c = ln \left|\right. \frac{x + \sqrt{x^{2} - a^{2}}}{a} \left|\right. + c$$

Since $x > a > 0$ and $\sqrt{x^{2} - a^{2}} \geq 0$, the quantity $x + \sqrt{x^{2} - a^{2}}$ is strictly positive, and the absolute value can be dropped. Moreover:

$$ln \left(\right. \frac{x + \sqrt{x^{2} - a^{2}}}{a} \left.\right) = ln \left(\right. x + \sqrt{x^{2} - a^{2}} \left.\right) - ln ⁡ a$$

and $ln ⁡ a$ is a constant that can be absorbed into $c$.

The result is:

$$\int \frac{d x}{\sqrt{x^{2} - a^{2}}} = ln \left(\right. x + \sqrt{x^{2} - a^{2}} \left.\right) + c$$

###### This completes the computation. The structure of the derivation closely mirrors that of Example 2: in both cases the substitution reduces the integral to $\int sec ⁡ \theta , d \theta$, and the difference lies entirely in the back-substitution step, where the expressions for $sec ⁡ \theta$ and $tan ⁡ \theta$ in terms of $x$ reflect the geometry of the two distinct radical forms.

## Summary

| Radical form | Substitution | Identity | Domain |
| --- | --- | --- | --- |
| $\sqrt{a^{2} - x^{2}}$ | $x = a sin ⁡ \theta$ | $1 - sin^{2} ⁡ \theta = cos^{2} ⁡ \theta$ | $\theta \in \left[\right. - \frac{\pi}{2} , \frac{\pi}{2} \left]\right.$ |
| $\sqrt{x^{2} + a^{2}}$ | $x = a tan ⁡ \theta$ | $1 + tan^{2} ⁡ \theta = sec^{2} ⁡ \theta$ | $\theta \in \left(\right. - \frac{\pi}{2} , \frac{\pi}{2} \left.\right)$ |
| $\sqrt{x^{2} - a^{2}}$ | $x = a sec ⁡ \theta$ | $sec^{2} ⁡ \theta - 1 = tan^{2} ⁡ \theta$ | $\theta \in \left[\right. 0 , \frac{\pi}{2} \left.\right)$ |

## Selected references

- **James Stewart**. [Trigonometric Substitution (Student Support)](https://www.stewartcalculus.com/data/CALCULUS%20Concepts%20and%20Contexts/upfiles/3c3-TrigonometSubstitu_Stu.pdf)
- **Trinity University**. [Trigonometric Substitution – Calculus II Lecture Slides](https://ramanujan.math.trinity.edu/rdaileda/teach/s21/m1312/lectures/lecture6_slides.pdf)
- **University of California**. [Trigonometric Substitution (Notes with Exercises)](https://www.math.ucdavis.edu/~kouba/CalcTwoDIRECTORY/trigsubdirectory/TrigSub.html)
