---
layout: post
title: "Open Sets and Closed Sets in ℝ – Definitions, Examples & Properties"
date: 2026-02-02
description: "Learn the precise definitions of open and closed sets in ℝ, their key properties, examples, and the relationship between them via complementation."
---

**Open sets** and **closed sets** are the two most fundamental concepts in topology. Understanding them rigorously is essential for all of real analysis.

---

## Open Sets

**Definition:** A set $G \subseteq \mathbb{R}$ is **open** if for every $x \in G$, there exists $\varepsilon > 0$ such that:

$$
N_\varepsilon(x) = (x-\varepsilon, x+\varepsilon) \subseteq G
$$

Every point of $G$ has an entire neighbourhood contained in $G$.

---

## Examples of Open Sets

- $(a, b)$ — open interval is open ✓
- $\mathbb{R}$ — the entire real line is open ✓
- $\emptyset$ — the empty set is open (vacuously) ✓
- $(1, 3) \cup (5, 7)$ — union of open intervals is open ✓
- $\mathbb{Q}$ — rational numbers are **NOT** open (no interval around any rational is entirely rational)

---

## Closed Sets

**Definition:** A set $F \subseteq \mathbb{R}$ is **closed** if its complement $F^c = \mathbb{R} \setminus F$ is open.

**Equivalent definition:** $F$ is closed if and only if it contains all its **limit points**.

---

## Examples of Closed Sets

- $[a, b]$ — closed interval is closed ✓
- $\mathbb{R}$ — closed (its complement $\emptyset$ is open) ✓
- $\emptyset$ — closed (its complement $\mathbb{R}$ is open) ✓
- $\{a\}$ — every singleton set is closed ✓
- $\mathbb{Z}$ — the integers are closed ✓

---

## Neither Open Nor Closed

- $[a, b)$ — half-open interval: not open (endpoint $a$ has no neighbourhood in the set), not closed (complement is not open)
- $\mathbb{Q}$ — not open, not closed

---

## Key Properties of Open Sets

1. $\emptyset$ and $\mathbb{R}$ are open
2. **Arbitrary union** of open sets is open:
$$\bigcup_{\alpha} G_\alpha \text{ is open}$$
3. **Finite intersection** of open sets is open:
$$G_1 \cap G_2 \cap \cdots \cap G_n \text{ is open}$$

**Warning:** Infinite intersection of open sets may NOT be open.

$$\bigcap_{n=1}^{\infty} \left(-\frac{1}{n}, \frac{1}{n}\right) = \{0\} \quad \text{(closed!)}$$

---

## Key Properties of Closed Sets

1. $\emptyset$ and $\mathbb{R}$ are closed
2. **Arbitrary intersection** of closed sets is closed
3. **Finite union** of closed sets is closed

**Warning:** Infinite union of closed sets may NOT be closed.

$$\bigcup_{n=1}^{\infty} \left[\frac{1}{n}, 1\right] = (0, 1] \quad \text{(not closed)}$$

---

## Relationship Between Open and Closed

$$F \text{ is closed} \iff F^c \text{ is open}$$
$$G \text{ is open} \iff G^c \text{ is closed}$$

**Note:** Sets can be:
- Open but not closed: $(0,1)$
- Closed but not open: $[0,1]$
- Both open and closed (clopen): $\emptyset$, $\mathbb{R}$
- Neither: $[0,1)$

---

## Characterization Theorem

**Theorem:** Every open set in $\mathbb{R}$ is a **countable union of disjoint open intervals**.

This elegant result shows that open intervals are the "building blocks" of all open sets in $\mathbb{R}$.
