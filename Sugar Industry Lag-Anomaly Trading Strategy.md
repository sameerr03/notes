### 1. Executive Summary

This report presents an analysis of a trading strategy based on the relationship between the largest cap stock in the Indian sugar industry (EID Parry) and other top stocks in the sector. The strategy aims to capitalize on potential lagged effects of significant price movements in EID Parry on other sugar industry stocks.

Key findings:

- In-sample performance (2020-2023): 12.33% annualized return
- Out-of-sample performance (2024 YTD): 1.39% annualized return
- Significant discrepancy between in-sample and out-of-sample results, indicating potential overfitting and the need for more robust anomaly identification techniques

### 2. Methodology

#### 2.1 Data

- Stocks analyzed (NSE Ticker symbols): EIDPARRY, BALRAMCHIN, RENUKA, TRIVENI, BAJAJHIND, BANARISUG, DALMIASUG, DCMSHRIRAM, DHAMPURSUG, AVADHSUGAR 
- Nifty 50 is taken as the index for beta calculations
- Time period: January 1, 2020 to August 19, 2024 (in-sample: 2020-2023, out-of-sample: 2024 YTD)
- Data source: Daily adjusted closing prices from Yahoo Finance

#### 2.2 Proxy for Event Based Moves

We look for large moves in EID Parry to determine if the remaining stocks in the industry follow the large moves in a lagged manner. However, when using algorithmic back testing, obtaining and algorithmically interpreting news is a difficult task. To get around this, we use a significant deviation in the return of EID Parry's return from the return of the Market as the classification condition for a 'significant move'.

We use the CAPM model to determine the beta$$R_{\text{EIDPARRY},i}=R_f+\beta R_{M,i}+ e_i$$We then find the deviations of the actual market return from the expected return, $$e_i=R_{\text{EIDPARRY},i}-R_f-\beta R_{M,i}$$We assume that $R_f \approx 0$ as we are focusing on short term trades, and so the risk free rate is not very significant. We find the mean and standard deviation of $e$ -  $\mu_e$ and $\sigma_e$, A day $i$ is considered a 'significant move' day if $$R_{\text{EIDPARRY},i} -\beta R_{M,\ i}>k\sigma_e + \mu_e$$For all results presented, we consider $k=2$. This method assumes a normal distribution of returns

#### 2.3 Picking Stocks to Trade

In order to determine if there are patterns after a significant move in EIDPARRY in the other stocks, we need to determine if the returns of stock $s$ at lag $l$ after a significant move ($m$) is different from the returns at lag $l$ not after a significant move ($n$). To do this, we set up the hypothesis testing framework: 

$H_0 : \mu_{s, l,m}= \mu_{s, l,n}$
$H_A: \mu_{s, l,m}\ne \mu_{s, l,n}$

Rejecting the null hypothesis implies that the returns of stock $s$, $l$ days after a significant move in EIDPARRY are statistically different to the returns of stock $s$ not after a significant move. This means that the returns could be due to an anomaly in prices and are less likely due to market noise. 

Further, we conduct cross-correlation analysis on the returns of EIDPARRY onto the returns of stock $s$ after a significant move, allowing us to see the relation of EIDPARRY returns on returns of $s$ at different lags $l$. A positive correlation implies that on average, a significant move up in EIDPARRY leads to a positive move in $s$. This can tell us what direction our trades should be placed (a negative correlation would imply we take the opposite position of EIDPARRY's move $l$ days after)

With the correlation, we can identify whether we take the same or inverted position in stock $s$, $l$ days after a significant move in EIDPARRY. To further ensure that our results are robust, we find the returns taking the appropriate position in $s$. We need to ensure that these returns are statistically different from 0, indicating that there is an anomaly and the results are not due to market noise. We use the hypothesis testing framework:

$H_0 :\mathbb E(R_{s, l,m})= 0$
$H_A: \mathbb E(R_{s, l,m})\ne 0$

We can also use the Granger causality test to determine if the lagged returns of $s$ after a significant move add to the explanatory power of an autoregressive model of EIDPARRY's returns for all significant moves. This would boost the robustness of the anomaly that we have identified. 

On the 2020-23 data, only one stock (BALRAMCHIN) passed all the statistical tests for any lags. However, we still considered stocks that passed the other two hypothesis tests for our analysis. The final list of stocks included:  BALRAMCHIN, RENUKA, BANARISUG, DALMIASUG, DHAMPURSUG, AVADHSUGAR

#### 2.4 Strategy Design

1. Calculate daily returns for all stocks and the market index (NIFTY 50).
2. Compute the beta ($\beta$) of EID Parry against the market: $\beta = \frac{Cov(R_{\text{EIDPARRY}}, R_{M})}{Var(R_{M})}$
3. Identify significant moves in EID Parry using a 2-sigma threshold on the CAPM residual: $e_t = R_{\text{EIDPARRY},i} - \beta R_{M,i}$ Significant move if: $e_i > \mu_e + 2\sigma_e$
4. Generate trading signals for each stock based on EID Parry's significant moves and specified lags (3 days for all stocks in this implementation from the previous selection criteria).
5. On signal days, invest equally in all stocks with active signals.
6. Calculate daily strategy returns as the average return of all invested stocks on each day.

### 2.5 Performance Metrics

- Annualized return
- Expected Internal Rate of Return (XIRR)
- Strategy Beta
- Strategy Alpha
- Sharpe ratio
- Maximum Drawdown
- Trade Win rate

### 3. Results

### 3.1 In-Sample Performance (2020-2023)

![[Pasted image 20240820022823.png|300]]
![[Pasted image 20240820022844.png]]
![[Pasted image 20240820022900.png]]
### 3.2 Out-of-Sample Performance (2024 YTD)
![[Pasted image 20240820022936.png|400]]
![[Pasted image 20240820022957.png]]
![[Pasted image 20240820023007.png]]

### 4. Analysis and Interpretation

The significant discrepancy between in-sample and out-of-sample performance suggests:

1. Potential overfitting to the in-sample data
2. Changes in market dynamics or the relationship between EID Parry and other sugar stocks
3. Need for more robust anomaly identification techniques

The strategy shows promise in capturing some relationship between the largest cap stock and other stocks in the sugar industry. However, the poor out-of-sample performance indicates that the current implementation may not be reliable for actual trading without further refinement.

### 5. Future Work

More robust anomaly detection tools are required. The strategy can use shorter rolling windows for analysis, adapting the thresholds to the latest market environment. Stricter stock selection metrics can be applied (Granger Causality Test can be a strict requirement). Machine Learning models could be applied to detect non linear relations, potentially improving anomaly detection. 

We also need to focus on preventing overfitting to historical data, ensuring that our models can achieve significant profitability out of sample. Sensitivity analysis using monte-carlo simulations can help us understand how much the profitability is affected by the changes in parameters (rolling window sizes, $k$, number of stocks, etc.). 

## 7. Conclusion

The initial analysis provides valuable insights into the potential relationships between stocks in the Indian sugar industry. While the in-sample results were promising, the poor out-of-sample performance highlights the need for further refinement and more robust methodologies. This work serves as a foundation for developing a more sophisticated and reliable trading strategy in the sugar industry sector.