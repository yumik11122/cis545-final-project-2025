# CIS 545 Final Project (Spring 2025) – Global Health Inequality Analysis

## Authors

This project was completed as part of the **CIS 5450 Big Data Analytics course** at the University of Pennsylvania (Spring 2025), by a team of 3 students (names withheld for privacy).

---

## Review Request

This is my first time uploading a project to GitHub. While I’ve used GitHub for coursework submissions, I’m still new to collaboration features like Pull Requests.

If you have a moment, I’d greatly appreciate any feedback on the overall structure, flow, and analysis presented in this notebook.

Thank you so much in advance!

---

## Overview

Global health inequality remains a persistent global challenge. While some countries have made significant progress in healthcare, others continue to face high infant mortality, limited access to care, and poor health outcomes.

This project investigates how economic indicators -- particularly GDP per capita -- relate to health outcomes across 258 countries and regions, using World Bank data spanning from 1960 to 2015. We place special emphasis on infant mortality as a key metric of national health.

We apply a combination of:
- Exploratory Data Analysis (EDA)
- Supervised learning models (Logistic Regression, Random Forest)
- Unsupervised clustering (K-means)

Our analysis reveals a **strong negative correlation (r = -0.43)** between GDP per capita and infant mortality. Both machine learning models confirm that GDP per capita alone is a powerful predictor of countries with high infant mortality rates (≥ 40 deaths per 1,000 live births), with **Random Forest**: 84% accuracy (compared to 79% for Logistic Regression)

### Key Findings

- **Clear economic–health link**: Our exploratory analysis confirmed a strong negative relationship between GDP per capita and infant mortality, using 258 unique World Bank country codes and more than 50 years of global health data (1960–2015).

- **Policy-relevant impact**: Among the lowest–GDP countries, diverting just 1% of GDP toward healthcare was associated with a ~12% reduction in infant mortality. For example, in a country with a $50B GDP, this equates to approx. $500M and could potentially save 60,000 infants -- or ~$8,300 per life saved.  
  In per capita terms, this corresponds to just $10–15 per person per year in a low-income country -- a potentially powerful message for policymakers and advocates.

- **GNP-based inequality**: Countries with high infant mortality had dramatically lower GNP per capita -- median ~$550 compared to ~$11,000 in low-mortality countries -- highlighting deeper structural inequalities not captured by GDP alone. This additional lens helped improve our understanding and interpretation of borderline economies.

- **Model accuracy**: Using GDP per capita alone, our supervised models achieved:  
  – **Logistic Regression**: 79% accuracy  
  – **Random Forest**: 84% accuracy  
  Accuracy refers to correct classification of countries as high– or low–risk for infant mortality.

- **Limitations of GDP–only approach**: Misclassifications were most common among middle–income countries, where health investment patterns often vary independently of economic development. Adding health-specific features (e.g., immunization rates) may improve performance.

### **Cluster Analysis Insights**
- K-means clustering revealed distinct country groupings based on health and economic indicators:

 - Cluster 1 (High-income countries): Characterized by high GDP per capita (~$35,000), low infant mortality (~5 per 1,000), and strong healthcare infrastructure

 - Cluster 2 (Middle-income countries): Moderate GDP (~$5,000), improving health metrics, but variable healthcare access

 - Cluster 3 (Low-income countries): Very low GDP (~$500), high infant mortality (~80 per 1,000), and limited healthcare resources

 - Cluster 4 (Transitional economies): Countries showing rapid improvement in health metrics despite modest economic growth


### **Limitations**
- **Single Economic Indicator:**  
  Our predictive models rely heavily on GDP per capita as the primary feature, which may oversimplify the complex determinants of infant mortality.  
  Future work could explore incorporating health-specific features such as immunization rates and healthcare expenditure to improve model precision -- especially for middle-income countries where health investment policies vary independently of economic development.

- **Data Gaps Post-2015:**  
  Limited recent data restricts our ability to analyze current trends.  
  One possible enhancement is integrating upcoming WHO 2024 data releases, which would enable analysis of more recent trends and validation of our findings across a more contemporary timeframe.

- **Static Regional Mapping:**  
  Country-to-region mapping is static and doesn’t account for geopolitical changes.  
  Another improvement could involve implementing dynamic regional mapping using yearly geopolitical reference data to better reflect changing global contexts and regional realignments.

- **Future Work**:
1. Enrich the feature set with vaccination coverage and health‑expenditure metrics.
2. Extend the time horizon by merging WHO 2024 data releases.
3. Build an interactive dashboard (Plotly Dash or Streamlit) to allow policymakers to explore scenario‑based outcomes.
4. Incorporate scenario-based simulations (e.g., best-case and worst-case) using dynamic region-health mappings to better inform resource allocation under uncertainty.

---

## Repository Structure

```
.
├── 545-Group-Project-v4.ipynb            # Final project notebook
├── data/
│   ├── WDICSV.csv                        # World Bank indicators (cleaned)
│   └── full_country_region_mapping.csv   # Country-to-region mapping
└── README.md                             # This file
```

> Note: Due to GitHub size limits, the original World Bank dataset (`WDICSV.csv`, ~195MB) is **not included**.  
> You can download it from:  
> [World Bank WDI Dataset - Data Catalog](https://datacatalog.worldbank.org/search/dataset/0037712/World-Development-Indicators)

---

## How to Run

1. Clone or download this repository.
2. Make sure the `data/` directory includes the following files:
   - WDICSV.csv
   - full_country_region_mapping.csv
3. Open the notebook (`.ipynb` file) using Jupyter Notebook or Google Colab.
4. Run all cells from top to bottom to reproduce the analysis and visualizations.

---

## Environment & Dependencies

Developed using **Python 3.9** with the following key libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

To install dependencies:
```bash
pip install -r requirements.txt
```
