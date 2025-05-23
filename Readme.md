# Problem Statement
- Heart disease describes a range of conditions that affect your heart. Diseases under the heart disease umbrella include blood vessel diseases, such as coronary artery disease, heart rhythm problems (arrhythmia), and heart defects you’re born with (congenital heart defects), among others. Prediction of cardiovascular disease is regarded as one of the most important subjects in the section of clinical data science. The amount of data in the healthcare industry is huge.

- Using machine learning algorithms for heart disease prediction improves accuracy of prediction by exploiting complex interactions between various existing risk factors. The aim of this project is to compare different machine learning models for early prediction of heart diseases.

## Research Paper on Comparative Analysis of ML Techniques for Heart Disease Prediction 
- [Read the Paper on ResearchGate](https://www.researchgate.net/publication/348607276_Comparative_Analysis_of_Machine_Learning_Algorithms_for_Heart_Disease_Prediction)

## About Dataset
- The data for heart disease prediction in this study was collected from the University of California, Iverine (UCI) online machine learning repository available at - [Dataset link](https://archive.ics.uci.edu/dataset/45/heart+disease).

- The Cleveland database which comprises 14 attributes are used in this study. With the goal of referring to the presence of heart disease using integer values of 0 (absence) to 1 (presence). The dataset taken include 303 patients made up of 241 males and 62 females.

# EDA & Data pre-processing
- Continuous Values: ['age', 'trestbps', 'chol', 'thalach', 'oldpeak']
- Categorical Values: ['sex', 'cp', 'fbs', 'restecg', 'exang', 'slope', 'ca', 'thal', 'target']
- Check correlation of the features with the target variable using correlation matrix. Found that fbs and chol are the least correlated with the target variable.
- All other variables have a significant correlation with the target variable.
- Standardize the numeric features using the StandardScaler() function.

# Model Training
- Train-test split - 80:20
- Performed cross-validation of 5-fold and 10-fold.
- We have used 5 ML algorithms for comparison:
      1) Logistic Regression 
      2) Random Forest 
      3) SVM
      4) DT 
      5) XG-Boost

# Evaluation metric
- In the context of heart disease prediction, a false negative occurs when the model fails to identify a person with heart disease as having the condition, which can be critical as it means a potential misdiagnosis and the person might not receive appropriate medical attention.
- Recall, also known as sensitivity or true positive rate, measures the ability of the model to correctly identify positive cases (cases of heart disease) out of all actual positive cases.
- So, we will be selecting the best model on the basis of the highest recall value.
- For both 5-fold cross-validation and 10-fold cross-validation, SVM is giving the highest recall value.
- SVM gives a recall of 90.27% with 10-fold cross-validation and a recall of 88.75% with 5-fold cross-validation. So, in our study, we find that the SVM method is best for this project.




