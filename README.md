# Data Cleaning in sql
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
[Dataset](https://github.com/babazeek/sql/blob/main/Nashville%20Housing%20Data%20for%20Data%20Cleaning.xlsx)
