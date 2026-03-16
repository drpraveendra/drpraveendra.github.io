---
layout: post
title: "Heine-Cantor Theorem & Uniform Continuity – Complete Guide"
date: 2026-02-11
description: "A complete guide to uniform continuity — epsilon-delta definition, differences from pointwise continuity, the Heine-Cantor theorem, and solved examples."
---

**Uniform continuity** is a stronger form of continuity where the same $\delta$ works for all points simultaneously. It is crucial for integration theory and approximation.

---

## Continuity vs Uniform Continuity

**Continuous at a point $a$:** $\delta$ may depend on both $\varepsilon$ and $a$

$$\forall\, \varepsilon > 0,\; \forall\, a,\; \exists\, \delta(\varepsilon, a) > 0: |x-a|<\delta \implies |f(x)-f(a)|<\varepsilon$$

**Uniformly continuous on $S$:** $\delta$ depends only on $\varepsilon$

$$\forall\, \varepsilon > 0,\; \exists\, \delta(\varepsilon) > 0: \forall\, x,y \in S,\; |x-y|<\delta \implies |f(x)-f(y)|<\varepsilon$$

Every uniformly continuous function is continuous, but not conversely.

---

## Heine-Cantor Theorem

**Theorem:** If $f: [a,b] \to \mathbb{R}$ is **continuous** on a **closed bounded interval**, then $f$ is **uniformly continuous** on $[a,b]$.

**Proof sketch:** Suppose not. Then $\exists\, \varepsilon_0 > 0$ and sequences $x_n, y_n$ with $|x_n - y_n| < \frac{1}{n}$ but $|f(x_n) - f(y_n)| \geq \varepsilon_0$.

Since $[a,b]$ is compact, $\{x_n\}$ has a subsequence $x_{n_k} \to c \in [a,b]$. Then $y_{n_k} \to c$ too. By continuity, $f(x_{n_k}) \to f(c)$ and $f(y_{n_k}) \to f(c)$, so $|f(x_{n_k}) - f(y_{n_k})| \to 0$ — contradiction. $\blacksquare$

---

## Examples

### Uniformly Continuous

**1.** $f(x) = x^2$ on $[0, 5]$:
Compact domain → uniformly continuous by Heine-Cantor. ✓

**2.** $f(x) = \sin x$ on $\mathbb{R}$:

$$|f(x)-f(y)| = |\sin x - \sin y| \leq |x-y|$$

Take $\delta = \varepsilon$. Uniformly continuous on all of $\mathbb{R}$. ✓

**3.** Any **Lipschitz function:** $|f(x)-f(y)| \leq L|x-y|$, take $\delta = \varepsilon/L$. ✓

---

### NOT Uniformly Continuous

**1.** $f(x) = x^2$ on $\mathbb{R}$:

Take $x_n = n + \frac{1}{n}$, $y_n = n$. Then $|x_n - y_n| = \frac{1}{n} \to 0$ but:

$$|f(x_n)-f(y_n)| = \left(n+\frac{1}{n}\right)^2 - n^2 = 2 + \frac{1}{n^2} \to 2 \neq 0$$

Not uniformly continuous on $\mathbb{R}$. ✗

**2.** $f(x) = \frac{1}{x}$ on $(0,1)$:

Take $x_n = \frac{1}{n}$, $y_n = \frac{1}{n+1}$. Then $|x_n - y_n| \to 0$ but:

$$|f(x_n) - f(y_n)| = |n - (n+1)| = 1 \not\to 0$$

Not uniformly continuous. ✗

---

## Lipschitz Condition

**Definition:** $f$ satisfies a **Lipschitz condition** on $S$ if $\exists\, L > 0$:

$$|f(x) - f(y)| \leq L|x-y| \quad \forall\, x,y \in S$$

$$\text{Lipschitz} \implies \text{Uniformly Continuous} \implies \text{Continuous}$$

None of these implications reverse in general.

---

## Extension Theorem

**Theorem:** If $f$ is uniformly continuous on $(a,b)$, then $f$ extends uniquely to a continuous function on $[a,b]$.

This fails for merely continuous functions: $f(x) = \sin\frac{1}{x}$ on $(0,1)$ is continuous but has no continuous extension to $[0,1]$.
