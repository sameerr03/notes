A choice function $c:\chi\to X$ is an overwhelming choice if there exists a strict preference ranking $\succ\subseteq X\times X$ and a [[competition filter]] $\Gamma:\chi\to X$ such that for any $S\in \chi$, $c(S)$ is the $\succ$ best alternative in $\Gamma(S)$.

#### characterizing OC
##### eliciting preferences from choices
The binary relation $Q_c\subseteq X\times X$ is defined by:
$$xQ_cy\text{ if }x=c(S),y=c(T),\text{ for some }\{x,y\}\subseteq S\subseteq T$$
This is because as $y$ is considered in set $T$, and $\Gamma$ is a competition filter, $y$ is automatically considered in every menu that is a subset of $T$.

if $c:\chi\to X$ is an OC with parameters $(\succ,\Gamma)$, then for any $x,y\in X$, $$xQ_c\implies x\succ y$$
**Proof:** $xQ_cy\implies \exists (xy)\subseteq S\subseteq T$ such that $x=c(S)$ and $y=c(T)$
Because $y=c(T)\implies y\in\Gamma(T)$. However, because $\Gamma$ is a competition filter, this implies that $y\in \Gamma(S)$. As $c(S)=x$, this means that $$x\succ y$$
##### cyclicity
$c:\chi\to X$ is an OC if and only if $Q_c$ is acyclic.

##### OC and [[WARP#Weak WARP|weak WARP]]
If $c:\chi\to X$ is an OC, then $c$ satisfies weak WARP.

**Proof:** $(xy)\subseteq S\subseteq T$, $x=c(xy)=c(T)$
We need to prove that $y\ne c(S)$

Suppose $c$ is an OC with $(\Gamma,\succ)$. If $x=c(xy)$ this implies the possibility of two cases
1. $(xy)\in \Gamma(xy)$ and $x\succ y$
2. $(x)\in \Gamma(xy)$, i.e., $y\not\in \Gamma(xy)$

If 2 is the case, since $\Gamma$ is a competition filter, $y\not\in\Gamma(xy)\implies y\not\in\Gamma(S)\implies y\ne c(S)$

If 1,
$x=c(T)\implies x\in\Gamma(T)\implies x\in\Gamma(S)$
In this case, even if $y\in \Gamma(S)$, since $x\succ y$, we have $y\ne c(S)$

Thereby, OC implies weak WARP. 



