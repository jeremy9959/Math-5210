---
layout: default
title: Day 9
nav_order: 5.4
parent: Course Content
---
## Some more work with semidirect products

### Groups of order 12

If $G$ has order $12$, then it has a Sylow subgroup $V$ of order $4$ and a Sylow subgroup $P$ of order $3$.
Either $V$ or $P$ is normal.  To see this, note that $V\cap P$ is the identity. Suppose $P$ is not normal, so $n_3=4$.  Then there are 8 elements
of order $3$ in $G$, and together with the identity this accounts for $9$ elements of $G$.  So there are
at most $3$ elements, plus the identity, available for $V$, so $n_2=1$.  

Since either $V$ or $P$ is normal, $G=VP$.  

If they are both normal, then $G$ is abelian, and the possibilities are:

- $\Zn{2}\times\Zn{2}\times\Zn{3}$ (invariant factors are $6$ and $2$).
- $\Zn{12}$

If $G$ is not abelian, it is a semidirect product.  Also, $P$ is cyclic of order $3$ and $V$ is either cyclic or $\Zn{2}\times\Zn{2}$. 

1. $V$ is normal.

    a. $V=\Zn{4}$.  Then we need to look at maps $P\to \Aut(V)$.  But $P$ has order $3$ and $\Aut(V)$ has order $2$ so there are no nontrivial homomorphisms, so in this case $G$ is cyclic.

    b. $V=\Zn{2}\times\Zn{2}$.  The automorphisms of $V$ are $\GL_{2}(\Zn{2})$.  This group has order $6$ and is isomorphic to $S_{3}$; it acts on $V$ by permuting the three non-zero elements. 
    Therefore we can send the generator of $P$ to an automorphism that cyclically permutes those elements. The resulting semi-direct product is $A_4$.

2. $P$ is normal.  The automorphism group of $P$ is $\Zn{2}$, with non-trivial automorphism $x\to x^{-1}$ where $x$ is a generator of $P$. 

    a. $V=\Zn{4}$.  We need a map from $V\to \Aut(P)$, and there's only one, which sends the generator $y\in V$ to the automorphism $x\mapsto x^{-1}$.  This gives us a group
    with generators $x$ and $y$ such that $x^3=y^4=1$ and $yxy^{-1}=x^{-1}$. 

    b. $V=\Zn{2}\times\Zn{2}$.  In this situation there are three nontrivial maps $V\to \Aut(P)$ (either $(1,0)$, $(0,1)$ or $(1,1)$ acts like $x\mapsto x^{-1}$.)  The resulting group 
    has generators $x,y,z$ where $x^3=y^2=z^2=1$, $y$ and $z$ commute with each other, $x$ and $z$ commute with each other, and $yxy^{-1}=x^{-1}$. 
     (The actual choice of map $V\to\Aut(P)$ does not affect the isomorphism class of the result).  This is the group $D_{12}$ of symmetries of the hexagon. 
    

So there are five isomorphism types of groups of order $12$, two abelian, three nonabelian: $D_{12}$, $A_{4}$, and $\Zn{3}\semi\Zn{4}$. 

