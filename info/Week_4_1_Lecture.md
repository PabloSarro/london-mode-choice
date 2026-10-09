|         |     |         |         |              | The | Logit         | Model       |     |
| ------- | --- | ------- | ------- | ------------ | --- | ------------- | ----------- | --- |
|         |     |         |         | Guided       |     | self-learning | session     |     |
|         |     |         |         | Mathematical |     | Modeling      | of Behavior |     |
| Purpose |     | of this | session |              |     |               |             |     |
This document guides you through the logit lecture. It does not replace the slides or the exercises.
It tells you what to study, provides the explanations normally given in class, and indicates when
| to stop | and | solve an | exercise. |     |     |     |     |     |
| ------- | --- | -------- | --------- | --- | --- | --- | --- | --- |
Thesessioncontainsfourperiodsofapproximately45minutes. Thesuggestedtimesareindicative.
Do not sacrifice understanding merely to follow the clock. If an activity takes much longer than
| expected, | record | the | difficulty | and | continue | with the | next block. |     |
| --------- | ------ | --- | ---------- | --- | -------- | -------- | ----------- | --- |
You need:
| •   | this document; |            |     |                  |        |     |     |     |
| --- | -------------- | ---------- | --- | ---------------- | ------ | --- | --- | --- |
| •   | the PDF        | of Lecture | 04, | The logit        | model; |     |     |     |
| •   | the Logit      | exercises  | and | their solutions. |        |     |     |     |
Work through the activities in order. Attempt every required exercise before reading its solution.
Optional activities are provided for students who finish the required path early.
|     | Period |     | Main | topic  |         |           |       | Time   |
| --- | ------ | --- | ---- | ------ | ------- | --------- | ----- | ------ |
|     | 1      |     | From | random | utility | to binary | logit | 45 min |
2 Multiple alternatives, choice sets and normalization 45 min
|     | 3   |     | Specifying |     | systematic     | utility |           | 45 min |
| --- | --- | --- | ---------- | --- | -------------- | ------- | --------- | ------ |
|     | 4   |     | Nonlinear  |     | specifications | and     | synthesis | 45 min |
1

1 Period 1: from random utility to binary logit
Learning objectives
At the end of this period, you should be able to:
• calculate logit probabilities from systematic utilities;
• derive a binary choice probability from a utility difference;
• state the distributional assumptions of the binary logit model;
• explain the role of the scale parameter.
Activity 1.1 — An operational choice model (10 minutes)
Slides to study: PDF pages 3–5 and 9–19.
The logit model converts systematic utilities into choice probabilities:
eµnVin
P (i | C ) = .
n n (cid:80) eµnVjn
j∈Cn
The attributes describe the alternatives and the choice context. The parameters describe
how these attributes contribute to utility. The scale parameter µ controls the importance
n
of systematic utility relative to the random component.
While studying the examples, identify three distinct operations:
1. determine the individual choice set;
2. calculate one systematic utility for each available alternative;
3. transform the scaled utilities into probabilities.
Mateo has no car available. Consequently, car is absent from the denominator. An unavail-
able alternative is not simply unattractive: it cannot be chosen.
Checkpoint
Without calculating anything, answer the following questions.
1. If the same constant is added to every V , do the probabilities change?
in
2. If an alternative is unavailable, should its exponential remain in the denominator?
3. Must the alternative with the greatest V have probability one?
in
Keep your answers. You will justify the first one formally in Period 2.
2

| Activity | 1.2 — | Binary | random |     | utility | (12 | minutes) |     |     |     |
| -------- | ----- | ------ | ------ | --- | ------- | --- | -------- | --- | --- | --- |
Slides to study: PDF pages 21–24 and 32–38. Pages 25–31 provide additional details
about the extreme-value distribution; consult them when indicated below.
| Consider | two alternatives |     | i and | j:  |     |     |     |         |     |     |
| -------- | ---------------- | --- | ----- | --- | --- | --- | --- | ------- | --- | --- |
|          |                  |     | U     | = V | +ε′ | ,   | U   | = V +ε′ | .   |     |
|          |                  |     |       | in  | in  | in  | jn  | jn      | jn  |     |
Alternative i is chosen when its utility is the greatest. Rearranging the choice condition
gives
|     |     |     | P (i | | {i,j}) | =   | Pr(U | ≥ U | )        |     |     |
| --- | --- | --- | ---- | -------- | --- | ---- | --- | -------- | --- | --- |
|     |     |     | n    |          |     | in   |     | jn       |     |     |
|     |     |     |      |          | =   | Pr(V | −V  | ≥ ε′ −ε′ | ).  |     |
|     |     |     |      |          |     | in   | jn  | jn       | in  |     |
This step is fundamental: a binary choice depends on a utility difference, not on the two
| absolute | utility | levels. |     |     |     |     |     |     |     |     |
| -------- | ------- | ------- | --- | --- | --- | --- | --- | --- | --- | --- |
For logit, the alternative-specific errors are independent and identically distributed extreme-
value random variables with a common scale. Their difference follows a logistic distribution.
Therefore,
|     |     |     |             |     |                 | 1   |     | eµnVin |         |     |
| --- | --- | --- | ----------- | --- | --------------- | --- | --- | ------ | ------- | --- |
|     |     | P   | (i | {i,j}) | =   |                 |     |     | =      |         | .   |
|     |     |     | n           |     | 1+e−µn(Vin−Vjn) |     |     | eµnVin | +eµnVjn |     |
Ifyouwanttoverifythedistributionalstep, studyPDFpages26–30. Thehistoricalmaterial
and the maximum-of-random-variables motivation are useful context, but are not required
| for the remaining |     | activities. |     |     |     |     |     |     |     |     |
| ----------------- | --- | ----------- | --- | --- | --- | --- | --- | --- | --- | --- |
Activity 1.3 — Exercise 1: binary logit probabilities (15 minutes)
| Open Logit | Exercise |      | 1, Binary | logit   | probabilities. |     |     |           |     |     |
| ---------- | -------- | ---- | --------- | ------- | -------------- | --- | --- | --------- | --- | --- |
| 1. Answer  | all      | four | MCQs      | without | consulting     |     | the | solution. |     |     |
2. For Question 3, calculate at least one row yourself before comparing the proposed
tables.
| 3. Record | the | utility | difference |     | V 1n −V | 2n for | each | person. |     |     |
| --------- | --- | ------- | ---------- | --- | ------- | ------ | ---- | ------- | --- | --- |
4. Consult the solution and correct both your answer and your reasoning.
| Activity | 1.4 — | The | scale | parameter |     | (8 minutes) |     |     |     |     |
| -------- | ----- | --- | ----- | --------- | --- | ----------- | --- | --- | --- | --- |
Open Logit Exercise 2, Scale and choice probabilities. Answer only the questions concerning
logit: Questions 1, 2 and 5. The probit questions are not part of this session.
| Use the | equivalent | expression |     |     |     |     |     |     |     |     |
| ------- | ---------- | ---------- | --- | --- | --- | --- | --- | --- | --- | --- |
1
|     |     |     |     | P   | (i) = |     |     | .   |     |     |
| --- | --- | --- | --- | --- | ----- | --- | --- | --- | --- | --- |
n
1+e−µn(Vin−Vjn)
It shows that µ multiplies the systematic utility difference. A small µ produces probabili-
|     | n   |     |     |     |     |     |     |     |     | n   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
ties close to equal shares. A large µ produces probabilities concentrated on the alternative
n
| with the | largest | systematic | utility. |     |     |     |     |     |     |     |
| -------- | ------- | ---------- | -------- | --- | --- | --- | --- | --- | --- | --- |
3

Checkpoint
| Before continuing, | verify that   | you can explain       | why:                   |
| ------------------ | ------------- | --------------------- | ---------------------- |
| • choice depends   | on V          | −V ;                  |                        |
|                    | in            | jn                    |                        |
| • independent      | extreme-value | errors produce        | a logistic difference; |
| • µ → 0 leads      | to equal      | binary probabilities; |                        |
n
• µ → +∞ leads to a nearly deterministic choice when the systematic utilities differ.
n
4

2 Period 2: multiple alternatives, choice sets and normalization
| Learning |         | objectives |              |     |            |         |     |     |     |     |
| -------- | ------- | ---------- | ------------ | --- | ---------- | ------- | --- | --- | --- | --- |
| At       | the end | of         | this period, |     | you should | be able | to: |     |     |     |
•
|     | distinguish |     | the | universal | choice | set from | an  | individual | choice | set; |
| --- | ----------- | --- | --- | --------- | ------ | -------- | --- | ---------- | ------ | ---- |
•
|     | incorporate |     | availability |     | into | logit probabilities; |     |     |     |     |
| --- | ----------- | --- | ------------ | --- | ---- | -------------------- | --- | --- | --- | --- |
•
|     | extend |     | the binary | formula | to  | several | alternatives; |     |     |     |
| --- | ------ | --- | ---------- | ------- | --- | ------- | ------------- | --- | --- | --- |
•
|     | recognize |     | equivalent |     | utility specifications; |     |     |     |     |     |
| --- | --------- | --- | ---------- | --- | ----------------------- | --- | --- | --- | --- | --- |
•
|     | distinguish |     | location |        | normalization | from             | the | choice | of utility units. |     |
| --- | ----------- | --- | -------- | ------ | ------------- | ---------------- | --- | ------ | ----------------- | --- |
|     | Activity    |     | 2.1 —    | Choice | sets          | and availability |     | (12    | minutes)          |     |
|     | Slides      | to  | study:   | PDF    | pages 40–45.  |                  |     |        |                   |     |
The universal choice set C contains every alternative relevant to the population and the
analysis. The individual choice set C ⊆ C contains the alternatives feasible for individual n
n
|     | in the | relevant | choice       | situation. |           |     |     |     |     |     |
| --- | ------ | -------- | ------------ | ---------- | --------- | --- | --- | --- | --- | --- |
|     | Define | the      | availability |            | indicator |     |     |     |     |     |
(cid:40)
|     |     |     |     |     |     |     | 1,  | i ∈ C n | ,   |     |
| --- | --- | --- | --- | --- | --- | --- | --- | ------- | --- | --- |
a =
in
|     |     |     |     |     |     |     | 0,  | i ∈/ C | .   |     |
| --- | --- | --- | --- | --- | --- | --- | --- | ------ | --- | --- |
n
|     | The | probability |     | can then | be written | using | either | set: |          |     |
| --- | --- | ----------- | --- | -------- | ---------- | ----- | ------ | ---- | -------- | --- |
|     |     |             |     |          |            |       | eµnVin |      | a eµnVin |     |
in
|     |     |     |     |     | P (i | C | ) =      |        | =        |        | .   |
| --- | --- | --- | --- | --- | -------- | -------- | ------ | -------- | ------ | --- |
|     |     |     |     |     | n n      | (cid:80) | eµnVjn | (cid:80) | eµnVjn |     |
a jn
|     |     |     |     |     |     | j∈Cn |     |     | j∈C |     |
| --- | --- | --- | --- | --- | --- | ---- | --- | --- | --- | --- |
Availability concerns feasibility or awareness under the adopted choice-set rules. It is not
determined by whether an alternative has low utility. A very unattractive alternative may
|     | remain | available. |     |     |     |     |     |     |     |     |
| --- | ------ | ---------- | --- | --- | --- | --- | --- | --- | --- | --- |
Activity 2.2 — Exercise 3: choice sets and interpretation (10 minutes)
Open Logit Exercise 3, Choice sets and model interpretation. Answer all questions, then
|     | consult | the | solution. |     |     |     |     |     |     |     |
| --- | ------- | --- | --------- | --- | --- | --- | --- | --- | --- | --- |
Pay particular attention to the distinction between these two statements:
•
|     |     | the systematic |     | utility | functions | are | specified; |     |     |     |
| --- | --- | -------------- | --- | ------- | --------- | --- | ---------- | --- | --- | --- |
•
|     |     | the distribution |     | of    | the random | errors       | is  | specified.   |         |     |
| --- | --- | ---------------- | --- | ----- | ---------- | ------------ | --- | ------------ | ------- | --- |
|     | The | first statement  |     | alone | does       | not identify | the | choice-model | family. |     |
5

Activity 2.3 — From binary to several alternatives (8 minutes)
| Slides | to study: PDF | pages | 46–49. |     |     |     |     |     |
| ------ | ------------- | ----- | ------ | --- | --- | --- | --- | --- |
For alternative i to be chosen, it must dominate the best of all its competitors:
|     |     |     |     | U   | ≥ max | U . |     |     |
| --- | --- | --- | --- | --- | ----- | --- | --- | --- |
|     |     |     |     | in  |       | jn  |     |     |
j∈Cn\{i}
A useful property of independent extreme-value random variables is that their maximum is
also extreme value. The comparison with the best competitor can therefore be treated as a
| binary | comparison. This | gives |     |     |     |     |     |     |
| ------ | ---------------- | ----- | --- | --- | --- | --- | --- | --- |
eµnVin
|     |     |     | P   | (i | C | ) =        |     | .   |     |
| --- | --- | --- | --- | ------ | ---------- | --- | --- | --- |
|     |     |     |     | n      | n (cid:80) |     |     |     |
eµnVjn
j∈Cn
| Check | two basic properties | directly |     | from | the formula: |     |     |     |
| ----- | -------------------- | -------- | --- | ---- | ------------ | --- | --- | --- |
(cid:88)
|     |     | 0 ≤ | P (i | | C ) | ≤ 1, | P   | (i | C | ) = 1. |
| --- | --- | --- | ---- | ----- | ---- | --- | ------ | ------ |
|     |     |     | n    | n     |      | n   | n      |        |
i∈Cn
| Activity | 2.4 — Utility | normalization |     |     | (15 minutes) |     |     |     |
| -------- | ------------- | ------------- | --- | --- | ------------ | --- | --- | --- |
Slides to study: PDF pages 51–53, followed by PDF page 38 for the scale interpretation.
| There | are two related | but distinct |     | invariances. |     |     |     |     |
| ----- | --------------- | ------------ | --- | ------------ | --- | --- | --- | --- |
Location. For any individual-specific quantity c common to every alternative,
n
|     |     |     |          | eµn(Vin+cn) |     | eµnVin   |     |     |
| --- | --- | --- | -------- | ----------- | --- | -------- | --- | --- |
|     |     |     |          |             | =   | (cid:80) | .   |     |
|     |     |     | (cid:80) | eµn(Vjn+cn) |     | eµnVjn   |     |     |
|     |     |     |          | j           |     | j        |     |     |
Only utility differences are identified. One common location must therefore be fixed.
Scale. Probabilities depend on the product µ V . The utility unit and the random-error
n in
scale cannot be identified separately from choice data. One scale convention is required.
A moneymetric specification fixes the cost coefficient in V to −1 and expresses utility in
in
| monetary | units: |     |     |     |     |     |     |     |
| -------- | ------ | --- | --- | --- | --- | --- | --- | --- |
(cid:88)
|     |     |     | V   | = −cost | +   | β   | z . |     |
| --- | --- | --- | --- | ------- | --- | --- | --- | --- |
|     |     |     |     | in      | in  | k   | ink |     |
k
The coefficient β is then measured in monetary units per unit of z .
|     | k   |     |     |     |     |     |     | k   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
NowopenLogitExercise4,Equivalentutilityspecifications. Answerallquestionsandconsult
the solution. Focus on why multiplying only the systematic utilities is not the same as
| changing | the arbitrary | unit | of the | complete | random | utilities. |     |     |
| -------- | ------------- | ---- | ------ | -------- | ------ | ---------- | --- | --- |
Checkpoint
| Complete | the following | statements |     | in your | own words. |     |     |     |
| -------- | ------------- | ---------- | --- | ------- | ---------- | --- | --- | --- |
1. An unavailable alternative is removed from the denominator because ...
2. Adding the same quantity to all utilities changes no probability because ...
3. MultiplyingV whilekeepingtheerrordistributionfixedchangesprobabilitiesbecause
in
...
4. Fixing a cost coefficient to −1 makes utility moneymetric because ...
6

| 3        | Period  |            | 3: specifying |     | systematic |         |     | utility |     |     |     |
| -------- | ------- | ---------- | ------------- | --- | ---------- | ------- | --- | ------- | --- | --- | --- |
| Learning |         | objectives |               |     |            |         |     |         |     |     |     |
| At       | the end | of         | this period,  | you | should     | be able | to: |         |     |     |     |
•
|     | explain |     | the role of | an alternative-specific |     |     | constant; |     |     |     |     |
| --- | ------- | --- | ----------- | ----------------------- | --- | --- | --------- | --- | --- | --- | --- |
•
|     | normalize |     | a system | of constants; |     |     |     |     |     |     |     |
| --- | --------- | --- | -------- | ------------- | --- | --- | --- | --- | --- | --- | --- |
•
|     | interpret |     | quantitative | and | qualitative |     | attributes; |     |     |     |     |
| --- | --------- | --- | ------------ | --- | ----------- | --- | ----------- | --- | --- | --- | --- |
•
|     | distinguish |     | generic | from | alternative-specific |     |     | coefficients; |     |     |     |
| --- | ----------- | --- | ------- | ---- | -------------------- | --- | --- | ------------- | --- | --- | --- |
•
|     | introduce |     | individual                 | characteristics |        | through |           | identified | interactions. |     |     |
| --- | --------- | --- | -------------------------- | --------------- | ------ | ------- | --------- | ---------- | ------------- | --- | --- |
|     | Activity  |     | 3.1 — Alternative-specific |                 |        |         | constants |            | (13 minutes)  |     |     |
|     | Slides    | to  | study: PDF                 | pages           | 55–63. |         |           |            |               |     |     |
Observed attributes rarely describe every systematic difference between alternatives. An
alternative-specific constant (ASC) captures the average contribution of omitted attributes
|     | associated |     | with one | named | alternative. |     | For example, |     |     |     |     |
| --- | ---------- | --- | -------- | ----- | ------------ | --- | ------------ | --- | --- | --- | --- |
(cid:88)
|     |     |     |     |     | V   | = ASC |     | +   | β z . |     |     |
| --- | --- | --- | --- | --- | --- | ----- | --- | --- | ----- | --- | --- |
|     |     |     |     |     |     | in    | i   |     | k ink |     |     |
k
|     | The | ASCs | are relative. | Adding | a common |     | constant |     | c gives  |     |     |
| --- | --- | ---- | ------------- | ------ | -------- | --- | -------- | --- | -------- | --- | --- |
|     |     |      |               | (ASC   | +c)−(ASC |     | +c)      | =   | ASC −ASC | ,   |     |
|     |     |      |               |        | i        |     | j        |     | i j      |     |     |
so the probabilities are unchanged. One ASC must be fixed, commonly to zero. Each
estimated ASC is then interpreted relative to that reference alternative.
AnASCisnotaparameteroftheerrordistribution. Itisthecoefficientofabinaryattribute
identifying an alternative. By common shorthand, both the attribute and its coefficient are
|     | often | called | the ASC. |     |     |     |     |     |     |     |     |
| --- | ----- | ------ | -------- | --- | --- | --- | --- | --- | --- | --- | --- |
Open Logit Exercise 7, Mean of error term. Answer the three short MCQs. Use them
to verify that an alternative-specific error mean can be absorbed into the corresponding
|     | systematic |        | utility without    |       | changing   | the | random | utility. |                   |     |     |
| --- | ---------- | ------ | ------------------ | ----- | ---------- | --- | ------ | -------- | ----------------- | --- | --- |
|     | Activity   |        | 3.2 — Quantitative |       | attributes |     |        | and      | units (8 minutes) |     |     |
|     | Slides     | to     | study: PDF         | pages | 65–66.     |     |        |          |                   |     |     |
|     | In a       | linear | specification,     |       |            |     |        |          |                   |     |     |
(cid:88)
|     |     |     |     |     | V   | in = ASC | i   | +   | β k z ink , |     |     |
| --- | --- | --- | --- | --- | --- | -------- | --- | --- | ----------- | --- | --- |
k
the unit of β k is the utility unit divided by the unit of z k . Changing the measurement unit
|     | of an        | attribute | requires | a   | compensating |     | change | in  | its coefficient. |       |     |
| --- | ------------ | --------- | -------- | --- | ------------ | --- | ------ | --- | ---------------- | ----- | --- |
|     | For example, |           | if       |     |              |     |        |     |                  |       |     |
|     |              | β         | t        |     | = β          |     | t      |     | , t              | = 60t | ,   |
mathrmmin mathrmmin mathrmhour mathrmhour mathrmmin mathrmhour
then
|     |     |           |             |     | β          |             | =   | 60β       | .         |     |     |
| --- | --- | --------- | ----------- | --- | ---------- | ----------- | --- | --------- | --------- | --- | --- |
|     |     |           |             |     | mathrmhour |             |     | mathrmmin |           |     |     |
|     | The | numerical | coefficient |     | changes;   | the modeled |     | utility   | does not. |     |     |
7

Activity 3.3 — Qualitative variables and coefficients (9 minutes)
Slides to study: PDF pages 67–70.
A qualitative variable with K levels can be represented by binary indicators. If every indi-
cator is included together with an ASC, one level is redundant because the indicators sum
to one. Select one level as the reference and interpret the other coefficients relative to it.
A generic coefficient imposes the same sensitivity across alternatives:
V = ···+β t .
in t in
Alternative-specific coefficients allow different sensitivities:
V = ···+β t .
in t,i in
Anindividualcharacteristics thatenterseveryutilitywiththesamecoefficientcancelsfrom
n
all utility differences. To influence choice, it must interact with alternatives or alternative-
specific attributes. For example,
V = ASC +γ s +β t .
in i i n t in
One γ must be normalized because adding the same γs to all utilities changes no proba-
i n
bility.
Activity 3.4 — Exercise 8: systematic utility (15 minutes)
Open Logit Exercise 8, Specification of systematic utility. Answer all four questions before
consulting the solution.
For every proposed transformation, apply this diagnostic sequence:
1. Write the original utility difference.
2. Write the transformed utility difference.
3. Check whether the two expressions agree for every observation.
4. Check that each coefficient has the correct unit.
If time remains, use Logit Exercise 9, Qualitative variables, as an optional application of
changing the reference category.
Checkpoint
Can you explain each term in the specification
V = ASC +γ s +β t +β c ?
in i i n t in c,i in
Identify which parameters require a location normalization. State which coefficients are
generic and which are alternative specific.
8

4 Period 4: nonlinear specifications and synthesis
Learning objectives
At the end of this period, you should be able to:
• explain why a linear effect may be behaviorally restrictive;
• distinguish interval indicators from piecewise-linear variables;
• construct continuous piecewise-linear variables;
• interpret their coefficients as marginal utilities;
• assemble the principal components of a logit specification.
Activity 4.1 — Why transform an attribute? (8 minutes)
Slides to study: PDF pages 72–75.
The linear term βx imposes a constant marginal utility:
∂V
= β.
∂x
Consequently, an additional five minutes has the same utility effect on a short trip and on a
long trip. This may be an acceptable approximation, but it is a behavioral restriction rather
than a mathematical necessity.
Nonlinearity in an attribute does not necessarily imply nonlinearity in the parameters. If
transformed variables are created first, a specification such as
V = β h (x )+β h (x )
in 1 1 in 2 2 in
remains linear in β and β .
1 2
Activity 4.2 — Piecewise-linear variables (14 minutes)
Slides to study: PDF pages 76–84.
Suppose travel time TT ≥ 0 has breakpoints at 30 and 90 minutes. Define
x = min(TT,30),
1
(cid:0) (cid:1)
x = min max(TT −30,0),60 ,
2
x = max(TT −90,0).
3
These variables decompose total time:
x +x +x = TT.
1 2 3
The contribution
β x +β x +β x
1 1 2 2 3 3
is continuous. Its marginal utility is β below 30 minutes, β between 30 and 90 minutes,
1 2
and β above 90 minutes.
3
Verify the construction for TT = 20, TT = 60, and TT = 105. In each case, calculate
(x ,x ,x ) and check that the components sum to TT.
1 2 3
9

Activity 4.3 — Exercise 10: piecewise-linear specification (13 minutes)
OpenLogitExercise10,Piecewise-linearspecification. Answerallfivequestions,thenconsult
the solution.
The first proposal in the exercise uses interval indicators. Those indicators assign a constant
utility contribution within an interval. They do not produce a continuous piecewise-linear
relationship. Make sure that you can explain this distinction without relying only on the
formulas.
Activity 4.4 — Synthesis (10 minutes)
Consider a choice among car, public transportation and bicycle. For individual n, suppose
that:
• car may be unavailable;
• travel time is observed for every available mode;
• monetary cost is observed for car and public transportation;
• the effect of public-transportation time may differ for students;
• bicycle time should have different marginal effects below and above 30 minutes.
Without assigning numerical values, write one identified set of systematic utility functions
containing:
1. one normalized ASC;
2. a generic cost coefficient;
3. a generic travel-time coefficient for car and public transportation;
4. a student interaction affecting public transportation time;
5. a continuous two-segment specification for bicycle time.
Then write the probability of choosing car using availability indicators. There is more
than one correct specification. Check identification by asking whether any included term is
common to every alternative for every individual.
Checkpoint
You have completed the required path if you can move through the sequence
choice set −→ V −→ error assumptions −→ P (i) −→ interpretation .
in n
For each arrow, explain what information or assumption is required.
Optional extension: the Box–Cox transformation
Ifyoufinishearly,studyPDFpages85–88andcompleteLogitExercise11. Forx > 0,theBox–Cox
transformation is
 xλ−1
 , λ ̸= 0,
B(x;λ) = λ
lnx, λ = 0.
The exercise examines the linear case, the logarithmic limit, and the role of λ in determining
curvature.
10

Final self-assessment
For each statement, decide whether you can explain it without consulting the slides.
| 1. Logit         | probabilities   | depend         | on     | scaled         | utility differences. |          |
| ---------------- | --------------- | -------------- | ------ | -------------- | -------------------- | -------- |
| 2. Availability  | and             | attractiveness |        | are            | different concepts.  |          |
| 3. A common      | additive        | utility        | term   | is             | not identified.      |          |
| 4. Utility       | scale must      | be normalized. |        |                |                      |          |
| 5. ASCs          | are interpreted | relative       |        | to a reference | alternative.         |          |
| 6. An individual | characteristic  |                | common |                | to every utility     | cancels. |
7. Piecewise-linear variables allow marginal utility to vary by interval.
Return to the relevant activity for every statement that you cannot yet justify.
11