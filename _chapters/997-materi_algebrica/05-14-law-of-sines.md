---
layout: chapter
title: "The Law of Sines"
chapter: "Trigonometry"
chapter_order: 5
section_order: 14
permalink: /materi-algebrica/trigonometry/the-law-of-sines/
---

## Definition

The law of sines states that in any triangle, the ratio between the length of a side and the [sine](https://algebrica.org/sine-and-cosine/) of its opposite angle is the same for all three sides. For a triangle with sides $a , b , c$ opposite to angles $\alpha , \beta , \gamma$ respectively, this common ratio equals twice the radius $r$ of the circumscribed circle:

$$\frac{a}{sin ⁡ \alpha} = \frac{b}{sin ⁡ \beta} = \frac{c}{sin ⁡ \gamma} = 2 r$$

The quantity $2 r$ is the diameter of the circumcircle, that is, the unique circle passing through all three vertices of the triangle.

![](https://algebrica.org/wp-content/uploads/resources/images/law-of-sines-3.png)

The law of sines is particularly useful when some sides or angles of a triangle are known and the remaining ones must be determined, since each unknown can be recovered through a simple proportion.

---

To establish the equality of the three ratios, consider the altitude $h$ drawn from the vertex opposite to side $c$ to the side $c$ itself. By the definition of the [sine](https://algebrica.org/sine-and-cosine/) function applied to angles $\alpha$ and $\beta$, one has $sin ⁡ \left(\right. \alpha \left.\right) = h / b$ and $sin ⁡ \left(\right. \beta \left.\right) = h / a$, from which $b sin ⁡ \left(\right. \alpha \left.\right) = h = a sin ⁡ \left(\right. \beta \left.\right)$. Dividing both sides by $sin ⁡ \left(\right. \alpha \left.\right) sin ⁡ \left(\right. \beta \left.\right)$ yields:

$$\frac{a}{sin ⁡ \left(\right. \alpha \left.\right)} = \frac{b}{sin ⁡ \left(\right. \beta \left.\right)}$$

An identical argument applied to the altitude from the vertex opposite to side $a$ gives $sin ⁡ \left(\right. \beta \left.\right) = h^{'} / c$ and $sin ⁡ \left(\right. \gamma \left.\right) = h^{'} / b$, and therefore:

$$\frac{b}{sin ⁡ \left(\right. \beta \left.\right)} = \frac{c}{sin ⁡ \left(\right. \gamma \left.\right)}$$

Since the first ratio equals the second and the second equals the third, all three are equal.

To see why the common value is $2 r$, note that when the triangle is inscribed in its circumcircle of radius $r$, the inscribed angle theorem implies that the chord of length $a$ subtends a central angle of $2 \alpha$. The relationship between a chord and the radius of the circle then gives $a = 2 r sin ⁡ \left(\right. \alpha \left.\right)$, from which $a / sin ⁡ \left(\right. \alpha \left.\right) = 2 r$. The same holds for the other two sides by symmetry.

> The law of sines is often used in conjunction with the [law of cosines](https://algebrica.org/law-of-cosines/), which provides a complementary approach to solving triangles when different combinations of sides and angles are known.

## Example 1

Consider a triangle in which $\alpha = 40^{\circ}$, $\beta = 65^{\circ}$ and $a = 10$. The goal is to determine the length of side $b$, which lies opposite to $\beta .$ Since the interior angles of any triangle sum to $180^{\circ}$, the third angle is $\gamma = 180^{\circ} - 40^{\circ} - 65^{\circ} = 75^{\circ}$. Applying the law of sines to the pair involving $a$ and $b$ gives:

$$\frac{10}{sin ⁡ 40^{\circ}} = \frac{b}{sin ⁡ 65^{\circ}}$$

Multiplying both sides by $sin ⁡ 65^{\circ}$ isolates $b$:

$$b = \frac{10 \cdot sin ⁡ 65^{\circ}}{sin ⁡ 40^{\circ}} = \frac{10 \cdot 0.9063}{0.6428} \approx 14.1$$

The length of side $b$ is approximately $14.1$ units.

## The ambiguous case

In the Side-Side-Angle (SSA) configuration, where two sides $a$ and $b$ and an angle $\alpha$ opposite to one of them are given, the law of sines does not necessarily determine a unique triangle. Isolating $sin ⁡ \left(\right. \beta \left.\right)$ from the proportion yields:

$$sin ⁡ \left(\right. \beta \left.\right) = \frac{b sin ⁡ \left(\right. \alpha \left.\right)}{a}$$

Since the sine function satisfies $sin ⁡ \left(\right. \theta \left.\right) = sin ⁡ \left(\right. 180^{\circ} - \theta \left.\right)$ for every $\theta \in \left(\right. 0^{\circ} , 180^{\circ} \left.\right)$, this value may correspond to two distinct angles, $\beta$ and $180^{\circ} - \beta$. Whether neither, one, or both of these yield a valid triangle depends on the relative magnitudes of $a$, $b$, and the altitude from the vertex opposite to $c$. Each candidate value of $\beta$ must therefore be examined individually to verify that the resulting angles sum to less than $180^{\circ}$ and that all sides are positive.

## Example 2

Consider a triangle in which $\alpha = 35^{\circ}$, $a = 7$ and $b = 10$. The goal is to determine all possible values of angle $\beta$ and, for each, the corresponding triangle. Applying the law of sines to isolate $sin ⁡ \left(\right. \beta \left.\right)$ gives:

$$sin ⁡ \left(\right. \beta \left.\right) & = \frac{b sin ⁡ \left(\right. \alpha \left.\right)}{a} \\ & = \frac{10 \cdot sin ⁡ 35^{\circ}}{7} \\ & = \frac{10 \cdot 0.5736}{7} \\ & \approx 0.8194$$

Since $0 < 0.8194 < 1$, the equation $sin ⁡ \left(\right. \beta \left.\right) = 0.8194$ admits two solutions in $\left(\right. 0^{\circ} , 180^{\circ} \left.\right)$:

$$\beta_{1} & = arcsin ⁡ \left(\right. 0.8194 \left.\right) \approx 55.0^{\circ} \\ \beta_{2} & = 180^{\circ} - 55.0^{\circ} = 125.0^{\circ}$$

Each value must be checked against the constraint that all three angles sum to $180^{\circ}$. For $\beta_{1} = 55.0^{\circ}$, the third angle is:
$$\gamma_{1} = 180^{\circ} - 35^{\circ} - 55^{\circ} = 90^{\circ}$$

This angle is positive, so the first triangle is valid. For $\beta_{2} = 125.0^{\circ}$, the third angle is:
$$\gamma_{2} = 180^{\circ} - 35^{\circ} - 125^{\circ} = 20^{\circ}$$

This case is also positive, so the second triangle is valid as well. The two triangles are non-congruent: the first has angles $35^{\circ} , 55^{\circ} , 90^{\circ}$ and the second has angles $35^{\circ} , 125^{\circ} , 20^{\circ}$.

Both are consistent with the given data $\alpha = 35^{\circ}$, $a = 7$, $b = 10$, confirming that two distinct triangles can satisfy the same initial conditions.

## A geometric criterion for the ambiguous case

The algebraic analysis of the ambiguous case can be complemented by a geometric criterion that allows the number of valid triangles to be determined before performing any computation. Given the angle $\alpha$ and the two sides $a$ and $b$, the quantity $b sin ⁡ \left(\right. \alpha \left.\right)$ coincides with the altitude of the triangle measured from the vertex opposite to side $c$. Comparing this altitude with the length of $a$ is sufficient to predict how many triangles are compatible with the given data.

Four situations arise depending on the relative size of $a$ with respect to $b sin ⁡ \left(\right. \alpha \left.\right)$ and $b$.

- When $a < b sin ⁡ \left(\right. \alpha \left.\right)$, the side $a$ is too short to reach the base from the vertex of $\alpha$, and no triangle exists.
- When $a = b sin ⁡ \left(\right. \alpha \left.\right)$, the side $a$ coincides with the altitude itself, producing exactly one right triangle with the right angle at the vertex opposite to $c$.
- When $b sin ⁡ \left(\right. \alpha \left.\right) < a < b$, the side $a$ reaches the base in two distinct points, and two non-congruent triangles satisfy the given data.
- When $a \geq b$, only one of the two possible positions yields a geometrically consistent triangle, and the configuration is again uniquely determined.

> The expression $b sin ⁡ \left(\right. \alpha \left.\right)$ should be read as the altitude from the vertex of angle $\alpha$ to the line containing side $c$. This interpretation makes the criterion easy to recall, since the question reduces to whether $a$ falls short of this altitude, equals it, lies between it and $b$, or exceeds $b$.

---

The criterion is consistent with the second example discussed above. With $\alpha = 35^{\circ}$ and $b = 10$, the altitude is:

$$b sin ⁡ \left(\right. \alpha \left.\right) = 10 \cdot sin ⁡ 35^{\circ} \approx 5.74$$

Since $a = 7$ satisfies $5.74 < 7 < 10$, the configuration falls in the range where two triangles coexist, which is precisely the outcome obtained from the algebraic analysis.

law of cosinesnumerical examplemultiple solutionsambiguous caseproportionssolving triangleschord relationinscribed anglesymmetryright triangle relationscircumcircleside-angle relationtriangle anglessine functionratiosapplicationsderivationstructure
