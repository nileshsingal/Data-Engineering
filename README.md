# Data-Engineering

# Data Engineering Lab: Extract, Transform, and Load Data using Python

## Introduction

Extract, Transform, and Load (ETL) operations are crucial for Data Engineers to efficiently manage and process data. In this lab, you will gain hands-on experience in performing these operations using Python. The primary tasks include reading data from CSV, JSON, and XML files, extracting necessary information, transforming the data to meet specific requirements, and finally saving it in a format ready for loading into a Relational Database Management System (RDBMS).

## Objectives

After completing this lab, you will be able to:

1. Read CSV, JSON, and XML file types using Python.
2. Extract the required data from different file types.
3. Transform the extracted data into the desired format.
4. Save the transformed data in a format suitable for loading into an RDBMS.


### 1. Download the Data

Download the zip file containing the required data in multiple formats.

```bash -- If wget is not installed then install using brew install wget

wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0221EN-SkillsNetwork/labs/module%206/Lab%20-%20Extract%20Transform%20Load/data/source.zip
unzip source.zip


# Conclusion

In this lab, you practiced the implementation of:

1. Extraction of data from CSV, JSON, and XML file formats.

2. Transformation of data as per requirement.

3. Loading the transformed data to a CSV file.

4. Logging the progress of the said operations.


# Web Scraping for Top 50 Movies

## Introduction
This Python script demonstrates web scraping techniques to extract information about the top 50 movies with the best average rating from a specific web page. The script utilizes the `requests` and `BeautifulSoup` libraries to fetch and parse the HTML content, respectively.

## Estimated Effort
Approximately 30 minutes

## Objectives
By the end of this script, you will be able to:

- Extract information such as Average Rank, Film, and Year from a web page
- Save the extracted data to both a CSV file (`top_50_films.csv`) and an SQLite database (`Movies.db`)

## Scenario
Imagine you have been hired by a Multiplex management organization, and your task is to extract information from the [provided web link](https://web.archive.org/web/20230902185655/https://en.everybodywiki.com/100_Most_Highly-Ranked_Films). The information needed includes Average Rank, Film, and Year for the top 50 movies.

## Instructions
1. Create a Python script named `webscraping_movies.py`.
2. Use the `requests` library to fetch the content of the provided web page.
3. Utilize the `BeautifulSoup` library to parse and analyze the HTML code.
4. Identify the HTML elements containing the required information (Average Rank, Film, and Year).
5. Extract the relevant information and save it to a CSV file named `top_50_films.csv`.
6. Save the same information to an SQLite database named `Movies.db` under the table name `Top_50`.

## Example Code
```python
import requests
from bs4 import BeautifulSoup
import csv
import sqlite3

python3.11 -m pip install pandas
python3.11 -m pip install bs4

# Practice Problems

## Problem 1
### Modify the code to extract Film, Year, and Rotten Tomatoes' Top 100 headers.

Try modifying the provided Python script (`webscraping_movies.py`) to extract additional information such as Film, Year, and the Rotten Tomatoes' Top 100 headers. Analyze the HTML structure of the web page and adjust the code accordingly. Save the extracted data to the CSV file and the SQLite database.

## Problem 2
### Restrict the results to only the top 25 entries.

Enhance the script to retrieve and save information only for the top 25 movies instead of the top 50. Adjust the code to handle this restriction while still maintaining the integrity of the extracted data.

## Problem 3
### Filter the output to print only the films released in the 2000s (year 2000 included).

Extend the functionality of the script to filter and display information only for the films released in the 2000s. Update the code to include a condition that checks the release year and prints only the relevant entries meeting the specified criteria.

**Note:** Solutions for the practice problems are not provided. Feel free to use the discussion forums if you need assistance or want to discuss your approach with others.


# Database Access using Python Script

Using databases is an important and useful method of sharing information. To preserve repeated storage of the same files containing the required data, it is a good practice to save the said data on a database on a server and access the required subset of information using database management systems.

## Objectives

In this lab, you'll learn how to:

- Create a database using Python
- Load data from a CSV file as a table to the database
- Run basic "queries" on the database to access the information

## Scenario

Consider a dataset of employee records that is available with an HR team in a CSV file. As a Data Engineer, you are required to create the database called STAFF and load the contents of the CSV file as a table called INSTRUCTORS.

### Dataset Headers:

- ID: Employee ID
- FNAME: First Name
- LNAME: Last Name
- CITY: City of residence
- CCODE: Country code (2 letters)

## Reading the CSV file

To read the CSV using Pandas, you can use the `read_csv()` function. Since this CSV does not contain headers, you can use the keys of the `attribute_dict` dictionary as a list to assign headers to the data.

```python
file_path = '/home/project/INSTRUCTOR.csv'
df = pd.read_csv(file_path, names=attribute_list)

