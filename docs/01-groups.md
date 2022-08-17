---
layout: default
title: 1. Groups
nav_order: 1
parent: Course Content
---
# Quick Review of Group Theory

**Definition:** A group is a set $G$ together with a map $m: G\times G\to G$ satisfying
the following axioms:

a.  There is an element $e\in G$ such that $m(e,x)=m(x,e)=x$ for all $x\in G$.  
b.  For all $x,y,z\in G$, we have $m(x,m(y,z))=m(m(x,y),z)$.
c.  For all $x\in G$, there is $y\in G$ such that $m(x,y)=m(y,x)=e$.

We usually just write $ab$ or $a+b$ for $m(a,b)$; and we usually write $G$, rather than $(G,m)$
when speaking about a group.

One can weaken these axioms and obtain an equivalent definition.  

For any group $G$ and $x\in G$:
    - there is only one element $e$ satisfying axiom (a).
    - the regrouping in axiom (b) extends to arbitrary many elements, so the product $a_1 a_2 \cdots a_n$ is well
    defined for any set of elements $a_1,a_2,\ldots, a_n\in G$. 
    - the inverse $y$ for $x$ required by axiom (c) is unique.

**Definition:** If $G$ is a group and $ab=ba$ for all $a,b\in G$ then $G$ is called *abelian*.

**Definition:** If $G$ is a group and $g\in G$ then the *order* of $g$ is the smallest positive integer $n$
such that $g^{n}=e$ (or infinity, if no such $n$ exists).


