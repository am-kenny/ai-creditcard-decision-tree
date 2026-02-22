# Credit Card Fraud Detection with Decision Tree

This repository contains a Jupyter notebook that builds and evaluates a **Decision Tree classifier** for detecting fraudulent credit card transactions.

## Project Overview

The notebook performs an end-to-end baseline workflow:

1. Loads transaction data from `data/creditcard.csv`
2. Splits features/target and creates train/test sets
3. Trains a `DecisionTreeClassifier`
4. Evaluates model performance
5. Visualizes:
   - Decision tree structure
   - Class frequency
   - Confusion matrix
   - Feature importance
   - ROC curve

Notebook path:

```text
code/Decision Tree - [fraudulent transactions prediction].ipynb
```

## Repository Structure

```text
.
├── code/
│   └── Decision Tree - [fraudulent transactions prediction].ipynb
├── data/
│   └── creditcard.csv
├── requirements.txt
└── README.md
```

> Note: plots are saved by the notebook into `res/` (created by you before execution).

## Prerequisites

- Python 3.9+ (recommended)
- `pip`
- Git LFS (required for the dataset file)
- Jupyter (already included in `requirements.txt`)

## Setup

Clone and enter the repository:

```bash
git clone https://github.com/am-kenny/ai-creditcard-decision-tree.git
cd ai-creditcard-decision-tree
```

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Download Git LFS data objects:

```bash
git lfs install
git lfs pull
```

If `data/creditcard.csv` starts with:

```text
version https://git-lfs.github.com/spec/v1
```

then LFS objects are not downloaded yet.

## Run the Notebook

Create a directory for generated figures:

```bash
mkdir -p res
```

Start Jupyter and open the notebook:

```bash
jupyter notebook "code/Decision Tree - [fraudulent transactions prediction].ipynb"
```

Run all cells from top to bottom.

## Model Configuration Used

The notebook trains:

- `DecisionTreeClassifier`
- `criterion='entropy'`
- `max_depth=6`
- `min_samples_leaf=5`
- `random_state=100`
- Train/test split: `test_size=0.3`

## Outputs

When all visualization cells are executed, the following files are written:

- `res/fraud_frequency.png`
- `res/confusion_matrix.png`
- `res/feature_importance.png`
- `res/roc_curve.png`

The notebook also prints baseline metrics, including an accuracy value from the test split.

## Important Notes

- The dataset is highly imbalanced (fraud cases are rare), so accuracy alone can be misleading.
- For a production-ready workflow, add precision/recall/F1 analysis, stratified validation, and threshold tuning.
- The project currently focuses on exploratory notebook-based modeling (no packaged training script yet).

## Team Members

- Andrii Prykhodko 51773650
- Artur Okseniuk 20258565
- Serhii Shymko 52264213
- Maksym Kashevarov 37544938
- Mark Shafarenko 83967814
- Karim Saliev 84082025
- Tae Yoon Lee 38321127
