---
layout: post
title: "Applications of Sequences – Fixed Points, Contractions & Newton's Method"
date: 2026-02-27
description: "Explore powerful applications of real sequences — Banach's Fixed Point Theorem, contraction mappings, and Newton-Raphson method as a convergent sequence."
---

Real sequences are not just theoretical — they power numerical algorithms, fixed-point theorems, and iterative methods. This post explores the most important applications.

---

## Fixed Points

**Definition:** A point $x^* \in \mathbb{R}$ is a **fixed point** of $f: \mathbb{R} \to \mathbb{R}$ if:

$$f(x^*) = x^*$$

**Example:** $f(x) = \frac{x}{2} + 1$ has fixed point $x^* = 2$ since $f(2) = 2$. ✓

---

## Contraction Mapping

**Definition:** $f: [a,b] \to [a,b]$ is a **contraction** if $\exists\, 0 \leq k < 1$:

$$|f(x) - f(y)| \leq k|x-y| \quad \forall\, x,y \in [a,b]$$

---

## Banach Fixed Point Theorem

**Theorem:** If $f: [a,b] \to [a,b]$ is a contraction with constant $k < 1$, then:

1. $f$ has a **unique fixed point** $x^*$
2. For any $x_0 \in [a,b]$, the sequence $x_{n+1} = f(x_n)$ converges to $x^*$

**Rate of convergence:**

$$|x_n - x^*| \leq \frac{k^n}{1-k}|x_1 - x_0|$$

---

## Proof Sketch

Define $x_{n+1} = f(x_n)$. Then:

$$|x_{n+1} - x_n| = |f(x_n) - f(x_{n-1})| \leq k|x_n - x_{n-1}| \leq \cdots \leq k^n|x_1 - x_0|$$

For $m > n$:

$$|x_m - x_n| \leq \sum_{j=n}^{m-1}|x_{j+1}-x_j| \leq \frac{k^n}{1-k}|x_1-x_0| \to 0$$

So $\{x_n\}$ is Cauchy → converges to some $x^*$. Taking limits: $f(x^*) = x^*$. $\blacksquare$

---

## Example 1 — Solving $x = \cos x$

Define $f(x) = \cos x$ on $[0, 1]$.

$|f'(x)| = |\sin x| \leq \sin(1) \approx 0.84 < 1$ → contraction with $k = 0.84$.

Starting from $x_0 = 0$:

$$x_1 = \cos 0 = 1,\quad x_2 = \cos 1 \approx 0.5403,\quad x_3 \approx 0.8576, \ldots$$

Converges to $x^* \approx 0.7391$ (Dottie number). ✓

---

## Newton-Raphson Method

To find roots of $g(x) = 0$, define:

$$x_{n+1} = x_n - \frac{g(x_n)}{g'(x_n)}$$

This is a fixed-point iteration for $f(x) = x - \frac{g(x)}{g'(x)}$.

**Example: $\sqrt{2}$ via $g(x) = x^2 - 2$**

$$x_{n+1} = x_n - \frac{x_n^2 - 2}{2x_n} = \frac{x_n}{2} + \frac{1}{x_n}$$

Starting from $x_0 = 1$:

| $n$ | $x_n$ |
|-----|-------|
| 0 | 1 |
| 1 | 1.5 |
| 2 | 1.41\overline{6} |
| 3 | 1.41421356... |
| 4 | $\sqrt{2}$ to 12 digits |

**Quadratic convergence:** The number of correct digits roughly doubles each step!

---

## Example 2 — Contraction on $\mathbb{R}$

**Claim:** $f(x) = \frac{1}{2}x + 3$ is a contraction on $\mathbb{R}$.

$$|f(x)-f(y)| = \frac{1}{2}|x-y|, \quad k = \frac{1}{2}$$

Fixed point: $x^* = \frac{1}{2}x^* + 3 \implies x^* = 6$.

Starting from $x_0 = 0$: $0, 3, 4.5, 5.25, 5.625, \ldots \to 6$. ✓

---

## Picard Iteration for ODEs

The Banach Fixed Point Theorem also solves ODEs. The initial value problem:

$$y' = f(x, y),\quad y(x_0) = y_0$$

is equivalent to the integral equation:

$$y(x) = y_0 + \int_{x_0}^x f(t, y(t))\, dt = T[y](x)$$

Under Lipschitz conditions on $f$, $T$ is a contraction → **unique solution exists** (Picard-Lindelöf theorem).
