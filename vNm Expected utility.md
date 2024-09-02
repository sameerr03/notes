There exists a [[Utility function]] $u:X\to \mathbb{R}$ (often referred to as the Bernoulli utility function) that describes preferences over [[Lotteries]]. Then, the function $V:\Delta(X)\to\mathbb{R}$ is given by:$$V(p)=\sum_{x\in X}p(x)u(x)$$where $p$ is a lottery and **$p(x)$ is the probability of getting $x$ from $p$.** 
From the two axioms, $p\succsim q$ if and only if $$V(p)\ge V(q)$$
Where p is the probability (non-[[subjective expected utility problem (SEU)|subjective]]) of the prize from lottery f and q from g.

The utility function that maps prizes to a value is called a **vNM function**

#### Characterization
- The first is standard: preferences are complete and transitive 
- The second is in the nature of a technical continuity requirement 
- The third, referred to as independence, captures the key behavioral restriction of the model

###### Separability
For all the lotteries $p,q,r$ and $\alpha\in[0,1]$
$$V(p)\ge V(q)\iff V(\alpha p+(1-\alpha)r)\ge V(\alpha q+(1-\alpha)r)$$

###### Independence axiom
For any $p,q,r\in\Delta(X)$, and $a\alpha\in[0,1]$$$p\succsim q\iff \alpha p+(1-\alpha)r\succsim \alpha q+(1-\alpha)r$$which is the same as separability but from the perspective of preferences and not vNm.

###### Consequentialism
Behavior should be entirely explicable by its consequences. In particular, changes in the structure of a decision problem should have no bearing on choices unless they change the feasible set of lotteries.

If choice behavior is consequentialist and dynamically consistent (preferences stay consistent with time) then it satisfies the independence axiom. 
**Illustration:**
square are choice nodes, circle are chance nodes. 
![[Pasted image 20231121205432.png|500]]
Consequentialism implies that in CP1 and in CP2, choices should not change
![[Pasted image 20231121205501.png|300]]
With dynamic consistency, behavior in CP2 and CP3 must be same as when the choices are made does not impact the outcome.
![[Pasted image 20231121205547.png|400]]
DM is made to choose between up and down strategy in CP4 over the same lotteries. Consequentialism implies that behavior in CP3 and CP4 have to be the same.
![[Pasted image 20231121205609.png|400]]
CP5 is a reduction of CP4. Reduction of compound lotteries implies that behavior between CP4 and CP5 must be the same

If CP1  1 for sure is chosen and CP5 bottom lottery is chosen ([[Allais paradox]]). If independence is violated, at some point there would be a flip in choice. If consequentialism or dynamic consistency are violated, independence is as well. 

