# CIS 545 Final Project (Spring 2025) – Global Health Inequality Analysis

## Authors

This project was completed as part of the **CIS 5450 Big Data Analytics course** at the University of Pennsylvania (Spring 2025),  
by a team of 3 students (names withheld for privacy).

---

## Review Request

This is my first time uploading a project to GitHub. While I’ve used GitHub for coursework submissions, I’m still new to collaboration features like Pull Requests.

If you have a moment, I’d greatly appreciate any feedback on the overall structure, flow, and analysis presented in this notebook.

Thank you so much in advance!

---

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
2. Ensure the `data/` directory contains the required `.csv` files.
3. Open `545-Group-Project-v4.ipynb` in Jupyter Notebook or Google Colab.
4. Run all cells to reproduce the analysis and visualizations.

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
