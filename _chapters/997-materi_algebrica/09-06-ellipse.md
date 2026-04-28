---
layout: chapter
title: "Ellipse"
chapter: "Lines, Planes and Conic Sections"
chapter_order: 9
section_order: 6
permalink: /materi-algebrica/lines-planes-and-conic-sections/ellipse/
---

## Introduction to conic sections

When introducing the [parabola](https://algebrica.org/parabola), we saw that when a plane intersects a cone, the resulting shape, when projected onto the plane, can be a [circumference](https://algebrica.org/circumference), a parabola, an ellipse, or a [hyperbola](https://algebrica.org/hyperbola). These curves are collectively referred to as conics. More formally, a conic is a second-degree algebraic curve in the plane. It is defined as the set of points $\left(\right. x , y \left.\right) \in \mathbb{R}^{2}$ that satisfy a general quadratic equation in the variables $x$ and $y$:

$$f \left(\right. x , y \left.\right) = a_{11} x^{2} + 2 a_{12} x y + a_{22} y^{2} + 2 a_{13} x + 2 a_{23} y + a_{33} = 0$$

Here, the coefficients $a_{i j} \in \mathbb{R}$, and to ensure the curve is truly quadratic, we require that both $a_{11}$ and $a_{22}$ are nonzero.

## What is an ellipse

Given two fixed points in the plane, $F_{1}$ and $F_{2}$, an ellipse is defined as the set of all points $P$ in the plane such that the sum of the distances from $P$ to each focus is constant.

$$\overset{―}{P F_{1}} + \overset{―}{P F_{2}} = \text{constant}$$

![](https://algebrica.org/wp-content/uploads/resources/images/ellipse-1.png)

$F_{1}$ and $F_{2}$ are the foci of the ellipse. Assuming that the focus $F_{1}$ has coordinates $\left(\right. - c , 0 \left.\right)$ and the focus $F_{2}$ has coordinates $\left(\right. c , 0 \left.\right)$, the distance between $F_{1}$ and $F_{2}$ is called the focal distance and is equal to $2 c$. The midpoint of the segment $\overset{―}{F_{1} F_{2}}$ is the center of the ellipse.

---

We define the major axis and minor axis of the ellipse, respectively, as the longest and shortest diameters passing through its center. The major axis lies along the direction of maximum extension of the ellipse and passes through both foci. Its total length is $2 a$, where $a$ is the semi-major axis. The minor axis is perpendicular to the major axis and also passes through the center of the ellipse. Its total length is $2 b$, where $b$ is the semi-minor axis.

---

By choosing a point $P = \left(\right. a , 0 \left.\right)$, located at the right endpoint of the major axis, we consider the case where the ellipse intersects the $x$-axis at its farthest horizontal extent. In this configuration, the distance from the left focus $F_{1} = \left(\right. - c , 0 \left.\right)$ to the point $P$ is $\overset{―}{F_{1} P} = a + c$. Similarly, we have $\overset{―}{F_{2} P} = a + c$.

![](https://algebrica.org/wp-content/uploads/resources/images/ellipse-2.png)

From this, we conclude that the constant sum of the distances from any point on the ellipse to the two foci is:

$$\overset{―}{F_{1} P} + \overset{―}{F_{2} P} = \left(\right. a + c \left.\right) + \left(\right. a - c \left.\right) = 2 a$$

In the standard form, an ellipse centered at the origin with horizontal major axis is described by the equation:

$$\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} = 1$$

where $b^{2} = a^{2} - c^{2}$, with $b > 0$ and $a > b$, from which it follows that:

$$c = \sqrt{a^{2} - b^{2}}$$

## Why is the sum of distances to the foci always constant in an ellipse?

Because that’s what defines it. An ellipse is the set of all points for which the sum of the distances to the two foci is exactly $2 a$. Any point not satisfying this condition lies outside or inside the curve.

## Vertices

An ellipse intersects the coordinate axes at four key points, its vertices. The two on the major axis represent the farthest horizontal reach.

![](https://algebrica.org/wp-content/uploads/resources/images/ellipse-3.png)

The two on the minor axis define the vertical extent. All are symmetric with respect to the center and capture the ellipse’s full geometric footprint.

## Eccentricity

The ratio between the focal distance and the length of the major axis of an ellipse is called its eccentricity. It is denoted by $e$ and satisfies the condition:

$$0 \leq e < 1$$

![](https://algebrica.org/wp-content/uploads/resources/images/ellipse-4.png)

The closer $e$ is to 0, the more circular the ellipse appears. As $e$ approaches 1, the ellipse becomes increasingly elongated. The value of the eccentricity $e$ is given by:

$$e = \frac{c}{a} = \frac{\sqrt{a^{2} - b^{2}}}{a}$$

##### Eccentricity describes how “stretched” an ellipse is. When $e = 0$, the ellipse is indistinguishable from a circle and its foci coincide at the center. As $e$ increases, the foci move apart and the shape elongates along the major axis. What matters is not the size, but the ratio: eccentricity is a pure measure of shape.

## Example

Let us determine the equation of the ellipse with foci $F_{1} = \left(\right. 1 , 0 \left.\right)$ and $F_{2} = \left(\right. - 1 , 0 \left.\right)$, such that the sum of the distances from any point on the ellipse to the two foci is equal to 6.

---

A point $P \left(\right. x , y \left.\right)$ belongs to the ellipse if it satisfies the condition:

$$\sqrt{\left(\right. x - 1 \left.\right)^{2} + y^{2}} + \sqrt{\left(\right. x + 1 \left.\right)^{2} + y^{2}} = 6$$

Each square root represents the Euclidean distance between $P \left(\right. x , y \left.\right)$ and one of the two foci. This equation expresses the geometric definition of the ellipse: the set of all points in the plane such that the sum of their distances to the two foci is constant. Hence, determining the equation of the ellipse simply requires performing the necessary calculations. We have:

$$& \left(\right. x - 1 \left.\right)^{2} + y^{2} = 36 + \left(\right. x + 1 \left.\right)^{2} + y^{2} - 12 \sqrt{\left(\right. x + 1 \left.\right)^{2} + y^{2}} \\ & x^{2} - 2 x + 1 + y^{2} = 36 + x^{2} + 2 x + 1 + y^{2} - 12 \sqrt{\left(\right. x + 1 \left.\right)^{2} + y^{2}} \\ & - 4 x - 36 = - 12 \sqrt{\left(\right. x + 1 \left.\right)^{2} + y^{2}} \\ & x + 9 = 3 \sqrt{\left(\right. x + 1 \left.\right)^{2} + y^{2}}$$

---

By squaring both sides of the equation, we obtain:

$$& \left(\right. x + 9 \left.\right)^{2} = \left(\right. 3 \sqrt{\left(\right. x + 1 \left.\right)^{2} + y^{2}} \left.\right)^{2} \\ & x^{2} + 18 x + 81 = 9 x^{2} + 18 x + 9 + 9 y^{2} \\ & 8 x^{2} + 9 y^{2} = 72$$

---

Dividing both sides of the equation by 72, we obtain:

$$\frac{8 x^{2}}{72} + \frac{9 y^{2}}{72} = 1$$

Therefore, the equation of the ellipse passing through the points mentioned above, and such that the sum of the distances from any point ( P ) on the curve to the two foci is equal to 6, is:

$$\frac{x^{2}}{9} + \frac{y^{2}}{8} = 1$$

## Glossary

- Ellipse: the set of all points in a plane where the sum of the distances to two fixed points (foci) is constant.
- Foci: the two fixed points in the plane used to define an ellipse.
- Conic section: a curve formed by the intersection of a plane and a cone; includes circumferences, parabolas, ellipses, and hyperbolas.
- Major axis: the longest diameter of an ellipse, passing through the foci and the center. Its length is $2 a$.
- Semi-najor axis: half the length of the major axis, denoted by $a$.
- Minor axis: the shortest diameter of an ellipse, perpendicular to the major axis and passing through the center. Its length is $2 b$.
- Semi-minor axis: half the length of the minor axis, denoted by $b$.
- Center: the midpoint of the segment connecting the two foci.
- Focal distance: the distance between the two foci, equal to $2 c$.
- Vertices: the four points where an ellipse intersects the coordinate axes.
- Eccentricity $e$: the ratio of the focal distance $2 c$ to the length of the major axis $2 a$, $e = c / a$. It is a measure of how stretched the ellipse is, with $0 \leq e < 1$.
