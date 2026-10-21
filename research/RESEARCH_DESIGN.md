# Research Design, Data and Measures

[← Portfolio home](../README.md) · [Models and findings →](FINDINGS_AND_MODEL_EVIDENCE.md) · [Limitations →](LIMITATIONS_AND_REFLECTION.md)

## Research problem

Immigration can disrupt established social ties. Social media potentially allows migrants to maintain remote relationships, but frequent use does not necessarily mean that online interactions provide emotional support.

The dissertation therefore asked:

> **Does social media use moderate the association between friendship quality and psychological wellbeing among UK immigrants?**

The research also compared two UKHLS survey periods, Wave 11 (2019–2020) and Wave 14 (2022–2023), to test whether the *moderation association* differed across these waves. These are not a randomised pandemic exposure and control period.

### Research hypotheses

- **H1 — friendship quality:** Higher friendship quality is associated with lower GHQ-12 psychological distress.
- **H2 — social compensation:** Social media use moderates the friendship-quality/mental-health association in a direction consistent with compensation for weaker offline ties.

**The difference between the hypotheses matters:** a statistically significant friendship-quality coefficient does not establish that social media compensates for weak friendships. The compensation claim requires evidence from an **interaction**.

## Data and sample

The study used **Understanding Society / UK Household Longitudinal Study (UKHLS)**.

**Why Wave 11 and Wave 14?** The seven friendship-quality items are administered as a rotating survey module. Both waves include these measures and allow a comparison spanning the COVID-19 period.

### Participant selection reported in the dissertation

| Selection step | Reported number |
| --- | ---: |
| Non-UK-born respondents identified using Wave 1 birthplace information (`ukborn = 5`) | 9,744 |
| Matched to Wave 11 | 2,328 |
| Matched to both Wave 11 and Wave 14 | **1,592** |
| Complete-case sample for main M1/M2 models | **1,408 individuals, 2,511 person-wave observations** |

The **1,592** identifies the initial two-wave respondent panel, while the **1,408 / 2,511** describes the analysis observations used by the main reported regression models. They must not be treated as interchangeable denominators. Main regression observations vary slightly across extended model specifications.

The main model uses observations with available values for the included variables. Consequently, even within the initially matched two-wave panel, the main estimation sample is **not a balanced two-observation-per-person sample**.

## Variable operationalisation

| Construct | UKHLS variable(s) | Coding / interpretation |
| --- | --- | --- |
| **Psychological distress (outcome)** | `scghq1_dv` | GHQ-12 Likert score (0–36); higher values indicate worse psychological wellbeing |
| **Friendship quality** | `scfrely`, `scfopenup`, `scfrendany`, `scfundstnd`, `scfcritic`, `scfletdwn`, `scfannoy` | Seven-item composite, with negative dimensions recoded to align higher scores with better friendship quality |
| **Social media use (moderator)** | `smlook`, `smpost` | Frequency of looking at social media and posting; response codes 1 = every day, 6 = never |
| **Time-varying controls** | Employment status and household income | Included in the extended controlled model |
| **Survey period** | Wave 11 vs Wave 14 | Period contrast and interaction term |

**Interpretive caution:** the social-media questions measure **frequency**, not emotional intimacy, whether interactions are with friends or strangers, or whether respondents receive support. The numeric codes run **in the opposite direction to frequency**: lower numbers mean more frequent use. This matters for interpreting a negative interaction coefficient.

### Missing-data handling

The submitted methodology describes treating negative non-response and inapplicability codes as missing before analysis, followed by listwise deletion in the relevant models. Friendship-quality questions had the largest item-level missingness (approximately 15–16% in the two waves); GHQ-12 and social-media measures had lower item-level missingness.

## Analytical strategy

The dissertation used **individual fixed effects**, **wave fixed effects** and a friendship × social-media interaction to estimate within-person associations.

- Individual fixed effects absorb **time-invariant** characteristics, including stable personal background factors.
- Wave effects account for shifts **common to respondents in the same surveyed wave**.
- The interaction tests whether the friendship-quality slope differs with social-media-use frequency.
- Cluster-robust standard errors, separate viewing/posting terms, time-varying covariates, a wave interaction and quadratic terms extend the main analysis.

These modelling choices reduce some sources of confounding, but do not by themselves eliminate **time-varying confounding, reverse causation or selective missingness**.

[See the sequence of estimated models and reported results →](FINDINGS_AND_MODEL_EVIDENCE.md)

## Evidence basis

Prepared from the submitted 2026 MSc dissertation, *Online Social Connection and Immigrant Mental Health: Testing the Compensatory Role of Social Media Use Before and After COVID-19*, particularly Chapters 2–4. No new sample extraction or independent UKHLS re-analysis has been performed for this portfolio.

[← Portfolio home](../README.md)
