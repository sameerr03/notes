#### Choquet integral
Let $f=(f_1,...f_n$) be an [[states of nature|act]], $u:X\to \mathbb{R}$ a utility function on $X$ and $v$ a **capacity** on $S$. Assume that $u(f_1)\ge u(f_2)\ge ...\ge u(f_n)\ge0$. We define the choquet integral w.r.t. the capacity $v$ by:$$\sum_{j=1}^{n-1}[uf_j)-y(f_{j+1})]v(\cup_{i=1}^js_j)+u(f_n)$$
##### Graphical explanation
![[Pasted image 20231123155211.png]]
![[Pasted image 20231123155239.png]]

#### Choquet integral Expected Utility (CEU)
$\succsim$ on $F$ has a CEU representation if there exists
- A capacity $v$ on $S$
- A non-constant utility function $u:X\to \mathbb{R}$.
such that the function $U:F\to \mathbb{R}$ given by $$U(f)=\sum_{j=1}^{n-1}[u(f_j)-u(f_{j+1})]v(\cup_{i=1}^js_j)+u(f_n)$$represents $\succsim$. 

Identification: Another pair ($\tilde v:A\to[0,1],\tilde u:X\to \mathbb R$) is a CEU representation of $\succsim$ iff $\tilde v=v$ and there exists constants $\beta>0,\beta'$ such that $\tilde u=\beta u+\beta'$. 

