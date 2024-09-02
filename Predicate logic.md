A **domain** is a set of all elements to which a function applies. A variable can take any of the values in its domain. 

A **predicate** is an expression of one or more variables defined on some specific domain. A predicate with variables can be made a proposition by:
- Assigning a value to the variable
- Quantifying the variable

Suppose the predicate $P(x)$ denote that $x>3$. In this example
- $x$ is the variable
- $P$ is the propositional function
- $P(x)$, once a value has been assigned to $x$ from its domain, is a proposition and can take a truth value 

$P(4)=T$, $P(2)=F$

### Difference between [[Propositional logic|proposition]] and predicate
$3+2=5$ is a proposition, as it can be true or false. 

$X+2=5$ is not a proposition, but a predicate as it contains a variable. Only when this variable takes a particular value can the statement be called a proposition. 

Considering a case with a propositional function, $P(x),x\in\{1,2,3\}$ is a predicate whereas $P(1)$ is a proposition. 

### Quantifying variables
Another method of converting a predicate into a proposition.
##### Universal quantification
 If $P(x)$ is a predicate on some domain, then
$\forall x\ P(x)$ is true if $P(x)$ is true for all values of $x$ in the domain
$\forall x\ P(x)$ is false if there is a value for $x$ for which $P(x)$ is false

##### Existential quantification
If $P(x)$ is a predicate on some domain, then
$\exists x\ P(x)$ is true if $P(x)$ is true for any $x$
$\exists x\ P(x)$ is false if for every $x$, $P(x)$ is false

Both of these methods of quantification can be negated. $\neg \forall x P(x)$, $\neg \exists x P(x)$

#### DeMorgan's Laws
$$\neg\forall x D(x)=\exists x\neg D(x)$$$$\neg \exists xA(x)=\forall x\neg A(x)$$

#### Precedence
Both $\forall$ and $\exists$ have higher precedence than all logical operators from propositional calculus. For example, the expression$$\forall xP(x)\vee Q(x)=(\forall x P(x))\vee Q(x)$$

#### free and bound variables
A variable $x$ is bound if a quantifier is used on it. The variable is free if it is not bound by a quantifier or set to a value. Some examples of this are illustrated
![[Pasted image 20240129222002.png]]

Bound variables may be renamed within the scope without changing the semantics of the expression $$\forall xP(x)\equiv \forall y P(y)$$$$\exists xP(x)\equiv \forall y P(y)$$
#### Nested quantifiers
The usage of one quantifier within another. 
$\forall x \forall y P(x,y)=T$ if $P(x,y)=T$ for all $x,y$ (shortform: $\forall x,y P(x,y)$)
$\forall x\exists y P(x,y)=T$ if for any $x$ there exists $y$ such that $P(x,y)=T$
$\exists x \forall yP(x,y)=T$ if there exists $x$ such that $P(x,y)=T$ for all $y$
$\exists x\exists y P(x,y)=T$ is there exists $x$ and there exists $y$ such that $P(x,y)=T$ (shortform: $\exists x,y P(x,y)$)

important to note that **quantifiers cannot be applied unless the domain has been identified**.


**nested quantifiers in different orders can result in different truth values**
$\forall x\exists y(y>x)=T$
$\exists y\forall x(y>x)=F$

