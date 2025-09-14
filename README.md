# Healthcare-Cost-W-Lin-and-Rand-Forest-Quantile-Regression
# Predicting Healthcare Costs: Linear Regression ➜ Random Forest Quantile Regression


A short, hands-on project at the intersection of **healthcare** and **finance**.  
I built a **Linear Regression** baseline and extend it with **Random Forest Quantile Regression** to produce **uncertainty-aware predictions** (10th/50th/90th percentiles) for **medical charges**.  
Includes a lightweight **data engineering pipeline**: Kaggle ingestion, validation, feature engineering, and Parquet storage.

---

## What’s inside
- **Data Engineering**:
  - Ingest data via **Kaggle API**
  - Schema & data validation (types, ranges, categories)
  - Feature engineering (age groups, BMI categories, one-hot encoding)
  - Persist **processed data** to **Parquet**
- **Modeling**
  - **Part 1:** Linear Regression baseline (MSE/RMSE/R², coefficient analysis)
  - **Part 2:** Random Forest **Quantile** Regression (10th, 50th, 90th), with **interactive Plotly** intervals
- **Visualization**
  - Actual vs. Predicted with shaded **uncertainty band**
- **Reproducibility**
  - Colab-ready cells

---

##  Dataset
**Medical Cost Personal Dataset** (Kaggle): `mirichoi0218/insurance`  
We access it via **Kaggle API** inside Colab. The repository does **not** commit raw data.

---

##  Getting started (Colab)
1. Open the notebook via the badge above (replace `ashabari/Healthcare-Cost-W-Lin-and-Rand-Forest-Quantile-Regression` in the link).
2. Run the **Kaggle API setup** cell (upload your `kaggle.json`).
3. Run the **Data Engineering** cells (ingest ➜ validate ➜ transform ➜ save to Parquet).
4. Run **Part 1** (Linear Regression) and **Part 2** (Random Forest Quantile Regression).
5. Explore the **Plotly** interactive chart for prediction intervals.

>  Add `kaggle.json` to your Colab runtime only; it’s listed in `.gitignore` so it won’t be committed.

---


## Environment
- Python 3.9+
- See `requirements.txt` for packages:
  - pandas, numpy, scikit-learn, matplotlib, seaborn, plotly, pyarrow/fastparquet, kaggle

---

## Results
- Linear Regression: RMSE ≈ …, R² ≈ …
- Quantile RF (Median): RMSE ≈ …, R² ≈ …
- Added value: **uncertainty intervals** (10th–90th) for risk-aware decisions in healthcare finance.


---

## License
This project is licensed under the **MIT License** (see `LICENSE`).


