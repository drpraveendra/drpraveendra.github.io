---
layout: post
title: "Introduction to Point Set Topology in ℝ – Basic Concepts"
date: 2026-02-01
description: "A beginner-friendly introduction to Point Set Topology in the real line — covering the real number system, absolute value, and the concept of distance."
---

**Point Set Topology** in $\mathbb{R}$ is the study of the structure of subsets of the real line using the concept of **openness, closedness, limits, and continuity**. It forms the rigorous foundation of real analysis.

---

## The Real Line $\mathbb{R}$

The set of all real numbers $\mathbb{R}$ is a **complete ordered field**. Key properties:

- **Ordered:** For any $a, b \in \mathbb{R}$, exactly one of $a < b$, $a = b$, $a > b$ holds
- **Field:** Addition and multiplication are well-defined with inverses
- **Complete:** Every non-empty subset bounded above has a **least upper bound** (supremum)

---

## Absolute Value and Distance

The **absolute value** of $x \in \mathbb{R}$ is:

$$
|x| = \begin{cases} x & \text{if } x \geq 0 \\ -x & \text{if } x < 0 \end{cases}
$$

The **distance** between two real numbers $a$ and $b$ is:

$$
d(a, b) = |a - b|
$$

---

## Properties of Absolute Value

For all $a, b \in \mathbb{R}$:

1. $|a| \geq 0$, and $|a| = 0 \iff a = 0$
2. $|ab| = |a||b|$
3. **Triangle Inequality:** $|a + b| \leq |a| + |b|$
4. **Reverse Triangle Inequality:** $\big||a| - |b|\big| \leq |a - b|$

---

## Proof of Triangle Inequality

Since $-|a| \leq a \leq |a|$ and $-|b| \leq b \leq |b|$, adding:

$$
-(|a|+|b|) \leq a+b \leq |a|+|b|
$$

$$
\therefore |a+b| \leq |a| + |b| \quad \checkmark
$$

---

## Intervals in $\mathbb{R}$

| Notation | Name | Definition |
|----------|------|------------|
| $(a,b)$ | Open interval | $\{x : a < x < b\}$ |
| $[a,b]$ | Closed interval | $\{x : a \leq x \leq b\}$ |
| $[a,b)$ | Half-open | $\{x : a \leq x < b\}$ |
| $(a,\infty)$ | Unbounded open | $\{x : x > a\}$ |
| $(-\infty, \infty)$ | Entire real line | $\mathbb{R}$ |

---

## The $\varepsilon$-Neighbourhood

A fundamental concept in topology:

$$
N_\varepsilon(a) = (a - \varepsilon,\, a + \varepsilon) = \{x \in \mathbb{R} : |x - a| < \varepsilon\}
$$

This is called the **$\varepsilon$-neighbourhood** of $a$, or an **open ball** of radius $\varepsilon$ centered at $a$.

**Example:** $N_{0.5}(3) = (2.5, 3.5)$ — all points within distance $0.5$ of $3$.

---

## Supremum and Infimum

Let $S \subseteq \mathbb{R}$, $S \neq \emptyset$.

- **Supremum** $\sup S$: the **least upper bound** of $S$
- **Infimum** $\inf S$: the **greatest lower bound** of $S$

**Completeness Axiom:** If $S$ is non-empty and bounded above, then $\sup S$ exists in $\mathbb{R}$.

**Example:** $S = \{1, \frac{1}{2}, \frac{1}{3}, \ldots\}$

$$
\sup S = 1, \quad \inf S = 0
$$

Note: $0 \notin S$ but $\inf S = 0$ — the infimum need not belong to the set.

---

## Why Topology?

Topology answers questions like:
- What does it mean for a sequence to **converge**?
- What makes a function **continuous**?
- What is the difference between an **open** and **closed** set?

All of these are answered using the $\varepsilon$-neighbourhood concept introduced here.
