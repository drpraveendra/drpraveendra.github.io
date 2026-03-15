---
layout: post
title: "Alternating Series Test (Leibniz Test) – Explanation & Examples"
date: 2026-03-07
description: "Learn the Alternating Series Test (Leibniz's Test) — conditions for convergence, error estimation, and solved examples with alternating signs."
---

An **alternating series** is one whose terms alternate between positive and negative. The **Alternating Series Test** (Leibniz's Test) gives a simple condition for convergence of such series.

---

## Definition

An alternating series has the form:

$$
\sum_{n=1}^{\infty} (-1)^{n-1} a_n = a_1 - a_2 + a_3 - a_4 + \cdots
$$

or $\sum (-1)^n a_n$, where $a_n > 0$.

---

## Leibniz's Alternating Series Test

The alternating series $\sum (-1)^{n-1} a_n$ **converges** if:

1. $a_n > 0$ for all $n$ (terms are positive)
2. $a_{n+1} \leq a_n$ for all $n$ (terms are **decreasing**)
3. $\lim_{n\to\infty} a_n = 0$ (terms approach **zero**)

---

## Error Estimation

If the series converges to $S$, the error in approximating $S$ by the partial sum $S_N$ satisfies:

$$
|S - S_N| \leq a_{N+1}
$$

The error is at most the **first omitted term**. This is a very useful bound!

---

## Solved Example 1 — Alternating Harmonic Series

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$

Let $a_n = \frac{1}{n}$.

1. $a_n = \frac{1}{n} > 0$ ✓
2. $a_{n+1} = \frac{1}{n+1} < \frac{1}{n} = a_n$ (decreasing) ✓
3. $\lim_{n\to\infty} \frac{1}{n} = 0$ ✓

All three conditions satisfied → series **converges**. ✓

*(Note: The regular harmonic series $\sum \frac{1}{n}$ diverges — alternating makes the difference!)*

---

## Solved Example 2

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{\sqrt{n}}$

Let $a_n = \frac{1}{\sqrt{n}}$.

1. $a_n > 0$ ✓
2. $\frac{1}{\sqrt{n+1}} < \frac{1}{\sqrt{n}}$ (decreasing) ✓
3. $\lim_{n\to\infty} \frac{1}{\sqrt{n}} = 0$ ✓

→ Series **converges**. ✓

---

## Solved Example 3 — Fails Condition 3

**Test:** $\displaystyle\sum_{n=1}^{\infty} (-1)^n \frac{n}{n+1}$

$$
\lim_{n\to\infty} \frac{n}{n+1} = 1 \neq 0
$$

Condition 3 fails → series **diverges** (by the Divergence Test). ✗

---

## Absolute vs Conditional Convergence

- $\sum \frac{(-1)^{n-1}}{n}$ converges (by Alternating Series Test) but $\sum \frac{1}{n}$ diverges.
- So $\sum \frac{(-1)^{n-1}}{n}$ is **conditionally convergent** but **not absolutely convergent**.

$$
\text{Absolutely Convergent} \Rightarrow \text{Convergent}
$$

But the converse is not always true.
