# Aggregate data for analysis

## Table of contents

1. [What is data aggregation?](#what-is-data-aggregation)
2. [Data preparation with VLOOKUP](#data-preparation-with-vlookup)
3. [Activity: Use VLOOKUP to perform a task](#activity-use-vlookup-to-perform-a-task)
4. [Activity: Explore how JOINs work](#activity-explore-how-joins-work)
5. [Aliasing in SQL](#aliasing-in-sql)
6. [SQL JOINs](#sql-joins)
7. [Activity: Queries for JOINs](#activity-queries-for-joins)
8. [Activity: COUNT and COUNT DISTINCT](#activity-count-and-count-distinct)
9. [Activity: Queries within queries](#activity-queries-within-queries)
10. [Activity: Use subqueries to refine data](#activity-use-subqueries-to-refine-data)
11. [Activity: Use subqueries to aggregate data](#activity-use-subqueries-to-aggregate-data)
12. [Review subqueries](#review-subqueries)
13. [Activity: Use subqueries](#activity-use-subqueries)
14. [Module 3 Glossary](#module-3-glossary)

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

## Activity: Explore how JOINs work

In this activity, I am exploring the four main types of SQL joins and how they combine data from multiple tables based on a primary key from one table and a foreign key from another table. My analysis of the activity **Explore how JOINs work** can be viewed [here](/activities/sql/c05m03-explore-joins/c05m03-joins-analysis.ipynb).

---

## Aliasing in SQL

***Aliasing*** in SQL allows you to give tables or columns a temporary, more readable name within a query. Aliases are implemented by making use of the AS command and the basic syntax is:

```sql
SELECT column_name AS column_alias
FROM table_name AS table_alias;
```

Some SQL databases do not support the AS command and in these cases you can leave it using this alternate syntax:

```sql
SELECT column_name column_alias
FROM table_name table_alias;
```

Queries will run with or without using the AS command for aliasing, but using AS makes your queries more readable.

---

## SQL JOINs

A ***JOIN*** combines tables by using a primary or foreign key to identify relationships and aligning corresponding values across tables. **Primary keys** reference columns in which each value is unique to that table, and **foreign keys** are values in a table that match primary key values in another table thus creating a link between the two tables. The general JOIN syntax is:

```sql
SELECT
    table_one.column_name
    table_two.column_name
FROM
    table_one
JOIN
    table_two
ON table_one.column_name = table_two.column_name
-- primary_key = foreign_key
```

The four main types of SQL joins are and work function as follows:

![SQL JOINs](/images/sql-joins.png 'SQL JOINs')

| JOIN | Definition |
| --- | --- |
| **INNER** | Returns records from the left/first table that match with values in the right/second table |
| **LEFT** | Returns all records from the left/first table and only records from the right/second table that match |
| **RIGHT** | Returns all records from the right/second table and only records from the left/first table that match |
| **OUTER** | Returns all records from the left/first table and all records from the right/second table |

---

## Activity: Queries for JOINs

The purpose of this activity is to practice writing queries that join multiple tables and using aliasing to make queries more readable. My analysis of the activity **Queries for JOINs** can be viewed [here](/activities/sql/c05m03-queries-for-joins/c05m03-queries-for-joins-activity.ipynb).

---

## Activity: COUNT and COUNT DISTINCT

In this activity, I explore COUNT and COUNT DISTINCT to understand the difference between these functions and how to use them to determine the amount of things. My analysis of the activity **COUNT and COUNT DISTINCT** can be viewed [here](/activities/sql/c05m03-count-distinct/c05m03-count-distinct-activity.ipynb).

---

## Activity: Queries within queries

The purpose of this activity is to introduce another SQL query: subqueries. A ***subquery*** is a SQL query that is nested inside of a larger query. They let you combine logic from different queries, making your code more efficient and readable.My analysis of the activity **Queries within queries** can be viewed [here](/activities/sql/c05m03-queries-within-queries/c05m03-queries-within-queries-activity.ipynb).

---

## Activity: Use subqueries to refine data

In this activity, I will practice using SELECT statements with FROM, WHERE, and GROUP BY clauses to build subqueries and analyzing the query’s results. My analysis of the activity **Use subqueries to refine data** can be viewed [here](/activities/sql/c05m03-subqueries-to-refine/c05m03-subqueries-to-refine-activity.ipynb).

---

## Activity: Use subqueries to aggregate data

The objective of this query is practice data aggregation with SQL joins combined with subqueries and using a CASE statement to add a classification column. My analysis of the activity **Use subqueries to aggregate data** can be viewed [here](/activities/sql/c05m03-subqueries-to-aggregate/c05m03-subqueries-to-aggregate-activity.ipynb).

---

## Review subqueries

- Subqueries are usually nested in the SELECT, FROM, WHERE and/or HAVING clauses.
- Subqueries can also be nested inside INSERT, UPDATE or DELETE statements.
- The statement containing a subquery is an outer query or outer select. Subqueries are nested within these statements, called inner queries or inner select.
- The innermost query executes first. Its parent query executes last so it can use the results returned by inner queries.
- Parentheses are used to mark the beginning and end of a subquery.
- Comparison operators such as >, <, or = help you compare data in subqueries and a subquery must be placed on the right side of the comparison operator.
- Subqueries that return more than one row can be handled using:
  - Multiple value operators: such as IN, ANY, or ALL
  - JOIN clauses: to combine data from the subquery with the main query.
- Subqueries can’t be nested in SET queries because it is used with UPDATE to adjust specific columns and values in a table.
- When used directly within the SELECT clause of the containing query, a subquery must typically return a single column. If a subquery needs to return multiple columns, it often needs to be nested within another subquery that isolates a single column for the outer SELECT clause.

--

## Activity: Use subqueries

Sometimes it is really useful to analyze a small subset of data that is contained within a much larger dataset. In this activity, I utilized subqueries to effectively isolate and analyze a smaller subset. My analysis of the activity can be viewed [here](/activities/sql/c05m03-use-subqueries/c05m03-use-subqueries-activity.ipynb).

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
