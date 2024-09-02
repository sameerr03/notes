
$$\dot{k}=sy-(\delta+n)k$$
$$y=k^\alpha$$
![[Screenshot_20230224_003910_Samsung Notes.jpg|400]]
At $k_0$, investment ($sy$) is more than depreciation ($(\delta+n)k$). Therefore, capital per worker rises. At $k_1$, investment is less than depreciation. Therefore, capital per worker falls. $k*$ is the long run-equillibrium, called the **steady state**. 

At the steady state,
$$sy=(\delta+n)k^*$$but, we know that $y=k^\alpha$. Therefore,$$sk*^\alpha=(\delta+n)k^*$$$$k*^{1-\alpha}=\frac{s}{\delta+n}$$$$k*=(\frac{s}{\delta+n})^{\frac{1}{1-\alpha}}$$And also,$$y*=k*^\alpha=(\frac{s}{\delta+n})^{\frac{\alpha}{1-\alpha}}$$The model predicts that GDP per worker is an increasing function according to MPS and a decreasing function according to depreciation and population growth. Therefore, countries with higher MPS will have more income per worker and countries with lower population growth (n) will have reducing income per worker.

#### The effect of an increase in savings rate
Savings rate goes from $s$ to $s'$. Both $y*$ and $k*$ will increase. When the increase is plotted to time, ![[Pasted image 20230208011439.png|400]]
The increase shows diminishing returns untill the new steady state is reached. This is due to the production function. 2nd derivative is negative as $\alpha$ is less than 1. Plotting the shift on the y-k axis, ![[Pasted image 20230208011738.png|400]]
The equation shows an upward shift and both capital and GDP per worker rise.

#### Growth Rates
The growth rates of both capital and output per worker are time derivatives of the log.$(\dot{k}/k)$

At $k*$, the growth rate of both capital and GDP per worker is 0. We know this as at $k*$,$$sk^\alpha=(\delta+n)k$$We also know from the solow equation that$$\dot{k}=sy-(\delta+n)k$$$$=0$$
We also know that $y=k^\alpha$, so applying the log derivative trick,$$\ln y=\alpha\ln k\implies \frac{d}{dt}\ln y=\alpha\frac{d}{dt}\ln k\implies\frac{\dot{y}}{y}=\alpha\frac{\dot{k}}{k}$$This means that the growth rates of both capital and labour is 0.
![[Pasted image 20230208013103.png|400]]
The further away an economy is from the steady-state (to the left), higher the growth rate.

Therefore there is no growth rate at the steady state, which contradicts the [[Kaldor facts]], creating the need for an exogenous variable to explain constant growth rates.



### Assumptions
- Economies produce an identical, single good (their [[Gross Domestic Product|GDPs]]).
- No trade
- Many firms, producing the same homogenous output 
- Firms enter and exit the market freely, and are perfectly competitive
- All produce using a similar [[Utility function#Cobb-Douglas function|cobb-douglas]] function

### Derivation
#### Production side
The real output/GDP of the economy $Y$ is produced according to the production function $$Y=F(K,L)$$
Where:
- K is the stock of capital goods
- L is the number of workers

This is written in cobb douglas form as$$Y=K^\alpha L^{1-\alpha}$$
Taking a firm as a representative for all others in the economy, their profit function is$$\Pi=K^\alpha L^{1-\alpha}-rK-wL$$
Where:
- $r$ is the rate of renting the capital goods for production
- $w$ is the wage of each worker

Differentiating according to inputs for maximum profit, we get$$\frac{\partial\Pi}{\partial L}=(1-\alpha)K^\alpha L^{-\alpha}-w=0$$
$$\frac{\partial\Pi}{\partial Y}\frac{\partial Y}{\partial L}=(1-\alpha)K^\alpha L^{-\alpha}=w$$
$$1\cdot MPL=(1-\alpha)\frac{K^\alpha L^{-\alpha}\cdot L}{L}=w$$
$$MPL=(1-\alpha)\frac{Y}{L}=w$$
Similarly,
$$MPK=\alpha\frac{Y}{K}=r$$
As a result, the total amount of money used for labour and capital is the total output, implying no profits for the firm (they are perfectly competitive, if there is profit, more firms join reducing it back to 0). 

The fraction of total output paid to each factor of production is $\alpha$ and $1-\alpha$ for K and L, respectively. This is consistent with the [[Kaldor facts]] on the US.  

The facts are mostly in output per worker. Therefore, dividing output by L we get$$y=\frac{Y}{L}=\frac{K^\alpha L^{1-\alpha}}{L}=\frac{K^\alpha}{L^\alpha}=k^\alpha$$
where:
- $y=\frac{Y}{L}$
- $k=\frac{K}{L}$

![[Pasted image 20230205015505.png|400]]
Capital per worker has a diminishing marginal output 

#### Capital accumulation side

$$\dot{K}=\frac{dK}{dt}=sY-\delta K$$
Where:
- $\dot{K}$ is the change in capital stock. Basically $K_{t+1}-K_t$ over infinite time periods
- $s$ (between 0 and 1) is the fraction of income that an individual saves (MPS). 
- $sY$ is the gross [[investment]](economy is closed)
- $\delta K$ is depreciation. Fraction of the existing stock of capital that breaks down

Dividing throughout by K,
$$\frac{\dot{K}}{K}=s\frac{Y}{K}-\delta$$
this is the growth rate of capital.

We know that
$$k=\frac{K}{L}$$
$$\ln k =\ln K-\ln L$$
$$\frac{\partial}{\partial t}\ln k=\frac{\partial}{\partial t}\ln K-\frac{\partial}{\partial t}\ln L$$
$$\frac{1}{k}\frac{\partial}{\partial t}k=\frac{1}{K}\frac{\partial}{\partial t}K-\frac{1}{L}\frac{\partial}{\partial t}\ln L$$
$$\frac{\dot{k}}{k}=\frac{\dot{K}}{K}-\frac{\dot{L}}{L}$$
Given the value of dotK/K, we get$$\frac{\dot{k}}{k}=s\frac{Y}{K}-\delta-\frac{\dot{L}}{L}$$
#### Population growth

We need to know the growth rate of workers, $\frac{\dot{L}}{L}$. Assuming that the workers grow at the same rate as the population, the growth equation can be$$L(t)=L(0)e^{nt}$$implying that the growth of workers is exponential (L(0) is the base value).

As a result, the growth rate is $$\frac{\dot{L}}{L}=n$$
#### Solow equation
Using the growth rate, we get
$$\frac{\dot{k}}{k}=s\frac{Y}{K}-\delta-n$$Rewriting,$$\frac{\dot{k}}{k}=s\frac{Y/L}{K/L}-\delta-n$$$$\frac{\dot{k}}{k}=s\frac{y}{k}-\delta-n$$$$\dot{k}=sy-(\delta+n)k$$Using the output per worker from the production side, we get$$\dot{k}=sk^\alpha-(\delta+n)k$$
