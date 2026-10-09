Mathematical Modeling of Behavior  | Assignment (2026-2027) | Michel Bierlaire | TAs: | Candice Baud, Anne-Valerie Preto, Andras Horkay, Luc Steiner |
Course assignment | September 8, 2026 | Aim and content |


The objective of this assignment is to develop a discrete choice model of
transport mode choice in the London metropolitan area. The assignment
follows an iterative modelling approach. You will start with a simple
model and gradually introduce new variables, interactions, non-linear specifications,
and more flexible error structures.
| ----------------- | --- | -------- | -------------- | ----- | ----------- | --- | --- | --- |
The goal is not to build the most complicated model. The goal is to learn
how to specify, estimate, test, and improve a model step by step. For each
new specification, you should understand the assumptions that are intro-
duced, checkwhethertheyaresupportedbythedata, andevaluatewhether
the model improves on the previous one. A simple model that is correctly
specified, identified, tested, and interpreted is better than a complex model
| that | cannot | be  | properly | justified | or estimated. |     |     |     |
| ---- | ------ | --- | -------- | --------------- | ------------- | --- | --- | --- |
A Python notebook will be provided. It follows the sequence of models
described in the assignment and contains the main structure needed to es-
timate and evaluate them. The notebook is a support tool. It does not
replace the interpretation of the results or the justification of the modelling
choices. During the exercise sessions, the teaching team will answer ques-
tions about the data, the implementation, and the interpretation of the
models.
The description of the data can be found on Moodle under the Datasets
link (London passenger mode choice, LPMC). Each group is assigned a dif-
Assignments
| ferent | sample | of  | the original | LPMC | data, | available | under | the |
| ------ | ------ | --- | ------------ | ---- | ----- | --------- | ----- | --- |
section on Moodle. All alternatives are available to all individuals.
1

Mathematical Modeling of Behavior
Assignment (2026-2027)
Michel Bierlaire.
TAs: Candice Baud, Anne-Valerie Preto, Andras Horkay, Luc Steiner
Course assignment | September 8, 2026
Learning objectives
By completing the assignment, you should be able to:
•
construct increasingly rich discrete choice models starting from a sim-
ple and interpretable specification;
•
explain the behavioral and statistical assumptions associated with
each model extension;
•
interpret estimation results and identify potential specification, nor-
malization, estimation, and identification problems;
•
compare competing specifications using appropriate statistical tests
and diagnostic measures;
•
assess whether model predictions and substitution patterns are be-
haviorally plausible;
•
justify why a specification was retained or rejected;
•
use the final model to calculate market shares and analyze policy
scenarios; and
•
critically evaluate both your own model and the models proposed by
other groups.
Intermediate and final presentations
Two group presentations will be organized during the semester:
October 13, 2026 — Intermediate assessment. Groupswillpresenttheir
assessment of the main dificulties encountered in the dataset and in
the modelling process, based on the work completed up to and in-
cluding Model 2. The 5 minute presentation should discuss the first
tested specifications, the data limitations, unexpected estimation re-
sults, possible identification issues, and the tests used to compare the
models.
2

|        |              | Mathematical |                            | Modeling |             | of     | Behavior |             |     |
| ------ | ------------ | ------------ | -------------------------- | -------- | ----------- | ------ | -------- | ----------- | --- |
|        |              |              | Assignment                 |          | (2026-2027) |        |          |             |     |
|        |              |              | Michel                     |          | Bierlaire.  |        |          |             |     |
|        | TAs: Candice |              | Baud, Anne-Valerie |          | Preto,      | Andras | Horkay,  | Luc Steiner |     |
| Course | assignment   |              | | September                | 8,       | 2026        |        |          |             |     |
December 1, 2026 — Final model presentation. Groups will present
their final mixture model and the iterative process that led to it.
The presentation should explain what was learned from the tested
specifications, what did not work, which tests were passed or failed,
which estimation or identification dificulties were encountered, and
why the final model was retained. Groups should also report the
predicted market shares and the main results of the policy scenarios.
During the final presentations, students are expected to critically assess the
modelsproposedbytheothergroups. Relevantquestionsfromtheteaching
team will be asked to all groups, and the students are expected to answer
them. The following questions can serve as a guide for the assessment of
the models:
•
Does the proposed specification correspond to the type of model re-
|     | quested | in the | assignment? |     |     |     |     |     |     |
| --- | ------- | ------ | ----------- | --- | --- | --- | --- | --- | --- |
• Is the progression from the initial specification to the final model
|     | clearly justified? |     |     |     |     |     |     |     |     |
| --- | ------------------------ | --- | --- | --- | --- | --- | --- | --- | --- |
• Are the behavioral assumptions and predicted substitution patterns
plausible?
•
|     | Has the      | model    | been compared |     | with          | appropriate |             | benchmarks | and |
| --- | ------------ | -------- | ------------- | --- | ------------- | ----------- | ----------- | ---------- | --- |
|     | tested using | suitable | statistical   |     | or predictive |             | procedures? |            |     |
• Are the reported market shares and policy responses plausible and
|            | supported | by  | the results? |     |     |     |     |     |     |
| ---------- | --------- | --- | ------------ | --- | --- | --- | --- | --- | --- |
| Submission |           | and | comments     |     |     |     |     |     |     |
Each group must submit a two-page PDF on Moodle under Assignments
by November 30, 2026 at noon. The file must be named Group XX.pdf,
where XX is the group number. Only the PDF must be submitted. The
teaching team may request the code or other files if necessary. The sum-
mary must be written in English, and all group members must contribute
3

|        |            |         | Mathematical |                      |        | Modeling    |        | of Behavior |             |
| ------ | ---------- | ------- | ------------ | -------------------- | ------ | ----------- | ------ | ----------- | ----------- |
|        |            |         |              | Assignment           |        | (2026-2027) |        |             |             |
|        |            |         |              |                      | Michel | Bierlaire.  |        |             |             |
|        | TAs:       | Candice | Baud,        | Anne-Valerie |        | Preto,      | Andras | Horkay,     | Luc Steiner |
| Course | assignment |         |              | | September          |        | 8, 2026     |        |             |             |
to its preparation.
The summary is intended for readers who are already familiar with the
assignment and the LPMC data. It is therefore not necessary to describe
the origin of the data or to review the general theory of discrete choice
| models. | The | summary |     | should | report: |     |     |     |     |
| ------- | --- | ------- | --- | ------ | ------- | --- | --- | --- | --- |
•
the main characteristics of the group’s dataset and the dificulties
encountered;
• the modelling process from Model 0 to Model 5 and the main lessons
|     | learned | from | the | specifications |     | that | were | tested; |     |
| --- | ------- | ---- | --- | -------------------- | --- | ---- | ---- | ------- | --- |
•
the final mixture model and its behavioral interpretation. We recom-
mend including a diagram of the model structure and a table report-
|     | ing the | main     | estimation |           | results | and      | their  | interpretation; |     |
| --- | ------- | -------- | ---------- | --------- | ------- | -------- | ------ | --------------- | --- |
|     | • the   | observed | and        | predicted |         | weighted | market | shares;         |     |
• the main results of the policy scenarios, including revenue, values of
|        | time, | and        | elasticities. |          |     |     |     |     |     |
| ------ | ----- | ---------- | ------------- | -------- | --- | --- | --- | --- | --- |
| Advice |       | and common |               | mistakes |     |     |     |     |     |
• When modifying a model from a previous task, verify that the new
|     | specification |     | is  | correctly | identified |     | and | normalized. |     |
| --- | ------------------- | --- | --- | --------- | ---------------- | --- | --- | ----------- | --- |
•
Once a model has been selected as the preferred model, use it as the
|     | base | specification |     | for | the next | task. |     |     |     |
| --- | ---- | ------------------- | --- | --- | -------- | ----- | --- | --- | --- |
•
There is no need to write unnecessarily complex code. The laboratory
sessions provide the main examples needed to answer the questions.
4

 Mathematical |                      |        | Modeling    | of Behavior    |             |
| ------ | ---- | ---------- | ------------ | -------------------- | ------ | ----------- | -------------- | ----------- |
              | Assignment           |        | (2026-2027) |                |             |
              |                      | Michel | Bierlaire.  |                |             |
|        | TAs: | Candice    | Baud,        | Anne-Valerie |        | Preto,      | Andras Horkay, | Luc Steiner |
| Course |      | assignment |              | | September          |        | 8, 2026     |                |             |
Tasks
Model 0 Start with a model specification that includes alternative spe-
cific constants, and cost and travel time of the dife)erent alternatives asso-
| ciated | with | generic | parameters. |     |     |     |     |     |
| ------ | ---- | ------- | ----------- | --- | --- | --- | --- | --- |
Calculate the total public transport duration as the sum of dur pt access,
dur pt rail, dur pt bus, and dur pt int. Similarly, calculate the total
driving cost as the sum of cost driving fuel and cost driving ccharge.
Report both the specification (i.e., the utility functions) and the estimation
results (parameter values, t-tests or p-values, null and final log likelihoods).
1. Comment on the estimation output (sign and significance of all pa-
rameters).
Model 1 Using Model 0 as the base model, include alternative-specific
parameters for one of the attributes of Model 0. Report both the specifi-
| cation | and | the | estimation |     | results | (as defined | previously). |     |
| ------ | --- | --- | ---------- | --- | ------- | ----------------- | ------------ | --- |
1. State the underlying assumption of defining alternative-specific pa-
|     | rameters |     | in this | specific | situation. |     |     |     |
| --- | -------- | --- | ------- | -------------- | ---------- | --- | --- | --- |
2. Comment on the estimation output (as defined previously, including
|     | any | changes | from | the | previous | model). |     |     |
| --- | --- | ------- | ---- | --- | -------- | ------- | --- | --- |
3. Compare Model 0 and Model 1 with an appropriate statistical test.
Justify your choice of test. State the null hypothesis and the result
|     | of  | the test. | Denote | the | preferred | model | as Model pref | .   |
| --- | --- | --------- | ------ | --- | --------- | ----- | ------------- | --- |
Model 2 Using Model as the base model, choose a socioeconomic char-
pref
acteristic and define two model specifications. In the first specification,
interact the socioeconomic characteristic with an alternative-specific con-
stant. In the second specification, interact it with an alternative attribute.
Report both the specification and the estimation results (parameter values,
| t-tests | or  | p-values, | null | and | final | log likelihoods). |     |     |
| ------- | --- | --------- | ---- | --- | ----------- | ----------------- | --- | --- |
5

|        |            |         | Mathematical |                      |        | Modeling    | of Behavior    |             |
| ------ | ---------- | ------- | ------------ | -------------------- | ------ | ----------- | -------------- | ----------- |
|        |            |         |              | Assignment           |        | (2026-2027) |                |             |
|        |            |         |              |                      | Michel | Bierlaire.  |                |             |
|        | TAs:       | Candice | Baud,        | Anne-Valerie |        | Preto,      | Andras Horkay, | Luc Steiner |
| Course | assignment |         |              | | September          |        | 8, 2026     |                |             |
1. State the underlying assumptions of the additional attribute and in-
|     | teraction  | in  | this   | specific | situation. |        |                                |     |
| --- | ---------- | --- | ------ | -------------- | ---------- | ------ | ------------------------------ | --- |
|     | 2. Comment |     | on the | estimation     |            | output | (as defined previously). |     |
3. Compare Model and Model 2 (both specifications) with an ap-
pref
propriate statistical test. Justify your choice of test. State the null
hypothesis and the result of the test. Denote the preferred model as
|     | Model | .   |     |     |     |     |     |     |
| --- | ----- | --- | --- | --- | --- | --- | --- | --- |
pref
Model 3 Using Model as the base model, include an appropriate non-
pref
linear transformation of on the time variables. Report both the specifica-
| tion | and the | estimation |     | results |     | (as defined | previously). |     |
| ---- | ------- | ---------- | --- | ------- | --- | ----------------- | ------------ | --- |
1. State the underlying assumption of the non-linear specification de-
|     | fined | in this | situation. |            |     |        |                                |     |
| --- | ----------- | ------- | ---------- | ---------- | --- | ------ | ------------------------------ | --- |
|     | 2. Comment  |         | on the     | estimation |     | output | (as defined previously). |     |
3. Compare Model and Model 3 with an appropriate statistical test.
pref
Justify your choice of test. State the null hypothesis and the result
|     | of the | test. | Denote | the | preferred | model | as Model | .   |
| --- | ------ | ----- | ------ | --- | --------- | ----- | -------- | --- |
pref
Model 4 Using Model as the base model, propose and estimate a
pref
nested logit model and a cross-nested logit model. Report both structures
using graphs, together with the specifications and estimation results.
1. State the underlying assumption of the proposed nesting structure in
|     | this       | specific | situation. |            |     |        |                                |     |
| --- | ---------- | -------------- | ---------- | ---------- | --- | ------ | ------------------------------ | --- |
|     | 2. Comment |                | on the     | estimation |     | output | (as defined previously). |     |
3. Compare Model and Model 4 with an appropriate statistical test.
pref
Justify your choice of test. State the null hypothesis and the result
|     | of the | test. | Denote | the | preferred | model | as Model | .   |
| --- | ------ | ----- | ------ | --- | --------- | ----- | -------- | --- |
pref
6

Mathematical Modeling of Behavior
Assignment (2026-2027)
Michel Bierlaire.
TAs: Candice Baud, Anne-Valerie Preto, Andras Horkay, Luc Steiner
Course assignment | September 8, 2026
Model 5 Using the best model from Model 3 as a starting point, propose
a mixture model that captures correlations across alternatives similar to
the one modeled in the best nested structure of Model 4. Relax the inde-
pendence of the error terms across alternatives. Estimate the model and
report its structure and results. Denote this mixture model as Model
pref
and use it as the reference model for all remaining questions.
1. State the behavioral assumption behind your proposed mixture spec-
ification. What type of correlation does it capture?
2. Comment on the estimation output (as defined previously).
3. Compare the estimates of this model with the estimates from the best
performing model from Model 4.
Market shares Assume that stratified random sampling was used to pro-
duce your sample. We consider the following strata:
• S1: females aged 42 years or younger;
• S2: females aged 43 years or older;
• S3: males aged 42 years or younger;
• S4: males aged 43 years or older.
Table 1 gives the size of each category in the full population.
Age < 43 Age ≥ 43
Male 2’926’408 1’379’198
Female 2’841’376 1’519’948
Table 1: London population estimates in 2015 (Source: ONS)
1. Report the size and weight of each stratum in your sample.
7

|     |     |     | Mathematical |     | Modeling    | of Behavior |     |     |
| --- | --- | --- | ------------ | --- | ----------- | ----------- | --- | --- |
|     |     |     | Assignment   |     | (2026-2027) |             |     |     |
Michel Bierlaire.
|        | TAs:       | Candice | Baud, Anne-Valerie |     | Preto,  | Andras | Horkay, | Luc Steiner |
| ------ | ---------- | ------- | -------------------------- | --- | ------- | ------ | ------- | ----------- |
| Course | assignment |         | | September                |     | 8, 2026 |        |         |             |
2. Using Model and the weights of your strata, compute the predicted
pref
market share of each mode and their confidence intervals. Do the
|     | obtained | results | match | your | expectations? |     |     |     |
| --- | -------- | ------- | ----- | ---- | ------------- | --- | --- | --- |
3. Compare the market shares predicted by Model with the weighted
pref
|     | market | shares | computed | using | the actual | choices. |     |     |
| --- | ------ | ------ | -------- | ----- | ---------- | -------- | --- | --- |
Forecasting Consider the following scenarios: (i) an additional charge of
£
1.5 for car users ; and (ii) A 20% decrease in public transport cost.
1. Report the market shares predicted by Model for each scenario.
pref
Do they match your expectations? Compare those with the original
|     | market | shares. |     |     |     |     |     |     |
| --- | ------ | ------- | --- | --- | --- | --- | --- | --- |
2. Which scenario is the most efe)ective policy if the goal is to decrease
|     | the share | of  | car? Explain | why. |     |     |     |     |
| --- | --------- | --- | ------------ | ---- | --- | --- | --- | --- |
3. Which scenario reports the highest public transportation total rev-
enue? Explain why. Is it higher than the total revenue obtained
|     | without | any | of the policies? |     | Can you | explain | why? |     |
| --- | ------- | --- | ---------------- | --- | ------- | ------- | ---- | --- |
4. Calculate the average value of time for car and public transportation.
|     | Comment | on  | the obtained |     | results. |     |     |     |
| --- | ------- | --- | ------------ | --- | -------- | --- | --- | --- |
5. Compute the direct and cross aggregate elasticities of car cost and
public transport cost and comment on the obtained results. Report
|     | the normalization |     | factors. |     |     |     |     |     |
| --- | ----------------- | --- | -------- | --- | --- | --- | --- | --- |
8