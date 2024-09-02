In the real world, technology does not seamlessly flow from the countries at the technological frontier to countries within the frontier. This model depicts how being behind the frontier affects countries growth rates and their policymaking power.

#### General model of a country
Similar to [[Romer model]] and [[Solow model - with ideas]], the labour force of the economy is split up into those that work on the output sector and those that work on R&D. This split is represented by $$L=L_A+L_Y$$The ratio of researchers in the economy to the total workforce is given by $\gamma_A$. The production function used in this economy is given by$$Y=AL_Y=A(1-\gamma_A)L$$In per worker terms,$$y=A(1-\gamma_A)$$We define the growth rates of A and y as $\hat A$ and $\hat y$ respectively. From the [[Romer model]], we know that $$\hat A=\frac{\theta L_A^{\gamma}}{A^{1-\phi}}$$If we assume $\theta=1/\mu$, $\lambda=1$, $\phi=1$, then$$\hat A=\frac{L_A}\mu=\hat y=\frac{\gamma_AL}{\mu}$$on the balanced growth path. This implies that the long run growth rate of the economy is higher if $\gamma_A$ is higher. An increased share in research and development increases long run growth, which contradicts both romer and solow, and is not according to the [[Kaldor facts]].

#### Modelling two contries
Country 1 (innovator ($i$)) and 2(imitator ($c$)), where 1 is the technology leader and 2 is the innovator. This means that the investment of country 1 into R&D is greater than the investment of country 2, i.e., $\gamma_{A_i}>\gamma_{A_c}$. For country $i$,$$Y_i=A_i(1-\gamma_{A_i})L$$$$y_i=A_i(1-\gamma_{A_i})$$Taking log derviatives, $$\hat y_i=\hat A_i$$As $\gamma_{A_i}$ is assumed to be constant, this is the result. Using the value of $\hat A$ from the general model,$$\hat A=\frac{\gamma_{A_i}L}{\mu_i}$$Where $\mu_i$ is the cost of innovation. 

For country $c$,
$$\hat A_c=\frac{\gamma_{A_c}L}{\mu_c}$$where $\mu_c$ is the cost of copying. We assume that the cost of copying is a function of $A_i$ and $A_c$. $$\mu_c=F(\frac{A_i}{A_c})$$If $A_i$ is much greater than $A_c$, it is easier to copy as the tech. inferior country is likely to try and copy outdated technology, patents have expired, or the knowledge is more available. $A_i/A_c\to\infty,\ \mu_c\to0$. Conversely, if $A_i$ and $A_c$ are similar, it is harder to copy, meaning that the const is similar to innovating.$A_i/A_c\to0,\ \mu_c\to\mu_i$. This means that the function is a negative function. 

##### Steady state
Substituting the function for $\mu_c$$$\hat A_c=\frac{\gamma_{A_c}L}{F(A_i/A_c)}$$When $A$ ratio increases, $\hat A$ increases. When $A$ ratio is lower, $\hat A$ is lower. We also know that $$\hat A_i=\frac{\gamma_{A_i}L}{\mu_i}$$We know that this is equal to $\hat y$ at the steady state. Plotting this graph out, 
![[SmartSelect_Pin (5).jpg|400]]
if $A_i>A_c$, $A_c$ will start to rise as $\mu_c$ is lower. However, as $A_c$ increases $\mu_c$ will increase resulting in reaching the steady state. Same for $A_i<A_c$. 

##### Policy changes
In the imitator country, if policy changes increase $\gamma_{A_c}$ to $\gamma_{A_c}'$, $\hat A_c$ increases for every valur of $\mu_c$. Therefore the $\hat A_c$ shifts upwards.
![[SmartSelect_Pin (6).jpg|400]]

While this shift leads to a level effect in $\hat A_c$, There is a new steady state level reached where the growth rate values are the same. Therefore there is no long run change to the growth rate of technology. 

In the innovator country, if policy changes increase $\gamma_{A_i}$ to $\gamma_{A_i}'$, $\hat A_i$ increases for every value of $\mu_c$
![[SmartSelect_Pin (7).jpg|400]]

If the innovator makes a policy change, this will lead to an increase in the long run growth of both the countries. While $y$ falls short term due to the increase, the long run increase happens due to the increase in $\hat A_i$. 