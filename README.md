# Case Study 2: Predicting Credit Risk and Detecting Fraud

## Overview
This case study focuses on the development of a **Credit Risk Scoring Model** to predict fraudulent activities and assess credit risk for consumer credit products. The goal is to build an interpretable machine learning model to assign a **Credit Risk Score** (0–1000) for customers, aiding financial institutions in decision-making and fraud detection.

## Problem Statement
The financial institution has observed a significant rise in charged-off accounts, particularly in credit card and personal loan divisions. Some of these charge-offs are attributed to **fraudulent behaviors**, where individuals exploit the system with no intention of repayment. Current models relying on financial ratios and FICO scores are insufficient to address evolving fraud patterns.

### Objectives
1. **Exploratory Data Analysis (EDA)**: Analyze patterns and key variable relationships, particularly those associated with fraudulent behavior and charge-offs.
2. **Model Development**: Build a predictive model to:
   - Determine the likelihood of an account being charged off.
   - Generate a **Credit Risk Score** between 0 (low risk) and 1000 (high risk).
   - Ensure **model interpretability** for regulatory compliance and actionable insights.

## Dataset
The dataset consists of **7,000 observations**, each representing an individual credit application. It includes **demographic**, **financial**, and **behavioral variables**. The target variable is `Charge Off Status` (True/False), where:
- **True**: Account is charged off (defaulted).
- **False**: Account is active and not yet defaulted.

### Data Dictionary
| Variable                          | Description                                                                                                                                                       |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Account_open_date`               | Date the account was opened.                                                                                                                                     |
| `Age`                             | Age of the customer.                                                                                                                                             |
| `Location`                        | Customer's geographical location.                                                                                                                                |
| `Occupation`                      | Customer's occupation.                                                                                                                                          |
| `Income_level`                    | Income level of the customer.                                                                                                                                   |
| `Fico_score`                      | Credit score (300–850), with higher scores indicating better creditworthiness.                                                                                   |
| `Delinquency_status`              | Days late on required payments.                                                                                                                                 |
| `Number_of_credit_applications`   | Number of recent credit applications.                                                                                                                            |
| `Debt_to_income_ratio`            | Ratio indicating financial distress, correlated with fraud risk.                                                                                                 |
| `Payment_methods_high_risk`       | Use of high-risk payment methods (e.g., cryptocurrencies).                                                                                                       |
| `Max_balance`                     | Maximum account balance recorded.                                                                                                                                |
| `Avg_balance_last_12months`       | Average balance over the past year.                                                                                                                              |
| `Number_of_delinquent_accounts`   | Count of accounts with missed payments.                                                                                                                          |
| `Number_of_defaulted_accounts`    | Count of accounts defaulted over time.                                                                                                                           |
| `Earliest_credit_account`         | Date the first credit account was opened.                                                                                                                        |
| `Recent_trade_activity`           | Date of the latest transaction.                                                                                                                                  |
| `New_accounts_opened_last_12months` | Number of accounts opened in the past year.                                                                                                                      |
| `Multiple_applications_short_time_period` | Boolean: Whether the user submitted multiple applications in a short period (`True`/`False`).                                                                  |
| `Unusual_submission_pattern`      | Boolean: Whether the user exhibited irregular behavior in transactions (`True`/`False`).                                                                          |
| `Applications_submitted_during_odd_hours` | Boolean: Whether transactions were submitted outside business hours (`True`/`False`).                                                                           |
| `Watchlist_blacklist_flag`        | Boolean: Whether the user is flagged as high risk on predefined lists (`True`/`False`).                                                                           |
| `Public_records_flag`             | Boolean: Whether the user has concerning public records (`True`/`False`).                                                                                        |
| **Target Variable**               | **`Charge Off Status`**: Boolean indicating if the account is charged off (`True`) or active (`False`).                                                           |

## Requirements
The project emphasizes **interpretability** for:
1. **Regulatory Compliance**: Transparency to meet legal standards.
2. **Customer Trust**: Fairness in decisions and explanations for flagged accounts.
3. **Internal Decision-Making**: Providing actionable insights for credit officers.

## Tasks
1. **Perform EDA**: Identify fraudulent patterns and relationships.
2. **Model Development**:
   - Predict the likelihood of charge-offs.
   - Generate and explain Credit Risk Scores.
3. **Ensure Explainability**: Highlight key contributing features for each prediction.
