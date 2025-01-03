# Aggregate data for analysis

## Table of contents

1. [What is data aggregation?](#what-is-data-aggregation)
2. [Data preparation with VLOOKUP](#data-preparation-with-vlookup)
3. [Activity: Use VLOOKUP to perform a task](#activity-use-vlookup-to-perform-a-task)
4. [Module 3 Glossary](#module-3-glossary)

---

## What is data aggregation?

***Data aggregation*** is the process of gathering data from multiple sources in order to combine it into a single summarized collection. It can help data analysts:

- identify trends
- make comparisons
- gain insights

that wouldn't be possible if each of the data elements were analyzed on its own.

---

## Data preparation with VLOOKUP

VLOOKUP (Vertical Lookup) is a spreadsheet function that searches for a specific value in a column and returns corresponding information. VLOOKUP can be a very useful data-cleaning tool in that it can help you identify these common data inconsistencies that needs to be cleaned:

- *Different Data Types*: VLOOKUP won't be able to find a match if the data types do not match - you can use the VALUE function to convert text strings representing numbers to numerical values.
- *Extra Spaces*: Just one extra space can cause VLOOKUP not to recognize a match - you can use the TRIM function to remove leading or trailing spaces.
- *Duplicates*: VLOOKUP will only identify the first match it finds in the reference table - utilize the "Remove Duplicates" tool to eliminate duplicate entries.

In order for VLOOKUP work correctly, your data needs to be formatted correctly and cleaned. When VLOOKUP is used on clean data, it can be used to combine data from different spreadsheets.

---

## Activity: Use VLOOKUP to perform a task

The purpose of this activity is to practice cleaning data and using VLOOKUP to consolidate information between two spreadsheet tabs. The analysis is completed by creating a pivot table. My analysis of the activity **Calculate weekly pay for employees** can be viewed [here](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-analysis.md).

---

## Module 3 Glossary

| Term | Definition |
| --- | --- |
| **Absolute reference** | A reference within a function that is locked so that rows and columns won’t change if the function is copied |
| **Aggregation** | The process of collecting or gathering many separate pieces into a whole |
| **Aliasing** | Temporarily naming a table or column in a query to make it easier to read and write |
| **COUNT DISTINCT** | A SQL function that only returns the distinct values in a specified range |
| **Data aggregation** | The process of gathering data from multiple sources and combining it into a single, summarized collection |
| **INNER JOIN** | A SQL function that returns records with matching values in both tables |
| **JOIN** | A SQL function that is used to combine rows from two or more tables based on a related column |
| **LEFT JOIN** | A SQL function that will return all the records from the left table and only the matching records from the right table |
| **LIMIT** | A SQL clause that specifies the maximum number of records returned in a query |
| **MATCH** | A spreadsheet function used to locate the position of a specific lookup value |
| **OUTER JOIN** | A SQL function that combines RIGHT and LEFT JOIN to return all matching records in both tables |
| **RIGHT JOIN** | A SQL function that will return all records from the right table and only the matching records from the left |
| **Subquery** | A SQL query that is nested inside a larger query |
| **VALUE** | A spreadsheet function that converts a text string that represents a number to a numeric value |

---

Continue to next module: [Perform data calculations](/5-Analyze-Data-to-Answer-Questions/4-Perform-data-calculations.md)
