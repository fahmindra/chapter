---
layout: chapter
title: "The Law of Cosines"
chapter: "Trigonometry"
chapter_order: 5
section_order: 15
permalink: /materi-algebrica/trigonometry/the-law-of-cosines/
---

## Definition

The law of cosines relates the sides of any triangle through the angle opposite to one of them. It can be viewed as a generalisation of the [Pythagorean theorem](https://algebrica.org/pythagorean-theorem/), valid not only for right triangles but for every triangle: the square of a side equals the sum of the squares of the other two sides, minus a corrective term that accounts for how open the angle between them is. For a triangle with sides $a , b , c$ and angle $\theta$ opposite to side $c$, the law states:

$$c^{2} = a^{2} + b^{2} - 2 a b cos ⁡ \left(\right. \theta \left.\right)$$

When $\theta = 90^{\circ}$ the [cosine](https://algebrica.org/sine-and-cosine) term vanishes and the formula reduces exactly to the Pythagorean theorem, which confirms that the law of cosines is a strict generalisation of that result. For any other angle, the corrective term either subtracts from or adds to the sum $a^{2} + b^{2}$, depending on whether $\theta$ is acute or obtuse.

![Law of cosine.](https://algebrica.org/wp-content/uploads/resources/images/law-of-cosine-1.png "Law of cosine.")

To derive the formula, drop the altitude $h$ from the vertex opposite to $c$ to the side $b$. This divides $b$ into two segments: $m = a cos ⁡ \left(\right. \theta \left.\right)$ and $n = b - a cos ⁡ \left(\right. \theta \left.\right)$, while the altitude itself satisfies $h = a sin ⁡ \left(\right. \theta \left.\right)$. Applying the Pythagorean theorem to the right triangle formed by $n$, $h$ and $c$ gives:

$$c^{2} & = n^{2} + h^{2} \\ & = \left(\right. b - a cos ⁡ \left(\right. \theta \left.\right) \left.\right)^{2} + \left(\right. a sin ⁡ \left(\right. \theta \left.\right) \left.\right)^{2} \\ & = b^{2} - 2 a b cos ⁡ \left(\right. \theta \left.\right) + a^{2} cos^{2} ⁡ \left(\right. \theta \left.\right) + a^{2} sin^{2} ⁡ \left(\right. \theta \left.\right) \\ & = b^{2} - 2 a b cos ⁡ \left(\right. \theta \left.\right) + a^{2} \left(\right. cos^{2} ⁡ \left(\right. \theta \left.\right) + sin^{2} ⁡ \left(\right. \theta \left.\right) \left.\right)$$

Since the [Pythagorean identity](https://algebrica.org/pythagorean-identity/) gives $sin^{2} ⁡ \left(\right. \theta \left.\right) + cos^{2} ⁡ \left(\right. \theta \left.\right) = 1$, the expression simplifies to:

$$c^{2} = a^{2} + b^{2} - 2 a b cos ⁡ \left(\right. \theta \left.\right)$$

> The law of cosines is often used in conjunction with the [law of sines](https://algebrica.org/law-of-sines/), which provides a complementary approach to solving triangles when different combinations of sides and angles are known.

## Example 1

Consider a triangle with sides $a = 8$, $b = 6$ and included angle $\theta = 60^{\circ}$. The goal is to determine the length of the third side $c$. Substituting the known values into the law of cosines gives:

$$c^{2} & = a^{2} + b^{2} - 2 a b cos ⁡ \left(\right. \theta \left.\right) \\ & = 64 + 36 - 2 \left(\right. 8 \left.\right) \left(\right. 6 \left.\right) cos ⁡ \left(\right. 60^{\circ} \left.\right) \\ & = 64 + 36 - 96 \cdot \frac{1}{2} \\ & = 100 - 48 \\ & = 52$$

Taking the positive square root, one obtains $c = \sqrt{52} = 2 \sqrt{13} \approx 7.21$.

The length of the third side is approximately $7.21$ units.

## Example 2

Consider a triangle with sides $a = 5$, $b = 7$ and $c = 9$. The goal is to determine the angle $\theta$ opposite to side $c$. Solving the law of cosines for $cos ⁡ \left(\right. \theta \left.\right)$ gives:

$$cos ⁡ \left(\right. \theta \left.\right) = \frac{a^{2} + b^{2} - c^{2}}{2 a b}$$

Substituting the known values:

$$cos ⁡ \left(\right. \theta \left.\right) & = \frac{25 + 49 - 81}{2 \left(\right. 5 \left.\right) \left(\right. 7 \left.\right)} \\ & = \frac{- 7}{70} \\ & = - 0.1$$

Since $cos ⁡ \left(\right. \theta \left.\right) < 0$, the angle $\theta$ is obtuse. Taking the inverse cosine yields:

$$\theta = arccos ⁡ \left(\right. - 0.1 \left.\right) \approx 95.7^{\circ}$$

The angle opposite to the longest side is approximately $95.7^{\circ}$.

## Vector interpretation

The law of cosines admits a reading in terms of vectors that exposes its deeper structure and connects it to the inner product. Consider a triangle with vertex $O$, and let $\overset{\rightarrow}{u}$ and $\overset{\rightarrow}{v}$ denote the two sides of length $a$ and $b$ issuing from $O$, so that $a = \left|\right. \overset{\rightarrow}{u} \left|\right.$ and $b = \left|\right. \overset{\rightarrow}{v} \left|\right.$. The third side of the triangle, of length $c$, is then represented by the vector $\overset{\rightarrow}{v} - \overset{\rightarrow}{u}$, which joins the endpoints of $\overset{\rightarrow}{u}$ and $\overset{\rightarrow}{v}$. Expanding the squared norm of this vector through the bilinearity of the inner product gives:

$$\left|\right. \overset{\rightarrow}{v} - \overset{\rightarrow}{u} \left|\right.^{2} & = \left(\right. \overset{\rightarrow}{v} - \overset{\rightarrow}{u} \left.\right) \cdot \left(\right. \overset{\rightarrow}{v} - \overset{\rightarrow}{u} \left.\right) \\ & = \left|\right. \overset{\rightarrow}{v} \left|\right.^{2} - 2 \overset{\rightarrow}{u} \cdot \overset{\rightarrow}{v} + \left|\right. \overset{\rightarrow}{u} \left|\right.^{2}$$

The geometric definition of the inner product states that:

$$\overset{\rightarrow}{u} \cdot \overset{\rightarrow}{v} = \left|\right. \overset{\rightarrow}{u} \left|\right. \left|\right. \overset{\rightarrow}{v} \left|\right. cos ⁡ \theta$$

$\theta$ is the angle between the two vectors at $O$, which coincides with the angle between the sides $a$ and $b$ of the triangle. Substituting this identity into the expansion above gives:

$$c^{2} = a^{2} + b^{2} - 2 a b cos ⁡ \theta$$

From this point of view the law of cosines is a reformulation of the identity that defines the inner product in terms of lengths and angles. The corrective term $- 2 a b cos ⁡ \theta$ that distinguishes a generic triangle from a right one is nothing other than $- 2 \overset{\rightarrow}{u} \cdot \overset{\rightarrow}{v}$, and the Pythagorean case corresponds to the situation in which the two vectors are orthogonal, so that $\overset{\rightarrow}{u} \cdot \overset{\rightarrow}{v} = 0$.

law of sinesinverse cosineangle computationside computationsolving trianglesalgebraic expansiontrigonometric componentspythagorean theoremright triangleprojectionpythagorean extensionangle oppositecosine termside relationstatementapplicationsderivationstructure
