---
layout: default
title: Day 23
nav_order: 12.3
parent: Course Content
---

## Trace and Determinant

**Definition:** If $A=(a_{ij})$ is a matrix in $M_{n}(F)$, then the trace of $A$ is
$$\mathrm{Tr}(A)=\sum_{i=1}^{n} a_{ii}.$$

**Proposition:** The trace is linear in the matrix $A$. Also

$$
\mathrm{Tr}(ABC)=\mathrm{Tr}(BCA)=\mathrm{Tr}(CAB).
$$

In particular $\mathrm{Tr}(AB)=\mathrm{Tr}(BA)$.

**Proof:**

Let $X=AB$. Then

$$
x_{ik}=\sum_{j=1}^{n} a_{ij}b_{jk}.
$$

Now if $Y=XC$ then

$$
y_{rs}=\sum_{t=1}^{n} x_{rt}c_{ts}=\sum_{t=1}^{n}\sum_{j=1}^{n} a_{rj}b_{jt}c_{ts}
$$

and then $\mathrm{Tr}(Y)$ is

$$
\mathrm{Tr}(ABC)=\sum_{r=1}^{n} y_{rr} = \sum_{r=1}^{n}\sum_{t=1}^{n}\sum_{j=1}^{n} a_{rj}b_{jt}c_{tr}.
$$

On the other hand

$$
\mathrm{Tr}(BCA) =\sum_{j=1}^{n}\sum_{r=1}^{n}\sum_{t=1}^{n} b_{jt}c_{tr}a_{rj}
$$

which is just a rearrangement of the sum; and similarly for $\mathrm{Tr}(CAB)$.

**Trace of a linear map:**

This allows us to define the trace of a linear map as the trace of any matrix representing it --
different matrices differ by conjugation by the change of basis matrix.

Notice also that trace is a conjugacy class invariant in $\GL_{n}(F)$. Two conjugate matrices
have the same trace.

### Multilinear Functions

**Definition:** A function $H:V_1\times V_2\times\cdots\times V_{k}\to W$ is multilinear if
it is linear as a function of each variable, with the other variables held fixed.

A function $H:\overbrace{V\times\cdots\times V}^{n}\to F$ is called an $n$-multilinear form.

If $A=\lbrace a_{1},\ldots, a_{n}\rbrace$ is a basis for $V$, then an n-multilinear form is determined
by its values $H(x_1,\ldots, x_n)$ where each $x_i$ is chosen from $A$. There are $n^{n}$ such values.

For example if $\dim V=2$ with basis $a_1, a_2$ then

$$
H(x_{11}a_1+x_{12}a_{2},x_{21}a_1+x_{22}a_2) =
x_{11}x_{21}f(a_1,a_1)+x_{11}x_{22}F(a_1,a_2)+x_{12}x_{21}F(a_2,a_1)+x_{12}x_{22}F(a_2,a_2)
$$

The "dot product" is a 2-linear form (a "bilinear" form) on $\R^{n}$ or more generally
on $F^{n}$.

If we think of the trace as a function of the column vectors of a matrix, it is a multilinear form.

### Symmetric and Alternating forms

A multilinear form $H:V^{n}\to F$ is called *alternating* if $H(v_1,\ldots, v_n)=0$ whenever
two adjacent $v_{i}$ are equal to each other.  It is called *symmetric* if 
$H(v_1,\ldots, v_n)$ stays the same under rearrangement of the $v_{i}$. 

The dot product is a symmetric bilinear form since $H(v,w)=H(w,v)$.  

**Lemma:** If $H$ is an alternating multilinear form, then $H(v_1,\ldots, v_n)=0$
whenever two of the $v_{i}$ coincide; and $H(v_1,\ldots, v_n)$ changes sign
whenever two of the $v_{i}$ are interchanged.  More generally,

$$
H(v_{\sigma(1)},v_{\sigma(2)},\ldots, v_{\sigma(n)})=\mathrm{sgn}(\sigma)H(v_{1},\ldots, v_{n})
$$

where $\sigma$ is a permutation in $S_{n}$ and $\mathrm{sgn}(\sigma)$ is the sign character.

**Proof:**  Suppose $H_{i,i+1}(x,y)$ is the function $H$ with fixed entries in all positions
except $i$ and $i+1$.  Then
$H_{i,i+1}(x+y,x+y)=0$ by the alternating property; but
$$
H_{i,i+1}(x+y,x+y)=H_{i,i+1}(x,x)+H_{i,i+1}(x,y)+H_{i,i+1}(y,x)+H_{i,i+1}(y,y)
$$
by multilinearity.  Since the outer terms are zero by the alternating property, we get
$$
H_{i,i+1}(x,y)=-H_{i,i+1}(y,x).
$$

Now if $H_{i,j}(x,y)$ is $H$ with all positions fixed except $i$ and $j$, notice that
we can progressively swap adjacent values until $y$ is in position $i+1$, changing signs each time.
Therefore $H_{i,j}(x,y)=\pm H_{i,i+1}(x,y)$.  In particular $H_{i,i+1}(x,x)=0=H_{i,j}(x,x).$

Therefore $H(v_1,\ldots, v_n)=0$ whenever any two of the $v_{i}$ coincide; and repeating the argument we used for adjacent entries we get that $H(v_1,\ldots, v_n)$ changes sign when we swap any two variables.

Since an arbitrary permutation is a product of transpositions, and the sign character is defined
as $(-1)^k$ where $k$ is the number of such transpositions, we get the formula for a general permutation.

**Remark:** Why not define alternating to mean $H(v_1,\ldots, v_n)$ changes sign if we swap adjacent entries?  Look at characteristic two.

**Corollary:** If $H$ is alternating, and $w_{i}=v_{i}$ except that $w_{j}=v_{j}+av_{k}$ for some $j$,
then $H(w_1,\ldots,w_n)=H(v_1,\ldots, v_n)$.  Use linearity in the $j$ slot to see this.

An alternating multilinear form is defined by its values $H(a_1,\ldots, a_n)$ where the $a_i$ are chosen
from a basis of $V$, but these elements of $F$ have to satisfy the permutation property *and*
must vanish if any basis elements are repeated. 

If $V$ is $n$-dimensional and $a_1,\ldots, a_n$ is a basis, then an $n$-multilinear form is determined
by a single value $H(a_1,a_2,\ldots, a_n)$ and if $v_{i}=\sum x_{ji}a_{j}$ then
$$
H(v_1,\ldots, v_{n})=H(a_1,\ldots, a_n)\sum_{\sigma}\mathrm{sgn}(\sigma)x_{\sigma(1)1}x_{\sigma(2)2}\cdots x_{\sigma(n)n}.
$$

**Definition:** The determinant is the unique alternating multilinear map $\det: M_{n}(F)\to F$ such that
$\det(I)=1$.  Here $\det$ is viewed as a function of the columns of a matrix $A$.

**Lemma:** The determinant of $A$ and its transpose are the same. 

**Proposition:** $\det(AB)=\det(A)\det(B)$.

Proof: Let $C=AB$.  Then the columns of $C$ are linear combinations of the columns of $A$. In fact
$$
C_{j}=\sum_{i=1}^{n} b_{ij}A_{i}
$$
where $C_{j}$ and $A_{i}$ are the corresponding columns of $C$ and $A$. So 
$$
\det C = \sum (\mathrm{sgn}(\sigma) b_{\sigma(1)1}b_{\sigma(2)2}\cdots b_{\sigma(n)n})\det(A_1,\ldots A_n)
=\det(B)\det(A)
$$

