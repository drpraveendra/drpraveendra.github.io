---
layout: post
title: "Absolute & Conditional Convergence – Definitions & Key Examples"
date: 2026-03-10
description: "Understand the difference between absolute and conditional convergence with clear definitions, theorems, and classic examples including the alternating harmonic series."
---

When dealing with series that have both positive and negative terms, we distinguish between two types of convergence: **absolute** and **conditional**.

---

## Definitions

**Absolute Convergence:**
A series $\sum a_n$ is **absolutely convergent** if $\sum |a_n|$ converges.

**Conditional Convergence:**
A series $\sum a_n$ is **conditionally convergent** if $\sum a_n$ converges but $\sum |a_n|$ diverges.

---

## Key Theorem

$$
\text{Absolutely Convergent} \implies \text{Convergent}
$$

If a series converges absolutely, it must converge. But not every convergent series converges absolutely.

---

## Example 1 — Absolute Convergence

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n^2}$

Check $\sum |a_n| = \sum \frac{1}{n^2}$ — this is a p-series with $p=2>1$, which **converges**.

Therefore $\sum \frac{(-1)^n}{n^2}$ is **absolutely convergent**. ✓

---

## Example 2 — Conditional Convergence

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \cdots$

**Step 1:** Check absolute convergence: $\sum \frac{1}{n}$ is the harmonic series — **diverges**. So NOT absolutely convergent.

**Step 2:** Check convergence: By Leibniz's Alternating Series Test:
- $a_n = \frac{1}{n} > 0$ ✓
- Decreasing ✓
- $\frac{1}{n} \to 0$ ✓

→ Series **converges conditionally**. ✓

---

## Example 3 — Neither

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n n}{n+1}$

$$
\lim_{n\to\infty} \frac{n}{n+1} = 1 \neq 0
$$

By the Divergence Test, the series **diverges** — neither absolutely nor conditionally convergent. ✗

---

## Riemann's Rearrangement Theorem

This is a famous and surprising result:

> A **conditionally convergent** series can be rearranged to converge to **any real number**, or even to $\pm\infty$.

For example, the alternating harmonic series $\sum \frac{(-1)^{n-1}}{n}$ converges to $\ln 2 \approx 0.693$. But by rearranging terms, you can make it converge to $5$, $-3$, or any number you like!

**Absolutely convergent** series do not have this problem — any rearrangement gives the same sum.

---

## Classification Summary

| Type | $\sum a_n$ | $\sum \|a_n\|$ |
|------|-----------|-------------|
| Absolutely convergent | Converges | Converges |
| Conditionally convergent | Converges | **Diverges** |
| Divergent | Diverges | May diverge |

---

## Testing Strategy

1. First test $\sum |a_n|$ — if it converges → **absolutely convergent** (done)
2. If $\sum |a_n|$ diverges, test $\sum a_n$ directly (e.g., Alternating Series Test)
3. If $\sum a_n$ converges but $\sum |a_n|$ diverges → **conditionally convergent**
