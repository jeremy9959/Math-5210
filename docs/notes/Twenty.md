---
layout: default
title: Day 20
nav_order: 10.7
parent: Course Content
---

## More on subspace and dimension

### Some counting

Let $F$ be a finite field with $q=p^d$ elements.  Let $W$ be a $k$-dimensional vector space.  Then

1. The number of distinct bases of $W$ is $(q^{k}-1)(q^{k}-q)(q^{k}-q^2)\cdots (q^{k}-q^{k-1})$.
2. The number of subspaces of dimension $k$ is 
$$
\frac{(q^{n}-1)(q^{n}-q)\cdots (q^{n}-q^{k-1})}{(q^{k}-1)(q^{k}-q)\cdots(q^{k}-(q^{k-1})}
$$
3. The group $\Aut(V)$ has the same order as in part 1.  (To see this, fix a basis of $V$.  Given another basis, there is a bijective linear map from the fixed basis to this new basis.  So the number of linear
maps is the same as the number of different bases of $V$)

###

**Proposition:** If $W\subset V$ is a subspace, then the abelian group $V/W$ is a vector space with $a(v+W)=av+W$ being the scalar multiplication.
The "isomorphism theorem" for abelian groups holds for vector spaces as well. 

$$
\begin{xy}
\xymatrix {
V\ar[rd]^{f}\ar[d]^{\pi} &  \\
V/W\ar[r]_{\overline{f}} & K\\
}
\end{xy}
$$

We have $\dim(V)=\dim W +\dim(V/W)$.  A linear map $f:V\to K$ is equivalent to an injective linear map $V/\ker(f)\to K$, and identifies the quotient
with a subspace of $K$.

**Proposition:** If $V$ and $W$ are of the same finite dimension, and $f:V\to W$ is a linear map, then the following are equivalent:
1. $f$ is injective.
2. $f$ is surjective.
3. $f$ is bijective.
4. If $v_1,\ldots, v_n$ is a basis of $V$, then $f(v_1),f(v_2),\ldots, f(v_n)$ is a basis of $W$.