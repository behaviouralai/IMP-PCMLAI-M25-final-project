# Credit Card Fraud Detection with XGBoost


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
This project aims to detect fraudulent credit card transactions using machine learning. Given the high stakes involved in financial fraud, an accurate and robust model is essential to protect consumers and financial institutions. The model predicts whether a transaction is fraudulent or not based on various features derived from the transaction data. It leverages advanced techniques to handle the significant class imbalance inherent in fraud detection problems. 

## DATA
The data used in this project is the Credit Card Fraud Detection dataset from the Machine Learning Group - ULB, available on Kaggle. The dataset contains 284,807 transactions, with 492 instances of fraud (0.172% of the dataset) and 284,315 instances of legitimate transactions. The features (V1 through V28) are principal components obtained via PCA to protect sensitive information, while the ‘Time’ and ‘Amount’ features were not anonymised. The ‘Class’ feature indicates whether a transaction is fraudulent (1) or not (0). 

**Data Source:**
- Kaggle: [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)


## MODEL 
The model used is an XGBoost classifier, chosen for its efficiency and effectiveness in handling large datasets and complex patterns. XGBoost is an implementation of gradient-boosted decision trees designed for speed and performance. It is particularly suitable for classification tasks with imbalanced datasets, such as fraud detection, due to its ability to handle class weights and provide high accuracy.

## HYPERPARAMETER OPTIMSATION
Hyperparameters for the XGBoost model were fine-tuned using RandomizedSearchCV with 5-fold cross-validation. The following hyperparameters were optimised:
- **Learning Rate:** 0.3
- **Number of Estimators:** 300
- **Max Depth:** 5
- **Subsample:** 0.9
- **Colsample_bytree:** 1.0

These values were chosen based on their performance in the cross-validation process, aiming to balance precision and recall effectively. 

## RESULTS
The model's performance was primarily evaluated using the Area Under the Precision-Recall Curve (AUPRC), which is particularly suited for imbalanced classification problems. The following metrics were achieved:
- **AUPRC:** 0.89
- **Precision:** 0.97
- **Recall:** 0.88

These results indicate that the model is highly effective in identifying fraudulent transactions while maintaining a low rate of false positives. 

**Performance Graph:**
![Screenshot](kfold_performance_graph.png)

### Key Insights:
- The model performs well in detecting fraudulent transactions with high precision and recall.
- The AUPRC metric demonstrates the model's capability to handle imbalanced data effectively.
- Continuous monitoring and retraining are essential to maintain the model's performance over time, especially as transaction patterns evolve.

