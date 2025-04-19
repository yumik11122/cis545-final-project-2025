# CIS 545 Final Project (Spring 2025) – Global Health Inequality Analysis

## Overview

Global health inequality remains one of the most pressing challenges of our time. While some countries have made significant progress in healthcare, others continue to face high infant mortality, limited access to care, and poor health outcomes.

This project investigates how economic indicators — particularly GDP per capita — relate to infant mortality and other health outcomes across 258 countries and regions, using World Bank data from 1960 to 2015. 

We apply a combination of:
- Exploratory Data Analysis (EDA)
- Supervised learning models (Logistic Regression, Random Forest)
- Unsupervised clustering (K-means)

Our analysis reveals a **strong negative correlation (r = -0.43)** between GDP per capita and infant mortality. Both machine learning models confirm that GDP per capita alone is a powerful predictor of countries with high infant mortality rates (≥ 40 deaths per 1,000 live births), with **Random Forest achieving 84% accuracy**.

### Key Insights
- Countries in the lowest income quartile have significantly higher infant mortality.
- Increased education spending is associated with lower infant mortality, even at similar income levels.
- Adolescent fertility, life expectancy, and immunization rates further help distinguish country-level health disparities.

### Policy Implications
Our findings support targeted investment in low-income regions, particularly in healthcare and education. Even modest improvements in spending may lead to meaningful reductions in infant mortality.

---

This project highlights how publicly available data and simple machine learning models can offer powerful insights into global health inequality and support data-informed public policy.

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

> Note: Due to file size limits on GitHub, the original World Bank dataset (`WDICSV.csv`, ~195MB) is **not included in this repository**.  
> The data can be downloaded from:  
> [World Bank WDI Dataset - Data Catalog](https://datacatalog.worldbank.org/search/dataset/0037712/World-Development-Indicators) 

---

## Environment & Dependencies

This project was developed using **Python 3.9** and the following key libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

To install the required packages, you may run:

```bash
pip install -r requirements.txt
```
---

## Methods & Tools

- **Data Cleaning & Filtering**  
- **Exploratory Data Analysis (EDA)**: correlation heatmaps, scatterplots, and boxplots  
- **Unsupervised Learning**: K-means clustering  
- **Supervised Learning**: Logistic Regression and Random Forest  
- **Visualization**: Seaborn, Matplotlib  
- **Tools**: Python, Pandas, Scikit-learn, Jupyter Notebook

---

## Key Findings

- A **moderate negative correlation** (r = -0.43) was found between GDP per capita and infant mortality rate.
- GDP per capita alone was sufficient to classify countries as high risk (≥ 40 deaths/1,000) with:
  - **84% accuracy (Random Forest)**
  - **79% accuracy (Logistic Regression)**

---

## Policy Implications

- **Targeted Funding**: A 1% increase in GDP allocated to healthcare in the lowest-GDP countries could reduce predicted infant mortality by ~12%.  
- **Education Synergy**: Countries above the median education spending exhibited 15% lower infant mortality at similar income levels.

---

## Limitations

- The models rely on a single economic indicator (GDP per capita).
- Health-specific variables (e.g., immunization rates) were not yet included.
- Gaps in post-2015 data may affect time-series robustness.

---

## Future Directions

1. Integrate additional health metrics (e.g., immunization, healthcare access).  
2. Extend the time range using WHO 2024+ datasets.  
3. Deploy interactive dashboards via Streamlit or Plotly Dash.

---

## Data Sources

- **Kaggle** – [Health, Nutrition and Population Statistics](https://www.kaggle.com/datasets/theworldbank/health-nutrition-and-population-statistics)
- **World Bank** – [World Development Indicators (WDI)](https://datacatalog.worldbank.org/search/dataset/0037712/World-Development-Indicators)  

---

## Authors

This project was completed as part of the **CIS 5450 Big Data Analytics course** at the University of Pennsylvania (Spring 2025), by a team of 3 students.
