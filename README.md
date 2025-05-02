# NEW PROJECT: https://github.com/AliceTernois/c242_project.git

# Colon Cancer Drug Response Prediction
**`UC Berkeley C242 Machine Learning Final Project`**

## Dataset

This [Colon Cancer Multitargeted Drug Discovery Dataset](https://www.kaggle.com/datasets/programmer3/colon-cancer-multitargeted-drug-discovery-dataset) integrates genomic, transcriptomic, and proteomic data from 7,643 patients and focuses on multitargeted drug discovery in colon cancer.

Key features:
- Gene expression data: Expression levels of key genes linked to colon cancer
- Protein interaction scores: Quantitative interaction scores from protein networks
- Pathway alterations: Categorical values indicating pathway dysregulation
- Drug response: Measures of drug efficacy (target variable)

## Project Goal 
Use gene expression, protein interaction scores, and pathway alterations as input features to predict drug response as an output.

## Machine Learning Methods 
TBD



## Code Structure Overview
The project is organized into three main components:

### 1. Data Processing: data_processor.ipynb
This notebook processes the raw dataset (raw_colon_cancer_data.csv):

Preprocessing: Normalizes, encodes, and splits the data into training and testing sets.

Output: Saves the processed data (X_train, X_test, y_train, y_test) in a pickle file (data_splits.pkl).

### 2. Model Training: alice_models.ipynb and rianna_models.ipynb
These notebooks train models using the preprocessed data:

Data Loading: Loads data_splits.pkl with:
    with open("data_splits.pkl", "rb") as f:
        X_train, X_test, y_train, y_test = pickle.load(f)
Model Training & Evaluation: Trains and evaluates models on X_train, y_train and tests on X_test, y_test.

### Workflow:
data_processor.ipynb: Processes and splits data, saves to data_splits.pkl.

alice_models.ipynb and rianna_models.ipynb: Train and evaluate models using the preprocessed data.
