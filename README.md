# Data_205_Capstone_Project# Cognitive Decline Risk Factors in U.S. Older Adults
## Exploratory Data Analysis | DATA 205 Capstone Project
**Montgomery College | Spring 2025**
**Author: Zivar Murphy**

---

## Project Overview

This project investigates the health, behavioral, and socioeconomic 
factors associated with cognitive decline among older adults across 
U.S. states. Using CDC BRFSS survey data (2015–2022) and U.S. Census 
Bureau ACS estimates, I examine which risk factors are most strongly 
correlated with state-level cognitive decline rates and how these 
patterns vary geographically across the United States.

---

## Research Questions

This project addresses 13 research questions across four themes:

**Geographic Patterns**
- RQ1: Which states have the highest and lowest cognitive decline rates?

**Demographics**
- RQ2: Does cognitive decline differ between the 50–64 and 65+ age groups?
- RQ3: How do early-stage and severe cognitive decline measures relate to each other?

**Health & Behavioral Risk Factors**
- RQ4–RQ9: How do depression, mental distress, physical inactivity, poor 
  health, disability, unhealthy days, smoking, and binge drinking correlate 
  with cognitive decline?

**Socioeconomic Factors & Prediction**
- RQ10: Does median household income relate to cognitive decline across states?
- RQ11: Does higher educational attainment reduce cognitive decline?
- RQ12: Which combination of variables best predicts cognitive decline?
- RQ13: Are health and behavioral risk factors getting better or worse over time?

---

| Dataset | Source | Years | Variables |
|---------|--------|-------|-----------|
| CDC BRFSS Alzheimer's Disease and Healthy Aging Data | [data.cdc.gov](https://data.cdc.gov/Healthy-Aging/Alzheimer-s-Disease-and-Healthy-Aging-Data/hfr9-rurv) | 2015–2022 | Cognitive decline, depression, mental distress, physical inactivity, poor health, disability, smoking, binge drinking |
| U.S. Census Bureau ACS 5-Year Estimates | [census.gov](https://www.census.gov/data/developers/data-sets/acs-5year/2022.html) | 2018–2022 | Median household income (DP03_0062E), % Bachelor's degree or higher (DP02_0068PE) |

---

## Key Findings

- **Poor health is the strongest predictor** of cognitive decline at the 
  state level (r = 0.80, p < 0.001), followed by disability (r = 0.69), 
  unhealthy days (r = 0.67), and mental distress (r = 0.67)
- **Southern states consistently show the highest rates** — Mississippi, 
  Tennessee, Alabama, Louisiana, and West Virginia cluster at the top 
  across all years
- **The 50–64 age group reports higher cognitive decline** (44.1%) than 
  the 65+ group (29.9%), likely reflecting differences in self-reporting 
  behavior
- **Higher income and education are associated with lower cognitive decline** 
  (r = −0.49 and r = −0.34 respectively)
- **Smoking is the only risk factor showing consistent improvement** over 
  2015–2022; Mental Distress is the only one showing a consistent rise
- **A multiple regression model** combining all 10 predictors explains 
  74.2% of the variation in state-level cognitive decline rates (R² = 0.742)
---
## Interactive Dashboard

Explore the CDC BRFSS cognitive decline data by state, including risk factors 
and local resources for older adults:

👉 **[View Live Dashboard](https://zeemurphy.github.io/Data_205_Capstone_Project/analysis/dashboard/cognitive_decline_dashboard.html)**
## How to Run

The notebook loads data directly from the CDC SODA2 API — no file 
downloads needed. Simply open the notebook in Google Colab or Jupyter 
and run all cells in order.

**Requirements:**
- Python 3.x
- pandas, numpy, matplotlib, seaborn, plotly, scipy, scikit-learn

```bash
pip install pandas numpy matplotlib seaborn plotly scipy scikit-learn
```

---

## Methodology Notes

- All correlations and regression analyses use **one mean value per state** 
  averaged across all reported years, giving every state equal weight 
  regardless of how many years it participated in the optional BRFSS 
  cognitive decline module
- Cognitive decline data is from an **optional BRFSS module** — coverage 
  ranges from 1 year (Montana, Massachusetts) to 8 years (Oregon)
- Risk factor variables are **mandatory BRFSS questions** with near-complete 
  coverage (50–51 states per year across all 8 years)
- **2020 values** are included in trend analysis and flagged where relevant 
  as a COVID disruption year

---
