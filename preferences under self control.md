Suppose there is a set of alternatives $X$ and set of menus $\chi$. The DM has preferences on the set of menus. There are two stages of the DMs choice. 
- ex ante stage: DM chooses between menus
- ex post stage: DM chooses an alternative from the menu chosen in the previous stage

The preference relation $\succsim$ has a **preference for commitment** at $S$ if there exists $T\subseteq S$ such that $T\succ S$. The preference relation $\succsim$ has **self control** at $W$ if there exists $S,T$ such that $W=S\cup T$ and $T\succ S\cup T\succ S$.

#### Gul-Pesendorfer (GP) representation
There exists functions $u,v:X\to \mathbb R$ such that the function $U:\chi\to\mathbb R$ given by $$U(S)=\text{max}_{x\in S}\{u(x)-[\text{max}_{y\in S}(v(y))-v(x)]\}$$represents $\succsim$
Here:
- $u$ is the DMs commitment utility
- $v$ is the DMs temptation utility
- $\text{max}_{y\in S}(v(y))-v(x)$ is the cost of exercising self-control in choosing $x$ from a menu against the most tempting option $y$.

The second stage choice is represented by $$c(S)=\text{argmax}_{x\in S}\{u(x)-[\max_{y\in S}-v(x)]\}$$The second stage choice satisfies [[WARP]]. Self control may result in menu effects in this model however. 

##### Convex self-control cost function
$$c(S)=\text{arg}\max_{x\in S}\{u(x)-\varphi(\max_{y\in S}-v(x))\}$$Where $\varphi$ is a convex function. 

##### Menu effects example
![[Pasted image 20231210013631.png]]
$\varphi(r)=r^2$

Consider the menu $S=\{x,y\}$
For $x$, $$u(x)-\varphi(\max_{w\in S}v(w)-v(x))=13-(3-1)^2=9$$For $y$, $$u(y)-\varphi(\max_{w\in S}v(w)-v(y))=7-(3-3)^2=7$$Therefore $$c(S)=x$$
Consider the menu $S'=\{x,y,z\}$
For $x$, $$u(x)-\varphi(\max_{w\in S'}v(w)-v(x))=13-(5-1)^2=-3$$For $y$, $$u(y)-\varphi(\max_{w\in S'}v(w)-v(y))=7-(5-3)^2=3$$For $z$,
$$u(z)-\varphi(\max_{w\in S'}v(w)-v(z))=2-(5-5)^2=2$$
Therefore $$c(S')=y$$This demonstrates a menu effect.