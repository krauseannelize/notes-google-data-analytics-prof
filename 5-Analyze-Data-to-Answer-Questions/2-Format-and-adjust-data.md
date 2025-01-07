# Format and adjust data

## Table of contents

1. [Activity: From one type to another](#activity-from-one-type-to-another)
   - [Check and change data type](#check-and-change-data-type)
   - [Convert temperatures from Fahrenheit to Celsius](#convert-temperatures-from-fahrenheit-to-celsius)
2. [Data validation](#data-validation)
3. [Conditional formatting](#conditional-formatting)
4. [Transform data with SQL](#transform-data-with-sql)
5. [Import and combine data: Spreadsheets](#import-and-combine-data-spreadsheets)
6. [Import and combine data: SQL](#import-and-combine-data-sql)
7. [Activity: Merge text strings to gain insights](#activity-merge-text-strings-to-gain-insights)
8. [Activity: Combine multiple pieces of data](#activity-combine-multiple-pieces-of-data)
9. [Activity: Strings in spreadsheets](#activity-strings-in-spreadsheets)
10. [Concatenate strings with SQL](#concatenate-strings-with-sql)
11. [SQL query recap](#sql-query-recap)
12. [When you get stuck](#when-you-get-stuck)
13. [Module 2 Glossary](#module-2-glossary)

---

## Activity: From one type to another

### Check and change data type

For this activity, I received the *Movie Data Start Project* spreadsheet, which can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1y-QBpy_q4mQuFM2nJhIROBKAn6fkPZ7pKo6KxQF8k0Q/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c05m02-1-type-to-another/c05m02-movie-project-data.xlsx). In Google Sheets, I performed the following actions to check and change the data type:

- selected column M **Budget ($)**
- selected column N **Box Office Revenue ($)**,
- in the Format menu, confirmed that both these columns were formatted as a number type,
- select the currency shortcut key *$* from the toolbar.

Columns M and N are now formatted as a currency type. The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/19SPXE3fn6MOuw1kk7RkWbbeReOombH_Z4og88vuPV4s/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c05m02-1-type-to-another/c05m02-movie-project-activity.xlsx).

### Convert temperatures from Fahrenheit to Celsius

I am using the CONVERT function to change units of measurement. The supplied weather data table can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1PLS2GIP2S4KMKXcAb_QKNpGAIgcr2ycZQHrPBweJ1io/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c05m02-1-type-to-another/c05m02-weather-convert-data.xlsx). In Google Sheets, I followed the following steps:

- update the heading in B1 to **Temperature (F)**,
- add the heading **Temperature (C)** in F1,
- enter the formula `=CONVERT(B2, "F", "C")` in F2, where *start_unit* is Fahrenheit (F) and *end_unit* is Celsius (C),
- fill the formula down in column F,
- add the heading `Wind Speed (m/s)` in G1,
- update the heading in D1 to **Wind Speed (mph)**,
- enter the formula `=CONVERT(D2, "mph", "m/s")` in G2, where *start_unit* is miles per hour (mph) and *end_unit* is meters per second (m/s),
- fill the formula down in column G.

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1_sHMu_OrtmZ-kebC25cCbONU3LG4PVan0xHMnxEtHhQ/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c05m02-1-type-to-another/c05m02-weather-convert-activity.xlsx).

---

## Data validation

Data validation lets you control what can and can't be entered in a worksheet using a drop-down list with predefined options, ensuring data integrity and consistency. By giving users a set of options to choose from, data entry is simplified and errors reduced. Data validation saves time and effort in data cleaning, whilst also protecting the integrity of your data and ensuring consistency across your spreadsheet.

---

## Conditional formatting

Conditional formatting is a spreadsheet tool that changes how cells appear when values meet specific conditions. By combining conditional formatting and data validation, you can enhance the readability and clarity of your spreadsheets. They provide a visual representation of key data points, making it easier to track progress and deadlines. Examples of use cases:

- Visualizing task status from a predefined dropdown list with different colors allows for quick identification of task progress within a project
- Track upcoming project deadlines by first ensuring only valid dates are entered, and secondly applying conditional formatting to highlight cells containing dates after today's date to indicate upcoming deadlines

---

## Transform data with SQL

CAST is the most common conversion function in SQL and the basic syntax is:

```sql
CAST(expression AS typename)

-- Example converting a number to a string
SELECT CAST(MyCount AS STRING) FROM MyTable

-- Example converting a date to a datetime
SELECT CAST (MyDate AS DATETIME) FROM MyTable

```

To avoid errors in the event of a failed query, use the SAFE_CAST function in BigQuery which will return a value of Null instead of an error when a query fails. The syntax for SAFE_CAST is the same as for CAST. Other SQL distributions often have their own functions or variations for safe casting, such as TRY_CAST in SQL Server and Azure SQL Database.

Other SQL conversion functions are:

- COERCION to work with big number
- UNIX_DATE returns the number of days that have passed since 1 January 1970 and is used to compare and work with dates across multiple timezones

---

## Import and combine data: Spreadsheets

In Course 3 module 3 entitled [Database Essentials](/3-Prepare-Data-for-Exploration/3-Database-essentials.md), various methods to import data into spreadsheets were covered in:

- Activity: Import data, and
- Activity: Dynamic imports.

To combine data in spreadsheets, use the CONCATENATE function to combine two or more text strings, adding spaces where needed using quotation marks.

---

## Import and combine data: SQL

SQL does not possess a single dedicated function for directly importing data from external files like CSV. While most Database Management Systems (DBMS) provide built-in tools or wizards for this purpose, specific database systems offer commands for importing data from files:

- LOAD DATA INFILE (MySQL)
- COPY (PostgreSQL)
- BULK INSERT (SQL Server)

To manipulate and move data within the same database, the `INSERT INTO ... SELECT` statement is employed. This versatile command allows you to copy data from one table to another, enabling data manipulation and selection based on specified conditions. The basic syntax is:

```sql
INSERT INTO destination_table_name
SELECT column_names -- separated by commas, or * for all columns
FROM source_table_name
WHERE condition;
```

In SQL, use the CONCAT function to join strings together to create new text strings. The basic syntax is:

```sql
SELECT CONCAT(field1, " ", field2)
FROM table_name;

/* Use AS to assign an ALIAS to your combined fields
   to help with readability */

SELECT CONCAT(first_name, " ", last_name) AS Customer_Name
FROM table_name;
```

---

## Activity: Merge text strings to gain insights

Using the public dataset `new_york` and table `citibike_trips`, we will use the SQL function CONCAT function to combine strings from multiple columns to create a new column. The full path of the database and table we will use is `bigquery-public-data.new_york.citibike_trips`. To create the query, I use the following:

- SELECT to display `usertype`, which will be either "customer" or "subscriber",
- CONCAT to create a new field `route` by combining the names of the start station with the end station,
- COUNT to calculate the number of trips on each route as `num_trips`,
- AVG to calculate the average route duration as `duration`,
- GROUP BY clause to partition the dataset into groups so the aggregate functions (COUNT, AVG) can operate within these groups,
- ORDER BY to sort the data by the number of trips for each route,
- LIMIT to restrict the number of rows returned by the query, improving performance and making it easier to explore and analyze large datasets.

The query I execute is as follows:

```sql
SELECT
  usertype,
  CONCAT (start_station_name," to ", end_station_name) AS route, 
  COUNT (*) as num_trips,
  ROUND(AVG(cast(tripduration as int64)/60),2) AS duration 
FROM 
  `bigquery-public-data.new_york.citibike_trips`
GROUP BY
  start_station_name, end_station_name, usertype 
ORDER BY 
  num_trips DESC 
LIMIT 10;
```

The query returns a summary table displaying the 10 routes with the highest amount of trips, as shown below:

![New York Citibike Route Query Results](/activities/sql/c05m02-ny-citibike-query-results.png 'New York Citibike Route Query Results')

---

## Activity: Combine multiple pieces of data

In this activity, I used the CONCAT and CONCATENATE functions in spreadsheets to combine multiple pieces of data to understand the difference between them. The spreadsheets used for this purpose can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1OyvzEv5nEdaBivJOonGSH-v7mpNhJz5LR3X0H4t09XA/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m02-combine-data/c05m02-concat-function-data.xlsx). In Google Sheets, I take the following steps:

- in cell F2, I enter the function `=CONCAT(A2,B2)` to combine the **First** and **Last** columns and copy the function down (*note that the two strings have been joined in the order that they have been entered in the function and no space was inserted between them*)
- in cell G2, I enter the function `=CONCATENATE(A2," ",B2)` to combine the **First** and **Last** columns and copy the function down (*note that the two strings have joined with a space inserted as string between them*)
- in cell H2, I enter the function `=CONCATENATE(D2," ",C2," ",E2)` to combine the `Day`, `Month` and `Year` columns with spaces between all strings to further illustrate how multiple strings can be joined with CONCATENATE.

CONCAT can be used to concatenate only two values and is equivalent to the `&` operator. If you would like to join multiple strings, CONCATENATE is the function to use. The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1N2NnTuOXe7uVrMRQiekGZOAAdTw82ObmejUN887ZspQ/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m02-combine-data/c05m02-concat-function-activity.xlsx). Below is a preview of the combined data:

![CONCAT and CONCATENATE functions](/activities/spreadsheets/c05m02-combine-data/c05m02-concat-function-activity.png 'CONCAT and CONCATENATE functions')

---

## Activity: Strings in spreadsheets

The purpose of this activity is to demonstrates the LEN, LEFT, RIGHT, and FIND functions to isolate specific characters in a string. The spreadsheet used for this purposes can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/16xmK3pTHhYIxy1sTTcgpMicMpabxIlleMi70T9twp7Q/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m02-strings-spreadsheets/c05m02-citi-bike-trip-data.xlsx). In Google Sheets, I proceed with the following:

- used the *Convert to table* feature to apply automatic formatting
- in cell B2, I enter the function `=LEFT(C2)` to calculate the length of the string in column C for start time, which is copied down the entire column
- all strings in column C are 19 characters except for one line which is 18, which can now be filtered and fixed
- insert a new column D and in cell D2, I enter the function `=FIND(" ", C2)` to find the position of the space character in the string
- the position of the space character for every string in column C is 11 so the timestamp substring will start at character 12
- insert a new column E and in cell E2, I enter the function `=RIGHT(C2, 8)` to return the eight rightmost characters in the string
- filtering the data, I can quickly see that one of the strings start with a space and fix it
- insert a new column F and in cell F2, I enter the function `=LEFT(C2, 10)` to return the ten leftmost characters in the string that represents the date

The completed activity can be be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1wksATfSOHKscPceqgt3M8TfpgJERrUtNl6IIenenouE/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m02-strings-spreadsheets/c05m02-citi-bike-trip-activity.xlsx). I have highlighted the cells that have been identified with inconsistent formatting and include a preview below:

![Bike Trip activity](/activities/spreadsheets/c05m02-strings-spreadsheets/c05m02-citi-bike-trip-activity.png 'Bike Trip activity')

---

## Concatenate strings with SQL

 It is useful to join strings together to create new text strings This allows the creation of new variables or features for data analysis, as well as more readable and informative output.

| Function / Operator | Use | Example | Result |
| --- | --- | --- | --- |
| **CONCAT** | Concatenate strings to create new text strings | `CONCAT('Google', '.com')` | `Google.com` |
| **CONCAT_WS** | Concatenate two or more strings together with a separator between each string | `CONCAT_WS(' . ', 'www', 'google', 'com')` | `www.google.com` |
| **\|\|** | Concatenate two or more strings together with the \|\| operator | `'Google' \|\| '.com'` | `Google.com` |

---

## SQL query recap

| Term | Definition |
| --- | --- |
| **ROUND** | Limit records to a certain number of decimal places |
| **CONVERT** | Change the unit of measurement of a value in data |
| **JOIN** | Combine rows from two or more tables based on a related column |
| **LIMIT** | Return a certain number of records |
| **CONCAT** | Add strings together to create new text strings that can be used as unique keys |
| **LEN**| Return the length of a string of text by counting the number of characters it contains |
| **LEFT**| Return a set number of characters from the left side of a text string |
| **FIND**| Locate specific characters in a string |
| **RIGHT**| Return a set number of characters from the right side of a text string |

---

## When you get stuck

- Reach out to your peers and mentors for help, as they can offer different perspectives and solutions. They may even have encountered and solved a similar problem before.
- Online resources are incredibly valuable and a simple search can lead you to forums such as [Stack Overflow](https://stackoverflow.com/) and tutorials with solutions to common problems. There's a combination of best practices that you can use to guide your search for answers online:
  - Practice thinking and problem-solving skills
  - Use the right data analytics terms and analysis tools
  - Use your basic knowledge of analysis tools

---

## Module 2 Glossary

| Term | Definition |
| --- | --- |
| **ROUND** | A SQL function that returns a number rounded to a certain number of decimal places |

---

Continue to next module: [Aggregate data for analysis](/5-Analyze-Data-to-Answer-Questions/3-Aggregate-data-for-analysis.md)
