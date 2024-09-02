#flashcards/micro #review 
# Utility functions
Utility functions are tools to display preference.

Utility functions are real value functions -> represent an element from the [[Choice sets|choice set]] as a real number.

A preference relation has a utility function if there exists a function $U: X\to R$ given that $(a,b\in X)$ such that $$a\succsim b \iff U(a) \ge U(b)$$

Optimal choice is obtained by maximising the Utility function. The maximal element of the choice set has the highest utility. Conversely, the optimised U function gives the maximal element. 

Values assigned to choices by the utility functions are of no magnitudal significance, they serve as just rankings.

## Equivalent U functions
There are infinitely many utility functions that represent the same choice set

Utility functions $V$ and $U$ are equivalent if they are strictly increasing monotone and 
$$V(x)=f(U(x))$$

## Cobb-Douglas function
For $\tilde{x}$, an n dimensional vector, the utility of the vector is given by the Cobb Douglas function :: $$U(\tilde{x})=\sum^N_{n=1}\alpha_n \ln(x_n)$$ where $\alpha_n$ is the utility weights for each vector dimension.
<!--SR:!2022-10-14,2,230-->

### Normalisation
Normalisation is the manipulation of the utility weights to make :: the sum of all the weights = 1 
<!--SR:!2022-10-15,3,268-->
$$\sum^N_{n=1} \alpha_n=1$$
Normalisation is done by :: dividing each weight with the sum of all the utility weights.
<!--SR:!2022-10-15,3,268-->

## Indirect utility function
The utility function that uses p1 p2 and m as the parameters. Substitute the values of x hat into the utility function to find the indirect function. 
