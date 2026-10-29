# Week 4: Supervised Learning — Titanic Survival Prediction

## Project overview
This project trains and compares two supervised machine-learning classifiers to predict Titanic passenger survival:
- Logistic Regression
- Decision Tree

The workflow includes dataset inspection, feature selection, preprocessing, an 80/20 stratified train-test split, model evaluation, five-fold stratified cross-validation, and a performance comparison chart.

## Dataset
Public CSV dataset:
https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

The notebook downloads the dataset directly, so a separate dataset file is not required.

## Main results

| Metric | Logistic Regression | Decision Tree |
|---|---:|---:|
| Test accuracy | 80.45% | 76.54% |
| Precision | 79.31% | 75.47% |
| Recall | 66.67% | 57.97% |
| F1-score | 72.44% | 65.57% |
| Mean 5-fold CV accuracy | 79.35% | 80.34% |

## Files
- `notebooks/titanic_supervised_learning_week4.ipynb` — runnable Jupyter/Google Colab notebook
- `reports/Week4_Supervised_Learning_Titanic_Report.docx` — detailed report
- `requirements.txt` — Python dependencies

## Run the notebook
### Option 1: Google Colab
1. Open https://colab.research.google.com/
2. Choose **File → Upload notebook**.
3. Upload `notebooks/titanic_supervised_learning_week4.ipynb`.
4. Run the cells from top to bottom.

### Option 2: Local Python
Install dependencies:
```bash
pip install -r requirements.txt
```
Then open the notebook with Jupyter Notebook or JupyterLab.

## Important methodology note
In the original experiment, missing values in `Age` and `Embarked` were filled before the train-test split. This can cause a small amount of data leakage because the imputation values use the full dataset. The report records this limitation. For a stricter experiment, create `X` from the original columns without filling missing values first and let the preprocessing pipeline fit its imputers only on the training data; the resulting metrics may change.

## Author
Chandana K B
