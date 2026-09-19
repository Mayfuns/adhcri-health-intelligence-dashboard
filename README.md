# ADHCRI Health Intelligence Dashboard — Team HealthSync

A Power BI public-health analytics project developed by **Team HealthSync** for the **10Alytics Global Hackathon 2026**.

[View the full portfolio case study](https://mayfuns.github.io/mariam-analytics-portfolio/adhcri.html)

## Project overview

The ADHCRI Health Intelligence Dashboard brings fragmented ASEAN public-health indicators into one structured analytical model so differences in health outcomes, disease burden, nutrition, prevention, investment and workforce capacity can be explored together.

The project was developed under the **ASEAN Digital Health and Climate Resilience Initiative** theme.

## Project scope

| Item | Detail |
| --- | --- |
| Countries | **10 ASEAN countries** |
| Valid records | **1,691** |
| Health indicators | **16+** |
| Historical coverage | **1990–2016**, depending on indicator |
| Dashboard pages | **3** |
| SDG alignment | **SDG 3, SDG 10, SDG 17** |

## Main analytical question

**Which ASEAN countries face the greatest public-health risks, and where should policymakers investigate intervention and investment priorities?**

### 1. ASEAN Public Health Overview

High-level comparison of health outcomes and mortality patterns using measures such as:

- Life expectancy
- Maternal mortality
- Under-5 mortality
- Infant mortality
- Crude death rate

### 2. Disease, Nutrition & Child Health Risk

Analysis of overlapping public-health vulnerability using:

- Undernourished population
- Underweight children
- Malaria prevalence
- TB prevalence
- HIV prevalence
- Under-5 mortality

### 3. Healthcare Capacity & Investment

Comparison of health-system strength, prevention capacity and investment using:

- Government health expenditure
- Physician density
- Nurses/midwives density
- Pharmaceutical worker density
- DPT immunisation
- Measles immunisation

## My contribution

As part of Team HealthSync, my contribution focused on the analytics workflow:

- Understanding and checking the source datasets
- Standardising inconsistent country names
- Removing unnecessary fields
- Correcting data types and text inconsistencies
- Reshaping year columns into a long format
- Adding indicator labels
- Appending multiple health datasets into a unified fact table
- Supporting the Power BI model and DAX logic
- Helping design and interpret the dashboard
- Contributing to the final report and presentation

## Power Query workflow

The raw files did not share one consistent structure. Power Query was used to:

1. Load the datasets.
2. Standardise country fields.
3. Remove unnecessary columns.
4. Clean text values.
5. Unpivot year columns.
6. Rename the resulting fields to `Year` and `Value`.
7. Add an `Indicator` field.
8. Correct inconsistent numeric values.
9. Keep missing values as blanks rather than forcing zeros.
10. Append the cleaned datasets into one analytical fact table.

## Data model

The project used a star-schema approach:

```text
Dim_Country
Dim_Year
Dim_Indicator
      ↓
Fact_Health_Indicators
```

The central fact table contains:

- Country
- Year
- Indicator
- Value

Indicator-specific measures were used because the source measures have different units and should not be averaged together indiscriminately.

## Selected findings

- Average life expectancy varied substantially across the ASEAN countries represented.
- Lao PDR, Cambodia and Myanmar showed higher historical under-5 and maternal mortality indicators than many of the other countries in the dataset.
- Disease and nutrition risks were not distributed evenly across the region.
- Healthcare expenditure and workforce capacity varied substantially between countries.
- The hackathon priority model placed Lao PDR, Cambodia and Myanmar in the high-priority group for further investigation.

## SDG alignment

- **SDG 3 — Good Health & Well-being:** mortality, disease, immunisation, nutrition and workforce indicators.
- **SDG 10 — Reduced Inequalities:** cross-country comparisons make regional disparities more visible.
- **SDG 17 — Partnerships for the Goals:** shared data and reporting can support regional evidence-based planning.

