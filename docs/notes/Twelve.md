---
layout: default
title: Day 12
nav_order: 6.8
parent: Course Content
---

# Ring homomorphisms

## Some example computations with ideals and quotient rings

- ideals of $\Z$ and quotients
- ideals $(x^2+1)R$ of $R=\Q[x]$, $R=\R[x]$, and $R=\C[x]$ 
- Ring of functions $X\to A$ and the evaluation map at points of $X$.
- Evaluation map on polynomials $R[x]\to S$ extending $R\to S$ given by evaluation at $s\in S$.
- $\Zn{p}[x]/(f(x))$
- $\Z[i]/2$, $\Z[i]/3$, $\Z[i]/5$
- two sided ideals of $M_{n}(R)$ 
- examples of left ideals of $M_{n}(R)$.

## Isomorphism theorems

1. $R$ a ring, $A$ a subring, and $B$ and ideal of $R$.  Let $A+B=\lbrace a+b | a\in A, b\in B\rbrace.$
Then $A\cap B$ is an ideal of $A$ and $(A+B)/B\isom A/(A\cap B)$.
2. If $I$ and $J$ are ideals of $R$ and $I\subset J$, then $J/I$ is an ideal of $R/I$ and $(R/I)/(J/I)\isom R/J$.
3. Let $I\subset R$ be an ideal.  There is a bijective correspondence $A\to A/I$ between subrings
of $R$ containing $I$ and subrings of $R/I$.   This correspondence respects ideals, so $A/I$ is an ideal
of $R/I$ if and only if $A$ is an ideal of $R$. 

## Sums and products of ideals

1. The sum $I+J$ of two ideals is the collection of sums of elements of $I$ and $J$; it is an ideal.
2. The product $IJ$ is the subring generated by products $ab$ with $a\in I$ and $b\in J$; it is an ideal.
3. $I^{n}$ is the product of $I$ with itself $n$ times. it is an ideal.

## Prime and maximal ideals

Suppose that $R$ has an identity element $1$ (and that $1$ is not zero, so the ring is not trivial).

- An ideal $I=R$ if and only if $I$ contains a unit. 
- $R$ is a field iff its only ideals are zero and $R$. 
- Any homomorphism from a field $F$ to another ring $R$ is either zero or injective.
