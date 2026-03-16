---
layout: post
title: "Point Set Topology in ℝ – Complete Summary & CSIR NET Problems"
date: 2026-02-13
description: "A complete summary of Point Set Topology in ℝ with key theorems, a quick-reference table, and solved CSIR NET / GATE style problems."
---

This post consolidates all major results in **Point Set Topology in $\mathbb{R}$** and provides CSIR NET / GATE style solved problems.

---

## Quick Reference — Key Definitions

| Concept | Definition |
|---------|-----------|
| Open set | Every point has an $\varepsilon$-neighbourhood inside the set |
| Closed set | Complement is open / contains all limit points |
| Limit point | Every neighbourhood contains another point of the set |
| Closure $\bar{S}$ | $S \cup S'$ — smallest closed set containing $S$ |
| Interior $S^\circ$ | Largest open set contained in $S$ |
| Boundary $\partial S$ | $\bar{S} \setminus S^\circ$ |
| Compact | Closed and bounded (Heine-Borel) |
| Connected | Cannot be separated into two disjoint open sets |
| Dense | $\bar{S} = \mathbb{R}$ |
| Perfect | Closed + every point is a limit point |

---

## Key Theorems at a Glance

| Theorem | Statement |
|---------|-----------|
| **Heine-Borel** | $K$ compact $\iff$ $K$ closed and bounded |
| **Bolzano-Weierstrass** | Every bounded infinite set has a limit point |
| **Completeness** | Every Cauchy sequence in $\mathbb{R}$ converges |
| **Nested Intervals** | Nested closed intervals have non-empty intersection |
| **Baire Category** | $\mathbb{R}$ is second category |
| **IVT** | Continuous image of connected set is connected |
| **EVT** | Continuous image of compact set is compact |
| **Heine-Cantor** | Continuous on compact $\implies$ uniformly continuous |

---

## CSIR NET Style Solved Problems

### Problem 1
**Which of the following is NOT open in $\mathbb{R}$?**

(a) $(0,1)$ (b) $\mathbb{R}$ (c) $\emptyset$ (d) $[0,1)$

**Solution:** $[0,1)$ — the point $0$ has no $\varepsilon$-neighbourhood contained in $[0,1)$. **Answer: (d)** ✓

---

### Problem 2
**The derived set of $S = \left\{\frac{1}{n} : n \in \mathbb{N}\right\}$ is:**

**Solution:** Every neighbourhood of $0$ contains $\frac{1}{n}$ for large $n$. No other point is a limit point (points are isolated). So $S' = \{0\}$. ✓

---

### Problem 3
**Which of these sets is compact?**

(a) $(0,1)$ (b) $[1,\infty)$ (c) $[-2, 5]$ (d) $\mathbb{Q} \cap [0,1]$

**Solution:**
- (a) Not closed ✗
- (b) Not bounded ✗
- (c) Closed and bounded ✓ → **compact**
- (d) Not closed (limit points like $\frac{1}{\sqrt{2}}$ not in $\mathbb{Q}$) ✗

**Answer: (c)** ✓

---

### Problem 4
**True or False: Every infinite subset of a compact set is compact.**

**Solution:** **False**. Counterexample: $K = [0,1]$ is compact. $S = (0,1) \subset K$ is infinite but not compact (not closed). ✓

---

### Problem 5
**The interior of $\mathbb{Q}$ in $\mathbb{R}$ is:**

**Solution:** $\text{int}(\mathbb{Q}) = \emptyset$ — no open interval is entirely rational. ✓

---

### Problem 6
**Is $f(x) = x\sin x$ uniformly continuous on $\mathbb{R}$?**

**Solution:** No. The derivative $f'(x) = \sin x + x\cos x$ is unbounded on $\mathbb{R}$, so $f$ is not Lipschitz. In fact, take $x_n = 2n\pi$ and $y_n = 2n\pi + \frac{1}{n}$: $|x_n - y_n| \to 0$ but $|f(x_n) - f(y_n)| \to \infty$. **Not uniformly continuous.** ✗

---

### Problem 7
**The Cantor set is:**
(a) Countable and closed (b) Uncountable and open (c) Uncountable, closed, nowhere dense (d) Finite

**Answer: (c)** — Uncountable, closed, nowhere dense, measure zero. ✓

---

## Common Mistakes to Avoid

1. $\lim a_n = L$ does not mean $L \in S$ (infimum need not be in the set)
2. Infinite unions of closed sets need NOT be closed
3. Infinite intersections of open sets need NOT be open
4. $\mathbb{Q}$ is **countable** but **dense** in $\mathbb{R}$ — countable sets can be dense!
5. Compact $\not\Rightarrow$ every subset is compact
6. Uniform continuity implies continuity, but **not** conversely
