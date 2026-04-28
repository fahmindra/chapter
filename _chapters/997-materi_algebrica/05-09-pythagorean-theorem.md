---
layout: chapter
title: "Pythagorean Theorem"
chapter: "Trigonometry"
chapter_order: 5
section_order: 9
permalink: /materi-algebrica/trigonometry/pythagorean-theorem/
---

## Statement

The Pythagorean theorem states that in every right triangle, the square of the hypotenuse is equal to the sum of the squares of the two legs:

$$a^{2} + b^{2} = c^{2}$$

In this relation $c$ denotes the hypotenuse, while $a$ and $b$ denote the two legs. The theorem applies exclusively to right triangles, that is, triangles containing exactly one angle of $90^{\circ}$.

![](https://algebrica.org/wp-content/uploads/resources/images/pythagorean-theorem-6.png)

From the identity $a^{2} + b^{2} = c^{2}$ one can isolate each side in turn, obtaining the hypotenuse as a function of the two legs and each leg as a function of the hypotenuse and the other leg:

$$c & = \sqrt{a^{2} + b^{2}} \\ a & = \sqrt{c^{2} - b^{2}} \\ b & = \sqrt{c^{2} - a^{2}}$$

The square roots are taken with the positive sign because $a$, $b$ and $c$ represent lengths.The converse of the theorem also holds. If in a triangle with sides $a$, $b$ and $c$ the relation

$$a^{2} + b^{2} = c^{2}$$

is satisfied, then the triangle is right-angled, and the right angle is the one opposite the side $c$.

## Applications

The Pythagorean theorem can be applied whenever a figure admits a decomposition that isolates a right triangle. This makes it possible to determine the length of sides, diagonals or other segments belonging to the original figure. A first illustration is provided by the square shown below:

![](https://algebrica.org/wp-content/uploads/resources/images/pythagorean-theorem-2-3.png)

Drawing the diagonal $\overset{―}{D B}$ partitions the square into two congruent right triangles, each having the diagonal as hypotenuse and two sides of the square as legs. The Pythagorean theorem applied to either of them gives:

$$\left(\overset{―}{D B}\right)^{2} & = \left(\overset{―}{A B}\right)^{2} + \left(\overset{―}{A D}\right)^{2} \\ \overset{―}{D B} & = \sqrt{\left(\overset{―}{A B}\right)^{2} + \left(\overset{―}{A D}\right)^{2}}$$

The same principle extends to isosceles and equilateral triangles, which can be split into two right triangles by drawing the height from the apex to the base.

![](https://algebrica.org/wp-content/uploads/resources/images/pythagorean-theorem-3-1.png)

Denoting by $H$ the foot of the height drawn from $C$ to the base $A B$, the right triangle $C H B$ has hypotenuse $\overset{―}{C B}$ and legs $\overset{―}{C H}$ and $\overset{―}{H B}$. Applying the theorem and its inverse forms yields:

$$\overset{―}{C B} & = \sqrt{\left(\overset{―}{C H}\right)^{2} + \left(\overset{―}{H B}\right)^{2}} \\ \overset{―}{C H} & = \sqrt{\left(\overset{―}{C B}\right)^{2} - \left(\overset{―}{H B}\right)^{2}} \\ \overset{―}{H B} & = \sqrt{\left(\overset{―}{C B}\right)^{2} - \left(\overset{―}{C H}\right)^{2}}$$

> The same principle extends to any figure that can be partitioned into right triangles, such as rectangles, rhombi or portions of trapezoids.

## Pythagorean triples

A Pythagorean triple is a set of three positive [integers](https://algebrica.org/integers/) $\left(\right. a , b , c \left.\right)$ satisfying the relation:

$$a^{2} + b^{2} = c^{2}$$

The smallest examples are the following:

$$& \left(\right. 3 , 4 , 5 \left.\right) \\ & \left(\right. 5 , 12 , 13 \left.\right) \\ & \left(\right. 7 , 24 , 25 \left.\right) \\ & \left(\right. 8 , 15 , 17 \left.\right)$$

A Pythagorean triple whose three entries are pairwise coprime is called a primitive triple. Every non-primitive triple is obtained by multiplying a primitive one by a positive integer, so that $\left(\right. 6 , 8 , 10 \left.\right)$ and $\left(\right. 9 , 12 , 15 \left.\right)$ are both non-primitive triples derived from $\left(\right. 3 , 4 , 5 \left.\right)$. All primitive triples are therefore Pythagorean, but the converse does not hold.

## Pythagorean identity on the unit circle

On the [unit circle](https://algebrica.org/unit-circle/), the [sine and cosine](https://algebrica.org/sine-and-cosine/) of an angle $\theta$ admit a direct geometric interpretation. Dropping a perpendicular from the point on the circle identified by $\theta$ to the horizontal axis produces a right triangle whose hypotenuse is the radius, whose horizontal leg has length $cos ⁡ \theta$ and whose vertical leg has length $sin ⁡ \theta$.

![](https://algebrica.org/wp-content/uploads/resources/images/pythagorean-theorem-4-1.png)

Applying the Pythagorean theorem to this triangle, with legs of length $sin ⁡ \theta$ and $cos ⁡ \theta$ and hypotenuse of length $1$, yields the [fundamental trigonometric identity](https://algebrica.org/pythagorean-identity/):

$$sin^{2} ⁡ \theta + cos^{2} ⁡ \theta = 1$$

The identity therefore holds for every real $\theta$ and is simply the Pythagorean theorem expressed in trigonometric form. The [law of cosines](https://algebrica.org/law-of-cosines/) generalises this relation to arbitrary triangles, reducing to the Pythagorean theorem when the angle between the two known sides is right, while the [law of sines](https://algebrica.org/law-of-sines/) expresses a different link between sides and opposite angles and is used to solve triangles in which a side-angle pair is known.

## Modulus of a complex number

A [complex number](https://algebrica.org/complex-numbers-introduction/) can be written in the algebraic form:

$$z = a + b i$$

The real part $a$ and the imaginary part $b$ identify the point of coordinates $\left(\right. a , b \left.\right)$ in the complex plane. The modulus $\left|\right. z \left|\right.$ is defined as the distance from the origin to this point, and since that distance is the hypotenuse of the right triangle with legs $a$ and $b$, the Pythagorean theorem gives:

$$\left|\right. z \left|\right. = \sqrt{a^{2} + b^{2}}$$

The modulus of a complex number is therefore a direct geometric application of the Pythagorean theorem in the Cartesian plane.

![](https://algebrica.org/wp-content/uploads/resources/images/pythagorean-theorem-5-1.png)

This construction holds for every complex number $z = a + b i$. Its modulus is always the distance from the origin to the point $\left(\right. a , b \left.\right)$, computed through the Pythagorean theorem applied to the right triangle with legs $a$ and $b$.

non-euclidean casesvector interpretationhigher dimensionseuclidean normcomplex modulussin² + cos² = 1unit circle identityfigure partitionpythagorean triplesdistance computationgeometric decompositiontriangle heightsquare diagonallength interpretationeuclidean contextconverse theorema² + b² = c²legs and hypotenuseright triangleextensionsapplicationsstatement
