# HerTechTrial-Project

### Project Title: Agricultural Sales Analysis
[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

---

### Project Overview 
The primary source of Data used here is Agricultural data.csv and a JSON file and this is an open source data that can be downloaded from an open source online such as Kaggle and FRED  
The Data Analysis Project aims to generate insight into the performance of the Agricultural project over the years . By Analysing the various parameters in the data received we seek to gather enough insight to make reasonable decisions which then enable us to tell compelling stories around our data from the insight gotten and to know the best performance from the data

### Data Sources 
---
- Python Language [Download Here](https://www.colab.goggle.com)
  1. For Data Cleaning
  2. For Analysis
  3. For Visualization

- Github for Portfolio Building

### Data Cleaning and Preparations
---
In the initial phase of the Data Cleaning and preparations, we perform the following
1. Data loading and inspection
2. Handling missing variables
3. Data Cleaning and formatting
4. Data Type conversion

### Exploratory Data Analysis 
---
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
# Create a new column 'sale_day' to store the day of the week
df['sale_day'] = df['sale_date'].dt.day_name()
print(df[['sale_date', 'sale_day']].head())
```
```Python
#Get the revenue generated by multiplying 'price_per_kg' and 'units_sold_kg' column
df['revenue_generated'] = df['price_per_kg'] * df['units_sold_kg']
print(df[['price_per_kg', 'units_sold_kg', 'revenue_generated']].head())
```
```Python
#Extracting the state from farm location
df['State']= df['farm_location'].apply(lambda x: x.split(',')[-1])
```

### Visualization 
![visualization1](https://github.com/user-attachments/assets/15803036-3d01-4cce-9ee6-5130e54e6b62)

![visualization2](https://github.com/user-attachments/assets/32204919-e255-43c4-ab83-d443a4a45355)

![visualization 3](https://github.com/user-attachments/assets/9f183a32-2eab-42f8-84e7-174c967506cd)

![visualization 4](https://github.com/user-attachments/assets/355e8891-156b-4896-b343-e69792d3fec2)

![visualization 5](https://github.com/user-attachments/assets/248e1080-485e-424c-8a94-2a692e87bc9c)

