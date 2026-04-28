---
layout: chapter
title: "Simple Harmonic Motion"
chapter: "Kinematics"
chapter_order: 21
section_order: 3
permalink: /materi-algebrica/kinematics/simple-harmonic-motion/
---

## What is simple harmonic motion

A simple harmonic motion is a straight-line motion obtained by projecting the uniform circular motion of a body onto a fixed diameter of the circle. In this case, a material point repeatedly moves along the diameter, oscillating back and forth, and returning to the same position at regular [intervals](https://algebrica.org/intervals/) of time equal to the period of the motion.

![](https://algebrica.org/wp-content/uploads/resources/images/harmonic-motion-1.png)

This projection creates a smooth and continuous oscillation, where the displacement from the center varies [sinusoidally](https://algebrica.org/sine-and-cosine) with time. The position as a function of time for simple harmonic motion is given by the equation:

$$x \left(\right. t \left.\right) = A sin ⁡ \left(\right. \omega t \left.\right)$$

- $A$ is the amplitude, the maximum displacement from the equilibrium position (the function $sin ⁡ \left(\right. \omega t \left.\right)$ oscillates between the values $+ 1$ and $- 1$).
- $\omega$ is the angular frequency (in radians per second).
- $t$ is the time variable.

Since the function is periodic with period $T$, meaning it repeats itself from $t$ to $t + T$, the argument of the trigonometric function must change by $2 \pi$.
 Therefore, we have:

$$\omega \left(\right. t + T \left.\right) - \omega t = 2 \pi$$

From this, we derive the fundamental relation:
$$\omega = \frac{2 \pi}{T}$$
where $\nu$ represents the frequency of the harmonic motion, and is related to the period by:

$$\nu = \frac{1}{T}$$

---

In simple harmonic motion where the center of oscillation does not coincide with the origin but is located at $x_{0}$, the general equation of motion is:

$$x - x_{0} = A sin ⁡ \left(\right. \omega t + \varphi \left.\right)$$

- $x \left(\right. t \left.\right)$ is the position of the material point at time ( t ),
- $x_{0}$ is the center around which the motion oscillates,
- $A$ is the amplitude,
- $\omega$ is the angular frequency,
- $\varphi$ is the initial phase.

## Example 1

For example, calculate the equation of a simple harmonic motion with period $T = 3 \text{s}$ and amplitude $A = 0.5 \text{m}$.

We find the angular frequency.

$$\omega = \frac{2 \pi}{T} = \frac{2 \pi}{3} \text{rad}/\text{s}$$

Thus, the motion equation is:

$$x \left(\right. t \left.\right) = 0.5 sin ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

## Velocity

To find the instantaneous [scalar velocity](https://algebrica.org/velocity) $v \left(\right. t \left.\right)$, we [differentiate](https://algebrica.org/derivatives) $x \left(\right. t \left.\right)$ with respect to time:

$$v \left(\right. t \left.\right) = \frac{d x}{d t}$$

Applying the derivative:
$$\frac{d}{d t} \left(\right. A sin ⁡ \left(\right. \omega t \left.\right) \left.\right) = A \omega cos ⁡ \left(\right. \omega t \left.\right)$$

Thus, the instantaneous velocity of the material point is:
$$v \left(\right. t \left.\right) = A \omega cos ⁡ \left(\right. \omega t \left.\right)$$

This expression shows that the velocity varies over time following a [cosine function](https://algebrica.org/cosine-function), reaching its maximum when the particle passes through the equilibrium position.

- The velocity in simple harmonic motion is not constant: it changes over time following the trend of a cosine function.
- When the body passes through the equilibrium position (that is, $x = 0$, the center of motion), the velocity is maximum.
- When the body reaches the extremes (that is, at the points $x = + A$ or $x = - A$), the velocity is zero.
- The velocity, being a function of the cosine, is phase-advanced with respect to the displacement $x$ in simple harmonic motion.

## Example 2

For example, calculate the instantaneous velocity of a simple harmonic motion with period $T = 3 \text{s}$ and amplitude $A = 0.5 \text{m}$.

---

We find the angular frequency.

$$\omega = \frac{2 \pi}{T} = \frac{2 \pi}{3} \text{rad}/\text{s}$$

The position function is:

$$x \left(\right. t \left.\right) = 0.5 sin ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

Differentiating with respect to time to find the velocity:

$$v \left(\right. t \left.\right) = \frac{d x}{d t} = 0.5 \times \frac{2 \pi}{3} cos ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

Simplifying we obtain:

$$v \left(\right. t \left.\right) = \frac{\pi}{3} cos ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

## Acceleration

To find the instantaneous [acceleration](https://algebrica.org/acceleration) $a \left(\right. t \left.\right)$, we [differentiate](https://algebrica.org/derivatives) the velocity function $v \left(\right. t \left.\right)$ with respect to time:

$$a \left(\right. t \left.\right) = \frac{d v}{d t}$$

Applying the derivative:

$$\frac{d}{d t} \left(\right. A \omega cos ⁡ \left(\right. \omega t \left.\right) \left.\right) = - A \omega^{2} sin ⁡ \left(\right. \omega t \left.\right)$$

Thus, the instantaneous acceleration of the material point is:

$$a \left(\right. t \left.\right) = - A \omega^{2} sin ⁡ \left(\right. \omega t \left.\right)$$

This expression shows that the acceleration varies over time following a [sine function](https://algebrica.org/sine-function), reaching its maximum magnitude when the particle is at the maximum displacement from the equilibrium position.

- The acceleration in simple harmonic motion is not constant: it changes over time following the trend of a sine function.
- When the body passes through the equilibrium position (that is, $x = 0$, the center of motion), the acceleration is zero.
- When the body reaches the extremes (that is, at the points $x = + A$ or $x = - A$), the acceleration reaches its maximum magnitude.

The acceleration, being a function of the sine, is in phase opposition with respect to the displacement $x$. In simple harmonic motion the acceleration has only a normal component $a_{n}$ and it is centripetal, always directed toward the center of oscillation. This means that as the particle moves, the acceleration acts continuously to pull it back toward the equilibrium position.

> In uniformly [accelerated rectilinear motion](https://algebrica.org/acceleration), the acceleration [vector](https://algebrica.org/vectors/) has two components: a normal component $a_{n}$ and a tangential component $a_{t}$. Since the trajectory is still a straight line, the normal component $a_{n} = 0$. However, the tangential component $a_{t}$ is constant and nonzero, representing a steady change in the velocity’s magnitude along the direction of motion.

## Example 3

For example, calculate the acceleration in a simple harmonic motion with period $T = 3 , \text{s}$ and amplitude $A = 0.5 \text{m}$.

---

Let’s review the steps followed in the previous examples. First, we find the angular frequency.

$$\omega = \frac{2 \pi}{T} = \frac{2 \pi}{3} \text{rad}/\text{s}$$

Starting from the motion equation:

$$x \left(\right. t \left.\right) = 0.5 sin ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

The velocity is:

$$v \left(\right. t \left.\right) = 0.5 \times \frac{2 \pi}{3} cos ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right) = \frac{\pi}{3} cos ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

Differentiating again, we find the acceleration:

$$a \left(\right. t \left.\right) = \frac{d v}{d t} = - \left(\right. \frac{\pi}{3} \times \frac{2 \pi}{3} \left.\right) sin ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$

Simplifying:

$$a \left(\right. t \left.\right) = - \frac{2 \pi^{2}}{9} sin ⁡ \left(\right. \frac{2 \pi}{3} t \left.\right)$$
