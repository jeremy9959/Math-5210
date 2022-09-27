---
layout: default
title: Day 7
nav_order: 4.5
parent: Course Content
---
## Automorphisms

$\Aut(G)$ is the group of isomorphisms from $G$ to $G$ under composition.  

For $\Zn{n}$, the automorphism group is $\Zn{n}^{\times}$, the multiplicative group of elements relatively prime to $n$.

For $\Zn{n}^{k}$ the automorphism group is $\GL_{n}(\Zn{n})$, the invertible $n\times n$ matrices with entries in $\Zn{n}$. 

The *inner automorphisms* of $G$ are the conjugations $f_{g}:G\to G$ given by $f_{g}(h)=ghg^{-1}$. The inner
automorphisms form a normal subgroup of the automorphism group.  The quotient group is called the group of *outer automorphisms.*

$S_{n}$ has the weird property that all of its automorphisms are inner unless $n=6$.

## Conjugacy in $S_{n}$

The conjugacy classes in $S_{n}$ correspond to the cycle decompositions, and there is one class for each
partition of $n$ as a sum of positive integers.

The centralizer of a cycle are the permutations which fix the integers appearing in the cycle.

The normalizer of a cycle was computed  in the homework, at least in one case. 

## $A_{5}$ is a simple group

The conjugacy classes in $S_{5}$ that contain even permutations are contained in $A_{5}$ but they might
split up into multiple classes.
- there is one conjugacy class of 3-cycles in $A_{5}$ (there are 20 of these)
- there are two conjugacy classes of 5-cycles in $A_{5}$ (there are 4!=24 5 cycles, but they split into two groups of 12)
- all elements of order $2$ in $A_{5}$ are conjugate to $(12)(34)$. There are $15$ of these. 

So the conjugacy classes in $A_{5}$ have orders 1, 12, 15, and 20. 

If $H$ were a normal subgroup, it would have to have order dividing 60, or 1,2,3,4,5,6,10,12,15,20,30,60.
And it would have to be 1 plus a sum of some subset of 12,12,15,20.  The only way that works is if it has order
1 or 60.

## Proof of the Sylow theorems

See [the main page for this section.](https://jeremy9959.net/Math-5210/04-sylow.html)


## Discussion of proof of Sylow's theorems