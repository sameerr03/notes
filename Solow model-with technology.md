Adding capital results in diminishing returns - [[technology]] pushes against the diminishing returns. 

$$\dot{\tilde k}=s\tilde k^\alpha-(\delta+n+g)\tilde k$$$$\tilde y=\tilde k^\alpha$$
![[Screenshot_20230209_190315_Samsung Notes.jpg|400]]

At the steady state, $\dot{\tilde k}=0$$$s\tilde k^\alpha*=(\delta+n+g)\tilde k*$$$$(\tilde k*)^{\alpha-1}=\frac{(\delta+n+g)}{s}$$$$\tilde k*=(\frac{s}{\delta+n+g})^{\frac{1}{1-\alpha}}$$Then,$$\tilde y*=(\frac{s}{\delta+n+g})^{\frac{\alpha}{1-\alpha}}$$

Suppose $s$ increases ot $s'$
![[Pasted image 20230209190509.png|400]]
![[Pasted image 20230209190544.png]]
growth rate $g$ is constant in steady state-> Resulting in an upward sloping straight line. Per worker capital increases but g returns to normal over time. This happens as $\dot k/k$ is immediately affected by the change in the savings rate (it is an increasing function). As $\dot y/y$ is a function of growth rate of capital per worker, it sees a jump as well. However, with the increase in capital per worker, diminishing returns reduce the growth rate back to $g$.

### Derivation
With labour augmenting technology, the new production function becomes$$Y=K^\alpha(AL)^{1-\alpha}$$with which we can build upon the [[Solow model]]$$=K^\alpha A^{1-\alpha}L^{1-\alpha}$$$$\frac{Y}{L}=\frac{K^\alpha}{L} A^{1-\alpha}L^{1-\alpha}$$$$y=(\frac{K}{L})^\alpha A^{1-\alpha}$$$$y=k^\alpha A^{1-\alpha}$$$$\ln y=\alpha\ln k+(1-\alpha)\ln A$$$$\frac{d}{dt}\ln y=\alpha\frac{d}{dt}\ln k+(1-\alpha)\ln A$$$$\frac{\dot{y}}{y}=\alpha\frac{\dot{k}}{k}+(1-\alpha)\frac{\dot{A}}{A}$$
For $y$ growth rate to be constant, $k$ growth rate has to be constant as well. We know this from the solow equation, where the growth rate of k can only be constant if $y/k$ is constant which is only constant if the growth rates between y and k are (in steady state). Taking this rate to be $g_y$,$$g_y=\alpha g_y+(1-\alpha)\frac{\dot{A}}{A}$$$$g_y=\frac{\dot{A}}{A}=g$$
This proves that the growth rate of output and capital per worker is the same as the growth rate of technology. In the steady state,$$g=\frac{\dot{k}}{k}=\frac{sy}{k}-(\delta+n)$$$$\delta+n+g=\frac{sk^\alpha A^{1-\alpha}}{k} $$$$k=(\frac{s}{\delta+n+g})^{\frac{1}{1-\alpha}}A$$$$y=(\frac{s}{\delta+g+n})^{\frac{\alpha}{1-\alpha}}A$$The solow model shows that it is not possible to maintain constant growth rates without technological progress.

In order to represent the model using similar graphs, we make a transformation in the variables
$\tilde{k}=\frac{k}{A}=\frac{K}{AL}$ and $\tilde{y}=\frac{y}{A}=\frac{Y}{AL}$. This is the capital per effective worker and output per effective worker respectively.
$$\tilde{k}=\frac{k}{A}$$$$\ln\tilde{k}=\ln k-\ln A$$$$\frac{d}{dt}\ln \tilde{k}=\frac{d}{dt}\ln k-\frac{d}{dt}\ln A$$$$\frac{\dot{\tilde k}}{\tilde{k}}=\frac{\dot{k}}{k}-\frac{\dot A}{A}$$We know that $\dot k/k$ is $sy/k-(\delta+n)$. Therefore,
$$\frac{\dot{\tilde k}}{\tilde{k}}=\frac{sy}{k}-(\delta+n)-g$$
$$\frac{\dot{\tilde k}}{\tilde{k}}=\frac{sy/A}{k/A}-(\delta+n)-g$$$$\frac{\dot{\tilde k}}{\tilde{k}}=\frac{s\tilde y}{\tilde k}-(\delta+n+g)$$$$\frac{\dot{\tilde k}}{\tilde{k}}=\frac{s}{\tilde k^{1-\alpha}}-(\delta+n+g)$$$$\dot{\tilde k}=s\tilde k^\alpha-(\delta+n+g)\tilde k$$
This is in the form of the solow equation