The greatest common divisor can be represented as $$\text{gcd}(a,b)
=am+bn, m,n\in \mathbb Z$$**Proof:** We define the set $$S_{a,b}=\{ax+by|x,y\in \mathbb Z, ax+by>0\}$$This [[Set theory|set]] $S_{a,b}\ne \emptyset$ if $a\ne 0$ as this implies that either$$a>0\implies a\in S_{a,b} (
x=1)$$or$$a<0\implies-a\in S_{a,b}(x=-1)$$
Therefore the set cannot be empty. By the well ordering principle, there is a smallest element $d=am+bn$ for some $m,n\in \mathbb Z$. We can claim that $d=\text{gcd}(a,b)$. To show this, we use the [[Division algorithm]] on $a$. This gives us $$a=qd+r=q(am+bn)+r$$This means that $r=a(1-qm)+b(-qn)$. We also know that $d>r\ge 0$. Therefore $r\in S_{a,b}$ if $r\ne 0$. As $r<d$, by the minimality of $d$ (well ordered pair), $r=0$. This shows that $d|a$. Similarly, $d|b$.

![[Pasted image 20240919040613.png]]




