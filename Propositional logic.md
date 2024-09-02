A **proposition** is a declarative sentence that is either true or false. A proposition that is always true is a **tautology**. A proposition that is always false is a **contradiction**. 

### Propositional operations
##### Negation
If $p$ is a proposition, the negation of $p$ ($\neg p$) is the statement "it is not the case that $p$". Represented in a truth table format,

| $p$ | $\neg p$ |
| ---- | ---- |
| T | F |
| F | T |

##### Conjunction
$p\wedge q$ is the preposition "p and q". It is true only if both $p$ and $q$ are true.

| $p$ | $q$ | $p\wedge q$ |
| ---- | ---- | ---- |
| F | F | F |
| F | T | F |
| T | F | F |
| T | T | T |

##### Disjunction
$p\vee q$ is the preposition $p$ or $q$. It is true if either $p$ or $q$ or both are true

| $p$ | $q$ | $p\vee q$ |
| ---- | ---- | ---- |
| F | F | F |
| F | T | T |
| T | F | T |
| T | T | T |
Is also called inclusive or

#### XOR
Exclusive or excludes the case when both $p$ and $q$ are true.

| $p$ | $q$ | $p \newcommand*\xor{\oplus} q$ |
| ---- | ---- | ---- |
| F | F | F |
| F | T | T |
| T | F | T |
| T | T | F |

#### Implication
If $p$ then $q$. If $p$ is true and $p$ is true then $p\to q$ is true

| $p$ | $q$ | $p \to q$ |
| ---- | ---- | ---- |
| F | F | T |
| F | T | T |
| T | F | F |
| T | T | T |
$p\to q\equiv \neg p\vee q$

Given $p\to q$
Converse: $q\to p$
Contrapositive: $\neg q \to \neg p$
Inverse: $\neg p\to \neg q$


#### Bi-implication/Equivalence/XNOR
$p \iff q$ 
$p$ if and only if $q$ 

| $p$ | $q$ | $p\iff q$ |
| ---- | ---- | ---- |
| F | F | T |
| F | T | F |
| T | F | F |
| T | T | T |

compound propositions $p,q$ are logically equivalent if $p\iff q$ is a tautology. 
### Reductive form
Conjunction, disjunction and negation are functionally complete. This means that any operator can eb expressed in terms of $\wedge, \vee, \neg$.

### Operation Precedence
1. NOT ($\neg$)
2. XOR ($\newcommand*\xor{\oplus}$)
3. XNOR ()
4. AND ($\wedge$)
5. NAND ($|$)
6. OR ($\vee$)
7. NOR
8. IMPLICATION ($\to$)
9. BI-IMPLICATION ($\iff$)

### DeMorgan's laws
1. $\neg(p\vee q)\equiv \neg p\wedge \neg q$
2. $\neg(p\wedge q)\equiv \neg p \vee \neg q$

### Clauses and normal forms
A **clause** is a propositional formula from a finite collection of literals and logical connections. Clauses that only contain $\vee$ are **disjunctive clauses** and clauses that only contain $\wedge$ are **conjunctive clauses**. 

Disjunctive clauses together with $\wedge$ is a **conjunctive normal form (CNF)**, conjunctive clauses together with $\vee$ are in **disjunctive normal form (DNF)**.

In order to turn a compound proposition to normal form,
1. Use reductive forms to get rid of $\to, \iff, \newcommand*\xor{\oplus}$
2. DeMorgan's law to get rid of $\neg$(Clause)
3. Double negation to get rid of $\neg\neg$
4. Use distributive rules to convert to normal form. 

