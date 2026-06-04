# DMBi Practicals

This repository contains practicals/notebooks and supporting code for **Data Mining for Business Intelligence**.

## Practicals overview (from the journal)

### Practical 1 — Toyota Corolla (EDA + correlation + dummy encoding)
- Explore correlations using a matrix/pair plot.
- Convert categorical variables into binary dummy variables using the **N-1 rule** (dummy variable trap avoidance).

### Practical 2 — Appliance Shipments & Souvenir Sales (time series plots + log transform + seasonality)
- Create time plots and zoom to inspect quarterly patterns.
- Re-create the same plots using an interactive tool (requires parsing quarter info as a date/quarter period).
- For Souvenir Sales: compare raw vs log scale to reveal an approximately linear trend.

### Practical 3 — Boston Housing (k-NN regression)
- Identify categorical predictors and handle them via dummy/binary encoding if needed.
- Run k-NN regression with **k = 1..5** (after normalization) using a **training/validation split**.
- Select the best k using validation error (RMSE).

### Practical 4 — Universities (hierarchical clustering) & Wal-Mart (time-series / AR)
- Hierarchical clustering with **complete linkage** and **Euclidean distance** on normalized continuous variables.
- Choose a reasonable number of clusters from the dendrogram.
- Characterize clusters; relate clustering results to categorical variables.
- For Wal-Mart: use time-series diagnostics (ACF + AR(1)) to assess random-walk behavior.

### Practical 5 — Automobile Accidents (Naive Bayes)
- Build a binary target `INJURY` from `MAX_SEV_IR`.
- Train Naive Bayes on categorical predictors.
- Evaluate using classification matrix and compute validation error.

### Practical 6 — Car Price Prediction (Neural Networks)
- Predict car `Price` using selected predictors.
- Convert categorical values to dummies (one-hot) and scale to **[0, 1]**.
- Train an `MLPRegressor` and report RMS error on training/validation.

### Practical 7 — Online Statistics Courses (Association Rules / Apriori)
- Use Apriori with `min_support = 0.05`.
- Generate association rules using **lift**; filter by `lift > 1.2`.

### Practical 8 — University Rankings (clustering + imputing missing values)
- Remove records with missing measurements before clustering.
- Run hierarchical clustering on normalized continuous variables.
- Use cluster assignments/statistics to impute missing values (assign partial records to the closest cluster).

### Practical 9 — Wal-Mart Stock (random walk test via differencing + AR(1))
- Create a time plot of the **differenced** series.
- Check autocorrelations / ACF and fit an **AR(1)** model.
- Decide whether the stock behaves like a random walk.

### Practical 10 — Souvenir Sales Forecasting (trend + log + validation split)
- Create a time plot of the monthly series.
- Transform to log scale to obtain a more linear relationship.
- Partition the last 12 months as validation (to mimic forecasting for the next year).

## Datasets used

| Dataset | File | Used in |
|---|---|---|
| Toyota Corolla | `ToyotaCorolla.csv` | 1, 6 |
| Appliance Shipments | `ApplianceShipments.csv` | 2 |
| Souvenir Sales | `SouvenirSales.csv` | 2, 10 |
| Boston Housing | `BostonHousing.csv` | 3 |
| Universities | `Universities.csv` | 4, 8 |
| Wal-Mart Stock | `WalMartStock.csv` | 4, 9 |
| Accidents Full | `accidentsFull.csv` | 5 |
| Course Topics | `Coursetopics.csv` | 7 |

## How to run

### Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels plotly nbformat mlxtend
```

### Jupyter notebooks

```bash
jupyter notebook
```

## Notes

- Dataset files must be present in the same folder structure expected by each notebook/script (for `Data-mining-practicals-/Practical*.py`, keep datasets alongside that folder or update file paths).
- Practical 6 requires feature scaling.
- Practical 7 requires `mlxtend`.

