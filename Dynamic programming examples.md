Problems that are solved by backwards induction
### 1.
To fish or not. If you fist, 70% of the fist are caught and they grow back the next year. If you dont fish, the population doubles. The profit is 1 USD per ton, 25% interest rate, and there are only 3 opportunities (3 years) to fish. This problem can be represented as the binomial lattice:
![[Pasted image 20240911190743.png|500]]
At node 10, 9, 8, 7 there are no decisions left. We should thus look at the nodes 4,5,6. Looking at node 4. the two options are $F=28, nF=0$. Therefore a rational player at node 4 will always fish. 

Similarly for node 5 and 6, $F=14,nF=0$, $F=7, nF=0$. The player will always fish. Therefore, with backwards induction
![[Pasted image 20240911192740.png|400]]
We have to use discounting to decide at the next step. At node 2, the decision is given by $F=14+0.8\times 14, nF=0.8\times 28\implies F=25.2, nF=22.4$. We will choose to fish. At node 3, $F=7+0.8\times 7, nF = 0.8\times 14\implies F=12.6, nF = 11.2$. We will choose to fish. Inducting backwards,  ![[Pasted image 20240911193336.png]]
At node 1, $F=7+0.8\times 12.6, nF=0.8\times 25.2\implies F=17.08, nF = 20.16$
We choose to not fish in year 1, fish in year 2 and 3. Discounted payoff is 20.16 T of fish or 20.16 USD. 





