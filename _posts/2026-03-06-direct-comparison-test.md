---
layout: post
title: "Direct Comparison Test – Statement & Solved Examples"
date: 2026-03-06
description: "Learn the Direct Comparison Test for series — how to choose the right comparison series and apply the test with step-by-step examples."
---

The **Direct Comparison Test** is the most straightforward convergence test. If you can bound a series above or below by a known series, you can immediately determine convergence or divergence.

---

## Statement of the Test

Let $\sum a_n$ and $\sum b_n$ be series with **non-negative terms** such that $a_n \leq b_n$ for all $n$.

- If $\sum b_n$ **converges** → $\sum a_n$ also **converges**
- If $\sum a_n$ **diverges** → $\sum b_n$ also **diverges**

**Memory trick:** A smaller series than a convergent series must converge. A larger series than a divergent series must diverge.

---

## Choosing the Right Comparison Series

The best comparison series are:
- **p-Series**: $\sum \frac{1}{n^p}$
- **Geometric Series**: $\sum ar^n$

Always look at the **dominant terms** of $a_n$.

---

## Solved Example 1 — Convergence

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + n}$

Since $n^2 + n > n^2$ for all $n \geq 1$:

$$
\frac{1}{n^2 + n} < \frac{1}{n^2}
$$

Since $\sum \frac{1}{n^2}$ converges (p-series, $p=2$) and $a_n < b_n$, the series **converges**. ✓

---

## Solved Example 2 — Convergence with Geometric Series

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{\sin^2 n}{2^n}$

Since $\sin^2 n \leq 1$ for all $n$:

$$
\frac{\sin^2 n}{2^n} \leq \frac{1}{2^n}
$$

Since $\sum \frac{1}{2^n}$ is a convergent geometric series ($r = \frac{1}{2} < 1$), the series **converges**. ✓

---

## Solved Example 3 — Divergence

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{\sqrt{n} + 1}$

Since $\sqrt{n} + 1 \leq 2\sqrt{n}$ for $n \geq 1$:

$$
\frac{1}{\sqrt{n}+1} \geq \frac{1}{2\sqrt{n}} = \frac{1}{2} \cdot \frac{1}{n^{1/2}}
$$

Since $\sum \frac{1}{n^{1/2}}$ diverges (p-series, $p = \frac{1}{2} \leq 1$), and our series is larger (up to a constant), it **diverges**. ✗

---

## Solved Example 4

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{n+1}{n^3}$

$$
\frac{n+1}{n^3} = \frac{1}{n^2} + \frac{1}{n^3} \leq \frac{1}{n^2} + \frac{1}{n^2} = \frac{2}{n^2}
$$

Since $\sum \frac{2}{n^2}$ converges, the series **converges**. ✓

---

## Direct vs Limit Comparison

| Situation | Use |
|-----------|-----|
| Easy to establish $a_n \leq b_n$ directly | Direct Comparison |
| Hard to establish inequality but ratio is simple | Limit Comparison |

When Direct Comparison is hard to set up, switch to the **Limit Comparison Test**.
