# Intermediate presentation: key content (Models 0–2)

Just some notes of interesting findings and stuff that we might say during the presentation next Tuesday.

**What the course asks for:** the main difficulties met in the dataset and in the modelling process up to Model 2:
- first tested specifications,
- data limitations,
- unexpected estimation results,
- possible identification issues,
- tests used to compare the models.

All numbers below come from `src/assignment.ipynb`.

---

## 1. Dataset: main characteristics

- **Size:** 5,000 trips, 4 alternatives (1 walk, 2 cycle, 3 PT, 4 car). All alternatives are available to everyone.
- **Observed shares:**

  | Mode | Trips | Share |
  |---|---|---|
  | Walk | 815 | 16.3% |
  | Cycle | 230 | 4.6% |
  | PT | 1,773 | 35.5% |
  | Car | 2,182 | 43.6% |

- **Units:** times are in hours and costs in GBP.
- **Constructed attributes (as required):**
  - `total_pt_duration` = access + rail + bus + interchange time.
  - `total_driving_cost` = fuel + congestion charge.
- **Mean distance by chosen mode:** walk 1.1 km, cycle 4.2 km, car 5.2 km, PT 7.8 km. Walking is a short-trip mode.

## 2. Data limitations and difficulties

- **Very few women:** only 5% of trips (250 of 5,000). In the market-share strata:

  | Stratum | Trips |
  |---|---|
  | Women < 43 | 117 |
  | Women ≥ 43 | 133 |
  | Men < 43 | 2,350 |
  | Men ≥ 43 | 2,400 |

  - Gender cannot reliably support an interaction, so age was used instead.
  - Preview of a later problem: the stratum weights will be extremely unbalanced (≈ 14.0 and 6.6 for women vs ≈ 0.72 and 0.33 for men). The predicted market shares will therefore depend heavily on about 250 observations.
- **Cycling is rare:** 4.6% of trips (230). Cycle-specific parameters have large standard errors, e.g. the age × cycle constant is not significant.
- **Repeated observations:** 5,000 trips come from 4,283 persons in 4,095 households. Trips are not fully independent (panel / household effect), which the logit model ignores.
- **Zero PT fares:** 22% of trips have `cost_transit = 0`, all of them with `faretype = 5` (free travel).
  - 90% of travellers aged 60+ travel for free (Freedom Pass), against 5% of younger ones.
  - So age and PT cost are strongly confounded.
- **Congestion charge:** a flat £10.50 that applies to 13% of trips. Among those trips only 10.7% choose car. Car cost is very skewed (mean £2.34, median £0.71, max £16.60).
- **Cost only varies for 2 modes:** walk and cycle have no monetary cost, so $\beta_{cost}$ is identified only from PT and car.
- **The car alternative mixes drivers and passengers:**
  - 21.8% of trips are made by people without a driving licence, and 153 of them still chose car (likely as passengers).
  - 103 car trips come from households with no car.
- **Long walking times:** 22.5% of trips have a walking time over 2 h (max 9.3 h), but the longest chosen walk is 2.6 h. Walking alternatives for long trips are dominated in practice.

## 3. Modelling process: specifications tested

- **Model 0:** constants plus generic time and cost.

  - $V_{walk} = \beta_{time} T_{walk}$
  - $V_{cycle} = ASC_{cycle} + \beta_{time} T_{cycle}$
  - $V_{pt} = ASC_{pt} + \beta_{time} T_{pt} + \beta_{cost} C_{pt}$
  - $V_{car} = ASC_{car} + \beta_{time} T_{car} + \beta_{cost} C_{car}$

  - Walk is the reference alternative ($ASC_{walk} = 0$).
- **Model 1:** separate time coefficients per mode ($\beta_{time,walk}$, $\beta_{time,cycle}$, $\beta_{time,pt}$, $\beta_{time,car}$). Cost stays generic: £1 is worth the same on every mode.
- **Model 2:** socio-economic variable = age, centred at 45 and in decades, $a_n = (\text{age}_n - 45)/10$. Centring keeps the base parameters interpretable for a 45-year-old.
  - **2a (age × constants):** $\beta_{age,i}\, a_n$ added to cycle, PT and car. Walk stays the reference.
  - **2b (age × time):** $\beta_{time,i}(a_n) = \beta_{time,i} + \beta_{time,age}\, a_n$, the same shift for all modes.
- **Specifications tried but not retained:**
  - Age × cost was not significant (t ≈ 0.97), probably because zero fares absorb the age effect on PT cost.
  - Licence × car constant improved the fit enormously (LL −4123.6 vs −4416.8). It is a strong candidate for later models.

## 4. Estimation results

| | Model 0 | Model 1 | Model 2a | **Model 2b** |
|---|---|---|---|---|
| Parameters (K) | 5 | 8 | 11 | 9 |
| Final LL | −4710.1 | −4416.8 | −4370.1 | **−4363.7** |
| ρ² (null LL = −6931.5) | 0.320 | 0.363 | 0.370 | 0.370 |
| ρ̄² | 0.320 | 0.362 | 0.368 | **0.369** |
| AIC | 9430 | 8850 | 8762 | **8745** |
| BIC | 9463 | 8902 | 8834 | **8804** |

- **Model 0:**
  - $\beta_{time} = -4.97$ (t = −26.7) and $\beta_{cost} = -0.149$ (t = −13.2). Both are negative as expected.
  - The constants relative to walk are $ASC_{cycle} = -3.27$, $ASC_{pt} = -0.52$, $ASC_{car} = -1.18$, all significant.
  - Implied value of time ≈ 33 £/h.
- **Model 1:**
  - Time sensitivity, from most to least sensitive:

    | Mode | Coefficient | t |
    |---|---|---|
    | Walk | −7.43 | −18.6 |
    | Car | −5.68 | −16.5 |
    | Cycle | −5.03 | −14.5 |
    | PT | −3.10 | −13.4 |

  - Cost stays stable at −0.137.
  - Values of time: PT ≈ 22.5 £/h, car ≈ 41 £/h.
- **Model 2a:**
  - Age × car = +0.254 (t = 8.6) and age × PT = +0.131 (t = 4.0): older travellers prefer car and PT over walking.
  - Age × cycle = +0.026 (t = 0.5) is not significant.
- **Model 2b:**
  - Age × time = −0.756 (t = −9.5): older travellers are more sensitive to time. The walking time coefficient goes from −7.7 at age 45 to −9.2 at age 65.
  - All other parameters are stable in sign, size and significance.

## 5. Unexpected results and points to discuss

- **Negative car constant despite the largest share:** the observed car share (43.6%) is already explained by time and cost. The constant then captures unobserved barriers relative to walking (no licence, no car, parking).
- **Big jump in the PT constant:** $ASC_{pt}$ goes from −0.52 to −2.25 when time becomes mode-specific. PT time is now valued less, so a larger negative constant is needed to reproduce the PT share. Constants and time coefficients are strongly linked.
- **Values of time look high:** 33 £/h generic, 41 £/h for car. Possible reasons:
  - self-selection of high-income drivers,
  - the flat £10.50 congestion charge dominating the cost variation,
  - no income variable in the model.
- **Age effect is not linear:**

  | Age group | Car share | PT share |
  |---|---|---|
  | ≤ 30 | 29% | 46% |
  | 31–45 | 44% | 36% |
  | 46–60 | 53% | 26% |
  | 60+ | 47% | 35% |

  - PT use rises again after 60, probably because of the free pass.
  - A linear age term cannot capture this; a piecewise or categorical age would.
- **Age × cost not significant:** this is explained by the confounding between age and zero fares (ref. Section 2).

## 6. Identification and normalisation issues

- **Constants:** only J−1 = 3 can be estimated. Walk is fixed to 0, and all constants are read relative to walking.
- **Age × constants:** age can interact with at most 3 constants. Only differences in utility are identified, so a term for walk would be redundant.
- **Centring age** only changes how the parameters are read, not the fit. Without it, the constants would refer to a newborn.
- **Generic cost with zero-cost alternatives:** this is fine for identification, since cost varies for PT and car.
- **Thin data for cycling:** parameters are technically identified but poorly estimated (large standard errors). This weak empirical identification is worth flagging as a risk for more complex models (nesting, mixtures).

## 7. Tests used to compare models

- **t-tests:** significance of each parameter (robust standard errors).
- **Likelihood ratio test** (nested models), $-2(\mathcal{L}_R - \mathcal{L}_U) \sim \chi^2_{K_U - K_R}$:

  | Comparison | H₀ | LR | df | Critical value (5%) | Decision |
  |---|---|---|---|---|---|
  | M0 vs M1 | all four time coefficients equal | 586.5 | 3 | 7.81 | Reject → **M1** |
  | M1 vs M2a | all age × constant terms = 0 | 93.5 | 3 | 7.81 | Reject |
  | M1 vs M2b | $\beta_{time,age}$ = 0 | 106.2 | 1 | 3.84 | Reject |

- **Non-nested comparison of 2a vs 2b:**
  - The LR test is not valid here, since neither model is a restriction of the other.
  - Adjusted ρ̄²: 2b = 0.3691 > 2a = 0.3679.
  - Horowitz test: P(2a is the true model) ≤ 0.0001.
  - AIC and BIC agree.
- **Current preferred model: Model 2b** (mode-specific time coefficients plus the age × time interaction).

## 8. Conclusions and next steps

- Mode-specific time sensitivity is the largest single improvement in fit.
- Age matters both as a taste shift and as a change in time sensitivity.
- Thin subgroups (women, cyclists) limit what can be estimated.

---

## Suggested slide plan (5 min ≈ 5–6 slides)

1. **Data:** shares, sample size, constructed attributes (Section 1).
2. **Data difficulties:** gender imbalance, rare cycling, free fares, congestion charge, drivers and passengers mixed in car (Section 2).
3. **Specifications M0 → M1 → M2a / M2b:** utility functions and modelling choices (Section 3).
4. **Results table and key coefficients:** values of time, age effects (Sections 4 and 5).
5. **Tests and identification:** LR tests, Horowitz test, normalisation (Sections 6 and 7).
6. **Conclusions and next steps** (Section 8).

## Questions to prepare for

- Why age and not gender? → only 5% of trips are by women.
- Why are the time coefficients mode-specific but cost is generic? → the disutility of time depends on the travel experience; money is fungible.
- Why is $ASC_{car}$ negative? → it is relative to walking, all else equal, and captures access barriers.
- Why can't 2a and 2b be compared with an LR test? → they are not nested; use ρ̄² and Horowitz.
- Are the values of time plausible? → high, but they have candidate explanations (Section 5). Income is not available.
- How will the unbalanced stratum weights affect the market shares later? → about 250 women carry about half of the population weight.
