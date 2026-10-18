# CO₂ Emission Prediction for Automotive Policy & Design

Predicting vehicle tailpipe CO₂ emissions (g/km) from engine, fuel and consumption specifications, and identifying which design and policy levers matter most for emission reduction.

## Overview

A regression project framed as an automotive data-analyst task: help a policy body understand what drives vehicle CO₂ emissions and which levers (efficiency, engine size, fleet composition, fuel type) have the greatest impact. The goal is an accurate regression model plus data-backed recommendations.

## Dataset

- **File:** `CO2_Emissions.csv` — 7,385 vehicles, 12 columns, no missing values
- **Target:** `CO2 Emissions(g/km)`

| Group | Columns |
|---|---|
| Vehicle identity | Make, Model, Vehicle Class |
| Engine | Engine Size (L), Cylinders, Transmission |
| Fuel | Fuel Type (X regular, Z premium, D diesel, E ethanol E85, N natural gas) |
| Consumption | City, Highway, Combined (L/100 km) and Combined (mpg) |

Column definitions are in `Dataset_Description.pdf`.

## Approach

1. **Data inspection** – shape, dtypes, missing values, duplicates, target distribution.
2. **Outlier analysis** – decide whether extremes (high-performance / commercial vehicles) are errors or genuine cases.
3. **Multicollinearity check** – the consumption columns carry nearly the same signal (and mpg is the inverse of L/100 km); diagnose with VIF and drop redundant features.
4. **Feature engineering** – encode categorical variables suited to the model family, scale numeric features where needed, and wrap everything in a single pipeline to avoid data leakage.
5. **Modelling** – train/test split, cross-validation, hyperparameter tuning.
6. **Evaluation** – complementary metrics (MAE, RMSE, R²).
7. **Residual analysis** – inspect the largest errors by vehicle class, fuel type and engine size.
8. **Recommendations** – translate feature importance into policy and design suggestions.

## Project Structure

```
├── co2emmisions.ipynb               # Analysis and modelling notebook
├── CO2_Emissions.csv                # Dataset
├── Dataset_Description.pdf          # Column definitions
└── CO2_Emission_Approach_Document.docx   # Problem brief and approach guidelines
```

## Tech Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · Jupyter Notebook

## Getting Started

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook co2emmisions.ipynb
```

## Results

> _To be completed once modelling is finished._

| Metric | Value |
|---|---|
| MAE | _TBD_ |
| RMSE | _TBD_ |
| R² | _TBD_ |

**Key findings:** _TBD (top emission drivers, fuel-type comparison, worst-predicted vehicles)._

**Recommendations:** _TBD._

## Author

**Khaja Siddique Ahmed** — [LinkedIn](https://linkedin.com/in/khaja-ahmed-352b21259) · khajaahmed936@gmail.com
