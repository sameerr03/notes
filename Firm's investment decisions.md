A company may at any point in time have multiple investment ideas in order to generate values for the shareholders. In order to decide between these opportunities, many different metrics can be used.

##### [[Future and present values#Net present value|NPV]] estimation
The NPV estimation for a project can be done in the following steps
1. Estimating the future [[Cash flows]]
2. Estimating a discount rate
3. Estimating initial costs

The project will be undertaken if it has a positive NPV value. All the alternative investment opportunities can be ranked based upon their NPV values. 

For a stream of cash flows, $$\text{NPV}=-C_0+\frac{C_1}{(1+r)}+\frac{C_2}{(1+r)^2}+\frac{C_3}{(1+r)^3}+\dots$$
#### Payback period
The payback period of the project is the number of years taken to recover the initial costs i.e., how long will a project take to pay back the initial investment. It is important to note that the calculation of payback period does not account for the time value of money. The future cash flows are not discounted. Additionally, the minimum acceptance criteria and the ranking criteria for multiple opportunities is arbitrary. 

The metric is also biased towards liquidity and short term projects will tend to have better payback periods. 

Alternatively, the discounted payback period can be calculated, which uses discounted cash flows to pay off the initial investment, which will result in a higher discounted payback period than the regular payback period.

#### Internal rate of return (IRR)
The discount rate that results in a NPV of 0. The minimum acceptance criteria is if the IRR exceeds the required rate of return. A key assumption is that all future cash flows are reinvested at the IRR. Mathematically, the IRR is given by $$-C_0+\frac{C_1}{(1+\text{IRR})}+\frac{C_2}{(1+\text{IRR})^2}+\frac{C_3}{(1+\text{IRR})^3}+\dots=0$$![[Pasted image 20240219165501.png|400]]
##### Problems with IRR
There are two types of project categorizations
**Mutually exclusive projects** are projects where only one out of several potential projects can be chosen. The projects are ranked based on various different criteria and one is chosen.

**Independent projects** are projects where accepting or rejecting them does not effect/is not affected by the decisions taken on other projects. The projects in this case are chosen based on whether they meet the minimum acceptance criteria.

**Investing vs Borrowing:** for a regular cash flow pattern(A), the project is undertaken if the discount rate is lower than the IRR. However, for a borrowing based project (B) that has cash inflow in the first period followed by smaller cash outflows, the acceptance criteria is reversed, and the project is only accepted when the discount rate is more than the IRR. 
![[Pasted image 20240219170946.png]]

**Multiple IRRs** If the cash flows change direction more than once, then there can be multiple IRRs which renders the metric ineffective for making investment decisions. Resort to NPV for making decisions in this case. 

**Mutually exclusive specific problems**
**Scale problem**: One project may be better in terms of IRR, but does not offer a high NPV as the scale is low. (1 dollar at 50% vs 10 dollars at 10% = 1.5 vs 11 dollars, 2nd will give a  higher NPV the same $r$)

**Timing Problem:** Two projects $A$ and $B$. Both have the same upfront investment. $B$ gives out more in terms of future value, but these cash flows are in a later time period. ![[Pasted image 20240219174340.png]]
In this case $B$ will have the worse IRR. In this case the better project can be selected by using the [[Firm's investment decisions#Crossover rate|crossover rate]] and the NPV of differenced cash flows. $A-B$ implies that if the NPV is positive, $A$ should be chosen and $B$ otherwise. 

##### Modified IRR
When there are multiple changes in the signs in the cash flows, cash flows are discounted appropriately and combined with cash flows from another period so that only one change in sign remains. These modified cash flows are then used to calculate the MIRR in the same manner. If $C_3$ is negative along with $C_0$, then the modified cash flows are found by discounting $C_3$ to the second period.
$$-C_0+\frac{C_1}{(1+\text{MIRR})}+\frac{C_2+(C_3/(1+r))}{(1+\text{MIRR})^2}+\dots=0$$

##### Crossover rate
The discount rate above which the NPV of project A falls below the NPV of project B. 

The crossover rate can be found by taking the cash flows at each period as $C_t^A-C_t^B$. Finding the IRR of the stream of differenced cash flows gives us the crossover rate, $CR$.

Suppose $IRR_A>IRR_B$, then
- $A$ is preferred if $r>CR$
- $B$ is preferred if $r<CR$
and $r<IRR_A$, else neither will be selected as neither have a positive NPV for discount rate $r$
This is not a certain rule, depends on the return profile.
#### Profitability Index (PI)
The profitability index is given by $$\text{PI}=\frac{\text{PV of cash flows subsequent to initial investment }}{\text{Initial investment}}$$
The minimum acceptance criteria is $\text{PI}>1$. Alternatives can be ranked based on the highest PI.

