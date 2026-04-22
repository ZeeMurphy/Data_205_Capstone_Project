# CDC BRFSS — Alzheimer's Disease and Healthy Aging Data

## Overview
This dataset is too large to store in this repository (140MB).
It is loaded directly from the CDC SODA2 API in the notebook.

## Source
- **Organization:** Centers for Disease Control and Prevention (CDC)
- **Survey:** Behavioral Risk Factor Surveillance System (BRFSS)
- **Dataset name:** Alzheimer's Disease and Healthy Aging Data
- **Years covered:** 2015–2022
- **URL:** https://data.cdc.gov/Healthy-Aging/Alzheimer-s-Disease-and-Healthy-Aging-Data/hfr9-rurv

## How to Access
The notebook loads this data automatically via the CDC SODA2 API:
```python
CDC_URL = "https://data.cdc.gov/resource/hfr9-rurv.csv?$limit=300000"
df = pd.read_csv(CDC_URL)
```
No API key or account is required.

## Dataset Characteristics
- **Rows:** 284,142
- **Columns:** 31
- **Unit of observation:** One row per survey question per
  location per year per demographic subgroup
- **Population:** U.S. adults aged 45 and older
- **Geographic coverage:** 50 states + DC + territories
- **Format:** Long format — reshaped to wide in the notebook

## Key Variables Used
| Variable | Description |
|---|---|
| Question | Survey question text |
| Data_Value | Percentage of respondents |
| LocationAbbr | State abbreviation |
| YearStart | Survey year |
| Stratification1 | Age group or Overall |
| Class | Health topic category |

## Notes
- The dataset includes 59 locations — territories and regional
  rollups are filtered out in the notebook
- The cognitive decline module is optional — not all states
  report it every year
- After filtering and pivoting: 406 state-year combinations
- After removing missing cognitive decline rows: 173 usable rows
