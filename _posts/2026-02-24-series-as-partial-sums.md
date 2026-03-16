---
layout: post
title: "Infinite Series as Sequences of Partial Sums – The Bridge to Series"
date: 2026-02-24
description: "Understand how infinite series are defined as sequences of partial sums — convergence of series via sequences, Cauchy criterion for series, and key examples."
---

An **infinite series** is not just an endless sum — it is rigorously defined as the **limit of a sequence of partial sums**. This connection between sequences and series is fundamental.

---

## Definition

Given a sequence $\{a_n\}$, define the **$N$-th partial sum**:

$$S_N = \sum_{n=1}^{N} a_n = a_1 + a_2 + \cdots + a_N$$

The **infinite series** $\displaystyle\sum_{n=1}^{\infty} a_n$ **converges** to $S$ if:

$$\lim_{N\to\infty} S_N = S$$

Otherwise the series **diverges**.

---

## The Series IS the Sequence $\{S_N\}$

All convergence theorems for sequences apply directly to series via their partial sums:

| Series concept | Sequence equivalent |
|---------------|-------------------|
| Series converges | $\{S_N\}$ converges |
| Series diverges | $\{S_N\}$ diverges |
| Sum of series $= S$ | $\lim S_N = S$ |
| Series is Cauchy | $\{S_N\}$ is Cauchy |

---

## Telescoping via Partial Sums

**Example:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$

$$S_N = \sum_{n=1}^N \left(\frac{1}{n} - \frac{1}{n+1}\right) = 1 - \frac{1}{N+1}$$

$$\lim_{N\to\infty} S_N = 1 \quad \checkmark$$

---

## Geometric Series via Partial Sums

**Example:** $\displaystyle\sum_{n=0}^{\infty} r^n$, $|r| < 1$

$$S_N = \frac{1 - r^{N+1}}{1-r}$$

Since $r^{N+1} \to 0$:

$$\lim_{N\to\infty} S_N = \frac{1}{1-r} \quad \checkmark$$

---

## Harmonic Series via Partial Sums

**Example:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n}$

$$S_N = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{N}$$

We showed $\{S_N\}$ is unbounded → $S_N \to \infty$ → series **diverges**. ✗

---

## Cauchy Criterion for Series

**Theorem:** $\displaystyle\sum a_n$ converges $\iff$ $\{S_N\}$ is Cauchy $\iff$:

$$\forall\, \varepsilon > 0,\;\exists\, N: m > n > N \implies \left|\sum_{k=n+1}^{m} a_k\right| < \varepsilon$$

---

## Necessary Condition: $a_n \to 0$

**Theorem:** If $\sum a_n$ converges, then $a_n \to 0$.

**Proof:** $a_n = S_n - S_{n-1} \to S - S = 0$. $\blacksquare$

**Warning:** $a_n \to 0$ does NOT guarantee convergence (Harmonic series!).

---

## Absolute Convergence via Partial Sums

$\sum a_n$ is **absolutely convergent** if $\{T_N\} = \left\{\sum_{n=1}^N |a_n|\right\}$ converges.

Since $\{T_N\}$ is increasing, it converges $\iff$ it is bounded above.

**Theorem:** Absolute convergence $\implies$ convergence.

**Proof:** $|S_m - S_n| \leq \sum_{k=n+1}^m |a_k| = T_m - T_n \to 0$ (Cauchy). $\blacksquare$

---

## Example: Comparing $\sum a_n$ and $\sum |a_n|$ via Partial Sums

| Series | $\{S_N\}$ | $\{T_N\}$ | Type |
|--------|-----------|-----------|------|
| $\sum \frac{(-1)^n}{n}$ | Converges | Diverges | Conditional |
| $\sum \frac{(-1)^n}{n^2}$ | Converges | Converges | Absolute |
| $\sum \frac{1}{n}$ | Diverges | Diverges | Diverges |

The partial sum sequence $\{S_N\}$ is the rigorous foundation for everything in series theory.
