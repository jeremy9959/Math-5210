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

## Group Actions

**Definition:** Let $G$ be a group and $X$ be a set.  A action of $G$ on $X$ is a map
$$
a: G\times X\to X
$$
that satisfies $a(e,x)=x$ for all $x$ and $a(g,a(h,x))=a(gh,x)$ for all $g,h\in G$ and $x\in X$.
(*Remark:* We usually write $gx$ or $g\cdot x$ instead of referring to the map $a$)

Equivalently, an action of $G$ on $X$ is a homomorphism $f:G\to S(X)$. 

**Note:** Whenever we have a function $f: A\times B\to C$ we can think of it equivalently as a
function $f:A\to \mathcal{F}(B,C)$ where $\mathcal{F}(B,C)$ is the set of all functions from $B$ to $C$.
The point is that we can take our function $f:A\times B\to C$, which is a function of two variables,
and define $\tilde{f}:A\to\mathcal{F}(B,C)$ by definining $\tilde{f}(a)$ to be the function
$\tilde{f}(a)(b)=f(a,b)$.  Conversely, if $h:A\to\mathcal{F}(B,C)$ is a function, we can make a function
$\overline{h}:A\times B\to C$ by setting $\overline{h}(a,b)=h(a)(b)$.  These are mutually inverse constructions
so $\mathcal{F}(A\times B,C)=\mathcal{F}(A,\mathcal{F}(B,C))$. 
This is a property of the cartesian product called *adjointness*
or more specifically *left adjointness*.

### Key Terminology

1. Let $x\in X$.  The set $Gx=\lbrace gx: g\in G\rbrace\subset X$ is called the **orbit** of $x$.  More generally,
if $H$ is a subgroup of $G$ then $Hx$, defined similarly, is the orbit of $x$ under $H$.
2. Let $x\in X$.  The set $\mathrm{Stab}_{G}(x)=\lbrace g : gx=x\rbrace\subset G$ is called the **stabilizer** of $x$. It is a subgroup of $G$.
3. An action is called *transitive* if there is an $x\in X$ so that $X=Gx$.
4. The set of $g\in G$ such that $gx=x$ for all $x\in X$ is the *kernel* of the action.
5. An action is *faithful* if its kernel is trivial; in other words, if the corresponding map $G\to S(X)$
is injective. 
6. If $G$ acts on $X$ and $Y$, a map $f:X\to Y$ is called a morphism of actions if $f(gx)=gf(x)$.
If $f$ is bijective then it is an isomorphism of actions. 


### Key formalities

1. If $G$ acts on $X$, the action partitions $X$ into a disjoint union of orbits.  These can be seen as the equivalence classes for the equivalence relation $x\sim y\iff x=gy$ for some $g\in G$.
2. The action of $G$ on each orbit is transitive (by definition).
3. Given $x\in X$, the map
$$
\pi: gH\mapsto gx
$$
gives a well-defined bijection between the cosets of 
$H=G/\mathrm{Stab}_{G}(x)$ and the orbit $Gx$.  
This bijection
is an isomorphism of group actions, since if $H=
\Stab_G(x)$, then 
$k\pi(gH)=kgx=\pi(kgH)$.  


If $G$ is finite,
the size of each orbit is a divisor of the order of $G$.

### Key examples

1. If $G$ is a group, and $H$ is a subgroup, let $X$ be the set of left cosets of $H$ in $G$ (regardless of
whether $H$ is normal).  Then $G$ acts on $X$ via $g\cdot kH=gkH$.  The set $X$ is called a *homogeneous space*
for $G$ and is sometimes written $G/H$ even when $H$ isn't normal.   Property 3 under "formalities"
says that *every orbit in a group action is isomorphic to a homogeneous space for the group.*  Notice that
if $H$ is the trivial subgroup, then this is the action of $G$ on itself by left multiplication; this is called the (left) *regular* action.+-
2. If $G$ is a group, then $G$ acts on itself via conjugation: $g\cdot h=ghg^{-1}$.  The orbits
are called *conjugacy classes.*  The stabilizer of an element $g$ under conjugation is the centralizer
$C_{G}(\lbrace g \rbrace)$ and the index of this stabilizer is the size of the conjugacy class of $g$. 
3. If $g\in Z(G)$ is an element of the center of $G$, then it forms a one-element conjugacy class and its centralizer is all of $G$. 


### The class equation

**Theorem:** Let $G$ be a finite group.  Let $G$ act on itself by conjugation, yielding
a partition of $G$ into disjoint conjugacy classes $K_1,\ldots, K_g$.  Choose a representative $g_{i}$
for each class. Then

$$
\mid G\mid = \sum_{i=1}^{g}\mid K_i\mid = \sum_{i=1}^{g} [G:C_{G}(g_{i})].
$$

Grouping the conjugacy classes of size one together, we can rewrite this as

$$
\mid G\mid = \mid Z(G)\mid + \sum_{\lbrace i : \mid K_{i}\mid>1\rbrace}  [G:C_{G}(g_{i})]
$$

This is called **the class equation**.

## Automorphisms

If $G$ is a group, the automorphism group $\Aut(G)$ of $G$ is the set of isomorphisms $G\to G$, with group operation given by composition of functions.

If $G=\Zn{n}$ then $\Aut(G)$ is $(\Zn{n})^{*}$, the multiplicative group of elements mod $n$ that are relatively
prime to $n$.

If $G=\Zn{n}^{k}$, then $\Aut(G)$ is $\GL_{n}(\Zn{n})$, the group of $n\times n$ matrices with entries in 
$\Zn{n}$ that are invertible (meaning their determinant is relatively prime to $n$).

For $g\in G$, conjugation by $g$ is an automorphism of $G$.  This gives a homomorphism $G\to \Aut(G)$. THe 
kernel of this map is the center of $G$.  The image is called the group of *inner automorphisms.* The
inner automorphisms form a normal subgroup of the automorphism group.

A group $G$ acts on a normal subgroup $H$ by conjugation.  The centralizer of $H$ is the kernel of the action.
Therefore $G/C_{G}(H)$ is a subgroup of $\Aut(H)$.  And $G/Z(G)$ is a subgroup of $\Aut(G)$.

**Definition:** A subgroup $H$ of $G$ is called *characteristic* if it is fixed by *every* automorphism of $G$,
not just the inner ones. 

**Weird fact:** Every automorphism of $S_{n}$ is inner, *except* $S_{6}$ has an outer automorphism.