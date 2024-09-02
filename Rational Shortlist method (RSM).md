In this method of decision making, the DM uses two "rationales" to discriminate between choices.

A choice function is an RSM whenever there exists an ordered pair $(\succ_1,\succ_2)$ of asymmetric binary relations on $X$ such that for any $S\in X$$$c(S)=\text{max}(\text{max}(S;\succ_1);\succ_2)$$
In any menu $S$, the un-dominated alternatives in $S$ according to the preference relation $\succ$ is given by $$\text{max}(S;\succ)=\{x\in S\}\text{ then there does not exist a }y\in S \text{ s.t. } y\succ x$$In the RSM, the DM has two such preference rankings, $\succ_1, \succ_2$ and alternates between them. 

#### Decision making
- All the dominated alternatives of $S$ according to $\succ_1$ are eliminated. The DM is left with the shortlisted alternatives.$$\text{max}(S;\succ_1)$$
- The dominated alternatives are then eliminated according to $\succ_2$ from the max set of shortlisted elements$$\text{max}(\text{max}(S;\succ_1);\succ_2)$$

Consider $X=\{a,b,c\}$: $b\succ_1c;c\succ_2a;a\succ_2b;c\succ_2b$
$\text{max}(a,b,c;\succ_1)=\{a,b\}$ as c is dominated
$\text{max}(\text{max}(a,b,c;\succ_1);\succ_2)=a$ as b is dominated

#### Characterizing an RSM
A choice function $c:\chi\to X$ is an RSM if and only if it satisfies [[WARP#Weak WARP|weak WARP]] and [[Expansion axiom]]. 

Let $c$ be an RSM with two rationales $(\succ_1,\succ_2)$
###### Weak WARP
let $\{x,y\}\subseteq S\subseteq T$
$x=c(xy)=c(T)$

In order to satisfy weak WARP, $y\ne c(S)$
If $x=c(xy)$, then either 
1. $x\succ_1 y$
2. $\neg(y\succ_1x)$ and $x\succ_2 y$ i.e., $x$ and $y$ are not comparable by the first rationale and $x$ dominates $y$ by the second.

**Considering case 1,**
Since $x\succ_1 y$ this means that $y\notin \text{max}(S;\succ_1)$
$$\implies y\ne c(S)$$
**Considering case 2,**
$x=c(T)\implies x\in\text{max}(T;\succ_1)$
this means that there does not exist $\not\exists\ z\in T$ s.t. $z\succ_1 x$

However, $S\subseteq T$
This means that $\not\exists\ z\in S$ s.t. $z\succ_1 x$
$\implies x\in \text{max}(S;\succ_1)$

from the case statement, we know that $x\succ_2 y$. Even if $y\in \text{max}(S;\succ_1)$, then since $x\in \text{max}(S;\succ_1)$ and $x\succ_2 y$$$\implies y\ne c(S)$$
Therefore, if $c$ is an RSM, it satisfies weak WARP. 

#### Identification of a RSM
The choice reversals present in the dataset tell us about the model parameters for an RSM to be used to explain the data. 

Consider the data:
$x=c(xy);y=c(yz);z=c(xz);x=c(xyz)$

Between $x$ and $z$, there are two cases possible
1. $z\succ_1 x$
2. $\neg(x\succ_1 z)$ and $z\succ_2 x$

We know that case 1 is not possible as $x=c(xyz)$. If $z\succ_1 x$, $x$ cannot belong to $\text{max}(xyz;\succ_1)$ and therefore $x\ne c(xyz)$. Therefore it must be the case that $z\succ_2 x$. For $x=c(xyz)$ then it must be that $z\notin \text{max}(xyz;\succ_1)$. $$\implies y\succ_1 z$$Therefore, $y\succ_1z$ and $z\succ_2x$ are implications of taking the data as an RSM that cannot be changed. There is no unique identification between $x$ and $y$, both cases 
1. $x\succ_1 y$
2. $\neg(y\succ_1 x)$ and $x\succ_2 y$
will result in the same choice set. Therefore the data is explained by an RSM.





#### RSMs and [[Always chosen]]
If a choice function is an RSM, it satisfies always chosen or conversely - RSM violates WARP if and only if it has binary cycles. 

**Proof:** Consider any $S\in \chi$ and $x\in S$ such that $x=c(xy), \forall\ y\in S,y\ne x$
To establish AC, we need to show that $x=c(S)$. As $c$ is an RSM, we know that $$c(S)=\text{max}(\text{max}(S;\succ_1);\succ_2)$$As $x=c(xy)$, this implies that either 
1. $x\succ_1 y$
2. $\neg (y\succ_1 x)$ and $x\succ_2 y$

**Considering case 1,**
In this case, clearly $y\not\in \text{max}(S;\succ_1)$. This means that $$y\ne c(S)$$Further, $\not\exists\ y\in S$ such that $y\succ_1 x$. Therefore$$x\in\text{max}(S;\succ_1)$$With this model parameter, the choice function thus satisfies AC.

**Considering case 2,**
In this case, $y\in \text{max}(S;\succ_1)$. However, for such a $y$, since $x\succ_2 y$, $$y\not\in \text{max}(\text{max}(S;\succ_1);\succ_2)$$This implies that$$y\ne c(S)\ \forall\ y\in S,y\ne x$$However, $c(S)$ is non empty. Therefore $$x=c(S)$$This shows that $c$ satisfies always chosen if it is an RSM. 



