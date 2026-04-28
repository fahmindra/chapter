---
layout: chapter
title: "Systems of Inequalities"
chapter: "Inequalities"
chapter_order: 8
section_order: 9
permalink: /materi-algebrica/inequalities/systems-of-inequalities/
---

## Linear systems of inequalities in one variable

A system of inequalities is a collection of two or more inequalities that involve one or several variables and are considered simultaneously. The goal is to determine the set of all values of the variables that satisfy every inequality in the system at the same time. In other words, the solution is given by the common region (or the intersection) of the individual solution sets associated with each inequality.

In this section, we focus on linear systems involving a single real variable $x$. Such systems typically consist of inequalities of first degree and can be written in the general form:

$$\left{\right. f_{1} \left(\right. x \left.\right) \geq 0 \\ f_{2} \left(\right. x \left.\right) \geq 0 \\ \vdots \\ f_{k} \left(\right. x \left.\right) \geq 0$$

where $f_{i} \left(\right. x \left.\right)$ are functions or expressions involving the variable $x$ and the relation can be any inequality sign: $< , \leq , > , \geq$. A system with no solutions is called an inconsistent system. If even a single inequality in the system has no solution, the entire system is considered inconsistent.

In the section on [linear inequalities](https://algebrica.org/linear-inequalities), we have seen examples of how to solve inequalities involving the [absolute value function](https://algebrica.org/absolute-value-function). In such cases, it is necessary to use a system of inequalities to find the solution. Let’s look at another example of how to solve a system of linear inequalities.

## Example 1

Consider the following system of linear inequalities:

$$\left{\right. 3 x + 6 > 0 \\ x - 3 \geq 0 \\ 9 - x > 0$$

We need to find the values of $x$ that simultaneously satisfy all three inequalities. Solving the individual inequalities, we obtain:

$$\left{\right. 3 x + > - 6 \rightarrow x > - 2 \\ x \geq 3 \\ - x > - 9 \rightarrow x < 9$$

We have, therefore, three intervals: $x > - 2$, $x \geq 3$, $x < 9$. As mentioned, the solution to the system is the one that satisfies all three inequalities simultaneously. We will represent the values on the number line and determine the common interval that meets the requirements.

|  | $$- 2$$ | $$3$$ | $$9$$ |  |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

The solution to the system is:
$$x \in \left[\right. 3 , 9 \left.\right)$$

##### This interval includes $3$ and excludes $9$. For a more detailed discussion of the structure and interpretation of intervals, refer to the [dedicated entry](https://algebrica.org/determining-the-domain-of-a-function/).

## General strategy for solving systems of inequalities

What we have seen is a very simple system of three linear inequalities involving the variable $x$. Systems of inequalities can be much more complex and may include rational functions, [roots](https://algebrica.org/radicals), [powers](https://algebrica.org/powers/), [logarithms](https://algebrica.org/logarithms), exponentials, and [trigonometric functions](https://algebrica.org/sine-and-cosine).

Although the specific solution procedure depends on the particular form and properties of the functions involved, the overarching principle remains the same: the admissible values are those that satisfy all inequalities in the system simultaneously, that is, the intersection of their individual solution sets.

In general, the solution of a system of inequalities follows a well-defined sequence of steps. The typical procedure is as follows:

- Solve each inequality individually and determine its corresponding solution set.
- When appropriate, represent the solution sets on the real line to visualize the resulting intervals.
- Identify the intersection of all solution sets, since only the values shared by every inequality satisfy the system.
- Express the final solution using the appropriate interval notation, ensuring that inclusions and exclusions at the endpoints are correctly indicated.

##### This structured approach provides a dependable framework that can be adapted to a wide variety of problems. As the complexity of the functions involved increases, the same principles guide the analysis, ensuring that each step remains logically grounded and methodologically consistent.

## Example 2

Consider the following system of linear inequalities:

$$\left{\right. log_{2} ⁡ \left(\right. 2 x + 4 \left.\right) > log_{2} ⁡ \left(\right. x \left.\right) \\ x - 2 > 0$$

To solve this inequality, we first need to determine the [domain](https://algebrica.org/determining-the-domain-of-a-function/) of the logarithm. A logarithm is defined only when its argument is greater than zero. Therefore, in this case, we have:

$$& 2 x + 4 > 0 \rightarrow x > - 2 \\ & x > 0 \rightarrow x > 0$$

The intersection of these two conditions yields $x > 0$. At this stage, we turn to the first inequality. Since the logarithms $log_{2} ⁡ \left(\right. 2 x + 4 \left.\right)$ and $log_{2} ⁡ \left(\right. x \left.\right)$ share the same base, the inequality can be analyzed by directly comparing the arguments of the two logarithmic expressions.

$$2 x + 4 > x \rightarrow x > - 2$$

Now, by intersecting this solution with the domain of the logarithm, we obtain $x > 0$. Considering the second inequality, we obtain $x > 2$. Now, let’s check where the two solutions are satisfied simultaneously:

|  | $$0$$ | $$2$$ |  |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

The solution to the system is:
$$x > 2$$

## Multivariable systems of inequalities

There are also more complex systems of inequalities consisting of $k$ inequalities involving $m$ variables, having the general form:

$$\left{\right. f_{1} \left(\right. x_{1} , x_{2} , \ldots x_{m} \left.\right) \geq 0 \\ f_{2} \left(\right. x_{1} , x_{2} , \ldots x_{m} \left.\right) \geq 0 \\ \vdots \\ f_{k} \left(\right. x_{1} , x_{2} , \ldots x_{m} \left.\right) \geq 0$$

These systems require more advanced solution methods, such as graphical methods, sign analysis, linear programming, and various numerical techniques. Therefore, they will be covered in more detail in other sections.
