A vector is an algebraic entity that has the ability to be added and scaled. In real or complex vector spaces they have properties like direction and length. Finite dimensional vectors can be visualized as arrays or row matrices. 

#### Vector Space
A vector space consists of the following things
1. A [[Field]] of scalers $\mathbb F$
2. A set $V$ of objects, called vectors
3. Vector addition associates with each pair of vectors $v, w\in V$ with a vector $v+w\in V$. This is the sum of the vectors $v$ and $w$ in such a way that
	1. Closure of addition: $v+w\in V\forall v,w \in V$
	2. Commutativity of addition: $v+w=w+v\forall v,w\in V$
	3. Associativity of addition: $u+(v+w)=(u+v)+w\in u,v,w\in V$
	4. Existence of additive identity: $\exists\ 0\in V$ called the 0 vector such that $v+0=0+v, \forall v\in V$
	5. Existence of additive inverse: $\forall v \in V$ there exists another vector $-v\in V$ such that $v+(-v)=0=(-v)+v$
4. Scalar multiplication associates each scalar $\lambda\in\mathbb F$ and a vector $v\in V$ to the vector $\lambda v \in V$, called the product of $\lambda$ and $v$ in such a way that 
	1. Closure of scalar multiplication: $\lambda v\in V,\ \forall \lambda\in \mathbb F,\ v\in V$
	2. Multiplication by 1: $1v=v\ \forall v\in V$
	3. Associativity of scalar multiplication: $(\lambda_1\lambda_2)v=\lambda_1(\lambda_2v),\ \forall \lambda_1,\lambda_2\in\mathbb F, v\in V$
	4. Distribution over vector addition: $\lambda(v_1+v_2)=\lambda v_1+\lambda v_2,\ \forall \lambda\in \mathbb F,\ v_1,v_2\in V$
	5. Distribution over scalar addition: $(\lambda_1+\lambda_2)v=\lambda_1v+\lambda_2v,\ \forall\lambda_1,\lambda_2\in \mathbb F, v\in V$

A vector space with addition, $(V,+)$ is an abelian [[Groups|group]]. It is important to note that an empty set cannot be a vector space as it will not have the additive identity. For the vector space $V$, we can specify the field of scalers for this vector space, $\mathbb F$, through the notation $V/\mathbb F$. 

##### Vector operations

Consider the two vectors $u$ and $v$, where $$u=(u_1, u_2, \dots, u_n),\ v=(v_1,v_2,\dots, v_n)$$$\in \mathbb F^n$ and $\lambda\in \mathbb F$, the sum of $v$ and $u$ is defined as$$u+v=(u_1+v_1, u_2+v_2,\dots, u_n+v_n)$$and scalar multiplication is defined as $$\lambda v=\lambda(v_1,v_2,\dots,v_n)=(\lambda v_1, \lambda v_2, \dots, \lambda v_n)$$ 
##### Linear combination and linear dependence
A vector $w$ belonging to the vector space $V$ is a linear combination of the vectors $v_1, v_2, \dots, v_n$ in $V$ if there are scalars $\lambda_1, \lambda_2,\dots, \lambda_n\in \mathbb F$ such that $w$ can be expressed as $$w=\lambda_!v_1+\lambda_2v_2+\dots+\lambda_nv_n=\sum_{i=1}^n\lambda_iv_i$$A set of vectors $\{v_1,v_2,\dots, v_n\}\subset V$ is said to be **linearly dependent** if there are scalars $\lambda_1, \lambda_2, \dots, \lambda_n$ not all zero, such that $$0=\lambda_1v_1+\lambda_2v_2+\dots+\lambda_nv_n=\sum_{i=1}^n\lambda_iv_i$$The set of vectors is said to be **linearly independent** if for some scalars $\lambda_1, \lambda_2, \dots, \lambda_n$ $$\sum_{i=1}^n\lambda_iv_i=0$$then all the $\lambda_i=0$.
 
#### Subspace of a vector space
Consider $V/\mathbb F$. A **subspace** of $V$ is defined as a subset $W$ of $V$ that is also a vector space over $\mathbb F$, and has the same operations that $V$ has (addition and scalar multiplication). 

(1)To verify if $W$ is a subspace of $V$, we can say that it is a subspace if and only if for each pair of vectors $v,w\in W$ and each scalar $\lambda\in \mathbb F$, the vector $v+\lambda w$ is again in $W$.

**Proof:** Suppose $W$ is a non-empty subset of $V$ such that $v+\lambda w\in W\ \forall v,w\in W, \forall \lambda\in \mathbb F$. Given that there exists $u\in W$, $u+(-1)u=0\in W$. Also, for any vector $v\in W$ and scalar $\lambda$, the vector $\lambda v=0+\lambda v\in W$. All the other conditions for a vector space are inherited from $V$. Therefore $W$ is a subspace of $V$.  

(2)Let $V/\mathbb F$. The intersection of any collection of subspaces of $V$ is a subspace of $V$

**Proof:** Let $W$ represent the intersection of a collection of subspaces $\{W_a\}$ of the vector space $V$. Since they are subspaces, all the vectors contain the zero vector, and thus $W$ contains the zero vector meaning that it is not empty. $v, w\in W$. By definition, $v,w\in W_a$ for every $W_a$. Also, since we are talking about vector subspaces, $v+\lambda w\in W_a$which means that $v+\lambda w\in W$. Thus (from the previous theorem) $W$ is a subspace of $V$
#### Span of a vector
Consider a set of vectors $S$ in the vector space $V$. The subspace spanned by $S$, $W$ is the intersection of all subspaces of $V$ that contain $S$. If $S$ is a finite set of vectors, $S=\{v_1,v_2,\dots, v_n\}$, we will refer to $W$ as the subspace spanned by the vectors $v_1,v_2,\dots, v_n$. 

(3)The subspace spanned by a non-empty subset of $S$ of a vector space $V$ is the set of all linear combinations of vectors in $S$. 
**Proof:** $W$ is the subspace generated by $S$. Every linear combination $\sum_i\lambda_iv_i$ of vectors $v_1, v_2, \dots, v_n$ in $S$ is in $W$ by theorem (1). $W$ encompasses the collection $L$ of all linear combinations of vectors in $S$, $L$ includes $S$. Assuming $w_1, w_2$ are a part of $L$, then $w_1$ is a linear combination $$w_1=\lambda_1v_1+\lambda_2v_2+\dots+\lambda_kv_k$$and similarly $$w_2=\mu_1u_1+\mu_2u_2+\dots+\mu_mu_m$$For any scalar $c$, $$w_1+cw_2=\sum_i\lambda_iv_i+\sum_j(c\mu_j)u_j$$Thus $w_1+cw_2$ is a subspace of $L$. Any subspace that includes $S$ must also include $L$, and $L$ is a subspace of $V$. Therefore $L$ is the intersection of all subspaces that contain $S$, therefore $L$ is the subspace generated by $S$. 