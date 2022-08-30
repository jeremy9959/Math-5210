---
layout: default
title: 2. Subgroups and quotient groups
nav_order: 2
parent: Course Content
---

# Subgroups and Quotient Groups

## Basic Definitions

Suppose $G$ is a group and $H$ is a subgroup of $G$.

1. The **centralizer** $C_{G}(H)$ of $H$ is the set of elements $g\in G$ such that $gh=hg$ for all $h\in H$. 
2. The **normalizer**  $N_{G}(H)$ of $H$ is the set of elements $g\in G$ such that $gHg^{-1}=H$.  In other words, $ghg^{-1}\in H$ for all
$h\in H$. 
4.  $H$ is a **normal subgroup** if $N_{G}(H)=G$.
5. The **center** $Z(G)$ of $G$ is the the of elements $z$ of $G$ such that $zg=gz$ for all $g\in G$. 
6. If $f:G\to H$ is a homomorphism, the **kernel** of $f$ is the set of $g\in G$ such that $f(g)=e$. 

Notice that:
1.  $C_{G}(H)\subset N_{G}(H)$
2.  The center $Z(G)$ is a normal subgroup of $G$. 
3.  $H\subset N_{G}(H)$ and $H$ is a normal subgroup of $N_{G}(H)$.
4.  The kernel of any homomorphism is a normal subgroup. (In fact, the converse is true as well, as we will see later)


## Subgroups from group actions

Suppose that $X$ is a set and $G$ acts on $X$.  Remember that one way to think of this is that we have a homomorphism from $G$ to $S(X)$.
Another way is that we have a map $G\times X\to X$ satisfying $ex=x$ and $g(h(x))=(gh)(x)$ for all $x\in X$ and all $g,h\in G$. 
Such an action yields subgroups of $G$ as follows:

1. The *kernel* of the action is the set of $g\in G$ such that $gx=x$ for all $x\in X$.  In other words, the kernel of the action is the kernel of the
homomorphism from $G$ to $S(X)$ corresponding to the action.  The kernel of the action is therefore a normal subgroup of G.
2. If $x\in X$, the set of elements $g\in G$ such that $gx=x$ is a subgroup of $G$ called the *stabilizer* of $x$. 
 

## Normalizers and centralizers via group actions

Let $\mathcal{P}(G)$ be the power set of $G$ -- that is, the set of subsets of $G$.  If $S\subset\mathcal{P}(G)$ is
a subset, define 
$$
g(S)=\{gsg^{-1} : s\in S\}.
$$
This defines an *action* of $G$ on $\mathcal{P}(S)$.

If we choose $S=H$, then by definition $N_{G}(H)$ is exactly the *stabilizer* of $H$ for this action.

If we restrict the action of $N_{G}(H)$ to the set $H$, then $C_{G}(H)$ is exactly the subset of $N_{G}(H)$
that fixes $H$ pointwise.  In other words, $C_{G}(H)$ is the *kernel* of the conjugation action of $N_{G}(H)$ on $H$. 

In general the operation $h\mapsto ghg^{-1}$ is called conjugation of $h$ by $g$. 