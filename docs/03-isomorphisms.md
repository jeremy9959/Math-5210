---
layout: default
title: 3. Group morphisms and group actions
nav_order: 3
parent: Course Content
---

# The isomorphism theorems

**Theorem:** (See DF Theorem 3.16) Let $f:G\to K$ be a homomorphism of groups, let $N$ be the kernel of $f$, and let
$\pi:G\to G/N$ be the canonical projection.  Then there is a unique *injective* homomorphism
$\overline{f}:G/N\to K$ such that $\overline{f}\circ\pi=f$.

$$
\begin{xy}
\xymatrix {
G\ar[rd]^{f}\ar[d]^{\pi} &  \\
G/N\ar[r]_{\overline{f}} & K\\
}
\end{xy}
$$

We sometimes say that "$f$ factors through $\pi$" or "$f$ factors through $G/N$".

**Theorem:** (See DF Theorem 3.18) Suppose that $G$ is a group and $A$ and $B$ are subgroups of $G$.  Suppose further
that $A$ is a subgroup of $N_{G}(B)$ so that $AB$ is a subgroup of $G$.  Then
1. $B$ is normal in $AB$.
2. $A\cap B$ is normal in $A$.
3. $AB/B$ is isomorphic to $A/(A\cap B)$.

$$
\begin{xy}
\xymatrix {
    & G & \\
    & AB\ar[u] & \\
    A\ar[ur] && B\ar[ul]^{=} \\
    & A\cap B\ar[ul]^{=}\ar[ur] & \\
    &1\ar[u]&\\
}\end{xy}
$$

The arrows marked with "=" are inclusions of normal subgroups, and the corresponding quotients are isomorphic.  

**Theorem:** (See DF, THeorem 3.19) Let $G$ be a group, and suppose that
$H$ and $K$ are normal subgroups of $G$ and $H$ is normal in $K$.
Then $K/H$ is normal in $G/H$ and $(G/H)/(K/H)$ is isomorphic to $G/K$. 

**Theorem:** (See DF, Theorem 3.20)  Let $G$ be a group and
$N$ be a normal subgroup of $G$.  Then map $A\mapsto A/N$ is
a bijection between the set of all subgroups of $G/N$ and
the set of subgroups of $G$ containing $N$. Furthermore,
if $A$ and $B$ are subgroups of $G$ containing $N$, then
1. $A\subset B$ if and only if $A/N\subset B/N$
2. If $A\subset B$ then $[A:B]=[A/N:B/N]$
3. $\langle A, B\rangle/N=\langle A/N,B/N\rangle$
4. $(A\cap B)/N=(A/N\cap B/N)$
5. $A$ is normal in $G$ if and only if $A/N$ is normal in $G/N$.

In other words, the lattice of subgroups of $G/N$ is exactly
the sublattice of the lattice of subgroups of $G$ containing $N$.
