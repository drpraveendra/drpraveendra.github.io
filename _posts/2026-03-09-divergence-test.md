---
layout: post
title: "Divergence Test (nth Term Test) – The First Test to Always Apply"
date: 2026-03-09
description: "The Divergence Test is the quickest way to detect divergence. Learn its statement, common mistakes, and when it is and isn't useful."
---

The **Divergence Test** (also called the **nth Term Test**) is the **first test you should always apply** before trying any other convergence test. It can quickly rule out convergence with minimal effort.

---

## Statement

If $\displaystyle\lim_{n\to\infty} a_n \neq 0$, then $\sum a_n$ **diverges**.

Equivalently: If $\sum a_n$ converges, then $\lim_{n\to\infty} a_n = 0$.

---

## The Critical Warning ⚠️

**The converse is FALSE.**

$$
\lim_{n\to\infty} a_n = 0 \;\;\not\!\!\!\implies \sum a_n \text{ converges}
$$

**Example:** $\sum \frac{1}{n}$ (Harmonic series) — here $a_n = \frac{1}{n} \to 0$, but the series **diverges**.

The Divergence Test can only **prove divergence**, never convergence.

---

## Solved Example 1 — Clear Divergence

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{n}{n+1}$

$$
\lim_{n\to\infty} \frac{n}{n+1} = 1 \neq 0
$$

→ Series **diverges**. ✗

---

## Solved Example 2

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{2n^2 + 3}$

$$
\lim_{n\to\infty} \frac{n^2}{2n^2+3} = \frac{1}{2} \neq 0
$$

→ Series **diverges**. ✗

---

## Solved Example 3 — Test is Inconclusive

**Test:** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2}$

$$
\lim_{n\to\infty} \frac{1}{n^2} = 0
$$

The Divergence Test is **inconclusive** here. (Use p-Series Test: converges since $p=2$.)

---

## Solved Example 4 — Oscillating Terms

**Test:** $\displaystyle\sum_{n=1}^{\infty} (-1)^n$

$$
\lim_{n\to\infty} (-1)^n \text{ does not exist}
$$

Since the limit doesn't equal 0 (it doesn't even exist), the series **diverges**. ✗

---

## Decision Flowchart

```
Start with any series ∑aₙ
        ↓
Compute lim(n→∞) aₙ
        ↓
  ≠ 0 or DNE?  →  DIVERGES ✗  (stop here)
        ↓
       = 0?
        ↓
  INCONCLUSIVE → Apply another test
```

---

## Summary

| Result | Conclusion |
|--------|------------|
| $\lim a_n \neq 0$ | **Definitely diverges** |
| $\lim a_n = 0$ | **Inconclusive** — need another test |
| $\lim a_n$ DNE | **Definitely diverges** |

Always check this test first — it takes 10 seconds and can save a lot of work.
