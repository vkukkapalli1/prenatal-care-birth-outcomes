# Prenatal Care Timing and Maternal Sociodemographic Factors Associated with U.S. Birth Outcomes

## Overview

This project examines how prenatal care timing and maternal sociodemographic factors are associated with birth outcomes in the United States. Using U.S. natality data from 2017–2023, the analysis evaluates relationships between maternal characteristics, prenatal care initiation, and infant outcomes such as birthweight and gestational age.

The project focuses on whether earlier prenatal care initiation is associated with more favorable birth outcomes after accounting for factors such as maternal age, education level, marital status, BMI category, delivery method, plurality, and gestational age.

## Research Question

How does the timing of prenatal care initiation relate to birth outcomes, specifically birthweight and gestational age, in the United States after accounting for maternal sociodemographic and clinical factors?

## Data Source

The project uses U.S. natality data from the National Center for Health Statistics (NCHS), managed by the Centers for Disease Control and Prevention (CDC). The original dataset included more than 25 million observations across 2017–2023. For this project, a sample of 70,000 observations was used, with 10,000 observations sampled from each year.

Raw data files are not included in this repository due to file size and data management considerations.

## Variables

### Outcomes

* Birthweight, measured in grams
* Gestational age, measured in completed weeks

### Predictors

* Prenatal care start timing
* Maternal education level
* Marital status
* Plurality
* Delivery method
* Maternal age
* Maternal BMI category
* APGAR score
* Year of birth

## Methods

The analysis was conducted in R and includes:

* Data cleaning and recoding
* Descriptive statistics for continuous and categorical variables
* One-way ANOVA to compare mean birthweight across prenatal care start groups
* Tukey post-hoc comparisons
* Chi-square test to evaluate the association between plurality and delivery method
* Multivariable linear regression to evaluate predictors of infant birthweight
* Regression diagnostic checks using residual plots and Q-Q plots

## Key Findings

The descriptive analysis showed that the mean birthweight in the study sample was approximately 3252 grams and the mean gestational age was approximately 38.5 weeks.

The ANOVA results suggested that birthweight differed by timing of prenatal care initiation. Births with no prenatal care had substantially lower average birthweight compared with births where prenatal care began in the first trimester.

The chi-square analysis showed a statistically significant association between plurality and delivery method, with cesarean delivery more common among multiple births.

The multivariable regression model indicated that gestational age, maternal BMI category, plurality, prenatal care timing, marital status, and maternal education were associated with infant birthweight. Multiple births, especially twins and triplets, were associated with substantially lower birthweight, while longer gestational age was strongly associated with higher birthweight.

## Repository Structure

```text
prenatal-care-birth-outcomes/
├── README.md
├── analysis/
│   └── prenatal_care_birth_outcomes_analysis.Rmd
├── reports/
│   ├── prenatal_care_birth_outcomes_report.docx
│   └── prenatal_care_birth_outcomes_rendered.html
├── presentations/
│   └── prenatal_care_birth_outcomes_presentation.pptx
├── data/
│   └── README.md
└── prenatal-care-birth-outcomes.Rproj
```

## Files in This Repository

| File                                                           | Description                                                 |
| -------------------------------------------------------------- | ----------------------------------------------------------- |
| `analysis/prenatal_care_birth_outcomes_analysis.Rmd`           | Main R Markdown analysis file containing code and narrative |
| `reports/prenatal_care_birth_outcomes_rendered.html`           | Rendered HTML output from the R Markdown analysis           |
| `reports/prenatal_care_birth_outcomes_report.docx`             | Final written project report                                |
| `presentations/prenatal_care_birth_outcomes_presentation.pptx` | Final project presentation slides                           |
| `data/README.md`                                               | Data access and usage notes                                 |
| `prenatal-care-birth-outcomes.Rproj`                           | RStudio project file                                        |

## Tools and Packages

This project was completed using R and RStudio. Main analysis tasks included data cleaning, descriptive statistics, statistical testing, visualization, and regression modeling.

Common R packages used in this workflow include:

* `tidyverse`
* `dplyr`
* `ggplot2`
* `car`
* `broom`
* `knitr`
* `kableExtra`

## Responsible Data Use

This repository does not include full raw natality CSV files. The data are documented in the project report, but raw files are excluded to keep the repository lightweight and focused on reproducible analysis code and final outputs.

## Author

Venkata Sai Krishna Kukkapalli
MS Health Data Science
Saint Louis University
