---
layout: chapter
title: "Trigonometric Identities"
chapter: "Trigonometry"
chapter_order: 5
section_order: 10
permalink: /materi-algebrica/trigonometry/trigonometric-identities/
---

## Introduction

A trigonometric identity is an equation involving trigonometric functions that holds for every admissible value of the variables. Unlike a trigonometric equation, which is solved for a specific set of angles, an identity is an equality valid throughout the common domain of the functions it relates. The study of these identities organises the algebraic relationships that tie [sine and cosine](https://algebrica.org/sine-and-cosine/), [tangent and cotangent](https://algebrica.org/tangent-and-cotangent/) together, and provides the tools needed to manipulate trigonometric expressions into equivalent forms that are easier to evaluate, [differentiate](https://algebrica.org/derivatives/), [integrate](https://algebrica.org/indefinite-integrals/), or interpret geometrically.

The identities presented below are grouped into families according to the type of transformation they perform. Some express a [function](https://algebrica.org/functions/) of a modified angle in terms of the original angle, others convert products into sums or sums into products, and others still reduce a general angle to a parametric variable. Each group plays a distinct role in the resolution of [trigonometric equations](https://algebrica.org/trigonometric-equations/), in the simplification of expressions, and in the broader apparatus of calculus.

## Fundamental identities

Before examining the transformations that relate trigonometric functions of different angles, it is useful to recall the elementary identities that connect the six trigonometric functions at a single angle. These identities descend directly from the definitions on the [unit circle](https://algebrica.org/unit-circle/) and from the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/), and they form the algebraic foundation on which every subsequent identity is built. The [Pythagorean identity](https://algebrica.org/pythagorean-identity/) expresses the constraint that the coordinates of any point on the unit circle satisfy the equation of the circle itself:

$$sin^{2} ⁡ \left(\right. \theta \left.\right) + cos^{2} ⁡ \left(\right. \theta \left.\right) = 1$$

Dividing both sides of this identity by $cos^{2} ⁡ \left(\right. \theta \left.\right)$, provided $cos ⁡ \left(\right. \theta \left.\right) \neq 0$, yields the corresponding identity involving the tangent and the [secant](https://algebrica.org/secant-and-cosecant/):

$$1 + tan^{2} ⁡ \left(\right. \theta \left.\right) = sec^{2} ⁡ \left(\right. \theta \left.\right)$$

An analogous division by $sin^{2} ⁡ \left(\right. \theta \left.\right)$, under the assumption $sin ⁡ \left(\right. \theta \left.\right) \neq 0$, produces the identity involving the cotangent and the cosecant:

$$1 + cot^{2} ⁡ \left(\right. \theta \left.\right) = csc^{2} ⁡ \left(\right. \theta \left.\right)$$

The quotient identities relate tangent and cotangent to the ratio of sine and cosine. They follow directly from the definitions of the four functions on the unit circle:

$$& tan ⁡ \left(\right. \theta \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{cos ⁡ \left(\right. \theta \left.\right)} \\ & cot ⁡ \left(\right. \theta \left.\right) = \frac{cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)}$$

> The first identity is valid for $cos ⁡ \left(\right. \theta \left.\right) \neq 0$, the second for $sin ⁡ \left(\right. \theta \left.\right) \neq 0$. Together, the Pythagorean and quotient identities are sufficient to re-express any trigonometric expression in terms of sine and cosine alone, a reduction that is often the first step in the simplification of more elaborate formulas.

## Reference angles and reflections

The method of [reference angles](https://algebrica.org/identities-using-reference-angles/), sometimes called the method of reflections, is a family of identities that allow one to express a trigonometric function of a non-acute angle in terms of the corresponding acute angle in the first quadrant of the Cartesian plane. Any trigonometric function, whether [sine](https://algebrica.org/sine-and-cosine/), [cosine](https://algebrica.org/sine-and-cosine/), [tangent](https://algebrica.org/tangent-and-cotangent/), or [cotangent](https://algebrica.org/tangent-and-cotangent/), with an argument of the form:

$$\frac{\pi}{2} \pm \alpha , \pi \pm \alpha , \frac{3 \pi}{2} \pm \alpha , 2 \pi - \alpha$$

can be rewritten as a function of the acute angle $\alpha$, with an appropriate adjustment of the sign determined by the quadrant in which the angle lies. Consider the angle:

$$\frac{\pi}{2} + \alpha$$

In Cartesian coordinates, this angle lies in the second quadrant.

![Trigonometric Identities.](https://algebrica.org/wp-content/uploads/resources/images/trigonometric-identities-.png "Trigonometric Identities.")

A direct geometric analysis of the corresponding point on the [unit circle](https://algebrica.org/unit-circle/) yields the following two identities:

$$& sin ⁡ \left(\right. \frac{\pi}{2} + \alpha \left.\right) = cos ⁡ \alpha \\ & cos ⁡ \left(\right. \frac{\pi}{2} + \alpha \left.\right) = - sin ⁡ \alpha$$

The vertical segment associated with the sine of $\alpha$ in the first quadrant has the same length as the horizontal segment associated with the cosine of $\frac{\pi}{2} + \alpha$ in the second quadrant, while the sign of the cosine becomes negative because the second quadrant lies to the left of the vertical axis. The same procedure applied to every angle of the form listed above produces a full catalogue of reduction formulas, discussed in detail in the page on [reduction formulas and reference angles](https://algebrica.org/reduction-formulas-and-reference-angles/).

## Sum and difference

The sum and difference formulas express a trigonometric function of the sum or difference of two angles as a combination of the trigonometric functions of the individual angles. For sine and cosine the following identities hold:

$$& sin ⁡ \left(\right. a + b \left.\right) = sin ⁡ \left(\right. a \left.\right) cos ⁡ \left(\right. b \left.\right) + cos ⁡ \left(\right. a \left.\right) sin ⁡ \left(\right. b \left.\right) \\ & sin ⁡ \left(\right. a - b \left.\right) = sin ⁡ \left(\right. a \left.\right) cos ⁡ \left(\right. b \left.\right) - cos ⁡ \left(\right. a \left.\right) sin ⁡ \left(\right. b \left.\right) \\ & cos ⁡ \left(\right. a + b \left.\right) = cos ⁡ \left(\right. a \left.\right) cos ⁡ \left(\right. b \left.\right) - sin ⁡ \left(\right. a \left.\right) sin ⁡ \left(\right. b \left.\right) \\ & cos ⁡ \left(\right. a - b \left.\right) = cos ⁡ \left(\right. a \left.\right) cos ⁡ \left(\right. b \left.\right) + sin ⁡ \left(\right. a \left.\right) sin ⁡ \left(\right. b \left.\right)$$

The analogous identities for tangent and cotangent follow by taking the ratio of the corresponding sine and cosine formulas, provided the denominators do not vanish:

$$& tan ⁡ \left(\right. a + b \left.\right) = \frac{tan ⁡ \left(\right. a \left.\right) + tan ⁡ \left(\right. b \left.\right)}{1 - tan ⁡ \left(\right. a \left.\right) tan ⁡ \left(\right. b \left.\right)} \\ & tan ⁡ \left(\right. a - b \left.\right) = \frac{tan ⁡ \left(\right. a \left.\right) - tan ⁡ \left(\right. b \left.\right)}{1 + tan ⁡ \left(\right. a \left.\right) tan ⁡ \left(\right. b \left.\right)} \\ & cot ⁡ \left(\right. a + b \left.\right) = \frac{cot ⁡ \left(\right. a \left.\right) cot ⁡ \left(\right. b \left.\right) - 1}{cot ⁡ \left(\right. a \left.\right) + cot ⁡ \left(\right. b \left.\right)} \\ & cot ⁡ \left(\right. a - b \left.\right) = \frac{cot ⁡ \left(\right. a \left.\right) cot ⁡ \left(\right. b \left.\right) + 1}{cot ⁡ \left(\right. b \left.\right) - cot ⁡ \left(\right. a \left.\right)}$$

> These identities form the backbone of the entire body of trigonometric identities. The double-angle, half-angle, and prosthaphaeresis formulas are all derived from them through appropriate substitutions or algebraic manipulations.

## Double-angle

The double-angle formulas express the trigonometric functions of an angle $2 \theta$ in terms of the trigonometric functions of $\theta$. For sine and cosine the following identities hold:

$$& sin ⁡ \left(\right. 2 \theta \left.\right) = 2 sin ⁡ \left(\right. \theta \left.\right) cos ⁡ \left(\right. \theta \left.\right) \\ & cos ⁡ \left(\right. 2 \theta \left.\right) = cos^{2} ⁡ \left(\right. \theta \left.\right) - sin^{2} ⁡ \left(\right. \theta \left.\right)$$

The cosine double-angle formula admits two equivalent forms obtained by applying the [Pythagorean identity](https://algebrica.org/pythagorean-identity/) $sin^{2} ⁡ \theta + cos^{2} ⁡ \theta = 1$:

$$& cos ⁡ \left(\right. 2 \theta \left.\right) = 1 - 2 sin^{2} ⁡ \left(\right. \theta \left.\right) \\ & cos ⁡ \left(\right. 2 \theta \left.\right) = 2 cos^{2} ⁡ \left(\right. \theta \left.\right) - 1$$

The corresponding identities for tangent and cotangent are:

$$& tan ⁡ \left(\right. 2 \theta \left.\right) = \frac{2 tan ⁡ \left(\right. \theta \left.\right)}{1 - tan^{2} ⁡ \left(\right. \theta \left.\right)} \\ & cot ⁡ \left(\right. 2 \theta \left.\right) = \frac{cot^{2} ⁡ \left(\right. \theta \left.\right) - 1}{2 cot ⁡ \left(\right. \theta \left.\right)}$$

---

The derivation of the sine double-angle formula proceeds from the sum identity for the sine:

$$sin ⁡ \left(\right. a + b \left.\right) = sin ⁡ \left(\right. a \left.\right) cos ⁡ \left(\right. b \left.\right) + cos ⁡ \left(\right. a \left.\right) sin ⁡ \left(\right. b \left.\right)$$

Setting $a = b = \theta$, the left-hand side becomes $sin ⁡ \left(\right. 2 \theta \left.\right)$ and the right-hand side reduces to two identical terms:

$$sin ⁡ \left(\right. 2 \theta \left.\right) = sin ⁡ \left(\right. \theta \left.\right) cos ⁡ \left(\right. \theta \left.\right) + cos ⁡ \left(\right. \theta \left.\right) sin ⁡ \left(\right. \theta \left.\right)$$

Combining the two identical terms on the right gives the final result:

$$sin ⁡ \left(\right. 2 \theta \left.\right) = 2 sin ⁡ \left(\right. \theta \left.\right) cos ⁡ \left(\right. \theta \left.\right)$$

The same reasoning applied to the sum identity for the cosine, with $a = b = \theta$, yields the double-angle formula for the cosine.

## Example

Consider the [integral](https://algebrica.org/indefinite-integrals/):

$$\int \frac{1 - cos ⁡ \left(\right. 2 \theta \left.\right)}{2} d \theta$$

The integrand contains a cosine of a doubled angle, which makes a direct computation awkward. The double-angle identity $cos ⁡ \left(\right. 2 \theta \left.\right) = 1 - 2 sin^{2} ⁡ \left(\right. \theta \left.\right)$ allows the numerator to be rewritten as:

$$1 - cos ⁡ \left(\right. 2 \theta \left.\right) = 1 - \left(\right. 1 - 2 sin^{2} ⁡ \left(\right. \theta \left.\right) \left.\right) = 2 sin^{2} ⁡ \left(\right. \theta \left.\right)$$

Substituting this result in the original expression transforms the integrand into a single [power](https://algebrica.org/powers) of the sine:

$$\int \frac{2 sin^{2} ⁡ \left(\right. \theta \left.\right)}{2} d \theta = \int sin^{2} ⁡ \left(\right. \theta \left.\right) d \theta$$

The identity has reduced the problem to the integration of $sin^{2} ⁡ \left(\right. \theta \left.\right)$, which is a standard form. The same double-angle identity can now be applied in the opposite direction to linearise the square, writing:

$$sin^{2} ⁡ \left(\right. \theta \left.\right) = \frac{1 - cos ⁡ \left(\right. 2 \theta \left.\right)}{2}$$

The integral becomes elementary:

$$\int sin^{2} ⁡ \left(\right. \theta \left.\right) d \theta = \frac{\theta}{2} - \frac{sin ⁡ \left(\right. 2 \theta \left.\right)}{4} + c$$

> The integral, which at first sight required a non-trivial technique, has been reduced to a sum of elementary antiderivatives through a single trigonometric identity.

## Half-angle formulas

The half-angle formulas express the trigonometric functions of $\frac{\theta}{2}$ in terms of the trigonometric functions of $\theta$. For sine and cosine the following identities hold:

$$& sin ⁡ \left(\right. \frac{\theta}{2} \left.\right) = \pm \sqrt{\frac{1 - cos ⁡ \left(\right. \theta \left.\right)}{2}} \\ & cos ⁡ \left(\right. \frac{\theta}{2} \left.\right) = \pm \sqrt{\frac{1 + cos ⁡ \left(\right. \theta \left.\right)}{2}}$$

The sign on the right-hand side is determined by the quadrant in which the half-angle $\frac{\theta}{2}$ lies, and must be selected according to the geometric position of the angle on the [unit circle](https://algebrica.org/unit-circle/).

The half-angle formulas for tangent and cotangent can be written either in radical form or in rational form. The rational form is generally preferred because it avoids the ambiguity of the sign:

$$& tan ⁡ \left(\right. \frac{\theta}{2} \left.\right) = \frac{sin ⁡ \left(\right. \theta \left.\right)}{1 + cos ⁡ \left(\right. \theta \left.\right)} = \frac{1 - cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)} \\ & cot ⁡ \left(\right. \frac{\theta}{2} \left.\right) = \frac{1 + cos ⁡ \left(\right. \theta \left.\right)}{sin ⁡ \left(\right. \theta \left.\right)} = \frac{sin ⁡ \left(\right. \theta \left.\right)}{1 - cos ⁡ \left(\right. \theta \left.\right)}$$

> The derivation of the half-angle formulas follows from the two alternative forms of the cosine double-angle identity. Writing $cos ⁡ \left(\right. \theta \left.\right) = 1 - 2 sin^{2} ⁡ \left(\right. \theta / 2 \left.\right)$ and solving for $sin ⁡ \left(\right. \theta / 2 \left.\right)$ yields the half-angle formula for the sine; the analogous manipulation on $cos ⁡ \left(\right. \theta \left.\right) = 2 cos^{2} ⁡ \left(\right. \theta / 2 \left.\right) - 1$ produces the half-angle formula for the cosine.

## Parametric formulas

The parametric formulas express the trigonometric functions of an angle $\theta$ in terms of the single auxiliary variable:

$$t = tan ⁡ \left(\right. \frac{\theta}{2} \left.\right)$$

Using this substitution, sine and cosine take the rational form:

$$& sin ⁡ \left(\right. \theta \left.\right) = \frac{2 t}{1 + t^{2}} \\ & cos ⁡ \left(\right. \theta \left.\right) = \frac{1 - t^{2}}{1 + t^{2}}$$

The corresponding expressions for tangent and cotangent are:

$$& tan ⁡ \left(\right. \theta \left.\right) = \frac{2 t}{1 - t^{2}} \\ & cot ⁡ \left(\right. \theta \left.\right) = \frac{1 - t^{2}}{2 t}$$

The substitution is valid whenever $\theta \neq \pi + 2 k \pi$ with $k \in \mathbb{Z}$, since at those values the tangent of the half-angle is undefined. The practical importance of the parametric formulas lies in their ability to reduce a trigonometric expression to a rational function of a single algebraic variable, a property widely exploited in the integration of rational functions of sine and cosine through the Weierstrass substitution.

## Werner’s formulas

Werner’s formulas transform the product of two trigonometric functions into a sum or difference of trigonometric functions. The three identities are:

$$& sin ⁡ \left(\right. \alpha \left.\right) sin ⁡ \left(\right. \beta \left.\right) = \frac{1}{2} \left[\right. cos ⁡ \left(\right. \alpha - \beta \left.\right) - cos ⁡ \left(\right. \alpha + \beta \left.\right) \left]\right. \\ & cos ⁡ \left(\right. \alpha \left.\right) cos ⁡ \left(\right. \beta \left.\right) = \frac{1}{2} \left[\right. cos ⁡ \left(\right. \alpha + \beta \left.\right) + cos ⁡ \left(\right. \alpha - \beta \left.\right) \left]\right. \\ & sin ⁡ \left(\right. \alpha \left.\right) cos ⁡ \left(\right. \beta \left.\right) = \frac{1}{2} \left[\right. sin ⁡ \left(\right. \alpha + \beta \left.\right) + sin ⁡ \left(\right. \alpha - \beta \left.\right) \left]\right.$$

Each identity follows by adding or subtracting the appropriate pair of sum and difference formulas. For example, adding the expansions of $cos ⁡ \left(\right. \alpha - \beta \left.\right)$ and $cos ⁡ \left(\right. \alpha + \beta \left.\right)$ cancels the sine terms and leaves twice the product $cos ⁡ \left(\right. \alpha \left.\right) cos ⁡ \left(\right. \beta \left.\right)$, from which the second identity is immediate. These formulas are particularly useful in the integration of products of trigonometric functions and in the analysis of the interference of waves in physics, where the product of two sinusoidal signals is naturally decomposed into components at the sum and difference frequencies.

## Prosthaphaeresis formulas

The prosthaphaeresis formulas perform the transformation opposite to Werner’s: they rewrite a sum or difference of sines or cosines as a product of trigonometric functions. The four identities are:

$$& sin ⁡ \left(\right. p \left.\right) + sin ⁡ \left(\right. q \left.\right) = 2 sin ⁡ \left(\right. \frac{p + q}{2} \left.\right) cos ⁡ \left(\right. \frac{p - q}{2} \left.\right) \\ & sin ⁡ \left(\right. p \left.\right) - sin ⁡ \left(\right. q \left.\right) = 2 cos ⁡ \left(\right. \frac{p + q}{2} \left.\right) sin ⁡ \left(\right. \frac{p - q}{2} \left.\right) \\ & cos ⁡ \left(\right. p \left.\right) + cos ⁡ \left(\right. q \left.\right) = 2 cos ⁡ \left(\right. \frac{p + q}{2} \left.\right) cos ⁡ \left(\right. \frac{p - q}{2} \left.\right) \\ & cos ⁡ \left(\right. p \left.\right) - cos ⁡ \left(\right. q \left.\right) = - 2 sin ⁡ \left(\right. \frac{p + q}{2} \left.\right) sin ⁡ \left(\right. \frac{p - q}{2} \left.\right)$$

These identities are derived from Werner’s formulas by the substitution:

$$\alpha = \frac{p + q}{2} , \beta = \frac{p - q}{2}$$

so that $p = \alpha + \beta$ and $q = \alpha - \beta$. Replacing these values in Werner’s identities and multiplying both sides by two yields the prosthaphaeresis formulas. Their name derives from the Greek words for addition and subtraction, and reflects the historical role they played in pre-logarithmic astronomy, where they were used to convert multiplications into additions and thus simplify numerical computation.

integration toolssum to productprosthaphaeresisproduct to sumwerner formulasangle reductionparametric substitutionhalf angledouble angledifference formulassum formulasreflectionsreference anglesalgebraic rewritingdomain conditionsfunction relationsquotient identitiespythagorean identityunit circlereformulationstransformationsfoundations
