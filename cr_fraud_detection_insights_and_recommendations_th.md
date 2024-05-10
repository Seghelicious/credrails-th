# Case Study Analysis

### Fraud Detection in Transaction data

The aim of this project is to detect anomalies a.k.a. fraudulent transctions in fictitious dataset of transaction data. In this case study the anomaly detection technique used was the Isolation Forest algorithm. This choice of this tree-based algorithm was based on the the principle of isolation to identify anomalies in datasets. The isolation forest algorithm can identify abnormal patterns in transactional data, such as in card and online transactions. The Isolation Forest algorithm is able to detect fraudulent transactions that deviate from the normal patterns of transactions, such as transactions that occur at unusual times or locations or involve unusually large amounts of money. 

Financial fraud is a crime of deceiving people in their transactions. Frauds in the credit cards industry are stealing or using stolen cards, or take more an aggressive form such as account takeover, counterfeiting and much more. The magnitude of card fraud, especially credit card is growing larger each day due to ever-increasing online transactions.

Anomaly detection is an unsupervised data processing technique to detect anomalies from the dataset. Anomalies are data points that stand out amongst other data points in the dataset and do not fit the normal behavior in the data. These data points or observations deviate from the dataset’s normal behavioral patterns. The anomaly detection is very useful to detect fraud transactions just like in our case.

##### Dataset

The dataset that is used for this exercise is a fictitions transaction data generated with Faker.
The dataset contains transactions made with credit cards, debit cards and online transactions with PayPal between May 2023 to May 2024. The data had 10 features including Transaction_ID, Date, Time, Customer_ID, Product_ID, Amount, Payment_Type, Country, Merchant_ID and Status. 300000 observations across each feature were used in this exercise.

##### Data Preparation

The data was engineered by creating additional by features with the Date/ Time columns and encoding the categorical features Payment_Type, Country, and Status. Customer ID, Product ID and Merchant ID were dropped.

##### Exploratory Data Analysis (EDA)

Details of the EDA can be found in the .ipynb file and the plots can be found in the images folder.

##### Model Development

Details of the model development can be found in the notebook.

#### Insights and Recommendations

True positives - 79038, 
False positives - 10353, 
False negatives - 20284, 
True negatives - 10325

Accuracy, Precision, Recall and F1-score 

           precision    recall  f1-score   support

      Normal       0.88      0.88      0.88     89391
     Anomaly       0.66      0.66      0.66     30609

    accuracy                           0.83    120000
   macro avg       0.77      0.77      0.77    120000
weighted avg       0.83      0.83      0.83    120000

ROC-AUC curve was 0.23

Recall is the preferred metric as it measures the proportion of anomalies correctly identified by the model. Recall is also the most costly metric and a poor recall could have severe consequences. The model achieved a recall of 66%, whic implies that a whooping 34% of fraudulent transactions went unidentified. The following could be the disastrous consequences for a situation where the model is deployed.


1. A direct financial loss is the most immediate cost, where the fraudulent transaction amount is directly lost by the fictitious company (e.g., stolen funds, unauthorized purchases).
2. A completed fraudulent transaction causes the victim (customer or business) to initiate a chargeback or dispute. This can lead to additional fees and potential loss of revenue for the company.
3. There are increased operational costs for investigating false negatives (unidentified fraudulent transactions). The processes, usually time-consuming and resource-wastingtypically involve manual review of transactions, potential customer support interactions, and potential legal fees.
4. When fraud occurs, especially if it's not detected promptly, customers might lose trust in the company's security measures. This can lead to customer churn and damage the brand reputation.
5. A failure to adequately detect fraud can lead to fines or penalties from regulatory bodies.

##### Strategies to counteract Fraudulent Transactions

1. ML and AI-powered fraud detection algorithms can be deployed to that can analyze transaction patterns, customer behavior, and risk factors to identify suspicious activities in real-time. The models can learn from historical fraud data and adapt to evolving fraud tactics.
2. Regularly analyis of transaction data to identify trends and anomalies that might uncover potential fraud rings or new fraud schemes. This proactive approach utilizing data analytics and monitoring helps a company stay ahead of evolving threats.
3. The utilization of strong customer verification methods like multi-factor authentication (MFA) to ensure the legitimacy of users attempting transactions including one-time passwords, fingerprint or facial recognition, or knowledge-based authentication (security questions) can be employed.
4. lerting systems with thresholds and alerts for monitoring suspicious activities which can can trigger manual review or automated actions like blocking transactions exceeding certain risk scores.
5. Ensure your fraud prevention measures comply with relevant industry regulations 
6. Regularly review and update your fraud prevention strategies based on new threats, emerging technologies, and the effectiveness of your existing methods.

