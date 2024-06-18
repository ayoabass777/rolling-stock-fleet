# Rolling Stock Fleet Project

## Table of Contents
- [Executive Summary](#executive-summary)
- [Problem Statement](#problem-statement)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Model Selection](#model-selection)
- [Visualization](#visualization)
- [Recommendations](#recommendations)
- [References](#references)

## Executive Summary
The "Rolling Stock Fleet" project aimed to analyze and optimize a vehicle fleet dataset comprising 1185 rows and 12 columns. The dataset recorded vital operational data including average mileage, downtime, and labor hours. Significant variability and data integrity issues were addressed through extensive cleaning and transformation, ensuring reliable analysis. The project employed the Random Forest Regressor to model non-linear relationships within the dataset, achieving high predictive accuracy. Visualizations highlighted fleet composition, usage, and maintenance needs, facilitating informed decision-making. Recommendations focused on reducing fleet size, improving sustainability, and enhancing operational efficiency.

## Problem Statement
The Rolling Stock Fleet dataset, capturing key operational data, faced significant challenges due to missing and inconsistent data, particularly in "HourMeter2020(hours)" and "Mileage2020 (km)." These issues compromised the dataset's reliability, necessitating comprehensive data cleaning and transformation. The objective was to ensure data integrity for accurate analysis, guiding fleet optimization and reducing operational costs and environmental impact.

## Data Cleaning and Transformation
To address data integrity issues, the following steps were taken:

1. **Error Identification and Missing Data Handling**:
   - Removed the "HourMeter2020(hours)" column with over 69% missing data.
   - Imputed missing values in other columns using logical assumptions and advanced statistical methods (e.g., K-Nearest Neighbors for mileage data).
   
2. **Normalization and Encoding**:
   - Applied logarithmic transformation to normalize skewed distributions of "DowntimeHours2020(hours)" and "LaborHours2020(hours)".
   - One-hot encoding was applied to categorical variables like equipment category and service group.
   
3. **CO2 Emissions Data Integration**:
   - Consolidated secondary CO2 emissions data from 1995 to 2019.
   - Merged datasets using a left-join strategy on 'Make' and 'Year'.

## Model Selection
The Random Forest Regressor was chosen to model the dataset's non-linear traits, achieving:

- Mean Squared Error: 14.5
- R² Score: 0.98
- Mean Absolute Percentage Error: 0.44

Hyperparameter tuning via GridSearchCV identified the optimal configuration, significantly improving model performance.

## Visualization
Key visualizations include:

### Correlation Matrix
![Correlation Matrix](./path/to/key-visual.png)

This correlation matrix highlights the significant negative correlation between the year of the vehicle and its average CO2 emissions (g/km). Older vehicles are shown to have a relationship with higher emissions, underscoring the need for fleet modernization to enhance environmental sustainability.

## Recommendations
1. **Fleet Downsizing**:
   - Identify and remove underutilized vehicles with high downtime and labor hours.
   - Replace older, more polluting vehicles with newer, efficient models.

2. **Operational Efficiency**:
   - Enhance fleet utilization and reduce operational costs.
   - Monitor and adjust strategies continuously to ensure flexibility.

3. **Environmental Sustainability**:
   - Aim for targeted reductions in CO2 emissions across the light-duty fleet.
   - Emphasize fuel efficiency, vehicle maintenance, and operational practices.

## References
- Government of Canada. (n.d). Fuel consumption ratings. OpenCanada. [Link](https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64/resource/2309538b-53d1-4635-a88e-e237bfcef7a2)


For further details, please refer to the complete project documentation and visualizations included in the appendices.
