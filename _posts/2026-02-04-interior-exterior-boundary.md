---
layout: post
title: "Interior, Exterior & Boundary of a Set in ℝ"
date: 2026-02-04
description: "Learn the definitions and properties of interior points, exterior points, and boundary points of a set in ℝ, with examples and their relationship to open and closed sets."
---

Every point in $\mathbb{R}$ relates to a set $S$ in one of three ways — it is either **inside**, **outside**, or on the **boundary** of $S$. These three concepts partition $\mathbb{R}$ completely.

---

## Interior Point

**Definition:** A point $x$ is an **interior point** of $S$ if there exists $\varepsilon > 0$ such that:

$$
N_\varepsilon(x) \subseteq S
$$

The entire neighbourhood of $x$ lies within $S$.

**The Interior** of $S$:

$$
\text{int}(S) = S^\circ = \{x \in \mathbb{R} : x \text{ is an interior point of } S\}
$$

---

## Exterior Point

**Definition:** A point $x$ is an **exterior point** of $S$ if it is an interior point of $S^c$:

$$
\exists\, \varepsilon > 0 : N_\varepsilon(x) \subseteq S^c
$$

**The Exterior** of $S$:

$$
\text{ext}(S) = \text{int}(S^c)
$$

---

## Boundary Point

**Definition:** A point $x$ is a **boundary point** of $S$ if every neighbourhood of $x$ contains at least one point in $S$ **and** at least one point in $S^c$:

$$
\forall\, \varepsilon > 0: N_\varepsilon(x) \cap S \neq \emptyset \quad \text{and} \quad N_\varepsilon(x) \cap S^c \neq \emptyset
$$

**The Boundary** of $S$:

$$
\partial S = \bar{S} \setminus \text{int}(S)
$$

---

## Partition of $\mathbb{R}$

For any set $S$, the three sets partition $\mathbb{R}$:

$$
\mathbb{R} = \text{int}(S) \cup \partial S \cup \text{ext}(S) \quad \text{(disjoint union)}
$$

---

## Solved Examples

**Example 1:** $S = (0, 1)$

- $\text{int}(S) = (0,1)$ — every interior point has a neighbourhood inside $(0,1)$
- $\partial S = \{0, 1\}$ — every neighbourhood of $0$ or $1$ hits both $(0,1)$ and its complement
- $\text{ext}(S) = (-\infty, 0) \cup (1, \infty)$

---

**Example 2:** $S = [0, 1]$

- $\text{int}(S) = (0,1)$
- $\partial S = \{0, 1\}$
- $\text{ext}(S) = (-\infty, 0) \cup (1, \infty)$

**Note:** $(0,1)$ and $[0,1]$ have the **same interior and boundary** — but one is open and one is closed.

---

**Example 3:** $S = \mathbb{Q}$

- $\text{int}(\mathbb{Q}) = \emptyset$ — no interval is entirely rational
- $\partial \mathbb{Q} = \mathbb{R}$ — every neighbourhood contains both rationals and irrationals
- $\text{ext}(\mathbb{Q}) = \emptyset$

---

**Example 4:** $S = \{1/n : n \in \mathbb{N}\}$

- $\text{int}(S) = \emptyset$ — singleton points have no neighbourhood inside $S$
- $\partial S = S \cup \{0\}$
- $\text{ext}(S) = \mathbb{R} \setminus (S \cup \{0\})$

---

## Key Relationships

$$\text{int}(S) \subseteq S \subseteq \bar{S}$$

$$\bar{S} = \text{int}(S) \cup \partial S$$

$$\partial S = \bar{S} \cap \overline{S^c}$$

---

## Characterization via Interior

- $S$ is **open** $\iff$ $S = \text{int}(S)$ (every point is interior)
- $S$ is **closed** $\iff$ $\partial S \subseteq S$ (contains all boundary points)
- $S$ is **clopen** $\iff$ $\partial S = \emptyset$ (only $\emptyset$ and $\mathbb{R}$ in $\mathbb{R}$)
