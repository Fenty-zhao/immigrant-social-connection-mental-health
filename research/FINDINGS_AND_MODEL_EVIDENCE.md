# Model Specification → Results → Interpretation

[← Portfolio home](../README.md) · [Research design](RESEARCH_DESIGN.md) · [Limitations](LIMITATIONS_AND_REFLECTION.md)

This page presents **model specifications and numerical results reported in the submitted dissertation**. It is an evidence map to the original study, not a claim that the regressions have been rerun in this repository.

## Model specification

The primary empirical design was an individual fixed-effects model with wave effects and an interaction between friendship quality and social-media use.

```text
GHQ_it = α_i + γ_t
       + β1 × Friendship_it
       + β2 × SocialMedia_it
       + β3 × (Friendship_it × SocialMedia_it)
       + δ × X_it + ε_it
```

Where:

- `GHQ_it` is the GHQ-12 distress score for person `i` at survey wave `t` (higher = worse).
- `α_i` is a person fixed effect, controlling for stable respondent-specific differences.
- `γ_t` is a wave fixed effect, capturing a shared difference between observed survey periods.
- `X_it` represents time-varying controls where included.
- **`β3` is the central moderation coefficient.** Without evidence on this coefficient, a positive or negative main friendship association does not establish social-media compensation.

Importantly, coefficients involving a non-centred interaction should be read **conditional on the other interacting variable**; the standalone friendship and social-media coefficients from interaction models are not unconditional average effects.

## Model sequence and results

### Baseline association (M1)

The baseline fixed-effects model examined friendship quality and social media use without their interaction.

| Variable | Submitted coefficient | Reported p-value |
| --- | ---: | --- |
| Friendship quality | **−1.225** | **<0.001** |
| Social media use | +0.090 | 0.407 |

**Interpretation:** Greater friendship quality was associated with a lower (better) GHQ-12 distress score in the reported baseline model. The model did not report a statistically significant main association for social-media frequency.

### Core moderation model (M2) and robust inference (M2r)

| Parameter | M2 | M2r (cluster-robust SE) |
| --- | ---: | ---: |
| Friendship × social media | **−0.131** | **−0.131** |
| Standard error | 0.188 | 0.221 |
| Reported p-value | **0.487** | **0.555** |
| Person-wave observations | 2,511 | 2,511 |
| Individuals | 1,408 | 1,408 |

**Interpretation:** The interaction did not reach conventional statistical significance, including with person-clustered standard errors. The data therefore did **not** provide convincing statistical support for H2 in these specifications.

**Reading the coding:** The social-media frequency scale is reversed (lower numeric values mean more frequent use). Coefficient direction needs to be interpreted alongside this coding; the **uncertainty** is more decisive here than the negative point estimate.

### Alternative social-media measures (M2a and M2b)

| Model | Interaction | Coefficient | Reported p-value |
| --- | --- | ---: | ---: |
| M2a | Friendship × viewing frequency | −0.249 | 0.155 |
| M2b | Friendship × posting frequency | +0.018 | 0.906 |

Separating viewing and posting frequencies did not produce a statistically significant interaction. These measures are not direct assessments of supportive versus non-supportive online relationships.

### Time-varying controls (M3)

With employment and income included, the friendship × social-media interaction remained non-significant (**β = −0.156, p = 0.409**). The submitted table reports **2,501 observations from 1,406 individuals** for this model.

### Survey-wave moderation contrast (M4)

The model added **Friendship × SocialMedia × Wave**, comparing Wave 11 with Wave 14.

- **Three-way interaction: β = −0.170, p = 0.560.**
- No statistically significant evidence that the moderation association differed between these two observation periods.
- This design does **not** isolate COVID-19 as a causal treatment.

**Specification note:** The original submitted Table 4 explicitly labels **M4 as including individual fixed effects only**, whereas M5/M6 include both individual and wave fixed effects. The specification comparison should therefore follow the table note rather than assume identical fixed-effects structures throughout.

### Nonlinear specifications (M5 and M6)

| Model | Quadratic term | Submitted coefficient | Reported p-value |
| --- | --- | ---: | ---: |
| M5 | Friendship quality squared | +0.816 | 0.145 |
| M6 | Social media use squared | −0.073 | 0.198 |

Neither quadratic term reached conventional significance. That **does not prove** the true underlying relationships are linear; it means these tests did not find clear evidence for the particular quadratic departures assessed.

## What the findings do—and do not—show

**Supported by the submitted models:** friendship quality showed a statistically significant negative association with GHQ-12 in the baseline within-person model.

**Not supported by the submitted models:** a statistically significant social-media compensation interaction, whether using the composite measure, viewing, posting, the controlled specification or the cross-wave three-way interaction.

**Not established:** a causal improvement in mental health from increasing friendship quality; a causal benefit or harm from social media use; or a causal effect of COVID-19 on moderation.

## Evidence trace

All numbers above refer to the final submitted 2026 dissertation:

- **Chapter 3 / Table 1:** model specifications and variable definitions
- **Chapter 4 / Table 2:** two-wave descriptive statistics and missingness
- **Chapter 4 / Table 3:** M1, M2, M2r, M2a, M2b and M3 regression results
- **Chapter 4 / Table 4:** M4, M5 and M6 extended models
- **Chapter 5:** interpretation and limitations

The original analysis is not independently reproduced in this repository, and access-controlled UKHLS person-level data are excluded.

[← Research design](RESEARCH_DESIGN.md) · [Limitations and reflection →](LIMITATIONS_AND_REFLECTION.md)
