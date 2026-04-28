---
layout: chapter
title: "Uniformly Accelerated Motion: Acceleration"
chapter: "Kinematics"
chapter_order: 21
section_order: 2
permalink: /materi-algebrica/kinematics/uniformly-accelerated-motion-acceleration/
---

## Introduction

Kinematics is the study of the motion of objects, describing their position, [velocity](https://algebrica.org/velocity), and acceleration over time. Before diving into a detailed explanation of these phenomena, it is essential to introduce some key concepts.

- A material point is an idealized object whose size is considered negligible relative to the distances involved in its motion.
- The trajectory is the path traced by a material point as it moves through space.
- A motion is said to be rectilinear if its trajectory lies along a straight line.

If a material point moves along a [straight-line](https://algebrica.org/lines) path under constant acceleration, meaning that the rate of change of velocity remains uniform over time, the motion is called **uniformly accelerated rectilinear motion**.

## Acceleration

Let us consider a particle moving along a straight-line trajectory, where the position as a function of time is not described by a [linear equation](https://algebrica.org/linear-equations/). Let $P_{1}$ and $P_{2}$ denote two positions of the material point along the $x$-axis at times $t_{1}$ and $t_{2}$, respectively. We denote by $\mathbf{v}_{1}$ and $\mathbf{v}_{2}$ the corresponding velocity [vectors](https://algebrica.org/vectors/), with $\mathbf{v}_{1} \neq \mathbf{v}_{2}$. The **vector acceleration** is defined as the following limit:

$$\mathbf{a} = \underset{\Delta t \rightarrow 0}{lim} \frac{\Delta \mathbf{v}}{\Delta t} = \frac{d \mathbf{v}}{d t}$$

We have seen, by analyzing the [velocity](https://algebrica.org/velocity), that:

$$\underset{\Delta t \rightarrow 0}{lim} \frac{\Delta \mathbf{r}}{\Delta t} = \frac{d \mathbf{r}}{d t} = \mathbf{v}$$

Thus, we have:

$$\mathbf{a} = \frac{d}{d t} \left(\right. \frac{d \mathbf{r}}{d t} \left.\right) = \frac{d^{2} \mathbf{r}}{d t^{2}}$$

---

Starting from the general expression of acceleration it is possible to introduce the concept of **tangential acceleration** As a point $P$ travels along a given path, the acceleration vector $\mathbf{a}$ can be broken down into two components:

- One tangential to the trajectory.
- One normal to the trajectory (also called centripetal acceleration that points toward the center of the curvature of the path).

The tangential acceleration, denoted by $\mathbf{a}_{t}$, corresponds to the variation of the speed over time. It is defined as:

$$a_{t} = \frac{d v}{d t} = \mathbf{i} a_{t}$$

where $v$ represents the magnitude of the velocity vector $\mathbf{v}$ and $\mathbf{i}$ represents a directed and oriented vector.

![The acceleration vector consists of two parts: a tangential component and a normal component.](https://algebrica.org/wp-content/uploads/resources/images/acceleration-1.png)

- If the magnitude of the velocity changes, there is tangential acceleration $\left(\right. a_{t} \neq 0 \left.\right)$.
- If the magnitude of the velocity remains constant, the tangential acceleration is zero $\left(\right. a_{t} = 0 \left.\right)$.

---

Uniformly accelerated motion is a type of motion in which the tangential acceleration $a_{t}$ is constant at every point and equal to the average acceleration over any time [interval](https://algebrica.org/intervals/). We have:

$$\frac{v - v_{0}}{t - t_{0}} = a_{t}$$

Starting from this formula, solving for $v$ and assuming $t_{0} = 0$, we obtain:

$$v = v_{0} + a_{t} t$$

In this way, derived the expression for velocity based on the definition of acceleration. Starting from the expression of velocity as a function of time we can derive the equation of motion by [integrating](https://algebrica.org/integrals) with respect to time:

$$y = \int_{0}^{t} v \left(\right. t \left.\right) d t = \int_{0}^{t} \left(\right. v_{0} + a_{t} t \left.\right) d t$$

Evaluating the integral, we obtain:

$$y = v_{0} t + \frac{1}{2} a_{t} t^{2}$$

where $y$ represents the displacement of the material point along the trajectory as a function of time.
