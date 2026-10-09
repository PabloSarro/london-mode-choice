| Estimation | of the     | parameters |
| ---------- | ---------- | ---------- |
| Maximum    | likelihood | estimation |
Michel Bierlaire
| Mathematical | Modeling | of Behavior |
| ------------ | -------- | ----------- |
1/62

Outline
Estimation of the parameters
Example
Output of the estimation
2/62

| Maximum | likelihood | estimation |     |     |
| ------- | ---------- | ---------- | --- | --- |
Motivation
▶
| The | logit model | involves unknown | parameters: | µ, β . |
| --- | ----------- | ---------------- | ----------- | ------ |
k
▶ Their value must be inferred from a sample of observations.
▶
| We  | use maximum | likelihood | to estimate their | value. |
| --- | ----------- | ---------- | ----------------- | ------ |
3/62

| Observed | and           | unobserved | heterogeneity |     |     |
| -------- | ------------- | ---------- | ------------- | --- | --- |
| Observed | heterogeneity |            |               |     |     |
▶
|     | Parameters | may depend | on observed | characteristics | s : |
| --- | ---------- | ---------- | ----------- | --------------- | --- |
n
|     |         |           | µ = µ(s ;γ),     | β = β(s  | ;θ), |
| --- | ------- | --------- | ---------------- | -------- | ---- |
|     |         |           | n n              | n        | n    |
|     | where γ | and θ are | common parameter | vectors. |      |
▶
This represents systematic differences across observed groups or
characteristics.
| Unobserved |     | heterogeneity |     |     |     |
| ---------- | --- | ------------- | --- | --- | --- |
▶
Differences not explained by s cannot generally be written as deterministic
n
|     | functions | of s . |     |     |     |
| --- | --------- | ------ | --- | --- | --- |
n
▶
They require additional assumptions, such as random coefficients or latent
classes.
4/62

| Example: | specification |               | table | of the model |            |
| -------- | ------------- | ------------- | ----- | ------------ | ---------- |
|          | Alternative   | i             |       | Alternative  | j          |
|          | β c cost      | of trip (CHF) |       | cost of      | trip (CHF) |
|          | β car         | (0/1)         |       | car (0/1)    |            |
1
|     | β travel | time (hours) |     | travel time | (hours) |
| --- | -------- | ------------ | --- | ----------- | ------- |
2
|     | β 3 headway | if train | (min.) | headway | if train (min.) |
| --- | ----------- | -------- | ------ | ------- | --------------- |
5/62

Observed variables
| 1. An indicator | variable | defined as |     |     |
| --------------- | -------- | ---------- | --- | --- |
(cid:12)
|     |     | 1 if individual | n chose alternative | i,  |
| --- | --- | --------------- | ------------------- | --- |
y =
|                | in           | 0 if individual | n chose alternative | j.  |
| -------------- | ------------ | --------------- | ------------------- | --- |
| For notational | convenience, | we also         | define y = 1−y      | .   |
|                |              |                 | jn                  | in  |
2. Two vectors of explanatory variables z and z , each containing K = 4
in jn
values.
6/62

Example: raw data
|       |         |          | Individual | 1 Individual | 2 Individual | 3     |
| ----- | ------- | -------- | ---------- | ------------ | ------------ | ----- |
|       | Train   | cost     |            | 40.00        | 7.80         | 40.00 |
|       |         | Car cost |            | 5.00         | 8.33         | 3.20  |
| Train | travel  | time     |            | 2.50         | 1.75         | 2.67  |
| Car   | travel  | time     |            | 1.17         | 2.00         | 2.55  |
|       | Headway |          |            | 60           | 60           | 30    |
|       |         | Choice   |            | Car          | Train        | Train |
7/62

| Example:  |              | formatted    | data         |         |                  |     |
| --------- | ------------ | ------------ | ------------ | ------- | ---------------- | --- |
| Unlabeled |              | alternatives |              |         |                  |     |
|           | n            | cost car     | time headway | cost    | car time headway |     |
|           |              | in in        | in           | in jn   | jn jn            | jn  |
|           | 1            | 5 1          | 1.17         | 0 40    | 0 2.5            | 60  |
|           | 2            | 7.8 0        | 1.75         | 60 8.33 | 1 2              | 0   |
|           | 3            | 40 0         | 2.67         | 30 3.2  | 1 2.55           | 0   |
| Chosen    | alternative: | i.           |              |         |                  |     |
8/62

| Example: | observed | variables |           |        |        |
| -------- | -------- | --------- | --------- | ------ | ------ |
|          |          | y = y     | = y = 1,y | = y =  | y = 0. |
|          |          | i1 i2     | i3        | j1 j2  | j3     |
|          |          | z =       | (5 1      | 1.17 0 | )T     |
i1
|     |     | z = | (40 0 | 2.5 60 | )T  |
| --- | --- | --- | ----- | ------ | --- |
j1
|     |     | z = | (7.8 0 | 1.75 60 | )T  |
| --- | --- | --- | ------ | ------- | --- |
i2
)T
|     |     | z = | (8.33 1 | 2 0 |     |
| --- | --- | --- | ------- | --- | --- |
j2
)T
|     |     | z = | (40 0 | 2.67 30 |     |
| --- | --- | --- | ----- | ------- | --- |
i3
|     |     | z = | (3.2 1 | 2.55 0 | )T  |
| --- | --- | --- | ------ | ------ | --- |
j3
9/62

Choice model
|     |   |     |
| --- | --- | --- |
−1
β
|     |  car  |     |
| --- | ------- | --- |
| β   | =     |     |
β
|     |  time  |     |
| --- | -------- | --- |
β
headway
eµβTzin
| P (i;β,µ) | =   | .   |
| --------- | --- | --- |
n
eµβTzin +eµβTzjn
Likelihood
For fixed observed data, the likelihood is the joint probability that the model
assigns to the observed choices, considered as a function of the unknown
parameters.
10/62

| Example: | likelihood |     |     |     |     |     |     |
| -------- | ---------- | --- | --- | --- | --- | --- | --- |
Individuals
▶
| Each | individual |     | n has | chosen | alternative | i.  |     |
| ---- | ---------- | --- | ----- | ------ | ----------- | --- | --- |
▶
| The | model | assigns |     | probability | P (i;β,µ) | to  | this outcome. |
| --- | ----- | ------- | --- | ----------- | --------- | --- | ------------- |
n
▶
| Assume |     | independence |     | of the | error | terms across | n.  |
| ------ | --- | ------------ | --- | ------ | ----- | ------------ | --- |
Likelihood
|         |        |     | L∗(β,µ) | =    | P (i;β,µ)P | (i;β,µ)P | (i;β,µ). |
| ------- | ------ | --- | ------- | ---- | ---------- | -------- | -------- |
|         |        |     |         |      | 1          | 2        | 3        |
| where β | ∈ RK=4 | and | µ       | > 0. |            |          |          |
11/62

Example: likelihood
Assume that
|     |    |    |     |     |
| --- | --- | --- | --- | --- |
−1
0
|     |    |       | 10−8, |     |
| --- | --- | ------ | ----- | --- |
| β = |    | , µ = |       |     |
0
|     |    |    |     |     |
| --- | --- | --- | --- | --- |
0
we have
| n V     |        | V P (i) | P (j) |     |
| ------- | ------ | ------- | ----- | --- |
|         | in     | jn n    | n     |     |
| 1 -5.0  | -40.00 | 0.5     | 0.5   |     |
| 2 -7.8  | -8.33  | 0.5     | 0.5   |     |
| 3 -40.0 | -3.20  | 0.5     | 0.5   |     |
L∗
| = 0.5 | · 0.5 | · 0.5 = | 0.125. | (1) |
| ----- | ----- | ------- | ------ | --- |
12/62

Example: likelihood
Assume that
|     |    |    |     |
| --- | --- | --- | --- |
−1
−1
|     |    |       |     |
| --- | --- | ------ | --- |
| β   | =  | , µ = | 0.1 |
−15
|     |    |    |     |
| --- | --- | --- | --- |
−0.3
we have
| n          | V V     | P (i)   | P (j)      |
| ---------- | ------- | ------- | ---------- |
|            | in      | jn n    | n          |
| 1 -23.55   | -95.50  | 0.999   | 0.001      |
| 2 -52.05   | -39.33  | 0.219   | 0.781      |
| 3 -89.05   | -42.45  | 0.009   | 0.991      |
| L∗ = 0.999 | · 0.219 | · 0.009 | = 0.00197. |
13/62

Example: likelihood
Assume that
 
−1
−20
 
| β = |    | , µ = | 0.04 |
| --- | --- | ------ | ---- |
−20
 
−0.1
we have
| n          | V V     | P (i)   | P (j)    |
| ---------- | ------- | ------- | -------- |
|            | in jn   | n       | n        |
| 1 -48.40   | -96.00  | 0.807   | 0.193    |
| 2 -48.80   | -68.33  | 0.642   | 0.358    |
| 3 -96.40   | -74.20  | 0.339   | 0.661    |
| L∗ = 0.807 | · 0.642 | · 0.339 | = 0.176. |
14/62

Definitions
Likelihood
(cid:89)N
L∗(β,µ)
|     |     | = P (i;β,µ)yinP | (j;β,µ)yjn, |
| --- | --- | --------------- | ----------- |
n n
n=1
| where β | ∈ RK and | µ > 0. |     |
| ------- | -------- | ------ | --- |
Log likelihood
(cid:88)N
|     | L(β,µ) | = (y lnP (i;β,µ)+y | lnP (j;β,µ)). |
| --- | ------ | ------------------ | ------------- |
in n jn n
n=1
15/62

| Maximum      | likelihood      | estimation |        |                 |      |
| ------------ | --------------- | ---------- | ------ | --------------- | ---- |
| Optimization | problem         |            |        |                 |      |
|              | β(cid:98),µ =   |            | L(β,µ) | = L(β ,β ,...,β | ,µ). |
|              | (cid:98) argmax | β∈RK,µ>0   |        |                 |      |
|              |                 |            |        | 1 2             | K    |
Software
biogeme.epfl.ch
16/62

| Estimation | of the parameters |     |               |     |
| ---------- | ----------------- | --- | ------------- | --- |
| Unknown    | parameters        |     |               |     |
|            |                   | µ,β | ,k = 1,...,K. |     |
k
| Contribution | to the | likelihood | of observation | n   |
| ------------ | ------ | ---------- | -------------- | --- |
(cid:80)
|               |              |            | e−µcostin+ µβ    | k z ink    |
| ------------- | ------------ | ---------- | ---------------- | ---------- |
|               | (i|C)        |            | k                |            |
|               | P =          |            | (cid:80)         | (cid:80) . |
|               | n            | e−µcostin+ | µβ z +e−µcostjn+ | µβ z       |
|               |              |            | k k ink          | k k jnk    |
| Issue: non    | linearity    |            |                  |            |
| ▶ Non-concave | formulation. |            |                  |            |
▶
| Algorithms  | may converge | to            | local maxima. |     |
| ----------- | ------------ | ------------- | ------------- | --- |
| ▶ A concave | formulation  | is desirable. |               |     |
17/62

| Estimation of | the parameters |         |          |          |     |
| ------------- | -------------- | ------- | -------- | -------- | --- |
| Rename the    | parameters     |         |          |          |     |
|               |                | β′ = −µ | and β′ = | µβ , ∀k. |     |
|               |                | c       | k        | k        |     |
(cid:80)
|     |         |               | eβ ′costin+   | β ′z       |           |
| --- | ------- | ------------- | ------------- | ---------- | --------- |
|     |         |               | c             | k k ink    |           |
|     | P (i|C) | =             | (cid:80)      | (cid:80)   | .         |
|     | n       |               | ′z            |            | ′z        |
|     |         | eβ c ′costin+ | k β k ink +eβ | c ′costjn+ | k β k ink |
Notes
▶
It is equivalent to the original specification, if µ is normalized to 1.
▶ Logit with this specification has a concave log-likelihood function.
▶
Once the parameters are estimated, the inverse transform must be applied
| to obtain | the willingness | to  | pay parameters |      |     |
| --------- | --------------- | --- | -------------- | ---- | --- |
|           |                 |     | β′             | β′   |     |
|           |                 |     | β = t =        | − t. |     |
t
|     |     |     | µ   | β′  |     |
| --- | --- | --- | --- | --- | --- |
c 18/62

| Moneymetric  | specification |          |         |       |
| ------------ | ------------- | -------- | ------- | ----- |
| Unnormalized | version:      | includes | all β’s | and µ |
(cid:88)
|     |     | µV = µβ | cost + | µβ z . |
| --- | --- | ------- | ------ | ------ |
|     |     | in      | c in   | k ink  |
k
| Normalization: | β   | = −1 |     |     |
| -------------- | --- | ---- | --- | --- |
c
(cid:88)
|     |     | µV = | −µcost + | µβ z . |
| --- | --- | ---- | -------- | ------ |
|     |     | in   | in       | k ink  |
k
19/62

| Moneymetric specification |     |     |     |     |     |     |
| ------------------------- | --- | --- | --- | --- | --- | --- |
| Normalization:            | β = | −1  |     |     |     |     |
c
(cid:88)
|     |     | µV = −µcost | +   | µβ z  | .   |     |
| --- | --- | ----------- | --- | ----- | --- | --- |
|     |     | in          | in  | k ink |     |     |
k
| Advantages |     |     | Drawbacks |     |     |     |
| ---------- | --- | --- | --------- | --- | --- | --- |
▶
| ▶                    |       |     |     | Not linear       | in the | parameters.  |
| -------------------- | ----- | --- | --- | ---------------- | ------ | ------------ |
| Convenient           | unit. |     |     |                  |        |              |
| ▶                    |       |     |     | ▶                |        |              |
| Easy interpretation. |       |     |     | More complicated |        | to estimate. |
▶
| ▶                       |      |             |     | Possibility | to be | caught in local |
| ----------------------- | ---- | ----------- | --- | ----------- | ----- | --------------- |
| Explicit representation |      | of µ.       |     |             |       |                 |
| ▶                       |      |             |     | maxima.     |       |                 |
| Scale can vary          | with | n: µ (s ;µ) |     |             |       |                 |
n n
20/62

| Linear-in-parameters |          | specification |         |       |
| -------------------- | -------- | ------------- | ------- | ----- |
| Unnormalized         | version: | includes      | all β’s | and µ |
(cid:88)
|     |     | µV = µβ | cost + | µβ z . |
| --- | --- | ------- | ------ | ------ |
|     |     | in      | c in   | k ink  |
k
| Normalization: | µ = | 1   |     |     |
| -------------- | --- | --- | --- | --- |
(cid:88)
|     |     | µV = | β cost + | β z . |
| --- | --- | ---- | -------- | ----- |
|     |     | in   | c in     | k ink |
k
21/62

| Linear-in-parameters |     | specification |     |     |     |     |
| -------------------- | --- | ------------- | --- | --- | --- | --- |
| Normalization:       |     | µ = 1         |     |     |     |     |
(cid:88)
|     |     | µV = | V = β cost | + β  | z . |     |
| --- | --- | ---- | ---------- | ---- | --- | --- |
|     |     | in   | in c       | in k | ink |     |
k
| Advantages |        |             |     | Drawbacks   |     |     |
| ---------- | ------ | ----------- | --- | ----------- | --- | --- |
| ▶          |        |             |     | ▶ Unitless. |     |     |
| Linear     | in the | parameters. |     |             |     |     |
▶
| ▶ Simple | to estimate.   |     |     | Coefficients | difficult to |     |
| -------- | -------------- | --- | --- | ------------ | ------------ | --- |
| ▶        |                |     |     | interpret.   |              |     |
| With     | logit, concave |     |     |              |              |     |
▶
|                |     |           |     | No explicit | representation | of µ. |
| -------------- | --- | --------- | --- | ----------- | -------------- | ----- |
| log-likelihood |     | function. |     |             |                |       |
▶
|     |     |     |     | Scale | µ the same for all |     |
| --- | --- | --- | --- | ----- | ------------------ | --- |
individuals.
22/62

| Linear-in-parameters | normalization |     |     |
| -------------------- | ------------- | --- | --- |
Heteroscedasticity
▶
| What | if µ varies across | individuals? |     |
| ---- | ------------------ | ------------ | --- |
n
▶
| In practice, | there is a | scale parameter | for each segment. |
| ------------ | ---------- | --------------- | ----------------- |
▶
Normalization: select one segment, and normalize the corresponding scale
| parameter  | to 1.                |     |                     |
| ---------- | -------------------- | --- | ------------------- |
| ▶ Estimate | the scale parameters | for | the other segments. |
▶
| Consequence: | not linear-in-parameters |     | anymore. |
| ------------ | ------------------------ | --- | -------- |
23/62

Normalization
Notes
▶
The choice of a specific normalization is arbitrary, as both lead to the exact
same choice model.
▶
The linear-in-parameters normalization has been widely adopted in the
literature, for historical reasons.
▶
The moneymetric normalization provides a better interpretation.
▶
Warning: if some parameters are assumed to be distributed (see the lecture
on mixtures), the choice of the distribution is conditional on the type of
normalization.
24/62

| Comparison |            | with | linear | regression |     |       |     |     |
| ---------- | ---------- | ---- | ------ | ---------- | --- | ----- | --- | --- |
| Linear     | regression |      |        | Choice     |     | model |     |     |
(cid:88)
(cid:88)
|     |            |     |        |     |     | U =        | β   | z +ε   |
| --- | ---------- | --- | ------ | --- | --- | ---------- | --- | ------ |
|     | y          | =   | β z +ε |     |     | in         | k   | ink in |
|     |            | n   | k nk   | n   |     |            |     |        |
|     |            |     | k      |     |     |            | k   |        |
|     | ▶ ∼        |     |        |     | ▶ ε | ∼ EV(η,µ). |     |        |
|     | ε N(η,σ2). |     |        |     | in  |            |     |        |
n
▶
|     | ▶ ε independent |     | from z. |     | ε   | independent | from | z.  |
| --- | --------------- | --- | ------- | --- | --- | ----------- | ---- | --- |
|     | n               |     |         |     | in  |             |      |     |
▶
|     | ▶              |     |     |     | U   | is latent, | not | observed. |
| --- | -------------- | --- | --- | --- | --- | ---------- | --- | --------- |
|     | y is observed. |     |     |     | in  |            |     |           |
n
▶
▶ All parameters are potentially Location: η does not play any role.
▶
|     | identified | if  | data allows. |     | Units: | normalization |     | is needed. |
| --- | ---------- | --- | ------------ | --- | ------ | ------------- | --- | ---------- |
25/62

Outline
Estimation of the parameters
Example
Output of the estimation
26/62

| Example: |     | interurban | mode | choice | in  | Switzerland |
| -------- | --- | ---------- | ---- | ------ | --- | ----------- |
Sample
▶
|     | Revealed | preference | data.   |          |      |              |
| --- | -------- | ---------- | ------- | -------- | ---- | ------------ |
|     | ▶ Survey | conducted  | between | 2009 and | 2010 | for PostBus. |
▶
|     | Questionnaires |     | sent to people | living | in rural | areas. |
| --- | -------------- | --- | -------------- | ------ | -------- | ------ |
▶ Each observation corresponds to a tour, a sequence of trips from home to
home.
▶
|        | Sample | size:          | 1899 tours. |     |     |     |
| ------ | ------ | -------------- | ----------- | --- | --- | --- |
| Model: |        | 3 alternatives |             |     |     |     |
▶
Car,
|     | ▶ public | transportation | (PT), |     |     |     |
| --- | -------- | -------------- | ----- | --- | --- | --- |
▶
slow modes.
27/62

Attributes
Travel cost
| ▶ Alternatives: | car and public | transportation. |
| --------------- | -------------- | --------------- |
▶
| Units: CHF. |     |     |
| ----------- | --- | --- |
▶
| Coefficient: | generic. |     |
| ------------ | -------- | --- |
Travel time
| ▶ Alternatives: | car and public | transportation. |
| --------------- | -------------- | --------------- |
▶
| Units: minutes. |     |     |
| --------------- | --- | --- |
▶ Coefficient: alternative specific, interacted with trip purpose.
28/62

Attributes
Waiting time
▶
| Alternative: | public | transportation. |     |
| ------------ | ------ | --------------- | --- |
▶
Units: minutes.
▶
| Coefficient: | interacted | with socio-professional | category. |
| ------------ | ---------- | ----------------------- | --------- |
Distance
▶
| Alternative: | slow mode. |     |     |
| ------------ | ---------- | --- | --- |
▶
Units: kilometers.
▶
| Coefficient: | interaction | with age. |     |
| ------------ | ----------- | --------- | --- |
29/62

| Parameters      | of       | the error | terms                  |     |     |
| --------------- | -------- | --------- | ---------------------- | --- | --- |
| Alternative     | specific | constants |                        |     |     |
| ▶ Alternatives: |          | car and   | public transportation. |     |     |
▶
| Units: | none | (0/1 indicator). |     |     |     |
| ------ | ---- | ---------------- | --- | --- | --- |
▶ Coefficient: interacted with public transportation subscription (GA) and
language region.
| Scale      | parameter |                       |     |              |       |
| ---------- | --------- | --------------------- | --- | ------------ | ----- |
| Interacted | with      | public transportation |     | subscription | (GA). |
30/62

Utility functions
Public transportation
|     | µ   | V    | = µ (asc |      | +β  | tc   | +β tt       | +β wt ), |
| --- | --- | ---- | -------- | ---- | --- | ---- | ----------- | -------- |
|     | n   | pt,n | n        | pt,n | c   | pt,n | t,pt,n pt,n | w,n n    |
where
| asc    | =asc | +asc          |       | 1(n ∈            | GA)+asc          |         | 1(n ∈     | german),        |
| ------ | ---- | ------------- | ----- | ---------------- | ---------------- | ------- | --------- | --------------- |
| pt,n   | pt   |               | pt,GA |                  |                  |         | pt,german |                 |
| µ      | =µ   | 1(n ∈         | GA)+µ |                  | 1(n              | ̸∈ GA), |           |                 |
| n      | GA   |               |       | noGA             |                  |         |           |                 |
| β      | =β   | +β            |       | 1(n              | ∈ non            | work),  |           |                 |
| t,pt,n | t,pt | t,pt,nonwork  |       |                  |                  |         |           |                 |
| β      | =β   | +β            |       | 1(n              | ∈ craftperson)+β |         |           | 1(n ∈ manager)+ |
| w,n    | w    | w,craftperson |       |                  |                  |         | w,manager |                 |
|        | β    |               | 1(n   | ∈ intellectual). |                  |         |           |                 |
w,intellectual
31/62

Utility functions
Car
|     | µ   | V     | = µ | (asc  | +β tc | +β            | tt ), |
| --- | --- | ----- | --- | ----- | ----- | ------------- | ----- |
|     | n   | car,n | n   | car,n | c     | car,n t,car,n | car,n |
where
| asc     | =asc | +asc  |               | 1(n  | ∈ GA)+asc |            | 1(n ∈ german), |
| ------- | ---- | ----- | ------------- | ---- | --------- | ---------- | -------------- |
| car,n   |      | car   | car,GA        |      |           | car,german |                |
| µ       | =µ   | 1(n   | ∈ GA)+µ       |      | 1(n       | ̸∈ GA),    |                |
|         | n GA |       |               | noGA |           |            |                |
| β       | =β   | +β    |               | 1(n  | ∈ non     | work),     |                |
| t,car,n |      | t,car | t,car,nonwork |      |           |            |                |
32/62

Utility functions
Slow modes
|     | µ V    | = µ (β distance | ),  |
| --- | ------ | --------------- | --- |
|     | n sm,n | n d,n           | n   |
where
| µ   | =µ 1(n | ∈ GA)+µ   | 1(n ̸∈ GA), |
| --- | ------ | --------- | ----------- |
|     | n GA   | noGA      |             |
| β   | =β +β  | 1(n ∈ age | < 65).      |
| d,n | d      | d,young   |             |
33/62

Parameters
19 parameters
asc β
pt w,craftperson
asc β
pt,GA w,manager
asc β
pt,german w,intellectual
asc β
car t,car
asc β
car,GA t,car,nonwork
asc β
car,german d
β β
c d,young
β µ
t,pt GA
β µ
t,pt,nonwork noGA
β
w
Normalizations: moneymetric: β = −1, linear-in-parameters: µ = 1.
c noGA
34/62

| Estimation     | results       |                    |             |           |
| -------------- | ------------- | ------------------ | ----------- | --------- |
| General        | statistics    |                    |             |           |
|                |               |                    | Moneymetric | Linear    |
| Number         | of estimated  | parameters         | 18          | 18        |
| Sample         | size          |                    | 1899        | 1899      |
| Null log       | likelihood    |                    | -2046.529   | -2046.529 |
| Final log      | likelihood    |                    | -1066.542   | -1066.542 |
| Likelihood     | ratio test    | for the null model | 1959.975    | 1959.975  |
| Rho-square     | for the       | null model         | 0.479       | 0.479     |
| Rho-square-bar | for           | the null model     | 0.47        | 0.47      |
| Akaike         | Information   | Criterion          | 2169.083    | 2169.083  |
| Bayesian       | Information   | Criterion          | 2268.967    | 2268.967  |
| Number         | of iterations |                    | 110         | 37        |
35/62

| Estimation | results: | moneymetric |     |     |
| ---------- | -------- | ----------- | --- | --- |
Robust
|     | Parameter                         |     | Coeff. Asympt.     |                |
| --- | --------------------------------- | --- | ------------------ | -------------- |
|     | number Description                |     | estimate std.error | t-stat p-value |
|     | 1 Ctereference(car)               |     | 41.4 17.3          | 2.4 0.0166     |
|     | 2 Ctediff.yearlysubscription(car) |     | -35.3 16.6         | -2.13 0.0335   |
|     | 3 Ctediff.Germanspeaking(car)     |     | -29.5 11.8         | -2.5 0.0126    |
|     | 4 Cte.reference(PT)               |     | -21.9 14.4         | -1.51 0.13     |
|     | 5 Ctediff.yearlysubscription(PT)  |     | 6.57 13.1          | 0.5 0.617      |
|     | 6 Ctediff.Germanspeaking(PT)      |     | 6.24 9.61          | 0.649 0.516    |
|     | 7 Cost[CHF]                       |     | -1.0               |                |
|     | 8 Traveltimereference(car)[min.]  |     | -1.28 0.382        | -3.34 0.000841 |
9 Traveltimediff.othertrippurposes(car)[min.] 0.653 0.35 1.87 0.0618
|     | 10 Traveltimereference(PT)[min.] |     | -0.328 0.136 | -2.41 0.016 |
| --- | -------------------------------- | --- | ------------ | ----------- |
11 Traveltimediff.othertrippurposes(PT)[min.] 0.148 0.124 1.19 0.235
|     | 12 Waitingtimereference[min.]         |     | -0.837 0.35    | -2.39 0.0168  |
| --- | ------------------------------------- | --- | -------------- | ------------- |
|     | 13 Waitingtimediff.craftperson[min.]  |     | 0.638 0.392    | 1.62 0.104    |
|     | 14 Waitingtimediff.intellectual[min.] |     | 0.601 0.457    | 1.32 0.188    |
|     | 15 Waitingtimediff.manager[min.]      |     | -1.25 0.55     | -2.26 0.0236  |
|     | 16 Distancereference[km]              |     | -11.3 4.19     | -2.7 0.00684  |
|     | 17 Distancediff.age<65[km]            |     | 4.68 2.91      | 1.61 0.108    |
|     | 18 Scale(noyearlysubscription)        |     | 0.0319 0.00894 | 3.56 0.000367 |
|     | 19 Scale(yearlysubscription)          |     | 0.0498 0.0201  | 2.47 0.0134   |
36/62

| Estimation | results: | linear-in-parameters |     |     |
| ---------- | -------- | -------------------- | --- | --- |
Robust
|     | Parameter                         |     | Coeff. Asympt.     |                |
| --- | --------------------------------- | --- | ------------------ | -------------- |
|     | number Description                |     | estimate std.error | t-stat p-value |
|     | 1 Ctereference(car)               |     | 1.32 0.382         | 3.45 0.000561  |
|     | 2 Ctediff.yearlysubscription(car) |     | -1.13 0.375        | -3.0 0.00268   |
|     | 3 Ctediff.Germanspeaking(car)     |     | -0.94 0.272        | -3.46 0.00054  |
|     | 4 Cte.reference(PT)               |     | -0.697 0.406       | -1.72 0.0862   |
|     | 5 Ctediff.yearlysubscription(PT)  |     | 0.209 0.411        | 0.509 0.611    |
|     | 6 Ctediff.Germanspeaking(PT)      |     | 0.199 0.3          | 0.662 0.508    |
|     | 7 Cost[CHF]                       |     | -0.0319 0.00894    | -3.56 0.000369 |
8 Traveltimereference(car)[min.] -0.0407 0.00777 -5.24 1.63e-07
9 Traveltimediff.othertrippurposes(car)[min.] 0.0208 0.00844 2.46 0.0137
10 Traveltimereference(PT)[min.] -0.0104 0.00379 -2.76 0.00583
11 Traveltimediff.othertrippurposes(PT)[min.] 0.0047 0.00352 1.34 0.181
|     | 12 Waitingtimereference[min.] |     | -0.0267 0.00843 | -3.16 0.00156 |
| --- | ----------------------------- | --- | --------------- | ------------- |
13 Waitingtimediff.craftperson[min.] 0.0203 0.0114 1.78 0.0744
14 Waitingtimediff.intellectual[min.] 0.0192 0.014 1.37 0.171
15 Waitingtimediff.manager[min.] -0.0397 0.0146 -2.72 0.00656
|     | 16 Distancereference[km]       |     | -0.361 0.1   | -3.6 0.000317 |
| --- | ------------------------------ | --- | ------------ | ------------- |
|     | 17 Distancediff.age<65[km]     |     | 0.149 0.0841 | 1.77 0.0764   |
|     | 18 Scale(noyearlysubscription) |     | 1.0          |               |
|     | 19 Scale(yearlysubscription)   |     | 1.56 0.525   | 2.98 0.0029   |
37/62

Estimation results: comparison
Parameter Description Moneymetric Linearinparameters
1 Ctereference(car) 41.4 1.32
2 Ctediff.yearlysubscription(car) -35.3 -1.13
3 Ctediff.Germanspeaking(car) -29.5 -0.94
4 Cte.reference(PT) -21.9 -0.697
5 Ctediff.yearlysubscription(PT) 6.57 0.209
6 Ctediff.Germanspeaking(PT) 6.24 0.199
7 Cost[CHF] -1.0 -0.0319
8 Traveltimereference(car)[min.] -1.28 -0.0407
9 Traveltimediff.othertrippurposes(car)[min.] 0.653 0.0208
10 Traveltimereference(PT)[min.] -0.328 -0.0104
11 Traveltimediff.othertrippurposes(PT)[min.] 0.148 0.0047
12 Waitingtimereference[min.] -0.837 -0.0267
13 Waitingtimediff.craftperson[min.] 0.638 0.0203
14 Waitingtimediff.intellectual[min.] 0.601 0.0192
15 Waitingtimediff.manager[min.] -1.25 -0.0397
16 Distancereference[km] -11.3 -0.361
17 Distancediff.age<65[km] 4.68 0.149
18 Scale(noyearlysubscription) 0.0319 1.0
19 Scale(yearlysubscription) 0.0498 1.56
38/62

| Estimation | results: | moneymetric |     |     |
| ---------- | -------- | ----------- | --- | --- |
β = −0.0319
c
Robust
|     | Parameter                         |     | Coeff. Asympt.     |                |
| --- | --------------------------------- | --- | ------------------ | -------------- |
|     | number Description                |     | estimate std.error | t-stat p-value |
|     | 1 Ctereference(car)               |     | 1.32 0.551         | 2.4 0.0166     |
|     | 2 Ctediff.yearlysubscription(car) |     | -1.13 0.53         | -2.13 0.0335   |
|     | 3 Ctediff.Germanspeaking(car)     |     | -0.941 0.377       | -2.5 0.0126    |
|     | 4 Cte.reference(PT)               |     | -0.697 0.461       | -1.51 0.13     |
|     | 5 Ctediff.yearlysubscription(PT)  |     | 0.209 0.419        | 0.499 0.617    |
|     | 6 Ctediff.Germanspeaking(PT)      |     | 0.199 0.306        | 0.649 0.516    |
|     | 7 Cost[CHF]                       |     | -0.0319            |                |
8 Traveltimereference(car)[min.] -0.0407 0.0122 -3.34 0.000841
9 Traveltimediff.othertrippurposes(car)[min.] 0.0208 0.0112 1.87 0.0618
|     | 10 Traveltimereference(PT)[min.] |     | -0.0105 0.00434 | -2.41 0.016 |
| --- | -------------------------------- | --- | --------------- | ----------- |
11 Traveltimediff.othertrippurposes(PT)[min.] 0.00471 0.00396 1.19 0.235
|     | 12 Waitingtimereference[min.] |     | -0.0267 0.0112 | -2.39 0.0168 |
| --- | ----------------------------- | --- | -------------- | ------------ |
13 Waitingtimediff.craftperson[min.] 0.0203 0.0125 1.62 0.104
14 Waitingtimediff.intellectual[min.] 0.0192 0.0146 1.32 0.188
|     | 15 Waitingtimediff.manager[min.] |     | -0.0398 0.0176 | -2.26 0.0236  |
| --- | -------------------------------- | --- | -------------- | ------------- |
|     | 16 Distancereference[km]         |     | -0.362 0.134   | -2.7 0.00684  |
|     | 17 Distancediff.age<65[km]       |     | 0.149 0.093    | 1.61 0.108    |
|     | 18 Scale(noyearlysubscription)   |     | 0.999 0.28     | 3.56 0.000368 |
|     | 19 Scale(yearlysubscription)     |     | 1.56 0.631     | 2.47 0.0134   |
39/62

Comments
| Moneymetric | vs. linear-in-parameters |     |
| ----------- | ------------------------ | --- |
▶ The two parameterizations produce identical choice probabilities and the
| same maximum | log likelihood. |     |
| ------------ | --------------- | --- |
▶
Their point estimates are related by a one-to-one transformation, up to
| numerical | precision. |     |
| --------- | ---------- | --- |
▶
Each table reports standard errors calculated directly by the estimation
| software | for the corresponding | parameterization. |
| -------- | --------------------- | ----------------- |
▶
t-statistics and p-values are not necessarily invariant to a nonlinear
| reparameterization | in finite | samples. |
| ------------------ | --------- | -------- |
▶
The moneymetric parameterization is more challenging for the optimization
| algorithm | in this example. |     |
| --------- | ---------------- | --- |
40/62

| Alternative | specific |       | constants: |       | moneymetric |         |        | model  |
| ----------- | -------- | ----- | ---------- | ----- | ----------- | ------- | ------ | ------ |
| Car vs.     | Slow     | modes |            |       |             |         |        |        |
|             |          | GA    | German     |       | Value       |         |        |        |
|             |          | No    |            | No    | 41.4        |         |        |        |
|             |          | No    |            | Yes   | 11.9        | = 41.4  | - 29.5 |        |
|             |          | Yes   |            | No    | 6.1         | = 41.4  | - 35.3 |        |
|             |          | Yes   |            | Yes   | -23.4       | = 41.4  | - 29.5 | - 35.3 |
| Public      | transp.  | vs.   | Slow       | modes |             |         |        |        |
|             |          | GA    | German     |       | Value       |         |        |        |
|             |          | No    |            | No    | -21.9       |         |        |        |
|             |          | No    | Yes        |       | -15.66      | = -21.9 | + 6.24 |        |
|             |          | Yes   |            | No    | -15.33      | = -21.9 | + 6.57 |        |
|             |          | Yes   | Yes        |       | -9.09       | = -21.9 | + 6.24 | + 6.57 |
41/62

| Travel time | coefficient |     |     |
| ----------- | ----------- | --- | --- |
Car
▶
| Trip purpose | work: -1.28.   |         |           |
| ------------ | -------------- | ------- | --------- |
| ▶ Other trip | purpose: -1.28 | + 0.653 | = -0.627. |
Public transportation
▶
| Trip purpose | work: -0.328.   |         |          |
| ------------ | --------------- | ------- | -------- |
| ▶ Other trip | purpose: -0.328 | + 0.148 | = -0.18. |
42/62

Waiting time coefficient
▶
Craftperson: -0.837+0.638=-0.199.
▶
Intellectual: -0.837+0.601=-0.236.
▶
Manager: -0.837-1.25=-2.087.
▶
Others: -0.837.
43/62

Distance coefficient
▶
| Less than | 65: -11.3 | + 4.68 = -6.62. |
| --------- | --------- | --------------- |
▶
| 65 or more: | -11.3. |     |
| ----------- | ------ | --- |
44/62

Outline
Estimation of the parameters
Example
Output of the estimation
45/62

Output of the estimation
Main outputs
▶
the parameter estimates β(cid:98),
▶ the value of the log likelihood function at the parameter estimates L(β(cid:98)).
Other output
▶
variance-covariance matrix of the estimates,
▶
standard errors,
▶
t-statistics,
▶
p-values,
▶
goodness of fit.
46/62

| Variance-covariance: |     |     | Cramer–Rao |     | bound |     |     |
| -------------------- | --- | --- | ---------- | --- | ----- | --- | --- |
Definition
|     |     |     |         |           | (cid:12) (cid:13)        |     |     |
| --- | --- | --- | ------- | --------- | ------------------------ | --- | --- |
|     |     |     |         |           | (cid:20) ∂2L(β) (cid:21) | −1  |     |
|     |     |     | (cid:2) | (cid:3)−1 |                          |     |     |
|     |     | −E  | ∇2L(β)  | =         | −E                       | .   |     |
∂β∂βT
Estimator
|     |     | (cid:20) | (cid:21) (cid:88)N | (cid:20) |               | (cid:21)    |     |
| --- | --- | -------- | ------------------ | -------- | ------------- | ----------- | --- |
|     |     | ∂2L(β)   |                    | ∂2(y     | lnP (i)+y lnP | (j))        |     |
|     |     |          |                    |          | in n jn       | n           |     |
|     | A = | E        | ≈                  |          |               |             | ,   |
|     |     | ∂β       | ∂β                 |          | ∂β ∂β         |             |     |
|     |     | k        | m                  |          | k m           |             |     |
|     |     |          | n=1                |          |               | β=β(cid:98) |     |
CR −1.
Σ(cid:98) = −A(cid:98)
β
47/62

| Variance-covariance: |        |     | robust   |          | estimator |     |     |     |     |
| -------------------- | ------ | --- | -------- | -------- | --------- | --- | --- | --- | --- |
| BHHH                 | matrix |     |          |          |           |     |     |     |     |
|                      |        |     | (cid:20) | (cid:21) | (cid:88)N |     |     |     |     |
∂2L(β)
(β(cid:98))T
|     |     | −E  |       |     | ≈   | ∇L (β(cid:98))∇L |     | =   | B(cid:98), |
| --- | --- | --- | ----- | --- | --- | ---------------- | --- | --- | ---------- |
|     |     |     | ∂β∂βT |     |     | n                | n   |     |            |
n=1
where
|        |             |               | ∇L (β(cid:98)) | =         | ∇(y            | lnP (i)+y   | lnP                   | (j)). |               |
| ------ | ----------- | ------------- | -------------- | --------- | -------------- | ----------- | --------------------- | ----- | ------------- |
|        |             |               | n              |           | in             | n           | jn                    | n     |               |
| Robust | or sandwich |               | estimator      |           |                |             |                       |       |               |
|        |             | Σ(cid:98) R = | (−A(cid:98))−1 | B(cid:98) | (−A(cid:98))−1 | = Σ(cid:98) | CR (Σ(cid:98) BHHH)−1 |       | Σ(cid:98) CR. |
|        |             | β             |                |           |                |             | β β                   |       | β             |
48/62

| Which variance–covariance |           |            | estimator? |     |
| ------------------------- | --------- | ---------- | ---------- | --- |
| Correctly                 | specified | likelihood |            |     |
▶
The expected negative Hessian and the expected outer product of the score
| vectors | are equal. |     |     |     |
| ------- | ---------- | --- | --- | --- |
▶
The inverse-Hessian and sandwich estimators agree asymptotically.
| If misspecification |                | is a concern |     |     |
| ------------------- | -------------- | ------------ | --- | --- |
| ▶ The               | two estimators | can differ.  |     |     |
▶
| Use | the sandwich | estimator | for robust standard | errors. |
| --- | ------------ | --------- | ------------------- | ------- |
49/62

Standard errors
Definition
(cid:113)
σ = Σ(cid:98) (k,k),
k β
where Σ(cid:98) (k,k) is diagonal element k of the matrix Σ(cid:98) .
β β
50/62

t statistics
Definition
β(cid:98) −β
k 0
t = ,
k
σ
k
where β is the value associated with the null hypothesis (usually 0).
0
Role
Typically used to test the null hypothesis that the true value of a coefficient is
zero. The null hypothesis can be rejected with 95% confidence (that is, at a 5%
significance level) if
|t | ⩾ 1.96.
k
51/62

p values
Definition
▶
It is the probability to get a t statistic at least as large (in absolute value) as
| the one | reported, under | the null hypothesis | that β | = 0. |
| ------- | --------------- | ------------------- | ------ | ---- |
k
▶ Consider an estimate β(cid:98) of the parameter β , and t its t statistic. The p
|          |               | k            | k    | k   |
| -------- | ------------- | ------------ | ---- | --- |
| value is | calculated as |              |      |     |
|          |               | p = 2(1−Φ(|t | |)), |     |
|          |               | k            | k    |     |
where Φ(·) is the cumulative density function of the univariate standard
normal distribution.
Role
▶
| Exact same | role as | the t statistics. |     |     |
| ---------- | ------- | ----------------- | --- | --- |
▶ The null hypothesis can be rejected at the significance level p .
k
52/62

| Goodness    | of fit  |     |     |     |
| ----------- | ------- | --- | --- | --- |
| Preliminary | remarks |     |     |     |
▶
| There  | are several measures |         | of goodness    | of fit. |
| ------ | -------------------- | ------- | -------------- | ------- |
| ▶ None | of them can          | be used | in an absolute | way.    |
▶
They can only be used to compare two models, estimated on the same data
| set, with | the same | dependent | variable. |     |
| --------- | -------- | --------- | --------- | --- |
53/62

| Goodness of | fit |     |
| ----------- | --- | --- |
Log likelihood
L(β(cid:98)).
| Normalized | log likelihood |     |
| ---------- | -------------- | --- |
L(β(cid:98))
ρ2
= 1− .
L(0)
| Comments | on ρ2 |     |
| -------- | ----- | --- |
▶ It is not the square of anything. It mimics R2 in linear regression.
▶ ⩽
| ρ2 1. | ρ2 = 1: perfect | fit. |
| ----- | --------------- | ---- |
▶ But the value is meaningless as such. And ρ2 < 0 is possible.
54/62

| Goodness | of fit:     | accounting | for the | number | of parameters |
| -------- | ----------- | ---------- | ------- | ------ | ------------- |
| Akaike   | Information | Criterion  | (AIC)   |        |               |
2K −2L(β(cid:98)).
| Note:      | the lower,  | the better. |       |                |     |
| ---------- | ----------- | ----------- | ----- | -------------- | --- |
| Normalized | AIC         |             |       |                |     |
|            |             |             | AIC   | L(β(cid:98))−K |     |
|            |             | ρ¯2 = 1+    | =     | 1−             | .   |
|            |             |             | 2L(0) | L(0)           |     |
| Note:      | the higher, | the better. |       |                |     |
55/62

| Goodness | of fit:     | accounting | for sample | size |
| -------- | ----------- | ---------- | ---------- | ---- |
| Bayesian | Information | Criterion  | (BIC)      |      |
ln(N)−2L(β(cid:98)).
K
| Note: | the lower, | the better. |     |     |
| ----- | ---------- | ----------- | --- | --- |
56/62

| Goodness  | of fit: benchmark |                  | models |
| --------- | ----------------- | ---------------- | ------ |
| Benchmark | model             | with 0 parameter |        |
1
P (i) = .
n
J
n
(cid:88)N
|     |     | L(0) | = − log(J ), |
| --- | --- | ---- | ------------ |
n
n=1
| where | N is the number | of observations. |     |
| ----- | --------------- | ---------------- | --- |
57/62

| Goodness  | of fit: | benchmark | models       |     |
| --------- | ------- | --------- | ------------ | --- |
| Benchmark | model   | with J −  | 1 parameters |     |
| We assume | that J  | = J, ∀n:  |              |     |
n
N
i
P (i) = p = .
n i
N
There are J parameters p , ..., p . They must sum up to one, removing one
|        |             | 1   | J   |     |
| ------ | ----------- | --- | --- | --- |
| degree | of freedom. |     |     |     |
(cid:88)J (cid:88)J
|     | L(c) | = N (lnN | −lnN) = N lnN | −N lnN. |
| --- | ---- | -------- | ------------- | ------- |
|     |      | i        | i i           | i       |
i=1 i=1
where N is the number of observations choosing alternative i.
i
58/62

| Likelihood-ratio | test: | setup |     |     |     |
| ---------------- | ----- | ----- | --- | --- | --- |
Nested models
Let
| ▶ L be | the maximized | log likelihood | of  | the restricted | model; |
| ------ | ------------- | -------------- | --- | -------------- | ------ |
R
▶ L
| be  | the maximized | log likelihood | of  | the unrestricted | model; |
| --- | ------------- | -------------- | --- | ---------------- | ------ |
U
| ▶ q be | the number | of independent | restrictions. |     |     |
| ------ | ---------- | -------------- | ------------- | --- | --- |
Null hypothesis
|     |     | H : the | q restrictions | are valid. |     |
| --- | --- | ------- | -------------- | ---------- | --- |
0
59/62

| Likelihood-ratio | test: statistic |     |     |
| ---------------- | --------------- | --- | --- |
Test statistic
|                | −2(L                  | −L 2(L −L |     |
| -------------- | --------------------- | --------- | --- |
|                | LR =                  | ) =       | ).  |
|                |                       | R U U     | R   |
| Reference      | distribution          |           |     |
| Under standard | regularity conditions | and H ,   |     |
0
d
LR →− χ2.
q
60/62

| Likelihood ratio | test |     |     |     |
| ---------------- | ---- | --- | --- | --- |
Statistic
−2(L(0)−L(β(cid:98)))
χ2
| is asymptotically | distributed | as with | K degrees | of freedom. |
| ----------------- | ----------- | ------- | --------- | ----------- |
Statistic
−2(L(c)−L(β(cid:98)))
is asymptotically distributed as χ2 with K −(J −1) degrees of freedom.
61/62

Summary
▶
| Maximum | likelihood estimation. |     |
| ------- | ---------------------- | --- |
▶
| Alternative | normalization:     | µ = 1. |
| ----------- | ------------------ | ------ |
| ▶ Output    | of the estimation. |        |
62/62