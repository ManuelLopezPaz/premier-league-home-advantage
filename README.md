# Premier League Home Advantage Analysis (2000–2025)

**ManuelLopezPaz**

---

## Questions

1. Which in-game statistics best predict match outcomes in the Premier League?
2. Did home advantage decline during COVID-19, when matches were played without fans?

---

## Main Findings

- Shots on target is the strongest predictor of goal difference — home (β = +0.25) and away (β = −0.27)
- The model explains 30.8% of variance in goal difference (R² = 0.308)
- Home win rate fell from 46.2% to 39.6% during COVID (p = 0.005)
- Average home goals dropped from 1.543 to 1.390 (p = 0.016)
- Cohen's d = 0.13 — the effect is real but small
- The COVID dummy is not significant in the OLS model (p = 0.069)

---

## Data

- Source: football-data.co.uk
- 9,380 Premier League matches across 25 seasons (2000/01 to 2024/25)
- Variables: results, shots, corners, fouls, cards

---

## Files
```
01_data_cleaning.ipynb    data loading, quality checks, and feature engineering
02_analysis.ipynb         EDA, OLS regression, and COVID analysis
epl_final.csv             raw dataset
epl_cleaned.csv           cleaned dataset
figures/                  all charts
```

---

## Limitations

- No possession or xG data — shots on target used as proxy
- GoalDiff is discrete — OLS is an approximation
- COVID flag is date-based (2020-06-13 to 2021-05-23), 472 matches

---

## Tools

Python · pandas · numpy · matplotlib · seaborn · statsmodels · scipy