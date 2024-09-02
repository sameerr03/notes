The choice function $c:\chi\to X$ is a CLA is there exists a strict preference ranking $\succ$ on $X$ that is complete and transitive and an [[Attention filter]] $\Gamma:\chi\to\chi$ such that for any $S\in \chi$, $c(S)$ is the best alternative in $\Gamma(S)$ with respect to $\succ$.

#### characterization of a CLA
[[WARP]] fails to hold with a CLA.$$(xy)\subseteq S\subseteq T$$but $c(xy)=c(S)=x$ and $c(T)=y$ due to $\Gamma(T)$


##### eliciting preferences from choices
**Example:**
consider the choice set $c(xyz)=x; c(xy)=x; c(yz)=y; c(xz)=z$
suppose that $y\not\in\Gamma(xyz)$. Then because the [[Consideration set]] is an attention filter, it must be that $$\Gamma(xyz)=\Gamma(xz)$$However, $$c(xz)=z\ne c(xyz)=x$$Therefore, $y$ must be considered in the choice set in $xyz$. Therefore, $c(xyz)=x$ implies that $x\succ y$ according to a CLA. We cannot say if $z$ is considered as $x$ could not have been a part of $\Gamma(xz)$ making $z$ the only viable choice in $(xz)$.


The relation $P_c\subseteq X\times X$ is defined by
$xP_cy$ if there exists a menu $T$ such that $x,y\in T$ and $c(T)=x\ne c(T-y)$

If $c:\chi\to X$ is a CLA with the parameters $(\succ, \Gamma)$, then for any $x,y\in X$,$$xP_cy\implies x\succ y$$**Proof:** We know that $xP_cy\implies \exists\ T$ such that $x=c(T)\ne c(T-y)$ with $x,y\in T$. If $c$ is a CLA with the parameters $(\succ, \Gamma)$, from the fact that $c(T)\ne c(T-y)$, this implies that$$y\in \Gamma(T)$$for if this was not the case, and $y\not\in \Gamma(T)$, then because $\Gamma$ is an attention filter, $\Gamma(T)=\Gamma(T-y)$ and accordingly, $c(T)=c(T-y)$. However this contradicts the antecedent that $xP_cy$. Therefore, $y\in \Gamma(T)$ and $x=c(T)$. Therefore, this implies that$$x\succ y$$

##### cyclicity of preferences
$c:\chi\to X$ is a CLA if and only if $P_c$ is acyclic. 