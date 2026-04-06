# cifs-head-start-sem-reproducibility
Reproducible analytic materials for a published study: matched observational data, SEM, and measurement invariance testing to examine preschool academic and social outcomes; data auditing and cleaning in R, latent-variable model specification in Mplus, and supplemental robustness work (propensity score matching, clustered models, and Bayesian SEM).

**Huang, R., Rosca, O., Liu, Q., Battista, C., & Baker, E. R. (2025). _Associations between father incarceration and Head Start children's academic and social competence: A case–control matching analysis_. Early Child Development and Care.**  
DOI: https://doi.org/10.1080/03004430.2025.2587743

## Overview

This repository documents the analytic workflow used to examine whether **father incarceration (FI)** was independently associated with **Head Start preschoolers' literacy, mathematics, and social competence**, above and beyond poverty-related risk factors.

The study used an urban Head Start dataset collected across multiple cohorts and applied a **case–control matching design** to compare children with incarcerated fathers to matched controls on:
- child age
- gender
- race/ethnicity
- year in program
- parental education
- income-to-needs ratio

After matching, the main analysis used **structural equation modeling (SEM)** to evaluate three latent outcomes:
- **Literacy**
- **Mathematics**
- **Social Competence**

The final reported findings indicated that, after matching and covariate adjustment, father incarceration did **not** show a detectable independent association with these latent outcomes in this sample. The paper also reports later robustness checks using clustered methods and Bayesian SEM on an alternative propensity-score-matched sample.

## What is included in this repository

### 1. Data cleaning and preprocessing (`data_cleaning/`)
This folder contains the R-based data-preparation workflow used to:
- inspect missing data patterns
- evaluate and resolve duplicate child IDs
- remove ineligible cases
- rename and standardize variables
- prepare the cleaned dataset and analytic sample for matching and modeling

The workflow documents major preprocessing decisions, including handling duplicated records, excluding cases with incarcerated mothers when isolating paternal incarceration, and constructing the final analytic sample.

### 2. Final Mplus model specifications (`mplus_inputs/`)
This folder contains the **final public Mplus input files** for the main SEM workflow:
- initial measurement model
- hypothesized structural model
- saturated/null comparison model
- measurement invariance models 1–3

These files document the latent-variable structure used in the study and show how the reported SEM analyses were specified in Mplus.

### 3. Robustness and supplemental materials (`supplement/`)
This folder contains materials related to the later robustness analyses conducted after peer review. These include:
- an alternative **1:1 propensity score matching (PSM)** approach
- **clustered GEE / mixed-model re-estimation** of observed outcomes
- a **Bayesian SEM** with matched-set random intercepts and model-based handling of missing outcomes

These supplemental analyses converged on the same substantive conclusion as the main case–control matching + SEM analysis.

## Analyses represented in this repository

This repository covers the following stages of the study:

### A. Data audit and cleaning
- duplicate-ID review and one-record-per-child decisions
- missing-data diagnostics
- variable harmonization
- preparation of analytic datasets

### B. Main latent-variable analysis
- initial measurement model
- revised measurement model
- multi-group measurement invariance testing
- hypothesized structural equation model

### C. Supplemental robustness analyses
- alternative 1:1 propensity score matching
- clustered outcome re-estimation
- Bayesian latent-variable sensitivity analysis

## Why output files are not included

This repository does **not** include Mplus output files or diagram files. The original output files used during manuscript development were not retained in a complete recoverable form, and the final numerical results are already fully presented in the published paper and supplementary materials.

For this reason, the repository is organized around the most useful reproducible artifacts that remain:
- preprocessing code
- final Mplus input specifications
- supplemental methods materials

## Data availability

The raw study data are **not included** in this repository.

The article states that the study data are available on OSF. Please refer to the published paper for the data-availability statement and access details.

## Software

The materials in this repository were produced using:
- **R**
- **Mplus 8.7**
- **Python / Google Colab** for later robustness analyses

## Skills demonstrated by this repository

This repository showcases work in:
- psychometric data cleaning and audit trails
- latent-variable modeling
- measurement invariance testing
- structural equation modeling
- matched-design analysis
- robustness/sensitivity analysis
- reproducible research organization across R, Mplus, and Python

## Citation

If you reference these materials, please cite the published article:

Huang, R., Rosca, O., Liu, Q., Battista, C., & Baker, E. R. (2025). _Associations between father incarceration and Head Start children's academic and social competence: A case–control matching analysis_. Early Child Development and Care. https://doi.org/10.1080/03004430.2025.2587743
