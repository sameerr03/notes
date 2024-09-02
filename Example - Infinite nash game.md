This game results in infinitely many [[Nash equilibrium#Mixed stratergy Nash Equillibrium|MSNEs]].

|Dog/You|L|M|R|
|---|---|---|---|
|T|2,2|0,3|1,3|
|B|3,2|1,1|0,2|

No [[Nash equilibrium#Pure stratergy Nash Equilibrium (PSNE)|PSNE]]. Looking at [[vNm Expected utility]],

**For player Y**
$\sigma_D(T,B)=(p,1-p)$
$EU_Y(L,\sigma_D)=2$
$EU_Y(M,\sigma_D)=2p+1$
$EU_Y(R,\sigma_D)=p+2$

**For player D**
$\sigma_Y(L,M,R)=(q_1,q_2,1-q_1-q_2)$
$EU_D(T,\sigma_Y)=2q_1+(1-q_1-q_2)$
$EU_D(B,\sigma_Y)=3q_1+q_2$

**Type A: Y mixes all 3 stratergies**
This means that$$EU_Y(L,\sigma_D)=EU_Y(M,\sigma_D)=EU_Y(R,\sigma_D)$$Substituting the Equations, this is not possible. There is no type A [[Equilibrium]]

**Type B: Y mixes L and M**
This means that $$EU_Y(L,\sigma_D)=EU_Y(M,\sigma_D)\ge EU_Y(R,\sigma_D)$$Substituting the EU equations, we get $p=1/2$. At this value of $p$, Y plays this type of mixed stratergy resulting in $q_1,q_2\in[0,1],q_1+q_2=1$

For player D,
$EU_D(T,\sigma_Y)=2q_1$
$EU_D(B,\sigma_Y)=3q_1+q_2=3_q1+(1-q_1)=1+2q_1$

We find that B [[dominant stratergy#Strictly dominant stratergy|strictly dominates]] T. Therefore D will never play T. This means that in D's mixed stratergy profile, $p=0$. Using this value for player Y,

$EU_Y(L,\sigma_D)=2$
$EU_Y(M,\sigma_D)=1$
$EU_Y(R,\sigma_D)=2$

R strictly dominates M, which contradicts the [[Nash equilibrium#Rules for MSNE]] stated above. Therefore there will not be a equilibrium of type B

**Type C: Y mixes L and R**
This means that $$EU_Y(L,\sigma_D)=EU_Y(R,\sigma_D)\ge EU_Y(M,\sigma_D)$$Substituting the EU equations, we get $p=0$. At this value of $p$, Y plays this type of mixed stratergy resulting in $q_1\in[0,1],q_2=0$

For player D,
$EU_D(T,\sigma_Y)=2q_1+(1-q_1)=1+q_1$
$EU_D(B,\sigma_Y)=3q_1$

As $p=0$ for this stratergy, this means that $EU_D(B)\ge EU_D(T)$ for D to play pure stratergy B. Using this equation,$$3q_1\ge 1+q_1$$$$q_1\ge \frac 12$$For any value of $q_1\ge 1/2,q_2=0$, there is a MSNE of type C.$$MSNE=(([\frac 12,1],0,1-q_1),(0,1))$$

**Type D: Y mixes M and R**
This means that $$EU_Y(M,\sigma_D)=EU_Y(R,\sigma_D)\ge EU_Y(L,\sigma_D)$$Substituting the EU equations, we get $p=1$. At this value of $p$, Y plays this type of mixed stratergy resulting in $q_1=0,q_2\in[0,1]$

For player D,
$EU_D(T,\sigma_Y)=0+(1-q_2)=1-q_2$
$EU_D(B,\sigma_Y)=q_2$

As $p=1$ for this stratergy, this means that $EU_D(T)\ge EU_D(B)$ for D to play pure stratergy B. Using this equation,$$1-q_2\ge q_2$$$$q_2\le \frac 12$$For any value of $q_1=0,q_2\le 1/2$, there is a MSNE of type D.$$MSNE=((0,[0,\frac 12],1-q_2),(1,0))$$

