# COMP333_Group_O
COMP 333 Winter 2026 Project Group O

# Course: **COMP 333 — Final Project Phase 1**
**Group:** O

**Names:**
- Carson Johnston - **Student ID:** 40312846
- Charlotte Lauzon - **Student ID:** 40285642
- Ava Samimi - **Student ID:** 40048117

# Dataset

We use the **US Used Cars** public dataset from Kaggle.
The full dataset (9.98GB) is publicly available on Kaggle:
https://www.kaggle.com/datasets/ananaymital/us-used-cars-dataset
Due to size constraints, it is not included in submission.
If the full dataset is downloaded and placed in the project's root directory, the notebook will automatically use it.
Otherwise, it will run on the included 200k rows sample.

# How to Reproduce

1. Download the dataset manually from the Kaggle link above.
2. Extract the CSV file.
3. Place the CSV file in the project’s root directory (same folder as the notebook).

The notebook automatically checks:
- If the full dataset (`used_cars_data.csv`) is present, it loads the full dataset.
- Otherwise, it loads the included `sample_used_cars_data.csv` file for reproducibility.

All analysis, cleaning, visualization and modeling steps are fully reproducible using either the full dataset or the sample dataset.

---

# Dependencies

This Project requires Python and the following libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scipy

Install with: 
pip instant pandas numpy matplotlib seaborn scipy

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