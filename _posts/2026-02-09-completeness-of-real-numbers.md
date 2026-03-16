---
layout: post
title: "Completeness of ℝ – Axiom, Cauchy Sequences & Consequences"
date: 2026-02-09
description: "Understand the completeness of ℝ — the completeness axiom, Cauchy sequences, and why ℝ is complete while ℚ is not, with proofs and examples."
---

**Completeness** is the property that distinguishes $\mathbb{R}$ from $\mathbb{Q}$. It guarantees that $\mathbb{R}$ has "no holes" — every Cauchy sequence converges, and every bounded set has a supremum.

---

## The Completeness Axiom

**Axiom (Least Upper Bound Property):** Every non-empty subset of $\mathbb{R}$ that is **bounded above** has a **supremum (least upper bound)** in $\mathbb{R}$.

This is an **axiom** — it is assumed as a fundamental property of $\mathbb{R}$, not proved.

---

## $\mathbb{Q}$ is NOT Complete

**Example:** The set $S = \{x \in \mathbb{Q} : x^2 < 2\}$ is bounded above in $\mathbb{Q}$ (e.g., by $2$), but its supremum is $\sqrt{2} \notin \mathbb{Q}$.

So $\mathbb{Q}$ fails the least upper bound property — it has "holes" at irrational numbers.

---

## Cauchy Sequences

**Definition:** A sequence $\{x_n\}$ is a **Cauchy sequence** if:

$$
\forall\, \varepsilon > 0,\quad \exists\, N \in \mathbb{N} \text{ such that } \forall\, m, n > N: |x_m - x_n| < \varepsilon
$$

The terms become **arbitrarily close to each other** — they cluster without necessarily knowing the limit.

---

## Complete Metric Space

**Definition:** A metric space is **complete** if every Cauchy sequence **converges** to a point in the space.

**Theorem:** $\mathbb{R}$ is **complete** — every Cauchy sequence in $\mathbb{R}$ converges to a real number.

---

## Proof Idea: Cauchy $\implies$ Convergent in $\mathbb{R}$

1. Every Cauchy sequence is **bounded**
2. By **Bolzano-Weierstrass**, it has a convergent subsequence $x_{n_k} \to L$
3. Since the sequence is Cauchy and a subsequence converges to $L$, the whole sequence converges to $L$

---

## $\mathbb{Q}$ is Not Complete — Example

The sequence:

$$
x_1 = 1,\quad x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n}
$$

is a Cauchy sequence in $\mathbb{Q}$ (the Newton-Raphson approximation to $\sqrt{2}$), but converges to $\sqrt{2} \notin \mathbb{Q}$.

So $\mathbb{Q}$ is **not complete**. ✗

---

## Equivalent Forms of Completeness

All of the following are equivalent to the Completeness Axiom:

1. **Monotone Convergence Theorem:** Every bounded monotone sequence converges
2. **Bolzano-Weierstrass Theorem:** Every bounded sequence has a convergent subsequence
3. **Nested Interval Property:** $\bigcap [a_n, b_n] \neq \emptyset$ for nested closed intervals
4. **Cauchy Completeness:** Every Cauchy sequence converges
5. **Archimedean Property + Density of $\mathbb{Q}$**

---

## Archimedean Property

**Theorem:** For any $x \in \mathbb{R}$, there exists $n \in \mathbb{N}$ such that $n > x$.

This means $\mathbb{N}$ is **not bounded above** in $\mathbb{R}$ — there is no "infinitely large" real number.

**Consequence:**

$$
\forall\, \varepsilon > 0,\quad \exists\, n \in \mathbb{N} : \frac{1}{n} < \varepsilon
$$

This is used constantly in analysis proofs.

---

## Summary

| Property | $\mathbb{Q}$ | $\mathbb{R}$ |
|----------|------------|------------|
| Ordered field | ✓ | ✓ |
| Archimedean | ✓ | ✓ |
| Dense in itself | ✓ | ✓ |
| Complete | ✗ | ✓ |

Completeness is the single property that makes $\mathbb{R}$ the "right" setting for calculus and analysis.
