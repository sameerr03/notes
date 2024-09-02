A paradox that shows that DMs preferences are inconsistent with [[subjective expected utility problem (SEU)]].

There is an urn with 90 balls
- 30 blue
- 60 are either red or green

One ball is drawn at random from the urn

##### Choice problem 1
The DM has to choose between $f$ and $g$
$f: 1000$ if blue ball, nothing otherwise
$g: 1000$ if red ball, nothing otherwise

Most DMs will choose $f$ as there is a guaranteed probability with it. 
$f\succ g\implies \pi(B)u(1000)+(1-\pi(B))u(0)>\pi(R)u(1000)+(1-\pi(R))u(0)$
$\implies  \pi(B)[u(1000)-u(0)]+u(0)>\pi(R)[u(1000)-u(0)]+u(0)$
$\implies  \pi(B)>\pi(R)$

##### Choice problem 2
The DM has to choose between $f'$ and $g'$
$f':1000$ if ball blue or green, nothing otherwise
$g':1000$ if ball is red or green, nothing otherwise

Most DMs will choose $g'$ as there is a guaranteed probability with it (1-P(blue ball))

$g'\succ f'\implies \pi(R\cup G)u(1000)+(1-\pi(R\cup G))u(0)>\pi(B\cup G)u(1000)+(1-\pi(B\cup G))u(0)$
$\implies \pi(R\cup G)u(1000)+\pi(B)u(0)>\pi(B\cup G)u(1000)+\pi(R)u(0)$
$\implies \pi(R)u(1000)+\pi(G)u(1000)+\pi(B)u(0)>\pi(B)u(1000)+\pi(G)u(1000)+\pi(R)u(0)$
$\implies \pi(R)[u(1000)-u(0)]>\pi(B)[u(1000)-u(0)]$
$\implies \pi(R)>\pi(B)$
Which contradicts [[Ellsberg's urn#Choice problem 1|CP1]]. 