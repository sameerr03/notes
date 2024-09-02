# Probability
The possibility of a particular event happening is its probability 

**sample space**: set of all possible outcomes of an experiment (S)
Any subset of the sample space is an **Event**

## De Morgan's laws
1. $(E\cup F)^C=E^C \cap F^C$
2. $(E\cap F)^C=E^C \cup F^C$

## Axioms of probability 
1. $0\le P(E) \le 1$
2. $P(S)=1$
3. For mutually exclusive events ($E \cap F = \emptyset$),$$P(E\cup F)=P(E)+P(F)$$

### Implications
1. $P(E^C)=1-P(E)$
2. $E\subset F$ then $P(E)<P(F)$
3. $P(E \cup F)=P(E) + P(F) -P(E\cap F)$. This is the inclusion exclusion theorem. Alternate parts are added and subtracted. All combinations of set intersections are considered.

## Odds
Probability of an event occuring relative to it not occuring.

$$\frac{P(A)}{P(A^C)}=\frac{P(A)}{1-P(A)}$$

## Conditional probability 
Probability of an event happening given that another event has already happpened. Probability of E given that F has occurred 
$$P(E|F)=\frac{P(E\cap F)}{P(F)}$$

## Independant events
2 events are independant if the knowledge that one event has happened does not affect the other.

If $P(E)=P(E|F)$ then the events are independant

=> $P(E\cap F)=P(E)\cdot P(F)$