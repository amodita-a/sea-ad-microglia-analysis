# Analysis Plan

## Project

**Microglial Immune Activation Across Alzheimer's Disease Pathology**

This document records the implemented educational analysis plan. It is not a preregistration.

## Research question

Do donor-level microglial interferon-response and antigen-presentation program scores differ between donors with lower versus higher Alzheimer's disease neuropathology?

## Data and analytic sample

- Public Seattle Alzheimer's Disease Brain Cell Atlas data accessed through CELLxGENE Census LTS release `2025-11-08`
- CELLxGENE dataset ID `c76098ba-eed3-45b1-98f2-96fcac55ed18`
- Middle temporal gyrus
- Microglial nuclei
- 38,905 nuclei from 84 donors with complete neuropathology metadata
- Five CELLxGENE donors without matching pathology metadata excluded
- Donor, rather than nucleus, used as the unit of statistical analysis

## Pathology groups

- Lower pathology: Not AD (9 donors) and Low (12 donors)
- Higher pathology: Intermediate (21 donors) and High (42 donors)
- Ordinal coding: Not AD = 0, Low = 1, Intermediate = 2, High = 3

## Prespecified gene programs

### Interferon response

`IFI6`, `IFI27`, `IFI44`, `IFI44L`, `IFIT1`, `IFIT2`, `IFIT3`, `ISG15`, `MX1`, `OAS1`, `OAS2`, `STAT1`

### Antigen presentation

`HLA-DRA`, `HLA-DRB1`, `HLA-DPA1`, `HLA-DPB1`, `HLA-DQA1`, `HLA-DQB1`, `CD74`, `CIITA`

## Score construction

For each nucleus, each program score was calculated as the mean CELLxGENE normalized expression across the program's available genes. All 20 prespecified genes were available. Nucleus-level scores were then averaged within donor.

## Statistical analyses

1. **Primary analysis:** two-sided Mann-Whitney U comparison of lower- versus higher-pathology donor scores, accompanied by Cliff's delta.
2. **Ordinal analysis:** Spearman correlation between donor-level score and four-level neuropathology coding.
3. **Adjusted sensitivity analysis:** donor-level ordinary least squares model including higher-pathology group, age at death, and sex, with HC3 robust standard errors.
4. **Assay-composition sensitivity:** repeat the adjusted model with the donor-level fraction of multiome nuclei. Assay is represented as a within-donor fraction because 27 donors contain nuclei from both assays, rather than assigning a potentially misleading single assay label to each donor.
5. **Minimum-nuclei sensitivity:** repeat the donor-level analyses among donors with at least 200 nuclei. This pragmatic threshold retains 77 of 84 donors and is used only as a stability check, not as a validated biological or quality-control cutoff.

## Interpretation rules

- Primary emphasis is placed on the nonparametric binary and ordinal analyses.
- Adjusted-model findings are treated as sensitivity analyses rather than replacements for the primary results.
- Effect direction, uncertainty, model assumptions, and agreement across analyses are considered alongside p-values.
- No causal or mechanistic conclusions are drawn from this observational cross-sectional analysis.

## Outputs

- Donor-level analysis table in `results/`
- Immune-program figures in `figures/`
- Reproducible analysis notebook in `notebooks/`
- Cautious written interpretation and limitations in the root `README.md`

## Status

The educational analysis MVP has been completed. The results are exploratory and have not undergone peer review.
