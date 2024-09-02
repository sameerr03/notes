DMs preferences over the [[states of nature|set of acts]] has a SEU representation if there exists 
- Unique probability over the [[states of nature]] ($\mu$ on $S$). 
- Utility function on the set of prizes.
such that the function $U:F\to\mathbb{R}$ given by$$U(f)=\sum_{s\in S}\mu(s)u(f(s))$$

For the [[decision matrix]],

|A/S|$S_1$|$S_2$|$S_3$|
|--|--|--|--|
|$f$|$x$|$y$|$z$|
|$g$|$x'$|$y'$|$z'$|

$fEg(S_1)=x\text{ if }S\in E, x'\text{ if }s\in E^C$

for the first parameter: $\pi(S_1), \pi(S_2), \pi(S_3) \in[0,1],\ \pi(S_1)+\pi(S_2)+\pi(S_3)=1$
for the second parameter: $u(x), u(y), u(z), u(x'), u(y'), u(z')$

$$\text{if }f\succ g\iff \pi(S_1)u(x)+\pi(S_2)u(y)+\pi(S_3)u(z)>\pi(S_1)u(x')+\pi(S_2)u(y')+\pi(S_3)u(z')$$

##### Identification
Another pair $(\tilde \mu,\tilde u)$ in an SEU representation of $\succsim$ iff $\tilde \mu=\mu$ and there exists constants $\beta>0,\beta'$ such that $\tilde u=\beta u +\beta'$.

##### Savage axioms
Savage conditions are met iff DMs preferences have a SEU representation. 
###### Rational preferences
Over the set of acts ($A$), preferences are complete and transitive
###### Sure thing principle
IF two acts give the same common outcome on some event, then replacing this common outcome with some other common outcome should not change the preference over the two acts. 
Imagine:
$f=a\text{ if }E;b\text{ if }E^c$
$g=a'\text{ if }E; b\text{ if }E^c$
$f'=a\text{ if }E;c\text{ if }E^c$
$g'=a'\text{ if }E; c\text{ if }E^c$
$$f\succ g\iff f'\succ g'$$
###### Eventwise monotonicity
If two acts $f$ and $g$ differ in only one event, where $f\to x$ and $g\to y$, then $f\succsim g \iff x\succsim y$.
Imagine:
$f=a\text{ if }E;o\text{ if }E^c$
$g=b\text{ if }E; o\text{ if }E^c$
$$f\succsim g\iff a\succsim b$$

###### Weak comparative probability 
If $x\succ y$ and $x'\succ y'$, then for any 2 events $A$ and $B$, DM prefers the bet that gives $x$ on $A$ and $y$ on $A^c$ to the bet that gives $x$ on $B$ and $y$ on $B^c$ iff she prefers the bet that gives $x'$ on $A$ and $y'$ on $A'^c$ to the bet that gives $x'$ on $B$ and $y'$ on $B^c$

This condition must imply that $\pi(A)>\pi(B)$

