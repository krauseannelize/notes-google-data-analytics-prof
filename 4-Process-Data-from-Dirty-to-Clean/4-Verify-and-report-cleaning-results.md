# Verify and report on cleaning results

## Table of contents

1. [Verify and report results](#verify-and-report-results)
2. [The big picture](#the-big-picture)
3. [Verification of data cleaning](#verification-of-data-cleaning)
4. [Data-cleaning verification checklist](#data-cleaning-verification-checklist)
5. [Module 4 Glossary](#module-4-glossary)

---

## Verify and report results

***Verification*** is a process to confirm that a data cleaning effort was well-executed and the resulting data is accurate and reliable. This ensures that the insights gained from the analysis can be trusted for decision-making, which prevents potentially wrong business decisions or misrepresentations based on flawed insights.

Reporting on your data cleaning efforts is vital for transparency and accountability, building trust with your team and stakeholders.
It involves:

- documenting your cleaning process,
- creating data-cleaning reports, and
- using changelogs to track modifications made to the dataset over time.

---

## The big picture

Data verification involves comparing your cleaned data to the original dataset to identify and correct any remaining errors.
You can use manual checks, conditional formatting, filters, or search functions to find discrepancies and ensure data accuracy.

Another key part of verification involves taking a big-picture view of your project. It's crucial to regularly realign your analysis with the original business problem and project goals. This prevents scope creep and ensures your efforts contribute to solving the intended issue. Taking a big picture view of your project involves doing three things:

- **Consider the business problem:** Will your data actually make it possible to solve your business problem?
- **Consider the goal:** Will the data you've collected and cleaned actually help your company achieve that goal?
- **Consider the data:** Is your data capable of solving the problem and meeting the project objectives?

Doing these three things ensures data reliability and insights gained from analysis can be trusted. Sometimes when you get too familiar with your data, it is easier to miss something or make assumptions. It's helpful to get a fresh perspective from teammates to identify potential issues or biases in your data.

---

## Verification of data cleaning

### Data Verification in Spreadsheets

- The **"Find and Replace"** tool helps locate and correct specific errors, like misspellings, throughout a spreadsheet.
- **Pivot tables** summarize data, allowing you to quickly identify potential errors by, for example, incorrect counts:
  - COUNT will only count cells that contain *numeric* values
  - COUNTA counts all cells that are not empty

### Data verification in SQL

The **CASE** statement in SQL helps conditionally modify data, such as correcting a misspelling, while leaving other values unchanged. Below is an example of using the CASE statement to correct the misspelling of the name Tony:

```sql
SELECT
    Customer_id,
    CASE
    WHEN first_name = 'Tnoy' THEN 'Tony'
    ELSE first_name
    END AS cleaned_name
FROM
   project-id.customer_data.customer_name
```

:exclamation: **Note:** This query will correct the misspelled name and leave other names unchanged in a new column called "cleaned_name". It corrects only the display of the name without updating the table’s data.

---

## Data-cleaning verification checklist

Identify the most common problems and correct them:

| Problem | Correction |
| --- | --- |
| **Sources of errors** | Did you use the right tools and functions to find the source of the errors in your dataset? |
| **Null data** | Did you search for NULLs using conditional formatting and filters? |
| **Misspelled words** | Did you locate all misspellings? |
| **Mistyped numbers** | Did you double-check that your numeric data has been entered correctly? |
| **Extra spaces and characters** | Did you remove any extra spaces or characters using the TRIM function? |
| **Duplicates** | Did you remove duplicates in spreadsheets using the Remove Duplicates function or DISTINCT in SQL? |
| **Mismatched data types** | Did you check that numeric, date, and string data are typecast correctly? |
| **Messy (inconsistent) strings** | Did you make sure that all of your strings are consistent and meaningful? |
| **Messy (inconsistent) date formats** | Did you format the dates consistently throughout your dataset? |
| **Misleading variable labels (columns)** | Did you name your columns meaningfully? |
| **Truncated data** | Did you check for truncated or missing data that needs correction? |
| **Business Logic** | Did you check that the data makes sense given your knowledge of the business? |

---

## Module 4 Glossary

| Term | Definition |
| --- | --- |
| **CASE** | A SQL statement that returns records that meet conditions by including an if/then statement in a query |
| **Changelog** | A file containing a chronologically ordered list of modifications made to a project |
| **COUNTA** | A spreadsheet function that counts the total number of values within a specified range |
| **Find and replace** | A tool that finds a specified search term and replaces it with something else |
| **Verification** | A process to confirm that a data-cleaning effort was well executed and the resulting data is accurate and reliable |

---

Continue to next module: [Add data to your resume](/4-Process-Data-from-Dirty-to-Clean/5-Add-data-to-your-resume.md)
