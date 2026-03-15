---
layout: post
title: "Limit Comparison Test Explained"
date: 2026-03-09
permalink: /blog/limit-comparison-test/
description: "A complete explanation of the Limit Comparison Test for series convergence with step-by-step solved examples."
---

The **Limit Comparison Test** is one of the most powerful and elegant tools for determining whether an infinite series converges or diverges. It is especially useful when direct comparison is difficult.

## Statement of the Test

Let $\sum a_n$ and $\sum b_n$ be two series with **positive terms**. Compute the limit:

$$
L = \lim_{n\to\infty} \frac{a_n}{b_n}
$$

Then:
- If $0 < L < \infty$ — both series **converge or both diverge**
- If $L = 0$ — if $\sum b_n$ converges, then $\sum a_n$ also converges
- If $L = \infty$ — if $\sum b_n$ diverges, then $\sum a_n$ also diverges

---

## When to Use It

Use the Limit Comparison Test when:
- The series looks like a rational function of $n$
- Direct comparison is not straightforward
- You can identify a simpler "comparison series" (usually a p-series)

---

## Solved Example 1

**Test the convergence of:**

$$
\sum_{n=1}^{\infty} \frac{1}{n^2 + 3}
$$

**Solution:** Compare with $\sum \frac{1}{n^2}$ (convergent p-series, $p=2$).

$$
L = \lim_{n\to\infty} \frac{\frac{1}{n^2+3}}{\frac{1}{n^2}} = \lim_{n\to\infty} \frac{n^2}{n^2+3} = 1
$$

Since $0 < 1 < \infty$ and $\sum \frac{1}{n^2}$ converges, the given series **converges**.

---

## Solved Example 2

**Test the convergence of:**

$$
\sum_{n=1}^{\infty} \frac{3n^2 + 2}{5n^4 - n + 1}
$$

**Solution:** For large $n$, the dominant terms give $\frac{3n^2}{5n^4} = \frac{3}{5n^2}$. So compare with $\sum \frac{1}{n^2}$.

$$
L = \lim_{n\to\infty} \frac{\frac{3n^2+2}{5n^4-n+1}}{\frac{1}{n^2}} = \lim_{n\to\infty} \frac{n^2(3n^2+2)}{5n^4-n+1} = \lim_{n\to\infty} \frac{3n^4+2n^2}{5n^4-n+1} = \frac{3}{5}
$$

Since $0 < \frac{3}{5} < \infty$ and $\sum \frac{1}{n^2}$ converges, the given series **converges**.

---

## Key Takeaway

Always look at the **highest degree terms** in numerator and denominator to choose your comparison series. The Limit Comparison Test turns a complicated series into a simple limit calculation.

---

*For more solved problems, visit the [Problems Section](/problems/problem1/).*
