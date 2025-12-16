# CIE532Project
Flood risk assessment 
# South Platte Flood Risk Model 🏞️

**Conditional flood probability analysis for USGS gage 06711565 (Englewood, CO)**  
*Graduate project - CIE 532 | Test AUC: 0.995 | 99th percentile threshold: 690 cfs*

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📊 Key Findings

- **Antecedent discharge dominates** flood prediction (odds ratio: **515**)
- **100% of floods** captured by flows >75th percentile previous day
- Local rainfall added minimal skill in regulated urban reach
- **Test AUC: 0.995** | Brier score: 0.019

**Figure 1** shows conditional probability curves - perfect for operational use!

---


---

## 🛠️ How It Works

1. **Data**: USGS 06711565 discharge + GHCND:US1COAR0214 precip (2009-2025)
2. **Flood definition**: ≥99th percentile discharge (690 cfs)
3. **Predictors**: Antecedent discharge, 1/2/3-day rain, season, interaction
4. **Model**: Logistic regression (`class_weight='balanced'`)
5. **Split**: 2009-2018 train | 2019-2025 test

**Generated outputs:**
- Figure 1: Conditional probability curves
- Figure 2: ROC curve (AUC 0.995)
- Figure 3: Reliability diagram
- Coefficients table

---

## 📝 Academic Paper

**Full analysis for "Conditional flood risk assessment using daily rainfall and river discharge"**

- **Introduction**: South Platte flood history + conditional modeling need
- **Methods**: Logistic regression w/ interaction term
- **Results**: Antecedent discharge explains ~95% of predictive power
- **Discussion**: Implications for regulated urban rivers

**[View paper sections in comments of `flood_model.py`]** 

---

## 🔗 Data Sources

- **USGS 06711565**: [waterdata.usgs.gov](https://waterdata.usgs.gov/monitoring-location/06711565/)
- **GHCND:US1COAR0214**: [NOAA NCEI](https://www.ncei.noaa.gov/access/search/data-search/global-hourly)

---

## 📊 Figures Preview

![Conditional Flood Probability](figures/flood_model_figures.png)

---

## 👨‍🎓 Author

**Daniel Galdamez**  
CIE 532 – Final Project  
[LinkedIn](https://linkedin.com/in/yourprofile) | [GitHub](https://github.com/yourusername)

---

*Built with ❤️ for flood risk analysis in urban rivers*


