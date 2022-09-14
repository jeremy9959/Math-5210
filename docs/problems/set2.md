---
layout: default
nav_exclude: true
---

# Problem Set 2

**Instructions:** Write up your solutions using LaTeX and submit them on HuskyCT by September 25, 2022.

**Problem 1:** Let $M$ and $N$ be normal subgroups of a group $G$ such that $G=MN$.

1. Prove that
$$
G/(M\cap N)\isom (G/M\times G/N).
$$
In the case where $M\cap N$ is trivial, we say that $G$ is the *internal direct product* of $M$ and $N$.
2. Prove inductively that $\Zn{m}$ is the internal direct product of the subgroups $\Zn{p_i^{e_i}}$ for $i=1,\ldots, k$ where $m=\prod_{i=1}^{k} p_{i}^{e_{i}}$ is the factorization of $m$ into powers of distinct primes. 

**Problem 2:** DF Problems 19-20 on Page 131. The conclusion of these problems is that, if $K(\sigma)$ is the conjugacy class of $\sigma$ in $S_{n}$, then $K(\sigma)$ is a conjugacy class in $A_{n}$ if and only if $\sigma$ commutes with an odd permutation.  Otherwise $K(\sigma)$ breaks up into two conjugacy classes.

**Problem 3:** (with thanks to Keith Conrad) The group $G=\SL_{2}(\Z)$ is the group of $2\times 2$
integer matrices with determinant $1$.  It acts on $\Z\times\Z$ viewed as column vectors with
integer entries by matrix multiplication.

1. Show that if $m\not=n$ in $\Z$ are positive, then $\left[\begin{matrix} m \cr 0\end{matrix}\right]$  
and $\left[\begin{matrix} n \cr 0\end{matrix}\right]$ are in different $G$-orbits. 
2. Show that the $G$ orbit of  $\left[\begin{matrix} x\cr y\end{matrix}\right]$ contains 
$\left[\begin{matrix} gcd(x,y)\cr 0\end{matrix}\right].$ Conclude that the orbits consist of the vectors
having the same gcd.
3. Show that the stabilizer of $\left[\begin{matrix} m \cr 0\end{matrix}\right]$ is the subgroup $N$
of upper triangular matrices with $1$ on the diagonal. 
4.  Conclude that the stabilizer in $G$ of a nonzero vector in $\Z^2$ is conjugate to $N$.
Make this explicit by finding an $A\in G$ so that $ANA^{-1}$ stabilizes $\left[\begin{matrix} 5 \cr 3\end{matrix}\right]$.


**Problem 4:** DF, Problem 18, p. 138.  This problem shows that if $n\not=6$ then every automorphism of $S_{n}$ is inner.
As it happens, $S_{6}$ has an outer automorphism, which is described in the Wikipedia article [Automorphisms of the symmetric and alternating groups](https://en.wikipedia.org/wiki/Automorphisms_of_the_symmetric_and_alternating_groups).

**Problem 5:** (another Keith Conrad problem)  Let $G$ be a group of order $1683=9\times 11\times 17.$

1. Prove $G=HK$ where $H$ is a cyclic normal subgroup of order $187$ and $K$ is a subgroup of order $9$.
2. Prove that $H$ and $K$ commute with each other.
3. Conclude that groups of order $1683$ are abelian (and up to isomorphism there are two of them).
