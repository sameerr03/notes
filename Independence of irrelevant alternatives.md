$$\text{For all }A,B\in\chi \text{ such that } A\subseteq B$$$$c(B)\in A\implies c(A)=c(B)$$
This means that in the case of $A$ being a subset of $B$, if the chosen alternative is in the section overlapping $B$ and $A$ (or **not** in the region of $B-A$), then the alternative chosen in $A$ and $B$ will be the same. This theory states [[WARP]] in a different way

#### IIA and WARP - Implications
##### 1. WARP Implies IIA
Let $S \subseteq T$ and $c(T)\in S$. To show that WARP implies IIA, we need to show that $c(S)=c(T)$. 

Let us call $c(T)=x$. We know that $x=C(T)$ and thus any $y$ in $S$ is also present in $T$. WARP implies that $$c(S)\ne y \text{ for any }y\in S,y\ne x$$However, $$c(S)\ne \emptyset$$Therefore, $$c(S)=x\implies c(S)=c(T)$$This shows that WARP implies IIA.

##### 2. IIA implies WARP
Let $x,y\in X$ and $S,T\in \chi$ such that $x,y\in S\cap T$ with $c(S)=x$. In order to show that IIA implies WARP, we need to show that $y\ne c(T)$.

To prove this by contradiction, we assume that $C(T)=y$. This implies that $x,y\in S\cap T$ and $x=c(S)$ and $y=c(T)$.

Considering $S\cap T$, using IIA
$$c(T)=y,\ (S\cap T)\subseteq T\implies c(S\cap T)=y$$However, at the same time, $c(S)=x$ and $x,y\in S\cap T$. As $x$ and $y$ are both present in the set interaction, this is a contradiction as with rational choices, if $x$ is present in the same choice set as $y$, only one of them is chosen over the other all times. Therefore, our assumption is proven wrong by contradiction. $$\implies c(T)\ne y$$Therefore, IIA implies WARP.  
