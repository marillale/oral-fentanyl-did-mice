# Data repository

**Voluntary oral fentanyl intake produces dose- and sex-dependent physical dependence in mice without overt affective disturbances**

Allichon, M.-C.¹²³, Boehm, S.F.²³, Jordan, N.D.², Nelson, L.H.², Joffe, M.E.¹²

¹Center for Neuroscience, University of Pittsburgh · ²Translational Neuroscience Program, Department of Psychiatry, University of Pittsburgh · ³Co-first authors

This repository contains the source data underlying the figures in the manuscript.

## Contents

```
Fig_2_Oxycodone_2h_DiD.xlsx                                  Figure 2
Fig_3_Fentanyl_2h_DiD.xlsx                                   Figure 3
Fig_4_Fentanyl_4h_DiD.xlsx                                   Figure 4
Fig_5_Fentanyl_4h_High-Dose_DiD.xlsx                         Figure 5
Fig_6_Average_z-scored_withdrawal_and_affective_behavior_.xlsx   Figure 6
Figure_Supp_1_Paw_withdrawal_threshold__g_.xlsx              Supplemental Figure 1
Figure_Supp_2_radar_plots.xlsx                               Supplemental Figure 2
Figure_Supp_4_Cumulative_Fentanyl_Consumption_x_somatics_signs.xlsx   Supplemental Figure 4
```

Supplemental Figure 3 (photograph of the 2-bottle-choice sipper apparatus) has no associated data file.

## Cohorts

| File | Cohort |
|---|---|
| `Fig_2_Oxycodone_2h_DiD.xlsx` | Cohort 1 — Oxycodone, 2 h/day |
| `Fig_3_Fentanyl_2h_DiD.xlsx` | Cohort 2 — Fentanyl, 2 h/day |
| `Fig_4_Fentanyl_4h_DiD.xlsx` | Cohort 3 — Fentanyl, 4 h/day |
| `Fig_5_Fentanyl_4h_High-Dose_DiD.xlsx` | Cohort 4 — Fentanyl, 4 h/day, high-concentration escalation |
| `Fig_6_...xlsx` | All four cohorts (composite z-scores) |
| `Figure_Supp_1_...xlsx` | All four cohorts (Von Frey) |
| `Figure_Supp_2_...xlsx` | All four cohorts (radar/spider plots) |
| `Figure_Supp_4_...xlsx` | Cohorts 2–4, pooled (consumption vs. withdrawal models) |

## File structure

Most workbooks follow the same pattern:

| Sheet | Contents |
|---|---|
| `mice info` | Animal-level metadata: cage, animal ID, sex, treatment group. Excluded animals (e.g., deaths during the procedure) are noted here where applicable. |
| `raw data DiD` | Session-by-session drinking data (date, animal, bottle weights, volumes, drug concentration, intake) |
| `summary` *(or `summary behavior` / `summary DiD-behaviors`)* | One row per animal — total intake, withdrawal signs, affective assay outputs |
| Panel sheets, e.g. `B-total fluid intake`, `E-F-G somatic signs`, `H-I-J affective behaviors` | Data reshaped into plotting-ready format, grouped by sex/treatment, matching the panel letters in the published figure |

Two files are structured differently:

- **`Fig_6_...xlsx`** — per cohort: a `raw data` sheet with the three affective z-scores per animal (EZM, FST, SI), and a summary sheet with the composite withdrawal z-score by sex.
- **`Figure_Supp_4_...xlsx`** — one sheet per somatic measure (escape jumps, wet-dog shakes, paw tremors), each with individual log-transformed consumption values and the corresponding behavioral count, by sex.

> Panel sheets (`B`–`J`, across all figures) group replicate values by sex/treatment without an animal ID per column. Individual animals can be traced back via the `summary`/`raw data` sheet in the same workbook.

## Software used

Figures were generated in GraphPad Prism [**version 11**]. The radar plots (Supplemental Figure 2) were built using a Python pipeline.

Statistics (two-way ANOVA, mixed-effects models, effect sizes) were computed in GraphPad Prism. The two-part (logistic + linear regression) model relating cumulative fentanyl consumption to withdrawal signs (Supplemental Figure 4) was implemented in Python using `statsmodels` and `marginaleffects`; code available upon request.

## Citation

Allichon, M.-C., Boehm, S.F., Jordan, N.D., Nelson, L.H., Joffe, M.E. *Voluntary oral fentanyl intake produces dose- and sex-dependent physical dependence in mice without overt affective disturbances.* 

## Contact

Max E. Joffe, Ph.D. — joffeme@upmc.edu
