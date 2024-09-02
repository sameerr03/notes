A capacity or a **non-additive probability** on the [[states of nature|state space]] $S$ is a function mapping $\mu:\xi\to[0,1]$, satisfying
- $\mu(\emptyset)=0,\mu(S)=1$
- For any $E, E'\subseteq S$, if $E\subseteq E'$, then $\mu(E)\le\mu(E')$

**Proof:**
For $E\subseteq E'$, $\mu(E)\le\mu(E')$

We know that 
$E'=E\cup (E'-E)$
Because $\mu$ is a probability,
$\mu(E')=\mu(E)+\mu(E'-E)$
But $\mu(E'-E)\ge 0$ as only $\mu(\emptyset)=0$ and $E'-E\ge \emptyset$ as $E\subseteq E'$
This implies that $\mu(E')\ge\mu(E)$


