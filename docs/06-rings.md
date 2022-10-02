---
layout: default
title: 6. Rings
nav_order: 6
parent: Course Content
---

## Rings - Basic Definitions and Examples

**Definition:** A ring is a set $R$ with *two* binary operations $+$ (addition) and $\times$ (multiplication) such that
1. $R$ is an abelian group under the addition operation.
2. Multiplication is associative.
3. The distributive law holds: $a\times(b+c)=a\times b+a\times c$ and $(b+c)\times a=b\times a+c\times a$. 
4. If multiplication is commutative, then $R$ is called a commutative ring.
5. If there is an identity element $1$ for multiplication, then $R$ is said to be a ring with identity or with unity. 

The properties of arithmetic you expect hold.  For example, if $-a$ is the additive inverse of $a$, then $(-a)(-b)=ab$. The identity element, if it exists, is unique.  See DF, Proposition 1 on page 226.


**Definitions:** Let $R$ be a ring with unity and assume $1\not=0$. 

1. A *unit* $x$ in $R$ is an element with a multiplicative inverse, so that there is $y$ such that $xy=yx=1$.  The
set $R^{*}$ of units in a ring form a group.
2. A *zero-divisor* in $R$ is a non-zero element $x$ such that there is $y\in R$ with $xy=0$ or $yx=0$. 
3. If every non-zero element in $R$ is a unit, then $R$ is called a *skew-field* or a *division ring*.
4. A commutative skew-field is called a *field.*
5. A commutative ring with no zero divisors is called a *domain* or an *integral domain.*

**Examples:** 

1. The rational numbers $\mathbb{Q}$, real numbers $\mathbb{R}$, and complex numbers $\mathbb{C}$ are all examples of
fields. 
2. The integers $\Z$ are a commutative ring with unity. It is also an integral domain, but not a field. 
3. For each $n\ge 2$, the groups $\Zn{n}$ are actually commutative rings with unity.  
4. If $p$ is prime, then $\Zn{p}$ is a field.
5. If $n$ is composite, then $\Zn{n}$ is not a domain.  Its units $(\Zn{n})^*$ are the multiplicative group of elements relatively prime to $n$. 
6. Let $R=C([0,1],\R)$ be the space of continuous real-valued functions on $[0,1]$.  $R$ is a commutative ring with unity; its units are the non-vanishing functions.  If $f$ vanishes at a point, then $f$ is not a unit, but it is also not a zero divisor.
7. The Gaussian integers $\Z[i]$ are an integral domain.  So is $\Z[\sqrt{2}]$. 
8. If $R$ is a ring, then the $n\times n$ matrices over $R$ are a ring  $M_{n}(R)$. If $R$ has a unit element, so does $M_{n}(R)$.
9. If $R$ is a commutative ring with unity, then $R[x]$, the polynomials over $R$, are a commutative ring with unity.    
10. If $R$ is any commutative ring with unity and $G$ is a finite group, then the group ring $R[G]$ consists
of functions on $G$ with multiplication by "convolution"
$$
(a*b)(g)=\sum_{h}a(h)b(gh^{-1})
$$
11. The real quaternion ring $\mathbb{H}$ consists of sums $a+b\mathbf{i}+c\mathbf{j}+d\mathbf{k}$ with multiplication
using the usual quaternion rules.  $\mathbb{H}$ is a division ring. 

**Proposition:** A finite integral domain is a field. 