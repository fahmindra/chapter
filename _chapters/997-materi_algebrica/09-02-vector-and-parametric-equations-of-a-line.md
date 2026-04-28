---
layout: chapter
title: "Vector and Parametric Equations of a Line"
chapter: "Lines, Planes and Conic Sections"
chapter_order: 9
section_order: 2
permalink: /materi-algebrica/lines-planes-and-conic-sections/vector-and-parametric-equations-of-a-line/
---

## From Cartesian to vector form

We’ve seen that the equation of a line can be written in [Cartesian form](https://algebrica.org/lines), such as the explicit equation:
$$y = m x + q$$

where the line is described using coordinates in the plane. However, lines can also be expressed in **vector form**, using points and direction [vectors](https://algebrica.org/vectors/) to represent their position and orientation.

---

Let’s consider a directed vector $\overset{\rightarrow}{v}$. The line passing through a point $P_{0}$ and parallel to $\overset{\rightarrow}{v}$ consists of all points $P$ such that the vector $P - P_{0}$ is parallel to $\overset{\rightarrow}{v}$. The **vector equation** of a line is given by:

$$P - P_{0} = t \overset{\rightarrow}{v} \text{with} t \in \mathbb{R}$$

![Vector equations of a line.](https://algebrica.org/wp-content/uploads/resources/images/vector-equation-line-1.png)

Here, $P_{0}$ is a fixed point on the line, $\overset{\rightarrow}{v}$ is a direction vector, and $t$ is a real parameter. The point $P$ varies along the line as $t$ changes.

##### The vector representation of a line expresses all its points in a compact and geometric form, making the direction and position immediately clear, and serves as a natural bridge between coordinate geometry and linear algebra.

## Parametric form

Let’s now fix an orthonormal basis, that is a reference system where the axes are perpendicular to each other and the vectors that define them have unit length. In practice, this means we’re working in the standard Cartesian plane, where the x-axis is aligned with $\overset{\rightarrow}{i} = \left(\right. 1 , 0 \left.\right)$ and the y-axis with $\overset{\rightarrow}{j} = \left(\right. 0 , 1 \left.\right)$.

Let’s represent the fixed point $P_{0}$ and a generic point $P$ using coordinates:

$$P_{0} = \left(\right. x_{0} , y_{0} \left.\right) \text{and} P = \left(\right. x , y \left.\right)$$

Using the vector equation of the line, we obtain:

$$P - P_{0} & = \left(\right. P - O \left.\right) - \left(\right. P_{0} - O \left.\right) \\ & = \left(\right. x - x_{0} \left.\right) \overset{\rightarrow}{i} + \left(\right. y - y_{0} \left.\right) \overset{\rightarrow}{j}$$

Let’s now take into account the fact that in an orthonormal basis, any vector can be decomposed along the x and y axes. In other words:

$$\overset{\rightarrow}{v} = (\text{movement along x}) \cdot \overset{\rightarrow}{i} + (\text{movement along y}) \cdot \overset{\rightarrow}{j}$$

Therefore, the term $t \overset{\rightarrow}{v}$ on the right-hand side of the vector equation of the line can be written as:

$$\overset{\rightarrow}{v} = k \overset{\rightarrow}{i} + h \overset{\rightarrow}{j}$$

so the expression becomes:

$$t \overset{\rightarrow}{v} = t \left(\right. k \overset{\rightarrow}{i} + h \overset{\rightarrow}{j} \left.\right)$$

We can now rewrite the vector equation of the line as:

$$\left(\right. x - x_{0} \left.\right) \overset{\rightarrow}{i} + \left(\right. y - y_{0} \left.\right) \overset{\rightarrow}{j} = t k \overset{\rightarrow}{i} + t h \overset{\rightarrow}{j}$$

By equating the components along the $\overset{\rightarrow}{i}$ and $\overset{\rightarrow}{j}$ directions, we obtain the following system of **parametric equations**:

$$\left{\right. x = x_{0} + k t \\ y = y_{0} + h t$$

## Example

Let’s find the parametric equations of the line passing through the points:

$$P_{0} = \left(\right. 2 , 1 \left.\right) \text{and} P = \left(\right. 5 , 4 \left.\right)$$

---

To define a line parametrically, we need a point and a direction. Since both $P_{0}$ and $P$ lie on the line, we can compute the direction vector $\overset{\rightarrow}{v}$ by subtracting their coordinates:

$$\overset{\rightarrow}{v} = P - P_{0} = \left(\right. 5 - 2 , 4 - 1 \left.\right) = \left(\right. 3 , 3 \left.\right)$$

This vector tells us how to move along the line starting from $P_{0}$: for every 3 units in the x-direction, we move 3 units in the y-direction. We now use the parametric form of the line, which expresses each coordinate as a function of a parameter $t$:

$$\left{\right. x = x_{0} + k t \\ y = y_{0} + h t \text{with} t \in \mathbb{R}$$

In our case we have:

- Coordinates of $P_{0}$: $x_{0} = 2$, $y_{0} = 1$
- components of the direction vector $\overset{\rightarrow}{v}$: $k = 3$, $h = 3$

Substituting into the equations, we obtain:

$\left{\right. x = 2 + 3 t \\ y = 1 + 3 t \text{with} t \in \mathbb{R}$

This system describes all the points on the line that passes through $\left(\right. 2 , 1 \left.\right)$ and $\left(\right. 5 , 4 \left.\right)$. By varying $t$, we can generate every point along the line in both directions.

##### This method works for any two points: by finding the direction vector and using the parametric form, we can always describe the entire line.

## How are the vector and parametric forms of a line different?

The vector form describes the line geometrically: it builds every point $P$ by starting from a fixed point $P_{0}$ and moving in the direction of a vector $\overset{\rightarrow}{v}$. It looks like this:

$$P = P_{0} + t \overset{\rightarrow}{v}$$

The parametric form takes that same rule and writes it out in terms of coordinates, one equation for each axis, using the components of the direction vector:

$$\left{\right. x = x_{0} + k t \\ y = y_{0} + h t t \in \mathbb{R}$$

Both forms describe the same set of points. The vector form is compact and geometric; the parametric form is explicit and ready to calculate with. Use whichever makes more sense for the problem you’re solving, they’re mathematically identical.
