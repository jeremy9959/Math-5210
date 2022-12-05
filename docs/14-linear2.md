---
layout: default
title: 14. Additional topics in linear algebra
nav_order: 14
parent: Course Content
---

## The Singular Value Decomposition

Suppose that $T:V\to W$ is a linear map between inner product spaces.  The adjoint $T^{*}$ of $T$ is the linear map $T^{*}:W\to V$
satisfying
$$
\langle w, Tv\rangle=\langle T^{*}w,v\rangle.
$$

To see that $T^{*}$ exists, fix $w$ and consider the linear map $\phi_w:v\mapsto \langle w, Tv\rangle$.  Since $\phi_w$ belongs to $\Hom(V,F)$,
there is a unique $v'\in V$ such that $\phi_w(v)=\langle v',v\rangle$.   Then $v'=T^{*}w$ by definition.  The adjoint has the properties:

- $(S+T)^{\ast}=S^{\ast}+T^{\ast}$ and $(aS)^{\ast}=\overline{a}S^{\ast}$
- $(ST)^{\ast}=T^{\ast}S^{\ast}$.
- $(T^{\ast})^{\ast}=T$
- $(T^{-1})^{\ast}=(T^{\ast})^{-1}$
- The identity is its own adjoint.  

The spectral theorem (over $\R$) applies to self-adjoint operators $T:V\to V$ where $V$ is an inner product space.  The singular value decomposition is a generalization to
operators $T:V\to W$.   So let $V$ and $W$ be real inner product spaces and $T:V\to W$ a linear map.

Let $Q=T^{\ast}T$.  Then $Q$ is a map from $V\to V$:

- $Q$ is self-adjoint.
- $\langle Qv, v\rangle \ge 0$ for all $v\in V$.   A self adjoint operator with this property is called *positive*.
- The null space of $Q$ is the same as the null space of $T$.
- The range (column space) of $Q$ is the same as the column space of $T^{\ast}$. 
- The ranks of $T$, $^{\ast}$, and $Q$ all coincide. 

**Proof:**

The key point is that $\langle Qv, v\rangle=\langle T^{\ast}Tv,v\rangle = \langle Tv, Tv\rangle$.  So $\langle Qv,v\rangle$ is greater than or equal to zero;
and if it equals zero then $Tv=0$ and conversely.  This proves that $\mathrm{null}(Q)=\mathrm{\null}(T)$.

In general:

- null space of $T^{\ast}$ is orthogonal to the range of $T$.
- range of $T^{\ast}$ is orthogonal to the null space of $T$.
- null space of $T$ is orthogonal to the range of $T^{\ast}$.
- range of $T$ is orthogonal to the nullspace of $T^{ast}$. 

So since the null space of $Q$ and the null space of $T$ coincide, and $Q$ is self-adjoint,  we have:
$$
\mathrm{range}Q = (\mathrm{null} Q)^{\perp}=(\mathrm{null}(T))^{\perp}=\mathrm{range}(T^{\ast}).
$$

Also
$$
\dim\mathrm{range}(T)=\dim\mathrm{null}(T^{\ast})^{\perp}=\dim W-\dim\mathrm{null}(T^{\ast})=\dim\mathrm{range}(T^{\ast}).
$$

**Definition:** If $T:V\to W$ is a linear operator, then $Q=T^{\ast}T$ is diagonalizable.  Let $\Lambda$ be diagonal the matrix of $Q$
in an orthonomormal basis given by the spectral theorem, with eigenvalues listed in decreasing order.  The singular values of $T$ are
the entries in $\Lambda^{1/2}$ -- the square roots of the eigenvalues of $Q$.

**Proposition:** (Singular value decomposition)  Let $T:V\to W$ be a linear map of inner product spaces with singular values $s_1,\ldots, s_n$.
Then there are orthonormal basis $e_1,\ldots, e_n$ and $f_1,\ldots, f_n$ for $V$ and $W$ such that
$$
T(v)=\sum_{i=1}^{n} s_i <v,e_i>f_i
$$
for all $v\in V$. In matrix terms this basically means that $T$ is "diagonal" in the bases given by the $e$'s and $f$'s (although $T$ needn't be square).

This is usually written like this for matrices.

**Theorem:** (SVD)  Let $A$ be an $m\times n$ matrix over $\R$.  Then there are orthogonal matrices $P$ and $Q$ such that
$$
A=PDQ
$$
where $P$ is $m\times m$, $Q$ is $n\times n$, and $D$ is $m\times n$.  The "diagonal" entries of $D$ are the singular values of $A$. 

This is the matrix version of the previous statement.

**Proof:** 

There's an orthonormal basis of $V$ so that $Qe_i=\lambda_i e_i$ where the $\lambda_i$ are the eigenvalues of the self-adjoint operator $Q$.
For the nonzero eigenvectors $e_i$ for $i=1,\dots, r$, 
the vectors
$$
f_i=\frac{Te_i}{\sqrt{\lambda_i}}
$$
are orthonormal.  We can complete the set of $f_i$ (if needed) to a basis of $W$.  Any $v\in V$ can be written
$$
v=\sum_{i=1}^{n} \langle v, e_i\rangle e_i.
$$
The sought-after formula comes from applying $T$ to this. 