Let $a$ and $b$ be integers with $b>0$. Then there exist unique integers $q$ and $r$ such that $$a=bq+r\tag 1$$where $0\le r<b$

**Proof:**
We need to first prove that $p$ and $q$ exist, and then prove that they are unique. 
Let $$S=\{a-bk|k\in\mathbb Z\text{ and }a-bk\ge0\}$$If $0\in S$, this means that $a=bk$, and since $k\in \mathbb Z$, this means that $b$ divides $a$. Looking at (1), this means that $q=a/b, r=0$. 

If $0\not\in S$, and if $a>0$, then $a-b\cdot 0\in S$. If $a<0$, then $a-b(2a)=a(1-2b)\in S$. In either case, $S\ne \emptyset$. By the [[Set theory#Subset|well ordering principle]], $S$ must have a smallest number in it, say $r=a-bq$. Therefore $a=bq+r, r\ge 0$. Suppose that $r>b$, then $a-b(q+1)=a-bq-b=r-b>0$. This means that inside set $S$, we would have $a-b(q+1)$. However, this contradicts the fact that $r$ is the smallest member of $S$. Since $0\in S, r\ne b$ therefore $r<b$. 
This proves that $q$ and $r$ exist. 

Now looking at uniqueness, Suppose there are integers $r,r_0, q, q_0$ such that $$a=bq+r, a=bq_0+r_0$$where $0\le r,r_0<b$. equating these two conditions, $$bq+r=bq_0+r_0$$If we assume that $r_0\ge r$, From the last equation we have $b(q-q_0)=r_0-r$. Since $q$ and $q_0$ are integers, $b$ must divide $r_0-r$. However, $r_0, r< b$. Therefore this is only possible if $r_0-r=0\implies r=r_0\implies q=q_0$. Therefore $q,r$ are unique.  

#### Euclidian Algorithm
Algorithm to find the gcd - greatest common divisor of 2 integers. To compute $\text{gcd}(a,b)=d$, we use repeated division to obtain a sequence of positive integers. $$b=aq_1+r_1$$$$a=r_1q_2+r_2$$$$r_1=r_2q_3+r_3$$$$\vdots$$$$r_{n-2}=r_{n-1}q_n+r_n$$$$r_{n-1}=r_nq_{n+1}$$We obtain the sequence $r_1>r_2>\dots>r_n=d$
