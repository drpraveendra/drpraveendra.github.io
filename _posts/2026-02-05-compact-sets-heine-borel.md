---
layout: post
title: "Compact Sets in ℝ – Heine-Borel Theorem & Properties"
date: 2026-02-05
description: "Understand compactness in ℝ — open cover definition, the Heine-Borel theorem, sequential compactness, and why compact sets are so important in analysis."
---

**Compactness** is one of the most powerful and important concepts in topology and analysis. In $\mathbb{R}$, it has a beautifully simple characterization.

---

## Open Cover

**Definition:** An **open cover** of a set $S \subseteq \mathbb{R}$ is a collection $\{G_\alpha\}$ of open sets such that:

$$
S \subseteq \bigcup_\alpha G_\alpha
$$

A **subcover** is a subcollection that still covers $S$. A **finite subcover** is a subcover with finitely many sets.

---

## Compact Set — Definition

**Definition:** A set $K \subseteq \mathbb{R}$ is **compact** if every open cover of $K$ has a **finite subcover**.

---

## Heine-Borel Theorem

This is the most important theorem about compactness in $\mathbb{R}$:

**Theorem:** A subset $K \subseteq \mathbb{R}$ is compact $\iff$ $K$ is **closed and bounded**.

This makes checking compactness in $\mathbb{R}$ extremely simple!

---

## Examples

**Compact:**
- $[a, b]$ — closed and bounded ✓
- $\{1, 2, 3, \ldots, n\}$ — finite sets are always compact ✓
- $\left[\frac{1}{n}, 2\right]$ for any fixed $n$ ✓

**Not Compact:**
- $(0, 1)$ — not closed ✗
- $[0, \infty)$ — not bounded ✗
- $\mathbb{R}$ — not bounded ✗
- $\mathbb{Z}$ — not bounded ✗

---

## Sequential Compactness

**Theorem:** $K$ is compact $\iff$ every sequence in $K$ has a subsequence that converges to a point **in $K$**.

This is called **sequential compactness**, and in $\mathbb{R}$ it is equivalent to the open cover definition.

**Example:** $K = [0, 1]$. Take any sequence $\{x_n\} \subseteq [0,1]$. Since it is bounded, by Bolzano-Weierstrass it has a convergent subsequence. The limit must be in $[0,1]$ since $[0,1]$ is closed. ✓

---

## Properties of Compact Sets

1. Every compact set is **closed and bounded**
2. Every **closed subset** of a compact set is compact
3. **Finite union** of compact sets is compact
4. **Arbitrary intersection** of compact sets is compact
5. If $K$ is compact and $f$ is continuous, then $f(K)$ is compact

---

## Nested Interval Property

**Theorem:** If $\{[a_n, b_n]\}$ is a sequence of closed bounded intervals with:

$$[a_1, b_1] \supseteq [a_2, b_2] \supseteq [a_3, b_3] \supseteq \cdots$$

Then:

$$\bigcap_{n=1}^{\infty} [a_n, b_n] \neq \emptyset$$

If additionally $b_n - a_n \to 0$, then the intersection contains **exactly one point**.

---

## Why Compactness Matters

Compactness guarantees:
- **Extreme Value Theorem:** A continuous function on $[a,b]$ attains its maximum and minimum
- **Uniform Continuity:** A continuous function on a compact set is uniformly continuous
- **Convergence:** Every sequence has a convergent subsequence

These powerful results all rely on compactness. Without it, continuous functions can be unbounded and sequences can fail to converge.

---

## Cantor Set (Bonus)

The **Cantor set** is a famous example of a compact set that is:
- Closed ✓
- Bounded ✓
- Uncountable ✓
- Has measure zero ✓
- Contains no intervals ✓

It is constructed by repeatedly removing the middle third of $[0,1]$.
