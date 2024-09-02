There is an urn with 101 balls, 
- 50 are labelled either 1 or 2
- 51 are labelled either 3 or 4
A ball is chosen from the urn at random. There are two choice lotteries
$f_1=$ 8000 if either 1,2; 4000 if either 3,4
$f_2=$ 8000 if either 1,3; 4000 if either 2,4

As $f_2$ combines the ball groups, there is less certainty in the outcome. Therefore we can imagine that a DM chooses $f_1\succ f_2$

Consider two more choice lotteries:
$f_3=$ 12000 for 1; 8000 for 2; 4000 for 3; 0 for 4
$f_4=$ 12000 for 1; 4000 for 2; 8000 for 3; 0 for 4

![[Pasted image 20231202212737.png]]

According to a bayesian, based on the number of outcomes $E_1=\frac{25}{101}; E_2=\frac{25}{101}; E_3=\frac{25.5}{101}; E_4=\frac{25.5}{101}$
Therefore it makes sense that $f_4\succ f_3$. However, $f_1\succ f_2$ and $f_4\succ f_3$ violate the [[subjective expected utility problem (SEU)#Savage axioms#Sure thing principle|sure thing principle]] as 8000 has been replaced by 12000 for $E_1$ and 4000 by 0 for $E_4$. $$f_1\succ f_2\implies P(E_2)>P(E_3)$$$$f_4\succ f_3\implies P(E_3)>P(E_2)$$Therefore subjected expected utility is violated

##### Evaluation with CEU
With the same preferences, evaluating CEU,
$$\text{CEU}(f_1)=u(4000)+[u(8000)-u(4000)]\phi(E_1\cup E_2)$$$$\text{CEU}(f_2)=u(4000)+[u(8000)-u(4000)]\phi(E_1\cup E_3)$$$$f_1\succ f_2 \implies \text{CEU}(f_1)>\text{CEU}(f_2)\implies \phi(E_1\cup E_2)>\phi(E_1\cup E_3)$$$$\text{CEU}(f_3)=u(0)+u(4000)\phi(E_1\cup E_2\cup E_3)+[u(8000)-u(4000)]\phi(E_1\cup E_2)+[u(12000)-u(8000)]\phi(E_1)$$$$\text{CEU}(f_4)=u(0)+u(4000)\phi(E_1\cup E_2\cup E_3)+[u(8000)-u(4000)]\phi(E_1\cup E_3)+[u(12000)-u(8000)]\phi(E_1)$$$$f_4\succ f_3 \implies \text{CEU}(f_4)>\text{CEU}(f_3)\implies \phi(E_1\cup E_3)>\phi(E_1\cup E_2)$$Thus a contradiction arises. This shows that [[Ambiguity]] is fundamental to event inseparability.
