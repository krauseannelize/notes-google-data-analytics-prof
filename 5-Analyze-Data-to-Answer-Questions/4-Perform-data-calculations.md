# Perform data calculations

## Table of contents

1. [Conditional spreadsheet functions](#conditional-spreadsheet-functions)
2. [Activity: Work with conditions](#activity-work-with-conditions)
3. [Composite functions](#composite-functions)
4. [Activity: Explore movie data with pivot tables](#activity-explore-movie-data-with-pivot-tables)
5. [Activity: Embed simple calculations with SQL](#activity-embed-simple-calculations-with-sql)
6. [Activity: Calculations with SQL](#activity-calculations-with-sql)
7. [Data validation](#data-validation)
8. [Module 4 Glossary](#module-4-glossary)

---

## Conditional spreadsheet functions

Conditional functions are functions that perform a specific task, but only on cells that satisfy some defined criteria. They are usually identified with an IF suffix to search for a single condition or an IFS suffix to search for multiple conditions. They are frequently used when constructing more complex queries that cannot be accomplished using more basic functions.

| Basic function | Conditional version |
| --- | --- |
| COUNT | COUNTIF/COUNTIFS |
| SUM | SUMIF/SUMIFS |
| AVERAGE | AVERAGEIF/AVERAGEIFS |
| MAX | MAXIFS |
| MIN | MINIFS |

---

## Activity: Work with conditions

In this activity, I practice using conditional spreadsheet functions to understand when and why they are appropriate. This enables me to do more complex analysis with spreadsheets, especially if used in conjunction with data validation to create a dynamic summary table.  My analysis of the activity **Work with conditions** can be viewed [here](/activities/spreadsheets/c05m04-work-with-conditions/c05m04-work-with-conditions-activity.md).

---

## Composite functions

A **composite function** is created when two or more functions are combined together into a single function. **SUMPRODUCT** is a composite function that multiplies corresponding values in two or more arrays, and returns the sum of those products. An **array** is a collection of *values within cells*, whereas a **range** refers to the collection of *cells* themselves. The basic syntax is: `=SUMPRODUCT(array1, array2)`.

I will investigate the SUMPRODUCT function using a spreadsheet with data from a kitchen supply store which can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1CKxAwvN32S5NmBxNCOhoGAK7LHsDHx0JhFtBM6ODTVw/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c05m04-sumproduct/c05m04-sumproduct-data.xlsx). In Google Sheets, I do the following:

- in cell A10, enter: "Total revenue"
- in cell B10, I enter the function `=SUMPRODUCT(B3:B7,C3:C7)` that multiplies each value in cell B3 to B7 with the corresponding value in C3 to C7 and which return $655.00
- in cell A11, enter: "Profit"
- in cell B11, I enter the function `=SUMPRODUCT(B3:B7,C3:C7,D3:D7)` that again multiplies each value in cell B3 to B7 with the corresponding value in C3 to C7, but also multiplies it with each value in D3 to D7, which return $156.25

To verify the results of the SUMPRODUCT function, I add two columns to the data:

- **Amount** that contains the product of quantity and unit price for each row (`=B3*C3`) and use SUM to calculate the total in row 8, which is $655.00
- **Profit** that contains the product of quantity, unit price and profit margin for each row (`=B3*C3*D3`) and use SUM to calculate the total in row 8, which is $156.25

This illustrates how you can use a composite function to perform complex calculations efficiently. The auxiliary columns visually demonstrates the intermediate steps and verify the accuracy of the SUMPRODUCT results. Below is a preview of the spreadsheet with the formulas use highlighted in yellow:

![Total revenue and profit](/activities/spreadsheets/c05m04-sumproduct/c05m04-revenue-profit.png 'Total revenue and profit')

The functions themselves can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1gzoF22fyVF660-UmWb3PfzXt1BlhIp6cBhpQn3CNVik/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c05m04-sumproduct/c05m04-sumproduct-activity.xlsx).

---

## Activity: Explore movie data with pivot tables

A **pivot table** is a tool used to sort, reorganize, group, count, total, or average data in spreadsheets. Pivot tables allow you to compare metrics, perform calculations, and generate reports for large datasets without altering the original dataset. It has 4 basic parts: Rows, Columns, Values, and Filters.

In this activity, I navigate an example workplace scenario and will create a pivot table to answer stakeholder questions and visualize data. My analysis of the activity **Explore movie data with pivot tables** can be viewed [here](/activities/spreadsheets/c05m04-pivot-tables/c05m04-pivot-tables-activity.md).

---

## Activity: Embed simple calculations with SQL

The goal of this activity is to find the total number of bags of avocados sold on every day at each location using simple calculations with SQL. My analysis of the activity **Embed simple calculations with SQL** can be viewed [here](/activities/sql/c05m04-simple-calculations/c05m04-simple-calculations-activity.ipynb).

---

## Activity: Calculations with SQL

In this activity, I practice using the four basic arithmetic operations to perform addition, subtraction, multiplication, and division in BigQuery. Combining multiple arithmetic operations in a single query, will enable me to quickly and efficiently discover significant patterns in datasets. My analysis of the activity **Calculations with SQL** can be viewed [here](/activities/sql/c05m04-calculations-with-sql/c05m04-calculations-with-sql-activity.ipynb).

---

## Data validation

**Data validation** is the process of checking and rechecking your data to make sure it is complete, accurate, secure, and consistent. It helps to ensure the integrity of data and assures you that the data you are using is clean. The following list outlines six types of data validation:

| Type | Purpose | Example | Limitations |
| --- | --- | --- | --- |
| **Data type** | Check that the data matches the data type defined for a field | Data values for school grades 1-12 must be a numeric data type | The data value 13 would pass the data type validation but would be an unacceptable value. For this case, data range validation is also needed |
| **Data range** | Check that the data falls within an acceptable range of values defined for the field | Data values for school grades should be values between 1 and 12 | The data value 11.5 would be in the data range and would also pass as a numeric data type. But, it would be unacceptable because there aren't half grades. For this case, data constraint validation is also needed |
| **Data constraints** | Check that the data meets certain conditions or criteria for a field. This includes the type of data entered as well as other attributes of the field, such as number of characters | Content constraint: Data values for school grades 1-12 must be whole numbers | The data value 13 is a whole number and would pass the content constraint validation. But, it would be unacceptable since 13 isn’t a recognized school grade. For this case, data range validation is also needed |
| **Data consistency** | Check that the data makes sense in the context of other related data | Data values for product shipping dates can’t be earlier than product production dates | Data might be consistent but still incorrect or inaccurate. A shipping date could be later than a production date and still be wrong |
| **Data structure** | Check that the data follows or conforms to a set structure | Web pages must follow a prescribed structure to be displayed properly | A data structure might be correct with the data still incorrect or inaccurate. Content on a web page could be displayed properly and still contain the wrong information |
| **Code validation** | Check that the application code systematically performs any of the previously mentioned validations during user data input | Common problems discovered during code validation include: more than one data type allowed, data range checking not done, or ending of text strings not well defined | Code validation might not validate all possible variations with data input |

---

## Module 4 Glossary

| Term | Definition |
| --- | --- |
| **Array** | A collection of values in spreadsheet cells |
| **Calculated field** | A new field within a pivot table that carries out certain calculations based on the values of other fields |
| **Data security** | Protecting data from unauthorized access or corruption by adopting safety measures |
| **Data validation process** | The process of checking and rechecking the quality of data so that it is complete, accurate, secure and consistent |
| **GROUP BY** | A SQL clause that groups rows that have the same values from a table into summary rows |
| **Modulo** | An operator (%) that returns the remainder when one number is divided by another |
| **Profit margin** | A percentage that indicates how many cents of profit has been generated for each dollar of sale |
| **Summary table** | A table used to summarize statistical information about data |
| **SUMPRODUCT** | A function that multiplies arrays and returns the sum of those products |
| **Temporary table** | A database table that is created and exists temporarily on a database server |
| **Underscores** | Lines used to underline words and connect text characters |

---

Continue to next course: [Share Data Through the Art of Visualization](/6-Share-Data-Through-the-Art-of-Visualization/README.md)
