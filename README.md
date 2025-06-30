# Liberal Party Support Analysis in Canada (2019 CES)

A stratified survey analysis of Canadian provincial voting patterns using the 2019 Canadian Election Study. Employs confidence interval estimation and logistic regression to explore how province and age influence the odds of voting for the Liberal Party.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Dataset](#dataset)  
- [Research Question](#research-question)  
- [Methods](#methods)  
- [Results](#results)  
- [Visualization](#visualization)  
- [Discussion](#discussion)  
- [Reproducibility](#reproducibility)  
- [Project Structure](#project-structure)  
- [Contributors](#contributors)  
- [License](#license)  

---

## Project Overview

This project analyzes data from the 2019 Canadian Election Study (CES) Web Survey to estimate the proportion of voters supporting the Liberal Party and model the effects of provincial residence and age on voting behavior.

---

## Dataset

- **Source:** 2019 Canadian Federal Election Study (CES)  
- **Observations:** Web survey respondents across Canadian provinces  
- **Key Variables:**  
  - `is_liberal` (binary indicator of voting Liberal)  
  - `province` (categorical: 13 provinces/territories)  
  - `age` (numeric)

---

## Research Question

> How do province of residence and voter age influence the probability of voting for the Liberal Party in Canada?

---

## Methods

1. **Proportion Estimate & Confidence Interval**  
   - Calculated weighted estimate of `p̂ = 0.336` for Liberal support  
   - 95% CI = [0.330, 0.341] using stratified standard error  
2. **Logistic Regression**  
   - Modeled log-odds of voting Liberal as a function of `age` and dummy indicators for each province (reference: Alberta)  
   - Examined coefficient estimates (`β`) for age and each province  
3. **Statistical Tests**  
   - Wald tests for coefficient significance  
   - Goodness-of-fit diagnostics

---

## Results

- **Proportion Support:** 33.6% (95% CI: 33.0%–34.1%)  
- **Logistic Regression Highlights:**  
  - Positive and significant province effects for BC, MB, NB, NL, NT, NS, NU, ON, PE, QC, YT  
  - Negative coefficients for SK and age (older voters less likely to vote Liberal)

---

## Visualization

- **Age Distribution:** Histogram of respondent ages  
- **Provincial Support:** Bar plot of Liberal vote proportion by province  
- **Sample Sizes:** Bar plot of respondent counts per province

---

## Discussion

Findings indicate significant regional variation in Liberal support, with Atlantic provinces and Ontario showing highest odds. Age negatively correlates with Liberal voting probability. Limitations include web-survey selection bias and omitted demographic covariates.

---

## Reproducibility

1. **Clone repository**  
   ```bash
   git clone https://github.com/your-username/liberal-support-analysis.git
   cd liberal-support-analysis
   ```  
2. **Install R packages**  
   ```r
   install.packages(c("tidyverse", "survey", "broom"))
   ```  
3. **Run analysis**  
   - Load data processing and analysis scripts in R  
   - View final report in `STA304_GROUP120_A2-report.pdf`

---

## Project Structure

```
├── STA304_GROUP120_A2-report.pdf   # Final written report  
├── data/                           # Cleaned survey data files  
├── scripts/                        # R scripts for analysis and visualization  
├── figures/                        # Plots and charts  
└── README.md                       # Project overview
```

---

## Contributors

- **Mohammad Danish Malik**  
- **Abdul Ahad Qureshi**  
- **Syed Hasan**

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
