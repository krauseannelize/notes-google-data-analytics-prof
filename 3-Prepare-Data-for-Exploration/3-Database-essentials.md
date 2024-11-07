# Database essentials

## Table of contents

1. [Work with databases](#work-with-databases)
2. [Metadata](#metadata)
3. [Activity: Inspect a dataset](#activity-inspect-a-dataset)
4. [Module 3 Glossary](#module-3-glossary)

---

## Work with databases

***Databases*** store and organize data in tables with information. A ***relational database*** is a database that contains a series of tables that can be connected to form relationships. Here is a sample database structure:

![Database Structure](/images/database-structure.png 'Database Structure')

For two tables to have a relationship, one or more of the same fields must exist inside both tables which are called primary or foreign keys. A ***primary key*** is an identifier that references a column in which each value is unique. A ***foreign key*** is a field within a table that is a primary key in another table. A table can have only one primary key, but it can have multiple foreign keys.

Some tables such as the revenue table above do not require a primary key, but have multiple foreign keys instead. An alternative primary key, called a  ***composite key***, can be created by combining two or more columns together that uniquely identify a row in a database table. For example:

- `Author ID` can be associated with multiple books
- `Title ID` can be associated with multiple authors
- The combination of `Author ID` and `Title ID` uniquely identifies a specific book.

***Structured Query Language (SQL)*** is the tool that enables data analysts to interact with relational databases using queries to extract specific information.

---

## Activity: Inspect a dataset

In this activity, we are guided through the process of inspecting a dataset to determine whether the data provided is sufficient to answer stakeholder questions. My analysis of the activity **"Inspect a dataset"** can be viewed [here](/activities/spreadsheets/c03m03-ice-cream-sales-analysis.md).

---

## Metadata

***Metadata*** is data about data. In database management, metadata provides information about other data and helps data analysts interpret the contents of the data within a database.

---

## Module 3 Glossary

| Term | Definition |
| --- | --- |
| **Administrative metadata** | Metadata that indicates the technical source of a digital asset |
| **CSV (comma-separated values) file** | A delimited text file that uses a comma to separate values |
| **Data governance** | A process for ensuring the formal management of a company’s data assets |
| **Descriptive metadata** | Metadata that describes a piece of data and can be used to identify it at a later point in time |
| **Foreign key** | A field within a database table that is a primary key in another table (Refer to primary key) |
| **FROM** | The section of a query that indicates where the selected data comes from |
| **Geolocation** | The geographical location of a person or device by means of digital information |
| **Metadata** | Data about data |
| **Metadata repository** | A database created to store metadata |
| **Naming conventions** | Consistent guidelines that describe the content, creation date, and version of a file in its name |
| **Normalized database** | A database in which only related data is stored in each table |
| **Notebook** | An interactive, editable programming environment for creating data reports and showcasing data skills |
| **Primary key** | An identifier in a database that references a column in which each value is unique (Refer to foreign key) |
| **Redundancy** | When the same piece of data is stored in two or more places |
| **Schema** | A way of describing how something, such as data, is organized |
| **SELECT** | The section of a query that indicates the subset of a dataset |
| **Structural metadata** | Metadata that indicates how a piece of data is organized and whether it is part of one or more than one data collection |
| **WHERE** | The section of a query that specifies criteria that the requested data must meet |
| **World Health Organization** | An organization whose primary role is to direct and coordinate international health within the United Nations system |

---

Continue to next module: [Organize and protect data](/3-Prepare-Data-for-Exploration/4-Organize-and-protect-data.md)
