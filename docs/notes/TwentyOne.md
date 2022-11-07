---
layout: default
nav_order: 11.3
title: Day 21
parent: Course Content
---
## Change of Basis

Given vector spaces $V$ and $W$ of dimension $n$ and $m$ respectively, and bases $a_1,\ldots, a_n$ and $b_1,\ldots, b_m$ for $V$ and $W$,
a linear map $L:V\to W$ has an $m\times n$ matrix representation

$$
[L]_{A}^{B}=\left[\begin{matrix} c_{11} & c_{12} &\cdots & c_{1n}\\\vdots & \vdots &\vdots &\vdots\\ c_{m1} & c_{m2} & \cdots & c_{mn}\end{matrix}\right]
$$

where the $c_{ij}$ are defined by

$$
L(a_{i}) = \sum_{j=1}^{m} c_{ji}b_{j}.
$$

If $v=\sum x_{i}a_{i}\in V$, define an $n\times 1$ matrix

$$
[v]_{A}=\left[\begin{matrix} x_{1}\\ \vdots \\x_{n}\end{matrix}\right]
$$

We can view this as an isomorphism from $V$ to $F^{n}$ if we write our elements of $F^{n}$ as column vectors.
We can do the same construction for $W$ and $F^{m}$, yielding $[w]_{B}$.

Then

$$
[Lv]_{B}=[L]_{A}^{B}[v]_{A}
$$

meaning that the matrix representation turns the map into matrix multiplication.

More generally if $L:V\to W$ and $H:W\to K$ are linear maps, and $A,B,C$ are bases for $V,W,K$ then

$$
[H\circ L]_{A}^{C} = [H]_{B}^{C}[L]_{A}^{B}.
$$

Now suppose we choose different bases $A'$ and $B'$ for $V$ and $W$.  

There is a unique invertible linear map $G:V\to V$ which satisfies $G(a_i')=a_i$ for $i=1,\ldots, n$. 
This means that if 

$$
v=\sum x_{i}a_{i}'
$$

then

$$
G(v)=\sum x_{i}a_{i}.
$$

**Important:** In this convention, the *inverse* of the linear map $G$ carries $a_{i}$ to $a_{i}'$, so if you look at its matrix 
$[G^{-1}]_{A}^{A}$ in the basis $A$, its columns give the coordinates of the new basis in terms of the old. This is in some ways the more natural
thing to consider.

Now

$$
[Gv]_{A} = [v]_{A'}.
$$

Since $[Gv]_{A}=[G]_{A}^{A}[v]_{A}$ we see that

$$
[v]_{A'} = [G]_{A}^{A}[v]_{A}.
$$

Now given a linear map $L:V\to W$ and basis $A'$ and $B'$ for $V$ and $W$, with:

-  $G$ the map carrying $a_i'$ to $a_i$, (note the convention here. The columns of $G^{-1}$ express the new basis in terms of the old one.) 
-  $H$ the map carrying $b_i'$ to $b_i$.

If $L(v)=w$ we know that the matrix for $L$ is characterized by 

$$
[L]_{A'}^{B'}[v]_{A'}=[w]_{B'}.
$$

Then

$$
[L]_{A'}^{B'}[G]_{A}^{A}[v]_{A}=[H]_{B}^{B}[w]_{B}
$$

so 


$$
[L]_{A'}^{B'}=(H_{B}^{B})^{-1}[L]_{A}^{B}G_{A}^{A}.
$$

So a change of basis on the source and target modifies the matrix of the linear map by left- and right- multiplication
by invertible matrices. 

### Example: Lagrange interpolation

Given $n+1$ points $x_0,\ldots, x_n$ in $\R$, there is a polynomial  of degree $n$ with prescribed values $f(x_i)=a_i$ 


Let

$$
f_{i}(x) = \frac{(x-x_0)(x-x_1)\cdots \widehat{(x-x_i)}\cdots (x-x_n)}{(x_i-x_0)\cdots (x_i-x_n)}
$$

This polynomial vanishes on all the $x$'s except $x_i$, where it takes value $1$.  These are linearly independent 
and 
$$
f=\sum a_i f_{i}
$$
is the desired expression.  

Now $x^{k}$ takes the value $x_i^k$ at $x_i$, so 

$$
x^k = \sum x_i^k f_{i}
$$

So the basis consisting of the powers of $x$, expressed in terms of the $x_i$, is the matrix
whose $k^{th}$ column, $i^{th}$ row  is $x_i^{k}$. Call this matrix $G$.

Let $D$ be the matrix giving the derivative operator on polynomials of degree $n$ in the standard basis $1,x,\ldots, x^n$.

Then $G^{-1}DG$ expresses the derivative operator in terms of the basis $f_{i}$. In practice this tells you have who to compute derivatives
from values of polynomials at chosen points.

See *Inverses of Vandermonde Matrices\ast, by N. Macon and A. Spitzbart, American Math Monthly 1958 vol 65 number 2. 

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

**Proposition:** If A is a finite basis for $V$ and $B$ is a finite basis for $W$ then let $A^{\ast}$ and $B^{\ast}$ be the corresponding dual bases.  Then
$[L^*]_{B^{\ast}}^{A^{\ast}}$ is the transpose of $[L]_{A}^{B}$.

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

### the double dual

The "Double dual" space $V^{\ast\ast}=\Hom(\Hom(V,F),F)$ is another vector space.  Notice that if $V$ is of dimension $n$ then $V^{\ast\ast}$ is also of dimension $n$.
But the relationship is closer than that.

Given $v$ in $V$, define $e_{v}$ in $V^{\ast\ast}$ by $e_{v}(f)=f(v)$.  This is called the "evaluation map".

If $V$ is finite dimensional, $e$ is an isomorphism.

In general, the evaluation map is injective but far from surjective. 







