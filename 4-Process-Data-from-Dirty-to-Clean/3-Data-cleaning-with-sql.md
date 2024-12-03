# Data cleaning with SQL

## Table of contents

1. [When to employ SQL](#when-to-employ-sql)
2. [Processing time with SQL](#processing-time-with-sql)
3. [Module 3 Glossary](#module-3-glossary)

---

## When to employ SQL

SQL is your go-to tool for extracting data from databases. Spreadsheets and SQL both have their advantages and disadvantages:

| Features of Spreadsheets | Features of SQL Databases |
| --- | --- |
| **Smaller data sets** | Larger datasets |
| **Enter data manually** | Access tables across a database |
| **Create graphs and visualizations in the same program** | Prepare data for further analysis in another software |
| **Built-in spell check and other useful functions** | Fast and powerful functionality |
| **Best when working solo on a project** | Great for collaborative work and tracking queries run by all users |

If it's in a database, SQL is the most efficient choice. However, if your data lives in a spreadsheet, stick with spreadsheet tools.

---

## Processing time with SQL

Data is measured by the number of bits it takes to represent it. This is then described in bytes, which are equal to 8 bits.

| Unit | Abbreviation | Equivalent to | Example (with approximate size) |
| --- | --- | --- | --- |
| **Byte** | B | 8 bits | 1 character in a string (1 byte) |
| **Kilobyte** | KB | 1024 bytes | A page of text (4 kilobytes) |
| **Megabyte** | MB | 1024 Kilobytes | 1 song in MP3 format (2-3 megabytes) |
| **Gigabyte** | GB | 1024 Megabytes | 300 songs in MP3 format (1 gigabyte) |
| **Terabyte** | TB | 1024 Gigabytes | 500 hours of HD video (1 terabyte) |
| **Petabyte** | PB | 1024 Terabytes | 10 billion Facebook photos (1 petabyte) |
| **Exabyte** | EB | 1024 Petabytes | 500 million hours of HD video (1 exabyte) |
| **Zettabyte** | ZB | 1024 Exabytes | All the data on the internet in 2019 (4.5 ZB) |

The size of the dataset you’re working with usually determines which tool is best suited for the task:

- Spreadsheets often start to have performance issues as dataset sizes increase beyond a few megabytes.
- SQL databases are much better at working with larger datasets that have billions of rows with sizes measured in gigabytes.

However, even in SQL, it takes longer for queries to complete when they’re run on longer datasets, depending on the query’s content and the number of rows SQL has to process. See below how the same SQL query performs on a small dataset (415.8 GB) versus a large dataset (4.1 TB):

![SQL query speed comparison](/images/sql-query-speed.png 'SQL query speed comparison')

---

## Basic SQL queries

| Query | Definition |
| --- | --- |
| **SELECT FROM** | Pull data from any table in a database |
| **SELECT DISTINCT** | Remove duplicates and only return unique values |
| **INSERT INTO** | Add new data into a database |
| **UPDATE** | Change existing data in a database |
| **CREATE TABLE IF NOT EXISTS** | Create new tables within a database to store extracted data for future use |
| **DROP TABLE IF EXISTS** | Remove unused or old tables, ensuring the database remains organized and efficient |
| **LENGTH()/LEN()** | Return the length of a string of text by counting the number of characters it contains |
| **SUBSTR()** | Return a limited number of characters to create substrings from longer strings of text |
| **TRIM()** | Remove leading, trailing, and repeated spaces in data |

---

## Module 3 Glossary

| Term | Definition |
| --- | --- |
| **CAST** | A SQL function that converts data from one datatype to another |
| **COALESCE** | A SQL function that returns non-null values in a list |
| **CONCAT** | A SQL function that adds strings together to create new text strings that can be used as unique keys |
| **DISTINCT** | A keyword that is added to a SQL SELECT statement to retrieve only non-duplicate entries |
| **Float** | A number that contains a decimal |
| **Substring** | A subset of a text string |
| **Typecasting** | Converting data from one type to another |

---

Continue to next module: [Verify and report on cleaning results](/4-Process-Data-from-Dirty-to-Clean/4-Verify-and-report-cleaning-results.md)
