# Datasheet Template

As far as you can, complete the model datasheet. If you have got the data from the internet, you may not have all the information you need, but make sure you include all the information you do have. 

## Motivation

- For what purpose was the dataset created?
  The dataset was created to detect fraudulent credit card transactions. The aim is to provide a dataset for machine learning and data mining researchers to develop and test algorithms for anomaly detection and fraud detection in financial transactions.
- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?
  The dataset was created by the Machine Learning Group (MLG) at Université Libre de Bruxelles (ULB). The creation of the dataset was likely funded by the university or through grants supporting research in machine learning and financial fraud detection.

 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?
  The instances represent credit card transactions made by European cardholders in September 2013. Each instance includes various features derived from the raw transaction data.
- How many instances of each type are there? 
  The dataset contains 284,807 transactions, with 492 instances of fraud (0.172% of the dataset) and 284,315 instances of legitimate transactions.
- Is there any missing data?
  No, there are no missing values in the dataset.
- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?
  No, the dataset does not contain any confidential data. The features in the dataset are numerical and anonymized, ensuring that individual cardholders’ identities and transaction specifics are not exposed.

## Collection process

- How was the data acquired? 
  The data was acquired from European credit card transactions in September 2013. The dataset was generated using a combination of raw transaction data and a set of anonymized and engineered features.
- If the data is a sample of a larger subset, what was the sampling strategy? 
  The dataset appears to be a complete set of transactions for a specific period rather than a sample of a larger dataset.
- Over what time frame was the data collected?
  The data was collected over a period of two days in September 2013.

## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section. 
  Yes, significant preprocessing was performed. The dataset’s features are the result of a PCA transformation applied to the original transaction data, excluding the features ‘Time’ and ‘Amount’. The ‘Class’ label was added to indicate whether a transaction was fraudulent (1) or not (0).
- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 
  No, only the preprocessed data is available. The raw transaction data is not included to protect cardholders’ privacy.
 
## Uses

- What other tasks could the dataset be used for?
  The dataset can be used for various tasks in anomaly detection, supervised learning, and fraud detection in financial transactions. It can also be useful for research in imbalanced classification problems and feature engineering techniques.
- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 
  The main consideration is the imbalanced nature of the dataset, which might lead to biased models if not handled correctly. Dataset consumers should use appropriate techniques to address class imbalance, such as resampling, cost-sensitive learning, or anomaly detection algorithms.
- Are there tasks for which the dataset should not be used? If so, please provide a description.
  The dataset should not be used to make direct inferences about the behavior of cardholders or to profile individuals. It is anonymized and should be used solely for developing and testing algorithms.

## Distribution

- How has the dataset already been distributed? 
  The dataset is publicly available on Kaggle and can be freely downloaded for research and educational purposes.
- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  
  The dataset is subject to the Kaggle terms of use and any applicable terms set by the Machine Learning Group at ULB. Users should refer to the Kaggle dataset page for specific licensing information.

## Maintenance

- Who maintains the dataset?
  The dataset is maintained by the Machine Learning Group at ULB. The Kaggle page does not specify ongoing maintenance or updates, implying that the dataset is static and no further updates are planned.
