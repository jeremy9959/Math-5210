---
layout: default
nav_exclude: true
---
## The fundamental theorem of finitely generated abelian groups

**Theorem:** Let $G$ be a finitely generated abelian group.  Then there is an integer $r\ge 0$
and integers $d_1,\ldots, d_k$ all at least two such that
$$
G\isom \mathbb{Z}^{r}\times \mathbb{Z}/d_{1}\mathbb{Z}\times\cdots\times\mathbb{Z}/d_{k}\mathbb{Z}.
$$

**Remark:** The integer $r$ is determined by $G$ up to isomorphism.  There are various ways to standardize
the $d_{i}$ so that they determine $G$ up to isomorphism but we take that up separately.

We will give a more-or-less constructive proof of this theorem. 

Let $g_1,\ldots, g_s$ be a generating set for $G$.  Consider the surjective homomorphism
$$
\pi: \overbrace{\Z\times\cdots\times\Z}^{s} \to G
$$

that sends the element $e_{i}$ having a one in position $i$ and zeros elsewhere to $g_{i}$. 

By the isomorphism theorems, if $N$ is the kernel of this map, then $G$ is isomorphic to $\Z^{s}/N$. 
We will study $N$.

Let's write the elements of $\Z^{s}$ as column vectors using the basis $\lbrace e_{i}\rbrace_{i=1}^{s}$. 
At first we know very little about $N$ except that it is generated by a (potentially infinite) set
of elements of $\Z^{s}$.  Let's choose generators $n_{1},n_{2},\ldots$ for $N$ and organize them in
a matrix with integer entries  (and potentially infinitely many columns):

$$
\mathbf{N}=\left[\begin{matrix} n_{11} & n_{12} & n_{13} & \ldots \cr
                     \vdots & \vdots & \vdots & \vdots \cr
                     n_{s1} & n_{s2} & n_{s3} & \ldots \cr\end{matrix}\right]
$$                     

First we are going to show that in fact $N$ is finitely generated, so we can assume $N$ has only finitely many columns. 

### Subgroups of finitely generated abelian groups are finitely generated. 

**Lemma:**  We show first that any subgroup of $\Z^{s}$ is finitely generated. 

**Proof:** We will proceed by induction on $s$.  If $s=1$, $N$ is a subgroup of $\Z$, and we know that any such subgroup is of the form $d\Z$ and is therefore generated by one element.  

Suppose that any subgroup of $\Z^{s-1}$
is finitely generated and that  $n_{1},\ldots$ generate $N\subset \Z^{s}$.  Consider the last row of the associated matrix $\mathbf{N}$. The integers $n_{s1},n_{s2},\ldots$ generate a subgroup of $\Z$  that is generated by 
the smallest positive element $d$ of this subgroup, which is the greatest common divisor of all of these $n_{sj}$. 
Then there are finitely many indices $i_1,i_2,\ldots,i_p$ and integers $a_{1},\ldots, a_{p}$ such that

$$
d=\sum_{j=1}^{p} a_{j}n_{si_{j}}.
$$

The vector $n=\sum_{j=1}^{p}a_{j}n_{i_{j}}\in N$ has $d$ as its last element.  For each column $n_{i}$ of $\mathbf{N}$,
there is an integer $k_{i}$ so that $n_{i}'=n_{i}-k_{i}n$ has a zero in its last entry. The set consisting of $n$
and the $n_{i}'$ generate $N$.  But the $n_{i}'$ all belong to a copy $\Z^{s-1}$ since their last entry is zero,
so by induction the subgroup of $\Z^{s-1}$ they generate is finitely generated.  
Therefore $N$ is finitely generated.

In fact we've shown that any subgroup of $\Z^{s}$ is generated by at most $s$ elements because we add at most one generator at each step in the induction.

**Corollary:** Any subgroup of a finitely generated abelian group $G$ is finitely generated.

**Proof:** A finitely generated abelian group is a quotient of $\Z^{s}$.  Given a subgroup $H$ of $G$,
it is the image of a subgroup $\tilde{H}$ of $\Z^{s}$, which is finitely generated.  The images of the generators
of $\tilde{H}$ in $H$ generate $H$.

**Note:** THIS IS FALSE for nonabelian groups.

### Proof of the fundamental theorem

As above, given as finitely generated abelian group, choose a surjective map

$$
\pi: \Z^{s}\to G.
$$

The kernel $N$ of this map is generated by a set $\mathbf{n}$ of at most $s$ elements, and we can arrange the generators of the kernel into a $s\times s$ matrix $\mathbf{N}$, adding zero columns if necessary.

The matrix $\mathbf{N}$ defines a homomorphism (we use the sa)

$$
\mathbf{N}:\Z^{s}\to\Z^{s}
$$

sending an element of the first $\Z^{s}$ viewed as a column vector $v$ to the second by matrix multiplication $\mathbf{n}v$. .  

The image of this homomorphism is exactly the kernel $N$ of the map $\pi$.  This is because $N$ is generated
by the columns of the matrix $\mathbf{N}$, and if

$$
v=\left[\begin{matrix} v_1\cr \vdots \cr v_s \cr\end{matrix}\right]
$$ is a column vector, 

then 

$$
\mathbf{N}v=\sum_{i=1}^{s} v_{i}n_{i}
$$

where the $n_{i}$ are the columns of $\mathbf{N}$, so the collection of products $\mathbf{N}v$ is exactly the subgroup
of $\Z^{s}$ generated by the columns of $N$.

We showed the following in our discussion of automorphisms.

**Lemma:** Suppose $f:\Z^{s}\to\Z^{s}$ is an automorphism.  Then there is an invertible $s\times s$ matrix
$\mathbf{F}$ with integer entries so that $f(v)=\mathbf{F}v$ where we write $v\in\Z^{s}$ as a column vector.

The composition $\mathbf{N}\circ f$ is given by the matrix $\mathbf{N}\mathbf{F}$.  Since $f$ is an automorphism,
the image of $\mathbf{N}\mathbf{F}$ in $\Z^{s}$ is the same as the image of $\mathbf{N}$, namely $N$.

Now suppose we apply an automorphism $k$ of $\Z^{s}$ on the right side of the map $\mathbf{N}$.  In that case,
the image $k(N)$ need not be $N$, but it is still the case that $\Z^{s}/g(N)$ and $\Z^{s}/N$ are isomorphic,
and therefore $\Z^{s}/g(N)$ is isomorphic to our original group $G$.

Therefore up to isomorphism we can modify our matrix $\mathbf{N}$ by multiplying it on either side
by invertible $s\times s$ integer matrices without changing the quotient $G$ we are trying to compute.

In particular we can:

- swap rows and columns of $\mathbf{N}$
- multiply any row or column of $\mathbf{N}$ by $\pm 1$
- do elementary row and column operations on $\mathbf{N}$ -- that is, replace a column $n_{i}$ by $n_{i}-an_{j}$ for
any integer $a$, and similarly for rows.

Using these operations, proceed as follows:

0. If the matrix is zero, the $G$ is $\Z^{s}$ and we're done.  Otherwise, swap rows so the first row isn't zero.
1. Make every element in the first row positive, and then swap columns so the smallest element in the first row is in the upper left corner of $\mathbf{N}$.  Call that element $a$.
2. Use elementary column operations to reduce the other elements in the first row to be less than $a$.
3. Repeat steps $1$ and $2$ until the upper left entry is the only nonzero entry.
4. Now follow the same process using row operations until the only nonzero entry in the first column is in the upper left corner.
5. Each round of this makes the entry in the upper left corner smaller, so eventually you must reach a point
where the first row and column of the matrix are zero, except for the upper left entry, which could be zero or nonzero.
6. Now continue this reduction process on the $(s-1)\times (s-1)$ submatrix.
7. Eventually you reach a diagonal matrix.  

When you have a diagonal matrix, you can see that 

$$
G\isom \Z^{r}\times \Z/d_{1}\Z\times \cdots \Z/d_{s-r}\Z
$$ 

where $r$ is the number of zero diagonal elements and the $d_{i}$ are the nonzero ones.

**Corollary:** If the matrix $\mathbf{N}$ is invertible, its determinant is the order of $G$.
