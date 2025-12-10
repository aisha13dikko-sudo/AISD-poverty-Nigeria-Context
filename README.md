# AISD Poverty Prediction – Nigeria Context (UCL MSc AI for Sustainable Development)

This repository contains the code used to generate the results presented in my coursework poster:

**“Poverty Prediction in Nigeria Using Geospatial and Household Indicators”**

## Notebooks

- **01_Baseline_Replication.ipynb**
Reproduces the approach from Jean et al. (2016) using proxy satellite-based features.

- **Nigeria_tabular_model.ipynb**
Implements the adapted XGBoost model using LSMS 2018 household tabular features.
Includes:
- data preparation
- log-transform of consumption
- train/validation/test split
- model training
- R² and RMSE evaluation
- predicted vs actual plot

- **01_env_check.ipynb**
Simple environment test (not required to run models).


## Data Availability

The LSMS 2018 dataset is **not included** in this repository due to licensing restrictions.
Notebooks assume the cleaned dataset is available locally:

```python
cons = pd.read_csv("totcons_final.csv")
hh   = pd.read_csv("nga_householdgeovars_y4.csv")
df = cons.merge(hh, on="hhid", how="inner")
```
## ⚙️ Environment


The analysis uses the following Python libraries:

pandas

numpy

scikit-learn

xgboost

matplotlib

Tested in Google Colab 

📊 Poster Link

Outputs from these notebooks (figures, performance metrics, and comparison tables) appear in the accompanying poster for:

Coursework 2 — AI for Sustainable Development, UCL

The poster summarises:

The adaptation of the Jean et al. (2016) methodology

The improved performance of LSMS + XGBoost

SDG alignment

Ethical reflections



