---
layout: post
title: "Continuity in Terms of Open Sets – Topological Characterization"
date: 2026-02-10
description: "Learn the topological definition of continuity using open sets — how it generalizes the epsilon-delta definition, with proofs and key theorems."
---

The **topological definition of continuity** using open sets is more elegant and general than the $\varepsilon$-$\delta$ definition. Understanding both and their equivalence is essential for real analysis and topology.

---

## Epsilon-Delta Definition (Recall)

$f: \mathbb{R} \to \mathbb{R}$ is **continuous at $a$** if:

$$
\forall\, \varepsilon > 0,\quad \exists\, \delta > 0 \text{ such that } |x - a| < \delta \implies |f(x) - f(a)| < \varepsilon
$$

---

## Topological Definition of Continuity

**Definition:** $f: \mathbb{R} \to \mathbb{R}$ is **continuous** if for every open set $V \subseteq \mathbb{R}$, the **preimage**:

$$
f^{-1}(V) = \{x \in \mathbb{R} : f(x) \in V\}
$$

is open in $\mathbb{R}$.

---

## Equivalence

**Theorem:** The $\varepsilon$-$\delta$ definition and the open set definition of continuity are **equivalent**.

**Proof sketch ($\Rightarrow$):** Let $V$ be open and $a \in f^{-1}(V)$. Then $f(a) \in V$, so $\exists\, \varepsilon > 0: N_\varepsilon(f(a)) \subseteq V$. By $\varepsilon$-$\delta$ continuity, $\exists\, \delta > 0: f(N_\delta(a)) \subseteq N_\varepsilon(f(a)) \subseteq V$. So $N_\delta(a) \subseteq f^{-1}(V)$, making $f^{-1}(V)$ open. $\blacksquare$

---

## Continuity via Closed Sets

**Equivalent condition:** $f$ is continuous $\iff$ the preimage of every **closed** set is **closed**.

Since $f^{-1}(V^c) = (f^{-1}(V))^c$, this follows immediately from the open set definition.

---

## Topological Properties Preserved by Continuity

If $f: \mathbb{R} \to \mathbb{R}$ is continuous:

1. **Compact $\to$ Compact:** If $K$ is compact, then $f(K)$ is compact
2. **Connected $\to$ Connected:** If $S$ is connected, then $f(S)$ is connected
3. **Extreme Value Theorem:** $f$ attains max and min on any compact set
4. **Intermediate Value Theorem:** $f$ takes all intermediate values on connected sets

---

## Uniform Continuity

**Definition:** $f$ is **uniformly continuous** on $S$ if:

$$
\forall\, \varepsilon > 0,\quad \exists\, \delta > 0 \text{ s.t. } \forall\, x, y \in S: |x-y| < \delta \implies |f(x)-f(y)| < \varepsilon
$$

The key difference: $\delta$ depends only on $\varepsilon$, not on the point $x$.

**Theorem (Heine-Cantor):** If $f$ is continuous on a **compact** set $K$, then $f$ is **uniformly continuous** on $K$.

---

## Example — Non-Uniform Continuity

$f(x) = \frac{1}{x}$ on $(0,1)$:

- Continuous on $(0,1)$ ✓
- **NOT** uniformly continuous — near $x=0$, small changes in $x$ cause large changes in $f(x)$ ✗

But $f(x) = \frac{1}{x}$ on $[0.1, 1]$ is uniformly continuous (compact domain). ✓

---

## Homeomorphism

**Definition:** $f: S \to T$ is a **homeomorphism** if:
- $f$ is a bijection
- $f$ is continuous
- $f^{-1}$ is continuous

Two sets are **topologically equivalent (homeomorphic)** if a homeomorphism exists between them.

**Examples:**
- $(0,1)$ and $\mathbb{R}$ are homeomorphic via $f(x) = \tan(\pi x - \frac{\pi}{2})$
- $(0,1)$ and $[0,1]$ are **NOT** homeomorphic — one is compact, the other isn't
