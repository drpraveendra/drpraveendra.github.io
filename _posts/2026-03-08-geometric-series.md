---
layout: post
title: "Geometric Series – Convergence, Sum Formula & Applications"
date: 2026-03-08
description: "Complete guide to geometric series — convergence condition, exact sum formula, and real-world applications with solved examples."
---

The **Geometric Series** is the most important series in mathematics. Its sum formula is used everywhere — from calculus to finance to physics.

---

## Definition

A geometric series is:

$$
\sum_{n=0}^{\infty} ar^n = a + ar + ar^2 + ar^3 + \cdots
$$

where $a$ is the first term and $r$ is the **common ratio**.

---

## Convergence Condition & Sum Formula

$$
\sum_{n=0}^{\infty} ar^n = \begin{cases} \dfrac{a}{1-r} & \text{if } |r| < 1 \\ \text{diverges} & \text{if } |r| \geq 1 \end{cases}
$$

---

## Derivation of the Sum Formula

Let $S = a + ar + ar^2 + \cdots$

Multiply both sides by $r$:

$$rS = ar + ar^2 + ar^3 + \cdots$$

Subtract:

$$S - rS = a \implies S(1-r) = a \implies S = \frac{a}{1-r}$$

This works only when $|r| < 1$ (so the series doesn't blow up).

---

## Solved Example 1

**Find the sum:** $\displaystyle\sum_{n=0}^{\infty} \frac{1}{3^n}$

$a = 1$, $r = \frac{1}{3}$, $|r| < 1$ ✓

$$
S = \frac{1}{1 - \frac{1}{3}} = \frac{1}{\frac{2}{3}} = \frac{3}{2}
$$

---

## Solved Example 2

**Find the sum:** $\displaystyle\sum_{n=1}^{\infty} \frac{2}{5^n}$

Rewrite: $\displaystyle\sum_{n=1}^{\infty} 2 \cdot \left(\frac{1}{5}\right)^n = 2\sum_{n=1}^{\infty}\left(\frac{1}{5}\right)^n$

This starts at $n=1$, so $a = \frac{1}{5}$, $r = \frac{1}{5}$:

$$
S = 2 \cdot \frac{\frac{1}{5}}{1 - \frac{1}{5}} = 2 \cdot \frac{\frac{1}{5}}{\frac{4}{5}} = 2 \cdot \frac{1}{4} = \frac{1}{2}
$$

---

## Solved Example 3 — Repeating Decimal

**Express $0.\overline{3} = 0.333\ldots$ as a fraction.**

$$
0.333\ldots = \frac{3}{10} + \frac{3}{100} + \frac{3}{1000} + \cdots = \sum_{n=1}^{\infty} \frac{3}{10^n}
$$

$a = \frac{3}{10}$, $r = \frac{1}{10}$:

$$
S = \frac{\frac{3}{10}}{1 - \frac{1}{10}} = \frac{\frac{3}{10}}{\frac{9}{10}} = \frac{3}{9} = \frac{1}{3}
$$

---

## Solved Example 4 — Divergence

**Test:** $\displaystyle\sum_{n=0}^{\infty} \left(\frac{4}{3}\right)^n$

$r = \frac{4}{3}$, $|r| = \frac{4}{3} > 1$ → **Diverges**. ✗

---

## Key Formula to Remember

$$
\boxed{\sum_{n=0}^{\infty} ar^n = \frac{a}{1-r}, \quad |r| < 1}
$$

This is one of the most frequently used formulas in all of analysis.
