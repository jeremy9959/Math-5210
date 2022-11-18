---
layout: default
title: 12. Trace and Determinant
nav_order: 12
parent: Course Content
---

## Trace and Determinant

### Trace

**Definition:** The *trace* is the linear map 

$$
\mathrm{Tr}: M_{n}(F)\to F 
$$

given by the sum of the diagonal elements; namely, if $A=(a_{ij})$, then 

$$
\mathrm{Tr}(A)=\sum_{i=1}^{n} a_{ii}
$$

In addition to linearity, the Trace map satisfies the following property.

**Proposition:** If $A$ and $B$ are two matrices in $M_{n}(F)$, then $\mathrm{Tr}(AB)=\mathrm{Tr}(BA)$.
More generally, given three matrices $A$, $B$, and $C$, we have 

$$\mathrm{Tr}(ABC)=\mathrm{Tr}(BCA)=\mathrm{Tr}(CBA).$$  

**Definition:** If $L:V\to V$ is a linear map, then the trace of $L$ is the trace of the matrix
$[L]_{B}^{B}$ where $B$ is any basis of $V$.

This definition makes sense because any two matrix representations of the linear map $L$ are related
by conjugation: $$[L]_{B}^{B}=C[L]_{A}^{A}C^{-1}.$$ Then

$$
\mathrm{Tr}([L]_{B}^{B})=\mathrm{Tr}(C[L]_{A}^{A}C^{-1})=\mathrm{Tr}([L]_{A}^{A}C^{-1}C)=\mathrm{Tr}([L]_{A}^{A})
$$

so any two matrix representations have the same trace.

### Multilinear maps

**Definition:** A map $F:V_1\times V_2\times V_k\to W$ is called multilinear if

$$

F(v_1,\ldots, av_s,\ldots v_k)=aF(v_1,\ldots, v_s,\ldots, v_k)
$$

and 

$$
F(v_1,\ldots, v_s+v_s',\ldots, v_k)=F(v_1,\ldots, v_s,\ldots, v_k)+F(v_1,\ldots, v_s',\ldots, v_k)
$$

for any scalar $a$, index $s$, and vectors $v_s$ and $v_s'$ in $V_{s}$.  In other words,
$F$ is linear in each of its variables provided the other variables are held constant.

**Definition:** A multilinear linear map $F:V^{k}\to W$ is *alternating*
if $F(v_1,\ldots, v_k)=0$ whenever two of the $v_{i}$ are the same. 

### Determinant

The *determinant* of a matrix $A=(a_{ij})$ in $M_{n}(F)$ can be given by the formula

$$
\det A = \sum_{\sigma\in S_{n}} \mathrm{sgn}(\sigma) a_{1\sigma(1)}a_{2\sigma(2)}\cdots a_{n\sigma(n)}.
$$

For a two by two matrix this gives $$\det A=a_{11}a_{22}-a_{12}a_{21}$$.

**Proposition:** The determinant has the following properties.

- It is multiplicative, so that $\det(AB)=\det(A)\det(B)$.
- Viewed as a function of the columns of $A$ (so as a map from $V^{n}\to F$), it is an alternating multilinear map.
- The determinant of the identity map is $1$.

In fact, the determinant is the **unique alternating multilinear map from $M_{n}(F)\to F$
(taking the columns of the matrix as the independent variables) which takes the value $1$ on the
identity matrix.** Multiplicativity follows from this characterization.

**Proposition:** The determinant of the transpose of a matrix is the same as the determinant of the matrix. 

Other important properties of the determinant (see DF pgs 438-440):

- One can (in principle, but not in practice) compute it recursively using the "cofactor" expansion yielding the determinant of a big matrix as a linear combination of determinants of submatrices.

- There is a (useless in practice) formula for the inverse of a matrix in terms of determinants of submatrices. ("Cramer's Rule")

Although Cramer's rule is useless in practice it has the theoretical consequence that a matrix $M$ over an integral domain is invertible if and only if its determinant is a unit in $R$. It also says that given a matrix $M$ over an integral domain, there is always a matrix $N$ so that $MN=\det(M)I$. git