### Pure stratergy Nash [[Equilibrium]] (PSNE)
$(s_1*,s_2*)$ will be a pure stratergy nash equilibrium if $$u_1(s_1*,s_2*)\ge u_1(s_1,s_2*)$$ such that $s_1 \in S_1$, and $$u_2(s_1*,s_2*)\ge u_2(s_1*,s_2)$$such that $s_2 \in S_2$

For an n-player game,
The stratergy profile $(s_i*,....,s_n*)$ in a strategic form game is a PSNE if for all $i\in N$$$u_i(s_i*,.....,s_n*)\ge u_i(s_i,.....,s_n*)$$ for all $s_i\in S_i$

Based on [[Best Response]], A stratergy profile $(s_i,.....s_n)$ is PSNE if for all $i\in N$$$s_i*\in B(s_{-i}*)$$
This means that every player is playing their best response to others

The equillibrium is found by fixing the strategy of one player and then finding the other  
according to the rules. Fixing that, finding the best course for the other player. Neither will deviate from this equilibrium unilaterally.

All Nash equilibriums are not [[dominant stratergy equilibrium(DSE)]]s but all [[dominant stratergy equilibrium(DSE)]]s are nash equilibriums

An example of a nash equillibrium is the [[battle of sexes]] game

### Mixed stratergy Nash Equillibrium 
Players play mixed stratergies, stratergies which use a probability distribution to mix two or more stratergies. These are as if the player is playing a pure stratergy according to a probability distribution ($\sigma_i$). This results in any finite game having a MSNE. PSNE + MSNE is almost always odd. An example of a game with mixed stratergies is a [[Zero sum game]].

A mixed stratergy can dominate a pure stratergy, resulting in the pure stratergy never being played, by [[Rationalizability]].

##### Rules for MSNE 
1. If a player plays $\sigma_1^*$ where $s_i'$ and $s_i''$ all recieve positive probability in equillibrium, $$EU_i(s_i',\sigma_{-i}*)=EU_i(s_i'',\sigma_{-i}*)$$
2. If $s_i'$ is player but not $s_i''$ in equillibrium, $$EU_i(s_i',\sigma_{-i}*)\ge EU_i(s_i'',\sigma_{-i}*)$$
### Sub game perfect Nash Equillibrium
A **sub-game** is a structure defined by a node $x$ and its successors. All nodes with successors can potentially be the start of their own subtrees. However, a sub game does not have any information sets outside of the subgame. 

A stratergy profile is a sub game perfect nash equilibria if it specifies a nash equilibrium in every subgame of the original game. This results in Nash equilibria that are not a part of the sub-game perfect nash equilibria. 

Sub game perfect Nash Equilibria use sequential [[Rationalizability|rationality]]. This means that the optimal stratergy of any player should maximise their payoffs conditional on [[extensive form games|information sets]]. This equilibrium can be obtained using **backwards induction**. This is where we start at pen terminal nodes (nodes where all actions result in termination), and selecting the optimal stratergy and moving backwards, reducing the game as we go along. SPNE is a stratergy profile, and therefore must have one stratergy for each node. The path taken is the SPNE outcome.

### [[Bayesian Form Game|Bayesian]] Nash Equilibirium
No unilateral profitable deviation from equilibirum across all types of the player. Stratergy profile $s^*=(s_1^*,...,s_n^*)$ is a BNE if and only if for all $i$ and type $t_i$, $s_i^*$ is the [[Best Response]] to $s_{-i}$.



