# COMP333_Group_O
COMP 333 Winter 2026 Project Group O

# Course: **COMP 333 — Final Project Phase 1**
**Group:** O

**Names:**
- Carson Johnston - **Student ID:** 40312846
- Charlotte Lauzon - **Student ID:** 40285642
- Ava Samimi - **Student ID:** 40048117

---

# Project Overview

This project predicts the selling price of used vehicles using machine learning. We perform exploratory data analysis (EDA) on the US Used Cars dataset to understand distributions and relationships, then build a baseline linear regression model. The goal is to establish a reproducible pipeline for data cleaning, visualization, and price prediction that can be extended with more advanced models.

---

# Notebook Structure

| Part | Description |
|------|-------------|
| **Part 1–2** | Data loading, cleaning pipeline, and preprocessing |
| **Part 3** | Exploratory Data Analysis — summary statistics, univariate/bivariate visualizations, correlation analysis |
| **Part 4** | Baseline model — linear regression for price prediction, train/val/test split, evaluation metrics (MAE, RMSE, R², MAPE, MedAE), residual analysis |

---

# Dataset

We use the **US Used Cars** public dataset from Kaggle.
The full dataset (9.98GB) is publicly available on Kaggle:
https://www.kaggle.com/datasets/ananaymital/us-used-cars-dataset
Due to size constraints, it is not included in the submission. The full dataset needs to be downloaded and put in the project's root directory. 
A trimmed ~1GB dataset is created by reading the full csv file by chunks, and sampling each chunk.

**Included in this repo:** `clean_cars.csv` — the cleaned subset used for analysis and modelling. The notebook loads this file **first**, so you can reproduce the pipeline **without** downloading the full Kaggle CSV.

To rebuild from raw data (optional): download the full dataset, place `used_cars_data.csv` in the project root, then run the trimming/cleaning steps in the notebook from phase 1.
With `clean_cars.csv`, you can run the notebook from phase 2 without needing the full dataset

# How to Reproduce

**Default (recommended):** Clone or copy this repository and ensure `clean_cars.csv` sits next to the notebook. Run the notebook from the project root; STEP 2 loads the cleaned data automatically.

**From full raw data (optional):**

1. Download the dataset manually from the Kaggle link above.
2. Extract the CSV file.
3. Place the CSV file in the project’s root directory (same folder as the notebook).

**Expected filename for raw data:** `used_cars_data.csv` in the project root. The notebook also checks `data/raw/used_cars_data.csv`.

The notebook automatically checks:
- **`clean_cars.csv`** in the project root (preferred — matches this repo).
- If the full dataset (`used_cars_data.csv`) is present, it can be used to create a trimmed file by reading the full csv in chunks and sampling those chunks.
- If the trim dataset is already in the project's root directory; if not, a trimmed ~1.2 GB dataset is created by reading the full csv file in chunks, and sampling those chunks.

All analysis, cleaning, visualization and modelling steps are fully reproducible.

---

# How to Run

1. **Run from the project root** — Open the notebook from the project directory so `os.getcwd()` resolves correctly for data loading.
2. **Run All** — Use "Run All" (or run cells in order from the top) to execute the full pipeline.
3. **If you see `ModuleNotFoundError: No module named 'sklearn'`** — Install scikit-learn (`pip install scikit-learn`), then restart the Jupyter kernel (Kernel → Restart) and run the notebook again.
4. Please install all dependencies and environment using pip or conda

---

# Results Summary

The baseline linear regression achieves **R² ≈ 73%** on train, validation, and test sets, explaining about 73% of price variation. **MAE ≈ $4,200** indicates average prediction error in dollars. The model performs best for mid-range vehicles ($30k–$40k) and tends to underestimate luxury prices.

---

# Dependencies

This Project requires Python and the following libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn

Install with: 
pip install pandas numpy matplotlib seaborn scipy scikit-learn

---

# Environment Setup

This project can be run using either pip or Conda.

### Using pip
Create a virtual environment and install dependencies:

pip install -r requirements.txt

### Using Conda
Create the Conda environment:

conda env create -f environment.yml
conda activate COMP333_PROJECT_GROUP_O