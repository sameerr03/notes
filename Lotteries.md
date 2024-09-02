#flashcards/micro 

**Lotteries** :: Events that distribute prizes based on Probability.

There are two components to a lottery, prizes -> represented by the set $Z$ and the probability of each prize, $p$.

$X$ is the [[Choice sets|choice set]] that contains all the lotteries with the same prize set (Z). If there are n prizes, the [[random variables#Probablilty distribution|probability distribution function]] of the prizes is $$PDF=(p_1,p_2,...p_n)$$$$\sum_{n=1}^Np_n=1$$
### Convex combination of lotteries

if $f,g$ are lotteries, and p and q are the respective propabilities of the lotteries, where $f,g$ have the same prizes from the set $Z$, For $\lambda \in[0,1]$,$$\lambda f+(1-\lambda )g=(\lambda p_1+(1-\lambda)q_2+...\lambda p_n+(1-\lambda)q_n)$$

### Simple and compound lotteries

A simple lottery is a one step lottery that distributes prizes based on probability 
![[Pasted image 20221019183040.png]]

A compound lottery is one that takes more than one step. It is a lottery of lotteries, with each lower level lottery distributing prizes

![[tempFileForShare_20221019-183327.jpg|400]]

### Axioms of lottery

The simple lottery is indifferent to a compound lottery if the probabilities
of the prizes are the same at the end.

**Reduction of compound lotteries**
For $f,g\in \Delta (Z),\ \lambda\in[0,1]$, the compound lottery $\lambda f+(1-\lambda)g$, which gives $f$ with a probability $\lambda$ and $g$ with the probability $1-\lambda$, is an element in $\Delta(Z)$ given by:
$$(\lambda f+(1-\lambda)g)(z)=\lambda f(z)+(1-\lambda)g(z)$$Where $z$ is a particular outcome and $Z$ is the set of all outcomes, $\Delta(Z)$ is the set of probability measures corresponding to each outcome in $Z$.

**Continuity axiom**:: given 3 lotteries $f\succ g\succ h$, there exists a compound lottery with $\lambda$ such that $$\lambda f+(1-\lambda)h\sim g$$
**Substitution Axiom**:: If there is a preference in prizes, $z_1\succ z_2$ then with the two lotteries f and g, → (p and q are the probabilities of getting $z_1$ in f and g respectively). If $p_1>q_1$ then $f\succ g$.

This is proved by substituting a compound lottery.


