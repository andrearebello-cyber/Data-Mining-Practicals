# DMBi Practicals

This repository contains practicals/notebooks and supporting code for **Data Mining for Business Intelligence**.

## Contents

- **`DMBi_Practicals.ipynb`** – Python notebook with multiple practical tasks (data loading, visualization, preprocessing, time-series analysis, clustering, and modeling).
- **Datasets (CSV/XLSX)** – e.g. `ToyotaCorolla.csv`, `SouvenirSales.csv`, `ApplianceShipments.csv`, `BostonHousing.csv`, `Universities.csv`, `WalMartStock.csv`.
- **Supporting scripts** – `prac1.R`, `prac2.R`, and `practice.py`.

## Datasets Used (examples)

- **ToyotaCorolla** (`ToyotaCorolla.csv`) – exploratory data analysis and correlation.
- **SouvenirSales** (`SouvenirSales.csv`) – time-series plotting and log transform.
- **ApplianceShipments** (`ApplianceShipments.csv`) – quarterly time plotting (including interactive Plotly).
- **BostonHousing** (`BostonHousing.csv`) – k-NN regression on MEDV.
- **Universities** (`Universities.csv`) – hierarchical clustering + dendrogram.
- **WalMartStock** (`WalMartStock.csv`) – differenced series, ACF, AR(1) modeling.

## How to Run

### Prerequisites

- Python 3
- Jupyter Notebook

### Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels plotly nbformat
```

### Launch

```bash
jupyter notebook
```

Open **`DMBi_Practicals.ipynb`** and run the cells.

## Notes

- Some notebook sections assume specific column names and/or dataset files being present in the same folder.
- If a cell fails, verify the dataset filename and column headers.

