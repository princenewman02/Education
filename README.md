# Predicting High School ACT Performance from Socioeconomic Factors

> An analysis examining whether socioeconomic factors predict U.S. high school ACT scores, revealing poverty as the dominant predictor.

---

## Project Overview

This project investigates educational inequality by analyzing the relationship between socioeconomic variables and high school ACT performance across the United States.

**Key Finding:** Socioeconomic factors explain 62.8% of variance in ACT scores, with poverty (free/reduced lunch eligibility) having six times greater impact than any other factor. School spending shows no significant effect when controlling for socioeconomic status.

- **Objective:** Determine which factors most strongly predict ACT scores and quantify their relative importance
- **Domain:** Educational Data Science / Social Inequality Analysis
- **Key Techniques:** Data integration, cleaning, exploratory analysis, multiple regression modeling, statistical validation

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** Link to the data source(s) 
    - https://github.com/princenewman02/Education/blob/main/Data/EdGap_Data.xlsx - ACT scores and socioeconomic variables (school/district level)
    - https://github.com/princenewman02/Education/blob/main/Data/ccd_sch_029_1617_w_1a_11212017%20(1).csv - School information and demographics
    - https://github.com/princenewman02/Education/blob/main/Data/school_finance_2016_17.csv - District-level expenditure and enrollment data

- **Description:** 
        The datasets contain school-level ACT performance, demographics, and socioeconomic variables for U.S. high schools. District-level financial data was merged using an extracted district ID to match granularity. Data was cleaned, transformed, and prepared for regression analysis. The output is `education_clean_new_2.csv` containing 7,227 high schools ready for analysis. 

- **License:** (if applicable)

---

## Analysis

    - The analysis was conducted using Education.ipynb, documenting the complete workflow from loading raw datasets to final regression modeling.
    - The process begins with importing and exploring the three main datasets to understand structure, data types, and quality.
    - A critical integration step resolved the granularity mismatch between school-level demographics and district-level finance data by creating `extracted_district_id` for harmonized merging using `[state, extracted_district_id]` as join keys.
    - Exploratory data analysis revealed poverty (percent_lunch) as the strongest predictor (r = -0.78) while school spending showed weak correlation (r = 0.10).
    - Quality control included removing invalid values, filtering for high schools only, handling missing data via state-median imputation for six states (MI, LA, IL, PA, TN, WI), and applying log transformations to skewed variables (expenditure_per_pupil, enrollment).
    - Multiple regression modeling progressed from simple linear regression (R² = 0.21) to full seven-predictor model (R² = 0.63 but severe multicollinearity) to final normalized three-predictor model (R² = 0.628, Condition Number = 1.93).
    - The final model identified poverty (percent_lunch), education attainment (percent_college), and unemployment as significant predictors, while school spending and median income were not significant.
    - To reproduce results, run Education.ipynb sequentially through data loading, merging, cleaning, transformation, and modeling steps.
 
    ---

## Results
    - Produced a cleaned, analysis-ready dataset linking ACT scores with socioeconomic and financial indicators
    - Socioeconomic factors explain 62.8% of variance in ACT scores with 1.15-point average prediction error
    - Poverty (percent_lunch) emerged as the dominant predictor with effect size six times larger than educational attainment
    - School spending showed no significant effect when controlling for socioeconomic factors
    - Established a reproducible data integration and modeling pipeline for educational inequality analysis.

---

## Authors

- Prince Newman (https://github.com/@princenewman02)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

 - Python libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
 - Project guidance from Data 5100 Education project modules
 - U.S. Department of Education datasets
