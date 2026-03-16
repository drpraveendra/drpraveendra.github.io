---
layout: post
title: "Connected Sets in ℝ – Definition, Characterization & Examples"
date: 2026-02-06
description: "Learn about connected sets in ℝ — definition via separation, the characterization that intervals are the only connected subsets, and path connectedness."
---

**Connectedness** captures the idea that a set is "in one piece" — it cannot be split into two separate open parts. In $\mathbb{R}$, connected sets have a beautifully simple characterization.

---

## Definition of Connected Set

**Definition:** A set $S \subseteq \mathbb{R}$ is **disconnected** if there exist two non-empty open sets $U$ and $V$ such that:

$$
S \subseteq U \cup V, \quad S \cap U \neq \emptyset, \quad S \cap V \neq \emptyset, \quad U \cap V = \emptyset
$$

$S$ is **connected** if it is NOT disconnected — i.e., it cannot be separated into two such parts.

---

## Characterization of Connected Sets in $\mathbb{R}$

**Theorem:** A subset $S \subseteq \mathbb{R}$ is connected $\iff$ $S$ is an **interval**.

(Here "interval" includes all types: open, closed, half-open, unbounded, and even single points and $\mathbb{R}$ itself.)

---

## Examples

**Connected:**
- $(a, b)$, $[a, b]$, $[a, b)$ — all intervals ✓
- $\mathbb{R}$, $(-\infty, a)$, $(a, \infty)$ ✓
- $\{a\}$ — single point ✓

**Disconnected:**
- $(0,1) \cup (2,3)$ — two separate pieces ✗
- $\mathbb{Q}$ — separated by any irrational ✗
- $\mathbb{Z}$ — each integer is isolated ✗
- $[0,1] \cup [2,3]$ ✗

---

## Proving $(0,1) \cup (2,3)$ is Disconnected

Take $U = (-\infty, 1.5)$ and $V = (1.5, \infty)$. Then:
- $U$ and $V$ are open and disjoint ✓
- $(0,1) \subseteq U$ and $(2,3) \subseteq V$ ✓
- $(0,1) \cup (2,3) \subseteq U \cup V$ ✓

So the set is disconnected. ✗

---

## Intermediate Value Theorem (Topological Form)

**Theorem:** If $f: S \to \mathbb{R}$ is continuous and $S$ is connected, then $f(S)$ is also connected (hence an interval).

This gives the classical **Intermediate Value Theorem:**

If $f$ is continuous on $[a,b]$ and $f(a) < k < f(b)$, then $\exists\, c \in (a,b)$ such that $f(c) = k$.

---

## Path Connectedness

**Definition:** $S$ is **path connected** if for any two points $x, y \in S$, there exists a continuous function $\gamma: [0,1] \to S$ with $\gamma(0) = x$ and $\gamma(1) = y$.

In $\mathbb{R}$: path connected $\iff$ connected $\iff$ interval.

(In higher dimensions, path connectedness is stronger than connectedness.)

---

## Clopen Sets and Connectedness

**Theorem:** $\mathbb{R}$ is connected $\iff$ the only subsets of $\mathbb{R}$ that are both open and closed are $\emptyset$ and $\mathbb{R}$.

This is an equivalent way to define connectedness, and it shows why $\mathbb{R}$ has no "gaps".

---

## Summary Table

| Set | Connected? | Reason |
|-----|-----------|--------|
| $[0,1]$ | ✓ | Interval |
| $(0,1) \cup (2,3)$ | ✗ | Two pieces |
| $\mathbb{Q}$ | ✗ | Dense gaps |
| $\mathbb{R}$ | ✓ | Interval (unbounded) |
| $\{5\}$ | ✓ | Trivially an interval |
| $[1,2] \cup \{3\}$ | ✗ | Not an interval |
