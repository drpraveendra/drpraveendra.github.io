---
layout: post
title: "Limit Comparison Test – Statement, Proof & Solved Examples"
date: 2026-03-01
description: "Learn the Limit Comparison Test for series convergence with clear statement, intuition, and step-by-step solved examples."
---

The **Limit Comparison Test** is one of the most powerful tools for determining whether an infinite series converges or diverges. It is especially useful when the series resembles a simpler known series.

---

## Statement of the Test

Let $\sum a_n$ and $\sum b_n$ be two series with **positive terms**. Compute:

$$
L = \lim_{n \to \infty} \frac{a_n}{b_n}
$$

- If $0 < L < \infty$ — both series **converge or both diverge**
- If $L = 0$ — if $\sum b_n$ converges, then $\sum a_n$ converges
- If $L = \infty$ — if $\sum b_n$ diverges, then $\sum a_n$ diverges

---

## Intuition

If $\frac{a_n}{b_n} \to L$ (a finite nonzero constant), it means $a_n \approx L \cdot b_n$ for large $n$. So both series behave the same — they either both converge or both diverge.

---

## Solved Example 1

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + 3}$

**Step 1:** For large $n$, $\frac{1}{n^2+3} \approx \frac{1}{n^2}$. Choose $b_n = \frac{1}{n^2}$.

**Step 2:** Compute:

$$
L = \lim_{n\to\infty} \frac{\frac{1}{n^2+3}}{\frac{1}{n^2}} = \lim_{n\to\infty} \frac{n^2}{n^2+3} = 1
$$

**Step 3:** Since $L = 1$ and $\sum \frac{1}{n^2}$ converges (p-series, $p=2$), the given series **converges**. ✓

---

## Solved Example 2

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{3n^2 + 2}{5n^4 - n + 1}$

Choose $b_n = \frac{1}{n^2}$.

$$
L = \lim_{n\to\infty} \frac{\frac{3n^2+2}{5n^4-n+1}}{\frac{1}{n^2}} = \lim_{n\to\infty} \frac{3n^4+2n^2}{5n^4-n+1} = \frac{3}{5}
$$

Since $0 < \frac{3}{5} < \infty$ and $\sum \frac{1}{n^2}$ converges, the series **converges**. ✓

---

## Solved Example 3

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{\sqrt{n}}{n^2 - 1}$

For large $n$: $\frac{\sqrt{n}}{n^2} = \frac{1}{n^{3/2}}$. Choose $b_n = \frac{1}{n^{3/2}}$.

$$
L = \lim_{n\to\infty} \frac{\frac{\sqrt{n}}{n^2-1}}{\frac{1}{n^{3/2}}} = \lim_{n\to\infty} \frac{n^{3/2} \cdot \sqrt{n}}{n^2-1} = \lim_{n\to\infty} \frac{n^2}{n^2-1} = 1
$$

Since $\sum \frac{1}{n^{3/2}}$ converges (p-series, $p = \frac{3}{2} > 1$), the series **converges**. ✓

---

## Key Tip

Always identify the **dominant terms** in numerator and denominator to choose your comparison series. The best comparison is usually a **p-series** $\sum \frac{1}{n^p}$.
