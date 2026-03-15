---
layout: post
title: "p-Series Test – Convergence, Divergence & Examples"
date: 2026-03-02
description: "Understand the p-Series Test completely — when it converges, when it diverges, and how to apply it with solved examples."
---

The **p-Series** is one of the most fundamental series in mathematics. It forms the backbone of many convergence tests including the Comparison Test and Limit Comparison Test.

---

## Definition

A **p-series** is a series of the form:

$$
\sum_{n=1}^{\infty} \frac{1}{n^p}
$$

where $p$ is a positive real constant.

---

## The p-Series Test

$$
\sum_{n=1}^{\infty} \frac{1}{n^p} \begin{cases} \text{converges} & \text{if } p > 1 \\ \text{diverges} & \text{if } p \leq 1 \end{cases}
$$

---

## Proof (Using Integral Test)

Consider $f(x) = \frac{1}{x^p}$, which is positive, continuous, and decreasing for $x \geq 1$.

**Case 1: $p \neq 1$**

$$
\int_1^{\infty} \frac{1}{x^p}\, dx = \left[\frac{x^{1-p}}{1-p}\right]_1^{\infty}
$$

- If $p > 1$: $1 - p < 0$, so $x^{1-p} \to 0$ as $x \to \infty$. The integral converges to $\frac{1}{p-1}$. ✓
- If $p < 1$: $1 - p > 0$, so $x^{1-p} \to \infty$. The integral diverges. ✗

**Case 2: $p = 1$ (Harmonic Series)**

$$
\int_1^{\infty} \frac{1}{x}\, dx = \ln x \Big|_1^{\infty} = \infty \quad \text{(diverges)}
$$

---

## Important Special Cases

| Series | $p$ value | Result |
|--------|-----------|--------|
| $\sum \frac{1}{n}$ | $p = 1$ | **Diverges** (Harmonic) |
| $\sum \frac{1}{n^2}$ | $p = 2$ | **Converges** ($= \frac{\pi^2}{6}$) |
| $\sum \frac{1}{n^3}$ | $p = 3$ | **Converges** |
| $\sum \frac{1}{\sqrt{n}}$ | $p = \frac{1}{2}$ | **Diverges** |
| $\sum \frac{1}{n^{3/2}}$ | $p = \frac{3}{2}$ | **Converges** |

---

## Solved Examples

**Example 1:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^5}$

$p = 5 > 1$ → **Converges** ✓

---

**Example 2:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^{0.9}}$

$p = 0.9 < 1$ → **Diverges** ✗

---

**Example 3:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{\sqrt[3]{n^2}}= \sum_{n=1}^{\infty} \frac{1}{n^{2/3}}$

$p = \frac{2}{3} < 1$ → **Diverges** ✗

---

**Example 4:** $\displaystyle\sum_{n=1}^{\infty} \frac{4}{n^2}$

This is $4 \cdot \sum \frac{1}{n^2}$, with $p = 2 > 1$ → **Converges** ✓

---

## Key Takeaway

The p-Series Test is your **first tool** to check before applying any other convergence test. Memorize the boundary: $p > 1$ converges, $p \leq 1$ diverges.
