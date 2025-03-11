# Customer Purchase Data Analysis

## Overview
This project analyzes a customer purchase dataset using Python and Pandas. The analysis includes demographic statistics, spending patterns, popular customer names, and email providers. The dataset is assumed to be in CSV format and needs to be loaded before executing the code.

## Dataset
The dataset (Cust_Purch_FakeData.csv) contains customer purchase details, including age, spending, profession, credit card type, and email provider. Ensure the file is available in the correct directory before running the code.

## Analysis and Code Snippets

### Age Analysis
```python
# Find max, min, and mean age
print('Max. age of the customer is:', df['age'].max())
print('Min. age of the customer is:', df['age'].min())
print('Avg. age of the customer is:', df['age'].mean())
```
**Results:**
- Max. age of the customer is: 65
- Min. age of the customer is: 18
- Avg. age of the customer is: 41.55

This helps understand the age distribution of customers.

### Most Common Customer Names
```python
# Find the three most common first names
df['first'].value_counts(ascending=False).head(3)
```
**Results:**
- Willie: 130
- Francis: 124
- Eula: 86

Identifies the most frequently occurring first names.

### Spending Analysis
```python
# Find max, min, and average spending
print('Max. spending is:', df['price(CAD)'].max())
print('Min. spending is:', df['price(CAD)'].min())
print('Avg. spending is:', df['price(CAD)'].mean())
```
**Results:**
- Max. spending is: 100.0
- Min. spending is: 0.0
- Avg. spending is: 49.99

This provides insights into how much customers typically spend.

### Credit Card Analysis
```python
# Count the number of people using Visa
print(df[df['cc_type'] == 'Visa'].count().iloc[0])
```
**Results:** 1721 customers use Visa as their credit card provider.

### Most Common Professions
```python
# Find the two most common professions
df['profession'].value_counts(ascending=False).head(2)
```
**Results:**
- Preschool Teacher: 112
- Distribution Manager: 107

Shows the most frequently occurring professions among customers.

### Popular Email Providers
```python
# Find the top 5 email providers
df['email'].apply(lambda x: x.split('@')[1]).value_counts().head(5)
```
**Results:**
1. gmail.com: 1687
2. me.com: 1676
3. outlook.com: 1664
4. live.com: 1660
5. hotmail.com: 1659

Identifies the most used email domains by customers.

### Busiest Day of the Week
```python
# Find which day of the week has the most customers
df['weekday'].value_counts().head(5)
```
**Results:**
1. Saturday: 4376 customers
2. Wednesday: 4365 customers
3. Thursday: 4327 customers
4. Friday: 4316 customers
5. Monday: 4216 customers

Determines which day brings the highest number of customers to the store.

## Insights
- The dataset reveals customer demographic trends, such as common age groups and professions.
- Spending habits vary, with some customers spending significantly more than others.
- Visa appears to be a common credit card provider.
- The most common customer names and email providers give insight into customer demographics.
- Identifying the busiest day helps optimize store operations.

## Conclusion
This analysis provides a foundational understanding of customer purchase behavior, helping businesses make data-driven decisions. Further analysis can be conducted by incorporating additional factors such as location, gender, and seasonal trends.

## Requirements
- Python 3.x
- Pandas library
- Dataset (Cust_Purch_FakeData.csv)

