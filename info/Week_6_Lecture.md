Tests
Specification testing
Michel Bierlaire
| Mathematical | Modeling | of Behavior |
| ------------ | -------- | ----------- |
1/60

Outline
| Difference | with classical | hypothesis | testing |
| ---------- | -------------- | ---------- | ------- |
| Informal   | tests and t    | tests      |         |
| Likelihood | ratio test     |            |         |
| Non-nested | hypotheses     |            |         |
| Prediction | tests          |            |         |
2/60

Motivation
Modeling
▶
It is generally impossible to determine a uniquely “correct” model
| specification |     | from | the      | data alone. |        |     |
| ------------- | --- | ---- | -------- | ----------- | ------ | --- |
| ▶ A good      | fit | does | not mean | a good      | model. |     |
▶
| Formal         | testing | is    | necessary, | but       | not sufficient. |     |
| -------------- | ------- | ----- | ---------- | --------- | --------------- | --- |
| ▶ No clear-cut |         | rules | can        | be given. |                 |     |
▶
| Subject-matter |          | judgment |      | remains  | necessary.       |          |
| -------------- | -------- | -------- | ---- | -------- | ---------------- | -------- |
| ▶ Good         | modeling | =        | good | judgment | + good analysis. |          |
| Wilkinson      | (1999)   |          | “The | grammar  | of graphics”.    | Springer |
... some researchers who use statistical methods pay more attention to goodness
of fit than to the meaning of the model... Statisticians must think about what
the models mean, regardless of fit, or they will promulgate nonsense.
3/60

| Classical | hypothesis | testing |     |     |
| --------- | ---------- | ------- | --- | --- |
| Null      | hypothesis | (H )    |     |     |
0
| A simple | hypothesis | contradicting | a theoretical | assumption. |
| -------- | ---------- | ------------- | ------------- | ----------- |
| Analogy: | court      | trial         |               |             |
▶
Theoretical assumption: an individual has committed a felony.
▶
|     | Null hypothesis: | she is innocent. |     |     |
| --- | ---------------- | ---------------- | --- | --- |
▶
Main principle: the defendant is presumed innocent until proved guilty.
▶
Similarly, H is considered correct, until the data provide sufficient evidence
0
that it is not.
4/60

| Classical | hypothesis | testing: | example |     |
| --------- | ---------- | -------- | ------- | --- |
| Lady      | tasting    | tea      |         |     |
▶
| Theory:  | a lady   | claims she   | can determine, | just by      |
| -------- | -------- | ------------ | -------------- | ------------ |
| tasting, | whether  | the milk was | poured         | into the cup |
| before   | or after | the tea.     |                |              |
▶
| H   | : the outcome | of the taste | is purely | random. |
| --- | ------------- | ------------ | --------- | ------- |
0
[Fisher, 1956]
5/60

Classical hypothesis testing: errors
Do not reject H Reject H
0 0
H is true Correct decision Type I error
0
H is false Type II error Correct decision
0
Definitions
▶
Significance level:
α = Pr(reject H | H is true).
0 0
▶
Type II error probability at a specified alternative:
β = Pr(do not reject H | H is false).
0 0
▶
Power at that alternative:
1−β = Pr(reject H | H is false).
0 0
6/60

| Specification   | testing: | example |     |     |     |
| --------------- | -------- | ------- | --- | --- | --- |
| Null hypothesis | (H       | )       |     |     |     |
0
| A simple hypothesis |          | contradicting | a theoretical | assumption. |                      |
| ------------------- | -------- | ------------- | ------------- | ----------- | -------------------- |
| Explanatory         | variable |               |               |             |                      |
|                     |          | ▶ Theory:     | a variable    | explains    | the choice behavior. |
▶
|     |     | H : | the coefficient | of the variable | is zero. |
| --- | --- | --- | --------------- | --------------- | -------- |
0
7/60

| Errors | in      | hypothesis     |            | testing   |      |                 |        |           |
| ------ | ------- | -------------- | ---------- | --------- | ---- | --------------- | ------ | --------- |
| Type   |         | I error        |            |           | Type | II error        |        |           |
|        | ▶       |                |            |           |      | ▶               |        |           |
|        | H       | rejected       | and        | H true.   |      | H accepted      | and    | H false.  |
|        | 0       |                |            | 0         |      | 0               |        | 0         |
|        | ▶       |                |            |           |      | ▶               |        |           |
|        | Include | an             | irrelevant | variable. |      | Omit a relevant |        | variable. |
|        | ▶       |                |            |           |      | ▶               |        |           |
|        | Loss    | of efficiency. |            |           |      | Specification   | error. |           |
|        | ▶       |                |            |           |      | ▶               |        |           |
|        | Cost:   | C              | .          |           |      | Cost: C         | ≫ C    | .         |
|        |         | I              |            |           |      | II              | I      |           |
Note
| In  | classical | hypothesis |     | testing, | C ≈ C |     |     |     |
| --- | --------- | ---------- | --- | -------- | ----- | --- | --- | --- |
I II
8/60

| Impact  | of an error       |     |
| ------- | ----------------- | --- |
| Four    | possible outcomes |     |
| Let P(H | true) = λ.        |     |
0
Outcome Probability×cost
H0 true,donotreject 0·λ(1−α)
H0 true,reject C I ·λα
H0 false,donotreject C II ·(1−λ)β
H0 false,reject 0·(1−λ)(1−β)
|     | E[C] | = 0·λ(1−α)+C ·λα |
| --- | ---- | ---------------- |
I
+C ·(1−λ)β+0·(1−λ)(1−β)
II
= λαC +(1−λ)βC .
I II
| Classical | hypothesis     | testing  |
| --------- | -------------- | -------- |
| λ ≈ 1,    | C ≈ C : prefer | small α. |
I II
9/60

| Impact of     | an error   |     |
| ------------- | ---------- | --- |
| Four possible | outcomes   |     |
| Let P(H       | true) = λ. |     |
0
Outcome Probability×cost
H0 true,donotreject 0·λ(1−α)
H0 true,reject C I ·λα
H0 false,donotreject C II ·(1−λ)β
H0 false,reject 0·(1−λ)(1−β)
|     | E[C] | = 0·λ(1−α)+C ·λα |
| --- | ---- | ---------------- |
I
+C ·(1−λ)β+0·(1−λ)(1−β)
II
= λαC +(1−λ)βC .
I II
| Specification | testing        |                |
| ------------- | -------------- | -------------- |
| λ ≈ 0.5,      | C ≫ C : larger | α can be used. |
II I
10/60

Outline
| Difference | with classical | hypothesis | testing |
| ---------- | -------------- | ---------- | ------- |
| Informal   | tests and t    | tests      |         |
| Likelihood | ratio test     |            |         |
| Non-nested | hypotheses     |            |         |
| Prediction | tests          |            |         |
11/60

Informal tests
Objective
Identify early inconsistencies between the model and a priori expectations.
Examples
▶
| Sign of | the coefficients | (e.g. cost, | travel time). |
| ------- | ---------------- | ----------- | ------------- |
▶
| Coefficients | in monetary | units (e.g. | value of time). |
| ------------ | ----------- | ----------- | --------------- |
12/60

t-test
Question
| Is the parameter | θ equal   | to a given | value θ∗? |     |
| ---------------- | --------- | ---------- | --------- | --- |
| ▶ H              | : θ = θ∗. |            |           |     |
0
▶
| H   | : θ ̸= θ∗. |     |     |     |
| --- | ---------- | --- | --- | --- |
1
| Statistic | (assuming | maximum | likelihood | estimator) |
| --------- | --------- | ------- | ---------- | ---------- |
Under H , if θˆ is normally distributed with known variance σ2:
0
θˆ−θ∗
∼ N(0,1).
σ
13/60

t-test: under H
0
95%
| -1.96 | θ∗  | 1.96 |
| ----- | --- | ---- |
14/60

| t-test: | if the statistic | lies outside |     |
| ------- | ---------------- | ------------ | --- |
95%
θ∗
-1.96 1.96
| H is | rejected at the | 5% significance | level. |
| ---- | --------------- | --------------- | ------ |
0
15/60

| Applying | the test |     |     |     |
| -------- | -------- | --- | --- | --- |
Statistic
θˆ−θ∗
|     |         | ⩽   | ⩽            |           |
| --- | ------- | --- | ------------ | --------- |
|     | P(−1.96 |     | 1.96) = 0.95 | = 1−0.05. |
σ
Decision
| H can | be rejected | at the 5% significance | level (α | = 0.05) if |
| ----- | ----------- | ---------------------- | -------- | ---------- |
0
(cid:12) (cid:12)
(cid:12)θˆ−θ∗(cid:12)
(cid:12) (cid:12) ⩾
1.96.
(cid:12) σ (cid:12)
(cid:12) (cid:12)
16/60

Comments
▶ If the variance σ2 is known and θ(cid:98) is normally distributed, then
θ(cid:98)−θ∗
z = ∼ N(0,1).
σ
Formally, this is a z-test.
▶
In the normal linear model, replacing σ by an appropriate estimate gives a
statistic with an exact Student t distribution, with model-dependent degrees
of freedom.
▶
For maximum likelihood estimation, the standard error is estimated and,
under standard regularity conditions,
θ(cid:98)−θ∗
d
t = →− N(0,1).
s
(cid:98)
e(θ(cid:98))
▶
In econometrics, this large-sample procedure is conventionally called a
t-test, even though its reference distribution is asymptotically normal rather
than exactly Student t.
17/60

p value
▶ Probability to get a t statistic at least as large (in absolute value) as the one
| reported, | under the | null hypothesis. |     |
| --------- | --------- | ---------------- | --- |
▶
| It is calculated | as  |     |     |
| ---------------- | --- | --- | --- |
2(1−Φ(|t|)),
p =
| where Φ(·) | is the CDF | of the standard | normal. |
| ---------- | ---------- | --------------- | ------- |
▶ The null hypothesis is rejected when the p-value is lower than the
| significance | level α. |     |     |
| ------------ | -------- | --- | --- |
18/60

Comparing two coefficients
Hypothesis
|     | H : β = | β . |     |
| --- | ------- | --- | --- |
|     | 0 1     | 2   |     |
Statistic
β(cid:98) −β(cid:98)
|     | 1 2 | ,   |     |
| --- | --- | --- | --- |
(cid:113)
|     | Var(β(cid:98) −β(cid:98) | )   |     |
| --- | ------------------------ | --- | --- |
|     | 1                        | 2   |     |
where
Var(β(cid:98) −β(cid:98) ) = Var(β(cid:98) )+Var(β(cid:98) )−2Cov(β(cid:98) ,β(cid:98) ).
| 1 2 | 1   | 2   | 1 2 |
| --- | --- | --- | --- |
Distribution
Under H and standard regularity conditions, distributed as N(0,1).
0
19/60

Outline
| Difference | with classical | hypothesis | testing |
| ---------- | -------------- | ---------- | ------- |
| Informal   | tests and t    | tests      |         |
| Likelihood | ratio test     |            |         |
| Non-nested | hypotheses     |            |         |
| Prediction | tests          |            |         |
20/60

Likelihood-ratio test
Objective
Compare a restricted model with an unrestricted model that contains it as a
special case.
Null hypothesis
H : the restrictions defining the restricted model are valid.
0
Requirement
The two models must be nested. The restrictions may be linear or nonlinear,
provided that the regularity conditions of the test hold.
21/60

| Likelihood | ratio | test |     |     |     |
| ---------- | ----- | ---- | --- | --- | --- |
Test
| Under | H and standard | regularity | conditions, |     |     |
| ----- | -------------- | ---------- | ----------- | --- | --- |
0
|     |     | −2(L(βˆ | )−L(βˆ | ∼ χ2 |     |
| --- | --- | ------- | ------ | ---- | --- |
)) ,
|                 |          |                | R U               | (K U −K | R ) |
| --------------- | -------- | -------------- | ----------------- | ------- | --- |
| asymptotically, | where    |                |                   |         |     |
| ▶ L(βˆ          | ) is the | log likelihood | of the restricted | model,  |     |
R
▶ L(βˆ
|     | ) is the | log likelihood | of the unrestricted | model, |     |
| --- | -------- | -------------- | ------------------- | ------ | --- |
U
▶ K is the number of parameters in the restricted model, and,
R
▶
| K   | is the number | of parameters | in the unrestricted |     | model. |
| --- | ------------- | ------------- | ------------------- | --- | ------ |
U
22/60

Benchmarking
| Unrestricted | model |        | Restricted        | model |
| ------------ | ----- | ------ | ----------------- | ----- |
|              |       |        | Equal probability | model |
|              | V = β | x +··· |                   | V = 0 |
|              | in 1  | ink    |                   | in    |
|              | V = β | x +··· |                   | V = 0 |
|              | jn 2  | jnk    |                   | jn    |
|              | .     |        |                   | .     |
|              | .     |        |                   | .     |
|              | .     |        |                   | .     |
Restrictions
β = 0, ∀k
k
23/60

Benchmarking
Log likelihood of the unrestricted Log likelihood of the restricted
model model
| L(β(cid:98)) | P = 1/J | , ∀i ∈ C ,∀n |
| ------------ | ------- | ------------ |
|              | in      | n n          |
(cid:88)N
|     | L(0) | = − log(J ) |
| --- | ---- | ----------- |
n
n=1
Statistic
−2(L(0)−L(β(cid:98))) ∼
χ2
K
24/60

| Benchmarking | revisited |        |                  |                    |
| ------------ | --------- | ------ | ---------------- | ------------------ |
| Unrestricted | model     |        | Restricted       | model              |
|              |           |        | Only alternative | specific constants |
|              | V = β     | x +··· |                  | V = β ,            |
|              | in 1      | ink    |                  | in i               |
|              | V = β     | x +··· |                  | V = β ,            |
|              | jn 2      | jnk    |                  | jn j               |
|              | .         |        |                  | .                  |
|              | .         |        |                  | .                  |
|              | .         |        |                  | .                  |
Restrictions
|     | All coefficients | but the constants | are constrained | to zero. |
| --- | ---------------- | ----------------- | --------------- | -------- |
25/60

Benchmarking revisited
Log likelihood of the unrestricted Log likelihood of the restricted
model model
L(β(cid:98)) P = N /N ∀i ∈ C,∀n.
in i
(cid:88)J
L(c) = N log(N /N).
i i
i=1
Statistic
−2(L(c)−L(β(cid:98))) ∼ χ2 with d = K −J +1.
d
26/60

Benchmarking
| Classical | output          | of estimation | software |
| --------- | --------------- | ------------- | -------- |
| Summary   | statistics      |               |          |
| Number    | of observations | = 2544        |          |
L(0)
= −2794.870
L(c)
= −2203.160
L(βˆ)
= −1640.525
−2[L(0)−L(βˆ)]
= 2308.689
27/60

| Test         | of generic | attributes |            |       |        |
| ------------ | ---------- | ---------- | ---------- | ----- | ------ |
| Unrestricted |            | model      | Restricted | model |        |
| Alternative  | specific   |            | Generic    |       |        |
|              | V =        | β x +···   |            | V = β | x +··· |
|              | in         | 1i ink     |            | in 1  | ink    |
|              | V =        | β x +···   |            | V = β | x +··· |
|              | jn         | 1j jnk     |            | jn 1  | jnk    |
|              | .          |            |            | .     |        |
|              | .          |            |            | .     |        |
|              | .          |            |            | .     |        |
Restriction
β = β = ···
1i 1j
28/60

| Test | of generic | attributes |     |     |     |
| ---- | ---------- | ---------- | --- | --- | --- |
Log likelihood of the unrestricted Log likelihood of the restricted
| model |     |             | model |             |     |
| ----- | --- | ----------- | ----- | ----------- | --- |
|       |     | L(β(cid:98) |       | L(β(cid:98) |     |
|       |     | )           |       |             | )   |
|       |     | AS          |       |             | G   |
Statistic
|     |     | −2(L(β(cid:98) )−L(β(cid:98) | ∼ χ2    |          |     |
| --- | --- | ---------------------------- | ------- | -------- | --- |
|     |     |                              | )) with | d = K −K | .   |
|     |     | G                            | AS d    | AS       | G   |
29/60

| Test of taste | variations |     |     |     |
| ------------- | ---------- | --- | --- | --- |
Segmentation
▶
| Classify | the data into | G groups. | Size of group | g: N . |
| -------- | ------------- | --------- | ------------- | ------ |
g
| ▶ The same | specification | is considered | for each group. |     |
| ---------- | ------------- | ------------- | --------------- | --- |
▶
| A different | set of parameters | is estimated | for each | group. |
| ----------- | ----------------- | ------------ | -------- | ------ |
30/60

Test of taste variations
| N N | N   | N   |     |
| --- | --- | --- | --- |
| 1 2 | 3   | 4   | N   |
(cid:80)
L (β(cid:98)1)L (β(cid:98)2) L (β(cid:98)3) L (β(cid:98)4) G L (β(cid:98)g)
| N1 N2 | N3  | N4  | Ng  |
| ----- | --- | --- | --- |
g=1
31/60

| Test of        | taste variations |      |            |              |        |     |
| -------------- | ---------------- | ---- | ---------- | ------------ | ------ | --- |
| Unrestricted   | model            |      | Restricted | model        |        |     |
| Group specific | coefficients     |      | Generic    | coefficients |        |     |
|                | (cid:88)G        |      |            | V = β        | x +··· |     |
|                |                  |      |            | in 1         | ink    |     |
| V              | = (δ β )x        | +··· |            |              |        |     |
| in             | ng 1g            | ink  |            |              |        |     |
|                |                  |      |            | V = β        | x +··· |     |
|                |                  |      |            | jn 2         | jnk    |     |
g=1
.
|     | (cid:88)G |     |     | .   |     |     |
| --- | --------- | --- | --- | --- | --- | --- |
.
| V   | = (δ β )x | +··· |     |     |     |     |
| --- | --------- | ---- | --- | --- | --- | --- |
| jn  | ng 2g     | jnk  |     |     |     |     |
g=1
.
.
.
Restrictions
|     |     | β = β | = ··· = | β , ∀k. |     |       |
| --- | --- | ----- | ------- | ------- | --- | ----- |
|     |     | k1    | k2      | kG      |     | 32/60 |

Test of taste variations
Log likelihood of the unrestricted Log likelihood of the restricted
model model
(cid:88)G
L (β(cid:98))
| L   | g)  |     | N   |
| --- | --- | --- | --- |
(β(cid:98)
Ng
g=1
Statistic
| (cid:34) | (cid:88)G | (cid:35) | (cid:88)G |
| -------- | --------- | -------- | --------- |
−2 L (β(cid:98))− L (β(cid:98) g) ∼ χ2 with d = K −K = (G −1)K.
| N   | Ng  | d   |     |
| --- | --- | --- | --- |
|     | g=1 |     | g=1 |
33/60

| Tests        | of     | nonlinear | specifications |     |     |            |               |       |     |
| ------------ | ------ | --------- | -------------- | --- | --- | ---------- | ------------- | ----- | --- |
| Unrestricted |        |           | model          |     |     | Restricted |               | model |     |
| Power        | series | (x        | > 0)           |     |     | Linear     | specification |       |     |
ref
(cid:88)L
|     |     |     | (cid:18) x | (cid:19)ℓ |     |     |     | V = β | x +··· |
| --- | --- | --- | ---------- | --------- | --- | --- | --- | ----- | ------ |
|     |     |     | ink        |           |     |     |     | in 1  | ink    |
|     | V   | =   | β          | +···      |     |     |     |       |        |
|     | in  |     | 1ℓ         |           |     |     |     | V = β | x +··· |
|     |     |     | x          |           |     |     |     | jn 2  | jnk    |
|     |     | ℓ=1 | ref        |           |     |     |     |       |        |
.
.
|     | V   | = β | x +··· |     |     |     |     | .   |     |
| --- | --- | --- | ------ | --- | --- | --- | --- | --- | --- |
|     | jn  | 2   | jnk    |     |     |     |     |     |     |
.
. .
Restrictions
|     |     |     |     | β = β | =   | ··· = β | =   | 0.  |     |
| --- | --- | --- | --- | ----- | --- | ------- | --- | --- | --- |
|     |     |     |     | 12    | 13  |         | 1L  |     |     |
34/60

Power series
V
in
x
ink
35/60

| Test | of nonlinear | specifications |     |     |     |
| ---- | ------------ | -------------- | --- | --- | --- |
Log likelihood of the unrestricted Log likelihood of the restricted
| model |     |               |     | model |               |
| ----- | --- | ------------- | --- | ----- | ------------- |
|       |     | L(β(cid:98) ) |     |       | L(β(cid:98) ) |
U R
Statistic
|     |     | (cid:104)      |               | (cid:105)   |          |
| --- | --- | -------------- | ------------- | ----------- | -------- |
|     |     | −2 L(β(cid:98) | )−L(β(cid:98) | ) ∼ χ2 with | d = L−1. |
|     |     |                | R U           | d           |          |
36/60

Notes
▶
High-order polynomial terms are usually difficult to interpret behaviorally.
▶
| They may | overfit | the estimation | sample. |     |
| -------- | ------- | -------------- | ------- | --- |
▶
Their extrapolation can be unstable outside the observed range.
| ▶ Other nonlinear | specifications |     | can be used | for testing: |
| ----------------- | -------------- | --- | ----------- | ------------ |
▶
| piecewise | linear, |     |     |     |
| --------- | ------- | --- | --- | --- |
▶ Box-Cox.
37/60

Outline
| Difference | with classical | hypothesis | testing |
| ---------- | -------------- | ---------- | ------- |
| Informal   | tests and t    | tests      |         |
| Likelihood | ratio test     |            |         |
| Non-nested | hypotheses     |            |         |
| Prediction | tests          |            |         |
38/60

| Non-nested | hypotheses |     |
| ---------- | ---------- | --- |
Nested hypotheses
| ▶ Restricted | and unrestricted | models. |
| ------------ | ---------------- | ------- |
▶
| Linear           | restrictions.     |     |
| ---------------- | ----------------- | --- |
| ▶ H : restricted | model is correct. |     |
0
▶
| Test: likelihood | ratio test. |     |
| ---------------- | ----------- | --- |
| Non-nested       | hypotheses  |     |
▶
| Need to | compare two models. |     |
| ------- | ------------------- | --- |
▶
| None of | them is a restriction | of the other. |
| ------- | --------------------- | ------------- |
▶
| Likelihood | ratio test cannot | be used. |
| ---------- | ----------------- | -------- |
39/60

Example
| Model 1 | Model  | 2           |       |
| ------- | ------ | ----------- | ----- |
| = β     | +···   | = β log(x   | )+··· |
| V       | x      | V           |       |
| in 1    | ink    | in 1        | ink   |
| V = β   | x +··· | V = β log(x | )+··· |
| jn 2    | jnk    | jn 2        | jnk   |
| .       |        | .           |       |
| .       |        | .           |       |
| .       |        | .           |       |
40/60

Cox test
| Back to   | nested hypotheses |                 |     |
| --------- | ----------------- | --------------- | --- |
| ▶ We want | to test model     | 1 against model | 2.  |
▶
We generate a composite model C such that both models 1 and 2 are
| restricted | cases of model | C.    |         |
| ---------- | -------------- | ----- | ------- |
|            |                | Model | C       |
|            | Model          | 1     | Model 2 |
41/60

Example
| Model 1 |        | Model | 2           |       |
| ------- | ------ | ----- | ----------- | ----- |
| V = β   | x +··· |       | V = β log(x | )+··· |
| in 1    | ink    |       | in 1        | ink   |
| V = β   | x +··· |       | V = β log(x | )+··· |
| jn 2    | jnk    |       | jn 2        | jnk   |
| .       |        |       | .           |       |
| .       |        |       | .           |       |
| .       |        |       | .           |       |
Model C
|     | V = β | x +β log(x | )+··· |     |
| --- | ----- | ---------- | ----- | --- |
|     | in 11 | ink 12     | ink   |     |
|     | V = β | x +β log(x | )+··· |     |
|     | jn 21 | jnk 22     | jnk   |     |
. .
.
42/60

Cox test
Testing
▶
| We test | 1 against C | using the likelihood | ratio test. |     |
| ------- | ----------- | -------------------- | ----------- | --- |
▶
| We test | 2 against C | using the likelihood | ratio test. |     |
| ------- | ----------- | -------------------- | ----------- | --- |
Conclusions
| C   | against 1       | C against 2       | Conclusion  |               |
| --- | --------------- | ----------------- | ----------- | ------------- |
| 1   | is not rejected | 2 is rejected     | Prefer 1    |               |
| 1   | is rejected     | 2 is not rejected | Prefer 2    |               |
| 1   | is rejected     | 2 is rejected     | Develop     | better models |
| 1   | is not rejected | 2 is not rejected | Use another | test          |
43/60

| Davidson | and McKinnon | J test |     |     |
| -------- | ------------ | ------ | --- | --- |
Motivation
Cox test may require to estimate a model with a potentially very large number of
parameters.
| Consider | two specifications |     |     |     |
| -------- | ------------------ | --- | --- | --- |
V(1)(x ;β)+ε(1),
M : U =
|     |     | 1 in | in in | in  |
| --- | --- | ---- | ----- | --- |
V(2)(x ;γ)+ε(2).
M : U =
|      |            | 2 in | in in | in  |
| ---- | ---------- | ---- | ----- | --- |
| Null | hypothesis |      |       |     |
| M is | correct.   |      |       |     |
1
44/60

| Davidson | and McKinnon   |        | J test |     |     |
| -------- | -------------- | ------ | ------ | --- | --- |
| First    | step           |        |        |     |     |
| Estimate | the parameters | γ of M | .      |     |     |
2
| Composite | specification       |             |             |                |     |
| --------- | ------------------- | ----------- | ----------- | -------------- | --- |
|           |                     | (1−α)V(1)(x | ;β)+αV(2)(x |                |     |
|           | M : U               | =           |             | ;γ)+ε (cid:98) | ,   |
|           | C in                |             | in in       | in in          | in  |
| where     | γ are the estimated | parameters  | of M .      |                |     |
|           | (cid:98)            |             | 2           |                |     |
Estimation
| Estimate | β and α. |     |     |     |     |
| -------- | -------- | --- | --- | --- | --- |
Test
| Under | H , the true value | of α is | 0. A t-test can | be used. |     |
| ----- | ------------------ | ------- | --------------- | -------- | --- |
0
45/60

| Davidson | and McKinnon        | J test |
| -------- | ------------------- | ------ |
| The      | test is directional |        |
The procedure tests M against M . It must be repeated in the opposite
1 2
direction, with M as the null model and predictions from M added to the
2 1
| composite | specification. |     |
| --------- | -------------- | --- |
46/60

| Adjusted   | likelihood | ratio | index |     |
| ---------- | ---------- | ----- | ----- | --- |
| Likelihood | ratio      | index |       |     |
L(β(cid:98))
|     |     |     | ρ2 = 1− | ,   |
| --- | --- | --- | ------- | --- |
L(0)
| Adjusted | likelihood | ratio index |     |     |
| -------- | ---------- | ----------- | --- | --- |
L(β(cid:98))−K
|     |     | ρ¯2 | = 1− | ,   |
| --- | --- | --- | ---- | --- |
L(0)
| where  | K is the number | of unknown  | parameters    | in the model. |
| ------ | --------------- | ----------- | ------------- | ------------- |
| Rule   | of thumb        |             |               |               |
| Select | the model with  | the highest | value of ρ¯2. |               |
47/60

Other criteria
| Akaike | Information | Criterion |
| ------ | ----------- | --------- |
2K −2L(β(cid:98)).
| Lower values | are preferred. |           |
| ------------ | -------------- | --------- |
| Bayesian     | Information    | Criterion |
ln(N)−2L(β(cid:98)).
K
| The smallest, | the better. |     |
| ------------- | ----------- | --- |
48/60

Outline
| Difference | with classical | hypothesis | testing |
| ---------- | -------------- | ---------- | ------- |
| Informal   | tests and t    | tests      |         |
| Likelihood | ratio test     |            |         |
| Non-nested | hypotheses     |            |         |
| Prediction | tests          |            |         |
49/60

| Prediction | tests |     |
| ---------- | ----- | --- |
Motivation
| Check if | the model is able | to predict. |
| -------- | ----------------- | ----------- |
50/60

Outlier analysis
Procedure
▶
| Apply | the model on | the sample. |     |
| ----- | ------------ | ----------- | --- |
▶
Examine observations where the predicted probability is the smallest for the
| observed | choice. |     |     |
| -------- | ------- | --- | --- |
▶
Test model sensitivity to outliers, as a small probability has a significant
| impact | on the log likelihood. |     |     |
| ------ | ---------------------- | --- | --- |
▶
| Potential | causes of low | probability: |     |
| --------- | ------------- | ------------ | --- |
▶
| coding | or measurement | error in | the data, |
| ------ | -------------- | -------- | --------- |
▶
| model         | misspecification, |                     |     |
| ------------- | ----------------- | ------------------- | --- |
| ▶ unexplained | variation         | in choice behavior. |     |
51/60

| Coding | or       | measurement |     |      | error  | in the data |
| ------ | -------- | ----------- | --- | ---- | ------ | ----------- |
|        | Look for | signs       | of  | data | errors |             |
▶
|     | Travel | time | is negative. |     |     |     |
| --- | ------ | ---- | ------------ | --- | --- | --- |
▶
|     | Number |     | is coded | as a | string. |     |
| --- | ------ | --- | -------- | ---- | ------- | --- |
▶
etc.
|     | Correct | or  | remove | the | observation |     |
| --- | ------- | --- | ------ | --- | ----------- | --- |
▶
|     | Go        | back | to the      | original | survey.  |     |
| --- | --------- | ---- | ----------- | -------- | -------- | --- |
|     | ▶ Correct |      | only if you | are      | certain. |     |
52/60

Model misspecification
| Improve the  | specification |           |                       |
| ------------ | ------------- | --------- | --------------------- |
| ▶ Seek clues | of missing    | variables | from the observation. |
▶
Why is the model associating such a low probability for this choice?
▶ Did we forget to account for age, income, or any other variable?
▶
| Should           | a nonlinear | specification | be investigated? |
| ---------------- | ----------- | ------------- | ---------------- |
| ▶ Use behavioral | intuition.  |               |                  |
53/60

| Inexplicable | variation       | in  | choice behavior |     |
| ------------ | --------------- | --- | --------------- | --- |
| Keep         | the observation |     |                 |     |
▶
|     | If no acceptable    | explanation  | is found, keep | the observation. |
| --- | ------------------- | ------------ | -------------- | ---------------- |
|     | ▶ Avoid overfitting | of the model | to the data.   |                  |
▶
The model should reflect how people behave, not how they should behave.
54/60

Estimation Validation
80% 20%
Cross-validation
Motivation
▶
| Purpose | of the model: | prediction. |
| ------- | ------------- | ----------- |
▶
| Is the model | able to | predict? |
| ------------ | ------- | -------- |
55/60

Estimation Validation
80% 20%
Cross-validation
Motivation
▶
| Purpose | of the model: | prediction. |
| ------- | ------------- | ----------- |
▶
| Is the model | able to | predict? |
| ------------ | ------- | -------- |
55/60

Cross-validation
Motivation
▶
| Purpose | of the model: | prediction. |
| ------- | ------------- | ----------- |
▶
| Is the model | able to | predict? |
| ------------ | ------- | -------- |
Estimation Validation
80% 20%
55/60

Methodology
| Split the | sample |     |     |     |     |     |     |
| --------- | ------ | --- | --- | --- | --- | --- | --- |
▶
| Decide | the size | of  | the validation | set     | (e.g.        | 20%) |      |
| ------ | -------- | --- | -------------- | ------- | ------------ | ---- | ---- |
| ▶ Draw | randomly | an  | estimation     | set and | a validation |      | set. |
▶
| Repeat | R times. |     |     |     |     |     |     |
| ------ | -------- | --- | --- | --- | --- | --- | --- |
Evaluate
| ▶ For each | pair | of estimation/validation |     |     | set... |     |     |
| ---------- | ---- | ------------------------ | --- | --- | ------ | --- | --- |
▶
Estimate the parameters of the model with the estimation set.
▶ Calculate a measure of fit of the estimated model on the validation set.
(cid:80)
| ▶   |     |     |     | N   |     | |x  |     |
| --- | --- | --- | --- | --- | --- | --- | --- |
Typically, the log-likelihood V logP(i ), or the expected number of
|           |           |     |              | n=(cid:80)1 | n       | n     |     |
| --------- | --------- | --- | ------------ | ----------- | ------- | ----- | --- |
| correctly | predicted |     | observations |             | N V P(i | |x ). |     |
|           |           |     |              |             | n=1     | n n   |     |
▶
| Calculate | the | average | measure | of fit. |     |     |     |
| --------- | --- | ------- | ------- | ------- | --- | --- | --- |
▶
Select the model with the highest average fit on the validation sets.
56/60

Practical recommendations
▶
| Tests are | designed to | check meaningful | hypotheses. |
| --------- | ----------- | ---------------- | ----------- |
▶
| Do not test | hypotheses | that do | not make sense. |
| ----------- | ---------- | ------- | --------------- |
▶
| Do not apply | the tests | blindly. |     |
| ------------ | --------- | -------- | --- |
▶
| Always use | your judgment. |     |     |
| ---------- | -------------- | --- | --- |
57/60

Summary
▶
Specification testing different from classical hypothesis testing.
▶
Informal tests.
▶
t-tests.
▶
Likelihood ratio test.
▶
Non-nested hypotheses.
▶
Prediction tests.
58/60

| 90%, 95% | and | 99% of | the χ2 | distribution |     | with | K degrees | of  |
| -------- | --- | ------ | ------ | ------------ | --- | ---- | --------- | --- |
freedom
|     |     | K 90%     | 95%    | 99%    | K 90%     | 95% 99%       |     |     |
| --- | --- | --------- | ------ | ------ | --------- | ------------- | --- | --- |
|     |     | 1 2.706   | 3.841  | 6.635  | 21 29.615 | 32.671 38.932 |     |     |
|     |     | 2 4.605   | 5.991  | 9.210  | 22 30.813 | 33.924 40.289 |     |     |
|     |     | 3 6.251   | 7.815  | 11.345 | 23 32.007 | 35.172 41.638 |     |     |
|     |     | 4 7.779   | 9.488  | 13.277 | 24 33.196 | 36.415 42.980 |     |     |
|     |     | 5 9.236   | 11.070 | 15.086 | 25 34.382 | 37.652 44.314 |     |     |
|     |     | 6 10.645  | 12.592 | 16.812 | 26 35.563 | 38.885 45.642 |     |     |
|     |     | 7 12.017  | 14.067 | 18.475 | 27 36.741 | 40.113 46.963 |     |     |
|     |     | 8 13.362  | 15.507 | 20.090 | 28 37.916 | 41.337 48.278 |     |     |
|     |     | 9 14.684  | 16.919 | 21.666 | 29 39.087 | 42.557 49.588 |     |     |
|     |     | 10 15.987 | 18.307 | 23.209 | 30 40.256 | 43.773 50.892 |     |     |
|     |     | 11 17.275 | 19.675 | 24.725 | 31 41.422 | 44.985 52.191 |     |     |
|     |     | 12 18.549 | 21.026 | 26.217 | 32 42.585 | 46.194 53.486 |     |     |
|     |     | 13 19.812 | 22.362 | 27.688 | 33 43.745 | 47.400 54.776 |     |     |
|     |     | 14 21.064 | 23.685 | 29.141 | 34 44.903 | 48.602 56.061 |     |     |
|     |     | 15 22.307 | 24.996 | 30.578 | 35 46.059 | 49.802 57.342 |     |     |
|     |     | 16 23.542 | 26.296 | 32.000 | 36 47.212 | 50.998 58.619 |     |     |
|     |     | 17 24.769 | 27.587 | 33.409 | 37 48.363 | 52.192 59.893 |     |     |
|     |     | 18 25.989 | 28.869 | 34.805 | 38 49.513 | 53.384 61.162 |     |     |
|     |     | 19 27.204 | 30.144 | 36.191 | 39 50.660 | 54.572 62.428 |     |     |
|     |     | 20 28.412 | 31.410 | 37.566 | 40 51.805 | 55.758 63.691 |     |     |
59/60

| Bibliography | I          |              |     |
| ------------ | ---------- | ------------ | --- |
| Fisher, R.   | A. (1956). |              |     |
| Mathematics  | of a lady  | tasting tea. |     |
In Newman, J. R., editor, The world of Mathematics, volume 3, pages
| 1512–1521, | New-York. | Simon qnd | Schuster. |
| ---------- | --------- | --------- | --------- |
60/60