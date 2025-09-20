# Car-Prices-Prediction---Regression-Model---RapidMiner
📈 Predict used Toyota Corolla prices using a RapidMiner Studio linear-regression workflow. Clean, reproducible pipeline ready to run and extend.

<img width="1170" height="536" alt="image" src="https://github.com/user-attachments/assets/21d8ba57-a98c-43dc-a22f-4bc57b3b1600" />

# 🚗 Toyota Corolla — Price Prediction (RapidMiner)


## ⚡ Overview

This repository contains a RapidMiner process (`project2.rmp`) that builds a **linear regression** model to predict car prices (`Price`) from the ToyotaCorolla dataset. It uses RapidMiner Studio **11.0.000** and covers the full pipeline: retrieve data → preprocess → train/test split → train model → evaluate.

> **Note:** The dataset itself is not embedded. Place it in your RapidMiner local repository to run.

---

## 🔍 Key Facts

* **Dataset path**: `//Local Repository/data/ToyotaCorolla`
* **Features used**: `Age_08_04`, `Automatic`, `CC`, `Doors`, `Fuel_Type`, `HP`, `Id`, `KM`, `Met_Color`, `Price`, `Quarterly_Tax`, `Weight`
* **Label & ID**: `Price` → label, `Id` → id
* **Categorical handling**: Dummy coding for `Fuel_Type`
* **Filtering**: First 1000 rows only
* **Split**: 60% train / 40% test
* **Random seed**: 2001 (global)
* **Model**: Linear Regression with ridge = `1.0E-8`, eliminates colinear features, α = `0.05`
* **Evaluation**: RMSE + absolute/relative/squared errors

---

## 🛠️ Pipeline Steps

1. Retrieve dataset from Local Repository
2. Preprocess: select attributes, set roles, encode `Fuel_Type`, filter rows
3. Split data (60/40)
4. Train `Linear Regression` model
5. Predict on test data & calculate residuals
6. Evaluate performance (RMSE, etc.)

---

## ▶️ How to Run

1. Install **RapidMiner Studio 11** (or compatible).
2. Add the dataset to `/Local Repository/data/ToyotaCorolla` or adjust the `Retrieve` operator.
3. Open `project2.rmp` in RapidMiner and click **Run**.
4. View results: model, metrics, predictions & residuals.

💡 Tip: For deterministic splits, enable local random seed in `Split Data`.

---

## 🚀 Next Steps & Improvements

* Try alternative models: Random Forest 🌲, Gradient Boosted Trees ⚡
* Use k-fold cross-validation instead of single split
* Add feature engineering & hyperparameter tuning 🔧
* Inspect residuals for heteroscedasticity 📊


📜 Add a LICENSE of your choice (MIT recommended) if you plan to share publicly.
