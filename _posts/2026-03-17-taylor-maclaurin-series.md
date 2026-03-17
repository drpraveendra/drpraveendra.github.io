---
layout: post
title: "Taylor & Maclaurin Series – Expansions, Derivations & Applications"
date: 2026-03-17
description: "Complete guide to Taylor and Maclaurin series — formula, derivations of standard expansions, convergence, and applications in approximation."
---

**Taylor Series** and **Maclaurin Series** allow us to represent functions as infinite power series. They are fundamental to analysis, physics, and numerical computation.

---

## Taylor Series

The Taylor series of $f(x)$ centered at $x = a$ is:

$$
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n
$$

$$
= f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \cdots
$$

When $a = 0$, it is called a **Maclaurin Series**.

---

## Standard Maclaurin Series

### 1. Exponential Function

$$
e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots \quad \forall\, x \in \mathbb{R}
$$

### 2. Sine Function

$$
\sin x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots
$$

### 3. Cosine Function

$$
\cos x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots
$$

### 4. Geometric Series

$$
\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + \cdots \quad |x| < 1
$$

### 5. Natural Logarithm

$$
\ln(1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots \quad -1 < x \leq 1
$$

---

## Derivation: Maclaurin Series for $e^x$

Since $\frac{d}{dx}e^x = e^x$, all derivatives at $x=0$ equal 1:

$$
f^{(n)}(0) = e^0 = 1
$$

So:

$$
e^x = \sum_{n=0}^{\infty} \frac{1 \cdot x^n}{n!} = \sum_{n=0}^{\infty} \frac{x^n}{n!}
$$

---

## Taylor Polynomial Approximation

The $N$-th degree Taylor polynomial approximates $f(x)$ near $x = a$:

$$
P_N(x) = \sum_{n=0}^{N} \frac{f^{(n)}(a)}{n!}(x-a)^n
$$

**Example:** Approximate $\sin(0.1)$ using 3 terms:

$$
\sin x \approx x - \frac{x^3}{6} + \frac{x^5}{120}
$$

$$
\sin(0.1) \approx 0.1 - \frac{0.001}{6} + \frac{0.00001}{120} \approx 0.09983
$$

*(Exact value: $0.099833...$) ✓*

---

## Taylor's Remainder Theorem

The error in using $P_N(x)$ is:

$$
|R_N(x)| \leq \frac{M \cdot |x-a|^{N+1}}{(N+1)!}
$$

where $M = \max|f^{(N+1)}|$ on the interval.

---

## Application: Euler's Formula

Combining the Maclaurin series for $e^x$, $\sin x$, and $\cos x$:

$$
e^{ix} = \cos x + i \sin x
$$

At $x = \pi$:

$$
e^{i\pi} + 1 = 0 \qquad \text{(Euler's Identity)}
$$

Often called the most beautiful equation in mathematics.
