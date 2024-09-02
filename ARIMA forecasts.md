The [[ARIMA Model]] can be forecasted by using [[Difference equations#Forward iteration|forward iteration]] on the model equation. Considering the AR(1) process$$y_t=a_0+a_1y_{t-1}+\epsilon_t$$Iterating forwards, $$y_{t+1}=a_0+a_1y_t+\epsilon_t$$Taking expectations in time $t$,$$\mathbb E_ty_{t+1}=a_0+a_1\mathbb E_ty_t+\mathbb E_t(\epsilon_{t+1})$$we know that $\mathbb E_t y_t=y_t$ as the expectation is from $t$. Since $\epsilon$ is [[white noise processes|white noise]], $\mathbb E_t(\epsilon_{t+1})=0$. Therefore the one step ahead forecast is $$\mathbb E_ty_{t+1}=a_0+a_1y_t\tag 1$$Iterating forwards, $$y_{t+2}=a_0+a_1y_{t+1}+\epsilon_{t+1}$$taking expectations, $$\mathbb E_ty_{t+2}=a_0+a_1\mathbb E_ty_{t+1}+\mathbb E_t\epsilon_{t+2}$$Substituting (1), 
$$\mathbb E_ty_{t+2}=a_0+a_0a_1+a_1^2y_{t}$$This is the 2 step ahead forecast

#### General case
$$\mathbb E_ty_{t+j}=a_0(1+a_1+a_1^2+\dots+a_1^{j-1})+a_1^jy_t$$This is the $j$ step ahead forecast. However, when $j\to\infty$, $$\mathbb E_ty_{t+j}=\frac{a_0}{1-a_1}$$which is the unconditional mean of the series. The forecasted value converges to the mean of the series. Longer run forecasts are not much better. 

#### Higher order process
Consider an ARMA(2,1) process$$y_t=a_0+a_1y_{t-1}+a_2y_{t-2}+\epsilon_t+\beta\epsilon_{t-1}$$iterating forwards,
$$y_{t+1}=a_0+a_1y_{t}+a_2y_{t-1}+\epsilon_{t+1}+\beta\epsilon_{t}$$Taking expectations,$$\mathbb E_ty_{t+1}=a_0+a_1y_t+a_2y_{t-1}+\beta_1\epsilon_t$$Therefore, 

### Forecast Errors
$$e(j)=y_{t+j}-\mathbb E_ty_{t+j}$$For the one step ahead forecast, $$e_t(1)=y_{t+1}-\mathbb E_ty_{t+1}=\epsilon_{t+1}$$which is the unforecastable component of the timeseries. Taking the two step ahead forecast, $$e_t(2)=y_{t+2}-\mathbb E_ty_{t+2}=a_0+a_1y_{t+1}+\epsilon_{t+2}-[a_0+a_0a_1+a_1^2y_{t}]$$$$=a_0+a_0a_1+a_1^2y_t+a_1\epsilon_{t+1}+\epsilon_{t+2}-a_0-a_0a_1-a^2_1y_t$$$$=\epsilon_{t+2}+a_1\epsilon_{t+1}$$ 
#### Higher order process
Consider an ARMA(2,1) process$$y_t=a_0+a_1y_{t-1}+a_2y_{t-2}+\epsilon_t+\beta\epsilon_{t-1}$$iterating forwards,
$$y_{t+1}=a_0+a_1y_{t}+a_2y_{t-1}+\epsilon_{t+1}+\beta\epsilon_{t}$$Taking expectations,$$\mathbb E_ty_{t+1}=a_0+a_1y_t+a_2y_{t-1}+\beta_1\epsilon_t\tag{1 step ahead fc}$$Therefore, $$e_t(1)=y_{t+1}-\mathbb E_ty_{t+1}=\epsilon_{t+1}$$
Iterating forwards $$y_{t+2}=a_0+a_1y_{t+1}+a_2y_t+\epsilon_{t+2}+\beta\epsilon_{t+1}$$Taking conditional expectations, $$\mathbb E_ty_{t+2}=a_0+a_1\mathbb E_ty_{t+1}+a_2y_t$$$$=a_0+a_1(a_0+a_1y_t+a_2y_{t-1}+\beta_1\epsilon_t)+a_2y_t$$$$=a_0(1+a_1)+a_1^2y_t+a_1a_2y_{t-1}+a_1\beta_1\epsilon_t+a_2y_t$$$$=a_0(1+a_1)+(a_1^2+a_2)y_t+a_1a_2y_{t-1}+a_1\beta_1\epsilon_t\tag{2 step ahead fc}$$
Therefore,$$e_t(2)=y_{t+2}-\mathbb E_ty_{t+2}$$$$=a_0+a_1y_{t+1}+a_2y_t+\epsilon_{t+2}-\mathbb E_ty_{t+2}$$$$=a_0+a_1(a_0+a_1y_t+a_2y_{t-1}+\beta_1\epsilon_t)+a_2y_t+\epsilon_{t+2}-\mathbb E_ty_{t+2}$$$$=a_0(1+a_1)+(a_1^2+a_2)y_t+a_1a_2y_{t-1}+a_1\beta_1\epsilon_t+\epsilon_{t+2}+\beta_1\epsilon_{t+1}+a_1\epsilon_{t+1}-a_0(1+a_1)-(a_1^2+a_2)y_t-a_1a_2y_{t-1}-a_1\beta_1\epsilon_t$$$$=(a_1+\beta_1)\epsilon_{t+1}+\epsilon_{t+2}$$
In the general case, 
$$y_{t+j}=a_0+a_1y_{t+j-1}+a_2y_{t+j-2}+\beta_1\epsilon_{t+j-1}+\epsilon_{t+j}$$$$\mathbb E_ty_{t+j}=a_0+a_1\mathbb E_ty_{t+j-1}+a_2\mathbb E_ty_{t+j-2}$$$$e_t(1)=y_{t+j}-\mathbb E_ty_{t+j}$$$$=a_1(y_{t+j-1}-\mathbb E_ty_{t+j-1})+a_2(y_{t+j-2}-\mathbb E_ty_{t+j-2})+\epsilon_{t+j}+\beta_{t=j-1}$$$$=a_1e_t(j-1)+a_2e_t(j-2)+\epsilon_{t+j}+\beta_1\epsilon_{t+j-1}$$Therefore the $j$ step ahead forecast error is a 2nd order [[Difference equations|difference equation]].
#### General case
$$e_t(j)=\epsilon_{t+j}+a_1\epsilon_{t+j-1}+a_1^2\epsilon_{t+j-2}+\dots+a_1^{j-1}\epsilon_{t+1}$$The mean of the errors is given by $$\mathbb E[e_t(j)]=\mathbb E[\epsilon_{t+j}+a_1\epsilon_{t+j-1}+a_1^2\epsilon_{t+j-2}+\dots+a_1^{j-1}\epsilon_{t+1}]=0$$as $\epsilon$ is white noise. Therefore, the forecasts are unbiased estimates of each value of $y_{t+j}$. 
$\text{Var}(e_t(1))=\sigma^2$
$\text{Var}(e_t(2))=\sigma^2(1+a^2)$

If we assume that $\epsilon\sim N(0,\sigma^2)$, we can find the [[Estimation of population mean|confidence interval]] for the forecasts.
For one step ahead,$$CI=a_0+a_1y_t\pm \sigma Z$$For two steps ahead,$$CI=a_0(1+a_1)+a_1^2y_t\pm Z\sigma\sqrt{(1+a^2)}$$
where $Z$ is the z score based on the $\alpha$ value chosen. 


### Forecast Evaluation
When estimating the model coefficients - $a_1, a_2,\dots$ there will be some estimation error. This means that larger models usually contain in sample estimation errors that can induce forecast errors. 

Forecasts using overly parsimonious models with little parameter uncertainty can provide better forecasts than models consistent with the actual timeseries.

While comparing forecast errors of two models, the following methods can be used:
##### Iterative method
Use the first $n$ observations to estimate both models. Construct the forecast error obtained from the two models. Re-estimate the models using $n+1$ observations and construct the forecast errors. Repeat this procedure for all observations ($N$). There will be $N-n$ forecast errors from each model. Then the models are constructed where $$y_{n+i}=a_0+a_1f_{1i}+v_{1i}\ \forall\ i=1,2,\dots N$$$$y_{n+1}=b_0+b_1f_{2i}+v_{2i}\ \forall\ i=1,2,\dots N$$The restrictions $a_0=0, a_1=1, b_0=0, b_1=1$ form the null for their respective regressions. The model with the higher F test value has the more accurate forecast. If similar the model with smallest residual variance. ($f$ terms are the forecasts)

##### Mean Square Prediction Error (MSPE)
Construct one step ahead forecasts for both models. The MSPE is given by $$\text{MSPE}_1=\frac 1H\sum_{i=1}^He_{1i}^2,\ \text{MSPE}_2=\frac 1H\sum_{i=1}^He_{2i}^2$$where $H$ is the number of one step forecasts. The hypothesis 
$H_0: \text{MSPE}_1=\text{MSPE}_2$
$H_1: \text{MSPE}_1\ne \text{MSPE}_2$

$F_{H,H}=\frac{\text{MSPE}_1}{\text{MSPE}_2}>1$ imply that forecast errors from model 1 are larger then model 2

##### Diebold-Mariano Test
Applies when the following assumptions are violated
- $\mathbb E(e_t(j))\ne 0$ -> $e_t(j)$ is not normally distributed
- $e_t(j)$s are serially correlated
- $e_t(j)$s are contemporaneously correlated

$H_0:$ two models have the same forecasting power
$H_A:$ two models have different forecasting power

? more in notes ig
she hasnt really taught this too muhc