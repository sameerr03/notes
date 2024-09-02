Variables in a [[Multiple variable regression]] that can take values of either 1 or 0. An example of a dummy variable is a catagorical variable. For example, the catagorical variable of soil type (sandy, loamy, coarse) can be represented as three separate dummy variables  (d_sandy, d_loamy, d_coarse) that can each take the value of one or zero.

However, all three cannot be accomodated into the regression at the same time as that violates the [[Multiple variable regression#Assumptions|assumption]] of no colinearity between the variables. (d_sandy can be represented as a function of d_coarse and d_loamy and they all cannot be present at the same time). Therefore only $d-1$ of the number of dummy variables can be in the regression at the same time. Taking the soil example into a regression,$$yeild=\beta_0+\beta_1d\_coarse+\beta_2d\_loamy+\epsilon$$to measure the change in yeild of a crop with respect to soil type. Here, as d_sandy has been dropped from the regression, it is considered the base dummy variable. The expected value of the yeild for different types of soil is (substituting the dummy variable values into the regression equation).

$E(yeild|d\_coarse=1,d\_loamy=0)=\beta_0+\beta_1$
$E(yeild|d\_coarse=0,d\_loamy=1)=\beta_0+\beta_2$
$E(yeild|d\_coarse=0,d\_loamy=0)=\beta_0$

The interpretation of these values is: $\beta_0$ is the effect of sandy soil on the yeild. $\beta_1$ is the effect of coarse soil on the yeild relative to sandy soil. Similar for loamy. If there are other factors being controlled for by the regression, $\beta_1$ would be the difference in yeild between sandy and loamy controlling for all the other variables.


### Changing the base dummy variable
Suppose we compare the original soil type regression with the alternate regression:$$yeild=\beta'_0+\beta'_1d\_coarse+\beta'_2d\_sandy+\epsilon$$The expected values of the yeild:
$E(yeild|d\_coarse=1,d\_sandy=0)=\beta'_0+\beta'_1$
$E(yeild|d\_coarse=0,d\_sandy=1)=\beta'_0+\beta'_2$
$E(yeild|d\_coarse=0,d\_sandy=0)=\beta'_0$

Finding the value of yeild due to coarse relative to loamy,$$E(yeild|d\_coarse=1,d\_loamy=0)-E(yeild|d\_coarse=0,d\_loamy=1)=E(yeild|d\_coarse=1,d\_sandy=0)-E(yeild|d\_coarse=0,d\_sandy=0)=\$$$$$(\beta_0+\beta_1)-(\beta_0+\beta_2)=\beta'_0+\beta'_1-\beta'_0$$$$\beta_1-\beta_2=\beta_1'$$

### Dummy variables for a [[Jointly distributed random variables|joint distribution]]
An example of this is if we want to check results on a sample that contains gender information as well as marital status information. Suppose there are only two dummy variables for each (male, female; married, unmarried). 

#### Cartesian product method
this means that using cartesian combination of the dummy variables(mm,mu,fm,fu), we can have four dummy variables that represent all possible combinations. One of the four is dropped and the other three are regressed. 

$$Earn=\beta_0+\beta_1MM+\beta_2MU+\beta_3FM+\epsilon$$
All the coefficients are in terms of the base dummy variable. 
$E(Earn|F=0,M=1)=\beta_0+\beta_1$
$E(Earn|F=0,M=0)=\beta_0+\beta_2$
$E(Earn|F=1,M=1)=\beta_0+\beta_3$
If the hypothesis is to find Earnings due to Marrried to unmarried women, the result would be $\beta_3$

#### [[Changes in form of MLR#Interaction among variables form|interaction]] method
The two dummy variables are multiplied as a separate dummy variable and are regressed on their own. The same example above would be regressed as 
$$Earn=\beta_0+\beta_1F+\beta_2M+\beta_3FM+\epsilon$$$E(Earn|F=0,M=1)=\beta_0+\beta_2$
$E(Earn|F=0,M=0)=\beta_0$
$E(Earn|F=1,M=1)=\beta_0+\beta_1+\beta_2+\beta_3$
$E(Earn|F=1,M=0)=\beta_0+\beta_1$

For the same hypothesis, the result would be $\beta_2+\beta_3$

