| The        | logit model       |     |
| ---------- | ----------------- | --- |
| Derivation | and specification |     |
Michel Bierlaire
| Mathematical | Modeling | of Behavior |
| ------------ | -------- | ----------- |
1/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
2/101

The logit model
Probability for individual n to choose alternative i within the set C :
n
eµnVin
|     | P(i|C | (cid:80) |        |
| --- | ----- | -------- | ------ |
|     |       | ) =      | .      |
|     |       | n        | eµnVjn |
j∈C
n
where
(cid:88)K
|     |     | V = β | z ,   |
| --- | --- | ----- | ----- |
|     |     | in    | k ink |
k=1
where
▶ C
| is the set | of alternatives | for individual | n,  |
| ---------- | --------------- | -------------- | --- |
n
▶ z are the attributes of alternative i for individual n, and
in
▶
µ and β , k = 1,...,K are parameters to be estimated from data.
n k
3/101

The logit model
Unknown parameters
▶
β , k = 1,...,K are taste parameters, capturing the relative importance of
k
each attribute on the overall utility.
▶
µ is a scale parameter, controlling how sensitive choices are to utility
n
differences.
4/101

| Example: | transportation | mode choice        | in Switzerland |     |
| -------- | -------------- | ------------------ | -------------- | --- |
|          |                | Three alternatives |                |     |
▶
Car,
|     |     | ▶ public | transportation (pt), |     |
| --- | --- | -------- | -------------------- | --- |
▶
Slow modes (sm).
Six alternative-specific attributes
▶
Car cost and car travel time.
|     |     | ▶ Public-transport | cost and in-vehicle | travel |
| --- | --- | ------------------ | ------------------- | ------ |
time.
▶
Public-transport waiting time.
▶
Slow-mode distance.
5/101

| Example: | n      | is Priya |            |     |     |     |
| -------- | ------ | -------- | ---------- | --- | --- | --- |
| Who is   | Priya? |          | Attributes |     |     |     |
▶
| ▶ German | speaking. |     | Car cost: | z   |     | = 0.34 CHF. |
| -------- | --------- | --- | --------- | --- | --- | ----------- |
car,Priya,1
| ▶    |     |     | ▶ Time | by car: | z           | = 3.0 min. |
| ---- | --- | --- | ------ | ------- | ----------- | ---------- |
| Age: | 44. |     |        |         | car,Priya,2 |            |
▶
| ▶ Gender: | female. |     | pt cost: | z   | =   | 3.0 CHF. |
| --------- | ------- | --- | -------- | --- | --- | -------- |
pt,Priya,1
| ▶             |     |        | ▶ Time | by pt: | z          | = 17.0 min. |
| ------------- | --- | ------ | ------ | ------ | ---------- | ----------- |
| Subscription: |     | no GA. |        |        | pt,Priya,2 |             |
▶
| ▶ Socio-prof. |     | category: manager. | Waiting | time: | z   | = 1.0 min. |
| ------------- | --- | ------------------ | ------- | ----- | --- | ---------- |
pt,Priya,3
| ▶                   |          |       | ▶ Distance: | z   |            | = 2.5 km. |
| ------------------- | -------- | ----- | ----------- | --- | ---------- | --------- |
| Trip                | purpose: | work. |             |     | sm,Priya,4 |           |
| ▶ Car availability: |          | yes.  |             |     |            |           |
6/101

| Example: | n is Priya         |          |            |          |         |         |          |
| -------- | ------------------ | -------- | ---------- | -------- | ------- | ------- | -------- |
| Utility: | function of        | the      | attributes |          |         |         |          |
| V        | = −(β +cost        |          | +β         | time     | +β      | waiting | time ).  |
| pt,Priya | 0,Priya            | pt,Priya | t,Priya    | pt,Priya | w,Priya |         | pt,Priya |
| Opposite | of the generalized |          | cost.      |          |         |         |          |
| Example  | of parameters      |          |            |          |         |         |          |
|          | = −14.64−cost      |          | −0.303     |          | −1.97   |         |          |
| V        |                    |          |            | time     |         | waiting | time     |
| pt,Priya |                    | pt,Priya |            | pt,Priya |         |         | pt,Priya |
= −24.8.
7/101

Example: n is Priya
| Utility: function of the | attributes |     |     |
| ------------------------ | ---------- | --- | --- |
| V                        | = −24.8,   |     |     |
pt,Priya
| V         | = 10.4−cost | −1.18 time |           |
| --------- | ----------- | ---------- | --------- |
| car,Priya |             | car,Priya  | car,Priya |
= 6.52,
| V        | = −6.16 distance |          |     |
| -------- | ---------------- | -------- | --- |
| sm,Priya |                  | sm,Priya |     |
= −15.4.
8/101

| Example: n   | is Priya        |                  |           |           |
| ------------ | --------------- | ---------------- | --------- | --------- |
| Logit model: | probability     | for Priya        | to choose | the car   |
|              | C               | {car,pt,sm},     |           |           |
|              |                 | =                | µ         | = 0.0347. |
|              | Priya           |                  | Priya     |           |
|              | µ V             | = 0.0347·(−24.8) |           | = −0.859, |
|              | Priya           | pt,Priya         |           |           |
|              | µ V             | = 0.0347·6.52    |           | = 0.226,  |
|              | Priya car,Priya |                  |           |           |
|              | µ V             | = 0.0347·(−15.4) |           | = −0.534. |
|              | Priya sm,Priya  |                  |           |           |
9/101

| Example: n   | is Priya    |           |           |            |
| ------------ | ----------- | --------- | --------- | ---------- |
| Logit model: | probability | for Priya | to choose | the public |
transportation
|     |     | C   | {car,pt,sm}. |     |
| --- | --- | --- | ------------ | --- |
=
Priya
e−0.859
|     | P (pt|C | ) =   |                 |          |
| --- | ------- | ----- | --------------- | -------- |
|     | Priya   | Priya |                 |          |
|     |         |       | e−0.859 +e0.226 | +e−0.534 |
= 0.187.
10/101

| Example: n   | is Priya    |           |              |         |
| ------------ | ----------- | --------- | ------------ | ------- |
| Logit model: | probability | for Priya | to choose    | the car |
|              |             | C =       | {car,pt,sm}. |         |
Priya
e0.226
|     | P (car|C | ) =   |                 |          |
| --- | -------- | ----- | --------------- | -------- |
|     | Priya    | Priya |                 |          |
|     |          |       | e−0.859 +e0.226 | +e−0.534 |
= 0.554.
11/101

| Example: n   | is Priya    |           |              |             |
| ------------ | ----------- | --------- | ------------ | ----------- |
| Logit model: | probability | for Priya | to choose    | a slow mode |
|              |             | C =       | {car,pt,sm}. |             |
Priya
e−0.534
|     | P (sm|C | ) =   |                 |          |
| --- | ------- | ----- | --------------- | -------- |
|     | Priya   | Priya |                 |          |
|     |         |       | e−0.859 +e0.226 | +e−0.534 |
= 0.259.
12/101

Example: n is Priya
Logit model for Priya
P (pt) = 18.7%,
Priya
P (car) = 55.4%,
Priya
P (sm) = 25.9%.
Priya
13/101

| Example: n       | is Mateo   |           |                  |            |
| ---------------- | ---------- | --------- | ---------------- | ---------- |
| Who is Mateo?    | Attributes |           |                  |            |
| ▶                |            | ▶         |                  |            |
| French speaking. |            | Car cost: | irrelevant.      |            |
| ▶                |            | ▶         |                  |            |
| Age: 35.         |            | Time by   | car: irrelevant. |            |
| ▶                |            | ▶         |                  |            |
| Gender:          | male.      | pt cost:  | z                | = 0.0 CHF. |
pt,Mateo,1
| ▶             |     | ▶       |       |             |
| ------------- | --- | ------- | ----- | ----------- |
| Subscription: | GA. | Time by | pt: z | = 17.0 min. |
pt,Mateo,2
| ▶           |                     | ▶       |         |            |
| ----------- | ------------------- | ------- | ------- | ---------- |
| Socio-prof. | category: craftman. | Waiting | time: z | = 1.0 min. |
pt,Mateo,3
| ▶             |           | ▶         |     |           |
| ------------- | --------- | --------- | --- | --------- |
| Trip purpose: | not work. | Distance: | z   | = 2.5 km. |
sm,Mateo,4
▶
| Car availability: | no. |     |     |     |
| ----------------- | --- | --- | --- | --- |
14/101

| Example:     | n is Mateo   |                             |              |          |     |
| ------------ | ------------ | --------------------------- | ------------ | -------- | --- |
| Systematic   | utility      | of public transportation    |              |          |     |
| V            | = −11.5−cost | −0.166time                  | −0.19waiting | time     | .   |
| pt,Mateo     |              | pt,Mateo                    | pt,Mateo     | pt,Mateo |     |
| Substitution | of Mateo’s   | attributes                  |              |          |     |
|              | V            | = −11.5−0−0.166(17)−0.19(1) |              |          |     |
pt,Mateo
= −14.512.
15/101

Example: n is Mateo
Systematic utilities
V = −14.512,
pt,Mateo
V = −10.6distance
sm,Mateo sm,Mateo
= −10.6(2.5) = −26.5.
16/101

Example: n is Mateo
Scaled systematic utilities
| C =            | {pt,sm}, µ        | = 0.0521. |
| -------------- | ----------------- | --------- |
| Mateo          | Mateo             |           |
| µ V            | = 0.0521(−14.512) | = −0.756, |
| Mateo pt,Mateo |                   |           |
| µ V            | = 0.0521(−26.5)   | = −1.381. |
Mateo sm,Mateo
17/101

Example: n is Mateo
Choice probabilities
C = {pt,sm}.
Mateo
e−0.756
| P     | (pt | C ) = | = 0.651, |
| ----- | ----------- | -------- |
| Mateo | Mateo       |          |
e−0.756 +e−1.381
e−1.381
| P (sm | | C ) = | = 0.349. |
| ----- | ------- | -------- |
| Mateo | Mateo   |          |
e−0.756 +e−1.381
P (pt) = 65.1%,
Mateo
P (car) = 0%,
Mateo
P (sm) = 34.9%.
Mateo
18/101

| How does it | work? |     |     |
| ----------- | ----- | --- | --- |
▶
| Where does | the logit | model come from? |     |
| ---------- | --------- | ---------------- | --- |
▶
| With | two alternatives. |     |     |
| ---- | ----------------- | --- | --- |
▶
| With | multiple alternatives. |     |     |
| ---- | ---------------------- | --- | --- |
▶
| How do | we specify | the utility functions? |     |
| ------ | ---------- | ---------------------- | --- |
▶
| What | variables | can be involved? |     |
| ---- | --------- | ---------------- | --- |
▶
| How | do we come | up with a functional | form? |
| --- | ---------- | -------------------- | ----- |
▶
How do we derive a different model for different individuals?
▶
| How do | we estimate | the parameters? |     |
| ------ | ----------- | --------------- | --- |
19/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
20/101

| The binary logit  | model |       |
| ----------------- | ----- | ----- |
|                   | C     | {i,j} |
| Two alternatives: | =     |       |
n
U = V +ε′ ,
in in in
U = V +ε′ .
jn jn jn
Main issue
▶
| Utility is | latent, not observed. |     |
| ---------- | --------------------- | --- |
▶
| Only the | choice is observed. |     |
| -------- | ------------------- | --- |
▶
| More complicated | than | linear regression. |
| ---------------- | ---- | ------------------ |
▶
| How do | we know the “zero” | of utility? |
| ------ | ------------------ | ----------- |
▶
| How do | we know the units | of utility? |
| ------ | ----------------- | ----------- |
21/101

Binary choice model
Choice model
|     | (i|{i,j}) |     |      | ⩾    |     |
| --- | --------- | --- | ---- | ---- | --- |
|     | P         | =   | Pr(U | U ). |     |
|     | n         |     | in   | jn   |     |
Invariant to shifts
| (i|{i,j}) |        |     | ⩾   |      | R.   |
| --------- | ------ | --- | --- | ---- | ---- |
| P         | = Pr(U | +η  | U   | +η), | ∀η ∈ |
| n         |        | in  |     | jn   |      |
Invariant to scale
| P (i|{i,j}) | = Pr(µU |     | ⩾ µU | ), ∀µ ∈ | R,µ > 0. |
| ----------- | ------- | --- | ---- | ------- | -------- |
| n           |         | in  | jn   |         |          |
22/101

| Binary choice | model |     |     |     |
| ------------- | ----- | --- | --- | --- |
Choice model
|               | P (i|{i,j}) | = Pr(U  | ⩾ U )  |          |
| ------------- | ----------- | ------- | ------ | -------- |
|               | n           |         | in jn  |          |
|               |             | = Pr(V  | +ε′ ⩾  | V +ε′ )  |
|               |             |         | in     | jn       |
|               |             |         | in     | jn       |
|               |             | = Pr(V  | −V ⩾   | ε′ −ε′ ) |
|               |             |         | in jn  | jn in    |
|               |             | = Pr(ε′ | ⩽ V −V | ),       |
|               |             |         | n in   | jn       |
| where ε′ = ε′ | −ε′ .       |         |        |          |
| n jn          | in          |         |        |          |
Note
▶
For binary choice, it would be sufficient to make assumptions about
| ε′ = ε′ −ε′ |     |     |     |     |
| ----------- | --- | --- | --- | --- |
.
| n jn | in  |     |     |     |
| ---- | --- | --- | --- | --- |
▶
| But we want | to generalize | later on. |     |     |
| ----------- | ------------- | --------- | --- | --- |
23/101

Error term
| Assumptions | about the | random variables | ε′ and ε′ |
| ----------- | --------- | ---------------- | --------- |
in jn
ε′ ε′
and are the maximum of many r.v. capturing unobserved attributes (e.g.
| in jn              |             |                   |         |
| ------------------ | ----------- | ----------------- | ------- |
| mood, experience), | measurement | and specification | errors. |
| Gumbel theorem     |             |                   |         |
The maximum of many i.i.d. random variables approximately follows an Extreme
| Value distribution: | EV(η,µ), | with µ > 0. |     |
| ------------------- | -------- | ----------- | --- |
24/101

Extreme value distribution
| Emil Julius | Gumbel |     | (1891–1966) |     |     |
| ----------- | ------ | --- | ----------- | --- | --- |
▶
| father | of extreme | value | theory, |     |     |
| ------ | ---------- | ----- | ------- | --- | --- |
▶
| politically | involved |     | left-wing | pacifist | in  |
| ----------- | -------- | --- | --------- | -------- | --- |
Germany,
▶
| strongly  | against       | right | wing’s  | campaign | of  |
| --------- | ------------- | ----- | ------- | -------- | --- |
| organized | assassination |       | (1919), |          |     |
▶
| first German |         | professor  | to       | be expelled | from     |
| ------------ | ------- | ---------- | -------- | ----------- | -------- |
| university   | under   | the        | pressure | of the      | Nazis,   |
| ▶ 1932:      | he left | Heidelberg |          | to Paris,   | where he |
| met Borel    | and     | Fr´echet,  |          |             |          |
▶
| 1940:        | he had | to escape | to       | New-York, | where |
| ------------ | ------ | --------- | -------- | --------- | ----- |
| he continued |        | his fight | against  | Nazism    | by    |
| helping      | the US | secret    | service. |           |       |
25/101

| The Extreme | Value        | distribution | EV(η,µ)               |     |
| ----------- | ------------ | ------------ | --------------------- | --- |
| Probability | density      | function     | (pdf)                 |     |
|             |              | f(t)         | = µe−µ(t−η)e−e−µ(t−η) | .   |
| Cumulative  | distribution | function     | (CDF)                 |     |
(cid:90)
c
|     |     | P(ε ⩽ | c) = F(c) = | f(t)dt |
| --- | --- | ----- | ----------- | ------ |
−∞
e−e−µ(c−η).
=
26/101

| The Extreme | Value | distribution |     |         |     |     |
| ----------- | ----- | ------------ | --- | ------- | --- | --- |
| pdf EV(0,1) |       |              | CDF | EV(0,1) |     |     |
0.8
0.3
0.6
0.2
0.4
0.1
0.2
| −3 −2 | −1  | 1 2 | 3 −3 | −2 −1 | 1 2 | 3   |
| ----- | --- | --- | ---- | ----- | --- | --- |
27/101

| The Extreme | Value | distribution |     |     |
| ----------- | ----- | ------------ | --- | --- |
Properties
ε ∼ EV(η,µ).
▶
| Mode:   | η.        |         |              |           |
| ------- | --------- | ------- | ------------ | --------- |
| ▶ Mean: | E[ε] = η+ | γ where | γ is Euler’s | constant. |
µ
| ▶         |        | π2  |     |     |
| --------- | ------ | --- | --- | --- |
| Variance: | Var[ε] | = . |     |     |
6µ2
Euler’s constant
(cid:90)
∞
|     |     | γ = − | e−x lnx | dx ≈ 0.5772. |
| --- | --- | ----- | ------- | ------------ |
0
28/101

| The Extreme | Value | distribution |     |     |     |
| ----------- | ----- | ------------ | --- | --- | --- |
Properties
| ▶ Let | ε ∼ EV(η,µ), | α > 0 and | β ∈ R. | Then |     |
| ----- | ------------ | --------- | ------ | ---- | --- |
∼
|     |     | αε+β | EV(αη+β,µ/α). |     |     |
| --- | --- | ---- | ------------- | --- | --- |
▶
| In particular, | if  | ε ∼ EV(0, | 1), then, |     |     |
| -------------- | --- | --------- | --------- | --- | --- |
αε+β ∼ EV(β,1/α).
| ▶          |      | ∼         |             |             |        |
| ---------- | ---- | --------- | ----------- | ----------- | ------ |
| Therefore, | if ε | EV(0, 1), | then, using | α = 1/µ and | β = η, |
1
∼
|     |     | ε′  | = η+ | ε EV(η,µ). |     |
| --- | --- | --- | ---- | ---------- | --- |
µ
29/101

| The Extreme | Value | distribution |     |     |     |     |
| ----------- | ----- | ------------ | --- | --- | --- | --- |
Properties
|       | ∼        |       | ∼    |                  |     |     |
| ----- | -------- | ----- | ---- | ---------------- | --- | --- |
| Let ε | EV(η ,µ) | and ε | EV(η | ,µ) independent: |     |     |
| 1     | 1        | 2     |      | 2                |     |     |
∼
|     |     | ε = | ε −ε | Logistic(η | −η  | ,µ), |
| --- | --- | --- | ---- | ---------- | --- | ---- |
|     |     |     | 1    | 2          | 1   | 2    |
that is
1
|     |     | F (x) | =   |     |     | .   |
| --- | --- | ----- | --- | --- | --- | --- |
ε
|     |     |     | 1+exp(−µ(x |     | −(η −η | ))) |
| --- | --- | --- | ---------- | --- | ------ | --- |
|     |     |     |            |     | 1      | 2   |
µ.
| Note: | the two EV distributions |     | must | have | the same | scale |
| ----- | ------------------------ | --- | ---- | ---- | -------- | ----- |
30/101

| The Extreme | Value distribution |     |     |     |     |     |
| ----------- | ------------------ | --- | --- | --- | --- | --- |
Properties
| ▶ ∼   |              | ∼   |          |              |       |          |
| ----- | ------------ | --- | -------- | ------------ | ----- | -------- |
| Let ε | EV(η ,µ) and | ε   | EV(η ,µ) | independent. | Then, |          |
| 1     | 1            | 2   | 2        |              |       |          |
|       |              |     |          | (cid:18)     |       | (cid:19) |
1
|     | ε = max(ε | ,ε  | ) ∼ EV | ln(eµη1 +eµη2),µ |     | .   |
| --- | --------- | --- | ------ | ---------------- | --- | --- |
1 2
µ
▶
| Let ε ∼ | EV(η ,µ), i | = 1,...,J | independent. | Then,    |     |          |
| ------- | ----------- | --------- | ------------ | -------- | --- | -------- |
| i       | i           |           |              |          |     |          |
|         |             |           |              | (cid:32) |     | (cid:33) |
(cid:88)J
1
|     |           |        | ∼   |       | eµηi,µ |     |
| --- | --------- | ------ | --- | ----- | ------ | --- |
|     | ε = max(ε | ,...,ε | )   | EV ln |        | .   |
|     |           | 1      | J   | µ     |        |     |
i=1
▶
| The sum | of two EV r.v. | is not | an EV | r.v. |     |     |
| ------- | -------------- | ------ | ----- | ---- | --- | --- |
31/101

Modeling assumptions
Distributions
▶
| ε′ and   | ε′ are i.i.d. EV(η | , µ ). |
| -------- | ------------------ | ------ |
| in       | jn                 | n n    |
| ▶ η ,µ ∈ | R, µ > 0.          |        |
| n n      | n                  |        |
▶
| i.i.d. =        | independent and | identically distributed. |
| --------------- | --------------- | ------------------------ |
| ▶ i.i.d. across | i.              |                          |
▶
| Independent | across n. |     |
| ----------- | --------- | --- |
32/101

| Modeling | assumptions   |             |            |
| -------- | ------------- | ----------- | ---------- |
| Change   | of variables: | isolate the | parameters |
ε′ = η + 1 ε ,
in n µn in
ε′ = η + 1 ε ,
jn n jn
µn
| where | ε , ε ∼ EV(0, | 1). |     |
| ----- | ------------- | --- | --- |
|       | in jn         |     |     |
33/101

| Binary logit | model |     |     |     |
| ------------ | ----- | --- | --- | --- |
Specification
| If the model | is specified | as  |        |       |
| ------------ | ------------ | --- | ------ | ----- |
|              |              | U = | V +η + | 1 ε , |
|              |              | in  | in n   | in    |
µn
|     |     | U = | V +η + | 1 ε , |
| --- | --- | --- | ------ | ----- |
|     |     | jn  | jn n   | jn    |
µn
∼
we can assume w.l.o.g. that ε , ε are i.i.d. EV(0, 1), across both i and n.
|     |     | in jn |     |     |
| --- | --- | ----- | --- | --- |
34/101

Binary logit model
Choice model
| (i|{i,j}) |     |      | ⩾   |     |     |     |
| --------- | --- | ---- | --- | --- | --- | --- |
| P         | =   | Pr(U | U   | )   |     |     |
| n         |     | in   | jn  |     |     |     |
(cid:16) (cid:17)
|     | =   | Pr V | +η  | + 1 ε | ⩾ V   | +η + 1 ε |
| --- | --- | ---- | --- | ----- | ----- | -------- |
|     |     | in   | n   |       | in jn | n jn     |
|     |     |      |     | µn    |       | µn       |
⩽
|     | =   | Pr( 1 (ε | −ε  | )   | V + η(cid:26) | −V − η(cid:26) ), |
| --- | --- | -------- | --- | --- | ------------- | ----------------- |
|     |     | µ        | jn  | in  | in (cid:26) n | jn (cid:26) n     |
n
|     | =   | Pr(ε | −ε  | ⩽ µ V | −µ V | ).  |
| --- | --- | ---- | --- | ----- | ---- | --- |
|     |     | jn   | in  | n     | in n | jn  |
Property of EV
|     | ε   | = ε  | −ε  | ∼ Logistic(0,1). |     |     |
| --- | --- | ---- | --- | ---------------- | --- | --- |
|     |     | n jn | in  |                  |     |     |
35/101

| The Logistic | distribution:    | Logistic(η,µ) |     |     |
| ------------ | ---------------- | ------------- | --- | --- |
| Probability  | density function | (pdf)         |     |     |
µe−µ(t−η)
f(t) = .
(1+e−µ(t−η))2
| Cumulative | distribution | function | (CDF) |     |
| ---------- | ------------ | -------- | ----- | --- |
(cid:90)
c
1
|     | P(c ⩾ ε) | = F(c) = | f(t)dt = | .   |
| --- | -------- | -------- | -------- | --- |
1+e−µ(c−η)
−∞
| with µ > | 0.  |     |     |     |
| -------- | --- | --- | --- | --- |
36/101

Binary logit model
Choice model
| P          | (i|{i,j}) = | Pr(ε | ⩽ µ V | −µ V ) = F | (µ V   | −µ V ). |
| ---------- | ----------- | ---- | ----- | ---------- | ------ | ------- |
|            | n           | n    | n in  | n jn       | ε n in | n jn    |
| The binary | logit model |      |       |            |        |         |
eµnVin
1
|     | P (i|{i,j}) | =   |     | =   |     | .   |
| --- | ----------- | --- | --- | --- | --- | --- |
n
|     |     |     | 1+e−µn(Vin−Vjn) | eµnVin | +eµnVjn |     |
| --- | --- | --- | --------------- | ------ | ------- | --- |
37/101

| The binary  | logit model |               |     |     |
| ----------- | ----------- | ------------- | --- | --- |
| Key element | of the      | specification |     |     |
µ V .
n in
Comments
| ▶ η does | not play any | role in | the model. |     |
| -------- | ------------ | ------- | ---------- | --- |
n
▶
| The | units of V must | be fixed. | The model must | be normalized. |
| --- | --------------- | --------- | -------------- | -------------- |
in
▶ Before doing it, we extend the model to more than two alternatives.
38/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
39/101

| Multiple | alternatives |          |     |     |
| -------- | ------------ | -------- | --- | --- |
| Choice   | set: C =     | {1,...,J | }   |     |
|          | n            |          | n   |     |
1
C
|     |     | U = | V +η + ε , | i ∈ , |
| --- | --- | --- | ---------- | ----- |
|     |     | in  | in n µ in  | n     |
n
| where | the ε are i.i.d. | EV(0,1). |     |     |
| ----- | ---------------- | -------- | --- | --- |
in
40/101

Choice set
C
| Universal     | choice set:  |         | Mode choice    |
| ------------- | ------------ | ------- | -------------- |
| ▶             |              |         | ▶              |
| All potential | alternatives | for the | driving alone, |
▶
| population. |     |     | walking, |
| ----------- | --- | --- | -------- |
▶
| Alternatives | relevant | to the | ▶   |
| ------------ | -------- | ------ | --- |
biking,
| analyst. |     |     | ▶   |
| -------- | --- | --- | --- |
subway,
▶
bus rapid transit,
▶
light rail,
▶
ride hailing,
▶
on demand transit,
▶
bicycle/e-scooter sharing,
▶
car sharing,
▶
air taxi. 41/101

Choice set
C
| Individual’s | choice set: |     | Mode choice |
| ------------ | ----------- | --- | ----------- |
n
| ▶           |          |     | ▶              |
| ----------- | -------- | --- | -------------- |
| No driver’s | license. |     | driving alone, |
▶
| ▶         |            |     | walking, |
| --------- | ---------- | --- | -------- |
| No auto   | available. |     |          |
| ▶         |            |     | ▶        |
| Awareness | of public  |     | biking,  |
▶
| transportation. |                |     | subway, |
| --------------- | -------------- | --- | ------- |
| ▶ Public        | transportation |     | ▶       |
bus rapid transit,
| unreachable. |     |     | ▶   |
| ------------ | --- | --- | --- |
light rail,
▶
| Walking | not an option | for long | ▶   |
| ------- | ------------- | -------- | --- |
ride hailing,
| distance. |     |     | ▶   |
| --------- | --- | --- | --- |
on demand transit,
▶
bicycle/e-scooter sharing,
▶
car sharing,
▶
air taxi. 42/101

Choice set
| Choice set | generation | is  | tricky |     |     |
| ---------- | ---------- | --- | ------ | --- | --- |
▶
| How    | to model “awareness”? |           |     |               |     |
| ------ | --------------------- | --------- | --- | ------------- | --- |
| ▶ What | does “long            | distance” |     | exactly mean? |     |
▶
| What      | does “unreachable” |     | exactly | mean? |     |
| --------- | ------------------ | --- | ------- | ----- | --- |
| We assume | here deterministic |     |         | rules |     |
▶
Car is available if n has a driver’s license and a car is available in the
household.
| ▶ Walking | is available | if  | trip length | is shorter than | 4km. |
| --------- | ------------ | --- | ----------- | --------------- | ---- |
43/101

| Availability | conditions |               |        |               |          |            |       |
| ------------ | ---------- | ------------- | ------ | ------------- | -------- | ---------- | ----- |
|              |            | (cid:12)      |        |               | (cid:12) |            |       |
|              |            |               | C      |               |          |            | C     |
|              |            | 1 if i        | ∈ ,    |               | 0        | if i       | ∈ ,   |
|              | δ =        |               | n or   | lnδ =         |          |            | n     |
|              | in         | 0 otherwise.  |        | in            | −∞       | otherwise. |       |
| Choice       | model      |               |        |               |          |            |       |
|              | P (i       | | C ) = Pr(U  | +lnδ   | ⩾ U           | +lnδ     | , ∀j       | ∈ C), |
|              | n          | n             | in     | in jn         |          | jn         |       |
| where        | ln0 = −∞   | is understood | in the | extended-real | sense.   |            |       |
44/101

Error terms
Logit assumptions
| For each individual | n,  | the standardized |     | errors ε are |     |
| ------------------- | --- | ---------------- | --- | ------------ | --- |
in
▶
| independent | across | alternatives | i;  |     |     |
| ----------- | ------ | ------------ | --- | --- | --- |
▶
| identically         | distributed      | as EV(0,1). |     |                    |     |
| ------------------- | ---------------- | ----------- | --- | ------------------ | --- |
| Across observations |                  |             |     |                    |     |
| ▶ Errors            | are also assumed | independent |     | across individuals | n.  |
▶
| The common | location | η cancels |     | from all utility comparisons. |     |
| ---------- | -------- | --------- | --- | ----------------------------- | --- |
n
| ▶ The scale | enters | the model | through | µ V . |     |
| ----------- | ------ | --------- | ------- | ----- | --- |
|             |        |           |         | n in  |     |
45/101

| The logit |             | model: | derivation |          |            |        |       |          |      |     |
| --------- | ----------- | ------ | ---------- | -------- | ---------- | ------ | ----- | -------- | ---- | --- |
|           | P(i|C       |        |            | ⩾        |            |        |       | ⩾        |      |     |
|           |             | ) =    | Pr(U       | max      | U ) = Pr(V |        | +ε    | max      | V +ε | ).  |
|           |             | n      | in         |          | jn         | in     | in    |          | jn   | jn  |
|           |             |        |            | j∈C \{i} |            |        |       | j∈C \{i} |      |     |
|           |             |        |            | n        |            |        |       | n        |      |     |
| Best      | alternative |        | different  | from     | i          |        |       |          |      |     |
|           |             |        | U          | = max    | U =        | max    | (V +ε | ).       |      |     |
|           |             |        | −in        |          | jn         |        | jn    | jn       |      |     |
|           |             |        |            | j∈C n    | \{i} j∈C   | n \{i} |       |          |      |     |
| Binary    |             | choice | model      |          |            |        |       |          |      |     |
|           |             |        |            | P(i|C    | ) = Pr(U   | ⩾ U    | ).    |          |      |     |
|           |             |        |            |          | n          | in     | −in   |          |      |     |
46/101

The logit model
Property of Extreme Value distribution
U = V +ε
−in −in −in
where
(cid:88)
1
V = ln eµnVjn,
−in
µ
n j∈C
n
\{i}
and
ε ∼ EV(0,µ ).
−in n
47/101

The logit model
Binary logit
eµnVin
P(i|C
) =
|     |     |     | n eµnVin | +eµnV−in |     |
| --- | --- | --- | -------- | -------- | --- |
Therefore...
(cid:80)
|     |     | 1    | eµnVjn,    |     |     |
| --- | --- | ---- | ---------- | --- | --- |
|     | V   | = ln |            |     |     |
|     | −in | µn   | j∈C n \{i} |     |     |
(cid:80)
(cid:80)
| eµnV−in |     | eµnµ | 1 ln j∈Cn\{i}eµnVjn |     | eµnVjn,  |
| ------- | --- | ---- | ------------------- | --- | -------- |
|         |     | =    | n                   | =   |          |
|         |     |      |                     |     | j∈C \{i} |
n
| P(i|C |     |         | (cid:80)eµnVin |            | eµnVin |
| ----- | --- | ------- | -------------- | ---------- | ------ |
|       | )   | =       |                | = (cid:80) | .      |
|       | n   | eµnVin+ | j∈Cn\{i}eµnVjn |            | eµnVjn |
j∈Cn
48/101

The logit model
eµnVin
P(i|C ) = (cid:80) .
n
j∈C
n
eµnVjn
where (cid:88)
V = β z ,
in k ink
k
where z is the vector of attributes of alternative i for individual n.
in
49/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
50/101

| Choosing the | units |     |     |     |     |
| ------------ | ----- | --- | --- | --- | --- |
Issue
▶
| As utility | is  | latent, | the units  | are arbitrary. |     |
| ---------- | --- | ------- | ---------- | -------------- | --- |
| ▶ We need  | to  | choose  | the units. |                |     |
▶
We first introduce a specification that is convenient to interpret.
Context
▶
| Utility | contains | a cost/price |     | variable | (in CHF, say). |
| ------- | -------- | ------------ | --- | -------- | -------------- |
▶
| We constrain |     | its coefficient |     | to be -1. |     |
| ------------ | --- | --------------- | --- | --------- | --- |
▶
| Utility | = opposite | of  | generalized | cost. |     |
| ------- | ---------- | --- | ----------- | ----- | --- |
▶
| Units: | CHF. |     |     |     |     |
| ------ | ---- | --- | --- | --- | --- |
51/101

Example
| Setting β | = −1 |     |     |     |     |     |
| --------- | ---- | --- | --- | --- | --- | --- |
c
|                |     | V = −cost        |     | +β time | +β direct | .   |
| -------------- | --- | ---------------- | --- | ------- | --------- | --- |
|                |     | in               | in  | t       | in h      | in  |
| Interpretation | of  | the coefficients |     |         |           |     |
▶
| Willingness | to  | pay for an | increase | of  | the variable. |     |
| ----------- | --- | ---------- | -------- | --- | ------------- | --- |
▶
| β : transforms |     | minutes | into CHF: | value | of time (opposite). |     |
| -------------- | --- | ------- | --------- | ----- | ------------------- | --- |
t
▶
| β : transforms |     | the feature | of direct |     | service into CHF. |     |
| -------------- | --- | ----------- | --------- | --- | ----------------- | --- |
h
52/101

Logit model
| Moneymetric utility | function |     |     |     |     |     |     |
| ------------------- | -------- | --- | --- | --- | --- | --- | --- |
(cid:88)
|     |     | V = −cost |     | +   | β z . |     |     |
| --- | --- | --------- | --- | --- | ----- | --- | --- |
|     |     | in        |     | in  | k ink |     |     |
k
Choice model
(cid:80)
|         |            | eµnVin |     | e−µncostin+ |     | k µ nβ k z ink |       |
| ------- | ---------- | ------ | --- | ----------- | --- | -------------- | ----- |
| P (i|C) | = (cid:80) |        | =   | (cid:80)    |     |                | .     |
| n       |            |        |     |             |     | (cid:80)       |       |
|         |            | eµnVjn |     | e−µncostjn+ |     | µnβ            | z     |
|         |            | j∈C    |     | j∈C         |     | k              | k jnk |
53/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
54/101

Relax the i.i.d. assumption
i.i.d. assumption
▶
Same η for all alternatives i: relaxed in this lecture.
▶
Same µ for all alternatives i: relaxed in the lecture on mixtures.
▶
Independence across alternatives i: relaxed in the lecture on MEV models.
▶
Independence across observations n: relaxed in the lecture on panel data.
55/101

Motivation
|     |     |     |     | iPhone | Samsung |
| --- | --- | --- | --- | ------ | ------- |
|     |     |     |     | $900   | $900    |
Price
|             |           | Cellular |             | 5G      | 5G     |
| ----------- | --------- | -------- | ----------- | ------- | ------ |
|             |           | Capacity |             | 128GB   | 128GB  |
|             |           | Display  |             | 6.6”    | 6.6”   |
|             | Market    | shares   | US (2026)   | 58.35 % | 21.31% |
| Conclusion: | we cannot | assume   | E[ε ] = E[ε | ].      |        |
|             |           |          | in          | jn      |        |
Source:gs.statcounter.com/vendor-market-share/mobile
56/101

Motivation
| ▶ The alternatives |     | may             | differ | through |        |
| ------------------ | --- | --------------- | ------ | ------- | ------ |
| attributes         |     | not represented |        | in the  | model. |
▶
| Examples   | include |               | brand, | operating | system,       |
| ---------- | ------- | ------------- | ------ | --------- | ------------- |
| ecosystem, |         | distribution, |        | design    | and installed |
base.
▶
| Their       | average | contribution            |     | can | be  |
| ----------- | ------- | ----------------------- | --- | --- | --- |
| represented |         | by alternative-specific |     |     |     |
constants.
| ▶ An ASC  | captures             |          | the mean | effect   | of  |
| --------- | -------------------- | -------- | -------- | -------- | --- |
| omitted   | alternative-specific |          |          | factors, |     |
| including | “brand               | equity.” |          |          |     |
57/101

Modeling
| Alternative | Specific | Constants |     |     |
| ----------- | -------- | --------- | --- | --- |
▶
| We define | new variables: |     |     |     |
| --------- | -------------- | --- | --- | --- |
(cid:12)
|     |     |     | 1 if i is | iPhone, |
| --- | --- | --- | --------- | ------- |
z =
|     |     | i,iPhone | 0 otherwise. |     |
| --- | --- | -------- | ------------ | --- |
(cid:12)
|     |     |     | 1 if i is | Samsung, |
| --- | --- | --- | --------- | -------- |
z =
i,Samsung
0 otherwise.
▶
| We include | them with | coefficients | in the utility | function. |
| ---------- | --------- | ------------ | -------------- | --------- |
58/101

| Alternative | Specific    | Constants |     |     |
| ----------- | ----------- | --------- | --- | --- |
| Original    | formulation |           |     |     |
1
|     |     | U = V | +η + ε . |     |
| --- | --- | ----- | -------- | --- |
|     |     | in in | n µ in   |     |
n
| New | formulation |     |     |     |
| --- | ----------- | --- | --- | --- |
1
|     | U = V +(β | z               | +β z )+η          | + ε . |
| --- | --------- | --------------- | ----------------- | ----- |
|     | in in     | iPhone i,iPhone | Samsung i,Samsung | n in  |
µ
n
59/101

| Alternative     | Specific | Constants |     |     |     |     |     |     |
| --------------- | -------- | --------- | --- | --- | --- | --- | --- | --- |
| New formulation |          |           |     |     |     |     |     |     |
1
|     | U        | =   | V        | +(β |        | +η  | )+  | ε .      |
| --- | -------- | --- | -------- | --- | ------ | --- | --- | -------- |
|     | iPhone,n |     | iPhone,n |     | iPhone | n   | µ   | iPhone,n |
n
1
|     | U         | =   | V         | +(β |         | +η  | )+  | ε .         |
| --- | --------- | --- | --------- | --- | ------- | --- | --- | ----------- |
|     | Samsung,n |     | Samsung,n |     | Samsung |     | n   | µ Samsung,n |
n
| Location | parameters |     |           |          |         |        |     |     |
| -------- | ---------- | --- | --------- | -------- | ------- | ------ | --- | --- |
|          |            |     | η         |          | = β     |        | +η  |     |
|          |            |     |           | iPhone,n |         | iPhone | n   |     |
|          |            |     | η         | =        | β       |        | +η  |     |
|          |            |     | Samsung,n |          | Samsung |        | n   |     |
60/101

| Alternative |             | Specific |     | Constants |     |     |     |     |
| ----------- | ----------- | -------- | --- | --------- | --- | --- | --- | --- |
| New         | formulation |          |     |           |     |     |     |     |
1
|     |     |     | U        | = V      | +η       | +   | ε          | .   |
| --- | --- | --- | -------- | -------- | -------- | --- | ---------- | --- |
|     |     |     | iPhone,n | iPhone,n | iPhone,n |     | µ iPhone,n |     |
n
1
|          |     |     | U         | = V       | +η        |     | + ε | .         |
| -------- | --- | --- | --------- | --------- | --------- | --- | --- | --------- |
|          |     |     | Samsung,n | Samsung,n | Samsung,n |     | µ   | Samsung,n |
| Comments |     |     |           |           |           |     | n   |           |
▶
The use of ASCs relaxes the assumption that the location parameters are
|     | the | same | across alternatives. |     |     |     |     |     |
| --- | --- | ---- | -------------------- | --- | --- | --- | --- | --- |
▶ Abuse of language: the coefficients of the ASCs are often called ASCs
themselves.
▶
In practice, the numbering of alternatives is often consistent with their
names (iPhone is always alternative 1, etc.) But it is not required.
▶
|     | There | is an | identification | issue. |     |     |     |     |
| --- | ----- | ----- | -------------- | ------ | --- | --- | --- | --- |
61/101

Identification
Issue
| For any value | of η , |     |     |     |     |     |     |
| ------------- | ------ | --- | --- | --- | --- | --- | --- |
n
|          |           |     | 1   |        |      | 1      |        |
| -------- | --------- | --- | --- | ------ | ---- | ------ | ------ |
| P (i|C ) | = Pr(V +η | +η  | + ε | ⩾ V +η | +η + | ε , ∀j | ∈ C ). |
| n n      | in        | n i | in  | jn     | n j  | jn     | n      |
|          |           |     | µ   |        |      | µ      |        |
|          |           |     | n   |        |      | n      |        |
Normalization
▶
| Select | any arbitrary | alternative | j, and | normalize | η = −η | .   |     |
| ------ | ------------- | ----------- | ------ | --------- | ------ | --- | --- |
|        |               |             |        |           | n      | j   |     |
▶
It is equivalent to normalize the ASC of alternative j to zero.
▶
| If there | are J alternatives, |     | only J −1 | ASCs | are identified. |     |     |
| -------- | ------------------- | --- | --------- | ---- | --------------- | --- | --- |
|          | n                   |     | n         |      |                 |     |     |
62/101

| Example: binary |     | choice |        |          |     |     |     |     |
| --------------- | --- | ------ | ------ | -------- | --- | --- | --- | --- |
| Normalization   |     | of the | iPhone | constant |     |     |     |     |
1
|     |     | U        | = V      |     | + ε |          | .   |     |
| --- | --- | -------- | -------- | --- | --- | -------- | --- | --- |
|     |     | iPhone,n | iPhone,n |     | µ   | iPhone,n |     |     |
n
1
|     | U   |           | = V       |     | +η        |     | + ε         | .   |
| --- | --- | --------- | --------- | --- | --------- | --- | ----------- | --- |
|     |     | Samsung,n | Samsung,n |     | Samsung,n |     | µ Samsung,n |     |
n
| Normalization |     | of the | Samsung |     | constant |     |     |     |
| ------------- | --- | ------ | ------- | --- | -------- | --- | --- | --- |
1
|     |     | U        | = V |          | +η       |     | + ε      | .   |
| --- | --- | -------- | --- | -------- | -------- | --- | -------- | --- |
|     |     | iPhone,n |     | iPhone,n | iPhone,n |     | iPhone,n |     |
µ
n
1
|     |     | U         | = V |           | +   | ε         | .   |     |
| --- | --- | --------- | --- | --------- | --- | --------- | --- | --- |
|     |     | Samsung,n |     | Samsung,n |     | Samsung,n |     |     |
µ
n
63/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
64/101

| Quantitative | attributes     |     |     |
| ------------ | -------------- | --- | --- |
| Numerical    | and continuous |     |     |
| ▶ z ∈        | R, ∀i,n,k.     |     |     |
ink
▶
| Associated | with a      | specific unit. |     |
| ---------- | ----------- | -------------- | --- |
| ▶ Vary     | across both | i and n.       |     |
Examples
▶
| Auto | in-vehicle time | (in minutes). |     |
| ---- | --------------- | ------------- | --- |
▶
| Transit | in-vehicle    | time (in minutes). |     |
| ------- | ------------- | ------------------ | --- |
| ▶ Auto  | out-of-pocket | cost (in cents).   |     |
▶
| Transit   | fare (in cents). |                 |               |
| --------- | ---------------- | --------------- | ------------- |
| ▶ Walking | time to          | the bus stop    | (in minutes). |
|           |                  | Straightforward | modeling      |
65/101

| Quantitative | attributes |     |     |     |     |     |     |
| ------------ | ---------- | --- | --- | --- | --- | --- | --- |
▶
β transforms the unit of the corresponding attribute into utility units.
| ▶ Example: | consider |     | two moneymetric |                 | specifications: |     |      |
| ---------- | -------- | --- | --------------- | --------------- | --------------- | --- | ---- |
|            |          |     | µV              | = −µcost+µβTT   |                 |     | +··· |
|            |          |     | in              |                 |                 |     | in   |
|            |          |     | µV              | = −µcost+µβ′TT′ |                 |     | +··· |
in
in
▶
| If TT | is a number |     | of minutes, | the | unit | of β | is CHF/minute. |
| ----- | ----------- | --- | ----------- | --- | ---- | ---- | -------------- |
in
▶
| If TT′ | is a number |     | of hours, | the | unit of | β′ is | CHF/hour. |
| ------ | ----------- | --- | --------- | --- | ------- | ----- | --------- |
in
▶
Both models are equivalent, but the estimated value of the coefficient will
be different
|     |     |     |         |     | β′  | TT  |          |
| --- | --- | --- | ------- | --- | --- | --- | -------- |
|     |     | βTT | = β′TT′ |     | =⇒  | =   | in = 60. |
in
|     |     |     |     | in  | β   | TT′ |     |
| --- | --- | --- | --- | --- | --- | --- | --- |
in
66/101

| Qualitative | attributes |     |
| ----------- | ---------- | --- |
Examples
| ▶ Level | of comfort | for the train. |
| ------- | ---------- | -------------- |
▶
| Reliability | of the | bus. |
| ----------- | ------ | ---- |
▶ Color.
▶
Shape.
▶ etc.
67/101

Modeling
| Identify | all possible | levels of |     |     |     |
| -------- | ------------ | --------- | --- | --- | --- |
the variable
|     |     |     | Example | with K | = 3 |
| --- | --- | --- | ------- | ------ | --- |
▶ Comfortable,
| ▶      |              |     | ▶   |                  |     |
| ------ | ------------ | --- | --- | ---------------- | --- |
| Rather | comfortable, |     | z   | for comfortable. |     |
c
▶
| ▶ Not | comfortable. |     | z   | for rather comfortable. |     |
| ----- | ------------ | --- | --- | ----------------------- | --- |
rc
▶
|            |       |               | z   | for not comfortable. |     |
| ---------- | ----- | ------------- | --- | -------------------- | --- |
| Introduce  | a 0/1 | attribute for | nc  |                      |     |
| each level | k     |               |     |                      |     |
z z z
c rc nc
|     |          |            |     | comfortable | 1 0 0 |
| --- | -------- | ---------- | --- | ----------- | ----- |
| z ∈ | {0,1},∀k | = 1,...,K, |     |             |       |
k
|     |           |     | rather | comfortable | 0 1 0 |
| --- | --------- | --- | ------ | ----------- | ----- |
|     | (cid:88)K |     | not    | comfortable | 0 0 1 |
|     | z =       | 1.  |        |             |       |
k
k=1
68/101

Modeling
| Utility function | with         | ASC   |     |        |       |        |      |
| ---------------- | ------------ | ----- | --- | ------ | ----- | ------ | ---- |
|                  | z = 1−z      | −z .  |     |        |       |        |      |
|                  | nc           | c rc  |     |        |       |        |      |
|                  | µV = −µ(cost | +β z  | +β  | z +β   | z +β  | )      |      |
|                  | i            | i c c | rc  | rc     | nc nc | i      |      |
|                  | = −µ(cost    | +β z  | +β  | z +β   | (1−z  | −z )+β | )    |
|                  |              | i c c | rc  | rc     | nc    | c rc   | i    |
|                  | = −µ(cost    | +(β   | −β  | )z +(β | −β    | )z +β  | +β ) |
|                  |              | i c   | nc  | c      | rc    | nc rc  | nc i |
|                  | = −µ(cost    | +β′z  | +β′ | z +β′) |       |        |      |
|                  |              | i c c | rc  | rc     | i     |        |      |
Comments
▶
Index n omitted.
▶
| Coefficient | of one | level is confounded |     | with | the | ASC. |     |
| ----------- | ------ | ------------------- | --- | ---- | --- | ---- | --- |
▶ In the presence of an ASC, only K −1 binary variables can be included.
69/101

| Alternative | specific       |     | coefficients |             |           |      |
| ----------- | -------------- | --- | ------------ | ----------- | --------- | ---- |
| Generic     | vs alternative |     | specific     |             |           |      |
|             |                |     | µ V          | = −µ cost+µ | β TT      | +··· |
|             |                |     | n car,n      | n           | n t car,n |      |
|             |                | µ   | V            | = −µ cost+µ | β TT      | +··· |
|             |                |     | n bus,n      | n           | n t bus,n |      |
or
|     |     | µ   | V       | = −µ cost+µ | β TT    | +···  |
| --- | --- | --- | ------- | ----------- | ------- | ----- |
|     |     |     | n car,n | n           | n t,car | car,n |
|     |     | µ   | V       | = −µ cost+µ | β TT    | +···  |
|     |     | n   | bus,n   | n           | n t,bus | bus,n |
Modeling assumption: a minute has/has not the same value whether it is
|     |     |     | incurred | on the auto | or bus mode. |     |
| --- | --- | --- | -------- | ----------- | ------------ | --- |
70/101

Outline
Normalization
Introduction
Alternative Specific Constants
Binary logit model
Coefficients of attributes
Logit with multiple alternatives
Nonlinear specifications
71/101

| Nonlinear |           | transformations |        |          | of     | the variables |      |
| --------- | --------- | --------------- | ------ | -------- | ------ | ------------- | ---- |
|           | Example   | with            | travel | time     |        |               |      |
|           | ▶ Compare |                 | a trip | of 5 min | with a | trip of 10    | min. |
▶
|     | Compare   |             | a trip | of 120 min | with    | a trip of 125 | min. |
| --- | --------- | ----------- | ------ | ---------- | ------- | ------------- | ---- |
|     | ▶ Utility | difference: |        | β · 5      | min, in | both cases.   |      |
T
|     | Behavioral |     | assumption |     |     |     |     |
| --- | ---------- | --- | ---------- | --- | --- | --- | --- |
One more minute of travel is not perceived the same way for short trips as for
|     | long trips. |     |     |     |     |     |     |
| --- | ----------- | --- | --- | --- | --- | --- | --- |
72/101

| Nonlinear | transformations | of the | variables |     |
| --------- | --------------- | ------ | --------- | --- |
Utility
1
|     |     |     | Travel | time |
| --- | --- | --- | ------ | ---- |
|     |     | 2 4 | 6 8    | 10   |
−1
−2
73/101

| Nonlinear  | transformations | of the variables |                |             |
| ---------- | --------------- | ---------------- | -------------- | ----------- |
| Assumption | 1: the marginal | impact           | of travel time | is constant |
|            |                 | V = β time       | +···           |             |
|            |                 | in T             | in             |             |
Assumption 2: the marginal impact of travel time decreases with
| travel | time |             |       |     |
| ------ | ---- | ----------- | ----- | --- |
|        | V    | = β ln(time | )+··· |     |
|        |      | in T        | in    |     |
74/101

| Nonlinear | transformations     |     | of the     | variables          |     |
| --------- | ------------------- | --- | ---------- | ------------------ | --- |
| Data      | can be preprocessed |     | to account | for nonlinearities |     |
(cid:88)
|     |     | V = V(h(z | ,s )) = | β (h(z | ,s )) |
| --- | --- | --------- | ------- | ------ | ----- |
|     |     | in        | in n    | k in   | n k   |
k
Note
Interactions between attributes and socio-economic characteristics are a special
| case of | h.  |     |     |     |     |
| ------- | --- | --- | --- | --- | --- |
75/101

| Piecewise linear   | specification |             |             |      |
| ------------------ | ------------- | ----------- | ----------- | ---- |
| Again: sensitivity | to travel     | time varies | with travel | time |
▶
| Log transform | is not | the only specification. |     |     |
| ------------- | ------ | ----------------------- | --- | --- |
▶ Another possibility: split the range of values of the variable.
▶
| Each category | is associated | with a different | coefficient. |     |
| ------------- | ------------- | ---------------- | ------------ | --- |
76/101

Piecewise linear specification
0
−1
ytilitU
−2
−3
| 0 50 | 100 150 | 200 250 | 300 |
| ---- | ------- | ------- | --- |
|      | Travel  | time    |     |
77/101

| Piecewise linear specification |     |     |
| ------------------------------ | --- | --- |
Procedure
| ▶ Select breakpoints | γ < γ | < ... < γ . |
| -------------------- | ----- | ----------- |
|                      | 1 2   | L           |
▶
| Define new variables. |     |     |
| --------------------- | --- | --- |
78/101

|     | γ   | γ   | ···  | γ   |
| --- | --- | --- | ---- | --- |
|     | 1   | 2   |      | L   |
| 0   | x   |     | γ −γ |     |
|     | in2 |     | 2 1  |     |
Piecewise linear specification
x
in
79/101

|     |     |     |     | 0   | x   | γ −γ |
| --- | --- | --- | --- | --- | --- | ---- |
|     |     |     |     |     | in2 | 2 1  |
Piecewise linear specification
x
in
| γ   | γ   | ··· | γ   |     |     |     |
| --- | --- | --- | --- | --- | --- | --- |
| 1   | 2   |     | L   |     |     |     |
79/101

Piecewise linear specification
x
in
|     | γ   | γ   | ···  | γ   |
| --- | --- | --- | ---- | --- |
|     | 1   | 2   |      | L   |
| 0   | x   |     | γ −γ |     |
|     | in2 |     | 2 1  |     |
79/101

| Piecewise | linear specification |     |     |     |     |     |
| --------- | -------------------- | --- | --- | --- | --- | --- |
Formulation
|     |     |     |     | γ   | γ ··· γ | x   |
| --- | --- | --- | --- | --- | ------- | --- |
|     |     |     |     | 1   | 2 L     | in  |
(cid:12)
|     | x if x       | < γ , |     | x     |      |     |
| --- | ------------ | ----- | --- | ----- | ---- | --- |
|     | in in        | 1     |     | 0 in2 | γ −γ |     |
| x   | =            |       |     |       | 2 1  |     |
| in1 | γ otherwise. |       |     |       |      |     |
1

|     |  0 | if x < γ | ,   |     |     |     |
| --- | --- | -------- | --- | --- | --- | --- |
|     |     | in       | ℓ−1 |     |     |     |
⩽
| x   | = x −γ   | if γ       | x < γ | ,   |     |     |
| --- | -------- | ---------- | ----- | --- | --- | --- |
| inℓ |  in ℓ−1 | ℓ−1        | in    | ℓ   |     |     |
|     | γ −γ     | otherwise. |       |     |     |     |
|     | ℓ ℓ−1    |            |       |     |     |     |
(cid:12)
|     | 0   | if x < γ , |     |     |     |     |
| --- | --- | ---------- | --- | --- | --- | --- |
|     | =   | in L       |     |     |     |     |
x
| in(L+1) | x −γ | otherwise. |     |     |     |     |
| ------- | ---- | ---------- | --- | --- | --- | --- |
|         | in L |            |     |     |     |     |
80/101

| Piecewise  | linear specification |     |     |     |     |     |     |
| ---------- | -------------------- | --- | --- | --- | --- | --- | --- |
| Equivalent | formulations         |     |     |     |     |     |     |
(cid:12)
|     | x if x  | < γ , |     |       |       |     |     |
| --- | ------- | ----- | --- | ----- | ----- | --- | --- |
| x   | = in in | 1     |     | min(x | ,γ ). |     |     |
| in1 |         |       |     |       | in 1  |     |     |
γ otherwise.
1

|     |  0      | if x < γ   | ,     |               |     |        |           |
| --- | -------- | ---------- | ----- | ------------- | --- | ------ | --------- |
|     |          | in         | ℓ−1   |               |     |        |           |
| x   | = x −γ   | if γ ⩽     | x < γ | , max(0,min(x |     | −γ     | ,γ −γ )). |
| inℓ |  in ℓ−1 | ℓ−1        | in ℓ  |               |     | in ℓ−1 | ℓ ℓ−1     |
|     | γ −γ     | otherwise. |       |               |     |        |           |
|     | ℓ ℓ−1    |            |       |               |     |        |           |
(cid:12)
|     | 0   | if x < γ |     |     |     |     |     |
| --- | --- | -------- | --- | --- | --- | --- | --- |
in L
| x       | =    |           |     | max(0,x | −γ  | ).  |     |
| ------- | ---- | --------- | --- | ------- | --- | --- | --- |
| in(L+1) | x −γ | otherwise |     |         | in  | L   |     |
|         | in L |           |     |         |     |     |     |
81/101

| Piecewise | linear | specification |     |     |     |     |
| --------- | ------ | ------------- | --- | --- | --- | --- |
Examples
| γ =     | 90, γ =  | 180, γ = 270. |     | γ = 1, | γ = 5, | γ = 10.    |
| ------- | -------- | ------------- | --- | ------ | ------ | ---------- |
| 1       | 2        | 3             |     | 1      | 2      | 3          |
|         | x 50     | 100 200       | 300 |        | x      | 0.5 4 8 12 |
|         | in       |               |     |        | in     |            |
|         | x 50     | 90 90         | 90  |        | x      | 0.5 1 1 1  |
|         | in1      |               |     |        | in1    |            |
|         | x 0      | 10 90         | 90  |        | x      | 0 3 4 4    |
|         | in2      |               |     |        | in2    |            |
|         | x 0      | 0 20          | 90  |        | x      | 0 0 3 5    |
|         | in3      |               |     |        | in3    |            |
|         | x 0      | 0 0           | 30  |        | x      | 0 0 0 2    |
|         | in4      |               |     |        | in4    |            |
| Utility | function |               |     |        |        |            |
(cid:88)L+1
|     |     |     | V = | β x . |     |     |
| --- | --- | --- | --- | ----- | --- | --- |
|     |     |     | in  | ℓ inℓ |     |     |
ℓ=1
82/101

Box-Cox transforms
Box and Cox (1964)
V = βB(x ;λ)+···
in in
where 
 xλ −1
 in if λ ̸= 0,
λ
B(x ;λ) =
in 

lnx if λ = 0,
in
and x > 0.
in
83/101

| Box-Cox transforms |          |             |               |         |
| ------------------ | -------- | ----------- | ------------- | ------- |
| Continuity         | at λ = 0 |             |               |         |
| The definition     | at λ = 0 | is obtained | by continuity | because |
xλ
−1
|     |     | lim in | = lnx , | x > 0. |
| --- | --- | ------ | ------- | ------ |
|     |     |        | in      | in     |
λ→0 λ
84/101

| Box-Cox   | transforms    |      |
| --------- | ------------- | ---- |
| Convexity | and concavity | in x |
in
∂B(x ;λ)
in xλ−1,
=
∂x in
in
∂2B(x ;λ)
in
= (λ−1)xλ−2.
∂x2 in
in
| For x > | 0:  |     |
| ------- | --- | --- |
in
▶
| B is | strictly convex | if λ > 1; |
| ---- | --------------- | --------- |
▶
| B is | linear if λ = 1; |     |
| ---- | ---------------- | --- |
▶
| B is | strictly concave | if λ < 1. |
| ---- | ---------------- | --------- |
85/101

Box-Cox transforms
8
6
4
2
0
−2
−4
0 1 2 3 4
Travel time
ytilitU
λ = −1
λ = 0
λ = 0.5
λ = 1
λ = 2
86/101

Summary
▶
| ε i.i.d. | EV(η, µ). |     |     |     |
| -------- | --------- | --- | --- | --- |
in
▶
| Derivation: | from binary | logit to multiple | alternatives. |     |
| ----------- | ----------- | ----------------- | ------------- | --- |
▶
| Identification | issues | due to the latent | nature | of utility. |
| -------------- | ------ | ----------------- | ------ | ----------- |
▶
| Normalization: | η does | not play any | role. |     |
| -------------- | ------ | ------------ | ----- | --- |
n
▶
| Normalization: | β = | −1: moneymetric | specification. |     |
| -------------- | --- | --------------- | -------------- | --- |
c
▶
| Alternative | Specific Constants. |     |     |     |
| ----------- | ------------------- | --- | --- | --- |
▶
| Continuous/quantitative |     | vs discrete/qualitative |     | variables. |
| ----------------------- | --- | ----------------------- | --- | ---------- |
▶
| Nonlinear | specifications. |     |     |     |
| --------- | --------------- | --- | --- | --- |
Appendices
▶
| The binary | probit model. |     |     |     |
| ---------- | ------------- | --- | --- | --- |
▶
| Gumbel’s | theorem. |     |     |     |
| -------- | -------- | --- | --- | --- |
87/101

| Appendix    | I: the probit | model                |     |
| ----------- | ------------- | -------------------- | --- |
| Assumption: | similar       | to linear regression |     |
ε and ε are the sum of many r.v. capturing unobserved attributes (e.g. mood,
| in           | jn            |                   |         |
| ------------ | ------------- | ----------------- | ------- |
| experience), | measurement   | and specification | errors. |
| Central      | limit theorem |                   |         |
The sum of many i.i.d. random variables approximately follows a normal
N(η,σ2).
distribution:
88/101

| The normal  | distribution |          | N(η,σ2)     |     |
| ----------- | ------------ | -------- | ----------- | --- |
| Probability | density      | function | (pdf)       |     |
|             |              |          | 1           | η)2 |
|             |              | f(t)     | = √ e−1 (t− | .   |
2 σ
σ 2π
| Cumulative | distribution | function | (CDF) |     |
| ---------- | ------------ | -------- | ----- | --- |
(cid:90)
c
⩾
|     |     | P(c | ε) = F(c) = | f(t)dt. |
| --- | --- | --- | ----------- | ------- |
−∞
89/101

| The normal | distribution |     |     |        |     |     |
| ---------- | ------------ | --- | --- | ------ | --- | --- |
| pdf N(0,1) |              |     | CDF | N(0,1) |     |     |
0.8
0.3
0.6
0.2
0.4
0.1
0.2
| −3 −2 | −1  | 1 2 | 3 −3 | −2 −1 | 1 2 | 3   |
| ----- | --- | --- | ---- | ----- | --- | --- |
90/101

The distribution
Assumptions
▶ ε and ε are normally distributed, with variance σ2 and σ2, respectively,
| in jn |     |     |     |
| ----- | --- | --- | --- |
i j
| and covariance | σ . |     |     |
| -------------- | --- | --- | --- |
ij
▶
| Note: identical | distribution | across n. |     |
| --------------- | ------------ | --------- | --- |
▶
If an alternative specific constant is in the model, their mean can be
| assumed to | be any constant. |     |     |
| ---------- | ---------------- | --- | --- |
▶
| ε = ε −ε | is also normally | distributed, | with variance |
| -------- | ---------------- | ------------ | ------------- |
| n jn     | in               |              |               |
|          |                  | σ2 σ2 +σ2    |               |
|          |                  | =            | −2σ .         |
|          |                  | i            | j ij          |
91/101

| The binary | probit | model |     |     |     |     |     |     |     |
| ---------- | ------ | ----- | --- | --- | --- | --- | --- | --- | --- |
Choice model
|            | P (i|{i,j}) |       | = Pr(ε | ⩽   | V −V | ) = F | (V −V | ).  |     |
| ---------- | ----------- | ----- | ------ | --- | ---- | ----- | ----- | --- | --- |
|            | n           |       |        | n   | in   | jn    | ε in  | jn  |     |
| The binary | probit      | model |        |     |      |       |       |     |     |
(cid:90)
|             |     | (cid:18) |      | (cid:19) |     | (Vin−Vjn)/σ |     | (cid:18) | (cid:19) |
| ----------- | --- | -------- | ---- | -------- | --- | ----------- | --- | -------- | -------- |
|             |     |          | V −V |          | 1   |             |     | 1        |          |
| P (i|{i,j}) | =   | Φ        | in   | jn =     | √   |             | exp | − u2     | du.      |
n
|     |     |     | σ   |     | 2π  |     |     | 2   |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
−∞
92/101

| Appendix | II: Gumbel | theorem |     |
| -------- | ---------- | ------- | --- |
Motivation
▶
X ,...,X i.i.d.
1 n
| ▶ f | (x) = f(x), F | (x) = F(x), | i = 1,...,n |
| --- | ------------- | ----------- | ----------- |
| Xi  | Xi            |             |             |
▶
| X′              | = max(X ,...,X | ).  |     |
| --------------- | -------------- | --- | --- |
|                 | n 1            | n   |     |
| ▶ Applications: |                |     |     |
▶
rainfall,
▶ floods,
▶
earthquakes,
▶
air pollution,
▶ ...
93/101

Extreme value distribution
▶
| X′ = max(X ,...,X |     | ).  |     |     |     |     |
| ----------------- | --- | --- | --- | --- | --- | --- |
n 1 n
▶ F(x)n.
F = Indeed
X′ n
|      | ⩽   |          | ⩽   |       | ⩽        | ⩽   |
| ---- | --- | -------- | --- | ----- | -------- | --- |
| P(X′ |     | x) = P(X |     | x)P(X | x)...P(X | x). |
|      | n   |          | 1   | 2     |          | n   |
▶ Warning: if n → ∞
(cid:12)
|     |     |       |       | 1 if | F(x) = 1, |     |
| --- | --- | ----- | ----- | ---- | --------- | --- |
|     |     | lim F | (x) = |      |           |     |
|     |     |       | X ′   | 0 if | F(x) < 1. |     |
|     |     | n→∞   | n     |      |           |     |
Degenerate distribution (if you a die sufficiently many times, the maximum
score will always be 6).
94/101

| Extreme value | distribution            |              |             |
| ------------- | ----------------------- | ------------ | ----------- |
| ▶ We want     | a limiting distribution | which is non | degenerate. |
▶
Limiting distribution of some sequence of transformed “reduced” values.
| ▶ For instance | a X′ +b | .   |     |
| -------------- | ------- | --- | --- |
|                | n       | n   |     |
n
▶
| a , b | do not depend | on x. |     |
| ----- | ------------- | ----- | --- |
n n
| ▶ CDF | of limiting distribution: | G(x). |     |
| ----- | ------------------------- | ----- | --- |
▶
| Let’s | identify desired | properties. |     |
| ----- | ---------------- | ----------- | --- |
95/101

Extreme value distribution
X ... X max(X ,...,X )
1 n 1 n
X ... X max(X ,...,X )
n+1 2n n+1 2n
. .
. .
. .
X ... X max(X ,...,X )
(i−1)n+1 in (i−1)n+1 in
. .
. .
. .
X ... X max(X ,...,X )
(N−1)n+1 Nn (N−1)n+1 Nn
Two ways of seeing max(X ,...,X ) when n → ∞.
1 Nn
1. As a max of many X , the CDF should look like G(a x +b ).
i N N
2. The CDF of the max of each row is G(x).
3. So the CDF of the max of all rows is G(x)N.
96/101

Extreme value distribution
| Stability postulate (Fr´echet, | 1927):  |             |     |
| ------------------------------ | ------- | ----------- | --- |
|                                | G(x)N = | G(a x +b ). |     |
N N
We consider here the case a = 1 to obtain the so-called “type I extreme value
N
distribution”
|     | G(x)N | = G(x +b ). |     |
| --- | ----- | ----------- | --- |
N
We have also
| G(x)MN | = G(x +b | )M = G(x +b | +b ), |
| ------ | -------- | ----------- | ----- |
|        |          | N           | N M   |
| G(x)MN | = G(x +b | ).          |       |
MN
97/101

| Extreme | value distribution |     |     |     |
| ------- | ------------------ | --- | --- | --- |
Therefore
|     |     | G(x +b | +b ) = G(x | +b ), |
| --- | --- | ------ | ---------- | ----- |
|     |     |        | N M        | MN    |
that is
|         |           |             | b +b = b | ,   |
| ------- | --------- | ----------- | -------- | --- |
|         |           |             | N M      | MN  |
| so that | b must be | of the form |          |     |
N
b = −µ′lnN,
N
| and the    | stability postulate | becomes  |                |     |
| ---------- | ------------------- | -------- | -------------- | --- |
|            |                     | G(x)N    | = G(x −µ′lnN). |     |
| Let’s take | the logarithm       | twice... |                |     |
98/101

| Extreme | value distribution |       |          |     |
| ------- | ------------------ | ----- | -------- | --- |
|         |                    | G(x)N | −µ′lnN). |     |
= G(x
−µ′lnN).
|          |             | N lnG(x)  | = lnG(x        |          |
| -------- | ----------- | --------- | -------------- | -------- |
| Warning: | G is a CDF, | so G(x)   | ⩽ 1 and lnG(x) | ⩽ 0, ∀x. |
|          |             | −N lnG(x) | = −lnG(x       | −µ′lnN). |
−µ′lnN)).
|             | lnN           | +ln(−lnG(x)) | = ln(−lnG(x |          |
| ----------- | ------------- | ------------ | ----------- | -------- |
| Define h(x) | = ln(−lnG(x)) | to           | obtain      |          |
|             |               | lnN          | +h(x) = h(x | −µ′lnN). |
h is affine.
99/101

Extreme value distribution
| lnN     | +h(x) = h(x | −µ′lnN),   |
| ------- | ----------- | ---------- |
|         | h(x) = αx   | +β,        |
|         | h(0) = β,   |            |
| lnN +αx | +β = α(x    | −µ′lnN)+β, |
|         | α = −       | 1 .        |
µ′
Therefore
x
|     | h(x) = h(0)− | .   |
| --- | ------------ | --- |
µ′
G is increasing in x (CDF), so h is decreasing in x. Therefore, µ′ > 0.
100/101

| Extreme value | distribution |     |     |     |     |     |
| ------------- | ------------ | --- | --- | --- | --- | --- |
x
|     |     | h(x) | = ln(−lnG(x)) | = h(0)− | .   |     |
| --- | --- | ---- | ------------- | ------- | --- | --- |
µ′
|     |         |     | (cid:18)  | x (cid:19)       | (cid:18) x −µ′h(0) | (cid:19) |
| --- | ------- | --- | --------- | ---------------- | ------------------ | -------- |
|     | −lnG(x) | =   | exp h(0)− | = exp            | −                  | .        |
|     |         |     |           | µ′               | µ′                 |          |
|     |         |     | (cid:18)  | (cid:18) −µ′h(0) | (cid:19)(cid:19)   |          |
x
|     |     | G(x) | = exp −exp | −   | .   |     |
| --- | --- | ---- | ---------- | --- | --- | --- |
µ′
| 1/µ′    |     | µ′h(0) |                 |        |     |     |
| ------- | --- | ------ | --------------- | ------ | --- | --- |
| Let µ = | and | η =    | = ln(−lnG(0))/µ |        |     |     |
|         |     | G(x)   | = exp(−exp(−µ(x | −η))). |     |     |
101/101