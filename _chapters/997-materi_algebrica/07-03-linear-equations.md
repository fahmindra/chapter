---
layout: chapter
title: "Linear Equations"
chapter: "Equations"
chapter_order: 7
section_order: 3
permalink: /materi-algebrica/equations/linear-equations/
---

## What are linear equations?

Linear equations describe the relationship between variables linearly. These equations are considered the simplest form of [equations](https://algebrica.org/equations/) involving addition, subtraction, and multiplication. The standard form is:

$$a_{1} x_{1} + a_{2} x_{2} + \ldots + a_{n} x_{n} = b$$

- $x_{1} , x_{2} , \ldots , x_{n} \in \mathbb{R}$ are the variables.
- $a_{1} , a_{2} , \ldots , a_{n} \in \mathbb{R}$ are the coefficients: at least one coefficient $a_{i}$ must be non-zero.
- $b \in \mathbb{R}$ is the constant term.
- When the constant term $b$ is zero, the linear equation is called homogeneous.

##### Linear equations, in general terms, can involve more than one variable. For example, the equation $a x + b y + c = 0$ is a linear equation in two variables $x$ and $y$.

---

Linear equations are the foundation of systems of equations and matrix operations, which allow us to study and solve multiple equations simultaneously in a structured and efficient way. These topics are explored further in the dedicated sections of Algebrica: [Systems of Linear Equations](https://algebrica.org/systems-of-linear-equations/) and [Matrices](https://algebrica.org/matrices/).

## Type of solution

Geometrically, the type of solution to a linear equation depends on the number of variables.

- With one variable, the solution is a single point on the number line.
- With two variables, it’s a [line](https://algebrica.org/lines/) in the plane.
- With three variables, it becomes a plane in space.
- With more than three, it defines what’s called a hyperplane in higher dimensions.

## Linear equations in one variable

A linear equation in one variable can be expressed in the form $a x = b$, which has a unique solution, given by:

$$x = \frac{b}{a}$$

It is important to note that, since $a \neq 0$ by definition, a linear equation like this always admits one and only one solution.

---

In some cases the coefficients of a linear equation are not fixed constants but depend on one or more real parameters. This leads to what are commonly called [linear equations with parameters](https://algebrica.org/linear-equations-with-parameters/), where the behaviour of the equation varies according to the value assigned to the parameter.

###### A change in the parameter can transform the equation into an ordinary linear relation with a unique solution, but it can also produce special situations in which the equation becomes an identity or turns into a contradiction.

Solving first-degree equations in one variable can be straightforward. If the initial equation is already in its standard form, the process typically involves a series of steps to isolate the variable and perform the necessary calculations.

## Example 1

Solve the equation $2 x + 3 = 11 x$.

As the first step, we brought the equation into its standard form. In this case, there are no restrictions on the value of $x$, which exists throughout the [domain](https://algebrica.org/determining-the-domain-of-a-function/) of [real numbers](https://algebrica.org/types-of-number) $x \in \mathbb{R}$. By performing the calculations, we obtain:

$$2 x + 3 & = 11 x \\ 2 x - 11 x & = - 3 \\ - 9 x & = - 3 \\ x & = \frac{3}{9} \\ x & = \frac{1}{3}$$

---

Substituting the value $x = \frac{1}{3}$ into the original equation is crucial to ensuring the solution’s accuracy. Based on the calculations performed, the final equality is indeed confirmed.

$$2 \left(\right. \frac{1}{3} \left.\right) + 3 & = 11 \left(\right. \frac{1}{3} \left.\right) \\ \frac{2}{3} + 3 & = \frac{11}{3} \\ \frac{2}{3} + \frac{9}{3} & = \frac{11}{3} \\ \frac{11}{3} & = \frac{11}{3}$$

The solution to the equation is:

$$x = \frac{1}{3}$$

## Linear equations in two variables

When a linear equation involves two variables and the constant term is zero, such as $a x + b y = 0$, we have a homogeneous linear equation. This type of equation admits **infinitely many solutions**, since there are infinitely many pairs $\left(\right. x , y \left.\right)$ that satisfy the condition. The general solution can be expressed as:

$$x = \lambda b , y = - \lambda a$$

where $\lambda$ is a parameter $\in \mathbb{R}$. Each value of $\lambda$ generates a point on the line defined by the equation, meaning all solutions lie on a [straight line](https://algebrica.org/lines/) through the origin.

## Example 2

Let’s take the homogeneous linear equation:
$$2 x - 3 y = 0$$

---

This is a linear equation in two variables where the constant term is zero. It represents a straight line that passes through the origin. To find the general solution, we can express one variable in terms of the other. Solving for $y$:

$$2 x = 3 y \rightarrow y = \frac{2}{3} x$$

---

This shows that every solution $\left(\right. x , y \left.\right)$ satisfies this relationship. We can also describe all solutions using a parameter $\lambda \in \mathbb{R}$:
$$x = \lambda y = \frac{2}{3} \lambda$$

![](https://algebrica.org/wp-content/uploads/resources/images/linear-equations-1.png)

We can now take arbitrary values of $\lambda$, such as $\lambda = 3$ and $\lambda = - 6$ (but they could be any real number). We obtain:

- For $\lambda = 3$, we have $x = 3$, $y = 2$
- For $\lambda = - 6$, we have $x = - 6$, $y = - 4$

The solution to the equation $2 x - 3 y = 0$ is the set of all points $\left(\right. x , y \left.\right)$ that lie on the line defined by:

$$y = \frac{2}{3} x$$

## Linear equations with three variables

When a linear equation involves three variables, such as $a x + b y + c z = 0$ we have a homogeneous linear equation in three variables. Its solutions form a plane in three-dimensional space that passes through the origin. There are infinitely many solutions, since there are infinitely many triples $\left(\right. x , y , z \left.\right)$ that satisfy the equation.

The general solution can be written in parametric form by choosing two parameters, for example $\lambda$ and $\mu$. One possible form is:
$$x = \lambda , y = \mu , z = - \frac{a \lambda + b \mu}{c}$$
where $\lambda , \mu \in \mathbb{R}$ and $c \neq 0$. Each pair $\left(\right. \lambda , \mu \left.\right)$ gives a point on the plane. All solutions together form a plane that goes through the origin.

## Example 3

Let’s consider the equation:
$$x + 2 y - z = 0$$

---

We isolate $z$:
$$z = x + 2 y$$

Now we assign parameters to $x$ and $y$:
$$x = \lambda , y = \mu$$

Then:
$$z = \lambda + 2 \mu$$

The solution to the equation $x + 2 y - z = 0$ is the set of all points $\left(\right. x , y , z \left.\right)$ of the form:
$$\left(\right. x , y , z \left.\right) = \left(\right. \lambda , \mu , \lambda + 2 \mu \left.\right) \text{with} \lambda , \mu \in \mathbb{R}$$

## Linear equations with a parameter

A natural extension of the study of linear equations is to explore what happens when the coefficients are not fixed numbers but depend on one or more real parameters. In this setting we speak of [linear equations with a parameter](https://algebrica.org/linear-equations-with-parameters/), a family of relations of the form

$$a \left(\right. k \left.\right) x + b \left(\right. k \left.\right) = c \left(\right. k \left.\right)$$

whose behaviour varies according to the chosen value of the parameter. Depending on how the functions $a \left(\right. k \left.\right)$, $b \left(\right. k \left.\right)$, and $c \left(\right. k \left.\right)$ interact, the equation may admit a unique solution, become an identity valid for every real $x$, or turn into a contradiction with no solution at all.

###### This parametric viewpoint provides a clearer understanding of how linear models respond to external quantities and how their solution set changes as the parameter varies.
