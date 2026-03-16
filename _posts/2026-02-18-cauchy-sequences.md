---
layout: post
title: "Cauchy Sequences – Definition, Properties & Completeness of ℝ"
date: 2026-02-18
description: "Understand Cauchy sequences — definition, the equivalence between Cauchy and convergent sequences in ℝ, and why this fails in ℚ. Includes proofs and examples."
---

**Cauchy sequences** provide a way to discuss convergence without knowing the limit in advance. In $\mathbb{R}$, they are equivalent to convergent sequences — a reflection of the completeness of $\mathbb{R}$.

---

## Definition

**Definition:** A sequence $\{a_n\}$ is a **Cauchy sequence** if:

$$
\forall\, \varepsilon > 0,\quad \exists\, N \in \mathbb{N} \text{ such that } \forall\, m, n > N:\quad |a_m - a_n| < \varepsilon
$$

The terms become arbitrarily close to **each other** — we don't need to specify a limit.

---

## Cauchy $\iff$ Convergent in $\mathbb{R}$

**Theorem:** A sequence of real numbers is convergent $\iff$ it is a Cauchy sequence.

---

## Proof: Convergent $\implies$ Cauchy

Let $a_n \to L$. Given $\varepsilon > 0$, $\exists\, N: n > N \implies |a_n - L| < \frac{\varepsilon}{2}$.

For $m, n > N$:

$$|a_m - a_n| \leq |a_m - L| + |L - a_n| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \quad \blacksquare$$

---

## Proof: Cauchy $\implies$ Convergent in $\mathbb{R}$

**Step 1:** Cauchy $\implies$ Bounded.

Take $\varepsilon = 1$: $\exists\, N: m,n > N \implies |a_m - a_n| < 1$. In particular, $|a_n| < |a_{N+1}| + 1$ for $n > N$.

Let $M = \max\{|a_1|, \ldots, |a_N|, |a_{N+1}|+1\}$. Then $|a_n| \leq M$ for all $n$.

**Step 2:** By Bolzano-Weierstrass, $\{a_n\}$ has a convergent subsequence $a_{n_k} \to L$.

**Step 3:** Since $\{a_n\}$ is Cauchy:

$$|a_n - L| \leq |a_n - a_{n_k}| + |a_{n_k} - L| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon$$

for large enough $n, k$. So $a_n \to L$. $\blacksquare$

---

## Examples

### Example 1 — Cauchy Sequence

$a_n = \frac{1}{n}$: For $m, n > N = \lceil\frac{2}{\varepsilon}\rceil$:

$$|a_m - a_n| = \left|\frac{1}{m} - \frac{1}{n}\right| \leq \frac{1}{m} + \frac{1}{n} < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \checkmark$$

---

### Example 2 — Not Cauchy

$a_n = (-1)^n$: Take $m = 2k$, $n = 2k-1$:

$$|a_m - a_n| = |1 - (-1)| = 2 \not< \varepsilon \text{ for } \varepsilon \leq 2$$

Not Cauchy → diverges. ✓

---

### Example 3 — Cauchy in $\mathbb{Q}$ but NOT convergent in $\mathbb{Q}$

The sequence $x_1 = 1$, $x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n}$ (Newton-Raphson for $\sqrt{2}$) is Cauchy in $\mathbb{Q}$ but converges to $\sqrt{2} \notin \mathbb{Q}$.

This shows $\mathbb{Q}$ is **not complete**. In $\mathbb{R}$, it converges to $\sqrt{2}$.

---

## Cauchy Criterion for Series

A series $\sum a_n$ converges $\iff$ its partial sums form a Cauchy sequence:

$$\forall\, \varepsilon > 0,\; \exists\, N: m > n > N \implies \left|\sum_{k=n+1}^m a_k\right| < \varepsilon$$

---

## Summary

| Property | $\mathbb{Q}$ | $\mathbb{R}$ |
|----------|------------|------------|
| Cauchy $\implies$ Convergent | ✗ | ✓ |
| Convergent $\implies$ Cauchy | ✓ | ✓ |

The equivalence in $\mathbb{R}$ is precisely what it means for $\mathbb{R}$ to be **complete**.
