# Iron Levels and Depression Symptoms in US Women

## Overview
This repository contains the analysis code and documentation for a study examining the associations between iron deficiency, ferritin levels, and depressive symptoms in US pregnant, nonpregnant, and postpartum women using NHANES 2005-2010 & 2015-2018 data.

## Research Question
How do iron deficiency and ferritin levels relate to depressive symptoms across pregnancy stages, and how does income level affect these relationships?

## Data Source
- National Health and Nutrition Examination Survey (NHANES) cycles 2005-2010 and 2015-2018
- Study population: Women aged 20-44 years (N=6107)
- Subgroups:
  - Pregnant women (N=575)
  - Postpartum women (N=430)
  - Non-pregnant women (N=5102)

## Key Variables
- **Iron Status Measures:**
  - Iron deficiency (ferritin < 15 μg/L)
  - Ferritin levels (continuous)
- **Depression Measure:**
  - PHQ-9 (Patient Health Questionnaire-9)
- **Key Covariates:**
  - BMI
  - Race/ethnicity
  - Age
  - High-sensitivity C-reactive protein (hsCRP)
  - Income level (PIR ≤ 1.85 for low income)

## Analysis Methods
- Logistic regression for binary depression outcomes
- Negative binomial regression for depression scores
- Complex survey design accounting for NHANES sampling weights
- Stratification by pregnancy status and income level
- Adjustment for key demographic and clinical covariates

## Key Findings

### Iron Deficiency (Binary Analysis)
- Iron deficiency (ferritin < 15 μg/L) showed no significant association with depression
- This finding was consistent across all groups, regardless of pregnancy status or income level

### Ferritin Levels (Continuous Analysis)
1. Pregnant Women:
   - Low-income pregnant women showed lower depression scores with higher ferritin levels
   - Effect size: IRR = 0.996 (95% CI: 0.993-0.999)

2. Postpartum Women:
   - Low-income postpartum women showed higher depression scores with higher ferritin levels
   - Effect size: IRR = 1.004 (95% CI: 1.001-1.006)
   - Notable contrast with the pregnancy findings

3. Non-pregnant Women:
   - No significant associations between ferritin levels and depression

### Additional Findings
- BMI was consistently associated with increased depression risk, particularly in non-pregnant women
- Age effects varied by group:
  - Increased depression risk in general low-income population
  - Decreased depression risk in low-income postpartum women
- All significant effects were relatively small in magnitude

These findings suggest that the relationship between iron status and depression varies by pregnancy status and income level, though the clinical significance of these small effect sizes requires further investigation.

## Repository Structure
```
├── data/                       # Directory for NHANES datasets
├── NHANES-analyses-R.ipynb     # R statistical analyses
├── NHANES-descriptive-statistics.ipynb  # Initial data exploration
├── step1_create_csv.ipynb      # Data extraction and CSV creation
├── step2_clean_data.ipynb      # Data cleaning procedures
├── step3_impute_values.ipynb   # Missing value imputation
├── step4_construct_weights.ipynb # Survey weight calculations
├── step5_descriptive_stats.ipynb # Detailed descriptive statistics
├── step6_prevalence_stats.ipynb # Prevalence calculations - Editing notebook will upload soon
├── step7_logistic_regression.ipynb # Main regression analyses - Editing notebook will upload soon
└── survey_weights_check.ipynb  # Survey weight validation
```

## Requirements

### Software Requirements
- Jupyter Notebook/JupyterLab
- Python 3.x
- R (for R-based analyses)

## Project Dependencies

## Python Dependencies
Install Python dependencies using:
`pip install -r requirements.txt`

## R Dependencies
Install R dependencies using:
`install.packages(c("survey", "ggplot2", "dplyr", "table1", "haven"))`

## Analysis Pipeline

The analysis is conducted through a series of Jupyter notebooks that should be run in the following order:

1. `step1_create_csv.ipynb`: Creates initial CSV files from NHANES data
2. `step2_clean_data.ipynb`: Cleans and preprocesses the data
3. `step3_impute_values.ipynb`: Handles missing values through imputation
4. `step4_construct_weights.ipynb`: Calculates appropriate survey weights
5. `step5_descriptive_stats.ipynb`: Generates descriptive statistics
6. `step6_prevalence_stats.ipynb`: Calculates prevalence statistics
7. `step7_logistic_regression.ipynb`: Performs main regression analyses

Additional notebooks:
- `NHANES-descriptive-statistics.ipynb`: Initial exploratory data analysis
- `NHANES-analyses-R.ipynb`: Additional R-based statistical analyses
- `survey_weights_check.ipynb`: Validates survey weight calculations

## Contributing
Contributions are welcome! Please read the contributing guidelines before submitting pull requests.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Citation
If you use this code or findings in your research, please cite:
```bibtex
@thesis{hartnett2024iron,
  title={Iron Levels and Depression Symptoms in US Pregnant, Nonpregnant, and Postpartum Women: NHANES 2005-2010 & 2015-2018},
  author={Hartnett, Eileen and Radin, Elizabeth},
  year={2024},
  school={[Columbia University]}
}
```

## Contact
For questions or feedback, please contact eah2134@columbia.edu
