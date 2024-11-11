# Database essentials

## Table of contents

1. [Work with databases](#work-with-databases)
2. [Activity: Inspect a dataset](#activity-inspect-a-dataset)
3. [Metadata](#metadata)
    - [Types of metadata](#types-of-metadata)
    - [Elements of metadata](#elements-of-metadata)
    - [Benefits of metadata](#benefits-of-metadata)
    - [Metadata repositories](#metadata-repositories)
    - [Metadata of external databases](#metadata-of-external-databases)
    - [Manage data with metadata](#manage-data-with-metadata)
4. [Activity: Import data](#activity-import-data)
5. [Activity: Dynamic imports](#activity-dynamic-imports)
6. [Activity: Clean data with sorting and filtering](#activity-clean-data-with-sorting-and-filtering)
7. [Get started with SQL](#get-started-with-sql)
8. [Activity: BigQuery in action](#activity-bigquery-in-action)
9. [Activity: Intro to BigQuery](#activity-intro-to-bigquery)
10. [Module 3 Glossary](#module-3-glossary)

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

***Metadata*** is data about data. In database management, metadata provides information about other data and helps data analysts interpret the contents of the data within a database. Examples include details embedded in digital photos (like date, time, location) or email headers (sender, recipient, subject).

### Types of metadata

| Type | This type of metadata: | Example |
| --- | --- | --- |
| **Descriptive** | Describes a piece of data for identification | The ISBN, author and title of a book |
| **Structural** | Indicates how data is organized, if it’s part of a collection and keeps track of the relationship between two things | How pages of a book form chapters or the digital book manuscript was actually the original version of a now printed book |
| **Administrative** | Indicates the technical source of a digital asset | File type, date, and time a photo was taken |

### Elements of metadata

| Element | Type of information |
| --- | --- |
| **File or document type** | What type of file or document are you examining? |
| **Date, time, and creator** | When was it created? Who created it? When was it last modified? |
| **Title and description** | What is the name of the item you are examining? What type of content does it contain? |
| **Geolocation** | If you’re examining a photo, where was it taken? |
| **Tags and categories** | What is the general overview of the item that you have? Is it indexed or described in a specific way? |
| **Who last modified it and when** | Were any changes made to the file? If yes, when were the most recent modifications made? |
| **Who can access or update it** | If you’re examining a dataset, is it public? Are special permissions needed to customize or modify it? |

### Benefits of metadata

- **Reliability:** Provides context on how and when data was collected, and how it's structured, making data more interpretable and usable.
- **Consistency:** Ensure data consistency and uniformity, which allows data analysts to compare data, discover relationships, organize, classify and access data, therefore improving efficiency and accuracy of analyses.

### Metadata repositories

Used to store metadata, these repositories describe the state and location of the metadata, the structure of the tables inside it, and who has accessed the repository. Data analysts use metadata repositories to ensure that they use the right data appropriately.

### Metadata of external databases

Data analysts use second-party and third-party data, which necessitates understanding the metadata to ensure consistency and reliability. It's crucial to confirm data reliability and obtain necessary permissions before using data from external sources.

### Manage data with metadata

Metadata is crucial for data analysts to maintain a single source of truth, ensuring data is accurate, precise, relevant, and timely. Metadata is stored centrally, providing standardized information about all data, including location and interconnections between systems.

Data governance ensures the formal management of a company's data assets, addressing security, privacy, integrity, usability, and data flows. Metadata specialists organize and maintain data quality, create standards, and make data accessible, playing a vital role in various organizations.

---

## Activity: Import data

In this activity, we were guided through the step of importing data into a spreadsheet by using:

- a comma separated values (.csv) file
- downloading a dataset

We were provided with a .csv file that can be access here: [Entertainment expenses](/activities/spreadsheets/c03m03-import-data-entertainment-expenses.csv). The second dataset could be downloaded by navigating to the [Global Health Observatory workforce statistics database](https://www.who.int/data/gho/data/themes/topics/health-workforce) and this downloaded .csv file can be access here: [Medical doctors](/activities/spreadsheets/c03m03-import-data-medical-doctors.csv).

I imported both datasets into one spreadsheet in two separate sheets called "entertainment-expenses" and "medical-doctors". The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1tEP0zSugQhcVzTAB_GoMyCbEIMiDZiu3lqDXrFdmm9Y/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c03m03-import-data-activity.xlsx).

---

## Activity: Dynamic imports

This section contains information on methods how to import data dynamically into Google Sheets. Automated data imports do not need to be updated continually. In Google Sheets, I took the following steps to import data dynamically:

- opened a new spreadsheet and renamed the first sheet "import-range"
- used the function `=IMPORTRANGE("https://docs.google.com/spreadsheets/d/1tEP0zSugQhcVzTAB_GoMyCbEIMiDZiu3lqDXrFdmm9Y/edit?usp=sharing", "medical-doctors!A1:AH12776")` to import the medical doctors dataset from the [previous activity](#activity-import-data) into the "import-range" sheet
- created a sheet called "import-html"
- used the function `=IMPORTHTML("https://www.worldometers.info/world-population/population-by-country/", "table", 1)` to import publicly available information [Countries in the world by population (2024)](https://www.worldometers.info/world-population/population-by-country/) into the "import-html" sheet
- created a sheet called "import-data"
- use the function `=IMPORTDATA("https://drive.google.com/uc?id=1zO8ekHWx9U7mrbx_0Hoxxu6od7uxJqWw&export=download")` to import the publicly available "customers-100.csv" file from [Datablist](https://www.datablist.com/learn/csv/download-sample-csv-files)

The completed activity with the automated data imports can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1H8MVgdceqhyE-Q8MOGwNt0CtrOeY2C-yO3AgPOzGb28/edit?usp=sharing).

---

## Activity: Clean data with sorting and filtering

In this activity, we used sorting and filtering to clean up a dirty dataset. Cleaning data is of critical importance because an analysis based on dirty data can lead to wrong conclusions and bad decisions. The cleaner your data, the better your results. My analysis of the activity **Clean data with sorting and filtering** can be viewed [here](/activities/spreadsheets/c03m03-student-performance-analysis.md).

---

## Get started with SQL

- [BigQuery](https://cloud.google.com/bigquery/docs/sandbox#limits)
- [MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/)
- [Microsoft SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/tutorial-getting-started-with-the-database-engine?view=sql-server-ver15)
- [PostgreSQL](https://www.postgresql.org/docs/10/tutorial-start.html)
- [SQLite](https://www.sqlite.org/quickstart.html)

---

## Activity: BigQuery in action

This activity is an introduction to Google Cloud's BigQuery and how to use it. We are guided through the process of accessing a large public database and writing a SQL query to filter a small subset of the data. My summary of the activity can be viewed [here](/activities/sql/c03m03-bigquery-in-action.ipynb).

---

## Activity: Intro to BigQuery

In this activity, we are familiarized with writing queries in the BigQuery interface and to use SQL queries to answer questions. My summary of the activity can be viewed [here](/activities/sql/c03m03-intro-to-bigquery.ipynb).

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
