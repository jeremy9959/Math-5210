---
layout: default
title: Day 2
nav_order: 1.8
parent: Course Content
---

**Euclid's Algorithm**

1. Well-ordering of the integers. Every nonempty set of positive integers has a least element.
2. Let $a$ and $b$ be nonzero integers.  Consider the set

$$
X= \{ax+by: x,y\in\Z \}
$$

1. $X$ contains positive elements.
2. $X$ contains a smallest positive element, call it $d$.  So $ax+by=d$.
3. Note that $X$ contains every (positive and negative) multiple of $d$. 
4. Take any other positive element $z$ of $X$.  Then $z=qd+r$ but also $z=ax'+by'$. 
Suppose $r>0$. So $qd+r=ax'+by'$ and therefore $r=a(x'-qx)+b(y'-qy)$. This means $r$ is in $X$;
but since $r$ is less than $d$, this cannot happen.  It follows that $r=0$ and every element of $X$
is a multiple of $d$. 
5. We conclude that $X=d\Z$.
6. Since $X$ contains both $a$ and $b$, we see that $d$ is a common divisor of $a$ and $b$.
7. If $g$ is any other common divisor of $a$ and $b$, then $g$ divides $d$.  
8. Therefore $d$ is the *greatest* common divisor of $a$ and $b$, and any other common divisor of $a$ and $b$
is a divisor of $d$.

**Theorem:** Given nonzero integers $x$ and $y$, the equation $ax+by=z$ has a solution if and only if $z$ is a multiple
of the greatest common divisor of $a$ and $b$. 

**Congruences**

The congruence equation 
$$
ax\equiv b\pmod{n}
$$
is equivalent to solving the equation
$$
ax+ny= b
$$

Euclid's algorithm tells us this equation has a solution if and only if $d=\gcd{a}{n}$ divides $b$.
If so, we can divide the equation through by $d$ to obtain
$$
\frac{a}{d}x+\frac{n}{d}y=\frac{b}{d}.
$$

Notice here that $a'=\frac{a}{d}$ and $n'=\frac{n}{d}$ have $\gcd{a'}{n'}=1$.  Having reduced to this case,
finish the proof of the fundamental congruences result.


**Cyclic Groups**

1. We know that $\Zn{6}$ is a subgroup of $\Zn{24}$.  Find all injective maps $\Zn{3}\to\Zn{12}$.
2. "Reduction mod 6" gives a surjective homomorphism $\Zn{24}\to\Zn{6}$.  Find the inverse image of $5$ under
this map. 
3. Find all surjective homomorphisms $\Zn{24}\to\Zn{6}$. 
4. Prove that $(\Zn{11})^{\times}$ is cyclic.  In fact $(\Zn{p})^{\times}$ is always cyclic, we'll prove this later.
5. Prove that the subgroups of a cyclic group of order $n$ are in bijection with the divisors of $n$. 

