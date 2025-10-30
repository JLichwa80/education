# Inequality in Educational Opportunity

> Analysis of socioeconomic factors affecting college entrance exam scores in U.S. high schools (2016-2017).

---

## Project Overview

This project examines the relationship between socioeconomic factors and student performance on ACT/SAT college entrance exams.

- **Objective:** Determine if socioeconomic factors and school investment significantly influence average exam scores
- **Domain:** Education
- **Key Techniques:** Multilinear Regression (OLS), Correlation Analysis, Data Transformation (Log)

---

## Project Structure

```
├── data/
│   └── education_data_cleaned.csv          # Cleaned dataset (7,227 schools)
├── code/
│   ├── Education_DATA_Preparation.ipynb    # Data preprocessing and cleaning
│   ├── Education_DATA_Analysis_And_Modeling.ipynb  # Analysis and modeling
│   └── Inequality_in_educational_opportutnity.md   # Report in markdown
├── reports/
│   ├── Inequality_in_educational_opportutnity.pdf  # Final report
│   └── img/                                # Visualizations and figures
└── README.md                               # Project documentation
```

---

## Data

- **Source:** [EdGap.org](https://edgap.org/) and [NCES](https://nces.ed.gov/)
- **Description:** Schools data with ACT/SAT scores, socioeconomic indicators (unemployment rate, college education, free/reduced lunch eligibility), and district expenditure data
- **Geographic Coverage:** Primarily Midwest and southern U.S. states

---

## Analysis

Data preprocessing is performed in `code/Education_DATA_Preparation.ipynb` where EdGap.org, NCES school information, and district finance datasets are merged, invalid values removed, filtered to high schools, and missing values imputed. Analysis in `code/Education_DATA_Analysis_And_Modeling.ipynb` performs exploratory correlation analysis, builds multilinear OLS regression models with statistically significant predictors, and applies log transformation to expenditure data. Run notebooks sequentially to reproduce results.

---

## Results

Our analysis identifies the best set of predictors for average exam scores (R² = 0.629): unemployment rate (negative effect), percentage with college degrees, district expenditure (positive effect), percentage of students on free/reduced lunch (negative effect) with percent of students on free/reduced lunch being the strongest predictor. All predictors are statistically significant (p < 0.05), with the model explaining 62.9% of variance in exam scores and achieving a mean absolute error of 1.14 points.

---

## Authors

- [@JLichwa80](https://github.com/JLichwa80)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Python (pandas, numpy, sklearn, statsmodels, matplotlib, seaborn)
- Jupyter Notebook