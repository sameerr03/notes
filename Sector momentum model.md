Let us construct the momentum score model. First we find the period wise returns of all the sector portfolios. (each period is the rebalancing frequency. (Strategy period size has been 10 so far)$$R_s(t)  = \frac{\Pi_s(t)}{\Pi_s(t-p)}$$Where:
- $R_s(t)$ is the return of sector portfolio of sector $s$ for the period number $t$
- $\Pi_s(t)$ is the value of sector portfolio of sector $s$ at time period number $t$

We then find the most recent number of continuous periods where the sector portfolio has made a profit. If the last $x$ periods of the sector portfolio has been profitable and the period before that made a loss, we make $n_s(t) = x, m_s(t) =0$. If on the other hand, the sector portfolio made a loss for the last $x$ periods and made a profit before that, $m_s(t) = x, n_s(t) = 0$

We then calculate the exponentially weighted average return for this period of most recent continuous profits/losses. We assign the weight $\lambda\in (0,1)$ for this purpose. Therefore, the weighted return is given by $$\mu_s(t) = |\frac{\sum_{k=0}^{n_s(t)-1}R_s(t-k)\cdot\lambda^k}{\sum_{k=0}^{n_s(t)-1}\lambda^k}|$$We then find the profit increment and the loss increment. These increments use a sigmoid function. The size of the increments is dependent on the number of periods of continuous profitability/losses and the weighted magnitude of the profit/losses. Therefore$$P_s(t) = \frac{1}{1+\exp(-\alpha(n_s(t)\mu_s(t)-\beta))}$$and $$L_s(t) = \frac{1}{1+\exp(-\alpha(m_s(t)\mu_s(t)-\beta))}$$Putting everything together, the momentum score for sector $s$ at time $t$, $M_s(t)$ is given by $$M_s(t) = M_s(t-1)+yP_s(t)-(1-y)L_s(t)$$Where:
$y = \min (n_s(t), 1)$ so that only one of $L_s(t)$ or $P_s(t)$ are used in the update at any given point in time. 

We then select the weight of pairs from each sector based on $$w_s(t) = \frac{M_s(t)}{\sum_{k=1}^NM_k(t)}$$We then multiply this by the number of total pairs we choose (10 or more) and round down (to increase diversification) and find those many pairs from that sector. $N$ is the number of sectors with nonnegative and nonzero momentum scores.

