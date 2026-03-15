---
layout: default
title: "Problem 1 – Series Convergence"
permalink: /problems/problem1/
---

# Problem 1 — Series Convergence

**Determine the convergence of the following series:**

$$
\sum_{n=1}^{\infty}\frac{1}{n^2+3}
$$

## Solution

We use the **Limit Comparison Test**. Choose the comparison series:

$$
\sum_{n=1}^{\infty}\frac{1}{n^2}
$$

which is a convergent **p-series** with $p = 2 > 1$.

**Step 1:** Compute the limit:

$$
L = \lim_{n\to\infty} \frac{a_n}{b_n} = \lim_{n\to\infty} \frac{\dfrac{1}{n^2+3}}{\dfrac{1}{n^2}} = \lim_{n\to\infty} \frac{n^2}{n^2+3}
$$

**Step 2:** Simplify:

$$
L = \lim_{n\to\infty} \frac{n^2}{n^2+3} = \lim_{n\to\infty} \frac{1}{1 + \frac{3}{n^2}} = 1
$$

**Step 3:** Since $0 < L = 1 < \infty$ and $\sum \frac{1}{n^2}$ converges, by the Limit Comparison Test:

$$
\sum_{n=1}^{\infty}\frac{1}{n^2+3} \quad \textbf{converges.}
$$
