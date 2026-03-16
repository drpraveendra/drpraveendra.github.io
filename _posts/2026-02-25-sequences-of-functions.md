---
layout: post
title: "Sequences of Functions – Pointwise vs Uniform Convergence"
date: 2026-02-25
description: "Learn about sequences of functions — pointwise convergence, uniform convergence, their differences, and why uniform convergence is essential for preserving continuity and integration."
---

When sequences involve functions instead of numbers, convergence becomes richer and more subtle. **Pointwise** and **uniform** convergence are two fundamentally different types.

---

## Sequences of Functions

A **sequence of functions** is $\{f_n\}$ where each $f_n: [a,b] \to \mathbb{R}$.

For each fixed $x$, $\{f_n(x)\}$ is a sequence of real numbers.

---

## Pointwise Convergence

**Definition:** $\{f_n\}$ converges **pointwise** to $f$ on $[a,b]$ if:

$$\forall\, x \in [a,b],\quad \lim_{n\to\infty} f_n(x) = f(x)$$

For each fixed $x$, the sequence of numbers $f_n(x) \to f(x)$.

The rate of convergence may differ for different $x$.

---

## Uniform Convergence

**Definition:** $\{f_n\}$ converges **uniformly** to $f$ on $[a,b]$ if:

$$\forall\, \varepsilon > 0,\;\exists\, N \text{ (independent of } x): n > N \implies |f_n(x) - f(x)| < \varepsilon \;\forall\, x \in [a,b]$$

The **same $N$ works for all $x$ simultaneously**.

**Equivalent condition:**

$$f_n \to f \text{ uniformly} \iff \sup_{x \in [a,b]} |f_n(x) - f(x)| \to 0$$

---

## Examples

### Example 1: $f_n(x) = x^n$ on $[0,1]$

**Pointwise limit:**

$$f(x) = \lim_{n\to\infty} x^n = \begin{cases} 0 & 0 \leq x < 1 \\ 1 & x = 1 \end{cases}$$

**Is it uniform?**

$$\sup_{x \in [0,1]} |f_n(x) - f(x)| = \sup_{x \in [0,1)} x^n$$

For any fixed $n$: $\sup_{x \in [0,1)} x^n = 1$ (approached as $x \to 1^-$).

So $\sup |f_n - f| = 1 \not\to 0$ → **NOT uniformly convergent** on $[0,1]$. ✗

But **uniformly convergent on $[0, r]$ for any $r < 1$** (since $\sup x^n = r^n \to 0$). ✓

---

### Example 2: $f_n(x) = \frac{x}{n}$ on $[0, 1]$

Pointwise: $f(x) = 0$.

$$\sup_{x \in [0,1]} \left|\frac{x}{n} - 0\right| = \frac{1}{n} \to 0$$

**Uniformly convergent.** ✓

---

### Example 3: $f_n(x) = \frac{nx}{1+n^2x^2}$ on $[0,1]$

Pointwise: $f(x) = 0$ for all $x \in [0,1]$ (including $x=0$).

$$\sup_{x \in [0,1]} f_n(x) = f_n\left(\frac{1}{n}\right) = \frac{n \cdot \frac{1}{n}}{1 + n^2 \cdot \frac{1}{n^2}} = \frac{1}{2} \not\to 0$$

**NOT uniformly convergent.** ✗

---

## Why It Matters: Properties Preserved

| Property | Pointwise | Uniform |
|----------|-----------|---------|
| Limit of continuous functions is continuous | ✗ | ✓ |
| Term-by-term integration | ✗ | ✓ |
| Term-by-term differentiation | ✗ | ✓ (with extra condition) |

### Failure under Pointwise Convergence

$f_n(x) = x^n$ on $[0,1]$: each $f_n$ is continuous, but the pointwise limit $f$ is **discontinuous** at $x=1$.

Under **uniform** convergence, the limit of continuous functions is always continuous.

---

## Dini's Theorem

**Theorem:** If $\{f_n\}$ is a **monotone** sequence of continuous functions converging **pointwise** to a continuous function $f$ on a compact set $[a,b]$, then the convergence is **uniform**.

This gives a sufficient condition for pointwise to imply uniform convergence.
