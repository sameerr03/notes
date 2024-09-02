#flashcards/stats

# Bayes' Theorem
Theorem that determines conditional probablility given multiple situations
Formula::$$P(F_j|E)=\frac{P(E|F_j)\cdot P(F_j)}{\sum_{i=1}^{j}P(E|F_i)\cdot P(F_i)}$$
<!--SR:!2022-10-12,1,210-->

## Derivation
![[Pasted image 20220921192629.png|300]]
$E=(E\cap F^C)\cup(E\cap F)$

$P(E)=P(E\cap F^C)+P(E\cap F)$ as the [[Probability#Axioms of probability|probabilities]] are mutually exclusive

$P(E)=P(E|F^C)P(F^C)+P(E|F)P(F)$ by the conditional probability formula