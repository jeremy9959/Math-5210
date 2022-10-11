---
layout: default
title: Day 13
nav_order: 7.4
parent: Course Content
---
**Proposition:** (Fermat) A prime number is the sum of two squares if and only if it is $2$ or is congruent to $1$ mod $4$. 

**Lemma:** The congruence $x^2\equiv -1\pmod{p}$ has a solution modulo a prime $p$ if and only if $p=2$ or $p\equiv 1\pmod{4}$. 

**Proof:** If $p=2$, $1$ is a solution.  If $p$ is odd, and $x^2=-1$ has a solution, then $(\Zn{p})^{*}$ has an element of order $4$, so $4\divides (p-1)$. 
Notice that $(\Zn{p})^{*}$ has only two elements of order dividing $2$, because of $x^2\equiv 1\pmod{p}$ then $p\divides (x^2-1)$, so $p\divides (x+1)(x-1)$, so either $x\equiv 1\pmod{p}$
or $x\equiv -1\pmod{p}$.  If $4\divides (p-1)$ then let $H$ be the Sylow $2$-subgroup of $(\Zn{p})^{*}$.  If $H$ were not cyclic, then there would be too many elements of order $2$ in $H$.
So $H$ must be cyclic and therefore there is an element of order $4$.

Now suppose that $p\equiv 1\pmod{4}$.  Let $u$ be a solution to $x^2+1\equiv 0\pmod{p}$.  Consider the ideal $I=(p,u+i)\subset \Z[i]$. This is a maximal ideal.
If $\pi=a+bi$ is a generator of this ideal, then $p=x\pi$.  If $x$ were a unit, then $u+i$ would have to be a multiple of $p$, which it visibly isn't.  Therefore $N(\pi)$ must be $p$.  
But $N(\pi)=a^2+b^2$, so we've found our representation. 

**Proposition:** The ring $\Z[\sqrt{-5}]$ is not a Euclidean ring.  In fact, the ideal $(3,1+\sqrt{-5})$ is not principal. It is a proper ideal, because the quotient of $\Z[\sqrt{-5}]$ by this ideal
is $\Zn{3}$.  If $\pi$ were a generator of this ideal,
then $3=x\pi$ means that either $N(\pi)=3$ or $N(\pi)=9$.  Also $(1+5i)=y\pi$ means that $N(\pi)$ divides $6$.  Since $\pi$ is not a unit, 
$N(\pi)=3$.  But the equation $x^2+5y^2=3$ has no integer solutions, so there is no element of norm 3 in this ring.  

