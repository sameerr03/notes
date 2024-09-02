A way of capturing a decision maker's behavior in any given environment.

A rational economic agent is one that exercises [[Utility]] maximization for their decisions. A utility function cannot be observed in real life and therefore, we have to use [[revealed preferences]] instead. 

These revealed preferences are built on an "internal consistency" of preferences for the decision maker. Due to this, their choices can be represented as maximizing behavior with respect to their preferences. 

The dataset for this kind of model is given by the DMs choices as their preferences are not observable. Let us assume a set containing all possible alternatives (Set of alternatives)
$$X:\{\text{finite set of all alternatives}\}$$Then, from this set we can obtain the set of all possible non-empty subsets of $X$. This set essentially reflects all the possible consumption bundles present from the total number of alternatives (Set of menus). $$\chi:\{\text{all possible non-empty subsets of X}\}$$For instance, if $X:\{a,b,c\}$, then $\chi:\{\{a\},\{b\},\{c\},\{a,b\},\{a,c\},\{b,c\},\{a,b,c\}\}$
If $A$ is a particular element from $\chi$, a choice function can be set up that gives us the DM's choices for each possible combination of alternatives. 

$c(\{a\})$ -> $a$
$c(\{a,b\})$ -> $a$
and so on.

This can be thought of as an experiment used to collect data. The preferences need not be transitive. 

Given the choice data we collect, we can conclude that the DM chooses as if they have preferences over the set of alternatives, and in any menu their choices are the best alternative according to these preferences if the choice data satisfies [[WARP]] or [[Independence of irrelevant alternatives]].

If a choice function $c:\chi\to X$ satisfies WARP, there exists a unique (strict) preference ranking on $X$ such that in any menu $A$, the chosen alternative $c(A)$ is the best alternative in $A$ according to this preference ranking. 

This preference ranking can be defined by:
For any $x,y\in X, x\ne y$ $$x\succ y \text{ if }x=c(\{x,y\})$$
#### Proof of preferences under WARP
To prove the above defined preferences behave as such under WARP, we need to prove that it is a preference ranking first (needs to satisfy completeness and transitivity), and the choice function is a representation of the maximizing of these preferences.

##### Completeness
Consider $x,y\ x\ne y$. Either $c(\{x,y\})=x$ or $c(\{x,y\})=y$ since we have data on all such menus for $\{x,y\}$. Hence either $x\succ y\text{ or }y\succ x$ based on the defined preferences. As all the outcomes are given an output by our definition of preferences, the preferences are complete.

##### Transitivity
Consider $x,y,z$. suppose in terms of the preference relation,$$x\succ y \text{ and } y\succ z$$For transitivity of the preferences to hold, $x\succ z$. From the above preference relations,$$x\succ y \to c(\{x,y\})$$$$y\succ z\to c(\{y,z\})$$We need to show that $x=c(\{x,z\})$
Consider the menu $\{x,y,z\}$. Since $c(\{y,z\})=y$ and not $z$, WARP implies that $c(\{x,y,z\})\ne z$.

Since $c(\{x,y\})=x$, WARP implies that $c(\{x,y,z\})\ne y$. Therefore,$$c(\{x,y,z\})=x$$In $\{x,z\}$, since $c(\{x,y,z\})=x$, WARP implies that $c(\{x,z\})\ne z$. Therefore by preferences,$$x\succ z$$hence, the preferences defined are transitive

##### Maximization
In any menu $A$. Let us call $m(A)$ the best alternative in menu $A$ according to the defined preferences. Suppose in $A$, $x=m(A)$
$$x\succ y\ \text{  for all  }\ y\in A,y\ne x$$By the definition of preferences, $$x=c(\{x,y\})$$Consider any $y\in A,y \ne x$. WARP implies that in no menu where $x$ and $y$ are present is $y$ chosen over $A$. $$y\ne c(A)$$However,$$c(A)\ne \varnothing$$Therefore,$$c(A)=x=m(A)$$
##### Uniqueness
Suppose the revealed preferences defined in the theorem where not unique. A different preference ranking $\succ'$, $\succ\ne \succ'$ where there is at least one alternative $x,y$ such that $$x\succ y\ \text{ and }\ y\succ' x$$$$x\succ y\implies x=(\{x,y\})$$$$y\succ' x\implies y=c(\{x,y\})$$This is a **contradiction**. Therefore there cannot be two different preference rankings cannot describe the same situation. => the defined preferences are unique. 


#### WARP and lack of data
The minimum amount of data needed for a preference relation to be created in a dataset satisfying WARP is all the choices on binary menus and menus of size three. 

Suppose $X=\{x,y,z\}$
There are only three datapoints $c=(\{x,y\})=x$, $c=(\{y,z\})=y$, $c=(\{x,z\})=z$
This satisfies WARP as there is no additional datapoint where $x,y,z$ are all present in the same menu, which is required in order to disprove WARP. The preference ranking does not hold as it violates transitivity.

Suppose $X=\{x,y,z\}$
There are only three datapoints $c=(\{x,y,z\})=z$, $c=(\{y,z\})=z$, $c=(\{x,z\})=z$
This satisfies WARP as $x,y$ are never chosen in the presence of $z$. However, the preferences do not hold as it is not unique -  there are two preference relations that explain the datapoints$$z\succ x\succ y\ ;\ z\succ'y\succ'x$$
#### Preferences and [[Utility]]
The information contained in a preference ranking can equivalently be represented through an ordinal [[Utility function]].

A choice set and function that satisfies WARP can be used to create both an ordinal utility function so that the DMs behavior can be represented as utility maximizing behavior. This is equivalent to maximization of a complete, transitive preference ranking. 





##### Additional?
$$x=c(xy)\iff x\succ y$$This is only true for the rational choice model, WARP =IIA holds only for RCMs