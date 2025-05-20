# a)COVID-19 Data Exploration – SQL Project 

For this project, I conducted an in-depth exploration of COVID-19 data using SQL Server. The goal was to analyze the impact of the pandemic across different countries and populations. The dataset contained information on COVID-19 cases, deaths, vaccinations, and population statistics. The analysis was performed using SQL techniques such as joins, common table expressions (CTEs), temporary tables, window functions, aggregate functions, and data type conversions.

# Process and Steps Taken:
1. Data Selection and Initial Exploration:
I began by retrieving key columns such as location, date, total_cases, new_cases, total_deaths, and population to understand the dataset's structure. I also filtered out records where continent was NULL to focus only on meaningful country-level data.

2. Analyzing COVID-19 Mortality Rate:
To determine the likelihood of death upon contracting COVID-19, I calculated the death percentage by dividing total_deaths by total_cases. This provided insights into the severity of the virus across different locations and time periods.

3. Evaluating Infection Rate by Population:
I measured the percentage of the population infected by dividing total_cases by population. This helped assess the spread of the virus and how different regions were affected over time.

4. Finding Countries with the Highest Infection and Death Rates:
By using aggregate functions, I identified the countries with the highest total cases, deaths, and mortality rates. Sorting by different metrics provided a clear view of the most impacted regions.

5. Exploring Global Trends Over Time:
Using window functions, I calculated rolling totals for cases and deaths, allowing for trend analysis over different time periods. This revealed how the pandemic evolved globally and in specific countries.

6. Vaccination Analysis:
I integrated vaccination data by joining it with case and death records. This helped measure vaccination effectiveness, observing trends in cases and deaths before and after vaccine rollouts.

7. Creating Views for Future Reporting:
To streamline reporting, I created SQL views for key insights, allowing for quick retrieval of pre-processed data without running complex queries repeatedly.

# Outcome:
The project provided valuable insights into the impact of COVID-19 on different populations, revealing patterns in infections, deaths, and vaccinations. The use of SQL Server for data exploration made it possible to extract meaningful trends efficiently. These insights can help in making data-driven decisions related to public health and policy responses



# b) Data Cleaning in sql Using Real Estate Data
For this project, I worked on cleaning a real estate dataset stored in SQL Server to improve data quality and consistency. The dataset contained various issues such as inconsistent date formats, missing addresses, duplicate records, and improperly formatted data. The cleaning process involved a structured approach using SQL queries to transform and standardize the data.

# Process and Steps Taken:
1.Standardizing Date Format:
The SaleDate column contained inconsistent formats, making it difficult to use in queries and analysis. I converted it into a proper Date format and stored it in a new column for better usability.

2.Handling Missing Property Addresses:
Some records had missing property addresses. Since addresses were often linked to Parcel IDs, I used a self-join to fill in missing values from other records with the same Parcel ID.

3.Breaking Down Address Components:
The dataset stored addresses in a single column, making filtering and searching inefficient. I split the PropertyAddress column into StreetAddress and City to enhance data usability.

4.Standardizing Owner Address Formatting:
The OwnerAddress column contained inconsistent formatting, with some records storing the address as a single text block. I separated the street, city, and state into distinct columns.

5.Correcting Y/N Values for Boolean Fields:
Some columns used "Y" and "N" instead of a standard Boolean (1/0) format. I replaced these values to improve data consistency and compatibility with other systems.

6.Removing Duplicate Records:
Duplicate records caused redundancy and potential inaccuracies in reporting. I identified and removed duplicates using ROW_NUMBER() and ensured that only the most relevant record was retained.

7.Handling Unnecessary Data Fields:
Some columns contained unnecessary or redundant data. I reviewed the dataset and removed unneeded fields to optimize storage and improve query performance.

# Outcome:
After cleaning, the dataset was more accurate, consistent, and structured, allowing for better reporting and analysis. The transformations improved data integrity, making it easier to use in business decision-making and further analysis. This structured approach demonstrates how SQL Server can be leveraged to automate and streamline data cleaning efficiently. 

# Data set
[Nashville Housing Data](https://github.com/babazeek/sql/blob/main/Nashville%20Housing%20Data%20for%20Data%20Cleaning.xlsx)
[Nashville Housing Data](https://github.com/babazeek/sql/blob/main/Covid_Deaths.xlsx)
[Covid_Vaccinations](https://github.com/babazeek/sql/blob/main/Covid_vaccinations.xlsx)




# c)🧺 Blinkit Grocery SQL Data Cleaning & Analysis

**🎯 Project Goal:** Clean raw retail data and generate key business insights using SQL for Power BI dashboards.

## 📌 Project Overview

This project focuses on cleaning and analyzing grocery retail data using SQL. The ultimate goal is to create a clean dataset for visualization in Power BI. The data cleaning process ensures consistency and reliability, while the analysis generates key metrics such as total sales, average ratings, and outlet performance.


## 📊 Step-by-Step Breakdown (15 Steps)



### ✅ Step 1: Explore the Raw Dataset

**What:** Open and view the full dataset.
**Why:** To understand its structure and identify which fields are useful or messy.
**Outcome:** You become familiar with columns like item type, outlet info, sales, and ratings. This informs how to clean and analyze the data effectively.

### ✅ Step 2: Count Total Records

**What:** Determine how many entries are in the dataset.
**Why:** To check data completeness and estimate its size.
**Outcome:** You confirm the dataset is intact and robust enough for analysis. This ensures the results you generate will be reliable.

### ✅ Step 3: Standardize Fat Content Labels

**What:** Replace inconsistent entries like "LF", "low fat", and "reg" with "Low Fat" and "Regular".
**Why:** Inconsistent naming creates errors in grouping and reporting.
**Outcome:** You eliminate redundancy and unify labels, enabling cleaner analysis and consistent reporting in Power BI.

### ✅ Step 4: Confirm Cleaned Fat Content Data

**What:** Check the cleaned `Item_Fat_Content` column.
**Why:** To verify that only "Low Fat" and "Regular" are present.
**Outcome:** You confirm that the cleaning was successful, and future queries using this field will return accurate, consolidated results.

### ✅ Step 5: Calculate Total Sales

**What:** Add up all sales values across the dataset.
**Why:** To understand the overall revenue.
**Outcome:** You get a single, readable figure (e.g., in millions) that represents total business performance — useful for management summaries.

### ✅ Step 6: Find Average Sales

**What:** Calculate the average sales per item/entry.
**Why:** To measure the typical transaction value.
**Outcome:** You identify how much each item contributes on average, offering insight into pricing or promotion effectiveness.

### ✅ Step 7: Count Total Items or Orders

**What:** Get the total number of entries (i.e., products sold).
**Why:** To understand transaction volume.
**Outcome:** You gauge the scale of operations and prepare for average-based calculations or comparisons.


### ✅ Step 8: Calculate Average Rating

**What:** Find the average customer rating.
**Why:** To assess general customer satisfaction.
**Outcome:** You get a summary metric that reflects product quality and customer experience across the dataset.


### ✅ Step 9: Analyze Sales by Fat Content

**What:** Compare total and average sales for Low Fat vs. Regular items.
**Why:** To identify customer preferences and high-performing categories.
**Outcome:** You uncover which fat content group drives more sales and better ratings — insights that inform stocking and marketing.


### ✅ Step 10: Analyze Sales by Product Type

**What:** Group and sort total sales by item category.
**Why:** To identify best-selling product types.
**Outcome:** You determine which items generate the most revenue. This can guide product promotions, inventory planning, and expansion.


### ✅ Step 11: Compare Sales by Location and Fat Content

**What:** Cross-analyze outlet location types (Urban, Tier 1, etc.) with fat content.
**Why:** To understand geographic trends in consumer preference.
**Outcome:** You create a pivot-style summary showing what sells best in which locations — ideal for geo-targeted strategies.


### ✅ Step 12: Track Sales by Outlet Establishment Year

**What:** Examine sales grouped by the year each outlet opened.
**Why:** To explore performance across different outlet ages.
**Outcome:** You see whether older or newer outlets generate more sales, offering insight into outlet lifecycle performance.


### ✅ Step 13: Compute Sales % by Outlet Size

**What:** Calculate each outlet size’s contribution to total sales.
**Why:** To measure the sales impact of small, medium, and large outlets.
**Outcome:** You visualize which store sizes bring in more revenue — informing future expansion or investment plans.


### ✅ Step 14: Analyze Sales by Outlet Location Type

**What:** Group sales by outlet location type.
**Why:** To assess which regions perform best overall.
**Outcome:** You understand which areas (urban, semi-urban, rural) are most profitable — supporting location-based planning.


### ✅ Step 15: Get Full Metrics by Outlet Type

**What:** Summarize sales, average rating, number of items, and visibility by outlet type.
**Why:** To evaluate how different outlet types perform across multiple dimensions.
**Outcome:** You build a well-rounded performance profile per outlet type. This summary is perfect for Power BI dashboards and executive reporting.



## 🧠 Key Skills Demonstrated

* SQL data cleaning
* Grouping and aggregation
* Percentage calculations
* Pivot-style analysis
* Dashboard-ready metrics for Power BI



## 📌 Next Step: Power BI Visualization

Now that the data is clean and metrics are ready, the next phase involves building interactive dashboards in Power BI to visually present these insights for decision-making.


# Data set
[Blinkit Data](https://github.com/babazeek/sql/blob/f64e09af56f915ffa81f399273d22c94eb9c52fd/BlinkIT%20Grocery%20Data.csv)
[Blinkit Queries](https://github.com/babazeek/sql/blob/main/Covid_Deaths.xlsx)
[Covid_Vaccinations](https://github.com/babazeek/sql/blob/main/Covid_vaccinations.xlsx)





