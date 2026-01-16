# ML/DL Google Colab Projects

A curated set of machine learning and data analysis notebooks designed for quick execution in **Google Colab** (or locally with Jupyter). Each notebook is self-contained, focuses on a real-world workflow, and includes data loading, modeling, evaluation, and insights.

## Contents

| Notebook | Focus | Data Source | Highlights |
| --- | --- | --- | --- |
| `AI_Model_Monitoring_for_Healthcare_Applications_Using_Logging.ipynb` | Model monitoring + logging | **Synthetic** healthcare signals | Train/test split, prediction logging, drift-aware thinking |
| `Customer_Churn_Prediction_Using_ANN.ipynb` | Customer churn (ANN) | **Kaggle** credit card churn dataset | End-to-end ANN pipeline, preprocessing, evaluation |
| `Drug_Clincial_Trial_Data_Assessing.ipynb` | Data quality assessment | **Local CSVs** (`patients.csv`, `treatments.csv`, `adverse_reactions.csv`, `treatments_cut.csv`) | Data auditing, cleaning, quality/tidiness checks |
| `Multi_Class_Classification_of_MNIST_by_ANN.ipynb` | MNIST digit classification | **Keras built-in** MNIST | Classic ANN pipeline, metrics + visualization |

## Quick Start (Colab)

Open any notebook in Colab using the built-in badge at the top of each notebook. Colab is the fastest way to run these without local setup.

## Local Setup

1. **Create a virtual environment (recommended)**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. **Install dependencies**
   ```bash
   pip install jupyter numpy pandas matplotlib seaborn scikit-learn tensorflow
   ```
3. **Launch Jupyter**
   ```bash
   jupyter notebook
   ```

> Notes
> - `tensorflow` may be heavy; use `tensorflow-cpu` if you prefer CPU-only installs.
> - Internet access is required for datasets that are downloaded at runtime (MNIST + Kaggle churn dataset).

## Dataset Notes & How to Run Each Notebook

### 1) AI Model Monitoring for Healthcare Applications
- **Dataset**: Synthetic data generated in-notebook (no external files needed).
- **Run**: Execute cells top-to-bottom; the notebook trains a classifier and logs predictions for new patient data.
- **Why it’s impressive**: Demonstrates monitoring mindset, not just model training.

### 2) Customer Churn Prediction Using ANN
- **Dataset**: Kaggle credit-card customer churn dataset.
- **Run**: The notebook includes a data download step and loads `Churn_Modelling.csv`.
- **Notes**: Requires internet access for the download. If running locally, ensure the dataset exists at the same path used in the notebook or update the path accordingly.

### 3) Drug Clinical Trial Data Assessing
- **Dataset**: Local CSV files referenced in the notebook:
  - `patients.csv`
  - `treatments.csv`
  - `adverse_reactions.csv`
  - `treatments_cut.csv`
- **Run**: Place the CSVs in the same directory as the notebook or update the file paths inside the notebook.
- **Why it’s impressive**: Focused on data quality and tidiness — critical skills for any data role.

### 4) Multi-Class Classification of MNIST by ANN
- **Dataset**: Keras built-in MNIST dataset.
- **Run**: The dataset is automatically downloaded when you run the notebook.
- **Why it’s impressive**: Classic vision benchmark, clean ANN pipeline, and clearly interpretable results.

## Documentation & Code Quality Commitments

- **Clear assumptions**: Each notebook specifies its data source and setup requirements.
- **Reproducible runs**: Dependencies and dataset expectations are documented here.
- **Professional structure**: Each notebook follows a structured flow (load → explore → preprocess → train → evaluate → explain).

## Suggested Next Improvements (Optional)

If you want to go further, consider:
- Adding `requirements.txt` to freeze dependencies.
- Exporting cleaned datasets or trained models as artifacts.
- Adding unit tests for preprocessing functions (if you refactor them into modules).

---

If you want any notebook refactored into a production-ready Python module or an end-to-end ML pipeline, just ask!
