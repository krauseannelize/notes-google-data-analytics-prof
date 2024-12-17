# Organize data for more effective analysis

## Table of contents

1. [Data analysis](#data-analysis)
2. [Organize data for analysis](#organize-data-for-analysis)
3. [Activity: Filter data with SQL](#activity-filter-data-with-sql)
4. [Activity: Use the SORT function in spreadsheets](#activity-use-the-sort-function-in-spreadsheets)
5. [Module 1 Glossary](#module-1-glossary)

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

## Activity: Filter data with SQL

In this activity, we are create a custom BigQuery dataset and use SQL queries to filter data. My summary of the activity can be viewed [here](/activities/sql/c05m01-filter-data-with-sql/c05m01-filter-data-with-sql.ipynb).

---

## Activity: Use the SORT function in spreadsheets

In this activity, we learn how to use the SORT function to arrange data into a meaningful order to make it easier to understand, analyze, and visualize. We were supplied with a spreadsheet containing a party plan that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1OyvzEv5nEdaBivJOonGSH-v7mpNhJz5LR3X0H4t09XA/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m01-sort-function-data.xlsx).

In Google Sheets, I enter the formula `=SORT(A2:D6, 2, TRUE)` in cell G1, which can be broken down as follows:

- cell range to sort: A2:D6
- column by which the data will be sorted: 2 (Table Number)
- sort ascending: TRUE (FALSE would sort descending)

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1cDrBynS2p9GU2EdAuQ9KghY_WqHrfzfRvKRDR_hje9M/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m01-sort-function-activity.xlsx).

---

## Module 1 Glossary

| Term | Definition |
| --- | --- |
| **ORDER BY** | A SQL clause that sorts results returned in a query |

---

Continue to next module: [Format and adjust data](/5-Analyze-Data-to-Answer-Questions/2-Format-and-adjust-data.md)
