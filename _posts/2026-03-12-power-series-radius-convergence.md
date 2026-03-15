---
layout: post
title: "Power Series & Radius of Convergence – Complete Guide"
date: 2026-03-12
description: "Understand power series, how to find the radius and interval of convergence using the Ratio Test, and key examples including common Maclaurin series."
---

A **Power Series** is an infinite series involving powers of $(x - a)$. Understanding when and where a power series converges is essential for calculus and analysis.

---

## Definition

A power series centered at $x = a$ is:

$$
\sum_{n=0}^{\infty} c_n (x-a)^n = c_0 + c_1(x-a) + c_2(x-a)^2 + \cdots
$$

When $a = 0$, it is called a **Maclaurin series**.

---

## Radius of Convergence

Every power series has a **radius of convergence** $R$ such that:
- The series **converges absolutely** for $|x - a| < R$
- The series **diverges** for $|x - a| > R$
- At $|x - a| = R$: must test separately

**Finding $R$ using the Ratio Test:**

$$
\frac{1}{R} = \lim_{n\to\infty} \left|\frac{c_{n+1}}{c_n}\right|
$$

---

## Solved Example 1

**Find radius of convergence:** $\displaystyle\sum_{n=0}^{\infty} \frac{x^n}{n!}$

$$
\left|\frac{a_{n+1}}{a_n}\right| = \left|\frac{x^{n+1}}{(n+1)!} \cdot \frac{n!}{x^n}\right| = \frac{|x|}{n+1} \to 0 \text{ as } n\to\infty
$$

$L = 0 < 1$ for all $x$ → **Converges for all $x \in (-\infty, \infty)$**, $R = \infty$.

*(This is the power series for $e^x$!)*

---

## Solved Example 2

**Find radius of convergence:** $\displaystyle\sum_{n=0}^{\infty} n!\, x^n$

$$
\left|\frac{a_{n+1}}{a_n}\right| = (n+1)|x| \to \infty \text{ for any } x \neq 0
$$

$R = 0$ — converges **only at $x = 0$**.

---

## Solved Example 3

**Find interval of convergence:** $\displaystyle\sum_{n=1}^{\infty} \frac{x^n}{n}$

$$
L = \lim_{n\to\infty} \left|\frac{x^{n+1}}{n+1} \cdot \frac{n}{x^n}\right| = |x| \lim_{n\to\infty} \frac{n}{n+1} = |x|
$$

Converges when $|x| < 1$, so $R = 1$.

**Check endpoints:**
- $x = 1$: $\sum \frac{1}{n}$ — Harmonic series, **diverges** ✗
- $x = -1$: $\sum \frac{(-1)^n}{n}$ — Alternating harmonic, **converges** ✓

**Interval of convergence:** $[-1, 1)$

---

## Important Maclaurin Series

| Function | Series | Radius |
|----------|--------|--------|
| $e^x$ | $\sum_{n=0}^{\infty} \frac{x^n}{n!}$ | $R = \infty$ |
| $\sin x$ | $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$ | $R = \infty$ |
| $\cos x$ | $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$ | $R = \infty$ |
| $\frac{1}{1-x}$ | $\sum_{n=0}^{\infty} x^n$ | $R = 1$ |
| $\ln(1+x)$ | $\sum_{n=1}^{\infty} \frac{(-1)^{n-1}x^n}{n}$ | $R = 1$ |

---

## Summary

1. Use the **Ratio Test** to find $R$
2. Check **both endpoints** separately
3. The interval of convergence can be open, closed, or half-open
