---
layout: post
title: "Integral Test for Series Convergence – Full Explanation with Examples"
date: 2026-03-05
description: "Understand the Integral Test for series convergence — conditions, proof idea, and solved examples connecting series to improper integrals."
---

The **Integral Test** connects the convergence of a series to the convergence of an improper integral. It is particularly useful when the general term $a_n = f(n)$ for some easily integrable function $f$.

---

## Statement of the Test

Let $f(x)$ be a function that is:
- **Positive**: $f(x) > 0$ for $x \geq 1$
- **Continuous** on $[1, \infty)$
- **Decreasing**: $f'(x) \leq 0$ for $x \geq 1$

Let $a_n = f(n)$. Then:

$$
\sum_{n=1}^{\infty} a_n \quad \text{and} \quad \int_1^{\infty} f(x)\, dx
$$

**both converge or both diverge.**

---

## Geometric Intuition

Think of each term $a_n$ as the area of a rectangle of width 1 and height $f(n)$. Since $f$ is decreasing, these rectangles approximate the area under the curve. If the total area under the curve is finite, so is the sum of rectangle areas.

---

## Solved Example 1 — p-Series

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2}$

Let $f(x) = \frac{1}{x^2}$ — positive, continuous, decreasing. ✓

$$
\int_1^{\infty} \frac{1}{x^2}\, dx = \left[-\frac{1}{x}\right]_1^{\infty} = 0 - (-1) = 1
$$

The integral converges → the series **converges**. ✓

---

## Solved Example 2 — Harmonic Series

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n}$

$$
\int_1^{\infty} \frac{1}{x}\, dx = \ln x \Big|_1^{\infty} = \infty
$$

The integral diverges → the series **diverges**. ✗

---

## Solved Example 3 — Logarithmic Series

**Test:** $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n \ln n}$

Let $f(x) = \frac{1}{x \ln x}$, positive, continuous, decreasing for $x \geq 2$.

$$
\int_2^{\infty} \frac{1}{x \ln x}\, dx
$$

Let $u = \ln x$, $du = \frac{dx}{x}$:

$$
= \int_{\ln 2}^{\infty} \frac{du}{u} = \ln u \Big|_{\ln 2}^{\infty} = \infty
$$

The integral diverges → the series **diverges**. ✗

---

## Solved Example 4

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + 1}$

$$
\int_1^{\infty} \frac{1}{x^2+1}\, dx = \arctan x \Big|_1^{\infty} = \frac{\pi}{2} - \frac{\pi}{4} = \frac{\pi}{4}
$$

The integral converges → the series **converges**. ✓

---

## Important Note

The Integral Test tells us **whether** a series converges — but the value of the integral is **not** equal to the sum of the series.

$$
\int_1^{\infty} f(x)\, dx \neq \sum_{n=1}^{\infty} a_n
$$

---

## Conditions Checklist

Before applying the Integral Test, always verify:
- [ ] $f(x) > 0$
- [ ] $f(x)$ is continuous on $[1, \infty)$
- [ ] $f(x)$ is eventually decreasing
