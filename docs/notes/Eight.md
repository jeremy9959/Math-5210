---
layout: default
title: Day 8
nav_order: 4.8
parent: Course Content
---

## Applications of Sylow's theorems

## Intersections of Sylow groups

**Lemma:** Let $p$ and $q$ be distinct primes and let $P$ and $Q$ be  Sylow $p$ and $q$ subgroups
of a finite group $G$. Then $P\cap Q$ is trivial.

**Proof:** An element of the intersection has order dividing a power of $p$ and a power of $q$,
so it must have order $1$.

### Abelian Groups

**Proposition:** Let $G$ be a finite abelian group and let $p$ be a prime dividing the order of $G$.
Let $P$ be the $p$-Sylow subgroup of $G$.  Then $P$ consists of the elements of $G$ whose order is a power of $p$.

**Proof:** Since $G$ is abelian, it's Sylow $p$-subgroup is unique. Clearly if $g\in P$ then the order
of $g$ is a power of $p$. Conversely if $g\in G$ has order a power of $p$, it generates a subgroup of $p$-power order, which must be contained in $P$. 

**Corollary:** Let $n$ be the order of $G$ and suppose $n=p^km$ where $(m,n)=1$.  Let $G[m]$ be
the elements of $G$ whose order divides $m$.  Then:

1. $G[m]$ is a subgroup of $G$.
2. $G[m]\cap P$ is the trivial subgroup. 
3. The map $G[m]\times P\to G$ given by $(a,b)\mapsto a+b$ is an isomorphism.

**Proof:** 

1. If $x$ and $y$ have order $h_1$ and $h_2$, both dividing $m$, then $\mathrm{lcm}(h_1,h_2)(x+y)=0$.  Let $h=\mathrm{lcm}(h_1,h_2)$, which divides $m$.  Then $h(x+y)=0$ so  $x+y$ has order dividing $m$ as well. 

2. This is the lemma above. 

3. If $(a,b)$ is in the kernel of the map, then since $a+b=0$ we have $a=-b$ which means both $a$
and $b$ are in the intersection of $G[m]$ and $P$.  By (2) this means $(a,b)=(0,0)$ so the map is injective. Then by counting we conclude it is surjective.  

**Corollary:** Any finite abelian group is isomorphic to the product of its Sylow $p$-subgroups.

This reduces the classification problem for finite abelian groups to the classification of finite abelian $p$-groups.

### Groups of order $pq$.

Suppose $G$ has order $pq$ and suppose $p\lt q$.  Let $Q$ be a Sylow $q$ subgroup. The number of such 
Sylow $q$ subgroups must be one of $1,p,q,pq$ and must be congruent to $1$ mod $q$.  The only possibility
is $1$.  Thus $Q$ is a normal subgroup.  Now let $P$ be any Sylow $p$-subgroup.  The intersection $P\cap Q$ is trivial so $PQ$ is a group of order $pq$ and must be $G$. 

Suppose further that $q\not\equiv 1\pmod{p}$.  Then $P$ must also be normal, because there cannot be $q$ Sylow $p$-subgroups.   $G$ acts on $P$
by conjugation, and in that action $P$ acts trivially (since $P$ is just a copy of $\Zn{p}$ which is
abelian).  Therefore $G/P\isom Q$ acts on $P$ by group automorphisms.  But $\Aut(P)\isom (\Zn{p})^{*}$
which has order $p-1$ and $Q$ is a cyclic group of order $q$, so there is no nontrivial map $Q\to\Aut(P)$. 
This means $Q$ commutes with $P$, so this group is abelian and in fact cyclic of order $pq$.

If $q\equiv 1\pmod{p}$, then the group need not be abelian.  For example $S_{3}$ or $D_{2n}$
with $n$ and odd prime are nonabelian groups of order $pq$ with $q\equiv 1\pmod{p}$. 

### Groups of order 30

**Proposition:** A group of order $30$ has a normal subgroup of index $2$ (which is necessarily cyclic of order $15$
by the previous problem).

**Lemma:** Let $P$ be a Sylow $3$-subgroup and $Q$ a Sylow $5$ subgroup.  If either of these groups is normal in $G$, then $PQ$ is a subgroup of $G$ of order $15$ -- which must be normal since it is of index $2$.  Now let $g\in G$.  Then $gQg^{-1}$ is contained in $PQ$ and since $Q$ is the Sylow $5$-subgroup of $PQ$ we have $gQg^{-1}=Q$.  Therefore $Q$ is normal in $G$; and similarly $P$ is normal in $G$.  So if either of the Sylow subgroups is normal, so is the other one, and we've found our subgroup.  

Assume therefore that neither of them is normal.  Then there must be at least $6$ conjugates of the Sylow 
$5$-subgroup and $10$ of the Sylow $3$ subgroup.  This accounts for $6*4+10*2=44$ elements of $G$, which
only has order $30$.  

### Groups of order $12$. 

**Proposition:** Let $G$ be a finite group of order $12$.  Then either $G$ contains
a normal subgroup of order $3$ or $G$ is isomorphic to $A_4$.

**Proof:** Let $n_{3}$ be the number of Sylow $3$-subgroups.  If $n_3=1$ we are done.
The divisors of $12$ are $1,2,3,4,6,12$.  If $n_3\gt 1$ then $n_3=4$.  Therefore the
group $G$ permutes the four Sylow $3$-subgroups transitively and this gives us a map
from $G$ to $S_{4}.  If $P$ is one such Sylow subgroup, the stabilizer of $P$ under this action is its normalizer, which contains
$P$ and thus has order at least $3$.  But its index must be $4$ since that's the size
of the orbit, so $N_{G}(P)=P$. 

The map to $S_{4}$ given by the conjugation action is injective.  To see this, suppose $x$ is
in the kernel of the action.  This means $xPx^{-1}=P$, $x\in P$.  But it also means $xgPg^{-1}x^{-1}=gPg^{-1}$ for one of the other conjugates of $P$.  That means $g^{-1}xg$ is also in $P$,
or $x\in gPg^{-1}$.  Since $gPg^{-1}$ is not $P$, the intersection of $P$ with $gPg^{-1}$ is a proper
subgroup of $P$, and since $P$ is cyclic of order $3$ that must be the trivial subgroup.

So the image of the permutation map is a subgroup of $S_{4}$ of order $12$. Furthermore,
the image meets $A_{4}$ in at least $9$ elements (the identity plus 8 elements of order 3). So it must be all of $A_4$. 

### A few more

Suppose $G$ has order $45$.  The divisors of $45$ are $1,3,5,9,15,45$.  The number of Sylow $3$-subgroups
has to be congruent to $1$ mod $3$, so it has to be $1$.  The number of Sylow $5$ subgroups has to be one mod $5$, so it has to be one.  So there is a normal subgroup of order $9$ and another of order $5$.
A group of order $9$ must be abelian so the only possibilities are $\Zn{3}\times\Zn{3}\times\Zn{5}$
or $\Zn{9}\times\Zn{5}$. 

The smallest possible odd order for a nonabelian group is $21$, and there is such a nonabelian group.
It has $7$ $3$-Sylow subgroups and a normal $7$-Sylow subgroup.  









