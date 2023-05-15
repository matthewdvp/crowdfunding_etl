### Crowdfunding_ETL Project

This mini project involves extracting and transforming data from Excel files to create DataFrames, exporting the DataFrames to CSV files, and creating a PostgreSQL database based on the extracted data. Here are the instructions for completing this project:

# Create the Category and Subcategory DataFrames
Extract and transform the data from the crowdfunding.xlsx Excel file to create a category DataFrame with the following columns:

category_id column with entries going sequentially from "cat1" to "catn", where n is the number of unique categories.
category column that contains only the category titles.
Export the category DataFrame as category.csv and save it to your GitHub repository.

Extract and transform the data from the crowdfunding.xlsx Excel file to create a subcategory DataFrame with the following columns:

subcategory_id column with entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories.
subcategory column that contains only the subcategory titles.
Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

# Create the Campaign DataFrame
Extract and transform the data from the crowdfunding.xlsx Excel file to create a campaign DataFrame with the following columns:

cf_id column.
contact_id column.
company_name column.
blurb column, renamed to description.
goal column converted to the float data type.
pledged column converted to the float data type.
outcome column.
backers_count column.
country column.
currency column.
launched_at column, renamed to launch_date, with UTC times converted to the datetime format.
deadline column, renamed to end_date, with UTC times converted to the datetime format.
category_id column with unique identification numbers matching those in the category_id column of the category DataFrame.
subcategory_id column with unique identification numbers matching those in the subcategory_id column of the subcategory DataFrame.
Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

# Create the Contacts DataFrame
Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel file:

Option 1: Use Python dictionary methods.
Import the contacts.xlsx file into a DataFrame.

Iterate through the DataFrame, converting each row to a dictionary.

Iterate through each dictionary, following these steps:

Extract the dictionary values from the keys using a Python list comprehension.
Add the values for each row to a new list.
Create a new DataFrame that contains the extracted data.

Split each "name" column value into a first and last name, placing each in a new column.

Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.
