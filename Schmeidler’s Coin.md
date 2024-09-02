A bet on a coinflip
$f:1000$ if H, 0 if T
$g:1000$ if T, 0 if H

There are two coins, one of the experimenter and one of the DM. The DM knows that their coin has a relative frequency of heads of 50%. The DM knows nothing about the experimenter's coin. 

#### resolution using [[non additive probability]]
The sample space of outcomes is given by $$S=\{HH,HT,TH,TT\}$$Where the first coin is the DMs coin and the second coin is the Experimenter's coin. Suppose there are two events $A$ and $B$. 
$A:$ Event that $H$ shows in the DMs coin
$B:$ Event that $H$ shows in the Experimenter's coin
$v(s)=\frac 14\forall s\in S$
$A=\{HH,HT\}$
$B=\{HH,TH\}$

The DM is confident about their coin, therefore they assign the subjective probability 
$\pi(A)=\frac 12$
The DM is not sure about the experimenter's coin, therefore the non-additive probability is assigned
$\pi(B)=\pi(B^c)=\frac 13$

#### Resolution using [[Maximin strategy]]
Maximin [[vNm Expected utility]] maximizes the minimum expected utility. In this example the DMs coin:
$\pi(H)=\frac 12=\pi(T)$

However, for the experimenter's coin, the non-unique probability $\alpha$ and $1-\alpha$ are set to $H$ and $T$ where $$\alpha \in[\frac 13, \frac23]$$From this, the probabilities of each outcome are
$P_\alpha(HH)=(\frac 12)(\alpha); P_\alpha(TH)=\frac 12(\alpha)$
$P_\alpha(HT)=\frac 12(1-\alpha); P_\alpha(TT)=\frac 12(1-\alpha)$

Therefore $P_\alpha(A)=\frac 12\alpha+\frac 12(1-\alpha)=\frac 12$
$P_\alpha(B)=\frac 12\alpha+\frac 12(\alpha)=\alpha$
$P_\alpha(B^c)=1-P_\alpha(B)=1-\alpha$

Finding the minimum expected utility (worst case scenario)
$\text{min}(P_\alpha(B))=\text{min}(\alpha)=\frac 13$
$\text{min}(P_\alpha(B^c))=\text{min}(1-\alpha)=\frac 13\ \ \ \ [\alpha=\frac 23]$
