---
layout: post
title: "Dense, Nowhere Dense & Perfect Sets in ℝ"
date: 2026-02-07
description: "Explore dense sets, nowhere dense sets, and perfect sets in ℝ — with the density of rationals, irrationals, and the remarkable Cantor set as examples."
---

The concepts of **dense** and **nowhere dense** sets describe how "spread out" a set is within $\mathbb{R}$. They are key to understanding the structure of $\mathbb{Q}$, $\mathbb{R} \setminus \mathbb{Q}$, and the Cantor set.

---

## Dense Sets

**Definition:** A set $S \subseteq \mathbb{R}$ is **dense in $\mathbb{R}$** if every non-empty open interval $(a,b)$ contains at least one point of $S$:

$$
\forall\, a < b,\quad S \cap (a,b) \neq \emptyset
$$

**Equivalent condition:** $\bar{S} = \mathbb{R}$

---

## Examples of Dense Sets

**1. $\mathbb{Q}$ is dense in $\mathbb{R}$:**

Between any two real numbers $a < b$, there exists a rational number. This is the **density of rationals**.

$$
\forall\, a < b \in \mathbb{R},\quad \exists\, r \in \mathbb{Q} : a < r < b
$$

**2. $\mathbb{R} \setminus \mathbb{Q}$ (irrationals) is dense in $\mathbb{R}$:**

Between any two reals, there is an irrational — e.g., $a + \frac{\sqrt{2}}{n}$ for large $n$.

**3. $\mathbb{R}$ is dense in itself.**

---

## Nowhere Dense Sets

**Definition:** A set $S$ is **nowhere dense** in $\mathbb{R}$ if its closure has empty interior:

$$
\text{int}(\bar{S}) = \emptyset
$$

Equivalently, $S$ is nowhere dense if every open interval $(a,b)$ contains an open subinterval that is entirely outside $S$.

---

## Examples of Nowhere Dense Sets

- $\mathbb{Z}$ — nowhere dense (no interval is contained in $\mathbb{Z}$) ✓
- $\left\{\frac{1}{n}\right\}$ — nowhere dense ✓
- Any finite set — nowhere dense ✓
- The **Cantor set** $C$ — nowhere dense (contains no intervals) ✓

---

## First and Second Category (Baire Categories)

**First category (meagre):** A set that is a **countable union of nowhere dense sets**.

Example: $\mathbb{Q} = \bigcup_{q \in \mathbb{Q}} \{q\}$ — each $\{q\}$ is nowhere dense, so $\mathbb{Q}$ is first category.

**Second category:** A set that is NOT first category.

**Baire Category Theorem:** $\mathbb{R}$ is of **second category** — it cannot be written as a countable union of nowhere dense sets. This is a deep result!

---

## Perfect Sets

**Definition:** A set $S$ is **perfect** if:
1. $S$ is **closed**
2. Every point of $S$ is a **limit point** of $S$ (i.e., $S = S'$)

**Examples:**
- $[a,b]$ — perfect ✓
- $\mathbb{R}$ — perfect ✓
- $\emptyset$ — perfect (vacuously) ✓
- The **Cantor set** — perfect ✓

---

## The Cantor Set — A Remarkable Example

The Cantor set $C$ is constructed by removing the open middle third of $[0,1]$ repeatedly:

$$
C_0 = [0,1]
$$
$$
C_1 = \left[0,\frac{1}{3}\right] \cup \left[\frac{2}{3},1\right]
$$
$$
C_2 = \left[0,\frac{1}{9}\right] \cup \left[\frac{2}{9},\frac{1}{3}\right] \cup \left[\frac{2}{3},\frac{7}{9}\right] \cup \left[\frac{8}{9},1\right]
$$
$$
C = \bigcap_{n=0}^{\infty} C_n
$$

**Properties of the Cantor set:**

| Property | Value |
|----------|-------|
| Closed | ✓ |
| Bounded | ✓ |
| Perfect | ✓ |
| Nowhere dense | ✓ |
| Measure | $0$ |
| Cardinality | Uncountable |

The Cantor set is **uncountable** yet has **measure zero** — a striking paradox showing that "size" in topology and measure theory are very different.
