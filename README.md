# Mumbai Rental Property Data Analysis

**IAAC — AI Methods | Group 3**

## Project Overview

This project investigates rental property listings in Mumbai using Python, pandas, and data visualization techniques.

Our objective is to develop a reproducible workflow combining data cleaning, exploratory data analysis (EDA), geographic comparisons, and data quality validation.

The final analysis is consolidated into a single Jupyter notebook.

## Team Members and Contributions

- **Ahmed Belahcen:** Initial exploration, preliminary cleaning and analysis, final notebook consolidation, and integration.
- **Nandini Rathod:** Data cleaning, refactoring, and dataset preparation.
- **Sanjana Kiran:** Exploratory data analysis, statistical comparisons, and visualizations.
- **Akanksha Dhumal:** Data validation, consistency checks, outlier analysis, and potential bias assessment.

All members contributed to project development and GitHub collaboration.

## Dataset

**Source:** Property Rental Listings Dataset — Kaggle  
**Author:** harshalhonde  
**Original file:** `Mumbai_property_details.csv`

- Original dataset: 23,405 records and 18 columns.
- Final analytical dataset: 18,846 records.
- Key variables: rental price, property area, BHK, bathrooms, balconies, furnishing, orientation, and location.

The original dataset contains missing values, inconsistent attributes, and potentially anomalous property listings.

## Project Structure

```text
Group3-day1assignment/
├── data/
├── notebooks/
│   └── final_analysis.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Methodology

### 1. Data Exploration and Cleaning

The dataset was inspected for missing values, duplicates, inconsistent categories, and potentially invalid numerical records.

Cleaning decisions aimed to improve consistency while preserving plausible property listings, including high-value luxury properties.

Missing balcony information was retained as missing rather than automatically interpreted as zero.

### 2. Exploratory Data Analysis

The analysis investigates relationships between rental prices and property characteristics, including:

- Property area and monthly rent.
- Bedroom count (BHK) and rental prices.
- Furnishing status and rental values.
- Property orientation and rent per reported area unit.
- Geographic differences between Mumbai neighborhoods.

### 3. Neighborhood and Orientation Analysis

Neighborhoods were extracted from property listing titles.

The analysis compares median rental values across locations and examines orientation-related differences within neighborhoods.

For greater comparability, the neighborhood-orientation analysis focuses on 2 BHK properties and uses median rent per reported area unit.

### 4. Data Validation

The final workflow includes:

- Missing-value assessment.
- Numerical consistency checks.
- Review of cleaning decisions and potential anomalies.
- Sample-size validation for neighborhood-orientation comparisons.
- Documentation of analytical limitations.

## Key Findings

- Rental values differ substantially across Mumbai neighborhoods and property categories.
- Lower Parel, Bandra, Khar, and Prabhadevi exhibit relatively high median rents in the analyzed sample.
- Borivali, Kandivali, and Kurla show comparatively lower median rents.
- Property size alone does not explain rental-price differences.
- Orientation-related rental differences vary across neighborhoods.
- In Andheri, several orientations show similar median rent-per-area values for 2 BHK properties.
- In Bandra, West-facing 2 BHK properties show higher median rent per area than East-facing properties.
- Some apparently large orientation-related differences are supported by relatively small samples and require cautious interpretation.

These findings are descriptive and do not establish causal relationships.

## Data Quality Summary

The final analytical dataset contains **18,846 listings**.

- Rental price, area, and BHK: no missing values in the final dataset.
- Bathrooms: 15 missing values.
- Balconies: 10,323 missing values (54.78%).
- Year of construction: 5,229 missing values (27.75%).

Missing data and sample coverage are considered when interpreting the results.

## How to Run

1. Clone the repository.
2. Create and activate a Python virtual environment.
3. Install the project dependencies:

```bash
pip install -r requirements.txt
```

4. Make the required dataset available at the path expected by the notebook.
5. Open `notebooks/final_analysis.ipynb` in VS Code or Jupyter.
6. Select the appropriate Python environment and run the notebook from beginning to end.

## Limitations

- Neighborhood information was extracted from listing titles and may not be geographically precise.
- The dataset may not represent the entire Mumbai rental market.
- The measurement unit of property area requires verification.
- Missing balcony and construction-year information limits certain comparisons.
- Property quality, amenities, building age, and micro-location may influence observed rental differences.
- Small sample sizes may affect the stability of some median estimates.
- The analysis does not establish causal effects or current market trends.

## Conclusion

This project demonstrates a collaborative approach to rental-market data analysis, combining data preparation, visualization, geographic comparisons, and quality assessment.

The consolidated notebook provides an exploratory foundation for future rental-price modeling and more advanced property valuation studies.

