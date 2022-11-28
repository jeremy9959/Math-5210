---
layout: default
title: Day 24
nav_order: 13.2
parent: Course Content
---

## Eigenvalues and Eigenvectors

**Defintion:** If $L:V\to V$ is a linear map of vector spaces over a field, an eigenvector for $L$
is a nonzero $v\in V$ such that $Lv=av$ for some $a\in F$.  The scalar $a$ is called an eigenvalue.

If $V$ is finite dimensional and $a$ is an eigenvalue, then $L-aI$ is a non-invertible linear map from $V\to V$, so it's determinant is zero.
Therefore the eigenvalues of $L$ are all roots of the *characteristic polynomial*
$$
P_{L}(T)=\det(L-TI).
$$

**Proposition:** Let $V$ be a finite dimensional complex vector space and $L:V\to V$ be a linear map.
Then $L$ has an eigenvector.

**Proof:** (See Axler, 5.21).  Choose nonzero $v\in V$ and consider the elements $v,L(v),L(L(v)),\ldots, L^n(V)$.
There are $n+1$ of these, so they are linearly dependent.  In fact there is a relation
$$
a_0v + a_1L(V)+\cdots+a_kL^k(v)=(a_0+a_1 L+\cdots + a_kL^k)v=0
$$
where $k$ is minimal. By the fundamental theorem of algebra, the polynomial 
$$
p(T)=a_1+a_1T+\ldots, a_kT^k
$$
has a root $\lambda$ and
$$
p(T)=(T-\lambda)q(T).
$$.
Therefore $(L-\lambda)q(L)v=0$.  Since $q(T)$ has degree less than $k$, we have $q(L)v\not=0$,
so $q(L)v$ is an eigenvector with eigenvalue $\lambda$.

The fact that $\C$ is algebraically closed is essential here.  The matrix 
$$
\left(\begin{matrix} 0 & 1 \\ -1 & 0\end{matrix}\right)
$$
gives a linear map on $\R^{2}$ corresponding to a ninety degree rotation; it has no eigenvector.

Even over $\C$, a linear map need only have one eigenvector/value pair.  For example the matrix
$$
\left(\begin{matrix} 1 & 1 \\ 0 & 1\end{matrix}\right)
$$
has eigenvector $$\left(\begin{matrix} 1 \\ 0 \end{matrix}\right)$$, but that's the only one. 

**Proposition:** Suppose that $L:V\to V$ is a linear map and $v_1,\ldots, v_n$ is a basis for $V$
consisting of eigenvectors of $L$.  Then the matrix of $L$ in that basis is diagonal.

Linear maps with this property are called *diagonalizable*; as we saw above, not all linear maps have this property, and figuring out exactly what's going on here is an important problem in linear algebra that we'll discuss in the broader context of modules over principal ideal domains next semester.

### Real and complex dot products

If $z=(z_1,\ldots, z_n)$ and $w=(w_1,\ldots, w_n)$ are elements of $\C^{n}$, then
$$
z\cdot w=\langle z,w\rangle = \sum z_i\overline{w}_{i}.
$$
(Notice that if $z$ and $w$ are real, this is the usual real dot product).

Then this dot product is:

- nondegenerate, so $z\cdot z=0$ if and only if $z=0$;
- linear in $z$ and "conjugate linear" in $w$
- positive definite, meaning $\langle z,z\rangle$ is real and greater than zero for all $z\not=0$.
- satisfies $\langle z,w\rangle=\overline{\langle w,z\rangle}$

**Lemma:** Suppose $A\in M_{n}(\C)$.  Then $\langle Av,w\rangle =\langle v,\overline{A}^{T}w\rangle$.
(Here $\overline{A}$ means the matrix whose entries are the conjugates of those in $A$.)

**Proof:** $\langle v,w\rangle=v^{T}\overline{w}$.  So 
$$
\langle Av,w\rangle=v^{T}A^{T}\overline{w}=\langle v,\overline{A}^{T}w\rangle
$$



**Proposition:** Suppose that $A$ is a real, symmetric matrix (so $A^{T}=A$).  Then its eigenvalues are real numbers.

**Proof:** Suppose that $v\not=0$ and  $Av=\lambda v$.  Pretend that $A$ is a complex matrix that happens to have real entries.
Then 
$$
\langle Av,v\rangle=\lambda\langle v,v\rangle=\langle v,A^{T}v\rangle=\langle v, Av\rangle=\overline{\lambda}\langle v,v\rangle.
$$
Since $\langle v,v\rangle\not=0$, this means $\overline{\lambda}=\lambda$ so $\lambda$ is real.

### More general inner products

**Definition:** An inner product on a finite dimensional complex vector $V$ space is a map 
$$
\langle\cdot,\cdot\rangle: V\times V\to \C
$$
which satisfies:

- $\langle v,v\rangle$ real and greater than or equal to zero, with equality only if $v=0$.
- $\langle v,w\rangle$ is $\C$-linear in its $v$ variable and conjugate linear in $w$.
- $\langle v,w\rangle=\overline{\langle w,v\rangle}$

An inner product on a finite dimensional real vector space is a bilinear map $V\times V\to \R$
which satisfies:

- $\langle v,v\rangle\ge 0$ with equality only if $v=0$.
- $\langle v,w\rangle=\langle w,v\rangle$.

In either case, given a basis $v_1,\ldots, v_n$ of $V$, a dot product is determined by the values
$\langle v_i,v_j\rangle$.  If we make the matrix $Q$ whose $i,j$ entry is $\langle v_i, v_j\rangle$,
then $Q$ is symmetric in the real case and satisfies $\overline{Q}^{T}=Q$ in the complex case. 

Also, if we write $z=\sum a_i v_i$ and $w=\sum b_i v_i$, then 

$$
\langle z,w\rangle = \left[\begin{matrix} a_1 & a_2 &\cdots&a_n\end{matrix}\right]Q\left[\begin{matrix}\overline{b_1}\\ \overline{b_2} \\ \vdots \\ \overline{b_n}\end{matrix}\right]=[z]^{T}Q\overline{[w]}
$$

**Definition:** Two vectors $v,w$ are orthogonal if $\langle v,w\rangle=0$. 

**Definition:** If $V$ is an inner product space, then the norm of a vector is the
square root of $\langle v,v\rangle=\norm{v}^2$. 

**Proposition:** (Cauchy-Schwartz) $\langle v,w\rangle\le \norm{v}\norm{w}$.

**Proof:** We can write
$$
v=\frac{\langle v,w\rangle}{\norm{w}^2}w+u
$$
for some vector $u$.  This is cooked up so that $\langle u,w\rangle=0$.  Then
$$
\norm{v}^2 = \frac{\|\langle v,w\rangle\|^2}{\norm{w}^2} + \norm{u}^2
$$
which after rearranging is what we want (since $\norm{u}^2\ge 0$. )

**Corollary:** The norm is a metric (it satisfies the triangle inequality).  

### Adjoints

Let $V$ be a (real or complex) inner product space.  Then the inner product gives us a linear map $\phi$
from $V$ to its dual space $V^{\ast}$ by setting
$$
\phi(w)(v)=\langle v,w\rangle
$$

**Proposition:** The map $\phi: V\to V^{\ast}$ is an isomorphism.

**Proof:** We'll prove it's injective.  Since $V$ and $V^{\ast}$ have the same dimension, that's enough.
Suppose that $\phi(w)=0$.  That means $\phi(w)(w)=0$, so $\norm{w}^2=0$, so $w=0$. 

Now consider the usual dot product on $\R^{n}$.  If $A\in M_{n}(\R)$ is a matrix, then
$$
\langle Av, w\rangle = v^{T}A^{T}w=\langle v, A^{T}w\rangle.
$$
In terms of our dot product and our map $\phi$, this means that $\phi(Av)(w)=\phi(v)(A^{T}w)$.

For matrices over $\C$, the adjoint is the conjugate transpose.

What is the generalization of this property of the transpose to general inner products?

**Proposition:** Let $A:V\to V$ be a linear map on a (real or complex) inner product space.  
Then there is a unique linear map $A^{\ast}:V\to V$ that satisfies
$$
\langle Av,w\rangle = \langle v, A^{\ast}w\rangle
$$
for all $v,w$.  This map is called the *adjoint* to $A$.

Constructing the adjoint requires a little trickery. 

First, why does $A^{\ast}$ exist?  It's defining property is that
$$
\langle v,A^{\ast}w\rangle=\langle Av,w\rangle.
$$
Fix $w$. We have an element of $V^{\ast}$ defined by $f(v)=\langle Av, w\rangle$. 
By our result above, this linear map must be of the form $v\mapsto \langle v, w'\rangle$
for a unique $w'\in V$.  Define $A^{\ast}$ to be this $w'$. 

We have to show that $A^{\ast}$ is linear.  By definition, $A^{\ast}(w_1+w_2)$ is the unique
$z$ such that
$$
\langle v, z\rangle = \langle Av, w_1+w_2\rangle.
$$
But $w_1'=A^{\ast}w_1$ and $w_2'=A^{\ast}w_2$ satisfy $\langle v, w_1'\rangle=\langle Av, w_1\rangle$
and $\langle v, w_2'\rangle=\langle Av, w_2\rangle$ respectively, so $w_1'+w_2'$ has the property
we need to be $z$.

Also, we have 
$$
\langle v, A^{\ast}(\lambda w)\rangle=\langle Av, \lambda w\rangle=\overline{\lambda}\langle Av, w\rangle
$$
and
$$
\langle v, \lambda A^{\ast}w\rangle =\overline{\lambda}\langle Av, w\rangle
$$
so $\lambda A^{\ast}w$ satisfies the same condition as $A^{\ast}(\lambda w)$. Thus $A^{\ast}$ is linear.

**Properties of the Adjoint:**

1.  $(A+B)^{\ast}=A^{\ast}+B^{\ast}$
2.  $(\lambda A)^{\ast}=\overline{\lambda}A^{\ast}$
3.  $(A^{\ast})^{\ast}=A$
4.  $(AB)^{\ast}=B^{\ast}A^{\ast}$.
5.  The identity is its own adjoint.
6.  If $A$ is invertible, then so is $A^{\ast}$ and $(A^{\ast})^{-1}=(A^{-1})^{\ast}$.

See Axler, 7.5 on page 220 for proofs of these properties. 

**Definition:** A linear map $A:V\to V$ is *self-adjoint* if $A^{\ast}=A$.

### Real Spectral Theorem



**Theorem:** Let $A:V\to V$ be a linear map on a finite dimensional real inner product space.
Then the following are equivalent:

1.  $A$ is self-adjoint.
2.  There is an orthonormal basis $B$ of $V$ for which the matrix $[A]_{B}$ is diagonal.
3.  $V$ has an orthonormal basis consisting of eigenvectors of $T$.  