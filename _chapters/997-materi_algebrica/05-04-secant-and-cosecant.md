---
layout: chapter
title: "Secant and Cosecant"
chapter: "Trigonometry"
chapter_order: 5
section_order: 4
permalink: /materi-algebrica/trigonometry/secant-and-cosecant/
---

## Secant

Consider the [unit circle](https://algebrica.org/unit-circle/) centered at the origin $\text{O} = \left(\right. 0 , 0 \left.\right)$ with radius $1$. Let $\theta$ be an angle in standard position, and denote by $\text{P}$ the point on the circle where the terminal side of $\theta$ intersects it. Draw the tangent line to the circle at the point $\text{P}$, and let $\text{S}$ be the point where this tangent line meets the $x$-axis. The secant of the angle $\theta$ is defined as the signed length of the segment $\overset{―}{O S}$, that is, the abscissa $x_{S}$ of the point $\text{S}$:

$$sec ⁡ \left(\right. \theta \left.\right) = \overset{―}{O S} = x_{S}$$

To express this length in terms of familiar trigonometric quantities, consider the right triangle formed by $\text{O}$, $\text{P}$, and the foot of the perpendicular from $\text{P}$ to the $x$-axis. Since $\text{OP} = 1$ and the horizontal component of $\text{P}$ is $cos ⁡ \left(\right. \theta \left.\right)$, while the tangent at $\text{P}$ is perpendicular to the radius $\overset{―}{O P}$, one can establish by similar triangles that:

$$sec ⁡ \left(\right. \theta \left.\right) = \frac{1}{cos ⁡ \left(\right. \theta \left.\right)}$$

![Secant.](https://algebrica.org/wp-content/uploads/resources/images/secant-2.png "Secant.")

Since the secant is the reciprocal of the [cosine](https://algebrica.org/sine-and-cosine/), it is defined only at angles where the cosine does not vanish. The cosine equals zero at all odd multiples of $\pi / 2$, so the domain of the secant excludes precisely those values:

$$sec ⁡ \left(\right. \theta \left.\right) = \frac{1}{cos ⁡ \left(\right. \theta \left.\right)} \forall \theta \neq \frac{\pi}{2} + k \pi , k \in \mathbb{Z}$$

From the geometric construction, the secant measures the factor by which the unit radius must be extended to reach the point $\text{S}$ where the tangent line at $\text{P}$ meets the $x$-axis. This interpretation makes it evident why $\left|\right. sec ⁡ \left(\right. \theta \left.\right) \left|\right. \geq 1$ wherever the function is defined: the intersection point $\text{S}$ necessarily lies at a distance from the origin no smaller than the radius of the unit circle itself.

> This section examines the secant from a geometric point of view. For the analytical properties of the function, including domain, symmetry, limits, derivatives, and integrals, see the dedicated entry on the [secant function](https://algebrica.org/secant-function/).

## Common values of the secant

Below are some commonly known values of $sec ⁡ \left(\right. \theta \left.\right)$ for selected angles, useful in various applications of trigonometry:

$$\theta & = 0^{\circ} = 0 \text{rad} & & sec ⁡ \left(\right. \theta \left.\right) = 1 \\ \theta & = 30^{\circ} = \pi / 6 \text{rad} & & sec ⁡ \left(\right. \theta \left.\right) = \frac{2 \sqrt{3}}{3} \\ \theta & = 45^{\circ} = \pi / 4 \text{rad} & & sec ⁡ \left(\right. \theta \left.\right) = \sqrt{2} \\ \theta & = 60^{\circ} = \pi / 3 \text{rad} & & sec ⁡ \left(\right. \theta \left.\right) = 2 \\ \theta & = 90^{\circ} = \pi / 2 \text{rad} & & sec ⁡ \left(\right. \theta \left.\right) \text{is undefined}$$

## Trigonometric identities for the secant

- $$\text{1}. sec ⁡ x = \frac{1}{cos ⁡ x}$$
- $$\text{2}. 1 + tan^{2} ⁡ x = sec^{2} ⁡ x$$
- $$\text{3}. sec ⁡ \left(\right. - x \left.\right) = sec ⁡ x$$
- $$\text{4}. sec ⁡ x tan ⁡ x = \frac{sin ⁡ x}{cos^{2} ⁡ x}$$
- $$\text{5}. sec^{2} ⁡ x - tan^{2} ⁡ x = 1$$

> These formulas collect the most useful identities involving the secant, including the reciprocal definition, the Pythagorean identity, the symmetry relation, and common algebraic transformations. For a broader overview, refer to the full collection of [trigonometric identities](https://algebrica.org/trigonometric-identities/).

## Cosecant

Consider again the same construction: the tangent line drawn at $\text{P}$ to the unit circle meets the $y$-axis at a point $\text{Q}$. The cosecant of the angle $\theta$ is defined as the signed length of the segment $\overset{―}{O Q}$, that is, the ordinate $y_{Q}$ of the point $\text{Q}$:

$$csc ⁡ \left(\right. \theta \left.\right) = \overset{―}{O Q} = y_{Q}$$

By an argument analogous to that given for the secant, applying similar triangles to the configuration yields the following expression in terms of the sine:

$$csc ⁡ \left(\right. \theta \left.\right) = \frac{1}{sin ⁡ \left(\right. \theta \left.\right)}$$

![Cosecant.](https://algebrica.org/wp-content/uploads/resources/images/cosecant-2.png "Cosecant.")

Since the cosecant is the reciprocal of the [sine](https://algebrica.org/sine-and-cosine/), it is defined only at angles where the sine does not vanish. The sine equals zero at all integer multiples of $\pi$, so the domain of the cosecant excludes precisely those values:

$$csc ⁡ \left(\right. \theta \left.\right) = \frac{1}{sin ⁡ \left(\right. \theta \left.\right)} \forall \theta \neq k \pi , k \in \mathbb{Z}$$

Analogous to the secant, the cosecant measures the factor by which the unit radius must be extended to reach the point $\text{Q}$ where the tangent line at $\text{P}$ meets the $y$-axis. This interpretation makes it evident why $\left|\right. csc ⁡ \left(\right. \theta \left.\right) \left|\right. \geq 1$ wherever the function is defined: the intersection point $\text{Q}$ necessarily lies at a distance from the origin no smaller than the radius of the unit circle itself.

> This section examines the cosecant from a geometric point of view. For the analytical properties of the function, including domain, symmetry, limits, derivatives, and integrals, see the dedicated entry on the [cosecant function](https://algebrica.org/cosecant-function/).

## Geometric interpretation

Both definitions stem from a single geometric object: the [tangent](https://algebrica.org/tangent-and-cotangent/) line drawn at $\text{P}$ simultaneously determines the point $\text{S}$ on the $x$-axis and the point $\text{Q}$ on the $y$-axis, yielding the secant and the cosecant from one construction.

This also makes transparent the asymmetric behaviour of the two functions. When the terminal side of $\theta$ approaches a horizontal position, the tangent line at $\text{P}$ becomes nearly parallel to the $x$-axis, driving $\text{S}$ to infinity and making the secant unbounded, while $\text{Q}$ remains well-defined. The situation is reversed when the terminal side approaches a vertical position.

## Common values of the cosecant

Below are some commonly known values of $csc ⁡ \left(\right. \theta \left.\right)$ for selected angles, useful in various applications of trigonometry:

$$\theta & = 0^{\circ} = 0 \text{rad} & & csc ⁡ \left(\right. \theta \left.\right) \text{is undefined} \\ \theta & = 30^{\circ} = \pi / 6 \text{rad} & & csc ⁡ \left(\right. \theta \left.\right) = 2 \\ \theta & = 45^{\circ} = \pi / 4 \text{rad} & & csc ⁡ \left(\right. \theta \left.\right) = \sqrt{2} \\ \theta & = 60^{\circ} = \pi / 3 \text{rad} & & csc ⁡ \left(\right. \theta \left.\right) = \frac{2 \sqrt{3}}{3} \\ \theta & = 90^{\circ} = \pi / 2 \text{rad} & & csc ⁡ \left(\right. \theta \left.\right) = 1$$

## Secant and cosecant functions

The [secant function](https://algebrica.org/secant-function/) $f \left(\right. x \left.\right) = sec ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, measured in radians, the value $1 / cos ⁡ \left(\right. x \left.\right)$. Its graph is a periodic curve with period $2 \pi$ and features vertical [asymptotes](https://algebrica.org/asymptotes/) at the points where the cosine vanishes, that is, at $x = \pi / 2 + k \pi$ for $k \in \mathbb{Z}$. The [domain](https://algebrica.org/determining-the-domain-of-a-function/) of $sec ⁡ \left(\right. x \left.\right)$ consists of all real numbers except those points, while its range is $\left(\right. - \infty , - 1 \left]\right. \cup \left[\right. 1 , + \infty \left.\right)$.

![Secant function.](https://algebrica.org/wp-content/uploads/resources/images/secant-function-2.png "Secant function.")

- Domain: $x \in \mathbb{R} : cos ⁡ \left(\right. x \left.\right) \neq 0 = x \in \mathbb{R} : x \neq \pi / 2 + k \pi \text{for all} k \in \mathbb{Z}$
- Range: $y \in \left(\right. - \infty , - 1 \left]\right. \cup \left[\right. 1 , \infty \left.\right)$
- Periodicity: periodic in $x$ with period $2 \pi$
- Parity: [even](https://algebrica.org/even-and-odd-functions/), $sec ⁡ \left(\right. - x \left.\right) = sec ⁡ \left(\right. x \left.\right)$

---

The [cosecant function](https://algebrica.org/cosecant-function/) $f \left(\right. x \left.\right) = csc ⁡ \left(\right. x \left.\right)$ assigns to each angle $x$, measured in radians, the value $1 / sin ⁡ \left(\right. x \left.\right)$. Its graph is a periodic curve with period $2 \pi$ and features vertical asymptotes at the points where the sine vanishes, that is, at $x = k \pi$ for $k \in \mathbb{Z}$. The [domain](https://algebrica.org/determining-the-domain-of-a-function/) of $csc ⁡ \left(\right. x \left.\right)$ consists of all real numbers except those points, while its range is $\left(\right. - \infty , - 1 \left]\right. \cup \left[\right. 1 , + \infty \left.\right)$.

![Cosecant function.](https://algebrica.org/wp-content/uploads/resources/images/cosecant-function.png "Cosecant function.")

- Domain: $x \in \mathbb{R} : sin ⁡ \left(\right. x \left.\right) \neq 0 = x \in \mathbb{R} : x \neq k \pi \text{for all} k \in \mathbb{Z}$
- Range: $y \in \left(\right. - \infty , - 1 \left]\right. \cup \left[\right. 1 , \infty \left.\right)$
- Periodicity: periodic in $x$ with period $2 \pi$
- Parity: [odd](https://algebrica.org/even-and-odd-functions/), $csc ⁡ \left(\right. - x \left.\right) = - csc ⁡ \left(\right. x \left.\right)$

## Trigonometric identities for the cosecant

- $$\text{1}. csc ⁡ x = \frac{1}{sin ⁡ x}$$
- $$\text{2}. 1 + cot^{2} ⁡ x = csc^{2} ⁡ x$$
- $$\text{3}. csc ⁡ \left(\right. - x \left.\right) = - csc ⁡ x$$
- $$\text{4}. csc ⁡ x cot ⁡ x = \frac{cos ⁡ x}{sin^{2} ⁡ x}$$
- $$\text{5}. csc^{2} ⁡ x - cot^{2} ⁡ x = 1$$

> These formulas collect the most useful identities involving the cosecant, including the reciprocal definition, the Pythagorean identity, the symmetry relation, and common algebraic transformations. For a broader overview, refer to the full collection of [trigonometric identities](https://algebrica.org/trigonometric-identities/).

rangeparityperiodicityasymptotesfunction graphstrigonometric identitiesintersection pointssegment interpretationsimilar trianglesgeometric constructiontangent lineunit circleundefined valuesdomain restrictionsreciprocal of sinereciprocal of cosinecosecantsecantpropertiesgeometrydefinitions
