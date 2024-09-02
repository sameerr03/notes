#flashcards/stats 
# Random [[Variables]]
A numerical value based on the outcome of a chance experiment

For example,
Roll 2 dice, $X$ is a random variable where $X$ is the larger of the two rolls. Then, $X={1,2,3,4,5,6}$. $x$ is a particular value that the random variable can take.

Each possible $x$ has a probablitiy associated with it.

## Distribution functions
### Probablilty distribution
Random variables can be depicted by a probability distribution function. This function maps a particular value of the random variable with its probability. $$f(x_i)=P(x_i)$$
 Graph for a discrete distribution
 ![[Pasted image 20221003211915.png|400]]
### Cumulative distribution
Probability that the random variable takes a value less than or equal to a particular value ($x$) within the rule of the random variable($X$).$$F(x_i)=P(X\le x_i)$$$$F(a)=\sum_{all\ x\le a}f(x)$$
 Graph for a discrete distribution
 ![[Pasted image 20221003212016.png|400]]
In a continuous distribution between a and b, 
$$F(a\le X\le b)=\int_{a}^{b}f(x)\ dx=1$$
$$P(a\le X\le b)=F(b)-F(a)=\int_{-\infty}^bf(x)\ dx-\int_{-\infty}^af(x)\ dx$$

#### Properties of F(x)
1. $F(-\infty)=0$ and $F=(\infty)=0$
2. if $a<b$ then $F(a)\le F(b)$

### Conversions
For continuous Random Variables, PDFs can be converted into CDFs.
$$f(x)=\frac{dF(x)}{dx}$$
$$F(x)=\int f(x)dx$$

## Expected value
Expected value of the random variable. value of tfhe random variable weighted with probability.$$E(X)=\sum_{i=1}^nx_if(x_i)$$

when taking values of the random variable, $x-c$ is the error, where c is a predicted value. $(x-c)^2$ is minimised when $c=\mu= E(X)$. E(X) or mu is the mean.

### Properties
1. $E(AX+B)=AE(X)+B$
2. $E(g(X))=\sum_x g(x)f(x)$
3. $E(c\cdot g(X))=c E(g(X))$
4. $E (X+Y)= E(X)+ E(Y)$
5. $E (X+Y+Z)= E(X)+ E(Y)+ E(Z)$
6. Var$(AX+b)=A^2\sigma^2$
7. Var$(aX+bY)=a^2\text{Var}(X)+b^2\text{Var}(y)+2ab\text{Cov}(X,Y)$
8. Var$(aX-bY)=a^2\text{Var}(X)+b^2\text{Var}(y)-2ab\text{Cov}(X,Y)$

