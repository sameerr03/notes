Linear multivariate optimization. Consider the example:

Manufacturing company makes 2 products $A$,$B$. Profit per unit of $A$ = 5000, $B=6000$. $A$ requires 3 hours of machine time/unit, B requires 4 hours of machine time per unit. The total time available is 240 hours per week. The demand of $A$ is 30 units per week, demand of $B$ is 20 u per week. This problem can thus be represented as $$\max_{x_A,x_B}5000x_A+6000x_B\ \text{s.t.}\ 3x_A+4x_B=240, x_A\ge30, x_B\ge 20$$
Graphically, we can represent the constraint as 
![[Pasted image 20240909200627.png|400]]
The inner triangle is the feasible set of solutions. We can use isoquants of the profit function to determine where the optimal solution will be within the constraint. In such optimization problems, the optimal solution is on one of the corner points. Looking at the 2 corner points, we can see that 53.33 of $A$ and 20 of $B$ is the optimal production amount. 