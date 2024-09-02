The [[Solow model-with technology]] proved to be impirically accurate. However, it was more accurate when it was extended to account for [[Human capital]]. The new [[Production Function]] that accounts for human capital is $$Y=K^\alpha(AH)^{1-\alpha}$$Where:
- A is technology
-  K is capital
- H is a function of L (labour)
$$H=e^{\psi u}L$$
Where:
- $\psi$ is the increase in H from one unit of time acquiring human capital
- $u$ is the amount of time spent acquiring human capital
- L is the labour force (number of workers)

In per worker terms, $$\frac{H}{L}=h=e^{\psi u}$$If $\psi=0.1$, H grows by 10% when u increases by 1 (the return t one year of acquiring H)

### Derivation
Finding the output with human capital in per worker terms,$$y=\frac{Y}{L}=(\frac{K}{L})^\alpha(\frac{H}{L})^{1-\alpha}A^{1-\alpha}=k^\alpha(Ah)^{1-\alpha}$$Taking logs on both sides,$$\ln y=\alpha\ln k+(1-\alpha)\ln A+(1-\alpha)\ln h$$Taking derivatives with respect to time,
$$\frac{\dot{y}}{y}=\alpha\frac{\dot{k}}k+(1-\alpha)\frac{\dot{A}}A+(1-\alpha)\frac{\dot{h}}h$$As human capital has impirically no trend growth rate, we assume that $\dot h/h$ is 0. Also, we already know that $\dot A/A=g$, the trend growth rate of technology. For the balanced growth path predicted by the [[Kaldor facts]], $\dot y/y$ must be constant, which requires that $\dot y/y=\dot k/k=g$. 

From the [[Solow model]], in the steady state, ($\dot k/k=g$ while $\dot {\tilde k}/k=0$ with technology.) $$\frac {\dot k}k=s\frac{k^\alpha}k-(\delta+n)$$as $y=k^\alpha$$$g=s\frac{y}k-(\delta+n)$$Substituting the production function per worker in,$$g=s\frac{(Ah)^{1-\alpha}}{k^{1-\alpha}}-(\delta+n)$$$$g+\delta+n=s(\frac{Ah}{k})^{1-\alpha}$$$$\frac{k}{Ah}=(\frac{s}{g+\delta+n})^\frac{1}{1-\alpha}$$$$y=k^\alpha(Ah)^{1-\alpha}=\frac{k^\alpha}{(Ah)^\alpha}(Ah)=(Ah)(\frac{k}{Ah})^\alpha$$ Combining both of the previous equations, $$y=Ah(\frac{s}{\delta+n+g})^\frac{\alpha}{1-\alpha}$$Substituting the value of h,$$y=Ae^{\psi u}(\frac{s}{\delta+n+g})^\frac{\alpha}{1-\alpha}$$This shows that human capital determined by u is an increasing function w.r.t output per worker, although it does not influence the growth rate per worker. Adding technology into the equation, $\tilde y=y/Ah$ can be used to find the steady state, setting $\dot{\tilde k}/k=0$
$$\tilde y^*=\frac{s}{n+g+\delta}^{\alpha/(1-\alpha)}$$

