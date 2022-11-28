---
layout: default
title: 13. The spectral theorem
nav_order: 13
parent: Course Content
---

## The Spectral Theorem

In the last two weeks of the course we will discuss the spectral theorem.  Since this is not covered in Dummit and Foote,
we will follow Sheldon Axler's Linear Algebra Done Right (4th edition, draft version) distributed in class.  Thanks to Professor Axler
for making this available to us.

The relevant sections are:

- Chapter 5, Section A: Eigenvalues and Eigenvectors
- Chapter 6
- Chapter 7, Sections A, B

If time permits we will discuss the singular value decomposition (Chapter 7, Section E).

### Eigenvalues and Eigenvectors

Let $L:V\to V$ be a linear map of vector spaces $V$ over a field $F$.  An *eigenvector* for $L$ is an element $v\in V$ for which there is a $\lambda\in F$
such that
$$
L(v)=\lambda v.
$$

If there is a basis of $V$ made up entirely of eigenvectors for $L$, then the matrix of $L$ in that basis
is diagonal.  This does not always happen.  

### The spectral theorem (real matrix version)

**Theorem:** Let $A\in M_{n}(\R)$ be a *symmetric* matrix, meaning that $A^{T}=A$.  Then
there is a basis $v_1,\ldots, v_n$ of $\R^{n}$ such that 

- $Av_i=\lambda_i v_i$ where the $\lambda_i$ are real numbers
- $v_i\cdot v_j=0$ when $i\not=j$, where $\cdot$ is the "dot product" of vectors in $\R^{n}$. 

### Inner Products

Now we look at the generalization of the dot product.

Let $V$ be a finite dimensional vector space over  field $\R$.  
Then a (real) *inner product* on $V$ is a symmetric bilinear map
$V\times V\to \R$ that satisfies $\langle v,v\rangle\ge 0$ for all $v\in V$ with equality if and only if $v=0$. 


Over $\C$, the natural generalization of the dot product involves conjugation:
$$
z\cdot w = (z_1,\ldots, z_n)\cdot (w_1,\ldots, w_n)=\sum_{i=1}^{n} z_i\overline{w}_{i}.
$$

Then $(z_1,\ldots, z_n)\cdot (z_1,\ldots, z_n)\ge 0$ with equality only if all the $z_i=0$; but
this "dot product" isn't bilinear because 

$$(\lambda z)\cdot w = \lambda z\cdot w=z\cdot (\overline{\lambda}w)$$

Such a map is sometimes called Hermitian or conjugate linear.

If $V$ is a finite dimensional vector space over $\C$, then an inner product on $V$ is
a map $\langle\cdot,\cdot\rangle:V\times V\to \C$ that satisfies

- $\langle w,w\rangle$ is real and nonnegative for all $w\in V$, and is zero only when $w=0$.
- $\langle v,w\rangle$ is complex-linear as a function of its first variable.
- $\langle v,w\rangle=\overline{\langle w,v\rangle}$.

**Definition:** An inner product space is a finite dimensional real or complex vector space with a specified inner product.


### The spectral theorem (for real inner product spaces)

**Definition:** Let $V$ be a real inner product space and let $L:V\to V$ be a linear map. Then there is
a unique linear map $L^{\ast}:V\to V$ such that $\langle L(v),w\rangle=\langle v,L^{\ast}(w)\rangle$.
This is called the *adjoint map* to $L.$  The adjoint $L^{\ast}$ depends on the inner product.

**Theorem:** Suppose that $L=L^{\ast}$.  (So $L$ is *self-adjoint.*) Then there is a basis  $v_1,\ldots, v_n$
for $V$ such that  $\langle v_i,v_j\rangle=0$ if $i\not=j$ and real numbers $\lambda_1,\ldots, \lambda_n$
such that $L(v_i)=\lambda_i v_i$.

Note: If the inner product is the usual dot product, then the adjoint to a linear map is its tranpose;
therefore "self-adjoint" means "symmetric" in that situation.
