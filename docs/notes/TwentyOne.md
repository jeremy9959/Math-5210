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

Since $$[Gv]_{A}=[G]_{A}^{A}[v]_{A}$$ we see that

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

See *Inverses of Vandermonde Matrices*, by N. Macon and A. Spitzbart, American Math Monthly 1958 vol 65 number 2. 

