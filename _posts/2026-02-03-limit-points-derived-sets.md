---
layout: post
title: "Limit Points, Derived Sets & Closure in ℝ"
date: 2026-02-03
description: "Understand limit points (accumulation points), derived sets, and closure of a set in ℝ — with precise definitions, examples, and key theorems."
---

**Limit points** are at the heart of topology. They tell us about the "clustering behaviour" of a set and are essential for understanding closed sets and convergence.

---

## Limit Point (Accumulation Point)

**Definition:** A point $x \in \mathbb{R}$ is a **limit point** (or **accumulation point**) of a set $S \subseteq \mathbb{R}$ if every $\varepsilon$-neighbourhood of $x$ contains at least one point of $S$ **different from $x$**:

$$
\forall\, \varepsilon > 0,\quad N_\varepsilon(x) \cap (S \setminus \{x\}) \neq \emptyset
$$

**Note:** $x$ itself need not belong to $S$.

---

## Examples

**Example 1:** $S = (0, 1)$

Every point of $[0,1]$ is a limit point of $S$:
- Points inside $(0,1)$: clearly limit points
- $x = 0$: every neighbourhood $(−\varepsilon, \varepsilon)$ contains points of $(0,1)$ ✓
- $x = 1$: similarly ✓
- $x = 2$: $N_{0.4}(2) = (1.6, 2.4)$ contains no points of $(0,1)$ ✗

---

**Example 2:** $S = \left\{\frac{1}{n} : n \in \mathbb{N}\right\} = \left\{1, \frac{1}{2}, \frac{1}{3}, \ldots\right\}$

- $x = 0$ is a limit point (every neighbourhood of $0$ contains $\frac{1}{n}$ for large $n$) ✓
- No other point is a limit point (the points are isolated) ✗

---

**Example 3:** $S = \mathbb{Z}$ (integers)

No integer is a limit point of $\mathbb{Z}$ — take $\varepsilon = 0.5$: $N_{0.5}(n)$ contains no other integer. $\mathbb{Z}$ has **no limit points**.

---

## Isolated Points

A point $x \in S$ is an **isolated point** if it is NOT a limit point of $S$ — i.e., some neighbourhood of $x$ contains no other point of $S$.

$$
\exists\, \varepsilon > 0 : N_\varepsilon(x) \cap S = \{x\}
$$

**Example:** Every point of $\mathbb{Z}$ is isolated.

---

## Derived Set

**Definition:** The **derived set** of $S$, denoted $S'$ or $D(S)$, is the set of all limit points of $S$:

$$
S' = \{x \in \mathbb{R} : x \text{ is a limit point of } S\}
$$

**Examples:**

| $S$ | $S'$ |
|-----|------|
| $(0,1)$ | $[0,1]$ |
| $\{1, \frac{1}{2}, \frac{1}{3}, \ldots\}$ | $\{0\}$ |
| $\mathbb{Z}$ | $\emptyset$ |
| $\mathbb{Q}$ | $\mathbb{R}$ |
| $[a,b]$ | $[a,b]$ |

---

## Closure of a Set

**Definition:** The **closure** of $S$, denoted $\bar{S}$ or $\text{cl}(S)$, is:

$$
\bar{S} = S \cup S'
$$

It is the smallest closed set containing $S$.

**Examples:**
- $\overline{(0,1)} = [0,1]$
- $\overline{\mathbb{Q}} = \mathbb{R}$
- $\overline{\{0\}} = \{0\}$
- $\bar{\mathbb{Z}} = \mathbb{Z}$

---

## Characterization of Closed Sets

**Theorem:** $S$ is closed $\iff$ $S' \subseteq S$ $\iff$ $S = \bar{S}$

A set is closed if and only if it **contains all its limit points**.

---

## Bolzano–Weierstrass Theorem

**Theorem:** Every **bounded infinite** subset of $\mathbb{R}$ has at least one limit point in $\mathbb{R}$.

This is one of the most important theorems in analysis — it guarantees that bounded infinite sets cannot be "spread out" without clustering somewhere.

**Example:** The set $\left\{\frac{1}{n}\right\}$ is bounded and infinite → it has a limit point ($0$). ✓
