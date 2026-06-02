# DMBi Practicals

This repository contains practicals/notebooks and supporting code for **Data Mining for Business Intelligence**.

## Contents

- **`DMBi_Practicals.ipynb`** – Python notebook covering practicals 1–4 (data loading, visualization, preprocessing, time-series analysis, clustering, and modeling).
- **`DMBi_Practicals(5,6,7).ipynb`** – Python notebook covering practicals 5–7 (Naive Bayes classification, Neural Network regression, and Association Rule Mining).
- **Datasets (CSV/XLSX)** – `ToyotaCorolla.csv`, `SouvenirSales.csv`, `ApplianceShipments.csv`, `BostonHousing.csv`, `Universities.csv`, `WalMartStock.csv`, `accidentsFull.csv`, `Coursetopics.csv`.
- **Supporting scripts** – `prac1.R`, `prac2.R`, and `practice.py`.

## Practicals Overview

### Practicals 1–4 (`DMBi_Practicals.ipynb`)

| Practical | Topic | Dataset |
|-----------|-------|---------|
| 1 | Exploratory Data Analysis & Correlation | ToyotaCorolla |
| 2 | Time-Series Plotting & Log Transform | SouvenirSales / ApplianceShipments |
| 3 | k-NN Regression | BostonHousing |
| 4 | Hierarchical Clustering & ACF/AR Modeling | Universities / WalMartStock |

### Practicals 5–7 (`DMBi_Practicals(5,6,7).ipynb`)

| Practical | Topic | Dataset | Algorithm |
|-----------|-------|---------|-----------|
| 5 | Automobile Accident Injury Prediction | accidentsFull.csv | Naive Bayes (MultinomialNB) |
| 6 | Car Price Prediction | ToyotaCorolla.csv | Neural Network (MLPRegressor) |
| 7 | Online Statistics Course Recommendations | Coursetopics.csv | Association Rule Mining (Apriori) |

#### Practical 5 – Naive Bayes (Automobile Accidents)
- Loads `accidentsFull.csv` and creates a binary target `INJURY` (yes/no) from `MAX_SEV_IR`.
- Uses 12 categorical predictors: hour, alignment, work zone, weekday, highway type, light condition, road profile, speed limit, surface condition, traffic control, traffic way, and weather.
- Splits data **60/40** into training/validation sets and evaluates via confusion matrix and accuracy score.

#### Practical 6 – Neural Networks (Car Sales)
- Loads `ToyotaCorolla.csv` and selects 16 features (price, age, KM, fuel type, HP, automatic, doors, tax, guarantees, airco, CD player, powered windows, sport model, tow bar).
- One-hot encodes `Fuel_Type`, then scales all features and target to `[0, 1]` with `MinMaxScaler`.
- Trains an `MLPRegressor` and reports RMSE on both training and validation partitions.

#### Practical 7 – Association Rule Mining (Online Courses)
- Loads `Coursetopics.csv` (a binary transaction matrix of course topic purchases).
- Runs the **Apriori** algorithm with `min_support = 0.05` to find frequent itemsets.
- Generates association rules filtered by `lift > 1.2` and displays the top rules sorted by lift descending.

## Datasets Used

| Dataset | File | Used In |
|---------|------|---------|
| Toyota Corolla | `ToyotaCorolla.csv` | Practicals 1, 6 |
| Souvenir Sales | `SouvenirSales.csv` | Practical 2 |
| Appliance Shipments | `ApplianceShipments.csv` | Practical 2 |
| Boston Housing | `BostonHousing.csv` | Practical 3 |
| Universities | `Universities.csv` | Practical 4 |
| Walmart Stock | `WalMartStock.csv` | Practical 4 |
| Accidents Full | `accidentsFull.csv` | Practical 5 |
| Course Topics | `Coursetopics.csv` | Practical 7 |

## How to Run

### Prerequisites

- Python 3
- Jupyter Notebook

### Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels plotly nbformat mlxtend
```

> **Note:** `mlxtend` is required for the Apriori algorithm used in Practical 7.

### Launch

```bash
jupyter notebook
```

- Open **`DMBi_Practicals.ipynb`** for practicals 1–4.
- Open **`DMBi_Practicals(5,6,7).ipynb`** for practicals 5–7.

Run the cells in order.

## Notes

- All dataset files must be present in the same folder as the notebook.
- If a cell fails, verify the dataset filename and column headers match exactly.
- Practical 6 requires feature scaling — do not skip the `MinMaxScaler` step.
- Practical 7 requires the `mlxtend` library; install it with `pip install mlxtend`.


