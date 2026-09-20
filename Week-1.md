# FinTrust Financial Intelligence & Digital Banking Support Solution
## Week 1 — Data Analytics Track
### Project Overview

FinTrust Digital Bank is a fictional digital banking organisation serving
customers through mobile and online banking channels.

The organisation collects increasing amounts of customer and transaction
data but needs a stronger way to transform this information into actionable
business intelligence.

As part of the multidisciplinary Data & AI Experience Lab, the Data
Analytics track focuses on exploring customer and transaction data,
developing KPIs, identifying meaningful patterns, and communicating
business insights that can support decision-making.

---

# 1. Business Understanding

## 1.1 What problem is FinTrust trying to solve?

FinTrust currently has customer and transaction information but lacks an
integrated approach for turning this data into useful business intelligence.

The organisation needs to:

- Gain clearer visibility into customer and transaction behaviour.
- Identify potentially unusual or higher-risk transaction patterns.
- Generate insights that support risk-related and operational decision-making.
- Understand important trends across customers, transactions, products,
  channels and transaction types.
- Provide reliable information that can support other technical components
  of the wider FinTrust solution.

The Data Analytics track contributes to this problem by transforming raw
customer and transaction data into structured information, KPIs, trends
and business insights.

---

## 1.2 Why is this problem important?

As FinTrust's customer base and transaction activity grow, the volume of
available data also increases.

Without effective analysis, management may find it difficult to understand:

- who its customers are;
- how customers use FinTrust's services;
- which transaction channels and types generate the most activity;
- how transaction behaviour changes over time;
- where unusual transaction patterns may exist; and
- which areas require further investigation.

Data-driven business intelligence can help management make decisions based
on evidence from the available data rather than relying only on assumptions.

---

## 1.3 How can Data Analytics contribute?

The Data Analytics track can contribute by:

1. Profiling the customer and transaction datasets.
2. Assessing data quality and identifying important limitations.
3. Analysing customer behaviour and transaction activity.
4. Identifying trends and patterns across relevant dimensions.
5. Developing meaningful business KPIs.
6. Creating visualisations and dashboards.
7. Communicating findings in a way that can support business decision-making.
8. Identifying patterns that may be relevant to the wider risk-analysis
   and predictive-modelling work.

The analytics outputs can also provide useful context for the Data Science,
Machine Learning and Generative AI tracks.

---

## 1.4 What outputs could the Data Analytics track provide?

The expected outputs include:

- Data profiling report
- Exploratory data analysis
- Business KPIs
- Customer and transaction insights
- Trend analysis
- Risk-related descriptive patterns
- Power BI dashboard
- Business intelligence visualisations
- Final analytical findings and recommendations

---

# 2. Review of Relevant Resources

## 2.1 Customer Dataset

### What it contains

The customer dataset contains information about FinTrust's customers.
The specific fields and characteristics of the dataset are documented in
the Data Understanding section below.

### How I expect to use it

The customer dataset will be used to:

- understand the structure of FinTrust's customer base;
- identify customer characteristics;
- explore possible customer segments;
- compare behaviour across customer groups;
- support customer-level KPIs and visualisations; and
- connect customer characteristics with transaction activity where
  appropriate.

### Limitations

- Missing key financial details: It lacks credit scores, employment status, total savings, and debt info, making deep risk profiling hard.

- Income is in broad groups: Monthly_Income_Band uses general ranges instead of exact figures, which reduces calculation accuracy.

- Basic demographics only: It only records basic facts like age, city, and account type, limiting complex customer insights.

- No external data: It does not include external credit bureau data or economic trends.


---

## 2.2 Transaction Dataset

### What it contains

The transaction dataset contains records of FinTrust customer transactions.
The specific fields, data types and characteristics are documented in the
Data Understanding section.

### How I expect to use it

The transaction dataset will be used to analyse:

- transaction volume;
- transaction value;
- transaction frequency;
- transaction channels;
- transaction types;
- transaction status;
- transaction trends over time; and
- patterns that may be relevant to risk analysis.

### Limitations

- Missing information: Columns like Device_Type and Location have 96 missing entries each (only 11,904 out of 12,000 records are complete).

- Date formatted as plain text: Transaction_DateTime is saved as text (object) instead of a true date format, requiring conversion before time analysis.

- Short timeframe: The dataset only logs 12,000 transactions across 1,500 customers (an average of 8 transactions per customer), which may not show long-term habits.

- Location data is general: City/location entries lack precise coordinates or IP addresses needed for advanced location-based fraud detection.

---

# 3. Data Analytics Track Objectives

The main objectives of my Data Analytics work are to:

1. Understand and profile FinTrust's customer and transaction datasets.
2. Assess data quality and identify important data limitations.
3. Analyse customer behaviour and transaction patterns to identify
   meaningful business trends.
4. Develop relevant KPIs that can help management monitor business
   performance and transaction activity.
5. Design a dashboard that communicates important customer, transaction
   and risk-related insights clearly.

---

# 4. Success Criteria

The eventual Data Analytics solution will be considered successful if it:

- provides an accurate understanding of the available datasets;
- answers meaningful business questions using the available data;
- provides clearly defined and relevant KPIs;
- identifies useful customer and transaction patterns;
- communicates findings clearly through appropriate visualisations;
- allows management to explore important dimensions of the data;
- identifies descriptive patterns that can support further risk analysis;
- uses appropriate data validation and quality checks; and
- produces insights that can support operational decision-making.

---

# 5. Data Understanding

## 5.1 Customer Dataset

| Number of records | 1500 |
| Number of columns | 12 |
| Field names | 'Customer_ID', 'Customer_Name', 'Age', 'Gender', 'City',
       'Customer_Segment', 'Account_Type', 'Tenure_Months',
       'Digital_Engagement_Score', 'Monthly_Income_Band', 'Preferred_Channel',
       'Account_Status' |
| Data types | Customer_ID   object
Customer_Name                object
Age                          int64
Gender                       object
City                         object
Customer_Segment             object
Account_Type                 object
Tenure_Months                int64
Digital_Engagement_Score     float64
Monthly_Income_Band          object
Preferred_Channel            object
Account_Status               object |
| Categorical variables | Customer_ID, Customer_Name, Gender, City, Customer_Segment, Account_Type, Monthly_Income_Band, Preferred_Channel, Account_Status |
| Numerical variables |Age,Tenure_Months, Digital_Engagement_Score|
| Date/time variables |0|
| Missing values | Zero Missing values |
| Obvious data-quality issues |
Missing income details: Income is shown in generic ranges (like "Low" or "High") instead of exact dollar or naira figures.
Missing financial history: The dataset lacks key risk info like credit scores, loan histories, savings totals, or job status.
Basic details only: It only covers simple facts (age, city, gender, account type), which limits deep analysis.
|

---

## 5.2 Transaction Dataset

| Number of records | 12000 |
| Number of columns | 11 |
| Field names | 'Transaction_ID', 'Customer_ID', 'Transaction_DateTime',
       'Transaction_Type', 'Amount_NGN', 'Channel', 'Device_Type', 'Location',
       'International_Transaction', 'Transaction_Status', 'Risk_Review_Flag' |
| Data types| Transaction_ID  object
Customer_ID                   object
Transaction_DateTime          object
Transaction_Type              object
Amount_NGN                   float64
Channel                       object
Device_Type                   object
Location                      object
International_Transaction     object
Transaction_Status            object
Risk_Review_Flag              object |
| Categorical variables | Customer_ID, Transaction_Type, Channel, Device_Type, Location, International_Transaction, Transaction_Status, Risk_Review_Flag |
| Numerical variables | Amount_NGN  |
| Date/time variables | Transaction_DateTime |
| Missing values | Device_Type: 96, Location: 96 |
| Obvious data-quality issues | 
Missing information: Columns like Device_Type and Location are missing data in 96 rows.
Dates saved as plain text: The date and time column (Transaction_DateTime) is stored as text, which stops Python from doing automatic time calculations or date filtering.
Short history: With 12,000 transactions across 1,500 people, each customer averages only 8 transactions, which is too short to track long-term spending patterns. 
|
---

## 5.3 Relationship Between the Datasets

The customer and transaction datasets connected through
a common customer identifier.

This relationship allows customer-level information to be analysed together
with transaction-level activity.

---

# 6. Analytical Questions

The following questions will guide the Data Analytics work.

## Customer Behaviour

1. Who are FinTrust's major customer segments based on the available customer characteristics?

2. How does transaction behaviour differ across customer groups?

3. Which customer groups demonstrate the highest transaction activity?

## Transaction Activity

4. How does transaction volume change over time?

5. How does transaction value change over time?

6. Which transaction channels and transaction types generate the greatest
   activity?

## Transaction Status

7. What proportion of transactions are successful, failed, pending or
   classified under other available statuses?

## Risk-Related Patterns

8. What customer, transaction, channel or value characteristics are
   associated with potentially unusual or higher-risk transaction patterns?

These questions will be refined if data limitations prevent specific
questions from being answered reliably.

---

# 7. KPI Planning

| KPI | Definition | Why It Matters | Required Data |
|---|---|---|---|
| Total Customers | Number of unique customers | Measures the size of the customer base | Customer ID |
| Total Transactions | Number of transaction records | Measures transaction activity | Transaction ID |
| Total Transaction Value | Sum of transaction amounts | Shows the overall value of transaction activity | Transaction amount |
| Average Transaction Value | Total transaction value divided by number of transactions | Shows the typical transaction size | Transaction amount, transaction ID |
| Transaction Success Rate | Successful transactions divided by total transactions × 100 | Measures transaction completion performance | Transaction status |
| Transaction Failure Rate | Failed transactions divided by total transactions × 100 | Helps identify transaction or operational issues | Transaction status |
| Active Customer Rate | Active customers divided by total customers × 100 | Provides an indication of customer engagement | Customer ID, transaction data |
| Transaction Volume by Channel | Number of transactions grouped by channel | Helps identify channel usage patterns | Transaction channel, transaction ID |

---

# 8. Dashboard Planning

## Proposed Dashboard Structure

### Section 1 — Executive Overview

Key KPI cards:

- Total Customers
- Total Transactions
- Total Transaction Value
- Average Transaction Value
- Transaction Success Rate
- Transaction Failure Rate

### Section 2 — Customer Insights

Potential visualisations:

- Customer distribution by segment
- Customer activity by segment
- Transaction activity by customer group
- Top customer groups by transaction activity

### Section 3 — Transaction Intelligence

Potential visualisations:

- Transaction volume over time
- Transaction value over time
- Transactions by channel
- Transactions by transaction type
- Transaction status distribution

### Section 4 — Risk & Operational Patterns

Potential visualisations:

- Failed transactions by channel
- High-value transactions
- Unusual transaction patterns
- Risk-related transaction trends

These visualisations will be developed only where the available data
supports the analysis.

### Dashboard Filters

Potential filters include:

- Date
- Customer segment
- Transaction channel
- Transaction type
- Transaction status

---

# 9. Initial Analysis Plan

## Week 2 — Data Preparation & Exploration

- Perform detailed data profiling.
- Validate data types.
- Check missing values and duplicates.
- Investigate obvious data-quality issues.
- Validate the relationship between datasets.
- Clean the data where appropriate.
- Begin exploratory data analysis.
- Calculate preliminary KPIs.

## Week 3 — Analysis & Insight Generation

- Analyse customer behaviour.
- Analyse transaction trends and values.
- Compare transaction channels and types.
- Analyse transaction status.
- Investigate descriptive risk-related patterns.
- Answer the analytical questions.
- Identify key business insights.

## Week 4 — Dashboard & Communication

- Develop the Power BI dashboard.
- Validate KPI calculations.
- Create final visualisations.
- Communicate key findings.
- Document limitations.
- Develop final recommendations based on the analysis.
- Prepare the final project presentation.

---

# 10. Tools

The main tools planned for the Data Analytics track are:

- Python
- Pandas
- SQL
- Excel
- Power BI
- GitHub

Tools will be used according to the requirements of each stage rather
than forcing every tool into the project.

