# Gaussian Process Regression for Ocean Temperature Anomaly Detection

This project explores the detection of climate anomalies using Gaussian Process Regression (GPR) on real satellite-derived oceanographic data. The goal is to model the expected behavior of a key variable (tdrop, representing the temperature drop across the ocean's cool skin layer) and identify regions or times where observations deviate significantly from this model.

---

## Project Overview

- **Data**: NASA satellite reanalysis data from the MERRA-2 dataset, available at Source: [Kaggle – OCEAN DATA / CLIMATE CHANGE / NASA](https://www.kaggle.com/datasets/brsdincer/ocean-data-climate-change-nasa)
- **Model**: Gaussian Process Regression (scikit-learn)
- **Target**: `tdrop` (temperature drop across cool layer)
- **Features**: 
  - `tbar` – average temperature of the interface layer  
  - `tskinice` – skin temperature over sea ice  
  - `rainocn` – ocean rainfall  
  - `delts` – surface skin temperature change  
- **Training**: August 1st, 2018  
- **Testing & Anomaly Detection**: August 1st, 2021

---

## Repository Structure

```bash
├── train_model.ipynb           # Notebook to train GPR model
├── analyze_results.ipynb       # Notebook to evaluate predictions and detect anomalies
├── gpr_model.pkl               # Saved trained GPR model
├── gpr_scaler.pkl              # Saved feature scaler
└── README.md                   # You are here!
