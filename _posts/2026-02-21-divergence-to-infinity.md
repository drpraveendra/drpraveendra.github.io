---
layout: post
title: "Sequences Diverging to Infinity – Definitions, Tests & Examples"
date: 2026-02-21
description: "Understand divergence to +∞ and −∞ in sequences — formal epsilon definitions, comparison test for divergence, and standard sequences that tend to infinity."
---

When a sequence diverges, it may do so in an **ordered way** — growing to $+\infty$ or $-\infty$. This is a structured form of divergence that deserves careful treatment.

---

## Definition: Divergence to $+\infty$

**Definition:** $\{a_n\}$ **diverges to $+\infty$** (written $a_n \to +\infty$) if:

$$\forall\, M > 0,\quad \exists\, N \in \mathbb{N} \text{ such that } \forall\, n > N:\quad a_n > M$$

No matter how large $M$ is, eventually all terms exceed $M$.

---

## Definition: Divergence to $-\infty$

**Definition:** $a_n \to -\infty$ if:

$$\forall\, M > 0,\quad \exists\, N \text{ such that } n > N \implies a_n < -M$$

---

## Examples

### Example 1: $a_n = n \to +\infty$

Given $M > 0$, choose $N = \lceil M \rceil$. For $n > N$: $a_n = n > N \geq M$. ✓

### Example 2: $a_n = n^2 \to +\infty$

Given $M > 0$, choose $N = \lceil\sqrt{M}\rceil$. For $n > N$: $n^2 > M$. ✓

### Example 3: $a_n = \sqrt{n} \to +\infty$

Choose $N = \lceil M^2 \rceil$. For $n > N$: $\sqrt{n} > M$. ✓

### Example 4: $a_n = \ln n \to +\infty$

Choose $N = \lceil e^M \rceil$. For $n > N$: $\ln n > M$. ✓ (But very slowly!)

### Example 5: $a_n = -n^2 \to -\infty$ ✓

---

## Comparison Test for Divergence to $\infty$

**Theorem:** If $a_n \leq b_n$ for all large $n$ and $a_n \to +\infty$, then $b_n \to +\infty$.

**Example:** Since $\ln n \to \infty$ and $n \geq \ln n$, we have $n \to \infty$ — obvious but confirms the principle.

---

## Rate of Growth Comparison

$$\ln n \ll n^p \ll a^n \ll n! \ll n^n \quad (p > 0,\; a > 1)$$

This means each grows infinitely faster than the previous:

$$\lim_{n\to\infty} \frac{\ln n}{n^p} = 0,\quad \lim_{n\to\infty} \frac{n^p}{a^n} = 0,\quad \lim_{n\to\infty} \frac{a^n}{n!} = 0$$

These are the most important rate comparisons in analysis.

---

## Sequences That Are Unbounded but Don't Diverge to $\pm\infty$

**Example:** $a_n = (-1)^n \cdot n$

- Unbounded ✓
- Does NOT diverge to $+\infty$ or $-\infty$ (oscillates between $\pm\infty$)

---

## Properties of Sequences Tending to $\infty$

If $a_n \to +\infty$ and $b_n \to +\infty$:

1. $a_n + b_n \to +\infty$
2. $a_n \cdot b_n \to +\infty$
3. $\frac{1}{a_n} \to 0$

If $a_n \to +\infty$ and $b_n \to L > 0$:

4. $a_n \cdot b_n \to +\infty$

**Warning (Indeterminate forms):**
- $a_n - b_n$ when both $\to \infty$: could be $0$, $\infty$, or finite
- $\frac{a_n}{b_n}$ when both $\to \infty$: depends on rates

---

## Classic Indeterminate Form

**Example:** $a_n = n^2 - n$

Both $n^2 \to \infty$ and $n \to \infty$, but:

$$n^2 - n = n(n-1) \to +\infty$$

**Example:** $a_n = \sqrt{n+1} - \sqrt{n}$

Both terms $\to \infty$, but rationalizing:

$$\sqrt{n+1} - \sqrt{n} = \frac{1}{\sqrt{n+1}+\sqrt{n}} \to 0$$

Always rationalize or factor before concluding!
