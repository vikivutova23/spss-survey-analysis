# Mean Age of Mothers at Childbirth: Bulgaria vs EU-27 (2001–2021)

Time series analysis and short-term forecast of the mean age of women at childbirth in Bulgaria and the EU-27, based on official Eurostat data. Developed as my Bachelor's thesis in Business Data Analysis at the University of National and World Economy (UNWE), Sofia.

## Objective

To analyse how the mean age of mothers at childbirth has changed in Bulgaria and the EU-27 over 2001–2021, compare the two trends, and forecast the indicator for Bulgaria for 2022–2024.

## Data

- **Source:** Eurostat, *Population and social conditions → Fertility* (`demo_find`), indicator "Mean age of women at childbirth"
- **Coverage:** Bulgaria and EU-27, annual data, 2001–2021 (21 observations)
- **File:** `mother_age_bg_eu27_2001_2021.csv`

## Tools

- **Microsoft Excel**: data preparation, dynamics indicators (absolute changes, growth rates), charts
- **IBM SPSS Statistics**: descriptive statistics, curve estimation, regression and ANOVA, ARIMA modelling and forecasting (Expert Modeler)

## Methodology

1. Time series construction for Bulgaria and EU-27
2. Dynamics indicators: chain and base absolute changes, average absolute change, average growth rate
3. Comparative analysis of the gap between Bulgaria and the EU-27
4. Descriptive statistics (mean, range, standard deviation)
5. Trend modelling: comparison of 10 regression models (linear, quadratic, cubic, exponential and others)
6. Short-term forecast with an ARIMA(1,1,0) model

## Key Findings

| Indicator | Bulgaria | EU-27 |
|---|---|---|
| Mean age in 2001 | 25.1 years | 29.0 years |
| Mean age in 2021 | 27.9 years | 31.1 years |
| Average annual increase | +0.14 years | +0.105 years |
| Average growth rate | 0.54% per year | 0.35% per year |
| Standard deviation | 0.886 | 0.623 |

- The mean age of mothers is **rising steadily** in both Bulgaria and the EU-27.
- Bulgaria remains **consistently below the EU-27 average**. The gap narrowed from 3.9 years (2001) to about 3.0 years (2010), then stabilised at 3.0–3.2 years.
- Although Bulgaria grows faster, this has not closed the gap with the EU since 2010.

## Modelling and Forecast

- **Linear trend model:** `y = 25.243 + 0.139t`, R² = 0.952, statistically significant (ANOVA F = 380.94, p < 0.001). The mean age in Bulgaria rises by about 0.139 years per year. Quadratic and cubic models reached R² = 0.993, but the linear model was chosen for easier interpretation.
- **ARIMA(1,1,0)** (selected by SPSS Expert Modeler): R² = 0.988, MAPE = 0.283%, Ljung-Box p = 0.789 (residuals are random, so the model is adequate)

**Forecast for Bulgaria:**

| Year | Forecast mean age |
|---|---|
| 2022 | 28.0 |
| 2023 | 28.2 |
| 2024 | 28.3 |

## Hypotheses

| Hypothesis | Result |
|---|---|
| H1: The mean age of mothers in Bulgaria increased over 2001–2021 | Accepted |
| H2: The mean age of mothers in the EU-27 increased over 2001–2021 | Accepted |
| H3: Bulgaria's mean age stayed below the EU-27 average throughout the period | Accepted |

## Repository Structure

```
├── README.md
├── mother_age_bg_eu27_2001_2021.csv   # Eurostat data used in the analysis
├── analysis.xlsx                      # Excel calculations and charts
├── analysis.sav                       # SPSS dataset with model outputs
└── thesis.pdf                         # Full thesis (in Bulgarian)
```

## Author

**Viktoria Vutova**: [LinkedIn](https://www.linkedin.com/in/viktoria-vutova-964294247)
