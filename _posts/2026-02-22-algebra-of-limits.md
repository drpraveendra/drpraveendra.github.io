---
layout: post
title: "Algebra of Limits of Sequences – Theorems & Solved Problems"
date: 2026-02-22
description: "Complete guide to the algebra of limits — sum, product, quotient, and composition rules with full proofs, examples, and common mistakes to avoid."
---

The **Algebra of Limits** provides rules for computing limits of combinations of sequences. Once you know individual limits, you can compute limits of sums, products, and quotients without using the $\varepsilon$-definition each time.

---

## Main Theorem

Let $\{a_n\}$ and $\{b_n\}$ be sequences with $a_n \to L$ and $b_n \to M$. Then:

| Rule | Result |
|------|--------|
| **Sum:** $a_n + b_n$ | $\to L + M$ |
| **Difference:** $a_n - b_n$ | $\to L - M$ |
| **Scalar multiple:** $c \cdot a_n$ | $\to cL$ |
| **Product:** $a_n \cdot b_n$ | $\to L \cdot M$ |
| **Quotient:** $\frac{a_n}{b_n}$ | $\to \frac{L}{M}$ (if $M \neq 0$) |
| **Power:** $a_n^k$ | $\to L^k$ |
| **Absolute value:** $\|a_n\|$ | $\to \|L\|$ |

---

## Proof of Product Rule

**Claim:** If $a_n \to L$ and $b_n \to M$, then $a_n b_n \to LM$.

**Proof:**

$$|a_n b_n - LM| = |a_n b_n - a_n M + a_n M - LM|$$
$$\leq |a_n||b_n - M| + |M||a_n - L|$$

Since $\{a_n\}$ converges, it is bounded: $|a_n| \leq K$ for all $n$.

Given $\varepsilon > 0$:
- $\exists\, N_1: n > N_1 \implies |b_n - M| < \frac{\varepsilon}{2K}$
- $\exists\, N_2: n > N_2 \implies |a_n - L| < \frac{\varepsilon}{2(|M|+1)}$

For $n > \max(N_1, N_2)$:

$$|a_n b_n - LM| \leq K \cdot \frac{\varepsilon}{2K} + (|M|+1) \cdot \frac{\varepsilon}{2(|M|+1)} = \varepsilon \quad \blacksquare$$

---

## Solved Examples

### Example 1

**Find:** $\displaystyle\lim_{n\to\infty} \frac{3n^2 + 5n - 2}{4n^2 - n + 7}$

Divide numerator and denominator by $n^2$:

$$= \lim_{n\to\infty} \frac{3 + \frac{5}{n} - \frac{2}{n^2}}{4 - \frac{1}{n} + \frac{7}{n^2}} = \frac{3 + 0 - 0}{4 - 0 + 0} = \frac{3}{4}$$

---

### Example 2

**Find:** $\displaystyle\lim_{n\to\infty} \frac{n^3 - 2n}{5n^3 + n^2}$

Divide by $n^3$:

$$= \frac{1 - \frac{2}{n^2}}{5 + \frac{1}{n}} = \frac{1}{5}$$

---

### Example 3

**Find:** $\displaystyle\lim_{n\to\infty} \left(\sqrt{n^2 + n} - n\right)$

Rationalize:

$$\sqrt{n^2+n} - n = \frac{(n^2+n) - n^2}{\sqrt{n^2+n}+n} = \frac{n}{\sqrt{n^2+n}+n} = \frac{1}{\sqrt{1+\frac{1}{n}}+1} \to \frac{1}{2}$$

---

### Example 4

**Find:** $\displaystyle\lim_{n\to\infty} \left(\frac{n+1}{n-1}\right)^n$

$$= \lim_{n\to\infty} \left(1 + \frac{2}{n-1}\right)^n = \lim_{n\to\infty} \left[\left(1+\frac{2}{n-1}\right)^{n-1}\right]^{\frac{n}{n-1}} = e^2 \cdot 1 = e^2$$

---

### Example 5

**Find:** $\displaystyle\lim_{n\to\infty} \frac{n!}{n^n}$

$$\frac{n!}{n^n} = \frac{1 \cdot 2 \cdot 3 \cdots n}{n \cdot n \cdot n \cdots n} \leq \frac{1}{n} \to 0$$

By Squeeze: $\lim \frac{n!}{n^n} = 0$.

---

## Common Pitfalls

| Situation | Mistake | Correct approach |
|-----------|---------|-----------------|
| $\infty - \infty$ | Cannot say $0$ | Rationalize or factor |
| $\frac{\infty}{\infty}$ | Cannot say $1$ | Divide by highest power |
| $0 \cdot \infty$ | Cannot say $0$ | Rewrite as $\frac{0}{1/\infty}$ |
| $1^\infty$ | Cannot say $1$ | Use $\left(1+\frac{x}{n}\right)^n \to e^x$ |
