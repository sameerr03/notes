In mathematical induction, we first prove the base case, $P(n_0)$ is true. We then generalize it and assume that $P(k)$ is true. We use $P(k)$ to prove that $P(k+1)$, $k\ge n_0$.

#### First principle of Mathematical Induction
Let $S(n)$ be a statement about integers for $n\in \mathbb Z$ and suppose $S(n_0)$ is true for some integer $n_0$. If then for all integers $k$ ($k\ge n_0$), $S(k)$ implies that $S(k+1)$ is true, then $S(n)$ is true for all integers $n$ greater than $n_0$

###### Example
The claim that 9 divides $7\times 10^{n+1}+3\times 10^n+8$, $n\ge 0$, $n\in \mathbb Z$

We use 0 as the base case. $P(0)=70+3+8=81$ which is divisible by 9. Generalizing using $k$ and assuming that $k$th case is true, $$7\times 10^{k+1}+3\times10^{k}+8=9m$$where $m$ is a natural number. Multiplying by 10 on both sides, $$10(7\times 10^{k+1}+3\times10^{k}+8)=90m$$$$70^{k+1+1}+3\times10^{k+1}+80=90m$$$$(7\times 10^{k+1+1}+3\times 10^{k+1}+8)+72=90m$$$$P(k+1)=9(10m-8)$$Which is divisibly by 9. Therefore as kth and k+1th case is true, we say that the claim is true by mathematical induction.

#### Second Principle of Mathematical Induction
Let $S(n)$ be a statement about integers for $n\in \mathbb Z$ and suppose $S(n_0)$ is true for some integer $n_0$. Then if $S(n_0), S(n_0+1), \dots, S(k)$ imply that $S(k+1)$ ($k\ge n_0$), then the statement $S(n)$ is true for all integers $n$ greater than $n_0$.  

###### Example
Tribonacci: 1,1,13,5,9,17,...
Claim: $a_n<3^n$
Assume: $P(k-2), P(k-1), P(k)$
$$a_{k-2}<3^{k-2}$$$$a_{k-1}<3^{k-1}$$$$a_{k}<3^k$$$$a_{k-2}+a_{k-1}+a_{k}<3^{k-1}+3^{k-1}+3^k$$$$a_{k+1}<3^{k-1}+3^{k-1}+3^k<3^k+3^k+3^k$$$$a_{k+1}<3\cdot 3^k$$$$a_{k+1}<3^{k+1}$$
therefore the claim is proved by induction


