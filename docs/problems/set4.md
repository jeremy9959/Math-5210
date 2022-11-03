---
layout: default
nav_order: 10.9
title: HW Set 4
parent: Course Content
---

## Homework Set 4

**Instructions:** These problems are due November 20.

### Problem 1. 

In $\Z[\sqrt{5}]$, the ideal $\mathbf{p}=(2,1+\sqrt{5})$ is maximal (and thus prime), and 
$\Z[\sqrt{5}]/\mathbf{p}$ is isomorphic to  $\Zn{2}$.  

1. Show that $X^3-\sqrt{5}X+1-2\sqrt{5}$ is irreducible mod $\mathbf{p}$ in $\Z[\sqrt{5}]$.

2. Show that $\mathbf{p}^2=\lbrace a+b\sqrt{5} : a,b \hbox{  both even} \rbrace$.

3. Show that $X^4+2(1-\sqrt{5})X^2-6X+3+\sqrt{5}$ is an Eisenstein polynomial in $\Z[\sqrt{5}][X]$ 
at the prime $\mathbf{p}$. 

4. Show that $X^n-(7+3\sqrt{5})$ is Eisenstein at $\mathbf{p}$ for every $n\ge 1$.

5. If $n\ge 2$ and $d\ge 1$, prove that $X_1^d+X_2^d+\cdots X_n^d-1$ is irreducible in 
$\Q[X_1,\ldots, X_n]$.  (Hint: For fixed $d$, use induction on $n$ and the Eisenstein Criterion
in its more general form as in DF Proposition 13 pg. 309.)

### Problem 2. 

Compute the matrix representation of the following linear maps with respect to the 
indicated ordered basis.  In each case the field is $\R$.

1.  $V=\C$; $m:V\to V$ is $m(x)=(2-i)x$; $B=\lbrace 1+i,3i\rbrace$.

2.  $V=\R[x]/(x^3-1)$; $m:V\to V$ is $m(v)=xv$; $B=\lbrace 1,x,x^2\rbrace$.

3.  $V$ is the space of solutions to the differential equation $y^{\prime\prime} +y^{\prime}+y=0$; $m:V\to V$ is $m(y)=y';$
you choose your basis.

### Problem 3.

DF Problem 12 on page 302.  This problem constructs an integral domain $R$ which has the property that any *finitely generated* ideal in $R$ is principal; but $R$ has some ideals which are not finitely generated.  Such a ring is called a Bezout ring. In such a ring, any two elements $a$ and $b$ have a gcd $d$ such that $ax+by=d$, but you don't have unique factorization because the other requirement -- that every element is a *finite* product of irreducibles -- fails.  In the ring you construct in this problem, there is an element $x$ which is not a unit but has roots of arbitrarily high order.

See Theorem 14 in DF on page 287 to see how, in the case when $R$ is a PID (in which *every* ideal is principal, not just the finitely generated ones), one has to use Zorn's lemma to prove that every non-zero non-unit in $R$ is a *finite* product of irreducibles. 

### Problem 4. 

For $n\ge 1$, Let $\Pol_{n}(\R)$ be the space of polynomials with real coefficients and degree *at most* $n$. So $\Pol_{n}$ is a vector space of dimension $n$ over $\R$.  Let $D:\Pol_{n}(R)\to\Pol_{n}(\R)$ be
the map $\frac{d}{dx}$, let $D^{j}$ be the $j^{th}$ derivative, and let 
$\D_{n}(\R)$ be the
vector space of linear differential operators in one variable with constant coefficients over $\R$. So
an element of $\D_{n}(\R)$ is a polynomial in $D$ of degree at most $n$.   Note for the sake
of clarity that $D^{0}$ is the identity map, so 

$$
(2-D+D^2)(x^3)=2x^3-3x^2+6x
$$

with the initial $2$ acting on a polynomial just by multiplication.

1.  For $f=a_0+a_1 X+\cdots +a_nX^n$, and $L=b_0+b_1D+\cdots+b_nD^n$, compute $(Lf)(0)$ in terms of the coefficients of $f$ and $L$. 

2. For $L\in \D_{n}(\R)$, define $L_{0}:\Pol_{n}(\R)\to\R$ by $L_{0}(f)=(Lf)(0)$. Show that the map $L\to L_{0}$ is an isomorphism of vector spaces from $\D_{n}$ to the dual space $\Pol_{n}(R)^{\vee}$. (Check the dimension of $\D_{n}(\R)$; prove the map is linear; check its kernel.)

3. Find the basis of $\D_{n}(\R)$ dual to the standard basis $1,X,\ldots, X^{n}$ of $\Pol_{n}(\R)$. 

4. Let $H(f)=f(1)$ and $G(f)=\int_{0}^{1}f(X) dX$.  Both $H$ and $G$ are elements of the dual space to $\Pol_{n}(\R)$ and therefore correspond to elements of $\D_{n}(\R)$.  What are those elements?

### Problem 5.

Let $V$ be a vector space of dimension $n$ over a field $F$.  A *complete flag* in $V$ is a sequence
of subspaces
$$
Z: W_{0}=(0)\subset W_1\subset W_2\subset \cdots \subset W_{n-1}\subset W_{n}=V
$$
where $W_{i}$ has dimension $i$.  So for example, in $\R^{3}$, one could choose 
$W_{1}$ to be the span of the vector $\mathbf{i}$ (the $x$-axis) and $W_{2}$ to be the span of the $x$ and $y$ axes (the $xy$-plane). 

The group $\GL(V)$ acts on the flags in $V$ by acting on the subspaces:

$$
gZ = gW_{0}=(0)\subset gW_{1}\subset \cdots \subset gW_{n-1}\subset W_{n}=V.
$$

1. Prove that the action of $\GL(V)$ on the flags is transitive. 

2. Fix a basis $a_1,\ldots, a_n$ for $V$ and let $Z$ be the standard flag where $W_{0}=0$ and $W_{i}=\span(a_1,\ldots, a_i)$ for $i=1,\ldots, n$. 
Prove that $g\in \GL(V)$ stabilizes $Z$ if and only if $g$ is upper triangular in the matrix representation coming from the choice of basis $\lbrace a_{i}\rbrace$. 

3.  Use the orbit stabilizer theorem for $\GL(V)$ to give a formula for the number of flags in a vector space of dimension $n$ over a field with $q$ elements. 

4.  Find the number of  flags  in the three dimensional vector space over $\Z/2\Z$.

