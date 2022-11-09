---
layout: default
nav_exclude: true
---

## Change of Basis and Lagrange Interpolation

Fix a positive integer $n$ and a field $F$ and consider the $n+1$ dimensional $F$-vector space
$$
\mathrm{Pol}_{n}(F)=\lbrace \sum_{i=0}^{n} a_{i}x^{i} \rbrace
$$
of polynomials of degree at most $n$ over $F$.

This vector space has the "obvious" basis $A=\lbrace 1, x, \ldots, x^{n}\rbrace$.

Now suppose we are given $n+1$ points $y_0,y_1,\ldots, y_n$ in $F$ and $n+1$ corresponding elements 
$c_0,\ldots, c_n$ in $F$.  We can construct a polynomial $f\in \mathrm{Pol}_{n}(F)$ that
has the property that $f(y_i)=c_i$ for $i=0,\ldots, n$.  

A nice way to do this is to construct a new basis $B$ for the polynomials consisting of
$\lbrace g_0,\ldots, g_n\rbrace$
where

$$
g_{i}(x)=\frac{(x-y_0)(x-y_1)\cdots\overbrace{(x-y_i)}^{\mathrm{omit}}\cdots (x-y_n)}{(y_i-y_0)\cdots (y_i-y_n)}
$$

The polynomials $g_{i}(x)$ have the property that

$$
g_{i}(y_{j})=\begin{cases} 1 & i=j\\0 & i\not=j\end{cases}
$$

These polynomials are a basis for $$\mathrm{Pol}_{n}(F)$$ because there are $n+1$ of them and they are linearly independent;
if
$$
\sum b_{i}g_{i}(x)=0
$$
then evaluating this at $y_{j}$ forces $b_{j}=0$ for $j=0,\ldots, n$.

Then we can construct our polynomial with prescribed values $c_{i}$ at $y_{i}$ by setting

$$
f(x)=\sum c_{i}g_{i}(x)
$$

Let's work out the change of basis process between the bases $A$ and $B$ described above. For the sake of concreteness, let $$D:\Pol_{n}(F)\to\Pol_{n}(F)$$ be the differentiation operator, the linear map
$$
D(f)(x)=f'(x).
$$

In terms of the standard basis $A$ consisting of powers of $x$, we find the basis of $D$ by computing
$$
D(x^i)=ix^{i-1}.
$$
Since the basis elements are $$a_i=x^i$$, this means $$D(a_i)=ia_{i-1}$$
and so

$$
[D]_{A}^{A}=\left[\begin{matrix} 0 & 1 & 0 &0 &\cdots & 0 \\
                                 0 & 0 & 2 & 0 &\cdots & 0 \\
                                 0 & 0 & 0 & 3 &\cdots & 0 \\
                                 \vdots & \vdots &\vdots &\vdots &\vdots&\vdots \\
                                 0 & 0 & 0 & 0& \cdots & n \\
                                 0 & 0 & 0 & 0& \cdots & 0\\\end{matrix}\right]
$$

Now in the notation of [these notes](jeremy9959.net/Math-5210/notes/TwentyOne.html) our change of basis formula says that

$$
[D]_{A}^{A} = [G^{-1}]_{B}^{B}[D]_{B}^{B}[G]_{B}^{B}
$$

where $G$ is the linear map that satisfies $G(x^{i})=g_{i}$ and $G^{-1}(g_{i})=x^i$.
The matrix $$[G^{-1}]_{B}^{B}$$ is the easiest to compute, because the *columns of this matrix
are the powers of $x$ written in terms of the $g_{i}$*.  The interpolation formula gives us

$$
x^{i}=\sum_{j=0}^{n}y_{j}^ig_{i}(x)
$$

so  $[G^{-1}]_{B}^{B}$ is what's called a Vandermonde matrix:

$$
[G^{-1}]_{B}^{B} = \left[\begin{matrix} 1 & y_0 & y_0^2 &\cdots & y_0^n \\
                          1 & y_1 & y_1^2 &\cdots & y_1^n \\
                          \vdots & \vdots &\vdots &\vdots &\vdots \\
                          1 & y_n & y_n^2 &\cdots & y_n^n\\
                          \end{matrix}\right]
$$

To lighten the notation a little bit, let's call this matrix $M$ and we see that

$$
[D]_{A}^{A} = [G^{-1}]_{B}^{B}[D]_{B}^{B}[G]_{B}^{B} = M^{-1}[D]_{B}^{B}M
$$

and

$$
[D]_{B}^{B} = M[D]_{A}^{A}M^{-1} 
$$

In the concrete case where $y_0=-1,y_1=0,y_2=1$, we have

$$[D]_{B}^{B} = 
\left[\begin{array}{ccc}
-\frac{3}{2} & 2 & -\frac{1}{2} 
\\
 -\frac{1}{2} & 0 & \frac{1}{2} 
\\
 \frac{1}{2} & -2 & \frac{3}{2} 
\end{array}\right]
$$

What this means is that $f(x)$ is a polynomial that satisfies $f(y_0)=c_0$, $f(y_1)=c_1$ and $f(y_2)=c_2$,
then the corresponding values of $f'$ at these three points are the entries in the vector

$$
\left[\begin{array}{ccc}
-\frac{3}{2} & 2 & -\frac{1}{2} 
\\
 -\frac{1}{2} & 0 & \frac{1}{2} 
\\
 \frac{1}{2} & -2 & \frac{3}{2} 
\end{array}\right]\left[\begin{matrix} c_0 \\ c_1 \\c_2\end{matrix}\right]=\left[\begin{matrix}
-(3/2)c_0+2c_1-(1/2)c_2 \\(c_2-c_0)/2 \\ (1/2)c_0-2c_1+(3/2)c_2\end{matrix}\right]
$$
