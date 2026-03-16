---
layout: post
title: "Convergence of Real Sequences – Epsilon Definition, Uniqueness & Examples"
date: 2026-02-15
description: "Master the epsilon definition of convergence of real sequences — uniqueness of limits, divergence, and detailed step-by-step examples using the definition."
---

**Convergence** is the most important concept in the study of sequences. A sequence converges if its terms get arbitrarily close to a fixed value — made precise by the $\varepsilon$-definition.

---

## Definition of Convergence

**Definition:** A sequence $\{a_n\}$ **converges to** $L \in \mathbb{R}$ if:

$$
\forall\, \varepsilon > 0,\quad \exists\, N \in \mathbb{N} \text{ such that } \forall\, n > N:\quad |a_n - L| < \varepsilon
$$

We write $a_n \to L$ or $\lim_{n\to\infty} a_n = L$.

**Interpretation:** For any tolerance $\varepsilon$, all terms after the $N$-th are within $\varepsilon$ of $L$.

---

## Uniqueness of Limits

**Theorem:** If $\{a_n\}$ converges, its limit is **unique**.

**Proof:** Suppose $a_n \to L$ and $a_n \to M$. Let $\varepsilon > 0$.

$\exists\, N_1: n > N_1 \implies |a_n - L| < \frac{\varepsilon}{2}$

$\exists\, N_2: n > N_2 \implies |a_n - M| < \frac{\varepsilon}{2}$

For $n > \max(N_1, N_2)$:

$$|L - M| \leq |L - a_n| + |a_n - M| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon$$

Since $\varepsilon > 0$ was arbitrary, $|L - M| = 0$, so $L = M$. $\blacksquare$

---

## Proving Convergence Using the Definition

### Example 1: $a_n = \frac{1}{n} \to 0$

**Claim:** $\lim_{n\to\infty} \frac{1}{n} = 0$.

**Proof:** Let $\varepsilon > 0$. Choose $N > \frac{1}{\varepsilon}$ (by Archimedean property).

For $n > N$: $|a_n - 0| = \frac{1}{n} < \frac{1}{N} < \varepsilon$. $\blacksquare$

---

### Example 2: $a_n = \frac{2n+1}{n+3} \to 2$

**Proof:** $|a_n - 2| = \left|\frac{2n+1}{n+3} - 2\right| = \left|\frac{-5}{n+3}\right| = \frac{5}{n+3} < \frac{5}{n}$

Given $\varepsilon > 0$, choose $N > \frac{5}{\varepsilon}$. Then $n > N \implies |a_n - 2| < \frac{5}{n} < \varepsilon$. $\blacksquare$

---

### Example 3: $a_n = \frac{n^2 - 1}{n^2 + 1} \to 1$

$|a_n - 1| = \left|\frac{n^2-1}{n^2+1} - 1\right| = \frac{2}{n^2+1} < \frac{2}{n^2} < \frac{2}{n}$

Choose $N > \frac{2}{\varepsilon}$. Then for $n > N$: $|a_n - 1| < \varepsilon$. $\blacksquare$

---

## Divergent Sequences

A sequence is **divergent** if it does not converge to any real number.

**Types of divergence:**

1. **Diverges to $+\infty$:** $a_n = n$ — terms grow without bound
2. **Diverges to $-\infty$:** $a_n = -n$
3. **Oscillates:** $a_n = (-1)^n$ — terms bounce between $-1$ and $1$

---

## Convergent $\implies$ Bounded

**Theorem:** If $\{a_n\}$ converges, then $\{a_n\}$ is **bounded**.

**Proof:** Let $a_n \to L$. Take $\varepsilon = 1$. $\exists\, N: n > N \implies |a_n - L| < 1 \implies |a_n| < |L| + 1$.

Let $M = \max\{|a_1|, |a_2|, \ldots, |a_N|, |L|+1\}$. Then $|a_n| \leq M$ for all $n$. $\blacksquare$

**Warning:** The converse is FALSE. $a_n = (-1)^n$ is bounded but diverges.

---

## Limit Laws

If $a_n \to L$ and $b_n \to M$, then:

$$a_n + b_n \to L + M$$
$$a_n \cdot b_n \to L \cdot M$$
$$\frac{a_n}{b_n} \to \frac{L}{M} \quad (M \neq 0)$$
$$|a_n| \to |L|$$
$$\sqrt{a_n} \to \sqrt{L} \quad (a_n \geq 0)$$
