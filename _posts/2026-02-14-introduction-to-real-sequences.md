---
layout: post
title: "Introduction to Real Sequences – Definition, Notation & Examples"
date: 2026-02-14
description: "A complete introduction to real sequences — precise definition, notation, range vs sequence, bounded sequences, and standard examples for B.Sc. and M.Sc. students."
---

A **real sequence** is one of the most fundamental objects in mathematical analysis. Understanding sequences rigorously is the gateway to understanding limits, continuity, and series.

---

## Definition

**Definition:** A **real sequence** is a function $f: \mathbb{N} \to \mathbb{R}$.

The value $f(n)$ is written as $a_n$ and called the **$n$-th term**. The sequence is denoted:

$$
\{a_n\}_{n=1}^{\infty} = \{a_1, a_2, a_3, \ldots\}
$$

---

## Sequence vs Range

- The **sequence** $\{a_n\}$ is an ordered list — repetitions matter
- The **range** is the set of values $\{a_n : n \in \mathbb{N}\}$ — no repetitions

**Example:** $a_n = (-1)^n$: sequence is $-1, 1, -1, 1, \ldots$ but range is just $\{-1, 1\}$.

---

## Standard Examples

| Sequence | Formula | First few terms |
|----------|---------|----------------|
| Constant | $a_n = c$ | $c, c, c, \ldots$ |
| Natural numbers | $a_n = n$ | $1, 2, 3, 4, \ldots$ |
| Reciprocals | $a_n = \frac{1}{n}$ | $1, \frac{1}{2}, \frac{1}{3}, \ldots$ |
| Geometric | $a_n = r^n$ | $r, r^2, r^3, \ldots$ |
| Alternating | $a_n = (-1)^n$ | $-1, 1, -1, 1, \ldots$ |
| Factorial | $a_n = \frac{1}{n!}$ | $1, \frac{1}{2}, \frac{1}{6}, \frac{1}{24}, \ldots$ |

---

## Bounded Sequences

**Bounded above:** $\exists\, M: a_n \leq M$ for all $n$

**Bounded below:** $\exists\, m: a_n \geq m$ for all $n$

**Bounded:** Both bounded above and below — $\exists\, K > 0: |a_n| \leq K$ for all $n$

**Examples:**
- $a_n = \frac{1}{n}$: bounded (between 0 and 1)
- $a_n = n$: bounded below (by 1), NOT bounded above
- $a_n = (-1)^n$: bounded (by 1)

---

## Monotone Sequences

**Increasing:** $a_{n+1} \geq a_n$ for all $n$ (non-decreasing)

**Strictly increasing:** $a_{n+1} > a_n$ for all $n$

**Decreasing:** $a_{n+1} \leq a_n$ for all $n$ (non-increasing)

**Examples:**
- $a_n = n$: strictly increasing
- $a_n = \frac{1}{n}$: strictly decreasing
- $a_n = 1 + \frac{1}{n}$: strictly decreasing, bounded below by 1
- $a_n = (-1)^n$: neither monotone

---

## Subsequences

**Definition:** A **subsequence** of $\{a_n\}$ is $\{a_{n_k}\}$ where $n_1 < n_2 < n_3 < \cdots$

**Example:** From $\{1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots\}$, take $n_k = 2k$:

$$
a_{n_k} = \frac{1}{2k} = \frac{1}{2}, \frac{1}{4}, \frac{1}{6}, \ldots
$$

---

## Recursively Defined Sequences

Some sequences are defined by a recurrence relation:

**Example 1 (Fibonacci):**
$$a_1 = 1,\quad a_2 = 1,\quad a_{n+2} = a_{n+1} + a_n$$
$$1, 1, 2, 3, 5, 8, 13, \ldots$$

**Example 2 (Newton-Raphson for $\sqrt{2}$):**
$$a_1 = 1,\quad a_{n+1} = \frac{1}{2}\left(a_n + \frac{2}{a_n}\right)$$
$$1,\; 1.5,\; 1.4167,\; 1.4142\ldots \to \sqrt{2}$$

---

## Key Principle

The study of sequences is the rigorous foundation for:
- Limits of functions
- Continuity and differentiability
- Infinite series (a series is just the sequence of partial sums)
- Convergence in metric spaces
