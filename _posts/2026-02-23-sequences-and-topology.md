---
layout: post
title: "Sequences & Topology – Characterizing Closed Sets and Continuity"
date: 2026-02-23
description: "Explore the deep connection between sequences and topology — how sequences characterize closed sets, limit points, and continuity in ℝ."
---

Sequences and topology in $\mathbb{R}$ are deeply interconnected. Almost every topological concept — closed sets, limit points, continuity — can be **characterized using sequences**. This is one of the beautiful features of $\mathbb{R}$.

---

## Sequences Characterize Limit Points

**Theorem:** $x$ is a limit point of $S \subseteq \mathbb{R}$ $\iff$ there exists a sequence $\{s_n\} \subseteq S$ with $s_n \neq x$ and $s_n \to x$.

**Proof ($\Rightarrow$):** Since $x$ is a limit point, for each $n$, $N_{1/n}(x) \cap (S \setminus \{x\}) \neq \emptyset$. Pick $s_n$ from this intersection. Then $|s_n - x| < \frac{1}{n} \to 0$, so $s_n \to x$. $\blacksquare$

---

## Sequences Characterize Closed Sets

**Theorem:** $F \subseteq \mathbb{R}$ is closed $\iff$ for every sequence $\{a_n\} \subseteq F$ with $a_n \to L$, we have $L \in F$.

In other words: **closed sets are exactly those that contain all limits of their sequences**.

**Proof ($\Rightarrow$):** If $F$ is closed and $a_n \to L$ with $a_n \in F$, then either $L \in F$ already, or $L$ is a limit point of $F$. Since $F$ is closed, it contains all limit points, so $L \in F$. $\blacksquare$

---

## Example

**Is $F = [0, 1]$ closed?**

Take any sequence $\{a_n\} \subseteq [0,1]$ with $a_n \to L$. Since $0 \leq a_n \leq 1$ for all $n$, taking limits: $0 \leq L \leq 1$. So $L \in [0,1] = F$. ✓ F is closed.

**Is $F = (0,1)$ closed?**

Take $a_n = \frac{1}{n} \in (0,1)$. Then $a_n \to 0 \notin (0,1)$. So $(0,1)$ is NOT closed. ✗

---

## Sequences Characterize Continuity

**Theorem (Sequential Characterization):** $f: \mathbb{R} \to \mathbb{R}$ is continuous at $a$ $\iff$:

$$a_n \to a \implies f(a_n) \to f(a)$$

for every sequence $\{a_n\}$ converging to $a$.

---

## Proof

**($\Rightarrow$):** Let $f$ be continuous at $a$ and $a_n \to a$. Given $\varepsilon > 0$, $\exists\, \delta > 0: |x-a| < \delta \implies |f(x)-f(a)| < \varepsilon$.

Since $a_n \to a$, $\exists\, N: n > N \implies |a_n - a| < \delta \implies |f(a_n) - f(a)| < \varepsilon$. $\blacksquare$

---

## Proving Discontinuity via Sequences

**Example:** $f(x) = \begin{cases} 1 & x > 0 \\ 0 & x \leq 0 \end{cases}$

Take $a_n = \frac{1}{n} \to 0$. Then $f(a_n) = 1$ for all $n$, but $f(0) = 0$. Since $f(a_n) \not\to f(0)$, $f$ is **discontinuous at $0$**. ✗

---

## Sequences Characterize Closure

**Theorem:** $x \in \bar{S}$ $\iff$ there exists a sequence $\{s_n\} \subseteq S$ with $s_n \to x$.

This says: the closure of $S$ is exactly the set of all limits of sequences from $S$.

**Example:** $\bar{\mathbb{Q}} = \mathbb{R}$ because every real number is the limit of a sequence of rationals (decimal approximations). ✓

---

## Summary Table

| Topological Concept | Sequential Characterization |
|--------------------|----------------------------|
| $x$ is a limit point of $S$ | $\exists\, \{s_n\} \subseteq S\setminus\{x\}$ with $s_n \to x$ |
| $S$ is closed | Every convergent sequence in $S$ has limit in $S$ |
| $x \in \bar{S}$ | $\exists\, \{s_n\} \subseteq S$ with $s_n \to x$ |
| $f$ continuous at $a$ | $a_n \to a \implies f(a_n) \to f(a)$ |
| $K$ is compact | Every sequence in $K$ has convergent subsequence in $K$ |
