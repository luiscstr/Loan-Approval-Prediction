## 1. PROBLEM STATEMENT 
A financial company wants to automate the loan eligibility process (real time) based on customer detail provided while filling online application form. These details are Gender, Marital Status, Education, Number of Dependents, Income, Loan Amount, Credit History and others. To automate this process, the company has provided a dataset which contains historical data of  customers whose loan was approved and customers whose loan was rejected.

## 2. SUMMARY OF THE PROJECT

Exploratory Data Analysis, including relationships between variables and between the variables and the target variable (loan approval).

Data transformation and imputation of missing values.

Development of six baseline binary classifiers (linear regressor classifier, support vector machine, K Nearst Neighbort, decision tree, random forsest and XGBoost) to predict if the customer loan will be approved. Scoring method used is accuracy*.
To improve the model, the following techniques/methods are used:
- Hyperparameter tuning (Gridsearch and Randomized Search)
- Feature Engineering: created four variables by combined some of the dataset variables.
- Feature selection: univariate feature selection (Slect K Best), model based feature selection, Recursive Feature Selection (RF and Exhaustive Feature Selection (EFS)
- Sampling methods: Random Under Sampling, Tomek Links, Random Over Sampling, SMOTE, SMOTE Tomek.

*This is a practice problem from Analytics Vidhya and accuracy is the score require to evaluate the test data set. 

## 3. DATA
Data is from Analytics Vidhya practice problem. Can be downloaded [here](https://datahack.analyticsvidhya.com/contest/practice-problem-loan-prediction-iii/download/train-file).

## 4. FOLDER STRUCTURE
- Data
  -  \raw: contains the original data set.
  -  \processed: contains cleaned and preprocessed files
- src: contains the notebooks
- results
    - results: pickle file that contains a pandas dataframe where the different models are stored. The dataframe contains the following fields
        - Algorithm: algorithm used for the model.
        - Model: saved model.
        - Features: indicates which features were used to build the model
        - Best_Score_train: accuracy of the training set.
        - Best_Score_test: accuracy of the test set
        - Case, Case_Descript: describe which techniques were used to build de model. For example, Gridsearch, Feature selection, sampling methods...
    - Features_Rank: pickle file that indicates if the feature has been selected by the different feature selection methods used. 
 
## 5. NOTEBOOK STRUCTURE
The repository contains a total of six (6) notebooks:
- *1. Data description and initial intuitions*: structure and characteristics of the data set (rows, columns, missing values...), field description and initial suposition/guesses prior to the analysis
- *2. EDA*: exploratory data analysis, subdivided in categorical variable and numerical variable.
- *3. Data Tratment*: application of One Hot Encoder and scaling.
- *4. Model*: train and test a logistic regression classifier, random forst classifier and a neural network. Includes hyper farameter tunning (Gridsearch) and sampling techniques.
- *5. Conclussuions: summary of the analysis and findings.
- *FUll:five previous notebooks consolidated.
