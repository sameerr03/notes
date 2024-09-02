# Combinatorics 
One experiment results in n outcomes and and other in m there are mn possible outcomes in both the experiments together

r experiments that result in $n_1$ for the relative experiment, the possible outcomes are $$n_1\cdot n_2.......n_r$$

## Permutations 
Permutations are **Ordered arrangements**

If n objects are to be arranged (where placement matters) and there are n number of spaces, there are n! posible arrangements

### With duplicates
n objects are to be arranged but $n_1,n_2...n_r$ are alike, then the number of arrangements will be 
$$\frac{n!}{n_1!n_2!.....n_r!}$$
## Combinations 
Order is irrelevant. The number of combinations of a set of data is$$C^n_r=\frac{n!}{(n-r)!r!}$$
Where:
- n→ number of objects  
- r-> number of positions

### Combinatorial identity
Total combinations = combinations with a particular object + combinations without that object
$$C^n_r=C^{n-1}_{r-1}+C^{n-1}_{r}$$
