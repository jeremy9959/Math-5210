---
layout: default
nav_order 11.8
title: Day 22
parent: Course Content
---

## Duality

### Linear forms

A *linear form* or a *linear functional* on a vector space $V$ over a field $F$ is a linear map $h: V\to  F$.

- The space $\Hom(V,F)$ of linear forms is a vector space called the **dual vector space** to $V$.  DF use the notation $V^{\ast}$ for $\Hom(V,F)$. 

Suppose that $S$ is a basis for $V$ (not necessarily finite).  For each $s\in S$, define a linear map $s^{\ast}: V\to F$ by saying that $s^{\ast}(s)=1$ and
$s^{\ast}(x)=0$ for any other $x\in S$; then extending $s^{\ast}$ by linearity to all of $V$.  *Note that the linear map $s^{\ast}$ depends on all of $S$, not just on $s$ itself.*

If $V$ is finite dimensional, and $s_1,\ldots, s_n$ is a basis for $V$, then $s_1^{\ast},\ldots, s_n^{\ast}$ is a basis for $V^{\ast}$ called the dual basis. 
To show that it spans $V^{\ast}$, let $f$ be any linear form and compute $f(s_{i})$.  Then 
$$
f=\sum f(s_{i})s_{i}^{\ast}
$$
since the right side agrees with $f$ on the basis $s_{i}$. The $s_{i}^{\ast}$ are linearly independent since if
$$
\sum a_{i}s_{i}^{\ast}=0
$$
Then
$$
(\sum a_{i}s_{i}^{\ast})(s_{i})=0=a_{i}
$$ 
for all  $i$. 

If $V$ is infinite dimensional and $S$ is a basis, you can still construct elements $s^{\ast}$ dual to the elements of $S$ and they are linearly independent.
However they won't span. 

### Dual transformations

Suppose $L:V\to W$ is a linear map.  Then there is a "dual map" $L^{\ast}:W^{\ast}\to V^{\ast}$ defined abstractly by setting $((L^*)(f))(v)=f(L(v))$.

**Proposition:** Given $L:V\to W$ and $G:W\to H$, we have
$$(G\circ L)^{\ast}=L^{\ast}\circ G^{\ast}$$.

**Proof:** $(G\circ L)^{\ast}$ is a linear map from $H^{\ast}\to V^{\ast}$.  If $h^{\ast}\in H^{\ast}$, we have 

$$
(G\circ L)^{\ast}(h^{\ast})(v)=h(G\circ L)(v)=(h\circ G\circ L)(v).
$$

On the other hand, $$L^{\ast}\circ G^{\ast}(h^{\ast})=L^{\ast}(h\circ G) = (h\circ G\circ L)$$
so the two things are the same.

**Proposition:** If A is a finite basis for $V$ and $B$ is a finite basis for $W$ then let $A^{\ast}$ and $B^{\ast}$ be the corresponding dual bases.  Then
$$
[L^\ast]_{B^{\ast}}^{A^{\ast}}
$$ is the transpose of $[L]_{A}^{B}$.

**Proof:** Consider $b_i^{\ast}$ in $B^{\ast}$.  Then
$$L^{\ast}(b_{j}^{\ast})(a_{i})=b_{j}^{\ast}(L(a_i))$$ which is the coefficient of $b_{j}$ in the expansion
of $L(a_{i})$. This is by definition the entry $x_{ji}$ in the matrix of $L$ relative to the bases $A$ and $B$.

On the other hand, if we write
$$
L^{\ast}(b_{j}^{\ast})=\sum y_{ij}a_{i}^{\ast}
$$
where $y_{ij}$ are the matrix entries of $L^{\ast}$ relative to the dual bases, then we see that $x_{ji}=y_{ij}$.  In other words, the matrix entries
for $L^{\ast}$ are those for $L$, but with rows and columns interchanged.

Let $H\subset V$ be a subspace.  Then any linear form on $V$ restricts to one on $H$, so there is a map $V^{\ast}\to H^{\ast}$.
This map is surjective since any linear form on $H$ extends to one on $V$.  It's kernel is the set of linear forms on $V$ that vanish on $H$;
this is called the "annihilator of $H$".  

**Corollary:** The row and column ranks of a matrix coincide.  

**Proof:** Let $L:V\to W$ and $L^{\ast}:W^{\ast}\to V^{\ast}$ be a linear map and its dual.  $L$ gives an isomorphism from $V/K$ to the image $H$ of $L$ in $W$ where $K$ is the kernel of $L$. 
So we can view $L:V/K\to H$. 

The dual transform $L^{\ast}$ takes a linear form on $W$ and makes it one on $V$ by the formula $L^{\ast}(f)(v)=f(L(v))$.  Since $L(v)\in H\subset W$, $L^{\ast}(f)$ is determined by its
values on $H$ and the kernel of $L^{\ast}$ is the annihilator of $H$.  Therefore the image of $L^{\ast}$ is $H^{\ast}$.  But $H^{\ast}$ and $H$ have the same dimension, so the rank of $L^{\ast}$
and the rank of $L$ are the same.  However, the rank of $L^{\ast}$ is the column rank of its matrix representation, which is the row rank of the matrix of $L$. 
 

### Some remarks on analysis

In very rough terms, the Riesz Representation theorem says that if $X$ is a compact hausdorff space and C(X) are the continuous functions on X, then
any(positive) *continuous* linear form
$a: C(X)\to R$ there is a unique Borel measure $\mu$ satisfying some extra properties such that 
$a(f)=\int f(x)d\mu$.

Roughly speaking, *continuous* linear forms are the same as measures. 

Continuity is essential here; the space of continuous linear forms is MUCH SMALLER than the space of all linear forms. Here the topology on $C(X)$ is the metric topology given
by the sup norm.

"Functional Analysis" is the study of possible topologies on vector spaces and their relationship to spaces of linear forms.

### The double dual

The "Double dual" space $V^{\ast\ast}=\Hom(\Hom(V,F),F)$ is another vector space.  Notice that if $V$ is of dimension $n$ then $V^{\ast\ast}$ is also of dimension $n$.
But the relationship is closer than that.

Given $v$ in $V$, define $e_{v}$ in $V^{\ast\ast}$ by $e_{v}(f)=f(v)$.  This is called the "evaluation map".

If $V$ is finite dimensional, $e$ is an isomorphism.

In general, the evaluation map is injective but far from surjective. 







