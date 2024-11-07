# Fraud Detection Project
This project focuses on building a system to classify transactions as either fraudulent or legitimate. It uses a simulated dataset with core transaction details and implements various fraud detection scenarios. The goal is to create a robust model capable of detecting patterns indicative of fraudulent behavior.
Project Overview
Fraud detection is essential for identifying potentially fraudulent transactions to protect users and financial institutions. This project uses a synthetic dataset that simulates fraud using different behavioral scenarios. Our objective is to detect such patterns and flag them as fraud with high accuracy.

## Dataset Details
The dataset is a simulated set of original and fraudulent transactions containing only the essential details of each transaction. Fraudulent transactions are labeled based on specific scenarios to create a realistic testing environment for fraud detection techniques.

Key Columns:
* TRANSACTION_ID: Unique identifier for each transaction.
* TX_DATETIME: Date and time when the transaction occurred.
* CUSTOMER_ID: Unique identifier for each customer.
* TERMINAL_ID: Unique identifier for each terminal or merchant.
* TX_AMOUNT: Amount of the transaction.
* TX_FRAUD: Binary label indicating whether the transaction is fraudulent (1) or legitimate (0).
## Fraud Scenarios
Three fraud scenarios are simulated in this dataset:

High-Value Transactions: Any transaction with an amount over 220 is marked as fraudulent. This simple pattern helps validate the baseline performance of the fraud detection model.

Compromised Terminals: Each day, two terminals are randomly selected, and all transactions on these terminals for the next 28 days are labeled fraudulent. This scenario mimics terminal misuse, such as phishing attacks.

Customer Credential Theft: Randomly, three customers are selected daily, and 1/3 of their transactions in the following 14 days have their amounts multiplied by 5 and are marked as fraudulent. This simulates high-value fraud due to leaked customer credentials.

# Features
To detect fraud effectively, new features were engineered based on the simulated fraud scenarios:

1. High_Amount_Flag: Identifies transactions over 220.<br>
2. Terminal_Fraud_Count: Tracks the frequency of frauds at specific terminals.<br>
3. Daily_Fraud_Transaction_Count: Counts the number of fraudulent transactions at each terminal per day.<br>
4. Customer_Spend_Avg: Monitors the average transaction amount for each customer.<br>
5. Transaction_Amount_Deviation: Measures how much a transaction deviates from a customer’s average spending.<br>
6. These features enable the model to detect both obvious and nuanced fraud patterns by analyzing transaction data over time and by individual customer behavior.<br>
These features enable the model to detect both obvious and nuanced fraud patterns by analyzing transaction data over time and by individual customer behavior.
