---
layout: post
title: "Telescoping Series – How to Find the Exact Sum"
date: 2026-03-13
description: "Learn how to identify and evaluate telescoping series using partial fractions. Includes step-by-step examples showing how most terms cancel."
---

A **Telescoping Series** is one where most terms cancel when you write out the partial sums — just like a collapsing telescope. These series are special because you can often find their **exact sum**.

---

## Definition

A series $\sum (b_n - b_{n+1})$ is telescoping because:

$$
S_N = (b_1 - b_2) + (b_2 - b_3) + \cdots + (b_N - b_{N+1}) = b_1 - b_{N+1}
$$

If $\lim_{N\to\infty} b_{N+1} = L$, then:

$$
\sum_{n=1}^{\infty} (b_n - b_{n+1}) = b_1 - L
$$

---

## How to Identify Telescoping Series

Use **partial fraction decomposition** to write $a_n$ as a difference:

$$
a_n = f(n) - f(n+1)
$$

---

## Solved Example 1

**Find the sum:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$

**Step 1:** Partial fractions:

$$
\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}
$$

**Step 2:** Write partial sums:

$$
S_N = \left(1 - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+1}\right) = 1 - \frac{1}{N+1}
$$

**Step 3:** Take limit:

$$
S = \lim_{N\to\infty} \left(1 - \frac{1}{N+1}\right) = 1
$$

$$
\boxed{\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = 1}
$$

---

## Solved Example 2

**Find the sum:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n(n+2)}$

**Partial fractions:**

$$
\frac{1}{n(n+2)} = \frac{1}{2}\left(\frac{1}{n} - \frac{1}{n+2}\right)
$$

**Partial sums:**

$$
S_N = \frac{1}{2}\left[\left(1 - \frac{1}{3}\right) + \left(\frac{1}{2} - \frac{1}{4}\right) + \left(\frac{1}{3} - \frac{1}{5}\right) + \cdots \right]
$$

After cancellation, only first two and last two terms survive:

$$
S_N = \frac{1}{2}\left(1 + \frac{1}{2} - \frac{1}{N+1} - \frac{1}{N+2}\right)
$$

$$
S = \frac{1}{2}\left(1 + \frac{1}{2}\right) = \frac{3}{4}
$$

$$
\boxed{\sum_{n=1}^{\infty} \frac{1}{n(n+2)} = \frac{3}{4}}
$$

---

## Solved Example 3 — With Square Roots

**Find the sum:** $\displaystyle\sum_{n=1}^{\infty} \left(\sqrt{n+1} - \sqrt{n}\right)$

$$
S_N = (\sqrt{2}-\sqrt{1}) + (\sqrt{3}-\sqrt{2}) + \cdots + (\sqrt{N+1}-\sqrt{N}) = \sqrt{N+1} - 1
$$

$$
S = \lim_{N\to\infty}(\sqrt{N+1}-1) = \infty
$$

→ Series **diverges**. ✗

---

## Key Steps

1. Apply **partial fractions** to express $a_n$ as a difference
2. Write out the **partial sum** $S_N$
3. Cancel middle terms
4. Take $\lim_{N\to\infty} S_N$
