# Housing Code Analysis
Code for Analysis of Housing Code Violations

## Overview
The goal of this project is to perform an ETL (Extract, Transform, Load) process and exploratory data analysis on public housing data to identify patterns in hazardous living conditions. This analysis aligns with the OAG's purview of supporting major initiatives and investigations that affect the lives of New Yorkers, particularly in areas concerning social and economic justice.

## Methodology & ETL Process
The analysis is conducted in Python, utilizing standard, reproducible methodologies to extract, clean, and visualize data. 

1. **Extraction (Data Sourcing):** * The project extracts a dataset of 5,000 recent housing violations directly from the NYC Open Data API.
2. **Transformation (Data Cleaning):**
   * **Standardization:** All dataset column names are converted to lowercase and stripped of hidden whitespace to ensure consistent querying.
   * **Formatting:** Inspection dates are converted into standard Python `datetime` objects for time-series compatibility.
   * **Filtering:** The dataset is filtered to isolate 'Class C' violations, which represent "Immediately Hazardous" conditions.
   * **Handling "Dirty" Data:** Rows missing critical geographic information (Zip Codes) are dropped to maintain the integrity of the location-based analysis.
3. **Load & Analysis:**
   * The cleaned data is aggregated to calculate the frequency of severe violations per zip code, pinpointing specific geographic hotspots that may warrant further investigation.

## Visualizations & Findings
To clearly communicate the findings, the notebook includes data visualizations built with `matplotlib`:
* **Severe Violation Hotspots (Bar Chart):** Highlights the Top 10 NYC Zip Codes with the highest concentration of Class C (Immediately Hazardous) violations. 
* **Violation Severity Distribution (Pie Chart):** Displays the overall distribution of all violation severities across the dataset to provide broader context on housing conditions.

## Technologies Used
* **Language:** Python 3
* **Libraries:** `pandas` (for data manipulation/ETL), `numpy`, `matplotlib` (for data visualization)
* **Environment:** Jupyter Notebook / Google Colab 

## How to Run
You can view and execute the code interactively by clicking the "Open in Colab" badge at the top of the Jupyter Notebook (`OAG_Code_for_Housing_Analysis.ipynb`). Local installation is not required.
