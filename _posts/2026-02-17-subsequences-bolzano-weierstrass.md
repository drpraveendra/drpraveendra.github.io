---
layout: post
title: "Subsequences & Bolzano-Weierstrass Theorem – Complete Guide"
date: 2026-02-17
description: "Learn about subsequences, the Bolzano-Weierstrass theorem, and limit superior/inferior — fundamental tools for analyzing divergent and bounded sequences."
---

**Subsequences** allow us to extract convergent patterns from divergent sequences. The **Bolzano-Weierstrass theorem** guarantees this is always possible for bounded sequences.

---

## Subsequences

**Definition:** A **subsequence** of $\{a_n\}$ is a sequence $\{a_{n_k}\}$ where:

$$n_1 < n_2 < n_3 < \cdots$$

is a strictly increasing sequence of natural numbers.

---

## Key Theorem on Subsequences

**Theorem:** If $a_n \to L$, then **every subsequence** $a_{n_k} \to L$.

**Proof:** Given $\varepsilon > 0$, $\exists\, N: n > N \implies |a_n - L| < \varepsilon$.

Since $n_k \geq k$ (strictly increasing), for $k > N$: $n_k \geq k > N \implies |a_{n_k} - L| < \varepsilon$. $\blacksquare$

**Contrapositive:** If some subsequence diverges, or two subsequences converge to different limits, then $\{a_n\}$ **diverges**.

---

## Using Subsequences to Prove Divergence

**Example:** $a_n = (-1)^n$

- Odd-indexed subsequence: $a_{2k-1} = -1 \to -1$
- Even-indexed subsequence: $a_{2k} = 1 \to 1$

Two subsequences converge to different limits → $\{(-1)^n\}$ **diverges**. ✓

---

## Bolzano-Weierstrass Theorem

**Theorem:** Every **bounded** sequence has a **convergent subsequence**.

**Proof (Bisection method):** Let $\{a_n\} \subseteq [a,b]$. Bisect $[a,b]$: at least one half contains infinitely many terms. Call it $[a_1,b_1]$.

Repeat: bisect $[a_1,b_1]$, take the half with infinitely many terms → $[a_2,b_2]$.

This gives nested intervals $[a_k,b_k]$ with $b_k - a_k = \frac{b-a}{2^k} \to 0$.

By nested interval property, $\bigcap [a_k,b_k] = \{L\}$. Pick $n_k$ with $a_{n_k} \in [a_k,b_k]$. Then $a_{n_k} \to L$. $\blacksquare$

---

## Limit Superior and Limit Inferior

For a bounded sequence $\{a_n\}$:

$$\limsup_{n\to\infty} a_n = \lim_{n\to\infty} \sup_{k \geq n} a_k = \inf_n \sup_{k\geq n} a_k$$

$$\liminf_{n\to\infty} a_n = \lim_{n\to\infty} \inf_{k \geq n} a_k = \sup_n \inf_{k\geq n} a_k$$

---

## Properties of $\limsup$ and $\liminf$

1. $\liminf\, a_n \leq \limsup\, a_n$ always
2. $\lim a_n = L \iff \liminf\, a_n = \limsup\, a_n = L$
3. $\limsup(-a_n) = -\liminf\, a_n$

---

## Examples

**$a_n = (-1)^n$:**

$$\limsup = 1, \quad \liminf = -1$$

Since $\limsup \neq \liminf$, the sequence diverges. ✓

---

**$a_n = (-1)^n + \frac{1}{n}$:**

$$\limsup = \lim(1 + \frac{1}{2k}) = 1, \quad \liminf = \lim(-1 + \frac{1}{2k-1}) = -1$$

Diverges. ✓

---

**$a_n = \frac{n+(-1)^n}{n}= 1 + \frac{(-1)^n}{n}$:**

$$\limsup = 1, \quad \liminf = 1 \implies a_n \to 1$$

---

## Cluster Points

A value $c$ is a **cluster point** (subsequential limit) of $\{a_n\}$ if some subsequence converges to $c$.

**Theorem:** $\limsup\, a_n$ is the **largest** cluster point; $\liminf\, a_n$ is the **smallest** cluster point.
