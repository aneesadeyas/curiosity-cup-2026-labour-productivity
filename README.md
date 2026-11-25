# Assessing Labour Productivity in Malaysia: Sectoral Trends and Analytical Insights

## Project Overview

This group research project was conducted as part of the Curiosity Cup 2026, a global SAS student competition, by Team Curiosity Catalysts from Universiti Malaya.

The study investigates labour productivity across Malaysian economic sectors from 2015 to 2024 using statistical analysis and machine learning techniques. It examines productivity trends, relationships between economic indicators, and structural differences in labour efficiency.

## Research Objectives

- Examine labour productivity trends across Malaysian economic sectors.
- Investigate relationships between GDP, employment, working hours, and labour productivity.
- Identify distinct productivity groups using K-means clustering.
- Classify productivity levels using decision tree modelling.
- Provide statistical insights to support evidence-based economic planning.

## Tools and Technologies

- SAS OnDemand for Academics
- SAS Viya
- SAS Model Studio

## Dataset Description

The labour productivity data was obtained from the Department of Statistics Malaysia (DOSM) through OpenDOSM.

- Study period: 2015–2024
- Data frequency: Annual
- Unit of analysis: Economic sector and year

### Main Variables

| Variable | Description |
|---|---|
| GDP | Gross Domestic Product |
| Working Hours | Labour input measured through working hours |
| Employment | Employment level |
| Output per Hour | Labour productivity measured by output per hour worked |
| Output per Employment | Labour productivity measured by output per worker |

### Data Source

Department of Statistics Malaysia (DOSM):
https://open.dosm.gov.my/data-catalogue/productivity_annual

## Methodology

### 1. Data Preparation

- Imported the dataset into SAS using PROC IMPORT.
- Verified dataset structure and variable information using PROC CONTENTS.
- Prepared economic and productivity indicators for statistical analysis.

### 2. Descriptive Statistics and Exploratory Data Analysis

- Examined the distribution and variability of economic indicators.
- Compared labour productivity across economic sectors.
- Visualised annual productivity trends.
- Examined productivity performance before, during, and after the COVID-19 pandemic.

### 3. Correlation Analysis

- Applied Pearson correlation analysis to examine relationships between economic and productivity indicators.
- Evaluated the direction, strength, and statistical significance of relationships.
- Investigated whether increases in labour input were associated with higher productivity.

### 4. K-Means Clustering

- Applied K-means clustering to identify distinct productivity groups.
- Used the elbow method to determine a suitable number of clusters.
- Selected a three-cluster solution (k = 3).
- Examined cluster characteristics using means and standard deviations.
- Categorised observations into low, moderate, and high productivity groups.

### 5. Decision Tree Classification

- Used productivity categories derived from K-means clustering as the target variable.
- Included GDP, working hours, and employment as predictor variables.
- Applied a training-validation split and cost-complexity pruning.
- Evaluated classification performance using a confusion matrix.

## Results and Key Findings

### Labour Productivity Trends

- Labour productivity generally improved before 2020.
- Productivity declined during the COVID-19 pandemic.
- A gradual but uneven recovery was observed from 2021 onwards.
- Productivity performance varied substantially across economic sectors.

### Correlation Analysis

- GDP, employment, and working hours exhibited strong positive correlations.
- Employment and working hours were negatively associated with labour productivity indicators.
- GDP showed weak and statistically insignificant relationships with productivity measures.

These findings suggest that increasing labour input does not necessarily lead to higher labour efficiency.

### K-Means Clustering

The elbow method supported a three-cluster solution.

| Productivity Group | Observations | Percentage |
|---|---:|---:|
| Low | 164 | 74.55% |
| Moderate | 46 | 20.91% |
| High | 10 | 4.55% |
| Total | 220 | 100% |

The clustering results highlight substantial differences in labour productivity across the observations, with the majority belonging to the low-productivity group.

### Decision Tree Classification

Working hours emerged as the primary splitting variable, while GDP helped distinguish between productivity categories.

#### Confusion Matrix

| Actual / Predicted | High | Low | Moderate |
|---|---:|---:|---:|
| High | 10 | 0 | 0 |
| Low | 0 | 162 | 2 |
| Moderate | 0 | 2 | 44 |

#### Classification Performance

- Correctly classified observations: 216 out of 220
- Misclassified observations: 4
- Overall classification accuracy: 98.18%

The reported confusion matrix indicates strong agreement between predicted and actual productivity categories. However, the evaluation subset is not clearly identified in the report, so this result should not be interpreted as independently verified test accuracy.

## Conclusion

The study identified substantial differences in labour productivity across Malaysian economic sectors.

The findings suggest that productivity improvement should focus on labour efficiency, skills development, technological advancement, and sector-specific economic conditions rather than relying solely on increases in employment and working hours.

This project demonstrates the application of statistical analysis and machine learning techniques to real-world economic data and evidence-based decision-making.

## Limitations

- Correlation does not establish causation.
- Productivity categories were derived from clustering rather than independently defined labels.
- Additional validation is required to assess model generalisability.
- The original SAS source code is not included in this repository.
- The exact filtering steps used to obtain the analytical dataset are not fully documented.

## Skills Demonstrated

- Descriptive statistics
- Exploratory data analysis
- Pearson correlation analysis
- Statistical data visualisation
- Unsupervised machine learning
- K-means clustering
- Elbow method
- Supervised machine learning
- Decision tree classification
- Model performance evaluation
- Statistical interpretation and reporting
- Collaborative research and analytical problem-solving

## Repository Contents

- `SAS project version 2.pdf` — Full competition research report, including methodology, statistical outputs, visualisations, and findings.
- `productivity_annual (2).csv` — Annual labour productivity dataset obtained from OpenDOSM.

## Competition Information

- Competition: SAS Curiosity Cup 2026
- Team: Curiosity Catalysts
- Institution: Universiti Malaya
- Programme: Bachelor of Science in Statistics
- Project Type: Group research project

## Reference

Department of Statistics Malaysia (DOSM). Annual Productivity by Economic Sector. OpenDOSM.

