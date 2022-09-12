---
layout: default
title: Day 6
nav_order: 3.5
parent: Course Content
---

## Quick review of examples of group actions

- Dihedral group $D_{2n}$ acts on vertices of regular polygon with $n$ sides. 
The stabilizer of a vertex is of order two; cosets are in bijection with $n$ vertices.  This group
also acts on itself by conjugation.  What are the orbits?


- $\GL_{2}(\R)$ acts transitively on lines through the origin in $\R^{2}$.  The stabilizer of the $x$-axis
are the matrices of shape 
$$
\left(
    \begin{matrix} a & b f\\ 0 & d\end{matrix}
\right)
$$
The cosets are in bijection with points of the real projective line, with representatives
$$\left[\begin{matrix} u & 1\end{matrix}\right]$$ and $$\left[\begin{matrix} 1 & 0 \end{matrix}\right].$$ The action on a coset representative is by linear fractional transformations in $u$.

- The symmetric group acts on the set $\lbrace 1,\ldots, \rbrace n$ through its natural realization as bijections
of this set to itself. 

- The symmetric group acts on its conjugacy classes.  What can you say about $S_{4}$ acting on its conjugacy classes?

- Let $F$ be a finite graph.  The automorphisms of $F$ are the maps from $F$ to itself that preserve the edges 
(so connected vertices stay connected).  Examples?


**Proposition:** Suppose that $G$ has order $n$ and $p$ is the smallest prime dividing $n$.  Then any subgroup of $G$ of index $p$ is normal.

**Proof:** Consider the action of $G$ on the $p$ cosets of $H$.  The kernel of this action is the set of $g\in G$
such that $gg_1H=g_1H$, which means that $gg_1=g_1h$ for some $h\in H$.  This in turn means that 
$g\in g_1Hg_1^{-1}$.  Since $g_1$ is arbitrary, we must have $g$ in the intersection of all conjugates
$g_1Hg_1^{-1}$ as $g_1$ ranges over $G$.  This is the largest normal subgroup of $G$ contained in $H$ -- call it $K$.  

The group $G/K$ acts faithfully on the cosets $G/H$, so it is isomorphic to a subgroup of $S_{p}$. Therefore
$[G:K]$ divides $p!$.  But $[G:K]=[G:H][H:K]=p[H:K]$ and if this is a divisor of $p!$ then $[H:K]$ can only have
prime divisors less than $p$.   Since $p$ is the smallest prime divisor of the order of $G$, this means $[H:K]=1$
so $K=H$ and $H$ is normal.

**Remark:** In the course of this we proved that, in general, the kernel of the action of $G$ on $G/H$ is the
largest normal subgroup of $G$ contained in $H$.


## Class equation and applications

**Lemma:** The stabilizer of an element $g\in G$ under conjugation is the centralizer of $\lbrace g\rbrace$.


**Theorem:** Let $G$ be a finite group.  Let $G$ act on itself by conjugation, yielding
a partition of $G$ into disjoint conjugacy classes $K_1,\ldots, K_g$.  Choose a representative $g_{i}$
for each class. Then

$$
\mid G\mid = \sum_{i=1}^{g}\mid K_i\mid = \sum_{i=1}^{g} [G:C_{G}(g_{i})].
$$

**Proposition:** Let $G$ be a group of prime power order.  Then $G$ has nontrivial center. 

**Corollary:** If $G$ has order $p^{2}$ for some prime $p$, then $G$ is abelian.

**Proof:** If $xZ$ generates the quotient group, then every element of $G$ is of the form $x^{i}z^{j}$
with $z\in Z$.  This forces $G$ to be abelian.

## Conjugacy in $S_{n}$

The conjugacy classes in $S_{n}$ correspond to the cycle decompositions, and there is one class for each
partition of $n$ as a sum of positive integers.

The centralizer of a cycle are the permutations which fix the integers appearing in the cycle.

The normalizer of a cycle was computed  in the homework, at least in one case. 

## $A_{5}$ is a simple group


