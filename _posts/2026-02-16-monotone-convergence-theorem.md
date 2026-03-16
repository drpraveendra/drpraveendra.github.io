---
layout: post
title: "Monotone Convergence Theorem – Statement, Proof & Applications"
date: 2026-02-16
description: "Learn the Monotone Convergence Theorem — one of the most useful tools for proving convergence without finding the limit first. Includes proof and classic applications."
---

The **Monotone Convergence Theorem** (MCT) is one of the most powerful tools in sequence analysis. It allows you to prove a sequence converges without knowing its limit in advance.

---

## Statement

**Theorem (Monotone Convergence Theorem):**

1. If $\{a_n\}$ is **increasing** and **bounded above**, then $\{a_n\}$ converges and:
$$\lim_{n\to\infty} a_n = \sup\{a_n : n \in \mathbb{N}\}$$

2. If $\{a_n\}$ is **decreasing** and **bounded below**, then $\{a_n\}$ converges and:
$$\lim_{n\to\infty} a_n = \inf\{a_n : n \in \mathbb{N}\}$$

---

## Proof (Case 1: Increasing & Bounded Above)

Let $L = \sup\{a_n\}$ — exists by the Completeness Axiom.

Let $\varepsilon > 0$. Since $L - \varepsilon$ is not an upper bound, $\exists\, N: a_N > L - \varepsilon$.

Since $\{a_n\}$ is increasing, for all $n > N$:

$$L - \varepsilon < a_N \leq a_n \leq L$$

$$\implies |a_n - L| < \varepsilon$$

So $a_n \to L$. $\blacksquare$

---

## Example 1 — Classic Application

**Show $a_n = \left(1 + \frac{1}{n}\right)^n$ converges.**

**Step 1 (Increasing):** By AM-GM inequality, $a_{n+1} \geq a_n$. ✓

**Step 2 (Bounded above):** Using the binomial theorem:

$$a_n = \sum_{k=0}^n \binom{n}{k} \frac{1}{n^k} \leq \sum_{k=0}^n \frac{1}{k!} \leq \sum_{k=0}^{\infty} \frac{1}{k!} = e < 3$$

By MCT, $\{a_n\}$ converges. Its limit is defined as $e \approx 2.71828$. ✓

---

## Example 2 — Recursive Sequence

**Show $a_1 = 1$, $a_{n+1} = \sqrt{2 + a_n}$ converges and find its limit.**

**Step 1 (Bounded above by 2):** By induction — if $a_n \leq 2$, then $a_{n+1} = \sqrt{2+a_n} \leq \sqrt{4} = 2$. ✓

**Step 2 (Increasing):** $a_{n+1} - a_n = \sqrt{2+a_n} - a_n > 0$ when $a_n < 2$ (verify algebraically). ✓

By MCT, $\lim a_n = L$ exists. Taking limits on both sides of $a_{n+1} = \sqrt{2+a_n}$:

$$L = \sqrt{2 + L} \implies L^2 = 2 + L \implies L^2 - L - 2 = 0 \implies (L-2)(L+1) = 0$$

Since $a_n > 0$, we have $L = 2$. ✓

---

## Example 3

**$a_n = \frac{n}{n+1}$**: increasing, bounded above by 1 → converges to 1. ✓

**$a_n = \frac{1}{2^n}$**: decreasing, bounded below by 0 → converges to 0. ✓

---

## When MCT Cannot Be Applied

- $a_n = (-1)^n$: bounded but NOT monotone → MCT doesn't apply (and sequence diverges)
- $a_n = n$: increasing but NOT bounded above → MCT doesn't apply (diverges to $\infty$)

---

## Key Takeaway

MCT is ideal for sequences defined recursively. The strategy is:
1. Prove monotonicity (often by induction)
2. Prove boundedness (often by induction)
3. Conclude convergence by MCT
4. Find the limit by solving $L = f(L)$
