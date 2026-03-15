---
layout: post
title: "Ratio Test – Statement, Proof & Solved Examples"
date: 2026-03-03
description: "Master the Ratio Test for series convergence — complete statement, proof, and multiple solved examples including factorials and exponentials."
---

The **Ratio Test** (also called D'Alembert's Test) is extremely effective for series involving **factorials**, **exponentials**, and **powers of $n$**.

---

## Statement of the Test

Let $\sum a_n$ be a series of positive terms. Compute:

$$
L = \lim_{n \to \infty} \frac{a_{n+1}}{a_n}
$$

- If $L < 1$ → series **converges absolutely**
- If $L > 1$ (or $L = \infty$) → series **diverges**
- If $L = 1$ → test is **inconclusive**

---

## When to Use It

The Ratio Test works best when $a_n$ contains:
- Factorials: $n!$, $(2n)!$
- Exponentials: $2^n$, $3^n$, $e^n$
- Products of the above

---

## Solved Example 1 — Factorial Series

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{n!}{2^n}$

$$
\frac{a_{n+1}}{a_n} = \frac{(n+1)!}{2^{n+1}} \cdot \frac{2^n}{n!} = \frac{n+1}{2}
$$

$$
L = \lim_{n\to\infty} \frac{n+1}{2} = \infty
$$

Since $L = \infty > 1$, the series **diverges**. ✗

---

## Solved Example 2 — Exponential Series

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{2^n}{n!}$

$$
\frac{a_{n+1}}{a_n} = \frac{2^{n+1}}{(n+1)!} \cdot \frac{n!}{2^n} = \frac{2}{n+1}
$$

$$
L = \lim_{n\to\infty} \frac{2}{n+1} = 0
$$

Since $L = 0 < 1$, the series **converges**. ✓

---

## Solved Example 3 — Combined

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{3^n}$

$$
\frac{a_{n+1}}{a_n} = \frac{(n+1)^2}{3^{n+1}} \cdot \frac{3^n}{n^2} = \frac{1}{3}\left(\frac{n+1}{n}\right)^2
$$

$$
L = \lim_{n\to\infty} \frac{1}{3}\left(1 + \frac{1}{n}\right)^2 = \frac{1}{3}
$$

Since $L = \frac{1}{3} < 1$, the series **converges**. ✓

---

## Solved Example 4 — Inconclusive Case

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2}$

$$
\frac{a_{n+1}}{a_n} = \frac{n^2}{(n+1)^2} \to 1
$$

$L = 1$ → **Inconclusive**. (Use p-Series Test instead: converges since $p=2$.)

---

## Limitation

When $L = 1$, the Ratio Test gives no information. In such cases, switch to the **p-Series Test**, **Comparison Test**, or **Integral Test**.
