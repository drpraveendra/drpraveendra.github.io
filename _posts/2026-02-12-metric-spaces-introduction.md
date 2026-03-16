---
layout: post
title: "Metric Spaces – Definition, Examples & Basic Topology"
date: 2026-02-12
description: "Introduction to metric spaces — axiomatic definition, standard examples including discrete and p-adic metrics, open and closed balls, and topology induced by a metric."
---

A **metric space** is a set equipped with a notion of distance. It generalizes the topology of $\mathbb{R}$ to abstract settings, and is the natural framework for analysis on general sets.

---

## Definition of a Metric Space

**Definition:** A **metric space** is a pair $(X, d)$ where $X$ is a set and $d: X \times X \to \mathbb{R}$ is a **metric** (distance function) satisfying:

For all $x, y, z \in X$:

1. **Non-negativity:** $d(x,y) \geq 0$
2. **Identity:** $d(x,y) = 0 \iff x = y$
3. **Symmetry:** $d(x,y) = d(y,x)$
4. **Triangle Inequality:** $d(x,z) \leq d(x,y) + d(y,z)$

---

## Standard Examples

### 1. Euclidean Metric on $\mathbb{R}$

$$d(x,y) = |x-y|$$

This is the standard metric we use throughout real analysis.

### 2. Euclidean Metric on $\mathbb{R}^n$

$$d(\mathbf{x}, \mathbf{y}) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}$$

### 3. Discrete Metric

$$d(x,y) = \begin{cases} 0 & x = y \\ 1 & x \neq y \end{cases}$$

Every set becomes a metric space with this metric. Open balls: $B(x,r) = \{x\}$ for $r \leq 1$, $B(x,r) = X$ for $r > 1$.

### 4. Taxicab (Manhattan) Metric on $\mathbb{R}^2$

$$d(\mathbf{x},\mathbf{y}) = |x_1 - y_1| + |x_2 - y_2|$$

### 5. Supremum Metric on $C[a,b]$

$$d(f,g) = \sup_{x \in [a,b]} |f(x) - g(x)|$$

---

## Open and Closed Balls

In a metric space $(X,d)$:

**Open ball:** $B(x,r) = \{y \in X : d(x,y) < r\}$

**Closed ball:** $\bar{B}(x,r) = \{y \in X : d(x,y) \leq r\}$

**Sphere:** $S(x,r) = \{y \in X : d(x,y) = r\}$

---

## Topology Induced by a Metric

**Open sets** in $(X,d)$: $G \subseteq X$ is open if every point has an open ball contained in $G$:

$$\forall\, x \in G,\; \exists\, r > 0: B(x,r) \subseteq G$$

This is exactly the definition we used for $\mathbb{R}$ — just replacing $N_\varepsilon(x)$ with $B(x,r)$.

---

## Equivalent Metrics

Two metrics $d_1$ and $d_2$ on $X$ are **equivalent** if they induce the same open sets (same topology).

**Example:** On $\mathbb{R}^2$, the Euclidean metric, taxicab metric, and supremum metric all induce the **same topology** — the open sets are the same.

---

## Complete Metric Spaces

**Definition:** $(X,d)$ is **complete** if every Cauchy sequence in $X$ converges to a point in $X$.

| Space | Complete? |
|-------|-----------|
| $(\mathbb{R}, |\cdot|)$ | ✓ |
| $(\mathbb{Q}, |\cdot|)$ | ✗ |
| $(C[a,b], d_\infty)$ | ✓ |
| $((0,1), |\cdot|)$ | ✗ |

---

## Why Metric Spaces?

By studying metric spaces abstractly, we prove theorems once and apply them to:
- $\mathbb{R}^n$ and $\mathbb{C}^n$
- Function spaces $C[a,b]$, $L^p$ spaces
- Sequence spaces $\ell^p$
- Differential equations as fixed points in metric spaces
