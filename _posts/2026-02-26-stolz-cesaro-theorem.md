---
layout: post
title: "Stolz-Cesàro Theorem – The L'Hôpital's Rule for Sequences"
date: 2026-02-26
description: "Learn the Stolz-Cesàro theorem — a powerful tool for evaluating indeterminate limits of sequences of the form 0/0 or ∞/∞. Includes proof and multiple solved examples."
---

The **Stolz-Cesàro Theorem** is the discrete analogue of L'Hôpital's rule. It is used to evaluate limits of sequences in indeterminate forms $\frac{0}{0}$ or $\frac{\infty}{\infty}$.

---

## Statement

**Theorem (Stolz-Cesàro):** Let $\{a_n\}$ and $\{b_n\}$ be sequences where $\{b_n\}$ is **strictly increasing** and **unbounded** ($b_n \to +\infty$). If:

$$\lim_{n\to\infty} \frac{a_{n+1} - a_n}{b_{n+1} - b_n} = L$$

then:

$$\lim_{n\to\infty} \frac{a_n}{b_n} = L$$

(where $L$ can be finite, $+\infty$, or $-\infty$.)

---

## Intuition

Just as L'Hôpital replaces $\frac{f(x)}{g(x)}$ with $\frac{f'(x)}{g'(x)}$, Stolz-Cesàro replaces $\frac{a_n}{b_n}$ with the ratio of **differences** $\frac{\Delta a_n}{\Delta b_n}$, where $\Delta a_n = a_{n+1} - a_n$.

---

## Solved Examples

### Example 1: Arithmetic Mean

**Find:** $\displaystyle\lim_{n\to\infty} \frac{1+2+3+\cdots+n}{n^2}$

Let $a_n = 1+2+\cdots+n$, $b_n = n^2$.

$b_n$ is strictly increasing and unbounded. ✓

$$\frac{a_{n+1}-a_n}{b_{n+1}-b_n} = \frac{n+1}{(n+1)^2 - n^2} = \frac{n+1}{2n+1} \to \frac{1}{2}$$

By Stolz-Cesàro: $\displaystyle\lim \frac{a_n}{b_n} = \frac{1}{2}$

*(Cross-check: $\frac{n(n+1)/2}{n^2} = \frac{n+1}{2n} \to \frac{1}{2}$ ✓)*

---

### Example 2

**Find:** $\displaystyle\lim_{n\to\infty} \frac{1^2 + 2^2 + \cdots + n^2}{n^3}$

Let $a_n = \sum_{k=1}^n k^2$, $b_n = n^3$.

$$\frac{a_{n+1}-a_n}{b_{n+1}-b_n} = \frac{(n+1)^2}{(n+1)^3 - n^3} = \frac{n^2+2n+1}{3n^2+3n+1} \to \frac{1}{3}$$

$$\therefore \lim_{n\to\infty} \frac{1^2+2^2+\cdots+n^2}{n^3} = \frac{1}{3}$$

---

### Example 3

**Find:** $\displaystyle\lim_{n\to\infty} \frac{\ln(n!)}{n\ln n}$

Let $a_n = \ln(n!) = \sum_{k=1}^n \ln k$, $b_n = n\ln n$.

$$\frac{a_{n+1}-a_n}{b_{n+1}-b_n} = \frac{\ln(n+1)}{(n+1)\ln(n+1) - n\ln n}$$

$$= \frac{\ln(n+1)}{\ln(n+1) + n\ln\frac{n+1}{n}} \approx \frac{\ln n}{\ln n + n \cdot \frac{1}{n}} = \frac{\ln n}{\ln n + 1} \to 1$$

$$\therefore \lim_{n\to\infty} \frac{\ln(n!)}{n\ln n} = 1$$

*(This recovers Stirling's approximation direction: $\ln(n!) \sim n\ln n$)*

---

### Example 4 — Cesàro Mean

**Theorem (Cesàro Mean):** If $a_n \to L$, then:

$$\frac{a_1 + a_2 + \cdots + a_n}{n} \to L$$

**Proof using Stolz-Cesàro:** Let $A_n = a_1 + \cdots + a_n$, $b_n = n$.

$$\frac{A_{n+1} - A_n}{b_{n+1} - b_n} = \frac{a_{n+1}}{1} = a_{n+1} \to L$$

By Stolz-Cesàro: $\frac{A_n}{n} \to L$. $\blacksquare$

---

## Important Note

The converse of Cesàro mean is **FALSE**:

$a_n = (-1)^n$ diverges, but $\frac{a_1+\cdots+a_n}{n} \to 0$.

Cesàro summability is weaker than ordinary convergence.
