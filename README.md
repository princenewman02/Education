# Educational Inequality Data Processing

> An analysis of the relationship between U.S. high school performance on standardized exams (ACT/SAT) and socioeconomic factors.

---

## Project Overview

This project explores inequality of educational opportunity across U.S. high schools by analyzing whether socioeconomic variables are associated with school performance on standardized exams such as the ACT and SAT.

The work focuses on cleaning, processing, and preparing educational data for further analysis and modeling.

- **Objective:** Examine how socioeconomic factors relate to ACT scores across schools in the United States..
- **Domain:** Education / Social Data Analysis
- **Key Techniques:** Data cleaning, exploratory data analysis (EDA), visualization, imputation, and data integration

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
    - EdGap_data.xlsx - ACT scores and socioeconomic data
    - ccd_sch_029_1617_w_1a_11212017.csv - school information dataset

- **Description:** 
    The datasets contain school-level ACT/SAT performance, demographics, and socioeconomic variables for U.S. high schools. Data was cleaned, joined, and prepared for regression and exploratory analysis. The output is a fully cleaned dataset ready for analysis. 

- **License:** (if applicable)

---

## Analysis

 - The analysis was conducted using a single Jupyter notebook, Education.ipynb, which documents the complete data processing workflow from loading raw datasets to exporting the cleaned dataset. 
 - The process begins with importing and exploring the two main datasets - EdGap_data.xlsx and ccd_sch_029_1617_w_1a_11212017.csv - to understand their structure, data types, and quality. 
 - Exploratory data analysis was then performed using pair plots to visually assess relationships between ACT scores and socioeconomic variables, providing early insights into potential correlations and data suitability. 
 - Next, the school information dataset was subsetted to retain only relevant columns, renamed for readability, and joined with the EdGap dataset using a left join to ensure all ACT data were preserved. Quality control steps followed, including removing invalid or out-of-range values, filtering for high schools, handling duplicates, identifying missing values and imputing them using regression-based techniques to ensure completeness. 
 - Finally, the cleaned dataset is exported as a CSV file for further statistical analysis or modeling.
 - To reproduce the results, run the Jupyter notebooks in sequential order - starting from data loading and exploration, through cleaning and imputation, and ending with the export of the final dataset.
 
    ---

## Results
    - Produced a cleaned, analysis-ready dataset linking ACT scores with socioeconomic indicators.
    - Identified clear relationships suggesting socioeconomic disparities in school performance.
    - Established a reproducible data-cleaning pipeline for educational data.

---

## Authors

- (https://github.com/@princenewman02)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

 - Python libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
 - Project guidance from Data 5100 Education project modules
 - U.S. Department of Education datasets
