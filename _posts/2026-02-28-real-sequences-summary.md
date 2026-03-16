---
layout: post
title: "Real Sequences – Complete Summary & CSIR NET / GATE Problems"
date: 2026-02-28
description: "A complete summary of Real Sequences with all key theorems, a quick-reference table, and 10 fully solved CSIR NET and GATE style problems."
---

This post consolidates the entire topic of **Real Sequences** with a reference table and solved exam-style problems.

---

## Quick Reference — All Key Theorems

| Theorem | Statement |
|---------|-----------|
| **Uniqueness of Limit** | A convergent sequence has exactly one limit |
| **Convergent $\Rightarrow$ Bounded** | Every convergent sequence is bounded |
| **Monotone Convergence (MCT)** | Bounded monotone sequence converges |
| **Bolzano-Weierstrass** | Every bounded sequence has a convergent subsequence |
| **Cauchy Criterion** | In $\mathbb{R}$: convergent $\iff$ Cauchy |
| **Squeeze Theorem** | $a_n \leq b_n \leq c_n$, $a_n,c_n \to L$ $\Rightarrow$ $b_n \to L$ |
| **Cesàro Mean** | $a_n \to L \Rightarrow \frac{a_1+\cdots+a_n}{n} \to L$ |
| **Subsequence** | If $a_n \to L$ then every subsequence $\to L$ |
| **Stolz-Cesàro** | Discrete L'Hôpital for $\frac{\infty}{\infty}$ sequences |
| **Banach FPT** | Contraction on $[a,b]$ has unique fixed point |

---

## Standard Limits to Memorise

$$\frac{1}{n^p} \to 0 \quad (p>0), \qquad r^n \to 0 \quad (|r|<1)$$

$$n^{1/n} \to 1, \qquad c^{1/n} \to 1, \qquad \left(1+\frac{1}{n}\right)^n \to e$$

$$\frac{n^k}{a^n} \to 0 \quad (a>1), \qquad \frac{a^n}{n!} \to 0, \qquad \frac{\ln n}{n} \to 0$$

---

## CSIR NET / GATE Solved Problems

### Problem 1
**The sequence $a_n = \frac{n \sin n}{n^2+1}$ converges to:**

Since $|\sin n| \leq 1$: $|a_n| \leq \frac{n}{n^2+1} = \frac{1}{n+\frac{1}{n}} \to 0$

By Squeeze: $a_n \to \mathbf{0}$ ✓

---

### Problem 2
**Is $a_n = \left(\frac{n+2}{n+1}\right)^n$ convergent? Find the limit.**

$$a_n = \left(1 + \frac{1}{n+1}\right)^n = \left(1+\frac{1}{n+1}\right)^{n+1} \cdot \left(1+\frac{1}{n+1}\right)^{-1} \to e \cdot 1 = \mathbf{e}$$

---

### Problem 3
**$\{a_n\}$ is defined by $a_1=1$, $a_{n+1}=\frac{1}{2+a_n}$. Does it converge?**

**Bounded:** $a_n \in (0,1]$ for all $n$ (induction). ✓

**Monotone:** Alternates but stays bounded. Check convergence by assuming $L = \frac{1}{2+L}$:

$$L(2+L) = 1 \implies L^2 + 2L - 1 = 0 \implies L = -1 + \sqrt{2} \approx 0.414$$

(Taking positive root.) The sequence converges to $\mathbf{\sqrt{2}-1}$. ✓

---

### Problem 4
**True/False: If $\{a_n^2\}$ converges, then $\{a_n\}$ converges.**

**False.** Counterexample: $a_n = (-1)^n$. Then $a_n^2 = 1 \to 1$, but $a_n$ diverges. ✗

---

### Problem 5
**Find $\limsup$ and $\liminf$ of $a_n = \frac{(-1)^n n}{n+1}$.**

Even $n$: $a_n = \frac{n}{n+1} \to 1$. Odd $n$: $a_n = -\frac{n}{n+1} \to -1$.

$$\limsup = 1, \quad \liminf = -1$$

---

### Problem 6
**Show $a_n = \sum_{k=1}^n \frac{1}{k^2}$ converges.**

$\{a_n\}$ is increasing. It is bounded above: $a_n \leq 1 + \sum_{k=2}^n \frac{1}{k(k-1)} = 1 + 1 - \frac{1}{n} < 2$.

By MCT, $\{a_n\}$ converges. (Sum $= \frac{\pi^2}{6}$.) ✓

---

### Problem 7
**If $a_n > 0$ and $\frac{a_{n+1}}{a_n} \to L < 1$, show $a_n \to 0$.**

Choose $r$ with $L < r < 1$. $\exists\, N: n > N \implies \frac{a_{n+1}}{a_n} < r$.

So $a_n < a_N \cdot r^{n-N} = C \cdot r^n \to 0$. By Squeeze: $a_n \to 0$. $\blacksquare$

---

### Problem 8
**Is every Cauchy sequence in $(0,1)$ convergent in $(0,1)$?**

**No.** $a_n = \frac{1}{n}$ is Cauchy in $(0,1)$ but converges to $0 \notin (0,1)$.

$(0,1)$ is **not complete**. ✗

---

### Problem 9
**Find $\lim_{n\to\infty} \frac{1^p + 2^p + \cdots + n^p}{n^{p+1}}$ for $p > 0$.**

By Stolz-Cesàro with $a_n = \sum k^p$, $b_n = n^{p+1}$:

$$\frac{(n+1)^p}{(n+1)^{p+1}-n^{p+1}} \approx \frac{n^p}{(p+1)n^p} = \frac{1}{p+1}$$

$$\lim = \frac{1}{p+1}$$

---

### Problem 10
**If $a_n \to L$ and all $a_n \geq 0$, show $\sqrt{a_n} \to \sqrt{L}$.**

**Case $L > 0$:**

$$|\sqrt{a_n} - \sqrt{L}| = \frac{|a_n - L|}{\sqrt{a_n}+\sqrt{L}} \leq \frac{|a_n-L|}{\sqrt{L}} \to 0$$

**Case $L = 0$:** $\sqrt{a_n} \leq \sqrt{|a_n - 0|} = \sqrt{a_n} \to 0$ directly. $\blacksquare$

---

## Common Exam Mistakes

1. Assuming bounded $\Rightarrow$ convergent (**FALSE** — need monotone too)
2. Assuming $a_n^2 \to L^2 \Rightarrow a_n \to L$ (**FALSE** — sign ambiguity)
3. Forgetting that Cauchy in $\mathbb{Q}$ need not converge in $\mathbb{Q}$
4. Using Stolz-Cesàro without verifying $b_n \to \infty$ strictly increasing
5. Confusing $\limsup$ with $\sup$ — they are different!
