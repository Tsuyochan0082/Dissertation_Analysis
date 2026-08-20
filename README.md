# Dissertation Analysis

## Cumulative Low Public-Transport Accessibility and Economic Inactivity in Comparable Urban Areas in England

This repository contains the data and R code used for my MSc dissertation at University College London (UCL).

The study examines whether economic inactivity increases with cumulative low public-transport accessibility across employment, GP services, and supermarkets in comparable urban areas in England, and whether the same relationship is reproduced within County Durham.

## Analysis Files

The analysis is organised into three R Markdown files and should be run in the following order:

### `01_data_preparation_final.Rmd`
Prepares the datasets used throughout the analysis.

This script:
- loads and cleans the raw datasets;
- links 2019 IMD data to 2021 LSOA geography;
- combines economic inactivity, accessibility, deprivation, Rural-Urban Classification, and spatial boundary data;
- constructs accessibility disadvantage scores for employment, GP services, and supermarkets;
- defines the UN1 main analytical sample and the UN1 + UF1 sensitivity sample;
- identifies low-accessibility dimensions using the relevant accessibility thresholds; and
- saves the processed analytical and spatial datasets used in the subsequent scripts.

### `02_phase1_national_analysis_final.Rmd`
Conducts Phase 1 of the analysis at the England-wide level.

This script:
- describes the national distribution of cumulative low accessibility;
- estimates the relationship between the number of low-accessibility dimensions and economic inactivity;
- ranks eligible local authorities according to the concentration of multidimensional low accessibility;
- selects County Durham as the case area using the predefined selection criteria;
- produces the England-wide spatial outputs; and
- conducts the UN1 + UF1 sensitivity ranking.

### `03_phase2_county_durham_final.Rmd`
Conducts Phase 2 of the analysis within County Durham.

This script:
- extracts the County Durham analytical sample;
- examines the internal distribution of the 0–3 low-accessibility measure;
- produces the County Durham accessibility and economic inactivity maps;
- compares economic inactivity across the four low-accessibility groups;
- compares the national and County Durham patterns;
- estimates unadjusted and deprivation-adjusted models;
- conducts the UN1 + UF1 sensitivity analysis; and
- produces the supplementary student-composition analysis reported in the dissertation appendix.

## Data Structure

The repository uses the following data structure:

```text
data/
├── raw/
└── processed/
