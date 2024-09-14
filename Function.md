A [[Relations|relation]] that maps 2 [[Set theory|sets]] (the domain to the co-domain). The notation for a function is $$f:X\to Y$$which represents a function between sets $X,Y$ which assigns to each $x\in X$, a unique element $f(x)\in Y$. The identity function $Id_X:X\to X$ is the function that maps every element in $X$ to itself.

A function is a special case of a relation. There may be cases in the sets $X$ and $Y$ such that $xRy$ for many $y\in Y$. A function is a relation such that every element of $X$ is related to exactly one element of $Y$. 

#### Graph of a function
The graph of a function $f:X\to Y$ is the subset $G_f$ of $X\times Y$ defined by $$G_f=\{(x,y)\in X\times Y:x\in X\ \text{and}\ y=f(x)\}$$
#### Range, Domain, and Co-Domain
The domain is the set of inputs to the function. For the function $f:X\to Y$, $X$ is the domain. $Y$ is the set over which the outputs of the function will be present. $Y$ is the co-domain. 

The **range** of a function $f:X\to Y$ is the set of values $$\text{ran}\ f=\{y\in Y: y=f(x)\ \text{for some }x\in X\}$$

#### Types of functions
- surjection (Onto) - a function is surjective if $\text{ran }f = Y$ (for every $y\in Y$, there exists an $x\in X$ such that $y=f(x)$)
	![[Pasted image 20240829194226.png|400]]
- injection (1:1 function) - A function is injective if it maps distinct elements of $X$ to distinct elements of $Y$. If $x_1, x_2\in X$ and $x_1\ne x_2$ then $f(x_1)\ne f(x_2)$
	![[Pasted image 20240829194414.png|400]]
- bijection - A function is bijective if it is both injective and surjective. 
	![[Pasted image 20240829194543.png|400]]


Injective, surjective and bijective functions are all dependent on the domain, co-domain and range definition - without changing the form of the function. **Bijective function maps always have an inverse.** A bijective function $f:X\to Y$ has an inverse function $f^{-1}:Y\to X$$$f^{-1}(y)=x\iff f(x)=y$$
#### Function composition
The composition of functions $f:X\to Y$ and $g:Y\to Z$ is the function $g\circ f:X\to Z$ defined by $$(g\circ f)(x)=g(f(x))$$The order of application of the functions are from right to left. This function can only be defined if the domain of $g$ includes the range of $f$. 