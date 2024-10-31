# Set up your data analytics toolbox

## Table of contents

1. [Overview](#overview)
2. [Spreadsheet basics](#spreadsheet-basics)
3. [Spreadsheet hands-on activity](#spreadsheet-hands-on-activity)
4. [Get started with SQL](#get-started-with-sql)
5. [Example SQL query](#example-sql-query)
6. [Formatting SQL queries](#formatting-sql-queries)
    - [Capitalization, indentation and semicolons](#capitalization-indentation-and-semicolons)
    - [Commenting](#commenting)
    - [Aliases](#aliases)
7. [Data visualization](#data-visualization)
    - [Steps to create meaningful data visualizations](#steps-to-create-meaningful-data-visualizations)
    - [Data visualization toolkit](#data-visualization-toolkit)
8. [Module 3 Glossary](#module-3-glossary)

---

## Overview

Spreadsheets, query languages, and data visualization tools are all a big part of a data analyst’s job. This part of the course teaches the basic concepts to use them for data analysis using interesting examples.

---

## Spreadsheet basics

This section gives a broad introduction of spreadsheets from entering data, adding labels or attributes, to organizing data by sorting it. The following resources can be consulted to learn more:

- [Google Sheets Training and Help](https://support.google.com/a/users/answer/9282959?visit_id=637361702049227170-1815413770&rd=1)
- [Google Sheets Cheat Sheet](https://support.google.com/a/users/answer/9300022)
- [Microsoft Excel for Windows Training](https://support.microsoft.com/en-us/office/excel-for-windows-training-9bc05390-e94c-46af-a5b3-d7c22f6990bb)

---

## Spreadsheet hands-on activity

In this activity, we were guided through the steps to use a spreadsheet to make a simple chart to illustrate how a simple graphical representation of information can be used to support data-driven business decisions. To highlight my analytical skills and visual communication abilities, I added aesthetic elements to the graph, making the exercise more visually appealing and insightful.

My analysis of the activity **"Generate a chart from a spreadsheet"** can be viewed [here](/1-Foundations-Data-Data-Everywhere/Activities/mod3-analysis-monthly-sales.md).

---

## Get started with SQL

A **query** is a request for data or information from a database. When you query databases, you use **SQL (Structured Query Language)** to communicate your question or request. As with every programming language, SQL follows a unique set of guidelines known as syntax. **Syntax** is the predetermined structure of a language that includes all required words, symbols, and punctuation, as well as their proper placement.

| Keyword | Purpose |
| --- | --- |
| SELECT | Choose the column(s) from which to retrieve the data. Separate multiple column names with a comma. Using an asterisk (*) will select all columns in a table |
| FROM | Choose the table from which to retrieve the data |
| WHERE | Filter the data by specifying criteria the data must meet |
| AND | Logical operator to connect conditions and all conditions separated by the AND must be true |
| OR | Logical operator to connect conditions and any of the conditions separated by the OR must be true |
| NOT | Logical operator used to display records if the condition(s) are not true |

The following resources can be consulted to learn more:

- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/default.asp)
- [SQL Cheat Sheet](https://www.sqltutorial.org/sql-cheat-sheet/)

---

## Example SQL Query

Below is an example of a SQL query selecting multiple column names from the table "customers" using multiple conditions to filter the records connected with the AND operator. Only records where both the conditions are true will be shown. Thus, the customer's first name must be "Jan" and country of residence must be "Germany", or the record will be excluded.

```sql
SELECT
    first_name,
    last_name,
    country
FROM
    customers
WHERE
    first_name = 'Jan' AND country = 'Germany'
```

The results from this query could be:

| first_name | last_name | country|
| --- | --- | --- |
| Jan | Kruger | Germany |
| Jan | Becker | Germany |
| Jan | Fischer | Germany |

---

## Formatting SQL queries

### Capitalization, indentation and semicolons

Although not strictly required, using **capitalization** and **indentation** when writing your query, will improve it's readability and make it easier to understand. You can write the entire query in lowercase without any indentation and it will execute, but it will be hard to review or troubleshoot.

```sql
/* The query below is written entirely in lowercase without any indentation and it will execute,
   but it is hard to review and troubleshoot. */

select column_name1, column_name2, column_name3 FROM table_name WHERE condition = "criteria"

/* The same query can be reformatted as indicated below using capitalization and indentation,
   which significantly improves the readability of the query. */

SELECT
    column_name1,
    column_name2,
    column_name3
FROM
    table_name
WHERE
    condition = "criteria"; -- semicolon clearly indicates the end of the query

```

Semicolons are statement terminators used at the end of a query to indicate the end of the query. Although it is not mandatory, some versions of SQL do require it so it is recommended to use a semicolon as statement terminators at the end of every query for better compatibility and clarity.

### Commenting

Adding comments to a SQL query can provide valuable context and additional information about data, tables or queries. This is especially important if you are working on a large person and the code will be shared with others. This will make reviewing your query and understanding its purpose much easier and faster to debug and maintain. SQL uses 2 types of comments:

- **Single-line comments** that begin with a **_double dash (--)_** and everything after it on the same line is treated as a comment.
- **Multi-line comments** that begin with a **_slash-asterisk (/\*)_** and end with an **_asterisk-slash (\*/)_**. Everything between these symbols is considered a comment, regardless of line breaks.

### Aliases

Aliases, assigned using the AS clause, provide temporary, user-friendly names for tables and columns within a query, enhancing readability without altering the actual database objects. You can, for example, temporarily rename a table or a column with a very long or unclear name something else to make your query easier to write and read:

```sql
SELECT
    this_column_contains_names_from_customers AS customer_name
    -- customer_name can now be used in the rest of the query
FROM
    a_very_long_table_name_from_a_database AS table_name
    -- table_name can now be used in the rest of the query
```

---

## Data visualization

Data visualization is the graphical representation of information that make your data easy to understand and interesting to look at. Because of its importance, most data analytics tools have a built-in visualization component while others specialize in visualization as their primary value-add.

### Steps to create meaningful data visualizations

1. Explore the data for patterns
2. Plan your visuals
3. Create your visuals
    - Line charts: Track a metric over time
    - Maps: Connect a metric to locations
    - Donut charts: Show segments
    - Bar chart: Compare metrics

### Data visualization toolkit

There are many different tools you can use for data visualization. At the end of the day, your needs and the complexity of the data will be the determining factor.

- **Spreadsheets** (like Microsoft Excel or Google Sheets) are great for smaller datasets and offer simple visualizations like bar graphs and pie charts, but also some advanced options like maps.
- **Visualization Software** (like Tableau) is a popular choice for creating interactive and visually appealing dashboards that are user-friendly and works well with large datasets.
- **Programming Languages** (like R with RStudio) offers powerful customization and control over your visualizations suitable for large datasets and complex projects.

---

## Module 3 Glossary

| Term | Definition |
| --- | --- |
| **Attribute** | A characteristic or quality of data used to label a column in a table |
| **Observation** | The attributes that describe a piece of data contained in a row of a table |

---

Continue to next module: [Become a fair and impactful data professional](/1-Foundations-Data-Data-Everywhere/4-Become-a-fair-and-impactful-data-professional.md)
