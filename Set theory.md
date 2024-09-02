A **set** is an abstract collection of abstract objects

Sets can be defined in 3 forms:
##### Roster form
$$A = \{1,3,5,7\}$$$$\emptyset = \{\}$$
This method of defining sets requires all numbers to be put in between the curly braces, denoting the set's contents

#### Set builder form
In this method, we use more generalized notations to represent the contents of a set$$A = \{x|x\in \mathbb N, 2\not{|}\ x, 1\le x\le7\}$$
#### Semantic form
Describes the set in words. A is the set of the first 4 odd numbers

### Sets of collections of numbers
- Set of natural numbers$$\mathbb N = \{1,2,3,\dots\}$$
- Set of integers$$\mathbb Z=\{\dots-3,-2,-1,0,1,2,3,\dots\}$$
- Set of real numbers ($\mathbb R$)
- Set of rational numbers $$\mathbb Q = \{a/b|a,b\in\mathbb Z, b\ne 0, \text{gcd}(a,b)=1\}$$where gcd is the greatest common divisor
- Set of complex numbers$$\mathbb C=\{a+bi|a,b\in\mathbb R, i=\sqrt{-1}\}$$

### Set operations
![[Pasted image 20240827210916.png]]

$A\sqcup B$ is the disjoint union. It is basically $A\cup B$ but $A$ and $B$ are such that $A\cap B=\emptyset$.   

### Subset
$A$ is a subset of $B$ ($A\subseteq B$) if $$x\in A\implies x\in B$$or $$A\cup B = B\iff A\cap B =A$$
### Power Set
The set of all the subsets in a set is the power set of that set. It includes the null set. $$P(A) = \{B|B\subseteq A\}$$
$$P(\{1,2\}) = \{\emptyset, \{1\},\{2\}, \{1,2\}\}$$
### Cartesian product of sets
For the sets $A$ and $B$, the cartesian product is given by $$A\times B =\{(a,b)|a\in A, b\in B\}$$
#### Equivalence class
A subset of a set that contains all elements that are equal to each other. 

#### Cardinality and infinite sets
Two sets are equivalent if they have the same cardinality - the number of elements in the set. 

If a set $A\subset \mathbb N$ has a bijective relation with the set $X$ and the cardinality of $|X|=n$ where $n$ is a finite number, then $A$ is a finite set.
