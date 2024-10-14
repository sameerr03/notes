A rectangular array that stores information. The size of a matrix tells us how many rows and columns it has. A matrix of size $x\times y$ has $x$ rows and $y$ columns. 
#### Matrix notation of a linear system
Given the example $$x_1-2x_2+x_3=0$$$$2x_2-8x_3=8$$$$-4x_1+5x_2+9x_3=-9$$We can construct the matrix of coefficients of $x_i$s called the coefficient matrix$$\begin{bmatrix}1&-2&1\\0&2&-8\\-4&5&9\end{bmatrix}$$and the matrix including the terms on the RHS is the augmented matrix$$\begin{bmatrix}1&-2&1&0\\0&2&-8&8\\-4&5&9&-9\end{bmatrix}$$
##### Row picture
We can write the example system of linear equations into the matrix form using the coefficient matrix as $$\begin{bmatrix}1&-2&1\\0&2&-8\\-4&5&9\end{bmatrix}\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}0\\8\\-9\end{bmatrix}$$When we multiply the coefficient matrix by the variable column, we get the system of individual equations from the example. 

##### Column picture
We can also take the individual variables and multiply them with their corresponding columns and we obtain$$x_1\begin{bmatrix}1\\0\\-4\end{bmatrix}+x_2\begin{bmatrix}-2\\2\\5\end{bmatrix}+x_3\begin{bmatrix}1\\-8\\9\end{bmatrix}=\begin{bmatrix}0\\8\\9\end{bmatrix}$$
#### Elementary matrix row operations
For the matrix $A/\mathbb F$, we define 3 elementary operations
1. Scaling: Multiplication of one row of $A$ (row $r$) by a nonzero scalar $c$
2. Replacement: Replace row $r$ by row $r$ plus $c$ times row $s$, $r\ne s$, where $c$ is a scalar
3. Interchange: Interchange two rows $r$ and $s$ of $A$. 

(1) To every elementary row operation $e$, there corresponds another elementary row operation $e_1$, of the same type of $e$ such that $e_1(e(A))=e(e_1(A))=A$. The inverse of an elementary row operation exists, and is an elementary row operation itself. 

If $A$ and $B$ are $m\times n$ matrices, we say that $B$ is **row equivalent** to $A$ if $B$ can be obtained by using a finite sequence of elementary row operations on $A$. This is a equivalence [[Relations|relation]]. 

(2) If $A$ and $B$ are row equivalent, then the systems $AX=0$, $BX=0$ have the same solution set. 

#### Reduced-row echelon form (RREF)
An $m\times n$ matrix $A$ is **row-reduced** if 
1. The first non-zero entry in each non-zero row of $A$ is 1
2. Each column of $A$ that contains a leading non-zero entry of some row has all its other entries 0. (if the leading element 1 of some row is in that column, the rest of the column should be 0)

(3) Every $m\times n$ matrix is equivalent to a row reduced matrix. 

A matrix $A$ is in row-reduced echelon form (RREF) if 
1. $A$ is row-reduced
2. Every zero row occurs below every nonzero row
3. If row $1,2,\dots,r$ are the nonzero rows of $A$ and if the leading nonzero entry of row $i$ occurs in column $k_i$, $1\le i\le r$, then $k_1<k_2<\dots<k_r$, $r$ is the rank of $A$ ($k$ is the column corresponding to the leading nonzero entry). Thus the leading entries should be in stepwise manner. 

(4) Every $m\times n$ matrix $A$ is row equivalent to a RREF matrix. The resulting RRED is unique to $A$ up to row equivalence. 

If $A$ and $B$ are row-equivalent matrices that are also RREF, then $A=B$. Alternatively, any 2 matrices are row equivalent if and only if they have the same RREF. 

If $A$ is an $m\times n$ matrix with $m<n$, then the homogeneous system $AX=0$ has a non trivial solution (there will be some free variables that satisfy the system of equations for a range of values whereas the others are fixed to one value)
Supposed $R$ is the RREF. Then the system of equations $RX=0$, the number of nonzero rows $r$ (rank of $R$) is less then the total number of variables $n$, then the system will have a non trivial solution (there will be free variables)

(5) If $A$ is a $n\times n$ matrix then $A$ is row equivalent to $I$ iff $AX=0$ has only the trivial solution
**Proof:** Suppose $AX=0$ has only the trivial solution $X=0$. $R$ is an $n\times n$ RREF matrix which is row equivalent to $A$. $r$ is the number of nonzero rows of $R$. $RX=0$ has no non-trivial solution => $r\ge n$, but since $R$ has $n$ rows, $r\le n$ => $r=n$. This means that $R$ has leading 1 in each row and the remaining elements in the columns are 0 and each 1 is in a different column. Therefore $R$ is the identity matrix $I$.

(6) Linear system is consistent (at least one solution exists) iff the rightmost column in the augmented matrix is not a pivot column i.e., iff the RREF of the augmented matrix has no rows of the form $[0,0,\dots,b], b\ne 0$. This means that the system has a unique solution and 0 free variables, or infinitely many solutions and at least one free variable.
###### Example of row-reduction using elementary operations
![[Pasted image 20240924171016.png]]
![[Pasted image 20240924171023.png]]



#### Matrix multiplication
Let $A$ be an $m\times n$ matrix over $\mathbb F$ and $B$ be a $n\times l$ matrix over $\mathbb F$. The product $C=AB$ is an $m\times l$ matrix over $\mathbb F$ whose entries are given by $$c_{ij}=\sum_{k=1}^na_{ik}b_{kj}$$The multiplication of two matrices are not always defined. It is only defined if the number of columns in the first matrix matches the number of rows in the second matrix. Further, it is not necessarily true that $AB=BA$. 

(7) If $A,B,C$ are matrices over $\mathbb F$ such that the product $BC$ and $A(BC)$ are defined, the so are the products $AB$ and $(AB)C$. We also have $$A(BC)=(AB)C$$
**Proof:** Let $B$ be an $n\times p$ matrix. If $C$ is defined, then it must have $p$ rows and $BC$ will have $n$ rows. Assuming that $A$ is an $m\times n$ matrix, we an infer that the product $AB$ exists and is an $m\times p$ matrix. As a result, the product $(AB)C$ also exists. We must prove that $$[A(BC)]_{ij}=[(AB)C]_{ij}$$for each $i,j$. By definition, $$[A(BC)]_{ij}=\sum_{k=1}^na_{ik}[BC]_{kj}$$$$=\sum_{k=1}^na_{ik}(\sum_{t=1}^pb_{kl}c_{lj})=\sum_{k=1}^n\sum_{l=1}^pa_{ik}b_{kl}c_{lj}=\sum_{l=1}^p(\sum_{k=1}^na_{ik}b_{kl})c_{lj}=\sum_{l=1}^p[AB]_{il}c_{lj}=[(AB)C]_{ij}$$\
When $A$ is a square matrix of size $n\times n$, the product of $A$ with itself - $AA$ can be represented as $A^2$. The product of $A$ multiplied by itself $k$ times can be denoted as $A^k$. 

#### Identity matrix
For each positive integer $n$ there is a specific matrix called the identity matrix $Id_n$ which is defined as $(Id_n)_{ij}=\delta_{ij}$. The symbol $\delta_{ij}$ is defined as $$\delta_{ij}=\begin{cases}0&\text{if } i\ne j\\1&\text{if }i=j\end{cases}$$This is the multiplicative identity of matrix multiplication, either from the right or the left side. $$Id_n\cdot A=A$$An $m\times m$ matrix is said to be an elementary matrix if it can be obtained from the $m\times m$ identity matrix by means of a single elementary row operation. Elementary matrices are invertible. This can be proved by using an elementary row operation and its inverse row operation so that we can get $I$, on both sides to show that it is invertible. 

(8) Let $e$ be an elementary row operation and $E=e(Id)$. Then for every $m\times n$ matrix $A$, $e(A)=E\cdot A$. 
**Proof:** Assume that row $r\ne s$ and $e$ represents the operation of replacing row $r$ with row $r$ plus $c$ times row $s$. $$E_{ij}=\begin{cases}\delta_{ij}&\text{if }i\ne r\\\delta_{rj}+c\delta_{sj}&\text{if }i=r\end{cases}$$Therefore, $$(EA)_{ij}=\sum_{k=1}^mE_{ik}A){kj}=\begin{cases}A_{ij}&\text{if }i\ne r\\A_{rj}+cA_{sj}&\text{if }i=r\end{cases}$$Therefore, $EA=e(A)$

#### Invertible matrices
Let $A$ be an $n\times n$ matrix over $\mathbb F$. An $n\times n$ matrix $B$ such that $BA=Id_n$ is called the left inverse of $A$. An $n\times n$ matrix $B$ such that $AB=Id_n$ is called the right inverse of $A$. If $AB=BA=Id_n$ then $B$ is called the two sided inverse of $A$, and $A$ is invertible. 

(9) If $A$ has a left inverse $B$ and a right inverse $C$, then $B=C$
**Proof:** Suppose $BA=I$ and $AC=I$, then $B=BI=B(AC)=(BA)C=IC=C$

(10) Let $A$ and $B$ be $n\times n$ matrices over $\mathbb F$, then 
1. If $A$ is invertible, so is $A^{-1}$, and $(A^{-1})^{-1}=A$
2. If both $A$ and $B$ are invertible, then $(AB)^{-1}=B^{-1}A^{-1}$
**Proof:** The first part is from the symmetry of the definition of the inverse. The second part:$$(AB)B^{-1}A^{-1}=A(BB^{-1})A^{-1}=A\cdot I\cdot A^{-1}=A\cdot A^{-1}=I$$One can similarly show that $B^{-1}A^{-1}(AB)=I$ 

If $A$ is an $n\times n$ matrix, then the following are equivalent
1. $A$ is invertible
2. $A$ is row equivalent to the $n\times n$ identity matrix
3. $A$ is a product of elementary matrices
4. The homogeneous system $AX=0$ has only trivial solution
5. The system of equations $AX=B$ has solution $X$ for every $n\times 1$ matrix $B$