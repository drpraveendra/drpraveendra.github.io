---
layout: post
title: "Raabe's Test – The Test That Works When Ratio Test Fails"
date: 2026-03-15
description: "Learn Raabe's Test — a higher-order convergence test that resolves cases where the Ratio Test is inconclusive (L=1). Includes full statement and solved examples."
---

**Raabe's Test** is a refinement of the Ratio Test. It is used specifically when the Ratio Test gives $L = 1$ (inconclusive). Raabe's Test goes one level deeper to determine convergence.

---

## Statement of Raabe's Test

Let $\sum a_n$ be a series of positive terms. Compute:

$$
R = \lim_{n\to\infty} n\left(\frac{a_n}{a_{n+1}} - 1\right)
$$

- If $R > 1$ → series **converges**
- If $R < 1$ → series **diverges**
- If $R = 1$ → test is **inconclusive**

---

## Equivalent Form

Equivalently, writing $L_n = \frac{a_{n+1}}{a_n}$:

$$
R = \lim_{n\to\infty} n(1 - L_n)
$$

---

## Why Ratio Test Fails Here

When $\lim \frac{a_{n+1}}{a_n} = 1$, all p-series $\sum \frac{1}{n^p}$ give $L = 1$, regardless of whether they converge or diverge. So we need a finer test.

Raabe's test effectively checks whether $a_n$ decays like $\frac{1}{n^p}$ with $p > 1$ or $p \leq 1$.

---

## Solved Example 1

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{(2n)!}{4^n (n!)^2}$

Compute:

$$
\frac{a_{n+1}}{a_n} = \frac{(2n+2)!}{4^{n+1}((n+1)!)^2} \cdot \frac{4^n(n!)^2}{(2n)!} = \frac{(2n+2)(2n+1)}{4(n+1)^2}
$$

$$
= \frac{(2n+1)}{2(n+1)} \to 1 \quad \text{(Ratio Test inconclusive)}
$$

Apply Raabe's Test:

$$
n\left(\frac{a_n}{a_{n+1}} - 1\right) = n\left(\frac{2(n+1)}{2n+1} - 1\right) = n \cdot \frac{1}{2n+1} \to \frac{1}{2}
$$

Since $R = \frac{1}{2} < 1$, the series **diverges**. ✗

---

## Solved Example 2

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1 \cdot 3 \cdot 5 \cdots (2n-1)}{2 \cdot 4 \cdot 6 \cdots (2n)} \cdot \frac{1}{2n+1}$

Let $a_n = \frac{1\cdot3\cdots(2n-1)}{2\cdot4\cdots(2n)(2n+1)}$.

$$
\frac{a_{n+1}}{a_n} = \frac{2n+1}{(2n+2)(2n+3)} \to 1
$$

Ratio Test: inconclusive. Apply Raabe's:

$$
R = \lim_{n\to\infty} n\left(\frac{(2n+2)(2n+3)}{(2n+1)^2} - 1\right) = \lim_{n\to\infty} n \cdot \frac{8n+5}{(2n+1)^2} = \lim_{n\to\infty} \frac{8n^2+5n}{4n^2+\cdots} = 2
$$

Since $R = 2 > 1$, the series **converges**. ✓

---

## Hierarchy of Tests

When one test is inconclusive, move to the next:

$$
\text{Divergence Test} \to \text{Ratio/Root Test} \to \text{Raabe's Test} \to \text{Gauss's Test}
$$

Each test is more sensitive than the previous one at the boundary $L = 1$.

---

## Key Formula

$$
\boxed{R = \lim_{n\to\infty} n\left(\frac{a_n}{a_{n+1}} - 1\right)}
$$

If $R > 1$: **converges**. If $R < 1$: **diverges**. If $R = 1$: try a higher-order test.
