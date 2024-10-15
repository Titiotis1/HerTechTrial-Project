# HerTechTrial-Project

### Project Title: Agricultural Sales Analysis
---

### Project Overview 
The primary source of Data used here is Agricultural data.csv and a JSON file and this is an open source data that can be downloaded from an open source online such as Kaggle and FRED  
The Data Analysis Project aims to generate insight into the performance of the Agricultural project over the years . By Analysing the various parameters in the data received we seek to gather enough insight to make reasonable decisions which then enable us to tell compelling stories around our data from the insight gotten and to know the best performance from the data

### Data Sources 
- Python Language [Download Here](https://www.colab.goggle.com)
  1. For Data Cleaning
  2. For Analysis
  3. For Visualization

- Github for Portfolio Building

### Data Cleaning and Preparations
In the initial phase of the Data Cleaning and preparations, we perform the following
1. Data loading and inspection
2. Handling missing variables
3. Data Cleaning and formatting
4. Data Type conversion

### Exploratory Data Analysis      
EDA involves exploring the data to answer some questions about the data such as;

- How much Revenue was generated from each products
- Top 5 suppliers by revenue generated
- Top 5 products by revenue generated

### Data Analysis
This is where we include some basic lines of code or queries used during the analysis ;

```Python
state_revenue = df.groupby(['State','farm_location'])['revenue_generated'].agg('sum').sort_values(ascending=False).head()
state_revenue = state_revenue.reset_index()
print(state_revenue)
```
```Python
df['sale_day'] = df['sale_date'].dt.day_name()
print(df[['sale_date', 'sale_day']].head())
```
```Python
df['revenue_generated'] = df['price_per_kg'] * df['units_sold_kg']
print(df[['price_per_kg', 'units_sold_kg', 'revenue_generated']].head())
```





