---
layout: post
title: "Cauchy Condensation Test – Statement, Proof & Examples"
date: 2026-03-14
description: "Learn the Cauchy Condensation Test — a powerful but lesser-known convergence test that works beautifully for logarithmic and slowly-decaying series."
---

The **Cauchy Condensation Test** is a powerful and elegant convergence test, especially useful for series involving **logarithms** where the Integral Test might be more complex.

---

## Statement of the Test

Let $f(n)$ be a **non-negative, decreasing** sequence. Then:

$$
\sum_{n=1}^{\infty} f(n) \quad \text{and} \quad \sum_{n=0}^{\infty} 2^n f(2^n)
$$

**both converge or both diverge.**

---

## Intuition

The condensation test "compresses" a slow series by sampling only at powers of 2. Since $f$ is decreasing, the behavior at $2^n$ captures the overall growth rate.

---

## Solved Example 1 — p-Series (Re-derived)

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^p}$

Apply condensation: $f(n) = \frac{1}{n^p}$, so $f(2^n) = \frac{1}{2^{np}}$.

$$
\sum_{n=0}^{\infty} 2^n \cdot \frac{1}{2^{np}} = \sum_{n=0}^{\infty} 2^n \cdot 2^{-np} = \sum_{n=0}^{\infty} 2^{n(1-p)} = \sum_{n=0}^{\infty} \left(2^{1-p}\right)^n
$$

This is a geometric series with ratio $r = 2^{1-p}$:
- Converges if $r < 1$, i.e., $1-p < 0$, i.e., $p > 1$
- Diverges if $r \geq 1$, i.e., $p \leq 1$

This gives the **p-Series Test** directly from the Condensation Test! ✓

---

## Solved Example 2 — Logarithmic Series

**Test:** $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n \ln n}$

$f(n) = \frac{1}{n \ln n}$, so $f(2^n) = \frac{1}{2^n \cdot n \ln 2}$.

$$
\sum_{n=1}^{\infty} 2^n \cdot \frac{1}{2^n \cdot n \ln 2} = \sum_{n=1}^{\infty} \frac{1}{n \ln 2} = \frac{1}{\ln 2} \sum_{n=1}^{\infty} \frac{1}{n}
$$

Since $\sum \frac{1}{n}$ diverges, the condensed series diverges → original series **diverges**. ✗

---

## Solved Example 3

**Test:** $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n (\ln n)^2}$

$f(2^n) = \frac{1}{2^n (n \ln 2)^2}$

$$
\sum_{n=1}^{\infty} 2^n \cdot \frac{1}{2^n n^2 (\ln 2)^2} = \frac{1}{(\ln 2)^2} \sum_{n=1}^{\infty} \frac{1}{n^2}
$$

Since $\sum \frac{1}{n^2}$ converges, the series **converges**. ✓

---

## Comparison: Logarithmic Series

| Series | Result |
|--------|--------|
| $\sum \frac{1}{n \ln n}$ | **Diverges** |
| $\sum \frac{1}{n (\ln n)^2}$ | **Converges** |
| $\sum \frac{1}{n \ln n \cdot \ln(\ln n)}$ | **Diverges** |

These results show how fine the boundary between convergence and divergence can be!

---

## When to Use This Test

- Series involving $\ln n$ where the Integral Test is messy
- When you want an alternative derivation of p-Series behavior
- For series of the form $\frac{1}{n (\ln n)^p}$
