---
layout: post
title: "Countable & Uncountable Sets – Cantor's Theory with Proofs"
date: 2026-02-08
description: "Understand countable and uncountable sets — bijection-based definitions, proofs that ℚ is countable and ℝ is uncountable, and Cantor's diagonal argument."
---

**Countability** is a fundamental concept in set theory and topology. It answers the question: are there different "sizes" of infinity? The answer, due to **Georg Cantor**, is a resounding yes.

---

## Finite and Infinite Sets

A set $S$ is **finite** if it has $n$ elements for some $n \in \mathbb{N}$. Otherwise it is **infinite**.

---

## Countable Sets

**Definition:** A set $S$ is **countably infinite** if there exists a **bijection** $f: \mathbb{N} \to S$.

A set is **countable** if it is finite or countably infinite.

Intuitively, a countable set can be listed: $s_1, s_2, s_3, \ldots$

---

## Examples of Countable Sets

**1. $\mathbb{Z}$ is countable:**

List: $0, 1, -1, 2, -2, 3, -3, \ldots$

$$
f(n) = \begin{cases} \frac{n}{2} & n \text{ even} \\ -\frac{n+1}{2} & n \text{ odd} \end{cases}
$$

**2. $\mathbb{N} \times \mathbb{N}$ is countable:**

Arrange in a grid and use diagonal enumeration (Cantor's pairing).

**3. $\mathbb{Q}$ is countable:**

List all fractions $\frac{p}{q}$ using diagonal enumeration of $\mathbb{Z} \times \mathbb{N}$, skipping duplicates.

---

## $\mathbb{R}$ is Uncountable — Cantor's Diagonal Argument

**Theorem:** The interval $(0,1)$ is uncountable.

**Proof (by contradiction):** Suppose $(0,1)$ is countable. List all elements:

$$
x_1 = 0.d_{11}d_{12}d_{13}\ldots
$$
$$
x_2 = 0.d_{21}d_{22}d_{23}\ldots
$$
$$
x_3 = 0.d_{31}d_{32}d_{33}\ldots
$$

Construct $y = 0.y_1 y_2 y_3 \ldots$ where:

$$
y_n = \begin{cases} 2 & \text{if } d_{nn} \neq 2 \\ 3 & \text{if } d_{nn} = 2 \end{cases}
$$

Then $y \in (0,1)$ but $y \neq x_n$ for any $n$ (differs in the $n$-th digit).

This **contradicts** our assumption that the list was complete. So $(0,1)$ is **uncountable**. ✗ (contradiction)

Since $(0,1) \subseteq \mathbb{R}$, $\mathbb{R}$ is also uncountable. $\blacksquare$

---

## Countability Properties

1. Every subset of a countable set is countable
2. **Countable union of countable sets is countable**
3. **Finite product** of countable sets is countable
4. $\mathbb{Q}$ is countable; $\mathbb{R} \setminus \mathbb{Q}$ is uncountable
5. Any open interval $(a,b)$ is uncountable

---

## Cardinality

The **cardinality** of a set measures its "size":

| Set | Cardinality | Symbol |
|-----|------------|--------|
| $\{1,2,3\}$ | Finite | $3$ |
| $\mathbb{N}$ | Countably infinite | $\aleph_0$ |
| $\mathbb{Z}$ | Countably infinite | $\aleph_0$ |
| $\mathbb{Q}$ | Countably infinite | $\aleph_0$ |
| $\mathbb{R}$ | Uncountably infinite | $\mathfrak{c} = 2^{\aleph_0}$ |
| $(0,1)$ | Uncountably infinite | $\mathfrak{c}$ |

---

## Cantor's Theorem

**Theorem:** For any set $S$, the power set $\mathcal{P}(S)$ has strictly larger cardinality than $S$:

$$
|S| < |\mathcal{P}(S)|
$$

This means there is no "largest" infinity — there are infinitely many levels of infinity!
