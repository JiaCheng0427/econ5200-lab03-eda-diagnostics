Pipeline Health Check — EDA, Corruption & Distribution Shift
Objective
This project focuses on identifying data-quality problems, correcting corrupted observations, and monitoring distribution shift before data is used in a production pipeline.
Methodology
- Used exploratory data analysis to identify five planted data-quality issues in a country-level panel dataset.
- Corrected negative GDP values and inconsistent GDP units.
- Fixed life expectancy values that were incorrectly stored in months.
- Identified duplicate country-year observations.
- Standardized inconsistent percentage values in the trade variable.
- Split the cleaned data into training and inference datasets.
- Measured distribution shift using the Population Stability Index (PSI).
- Compared manual EDA with automated profiling using ydata-profiling.
- Created reusable EDA utility functions for data-quality checks, PSI calculation, and dataset summaries.
- Built an interactive pipeline-health dashboard for monitoring distributions, constraints, and data quality.
Key Findings
The original dataset contained five different data-quality issues that were identified and corrected through EDA. After cleaning, all verification checks passed.
The GDP variable showed a clear distribution shift between the training and inference datasets, with a PSI value of 2.4589. Other variables showed smaller differences, highlighting the importance of considering sample size and normal variation when interpreting PSI.
The comparison between manual and automated EDA also showed that automated profiling can quickly detect unusual values and outliers, but some problems, such as unit mismatches and duplicate country-year observations, still require domain knowledge and manual investigation.
Overall, this lab showed how data-quality checks and distribution monitoring can be combined to improve the reliability of a production data pipeline.
