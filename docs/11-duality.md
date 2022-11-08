---
layout: default
title: 11. Duality
nav_order: 11
parent: Course Content
---

## Change of Basis

We work out how the choice of basis affects the passage from linear maps to matrices. See DF page 419.
Axler works this out, partly in the exercises, in Section 3D of LADR.

## Duality

The dual vector space $\Hom(V,F)$ consists of linear maps from $V$ to the one-dimensional vector space $F$. We write this vector space as $V^{\ast}$; it is called the *dual space*.

If $L:V\to W$ is a linear map, there is an associated linear map
$$
L^{\ast}:W^{\ast}\to V^{\ast}
$$

defined by $L^{\ast}(f)(v)=f(L(v))$.  

Duality is an example of a *contravariant functor.*

If $L:V\to W$ and $G:W\to K$ then $L^{\ast}:W^{\ast}\to V^{\ast}$ and $G^{\ast}:K^{\ast}\to W^{\ast}$.
Then
$$
(L\circ G)^{\ast}=G^{\ast}\circ L^{\ast}.
$$

If $f: W\subset V$ is the inclusion map of a subspace then $f^{*}$ is the restriction map from functions on $V$ to functions on $W$.  

If $\pi: V\to V/W$ is the projection to the quotient space, then $\pi^{\ast}:(V/W)^{\ast}\to V^{\ast}$
is the "extension" map that views a function on $V/W$ as a function on $V$ that vanishes on $W$.
 
If $W\to V\to V/W$ is an "exact sequence" then the dual $(V/W)^{\ast}\to V^{\ast}\to W^{\ast}$
is also "exact".  The first map takes a function on $V/W$ and views it as a functional on $V$ vanishing on $W$; the second map restricts a function on $V$ to $W$.  So the kernel of the second map is the image of the first. 

**Proposition:** The restriction map from $V^{\ast}$ to $W^{\ast}$ is surjective and the "extension" map
from $(V/W)^{\ast}$ to $V^{\ast}$ is injective.

If $L:V\to W$ is a linear map, then $L$ is an injective map $V/K\to H\subset W$ where $K$ is the kernel of $L$ and $H$ is its range.  