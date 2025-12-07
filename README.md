# “Will they pay?” - predicting loan bayback
### Kaur Vadi, Tregert Värv, Group - B8


## 1. Motivation and Goal

In this project, we study a synthetic loan dataset provided by Kaggle (Playground Series S5E11) that includes borrower demographics, financial information, loan attributes and credit history. The main aim is to predict whether a borrower will successfully repay their loan. When a borrower fails to fully repay their loan, the loan is considered to have defaulted.

To achieve this, we evaluate several machine learning models and compare their ability to predict loan repayment outcomes. Our goal is to identify which approach performs best and what factors contribute most to repayment likelihood.

---

## 2. Dataset

We use the dataset from the Kaggle Playground Series S5E11 competition, originally based on the “Loan Prediction Dataset – 2025”.

- The dataset contains around 594 000 rows and 13 features.
- It includes borrower demographics, loan details and financial indicators.  
- The target variable is loan_paid_back (1 = repaid, 0 = defaulted).  
- The dataset contains no missing values and is already cleaned.

**Sources:**
- https://www.kaggle.com/competitions/playground-series-s5e11  
- https://www.kaggle.com/datasets/nabihazahid/loan-prediction-dataset-2025  

---

## 3. Repository Structure
- **main.ipynb**  
  The main modelling notebook. Performs data preprocessing (encoding and scaling), splits the dataset, trains all machine learning models (Logistic Regression, Random Forest, kNN, SVM, Gradient Boosting, XGBoost), evaluates them using AUC/accuracy/precision/recall.
  
- **analyzing_data.ipynb**     
  Exploratory data analysis notebook. Computes default rates for different demographic and financial groups and produces all visualisations used in the poster.
  
- **train.csv**  
  The main dataset downloaded from Kaggle (Playground Series S5E11).

- **test.csv**  
  Optional competition test dataset provided by Kaggle.

- **sample_submission.csv**  
  Template file showing the expected Kaggle submission format.

- **Group_B8_report.pdf**  
  The written report submitted as part of the project.

- **README.md**  
  Main documentation file explaining the project, dataset, repository structure, and reproducibility instructions.

  
## 4. How to replicate the analysis

It is possible to fully reproduce our analysis because:

- All code used in the project is contained inside two Jupyter notebooks (analyzing_data.ipynb and main.ipynb).

- The analysis begins with analyzing_data.ipynb, which loads the dataset and provides an overview of the data through exploratory visualisations (default-rate comparisons, distributions and category-based analysis).

- After understanding the data, running main.ipynb reproduces the entire modelling workflow, including preprocessing, training all machine learning models, generating evaluation metrics, ROC curves and feature-importance plots.

- The dataset is publicly available, so anyone can download the same train.csv file from Kaggle and place it in the project directory.

- Fixed random_state values ensure full reproducibility, meaning the models will produce the same metrics and figures every time the notebooks are executed.

- No external setup or additional scripts are required, so simply opening both notebooks in Jupyter and running the code cells in order will recreate our complete analysis from start to finish.
