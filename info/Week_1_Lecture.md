| Mathematical | Modeling | of Behavior |
| ------------ | -------- | ----------- |
Motivation
Michel Bierlaire
| Mathematical | Modeling | of Behavior |
| ------------ | -------- | ----------- |
1/62

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
2/62

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
3/62

Motivation
Human dimension in
▶
engineering
▶
business
▶
marketing
▶
planning
▶
policy making
4/62

Motivation
| Concept     | of demand   |                   |     |
| ----------- | ----------- | ----------------- | --- |
| Willingness | and ability | to purchase       | a   |
| commodity   | or service  | [Merriam-Webster] |     |
5/62

Applications
Transportation
▶
Choice of destination
▶
Choice of transportation mode
▶
Choice of itinerary
▶
Choice of vehicle
6/62

Applications
Marketing
▶
Choice of packaging
▶
Choice of store
▶
Choice of product
▶
Choice of brand
7/62

Applications
Health
▶
Choice of treatment
▶
Choice of doctor
▶
Choice of training for doctors
8/62

Applications
Energy
▶
Choice of appliances
▶
Choice of energy savings measures
▶
Choice of heating equipment
9/62

Motivation
Need for
▶
| behavioral     | theories |     |
| -------------- | -------- | --- |
| ▶ quantitative | methods  |     |
▶
| operational | mathematical | models |
| ----------- | ------------ | ------ |
10/62

In this course...
Focus
▶ Individual / disaggregate behavior (vs. aggregate behavior)
▶
| Theory | of behavior which | is  |     |
| ------ | ----------------- | --- | --- |
▶
descriptive (how people behave) and not normative (how they should
behave)
| ▶ general: | not too specific |     |     |
| ---------- | ---------------- | --- | --- |
▶
| operational: | can be           | used in practice | for forecasting |
| ------------ | ---------------- | ---------------- | --------------- |
| ▶ Type of    | behavior: choice |                  |                 |
11/62

Case studies
| Mode choice | in the | Netherlands |     |
| ----------- | ------ | ----------- | --- |
▶
| Context:     | car vs rail    | in Nijmegen.   |                    |
| ------------ | -------------- | -------------- | ------------------ |
| ▶ Objective: | sensitivity    | to travel time | and cost, inertia. |
| Mode choice  | in Switzerland |                |                    |
▶
| Context: | Car Postal. |     |     |
| -------- | ----------- | --- | --- |
▶
| Objective: | demand | forecasting. |     |
| ---------- | ------ | ------------ | --- |
12/62

Case studies
Swissmetro
▶
| Context: | new transportation |     | technology. |     |     |
| -------- | ------------------ | --- | ----------- | --- | --- |
▶
| Objective:  | demand    | pattern, | pricing. |     |     |
| ----------- | --------- | -------- | -------- | --- | --- |
| Residential | telephone | services |          |     |     |
▶
| Context: | flat rate | vs. measured. |     |     |     |
| -------- | --------- | ------------- | --- | --- | --- |
▶
| Objective:        | offer the | most | appropriate | service. |     |
| ----------------- | --------- | ---- | ----------- | -------- | --- |
| Airline itinerary | choice    |      |             |          |     |
▶
| Context: | questionnaire | about | itineraries | across | the US. |
| -------- | ------------- | ----- | ----------- | ------ | ------- |
▶ Objective: help airlines and aircraft manufacturer to design a better offer.
13/62

Importance
| Daniel L. | McFadden |     |     |
| --------- | -------- | --- | --- |
▶
| UC Berkeley | 1963, | MIT 1977, | UC Berkeley |
| ----------- | ----- | --------- | ----------- |
1991
| ▶ Laureate | of The Bank | of Sweden | Prize in  |
| ---------- | ----------- | --------- | --------- |
| Economic   | Sciences    | in Memory | of Alfred |
| Nobel      | 2000        |           |           |
▶
| Owns | a farm and vineyard | in  | Napa Valley |
| ---- | ------------------- | --- | ----------- |
▶
| “Farm    | work clears | the mind, and  | the       |
| -------- | ----------- | -------------- | --------- |
| vineyard | is a great  | place to prove | theorems” |
14/62

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
15/62

Simple example
Objectives
| Introduce | basic components | of  | choice modeling: |
| --------- | ---------------- | --- | ---------------- |
▶
| definition | of the | problem |     |
| ---------- | ------ | ------- | --- |
▶ data
▶
| model       | specification |     |     |
| ----------- | ------------- | --- | --- |
| ▶ parameter | estimation    |     |     |
▶
| model | application |     |     |
| ----- | ----------- | --- | --- |
Application
| Analysis | of the market | for electric | cars |
| -------- | ------------- | ------------ | ---- |
16/62

Choice problem
Choice
| Consumer’s | choice to |     |
| ---------- | --------- | --- |
▶
| own an | electric car |     |
| ------ | ------------ | --- |
▶
| own a | car with combustion | engine |
| ----- | ------------------- | ------ |
Research questions
▶
| what is       | the current | market        |
| ------------- | ----------- | ------------- |
| penetration   | of electric | cars relative |
| to combustion | engine      | cars?         |
▶
| how will | the penetration | change in |
| -------- | --------------- | --------- |
the future?
17/62

Data (synthetic)
| Population       |              | Sample           |          |
| ---------------- | ------------ | ---------------- | -------- |
| ▶                |              | ▶                |          |
| adults aged      | 20 and above | 2500 individuals |          |
| ▶ in Switzerland |              | ▶ randomly       | selected |
▶
| owning a | car |     |     |
| -------- | --- | --- | --- |
18/62

Questions
| Is your car | electric? | What  | is your age | range? |
| ----------- | --------- | ----- | ----------- | ------ |
| ▶           |           | ▶     |             |        |
| Yes,        |           | 20–39 |             |        |
| ▶           |           | ▶     |             |        |
| No.         |           | 40–64 |             |        |
▶
65+
19/62

Data
| Contingency | table: Y |     | Notation | (sample) |     |
| ----------- | -------- | --- | -------- | -------- | --- |
▶
|     |     |     | Y   | : number | of  |
| --- | --- | --- | --- | -------- | --- |
ik
|     |     |     | individuals |     | with |
| --- | --- | --- | ----------- | --- | ---- |
Age
|          |             |           | ownership |          | status i and |
| -------- | ----------- | --------- | --------- | -------- | ------------ |
|          | 20–39 40–64 | 65+ Total |           |          |              |
|          |             |           | age       | group    | k.           |
| Electric | 65 55       | 5 125     |           | (cid:80) |              |
▶
| Not electric | 835 1045 | 495 2375 | N     | =           | Y : number |
| ------------ | -------- | -------- | ----- | ----------- | ---------- |
|              |          |          | k     | i           | ik         |
|              | 900 1100 | 500 2500 | of    | individuals | in age     |
|              |          |          | group | k.          |            |
▶
|     |     |     | Y        | = Y      | : number of |
| --- | --- | --- | -------- | -------- | ----------- |
|     |     |     | k        | yes,k    |             |
|     |     |     | electric | vehicles | in age      |
|     |     |     | group    | k.       |             |
(cid:80)
▶
|     |     |     | N   | =   | N . |
| --- | --- | --- | --- | --- | --- |
k
k
20/62

Data
| Contingency | table: Y |     | Market penetration |     |
| ----------- | -------- | --- | ------------------ | --- |
|             |          |     | ▶ In the sample    |     |
|             |          |     | (cid:80) (cid:80)  |     |
Y / N =
|              | Age         |           | k k            | k k         |
| ------------ | ----------- | --------- | -------------- | ----------- |
|              |             |           | 125/2500       | = 5%        |
|              | 20–39 40–64 | 65+ Total |                |             |
|              |             |           | ▶ Currently in | the         |
| Electric     | 65 55       | 5 125     |                |             |
|              |             |           | population:    | by          |
| Not electric | 835 1045    | 495 2375  |                |             |
|              |             |           | inference,     | estimate is |
|              | 900 1100    | 500 2500  |                |             |
5%
▶
|     |     |     | How do we | predict? |
| --- | --- | --- | --------- | -------- |
|     |     |     | We need a | model.   |
21/62

Model
Variables
▶
| i: status | of electric | car ownership | (yes or no) |
| --------- | ----------- | ------------- | ----------- |
▶
| k: age category | (20–39, | 40–64 | or 65+) |
| --------------- | ------- | ----- | ------- |
22/62

Model
| Decomposition: | Bayes’ theorem |                           |
| -------------- | -------------- | ------------------------- |
|                | P(i,k)         | = P(i|k)P(k) = P(k|i)P(i) |
Interpretation
▶
| P(i|k): age | explains electric | car ownership |
| ----------- | ----------------- | ------------- |
▶ P(k|i):
| electric | car ownership | explains age |
| -------- | ------------- | ------------ |
23/62

Model
Model
▶
| Assume | stable causal relationships | between |
| ------ | --------------------------- | ------- |
the variables.
| ▶ Stability | over time necessary | to forecast.  |
| ----------- | ------------------- | ------------- |
| ▶           | P(i|k)              |               |
| Here:       | we select as        | an acceptable |
| behavioral  | model.              |               |
24/62

Model
| Specification |     |     | Parameters |            |     |
| ------------- | --- | --- | ---------- | ---------- | --- |
|               |     |     | ▶ π =      | (π , π , π | )   |
1 2 3
▶
unknown
| P(i = | yes | k = 20–39) | = π , |     |     |     |
| ----- | ---------------- | ----- | --- | --- | --- |
1
|       | |              |       | ▶ must | be estimated | from data |
| ----- | -------------- | ----- | ------ | ------------ | --------- |
| P(i = | yes k = 40–64) | = π , |        |              |           |
2
|
| P(i = | yes k = 65+) | = π . |     |     |     |
| ----- | ------------ | ----- | --- | --- | --- |
3
25/62

Model estimation
Age
|     |     |       |       |                  | 20–39         | 40–64               | 65+ Total     |        |     |
| --- | --- | ----- | ----- | ---------------- | ------------- | ------------------- | ------------- | ------ | --- |
|     |     |       |       | Electric         | 65            | 55                  | 5             | 125    |     |
|     |     |       | Not   | electric         | 835           | 1045                | 495 2375      |        |     |
|     |     |       |       |                  | 900           | 1100                | 500 2500      |        |     |
|     |     |       |       |                  |               |                     | P(cid:98)(i = | yes,k) | Y   |
|     |     |       |       | |                |               | |                   |               |        | k   |
|     | π   | = P(i | = yes | k) ≈ π (cid:98)k | = P(cid:98)(i | = yes               | k) =          |        | = . |
|     | k   |       |       |                  |               |                     |               |        | N   |
|     |     |       |       |                  |               |                     | P(cid:98)(k)  |        | k   |
|     |     |       |       |                  |               | P(cid:98)(i = yes,k | = 20–39)      |        | 65  |
yes|k
| π   | ≈ π         | = P(cid:98)(i | =   | = 20–39) | =   |             |          | =   | = 0.0722. |
| --- | ----------- | ------------- | --- | -------- | --- | ----------- | -------- | --- | --------- |
|     | 1 (cid:98)1 |               |     |          |     |             |          |     | 900       |
|     |             |               |     |          |     | P(cid:98)(k | = 20–39) |     |           |
26/62

Model estimation
Age
|     |     |       |       |          |           | 20–39         | 40–64 | 65+         | Total        |     |     |     |
| --- | --- | ----- | ----- | -------- | --------- | ------------- | ----- | ----------- | ------------ | --- | --- | --- |
|     |     |       |       | Electric |           | 65            |       | 55 5        | 125          |     |     |     |
|     |     |       | Not   | electric |           | 835           | 1045  | 495         | 2375         |     |     |     |
|     |     |       |       |          |           | 900           | 1100  | 500         | 2500         |     |     |     |
|     |     |       |       |          |           |               |       | P(cid:98)(i | = yes,k)     |     | Y   |     |
|     |     |       |       | |        |           |               |       | |           |              |     | k   |     |
|     | π   | = P(i | = yes | k)       | ≈ π       | = P(cid:98)(i | = yes | k) =        |              | =   | .   |     |
|     |     | k     |       |          | (cid:98)k |               |       |             |              |     |     |     |
|     |     |       |       |          |           |               |       |             | P(cid:98)(k) |     | N   |     |
k
|     |     |               |         |     |        | P(cid:98)(i | = yes,k | = 20–39) |     | 65  |           |     |
| --- | --- | ------------- | ------- | --- | ------ | ----------- | ------- | -------- | --- | --- | --------- | --- |
| π   | ≈ π | = P(cid:98)(i | = yes|k | =   | 20–39) | =           |         |          |     | =   | = 0.0722, |     |
1 (cid:98)1
|     |     |     |     |     |     |             | P(cid:98)(k | = 20–39) |     | 900 |     |     |
| --- | --- | --- | --- | --- | --- | ----------- | ----------- | -------- | --- | --- | --- | --- |
|     |     |     |     |     |     | P(cid:98)(i | = yes,k     | = 40–64) |     | 55  |     |     |
yes|k
| π   | ≈ π         | = P(cid:98)(i | =       | =   | 40–64) | =           |             |          |     | =         | = 0.0500, |     |
| --- | ----------- | ------------- | ------- | --- | ------ | ----------- | ----------- | -------- | --- | --------- | --------- | --- |
|     | 2 (cid:98)2 |               |         |     |        |             |             |          |     | 1100      |           |     |
|     |             |               |         |     |        |             | P(cid:98)(k | = 40–64) |     |           |           |     |
|     |             |               |         |     |        | P(cid:98)(i | = yes,k     | = 65+)   |     | 5         |           |     |
| π   | ≈ π         | = P(cid:98)(i | = yes|k | =   | 65+)   | =           |             |          | =   | = 0.0100. |           |     |
3 (cid:98)3
|     |     |     |     |     |     |     | P(cid:98)(k | = 65+) |     | 500 |     | 27/62 |
| --- | --- | --- | --- | --- | --- | --- | ----------- | ------ | --- | --- | --- | ----- |

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
28/62

| Simple | example: | quality | of the estimates |
| ------ | -------- | ------- | ---------------- |
Motivation
| ▶   | We have a | model with | parameters. |
| --- | --------- | ---------- | ----------- |
▶
We have used statistical inference to estimate the value of the parameters.
▶ This is subject to errors, as we have used the sample and not the population.
▶
|     | How accurate | are these | estimates? |
| --- | ------------ | --------- | ---------- |
29/62

Informal checks
▶
|            |           | Do these  | estimates | make sense?  |
| ---------- | --------- | --------- | --------- | ------------ |
| π = 65/900 | = 0.0722, | ▶ Do they | match     | our a priori |
(cid:98)1
| π = 55/1100 | = 0.0500, | expectations? |     |     |
| ----------- | --------- | ------------- | --- | --- |
(cid:98)2
| π = 5/500 | = 0.0100. | ▶     |                   |                 |
| --------- | --------- | ----- | ----------------- | --------------- |
| (cid:98)3 |           | Here: | as age increases, | the market      |
|           |           | share | of electric       | cars decreases. |
30/62

| Quality of the | estimates |     |     |     |
| -------------- | --------- | --- | --- | --- |
▶
| How is | π different from | π ? |     |     |
| ------ | ---------------- | --- | --- | --- |
|        | (cid:98)k        | k   |     |     |
▶
| We have | no access to | π . |     |     |
| ------- | ------------ | --- | --- | --- |
k
▶
| For each | sample, we | would obtain a different | value of | π . |
| -------- | ---------- | ------------------------ | -------- | --- |
(cid:98)k
▶
π is distributed.
(cid:98)k
31/62

Distribution of π
(cid:98)1
50
40
30
20
10
0
2·10−24·10−26·10−28·10−2 0.1
60.0
=
π
1
)2270.0(
etamitse
ruo
π
(cid:98)1
)
π(
f
1(cid:98)
1N
32/62

| Distribution | of π |     |     |     |
| ------------ | ---- | --- | --- | --- |
(cid:98)1
| ▶ Smaller | samples | are associated | with wider | spread. |
| --------- | ------- | -------------- | ---------- | ------- |
▶
| Larger | samples improve | precision. |     |     |
| ------ | --------------- | ---------- | --- | --- |
▶ In practice, impossible to repeat the sampling multiple times.
▶
Distributions derived from theoretical results or simulation.
33/62

Distribution of π
(cid:98)1
50
40
30
20
10
0
2·10−24·10−26·10−28·10−2 0.1
60.0
=
π
1
)2270.0(
etamitse
ruo
π
(cid:98)1
)
π(
f
1(cid:98)
1N
N = 2500 (N = 900)
1
N = 1000 (N = 360)
1
34/62

| Statistical | properties |     |     |     |
| ----------- | ---------- | --- | --- | --- |
▶
If we code yes as 1 and no as 0, we have Bernoulli (0/1) random variables.
| ▶ Variance: | σ2 = π | (1−π ). |     |     |
| ----------- | ------ | ------- | --- | --- |
|             | k      | k       |     |     |
k
▶
| Sample | average: unbiased | estimator. |     |     |
| ------ | ----------------- | ---------- | --- | --- |
(cid:112)
| ▶ Standard | error of | the estimator: | σ2/N . |     |
| ---------- | -------- | -------------- | ------ | --- |
k
k
▶
| Estimated | standard | error: |     |     |
| --------- | -------- | ------ | --- | --- |
(cid:112)
|     |     | s =       | π (1−π )/N          | .   |
| --- | --- | --------- | ------------------- | --- |
|     |     | (cid:98)π | (cid:98)k (cid:98)k | k   |
k
35/62

Bootstrap
Principle
▶
Treat the empirical distribution as if it were the true distribution.
| ▶ Repeatedly | generate | new samples | from the data itself. |
| ------------ | -------- | ----------- | --------------------- |
▶
Recompute the statistic of interest on each resampled dataset.
▶ The variability of these statistics approximates sampling uncertainty.
| Bootstrap | sample for | parameter | π   |
| --------- | ---------- | --------- | --- |
k
▶
| Drawing | N observations, |     |     |
| ------- | --------------- | --- | --- |
k
| ▶ with | replacement, |     |     |
| ------ | ------------ | --- | --- |
▶
| from | the original | N values. |     |
| ---- | ------------ | --------- | --- |
k
Some observations may appear multiple times; others not at all.
36/62

Bootstrap estimator of π
k
▶
For bootstrap replication r = 1,...,R:
1. Draw a bootstrap sample {i ∗(r) ,...,i ∗(r)}.
1 N
k
2. Compute:
(cid:88)N
1 k
∗(r) ∗(r)
π = i .
(cid:98)k
N
n
k
n=1
▶
This produces R bootstrap estimates:
π∗(1),...,π∗(R).
(cid:98)k (cid:98)k
37/62

| Bootstrap | standard | error |     |     |
| --------- | -------- | ----- | --- | --- |
▶
|     | The bootstrap | estimate | of the standard | error is: |
| --- | ------------- | -------- | --------------- | --------- |
(cid:118)
|     |     |           | (cid:117)   | (cid:88)R           |
| --- | --- | --------- | ----------- | ------------------- |
|     |     |           | 1           | (cid:16) (cid:17)2  |
|     |     |           | (cid:117)   | π∗(r)               |
|     |     | sboot     | = (cid:116) | −π∗ ,               |
|     |     | (cid:98)π |             | (cid:98)k (cid:98)k |
|     |     | k         | R −1        |                     |
r=1
where
(cid:88)R
1
|     |     |     | π∗ =      | π∗(r).    |
| --- | --- | --- | --------- | --------- |
|     |     |     | (cid:98)k | (cid:98)k |
R
r=1
|     | ▶ This estimates | the sampling | variability | of π . |
| --- | ---------------- | ------------ | ----------- | ------ |
(cid:98)k
38/62

| Bootstrap | estimator | of π |
| --------- | --------- | ---- |
k
R = 100 R = 10000
39/62

Estimators of s
π
k
Comparison
| Analytical | R = 100 | R = 10000 |
| ---------- | ------- | --------- |
Age
| 1 0.00863 | 0.00974 | 0.00863 |
| --------- | ------- | ------- |
| 2 0.00657 | 0.00695 | 0.00654 |
| 3 0.00445 | 0.00400 | 0.00446 |
40/62

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
41/62

| Simple | example: | maximum |     | likelihood | estimation |
| ------ | -------- | ------- | --- | ---------- | ---------- |
Motivation
|     | ▶ We investigate | another | estimator. |     |     |
| --- | ---------------- | ------- | ---------- | --- | --- |
▶
Indeed, using the sample average is not possible for more complex models.
|     | ▶ Later, | we will use | the maximum | likelihood | estimator. |
| --- | -------- | ----------- | ----------- | ---------- | ---------- |
▶
|     | We remind | the concept | on  | the simple | example. |
| --- | --------- | ----------- | --- | ---------- | -------- |
42/62

| Maximum     | likelihood     | estimation |     |     |
| ----------- | -------------- | ---------- | --- | --- |
| Probability | and likelihood |            |     |     |
For a given parameter vector π, the model assigns probability
|
Pr(Y π)
to the observed data. Viewed as a function of π, this is the likelihood:
(cid:89)N
|     | L∗(Y;π) | := Pr(Y | | π) = Pr(i | | k ,π). |
| --- | ------- | --------- | --------- | -------- |
n n
n=1
43/62

| Maximum |     | likelihood |     | estimation |     |     |     |
| ------- | --- | ---------- | --- | ---------- | --- | --- | --- |
Estimates
▶
|     | Values | of  | π that | maximize | L∗(Y;π). |     |     |
| --- | ------ | --- | ------ | -------- | -------- | --- | --- |
▶
|     | In  | practice, | maximize | the | log-likelihood |     |     |
| --- | --- | --------- | -------- | --- | -------------- | --- | --- |
(cid:88)N
|     |     |     | L(Y;π) |     | = lnL∗(Y;π) | = lnPr(i | | k ,π). |
| --- | --- | --- | ------ | --- | ----------- | -------- | -------- |
n n
n=1
|     | As  | 0 ⩽ L∗(Y;π) |     | ⩽ 1, | we have L(Y;π) | ⩽ 0. |     |
| --- | --- | ----------- | --- | ---- | -------------- | ---- | --- |
44/62

| Maximum | likelihood   |        | estimation: |                |                   | back           | to the example |     |
| ------- | ------------ | ------ | ----------- | -------------- | ----------------- | -------------- | -------------- | --- |
| Using   | the binomial | model, |             | the likelihood |                   | can be written | as             |     |
|         |              |        |             | (cid:89)3      | (cid:18) (cid:19) |                |                |     |
N
|     |     | L∗(Y;π) |     | =   | k   | πY k (1−π | )N −Y k. |     |
| --- | --- | ------- | --- | --- | --- | --------- | -------- | --- |
k k
|     |     |     |     |     | Y   | k   |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
k
k=1
| Taking | the logarithm |     | of the    | likelihood, | we  | obtain |     |     |
| ------ | ------------- | --- | --------- | ----------- | --- | ------ | --- | --- |
|        | L(Y;π)        |     | lnL∗(Y;π) |             |     |        |     |     |
=
|     |     |     | (cid:88)3 | (cid:18) (cid:19) |     |     |     |           |
| --- | --- | --- | --------- | ----------------- | --- | --- | --- | --------- |
|     |     |     | (cid:104) | N                 |     |     |     | (cid:105) |
k
|     |     | =   |     | ln  | +Y  | lnπ +(N | −Y )ln(1−π | ) . |
| --- | --- | --- | --- | --- | --- | ------- | ---------- | --- |
|     |     |     |     | Y   | k   | k       | k k        | k   |
k
k=1
45/62

| Maximum | likelihood |                  | estimation |     |     |     |     |     |
| ------- | ---------- | ---------------- | ---------- | --- | --- | --- | --- | --- |
|         |            | (cid:0)N (cid:1) |            |     |     |     |     |     |
The terms ln k do not depend on the parameters π . They therefore play no
|     |     | Y   |     |     |     | k   |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
k
| role | in the maximization. |     |     |     |     |     |     |     |
| ---- | -------------------- | --- | --- | --- | --- | --- | --- | --- |
Up to an additive constant, the log-likelihood can be written as
(cid:88)3
|     |     |        |     | (cid:104) |     |         | (cid:105) |     |
| --- | --- | ------ | --- | --------- | --- | ------- | --------- | --- |
|     |     | L(Y;π) | =   | Y lnπ +(N | −Y  | )ln(1−π | ) .       |     |
|     |     |        |     | k k       | k   | k       | k         |     |
k=1
| Function | to         | maximize |         |             |     |        |            |     |
| -------- | ---------- | -------- | ------- | ----------- | --- | ------ | ---------- | --- |
| 65lnπ    | +835ln(1−π |          | )+55lnπ | +1045ln(1−π |     | )+5lnπ | +495ln(1−π | ).  |
|          | 1          |          | 1       | 2           |     | 2      | 3          | 3   |
46/62

| Maximum | likelihood | estimation |
| ------- | ---------- | ---------- |
Properties
| ▶ Consistency. |     |     |
| -------------- | --- | --- |
▶
Asymptotic efficiency.
47/62

Maximum likelihood
0
log(π65(1−π )835)
1 1
log(π55(1−π )1045)
2 2
−100
log(π5(1−π )495)
3 3
−200
−300
−400
0 5·10−2 0.1
48/62

Maximum likelihood
0
log(π65(1−π )835)
1 1
log(π55(1−π )1045)
2 2
−100
log(π5(1−π )495)
3 3
−200
−300 270.0
| 10.0      | 50.0                |     |
| --------- | ------------------- | --- |
| −400 =    | = =                 |     |
| (cid:99)3 | (cid:99)2 (cid:99)1 |     |
| π         | π π                 |     |
| 0         | 5·10−2              | 0.1 |
49/62

Maximum likelihood
Comments
▶
In this example, the maximum likelihood estimates happen to be the same
as the sample average.
▶
For more complex models, the (log) likelihood function is not necessarily
separable.
▶
The maximization is then more complicated to perform, but the concept is
the same.
50/62

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
51/62

| Hypothesis | testing |     |     |     |
| ---------- | ------- | --- | --- | --- |
Motivation
| ▶ Modeling | assumption: | age explains | electric | car ownership. |
| ---------- | ----------- | ------------ | -------- | -------------- |
▶
| We indeed  | observe    | that the   | three parameters | are different. |
| ---------- | ---------- | ---------- | ---------------- | -------------- |
| ▶ But this | difference | may be due | to sampling      | errors.        |
▶
| What | can we say | about our | hypothesis? |     |
| ---- | ---------- | --------- | ----------- | --- |
52/62

| Hypothesis | testing |     |     |     |     |     |     |     |
| ---------- | ------- | --- | --- | --- | --- | --- | --- | --- |
Null hypothesis
▶
|     | Age does       | not explain | electric | car | ownership. |     |     |     |
| --- | -------------- | ----------- | -------- | --- | ---------- | --- | --- | --- |
| ▶   | If it is true, | then        | π = π    | = π | = π.       |     |     |     |
|     |                |             | 1        | 2 3 |            |     |     |     |
▶
|     | But it does | not | mean that | π         | = π = π .           |     |     |     |
| --- | ----------- | --- | --------- | --------- | ------------------- | --- | --- | --- |
|     |             |     |           | (cid:98)1 | (cid:98)2 (cid:98)3 |     |     |     |
LR
| Restricted |     | log likelihood |     |     |     |     |     |     |
| ---------- | --- | -------------- | --- | --- | --- | --- | --- | --- |
125lnπ+2375ln(1−π).
LU
| Unrestricted |            | log | likelihood |     |             |        |            |     |
| ------------ | ---------- | --- | ---------- | --- | ----------- | ------ | ---------- | --- |
| 65lnπ        | +835ln(1−π |     | )+55lnπ    |     | +1045ln(1−π | )+5lnπ | +495ln(1−π | ).  |
|              | 1          |     | 1          | 2   |             | 2      | 3          | 3   |
53/62

| Likelihood | ratio test |     |
| ---------- | ---------- | --- |
Intuition
If the null hypothesis is true, the estimates for the restricted and the unrestricted
| model | should not be too | different. |
| ----- | ----------------- | ---------- |
Formally
| Under | the null hypothesis, | the statistic |
| ----- | -------------------- | ------------- |
−2(LR −LU)
is asymptotically distributed as χ2 with degrees of freedom equal to the number
| of restrictions | (in our | case, 2). |
| --------------- | ------- | --------- |
54/62

| Hypothesis   | testing |     |     |     |
| ------------ | ------- | --- | --- | --- |
| Unrestricted | model   |     |     |     |
LU
|            | π = 0.0722, | π = 0.0500, | π = 0.0100,    | = −479.782. |
| ---------- | ----------- | ----------- | -------------- | ----------- |
|            | (cid:98)1   | (cid:98)2   | (cid:98)3      |             |
| Restricted | model       |             |                |             |
|            |             | π = 0.05,   | LR = −496.288. |             |
(cid:98)
| Statistic: | likelihood | ratio |      |     |
| ---------- | ---------- | ----- | ---- | --- |
|            |            | −2(LR | −LU) |     |
= 33.01
The probability to obtain such a value under the null hypothesis is lower than
10−5. This provides strong evidence against equal ownership rates across age
groups.
55/62

Outline
Context
| Simple example: | model       | development           |
| --------------- | ----------- | --------------------- |
| Simple example: | quality     | of the estimates      |
| Simple example: | maximum     | likelihood estimation |
| Simple example: | hypothesis  | testing               |
| Simple example: | forecasting |                       |
56/62

Simple example: forecasting
Motivation
▶
At this stage, we have a tested model.
▶
We are ready to use it.
▶
We want to forecast the future market shares of electric cars.
57/62

Present situation
|              |             | Age group     | 20–39 | 40–64 65+ |         |
| ------------ | ----------- | ------------- | ----- | --------- | ------- |
|              |             | Current share | 36 %  | 44% 20%   |         |
|              | Market      | penetration   | 7.2%  | 5% 1%     |         |
| Total market | penetration | = 36% 7.2%    | + 44% | 5% + 20%  | 1% = 5% |
58/62

Future scenario
| Age structure | will change | in the        | future      |     |
| ------------- | ----------- | ------------- | ----------- | --- |
|               |             | Age group     | 20–39 40–64 | 65+ |
|               |             | Current share | 36 % 44%    | 20% |
|               |             | Future share  | 25 % 50%    | 25% |
|               | Market      | penetration   | 7.2% 5%     | 1%  |
Future total market penetration = 25% 7.2% + 50% 5% + 25% 1% = 4.55%
59/62

| Confidence         | interval |            |           |     |     |
| ------------------ | -------- | ---------- | --------- | --- | --- |
| Theoretical        | 95%      | confidence | intervals |     |     |
| Bernoulli outcomes |          | imply      |           |     |     |
(cid:112)
|                  |     |           | s = π               | (1−π )/N   | .   |
| ---------------- | --- | --------- | ------------------- | ---------- | --- |
|                  |     |           | (cid:98)k (cid:98)k | (cid:98)k  | k   |
| Using asymptotic |     | normality | of π : π            | ±1.96s .   |     |
|                  |     |           | (cid:98)k (cid:98)k | (cid:98)k  |     |
| 95% percentile   |     | bootstrap | confidence          | intervals. |     |
Bootstrap samples: 10000. Perform the forecast for each of them and calculate
the quantiles.
|     |     |         | Point  | CI 2.5% | CI 97.5% |
| --- | --- | ------- | ------ | ------- | -------- |
|     |     | Present | 0.0500 | 0.0417  | 0.0588   |
|     |     | Future  | 0.0456 | 0.0378  | 0.0538   |
60/62

Forecasting
| ▶ Causal | relationship | does not vary | over | time. |
| -------- | ------------ | ------------- | ---- | ----- |
▶
Characterized by the model specification, including the values of its
parameters.
▶
| Values | of the explanatory | variables | evolve | over time. |
| ------ | ------------------ | --------- | ------ | ---------- |
61/62

Summary
▶
Motivation
▶
Simple example:
1. definition of the problem,
2. data collection,
3. model specification,
4. parameter estimation,
5. hypothesis testing,
6. model application.
62/62