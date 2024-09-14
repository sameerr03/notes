A relation is a collection of ordered pairs, where each pair contains one object from each [[Set theory|set]]

For the [[Set theory#Cartesian product of sets|cartesian product]] of the two sets $A$ and $B$, the relation $R$ exists such that $$R\subseteq A\times B$$We write $aRb$ if $a\in A$ and $b \in B$ are related. 
#### Types of relations
- Reflexive: $$aRa\ \forall\ a\in A $$This evaluates if this relation holds with a set to itself. For the relation "is parallel to", A line $l$ is parallel to itself, and thus the relation is reflexive
- Symmetric:$$aRb\implies bRa$$if the line $l$ is parallel to $m$, then $m$ is parallel to $l$. This is a symmetric relation
- Transitive:$$aRb, bRc \implies aRc$$If $l$ is parallel to $m$ and $m$ is parallel to $n$, then $l$ is parallel to $n$. This is a transitive relation
- Anti-symmetric:$$aRb, bRa \implies a=b$$If $l$ is parallel to $m$ and $m$ is parallel to $l$ this does not mean that $l=m$. Therefore this is not an anti-symmetric relation
- Equivalence: A relation that is symmetric, transitive and reflexive. "is parallel to" is such a relation. $a\sim b$ is used instead of $aRb$ to represent a equivalence relation. 
- Order: A relation that is transitive, reflexive and anti symmetric. a subset is such a relation

#### Equivalence Class
Let $\sim$ be an equivalence relation on the set $A$. For every $a\in A$, we define the equivalence class of $a$, denoted by $[a]$ as the set of all elements of $A$ related to $a$. $$[a]=\{x\in A|a\sim x\}$$
#### Partition
A partition of a set $A$  a collection of disjoint subsets of $A$, such that when combined together, their union is $A$. This means that each of these subsets have no overlap with the other subsets and join perfectly to make $A$$$A=\cup_{i}A_i\ \ \ A_i\cap A_j=\emptyset\ \text{if}\ i\ne j$$
Given an equivalence relation on a set, it partitions the set with the disjoint subsets being the equivalence classes within the set. 

**Proof:** Given an equivalence relation $\sim$ on a set $X$, we have to show that the equivalence classes partition $X$. We know that by reflexivity, every $x\in X$ belongs to $[x]$. Therefore teh union of equivalence classes is just $X$. 

However, to complete the argument we need to show that either equivalence classes are disjoint or equal. Let $x,y\in X$ such that $[x]\cap [y]\ne \emptyset$. By the definition of an equivalence class, this must mean that we have some $z\in X$ such that $x\sim z, y\sim z$. Transitivity and symmetry (equivalence relation) give us that $x\sim y$. If there was an element $u\in [y]$, then $y\sim u$, but $x\sim y\implies x\sim u\implies u\in [x]$. This tells us that $[y]\subseteq [x]$. A similar argument tells us that $[x]\subseteq [y]$, which means that $[x]=[y]$. 