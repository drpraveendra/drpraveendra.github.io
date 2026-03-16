---
layout: post
title: "Dirichlet's Test & Abel's Test – Advanced Convergence Tests"
date: 2026-03-16
description: "Learn Dirichlet's Test and Abel's Test for series convergence — two powerful tests for series with products of sequences. Includes full statements and examples."
---

**Dirichlet's Test** and **Abel's Test** are advanced convergence tests used when a series is a product of two sequences. They are especially important for CSIR NET and GATE examinations.

---

## Dirichlet's Test

**Statement:** Let $\sum a_n b_n$ be a series where:
1. The partial sums $A_N = \sum_{n=1}^N a_n$ are **bounded** (i.e., $|A_N| \leq M$ for all $N$)
2. $b_n$ is **monotonically decreasing** to zero: $b_n \searrow 0$

Then $\sum a_n b_n$ **converges**.

---

### Application: Alternating Series Test is a Special Case

If $a_n = (-1)^{n-1}$, then $A_N$ alternates between 0 and 1 — **bounded**. If $b_n \searrow 0$, Dirichlet's Test gives convergence. This is exactly the Alternating Series Test!

---

### Solved Example 1

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{\sin n}{n}$

Let $a_n = \sin n$ and $b_n = \frac{1}{n}$.

**Step 1:** Bound partial sums of $\sin n$. Using the formula:

$$
\left|\sum_{n=1}^N \sin n\right| = \left|\frac{\sin\frac{N+1}{2} \cdot \sin\frac{N}{2}}{\sin\frac{1}{2}}\right| \leq \frac{1}{\sin\frac{1}{2}} \approx 2.09
$$

So partial sums are bounded. ✓

**Step 2:** $b_n = \frac{1}{n}$ is decreasing to 0. ✓

By Dirichlet's Test → series **converges**. ✓

---

### Solved Example 2

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{\cos n\theta}{n}$ for $\theta \neq 2k\pi$

Similarly, partial sums of $\cos n\theta$ are bounded when $\theta \neq 2k\pi$, and $\frac{1}{n} \searrow 0$.

→ Series **converges**. ✓

---

## Abel's Test

**Statement:** Let $\sum a_n b_n$ be a series where:
1. $\sum a_n$ **converges**
2. $\{b_n\}$ is **monotone and bounded**

Then $\sum a_n b_n$ **converges**.

---

### Solved Example 3

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n} \cdot \left(1 + \frac{1}{n}\right)$

Let $a_n = \frac{(-1)^n}{n}$ and $b_n = 1 + \frac{1}{n}$.

- $\sum a_n = \sum \frac{(-1)^n}{n}$ converges (alternating harmonic). ✓
- $b_n = 1 + \frac{1}{n}$ is **decreasing** and **bounded** (between 1 and 2). ✓

By Abel's Test → series **converges**. ✓

---

## Comparison of the Two Tests

| Feature | Dirichlet's Test | Abel's Test |
|---------|-----------------|-------------|
| Condition on $a_n$ | Partial sums **bounded** | $\sum a_n$ **converges** |
| Condition on $b_n$ | $b_n \searrow 0$ | $b_n$ monotone & **bounded** |
| More general | Yes | No (Abel is a consequence) |

**Abel's Test follows from Dirichlet's Test** — if $\sum a_n$ converges, its partial sums are bounded, and if $b_n$ is bounded and monotone, $b_n \to L$, so $b_n - L \searrow 0$.

---

## Key Takeaway

Use **Dirichlet's Test** for products like $\frac{\sin n}{n}$, $\frac{\cos n\theta}{n^p}$.
Use **Abel's Test** when $\sum a_n$ already converges and $b_n$ is a bounded monotone modifier.
