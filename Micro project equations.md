$$m=p_1x_1+p_2x_2$$
Utility function 
$$U(x_1,x_2)=\ln x_1+\ln x_2$$
Expected utility function
$$(1-\lambda)U(x_1,x_2)+\lambda\ \psi\ U(x_1,x_2)$$

$$x_2=\frac{m}{p_2}-\frac{p_1}{p_2}x_1$$
$$max\ U(x_1)=\ln x_1+\ln (\frac{m}{p_2}-\frac{p_1}{p_2}x_1)$$
Maximising,
$$\frac{1}{\hat{x}_1}+\frac{p_2}{m-p_1\hat{x}_1}(-\frac{p_1}{p_2})=0$$
$$\frac{1}{\hat{x}_1}=\frac{p_1}{m-p_1\hat{x}_1}$$
$$m-p_1\hat{x}_1=p_1\hat{x}_1$$
$$\hat{x}_1=\frac{m}{2p_1}$$
Subsitituting this value into the constraint,
$$\hat{x}_2=\frac{m}{p_2}-\frac{p_1}{p_2}\frac{m}{2p_1}$$
$$\hat{x}_2=\frac{m}{2p_2}$$
Can obtain the indirect utility function by substituting optimal values of x1 and x2 into the utility function
$$U(m,p_1,p_2)=\ln(\frac{m}{2p_1})+\ln(\frac{m}{2p_2})$$
**In scenario 1**
$$\lambda=0.01,\ p_1=1,\ p_2=2,\ m=20,\ \psi=0.3$$
The budget constraint becomes
$$20=x_1+2x_2$$
The new utility function is 
$$U(x_1)=\ln x_1+\ln (\frac{20-x_1}{2})$$
Maximising (using the general case found earlier),
$$\hat{x}_1=\frac{20}{2\times 1}=10,\ \hat{x}_2=\frac{20}{2\times 2}=5$$
Putting these values back into the utility function,
$$U(x_1,x_2)=\ln(10)+\ln(5)=3.91$$
The utility for getting an online delivery is 3.91. However, there is an uncertainty in the right order. Putting this utility value into the expected utility function accountign for this uncertainty, we get
$$EU_B=(1-0.01)\times 3.91+0.01\times 0.3\times 3.91$$
$$EU_B=3.88$$
**In scenario 2**
$$\lambda=0.2,\ p_1=1,\ p_2=2,\ m=20,\ \psi=0.3$$
Utility of getting the good remains the same. The expected utility after the outbreak becomes
$$EU_P=(1-0.2)\times3.91+0.2\times 0.3\times3.91$$
$$EU_P=3.36$$
The utiltiy drops in case 2 by a considerable margin. Consumers look for alternative markets to obtain groceries. 

**Middleman response**
In order to keep the consumers from looking for alternatives, the middleman must keep their expected utiltiy constant between both scenarios in the short term. Using the intial EU value along with the indirect utility function where only prices of the groceries change,
$$EU_B=(1-\lambda_p)U(m,p_1^*,p_2)+\lambda_p\psi\ U(m,p_1^*,p_2)$$
$$3.88=0.8\ U(m,p_1^*,p_2)+0.06\ U(m,p_1^*,p_2)$$
$$3.88=0.86\ U(m,p_1^*,p_2)$$
$$U(m,p^*_1,p_2)=4.51$$
$$\ln(\frac{m}{2p_1^*})+\ln(\frac{m}{2p_2})=4.51$$
$$\ln(\frac{20}{2p^*_1})+\ln(\frac{20}{2\times 2})=4.51$$
$$\ln(\frac{20}{2p^*_1})=4.51-\ln(5)$$
$$\ln(\frac{20}{2p^*_1})=2.9$$
$$\frac{20}{2p_1^*}=e^{2.9}=18.17$$
$$p^*_1=\frac{20}{2\times18.17}$$
$$p_1^*=0.55$$
Prices reduce by 45% in this case to keep the consumer at the same utility. 