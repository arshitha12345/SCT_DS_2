# TITANIC — Data Cleaning & Exploratory Data Analysis (EDA)

## Project Overview
This repository contains a complete **data cleaning** and **exploratory data analysis (EDA)** workflow on the classic **Titanic** dataset (`train.csv`, `test.csv`, `gender_submission.csv`).  
The goal is to demonstrate a clean, reproducible analysis with clear visualizations and concise insights.

## Technical Skills Demonstrated
| Area | Tools & Techniques |
|---|---|
| Data Cleaning | Handling missing values (median/mode), extracting features (Deck from Cabin), type casting |
| Data Wrangling | Filtering, grouping, crosstabs, binning (age bands) |
| Visualization | Matplotlib + Seaborn (professional whitegrid theme) |
| Workflow | Reproducible analysis in a Jupyter Notebook |

## Repository Contents
| File | Description |
|---|---|
| `Titanic_EDA.ipynb` | Executable Jupyter Notebook with full cleaning + detailed EDA |
| `requirements.txt` | Minimal dependencies to run the notebook |
| `train.csv`, `test.csv`, `gender_submission.csv` | Input data files (not included here; upload to the repo root) |

## How to Run
1. **Clone** or download this repository.
2. Place the three CSV files in the **repo root**:
   - `train.csv`
   - `test.csv`
   - `gender_submission.csv`
3. (Optional) Create a virtual environment and install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Open the notebook:
   - Jupyter: `jupyter lab` or `jupyter notebook` → open `Titanic_EDA.ipynb`
   - Google Colab: Upload the notebook and the CSVs; update the file paths if needed.

## What the Notebook Does
- **Data Cleaning**
  - Fills `Age` with **median**
  - Fills `Embarked` with **mode**
  - Extracts **Deck** from `Cabin` (falls back to `Unknown` when missing)
  - Casts `Survived`, `Pclass`, `Sex`, `Embarked`, `Deck` to `category`
  - Drops non-essential ID/text columns for EDA (`PassengerId`, `Name`, `Ticket`, `Cabin`)
- **Detailed EDA**
  - Distributions: `Survived`, `Sex`, `Pclass`, `Age`, `Deck`, `Embarked`
  - Survival rate by: `Sex`, `Pclass`, `Embarked`, `Deck`
  - Age analysis with KDE overlays (Survived vs Not Survived)
  - Correlation heatmap
  - Multivariate crosstabs (e.g., `Sex` × `Pclass` vs `Survived`)
- **Insights Summary**
  - Typical findings include higher survival among **females** and **1st class**, and port/class effects.

## Notes
- Keep CSV filenames exactly as above or adjust paths in the notebook.
- This project focuses on **clean EDA** (not model building). You can extend with feature engineering or classification later.

---

**Author:** Arshitha  
**Dataset:** Titanic (Kaggle / public)  
**License:** MIT
