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



# b) Data Cleaning in sql
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
