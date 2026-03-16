---
layout: post
title: "Squeeze Theorem & Standard Limits of Sequences"
date: 2026-02-20
description: "Master the Squeeze Theorem (Sandwich Theorem) for sequences with proofs and applications, plus a complete table of standard limits every analysis student must know."
---

The **Squeeze Theorem** is one of the most elegant tools for evaluating limits — when you can't compute a limit directly, trap it between two sequences that converge to the same value.

---

## Squeeze Theorem (Sandwich Theorem)

**Theorem:** Let $\{a_n\}$, $\{b_n\}$, $\{c_n\}$ be sequences such that:

$$a_n \leq b_n \leq c_n \quad \text{for all } n \geq N_0$$

If $\lim_{n\to\infty} a_n = \lim_{n\to\infty} c_n = L$, then:

$$\lim_{n\to\infty} b_n = L$$

---

## Proof

Given $\varepsilon > 0$:

$\exists\, N_1: n > N_1 \implies |a_n - L| < \varepsilon \implies L - \varepsilon < a_n$

$\exists\, N_2: n > N_2 \implies |c_n - L| < \varepsilon \implies c_n < L + \varepsilon$

For $n > N = \max(N_0, N_1, N_2)$:

$$L - \varepsilon < a_n \leq b_n \leq c_n < L + \varepsilon$$

$$\therefore |b_n - L| < \varepsilon \quad \blacksquare$$

---

## Solved Examples

### Example 1

**Find:** $\displaystyle\lim_{n\to\infty} \frac{\sin n}{n}$

Since $-1 \leq \sin n \leq 1$:

$$-\frac{1}{n} \leq \frac{\sin n}{n} \leq \frac{1}{n}$$

Since $-\frac{1}{n} \to 0$ and $\frac{1}{n} \to 0$, by Squeeze Theorem:

$$\lim_{n\to\infty} \frac{\sin n}{n} = 0 \quad \checkmark$$

---

### Example 2

**Find:** $\displaystyle\lim_{n\to\infty} \frac{\cos(n^2)}{n^2 + 1}$

Since $|\cos(n^2)| \leq 1$:

$$-\frac{1}{n^2+1} \leq \frac{\cos(n^2)}{n^2+1} \leq \frac{1}{n^2+1}$$

Both bounds $\to 0$, so the limit is $\mathbf{0}$. ✓

---

### Example 3

**Find:** $\displaystyle\lim_{n\to\infty} n^{1/n}$

Note: $n^{1/n} = e^{\frac{\ln n}{n}}$ and $\frac{\ln n}{n} \to 0$, so $n^{1/n} \to e^0 = 1$.

**Alternatively (using Squeeze):** For $n \geq 3$, write $n^{1/n} = 1 + h_n$ where $h_n > 0$. By binomial theorem $n \geq \binom{n}{2}h_n^2$, so $h_n \leq \sqrt{\frac{2}{n}} \to 0$.

Thus $1 \leq n^{1/n} \leq 1 + \sqrt{\frac{2}{n}} \to 1$.

$$\lim_{n\to\infty} n^{1/n} = 1 \quad \checkmark$$

---

### Example 4

**Find:** $\displaystyle\lim_{n\to\infty} \frac{2^n}{n!}$

Since $\frac{2^n}{n!} = \frac{2}{1} \cdot \frac{2}{2} \cdot \frac{2}{3} \cdots \frac{2}{n} \leq \frac{4}{n} \cdot \frac{2^{n-2}}{(n-2)!}$... 

More simply: $0 < \frac{2^n}{n!} \leq \frac{4}{n}$ for $n \geq 4$.

By Squeeze: $\lim \frac{2^n}{n!} = 0$. ✓

---

## Standard Limits — Must Know Table

| Limit | Value |
|-------|-------|
| $\displaystyle\lim_{n\to\infty} \frac{1}{n}$ | $0$ |
| $\displaystyle\lim_{n\to\infty} \frac{1}{n^p},\; p>0$ | $0$ |
| $\displaystyle\lim_{n\to\infty} r^n,\; \|r\|<1$ | $0$ |
| $\displaystyle\lim_{n\to\infty} r^n,\; r>1$ | $\infty$ |
| $\displaystyle\lim_{n\to\infty} n^{1/n}$ | $1$ |
| $\displaystyle\lim_{n\to\infty} c^{1/n},\; c>0$ | $1$ |
| $\displaystyle\lim_{n\to\infty} \left(1+\frac{1}{n}\right)^n$ | $e$ |
| $\displaystyle\lim_{n\to\infty} \left(1+\frac{x}{n}\right)^n$ | $e^x$ |
| $\displaystyle\lim_{n\to\infty} \frac{n^k}{a^n},\; a>1$ | $0$ |
| $\displaystyle\lim_{n\to\infty} \frac{a^n}{n!},\; a>0$ | $0$ |
| $\displaystyle\lim_{n\to\infty} \frac{\ln n}{n}$ | $0$ |
| $\displaystyle\lim_{n\to\infty} \frac{\sin n}{n}$ | $0$ |

---

## Key Principle

When a sequence is difficult to evaluate directly, try to **bound it above and below** by simpler sequences. This is the essence of the Squeeze Theorem.
