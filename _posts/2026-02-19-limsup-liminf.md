---
layout: post
title: "Limit Superior & Limit Inferior – Definitions, Properties & Examples"
date: 2026-02-19
description: "A complete guide to limit superior (limsup) and limit inferior (liminf) of sequences — formal definitions, computation methods, properties, and CSIR NET examples."
---

**Limit superior** and **limit inferior** extend the concept of limits to all bounded sequences — even those that don't converge. They are essential tools in real analysis and CSIR NET.

---

## Definitions

Let $\{a_n\}$ be a bounded sequence. Define:

$$
u_n = \sup_{k \geq n} a_k = \sup\{a_n, a_{n+1}, a_{n+2}, \ldots\}
$$

$$
v_n = \inf_{k \geq n} a_k = \inf\{a_n, a_{n+1}, a_{n+2}, \ldots\}
$$

Then:

$$
\limsup_{n\to\infty} a_n = \lim_{n\to\infty} u_n = \inf_n u_n
$$

$$
\liminf_{n\to\infty} a_n = \lim_{n\to\infty} v_n = \sup_n v_n
$$

---

## Why These Limits Exist

$\{u_n\}$ is **decreasing** (taking sup over smaller sets) and bounded below → converges by MCT.

$\{v_n\}$ is **increasing** and bounded above → converges by MCT.

---

## Fundamental Inequality

$$\liminf\, a_n \leq \limsup\, a_n$$

Always. Equality holds $\iff$ $\lim a_n$ exists.

---

## Worked Examples

### Example 1: $a_n = (-1)^n$

$$u_n = \sup\{(-1)^n, (-1)^{n+1}, \ldots\} = 1 \text{ for all } n$$
$$v_n = \inf\{\ldots\} = -1 \text{ for all } n$$

$$\limsup = 1,\quad \liminf = -1$$

---

### Example 2: $a_n = \frac{(-1)^n \cdot n}{n+1}$

For even $n$: $a_n = \frac{n}{n+1} \to 1$

For odd $n$: $a_n = -\frac{n}{n+1} \to -1$

$$\limsup = 1,\quad \liminf = -1$$

---

### Example 3: $a_n = \sin\left(\frac{n\pi}{2}\right)$

Values cycle: $1, 0, -1, 0, 1, 0, -1, 0, \ldots$

$$\limsup = 1,\quad \liminf = -1$$

---

### Example 4: $a_n = \frac{1}{n} + (-1)^n$

Even terms: $\frac{1}{2k} + 1 \to 1$

Odd terms: $\frac{1}{2k-1} - 1 \to -1$

$$\limsup = 1,\quad \liminf = -1$$

---

### Example 5 (Convergent): $a_n = \frac{1}{n}$

$$\limsup = \liminf = 0 \implies \lim a_n = 0 \checkmark$$

---

## Properties

Let $\{a_n\}$ and $\{b_n\}$ be bounded sequences:

1. $\limsup(-a_n) = -\liminf(a_n)$

2. $\limsup(a_n + b_n) \leq \limsup(a_n) + \limsup(b_n)$

3. $\liminf(a_n + b_n) \geq \liminf(a_n) + \liminf(b_n)$

4. If $a_n \leq b_n$ for all $n$: $\limsup(a_n) \leq \limsup(b_n)$

5. $\limsup(a_n \cdot b_n) \leq \limsup(a_n) \cdot \limsup(b_n)$ (for non-negative sequences)

---

## Convergence Criterion

$$\lim_{n\to\infty} a_n = L \iff \liminf_{n\to\infty} a_n = \limsup_{n\to\infty} a_n = L$$

---

## Application: Radius of Convergence

The radius of convergence of $\sum c_n x^n$ is:

$$R = \frac{1}{\limsup_{n\to\infty} |c_n|^{1/n}}$$

This is the **Cauchy-Hadamard formula** — limsup is essential here because the sequence $|c_n|^{1/n}$ may not converge.
