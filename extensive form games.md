Games that take into account the order of moves made by the players. These games can be represented by a game tree. Game trees contain 
- Root nodes
- Decision nodes - tree splits here
- Terminal  nodes - Payoffs are here
Each node is associated with a player.

Nodes can be a part of an **information set**, which is a set in which the active player is not sure which node they are at. (The actions available to the at each of the node within the set must be the same). A game in which all IS for all players are **singletons**, the game is a **perfect information game**. An imperfect information game has at least one IS.

Extensive form prisioners dillema
![[SmartSelect_20230223_013724_Samsung Notes.jpg|400]]

In this game, the [[Equilibrium]] is $(P_1,P_2):(C,C)$. 

In this game, [[Nash equilibrium]] fails to produce an accurate equillibrium as it does not account for a time dimension. The outcomes for these games are found through **backwards induction**.

### Converting a extensive into simultaneous
However, the game can be made simultaneous game by creating **information sets** 
Converting the prisioners dillemma into a table,
![[tempFileForShare_20230223-014312.jpg|400]]
The red is from node 3 and the green from 2, as the player needs a choice for both as he does not know which node he is at.
Fixing $P_1$ as C,
$B_2(C)=C,C$ or $C,NC$
Fixing $P_1$ as NC,
$B_2(NC)=C,C$ or $NC,C$

Fixing $P_2$ as C,C
$B_1(C,C)=C$

Therefore the nash equilibrium is at $(P_1,P_2):(C,C,C)$
![[SmartSelect_20230223_014851_Samsung Notes.jpg]]