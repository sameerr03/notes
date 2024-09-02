This [[Solow model|solow model]] uses [[ideas]] as a function in order to determine the rate of [[technology]] on population growth. The labour force $(L)$ is divided into two sections, where one develops new ideas ($L_A$) and the other uses those ideas for final production($L_Y$). This results in two production functions, where $$Y=K^\alpha(AL_Y)^{1-\alpha}$$
and $$\dot A=\bar\theta L_A$$
where $\bar\theta$ is the productivity rate of a researcher. $\bar\theta$ is based on the number of R&D workers, as well as pre-existing technology. More $L_A$ leads to higher chance of a new idea, but the problem of overlapping work (only the first gets credited with the new idea). Higher $A$ results in a larger set of tools used for R&D but also ideas become harder to develop (more expensive, more training required to reach the frontier as a researcher). Higher technology leads to a lower productivity of worker. This leads to the formula$$\bar\theta=\theta A^\phi[L_A]^{\lambda-1}$$Where:
- $\phi=0$=> Knowledge does not affect acquiring new knowledge
- $\phi<0$=> More knowledge = less ideas
- $\lambda<1$ but positive, more labour affects the production of ideas.

The final equation for output per worker is given by $$y=\frac{\theta s_rL}{g}(1-s_R)(\frac{s}{\delta+n+g})^{\alpha/1-\alpha}$$Where $s_r$ is a the ratio of workers in the research sector. It is assumed that this remains constant after population growth. 

### Policy changes
$$\frac{\dot A}{A}=\frac{\theta s_rL}{A}$$when $\lambda=1,\phi=0$. By increasing $s_r$ using policy, we get no long term growth. The technology shows an increase in growth rate initially, but by the increase in A the growth rate slows down diminishingly. $s_r$ eventually falls to the before policy level (third graph, $L_A$ is related to $s_r$). 
![[SmartSelect_Pin (1).jpg|300]]
![[SmartSelect_Pin (2).jpg|300]]
![[Screenshot_20230317_002703_Samsung Notes.jpg|300]]
There is a permanent increase in $A$ due to the jump in growth rate, but no long term effects on growth rate. 

### Derivation
$$L=L_A+L_Y$$
and $$\dot A=\bar\theta L_A$$Substituting with the formula for $\bar\theta$,
$$\dot  A=\theta A^\phi L_A^\lambda$$Using log derivatives,$$\frac{\dot A}{A}=\theta A^{\phi-1} L_A^\lambda$$
$$y=\frac YL=\frac{K^\alpha(AL_Y)^{1-\alpha}}{L}=(\frac KL)^\alpha(\frac{AL_Y}{L})^{1-\alpha}$$$$y=k^\alpha(\frac{A(1-s_r)L}{L})^{1-\alpha}=k^\alpha(A(1-s_r))^{1-\alpha}$$Using log-derivatives,$$\frac{\dot y}{y}=\alpha\frac{\dot k}{k}+(1-\alpha)\frac{\dot A}{A}+0$$As the time derivative of the constant $s_r$ is 0. Along the balanced growth path, we know that output and capital grow at the same rate.$$g_y=\frac {\dot y}{y}=\frac{\dot k}{k}$$By substitution,
$$g_y=\alpha g_y+(1-\alpha)\frac{\dot A}{A}$$$$g_y=\frac{\dot A}{A}$$Substituting this into the equation for ideas$$g_y=\theta A^{\phi-1} L_A^\lambda$$As $g_y$ is a constant, $\theta L_A^\lambda/A^{1-\phi}$ must be constant, implying that $L_A^\lambda$ and $A^{1-\phi}$ have to grow at the same rate. Taking log derivatives and equating the growth rates,$$\lambda\frac{\dot L_A}{L_A}=(1-\phi)\frac{\dot A}{A}=g_A(1-\phi)$$$$g_A=\frac{\lambda}{1-\phi}(\frac{\dot L_A}{L_A})$$as $s_r$ is constant, $\dot L_A/L_A=\dot L/L=n$. At the steady state, $g_y=g_A$. Therefore$$g_A=\frac{\lambda n}{1-\phi}$$Unlike the solow model, there is a positive dependance of the growth rate of technology with $n$.

From the [[Solow model]],$$\frac{\dot k}{k}=s\frac YK-\delta-n$$$$g_A=s\frac{K^\alpha(AL_Y)^{1-\alpha}}{K}-(\delta+n)$$$$g_A+\delta+n=s(\frac KL)^{\alpha-1}(A(1-s_r))^{1-\alpha}$$$$sk^{\alpha-1}[A(1-s_r)]^{1-\alpha}=\delta+n+g_A$$$$k^\alpha=(\frac{s}{\delta+n+g})^{\alpha/1-\alpha}[A(1-s_r)]^\alpha$$We know that $y=k^\alpha[A(1-s_r)]^{1-\alpha}$$$y=A(1-s_r)(\frac{s}{\delta+n+g})^{\alpha/1-\alpha}$$We also know that $g_A=\dot A/A=\theta L_A^\lambda/A^1-\phi$. Setting $\lambda=1,\phi=0$ we get $g_A=\theta L_A/A$ => $A=\theta s_rL/g_A$. Substituting this into the solow equation,
$$y=\frac{\theta s_rL}{g_A}(1-s_R)(\frac{s}{\delta+n+g})^{\alpha/1-\alpha}$$$s_r$ has conflicting effects on $y$. There are also conflictine effects on population. Higher L leaves lower y but also increases the production of ideas.