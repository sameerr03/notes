### Simple difference estimator
$$\text{ATE}=E[Y_{1T}|T=1]-E[Y_{1T}|T=0]$$$$\text{ATE}=E[Y_{1T}|T=1]-E[Y_{1C}|T=0]$$
ATE is the average treatment effect. The subscript 1 is the time and the letter is either the treatment and the control group. The first equation is not possible, as $E[Y_{1T}|T=0]$ is not observable (cannot observe the treatment group if they did not take the treatment). Instead, the control group is used as the counterfactual. This method can only be used when the control group is statistically representative of the treatment group (like in a [[Randomised Control Trials (RCTs)]]).

the [[Simple Linear Regression|OLS estimator]] can be used to find out the ATE, setting up the regression $$y_i=\alpha+\beta_1\text{Treat}+u_i$$Here $\beta_1$ is the simple difference estimator

### Pre post estimator
$$\text{ATE}=E[Y_{1T}|T=1\text{ (post)}]-E[Y_{0T}|T=1\text{ (pre)}]$$Assumption: there is no time trend that would have affected the treatment group regardless, the past is a suitable counterfactual. OLS estimator setup:$$y_i=\alpha+\beta_1\text{Treat}+u_i$$Here, $\beta_1$ is the pre-post estimator

### Difference in Differences (DiD)
Looks at changes over time with the outcome of the treatment in both the treatment and control group. 
$$(E[Y_{1T}|T=1\text{ (post)}]-E[Y_{0T}|T=1\text{ (pre)}])-(E[Y_{1C}|T=1\text{ (post)}]-E[Y_{0C}|T=1\text{ (pre)}])$$
This controls for the fact that the two groups are following a trend and the treatment group needs to be evaluated with that trend in mind (assumes that the treatment group without treatment would have continued the same trend as the control group). OLS estimator setup:$$y_i=\alpha+\beta_1\text{Treat}_i+\beta_2\text{Post}_i+\beta_3\text{Treat}\cdot\text{Post}+u_i$$Here, $\beta_3$ is the DiD estimator


