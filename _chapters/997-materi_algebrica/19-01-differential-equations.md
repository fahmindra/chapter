---
layout: chapter
title: "Differential Equations"
chapter: "Differential Equations"
chapter_order: 19
section_order: 1
permalink: /materi-algebrica/differential-equations/differential-equations/
---

## What Are Differential Equations?

An ordinary differential equation is a relation involving a function $f \left(\right. x \left.\right)$, defined on an interval $I \subset \mathbb{R}$, together with a finite number of its [derivatives](https://algebrica.org/derivatives). The equation is required to hold for all $x$ in the interval $I$. The general form of an ordinary differential equation of order $n$ is:

$$F \left(\right. x , f \left(\right. x \left.\right) , f^{'} \left(\right. x \left.\right) , f^{''} \left(\right. x \left.\right) , \ldots , f^{\left(\right. n \left.\right)} \left(\right. x \left.\right) \left.\right) = 0$$

where $F$ is a given function that depends on the independent variable $x$, the unknown function $y = f \left(\right. x \left.\right)$, and its derivatives up to order $n$. An example of a differential equation is:

$$f^{'} \left(\right. x \left.\right) + x f \left(\right. x \left.\right) = 0 \text{or} y^{'} + x y = 0$$

## Order of a differential equation

The order of a differential equation is defined as the order of the highest derivative that appears in the equation. For example, the following differential equation is of third order because the third derivative of $y$ is the highest-order derivative appearing in the equation:

$$y^{''} - 3 y^{'} + 2 y = 0$$

Differential equations are often considered challenging. For this reason, we will introduce the concepts gradually, with the goal of building a solid understanding of the methods used to solve them.

## Solutions of a differential equation

In general, a differential equation may admit infinitely many solutions. A general solution is a family of functions depending on $n$ arbitrary constants, where $n$ corresponds to the order of the equation. This family includes every possible solution of the differential equation.

- Any function that satisfies the differential equation is called a solution, or integral of the equation.
- A particular solution of a differential equation is a specific function obtained by assigning concrete values to the arbitrary constants in the general solution.
- Initial conditions are constraints that allow us to select a particular solution from the general family.

## Forms and Types of Differential Equations

A differential equation is said to be in normal form when it can be written as:

$$y^{\left(\right. n \left.\right)} = F \left(\right. x , y , \ldots , y^{\left(\right. n - 1 \left.\right)} \left.\right)$$

That is, the equation is explicitly solved with respect to the highest-order derivative.

---

A differential equation is said to be autonomous if the independent variable does not appear explicitly in its expression. The equation$y^{'} = y^{2} - 1$ is autonomous, since the right-hand side depends only on $y$, not on the independent variable $x$.

---

Given a differential equation along with a set of initial conditions, the problem of finding a solution that satisfies both the equation and the specified conditions is called a Cauchy problem. A Cauchy problem for a first-order differential equation is typically written as:

$$\left{\right. y^{'} \left(\right. x \left.\right) = f \left(\right. x , y \left(\right. x \left.\right) \left.\right) \\ y \left(\right. x_{0} \left.\right) = y_{0}$$

where $y^{'} \left(\right. x \left.\right) = f \left(\right. x , y \left(\right. x \left.\right) \left.\right)$ is the differential equation, and $y \left(\right. x_{0} \left.\right) = y_{0}$ is the initial condition, specifying the value of the solution at $x = x_{0}$.

## How to solve simple differential equations

Let’s begin by solving very simple differential equations, specifically first-order equations of the form $y^{'} = f \left(\right. x \left.\right)$. In this case, the solution is obtained by [integrating](https://algebrica.org/indefinite-integrals/) both sides of the equation, yielding:

$$\int y^{'} d x = \int f \left(\right. x \left.\right) d x$$

For this type of equation, the general solution is given by:

$$y \left(\right. x \left.\right) = \int f \left(\right. x \left.\right) d x + c$$

where $c \in \mathbb{R}$ is an arbitrary constant.

## Example 1

Let’s solve the differential equation:

$$y^{'} - 3 x = 0$$

---

Let’s rewrite it in standard form and integrate both sides:

$$y^{'} = 3 x$$

$$\int y^{'} d x = \int 3 x d x \rightarrow y \left(\right. x \left.\right) = \frac{3}{2} x^{2} + c$$

---

The solutions are represented by the integral curves given by the equation:

$$y \left(\right. x \left.\right) = \frac{3}{2} x^{2} + c$$

![](https://algebrica.org/wp-content/uploads/resources/images/differential-equations-1-1.png)

---

##### Each curve represents a particular solution of the general form. The value of $C$ determines the vertical position (a vertical translation) of the curve. All the curves share the same upward-opening [parabolic](https://algebrica.org/parabola) shape, but they are vertically shifted depending on the value of $C$. Together, this family of curves represents the complete set of solutions to the differential equation.

The solution is:

$$y \left(\right. x \left.\right) = \frac{3}{2} x^{2} + c$$

## Separable Differential Equations

A first-order differential equation is said to be separable if it can be rewritten in the form:

$$y^{'} = a \left(\right. x \left.\right) b \left(\right. y \left.\right)$$

To find the general integral of this type of equation, we begin by dividing both sides of the equation by $b \left(\right. y \left.\right)$. We obtain:

$$\frac{y^{'}}{b \left(\right. y \left.\right)} = a \left(\right. x \left.\right)$$

We then integrate both sides with respect to $x$, obtaining:

$$\int \frac{y \left(\right. x \left.\right)^{'}}{b \left(\right. y \left(\right. x \left.\right) \left.\right)} d x = \int a \left(\right. x \left.\right) d x + c$$

By substituting $y = y \left(\right. x \left.\right)$, we obtain:

$$\int \frac{d y}{b \left(\right. y \left.\right)} d x = \int a \left(\right. x \left.\right) d x + c$$

## Example 2

Let’s solve the differential equation:

$$y^{'} = x y$$

---

We have a separable differential equation. We rewrite all the terms involving $y$ on one side and those involving $x$ on the other:

$$\frac{1}{y} d y = x d x$$

---

We integrate both sides and obtain:

$$\int \frac{1}{y} d y = \int x d x$$

$$ln ⁡ \left|\right. y \left|\right. = \frac{x^{2}}{2} + c$$

##### For a complete overview of integration rules and common integrals, see the [dedicated entry](https://algebrica.org/indefinite-integral) on the topic.

---

To isolate $y$, we eliminate the logarithm by exponentiating both sides:

$$\left|\right. y \left|\right. = e^{\frac{x^{2}}{2} + c} = e^{c} \cdot e^{\frac{x^{2}}{2}} = c e^{\frac{x^{2}}{2}}$$

where $c$ is a constant representing $e^{c}$.

Since $c$ is an arbitrary constant in $\mathbb{R}$, which may be either positive or negative, we can write the general solution of the equation as:

$$y \left(\right. x \left.\right) = c e^{\frac{x^{2}}{2}} , c \in \mathbb{R}$$

---

The solutions are represented by the following integral curves:

![](https://algebrica.org/wp-content/uploads/resources/images/differential-equations-2.png)

Therefore, the general solution is:

$$y \left(\right. x \left.\right) = c e^{\frac{x^{2}}{2}} , c \in \mathbb{R}$$

## Glossary

- Ordinary differential equation: a relation involving a function defined on an interval and a finite number of its derivatives, which holds true at all points in the interval.
- Order of a differential equation: the order of the highest derivative present in the equation.
- General solution: a family of functions that satisfies the differential equation and contains arbitrary constants equal in number to the order of the equation.
- Particular solution: a specific function obtained from the general solution by assigning concrete values to the arbitrary constants.
- Initial conditions: conditions specifying the value of the solution and possibly its derivatives at a particular point, used to determine a unique particular solution.
- Cauchy problem: the task of finding a solution to a differential equation that satisfies given initial conditions, typically expressed as:
  $$y \left(\right. x_{0} \left.\right) = y_{0} , y^{'} \left(\right. x_{0} \left.\right) = y_{1} , \ldots$$
- Integral curves: the graphs of the solutions of a differential equation, representing how the function evolves along the plane.
