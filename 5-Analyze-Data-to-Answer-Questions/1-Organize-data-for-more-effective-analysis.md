# Organize data for more effective analysis

## Table of contents

1. [Data analysis](#data-analysis)
2. [Organize data for analysis](#organize-data-for-analysis)
3. [Activity: Filter and sort data with SQL](#activity-filter-and-sort-data-with-sql)
4. [Activity: Use the SORT function in spreadsheets](#activity-use-the-sort-function-in-spreadsheets)
5. [Sort and filter in spreadsheets](#sort-and-filter-in-spreadsheets)
6. [Activity: SQL sorting queries](#activity-sql-sorting-queries)
7. [Activity: Analyze weather data in BigQuery](#activity-analyze-weather-data-in-bigquery)
8. [Module 1 Glossary](#module-1-glossary)

---

## Data analysis

***Data analysis*** is used to make sense of collected data, identify trends, and relationships to answer specific questions. To do this, you should stick to the 4 phases of analysis:

| Phase | Example: Buying a wedding gift |
| --- | --- |
| **Organize data** | Gift registry is like an organized dataset |
| **Format and adjust data** | Filter prices to include gifts that are within your budget |
| **Get input from others** | Wedding guests collaborate by marking off what they bought so you can inform yourself what not to buy |
| **Transform data** | Identifying relationships and patterns between the data points, you chose, purchased, and sent a gift that would answer the problem (liked gift that fits budget and that wasn’t already purchased) you wanted to solve |

---

## Organize data for analysis

Keeping your data organized, whether you're using a spreadsheet or a database, significantly impacts your findings as it clarifies data classification and structure. Organized data enables you to easily capture and collect the information needed for analysis. Sorting arranges data in a meaningful order, while filtering displays only data that meets specific criteria. Combining filtering and sorting allows for organizing only relevant data for analysis.

---

## Activity: Filter and sort data with SQL

In this activity, we are create a custom BigQuery dataset and use SQL queries to filter and sort data. My summary of the activity can be viewed [here](/activities/sql/c05m01-filter-data-with-sql/c05m01-filter-data-with-sql.ipynb).

---

## Activity: Use the SORT function in spreadsheets

In this activity, I learnt how to use the SORT function to arrange data into a meaningful order to make it easier to understand, analyze, and visualize. I was supplied with a spreadsheet containing a party plan that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1OyvzEv5nEdaBivJOonGSH-v7mpNhJz5LR3X0H4t09XA/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m01-sort-function/c05m01-sort-function-data.xlsx).

In Google Sheets, I enter the formula `=SORT(A2:D6, 2, TRUE)` in cell G1, which can be broken down as follows:

- cell range to sort: A2:D6
- column by which the data will be sorted: 2 (Table Number)
- sort ascending: TRUE (FALSE would sort descending)

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1cDrBynS2p9GU2EdAuQ9KghY_WqHrfzfRvKRDR_hje9M/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m01-sort-function/c05m01-sort-function-activity.xlsx).

---

## Sort and filter in spreadsheets

Both Google Sheets and Microsoft Excel allow you to sort data alphabetically or numerically, helping you identify trends and patterns Filtering lets you narrow down your data to focus on specific information that meets your criteria. You can do this with functions or by using menus and buttons.

| Task | Google Sheets function | Excel function |
| --- | --- | --- |
| Sorting | SORT | SORT and SORTBY |
| Filtering | FILTER | FILTER |

---

## Activity: SQL sorting queries

We use a large public dataset that reports statistics for live births occurring within the United States to U.S. residents as recorded by the Centers for Disease Control and Prevention (CDC). My summary of the activity can be viewed [here](/activities/sql/c05m01-sql-sorting-queries/c05m01-sql-sorting-queries.ipynb).

---

## Activity: Analyze weather data in BigQuery

Using a public dataset that contains global summaries of the day (GSOD) from the National Oceanic and Atmospheric Administration (NOAA), we will clean, prepare, and analyze a dataset whereafter the results will be saved as a new table. My summary of the activity can be viewed [here](/activities/sql/c05m01-analyze-weather-data/c05m01-analyze-weather-data.ipynb).

---

## Module 1 Glossary

| Term | Definition |
| --- | --- |
| **ORDER BY** | A SQL clause that sorts results returned in a query |

---

Continue to next module: [Format and adjust data](/5-Analyze-Data-to-Answer-Questions/2-Format-and-adjust-data.md)
