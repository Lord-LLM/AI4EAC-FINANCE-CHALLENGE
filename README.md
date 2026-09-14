# AI4EAC Finance Challenge

Machine learning solution for the [AI4EAC Finance Practice Challenge on Zindi](https://zindi.world/competitions/the-ai4eac-finance-practice-challenge).

## Project Overview

The goal of the challenge is to predict the likelihood that a customer will default on a loan. The model uses customer, loan, lender, repayment, date, and economic indicator data to classify each loan as either:

- `1`: the customer defaulted
- `0`: the customer did not default

The competition uses **F1 score** for evaluation. This project explores feature engineering, preprocessing, and ensemble machine learning models for this binary classification problem.

## Repository Contents

| File | Description |
| --- | --- |
| `ensemble.ipynb` | Main notebook containing data preparation, feature engineering, model training, evaluation, and prediction generation |
| `Train.csv` | Training data with the `target` label |
| `Test.csv` | Unlabelled data used to generate competition predictions |
| `economic_indicators.csv` | Economic indicator data used as additional model features |
| `VariableDefinitions.txt` | Descriptions of the dataset variables |
| `pyproject.toml` | Python project metadata and dependency definitions |

## Getting Started

### Requirements

- Python 3.11 or newer
- Jupyter Notebook or JupyterLab
- The packages listed in `pyproject.toml`

### Installation

From the project directory, create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install the project dependencies:

```bash
pip install -e .
```

Start Jupyter:

```bash
jupyter notebook
```

Open `ensemble.ipynb` and run the cells from top to bottom.

## Workflow

The notebook follows this general process:

1. Load the training, test, and economic indicator data.
2. Inspect and clean the input features.
3. Create useful features from loan amounts, repayment information, categories, and dates.
4. Train and compare classification models.
5. Evaluate predictions using the F1 score.
6. Generate predictions for the test data.
7. Save a submission file containing `ID` and `Target` columns.

## Submission Format

The final submission should contain exactly two columns:

```text
ID,Target
ID_C7AV4GEJP9,1
ID_AFVZYGLXXY,0
```

The `Target` column contains the predicted class, where `1` represents a predicted loan default.

## Reproducibility

Run the notebook in order from a clean environment. Keep the original CSV files in the project root, and set a fixed random seed when training models so that results can be reproduced.

## Competition Reference

Read the full challenge description, rules, and submission requirements on [Zindi](https://zindi.world/competitions/the-ai4eac-finance-practice-challenge).
