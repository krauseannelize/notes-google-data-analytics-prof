# Clean data for more accurate insights

## Table of contents

1. [Clean data](#clean-data)
2. [Dirty data](#dirty-data)
   - [Duplicate data](#duplicate-data)
   - [Outdated data](#outdated-data)
   - [Incomplete data](#incomplete-data)
   - [Incorrect/inaccurate data](#incorrectinaccurate-data)
   - [Inconsistent](#inconsistent-data)
3. [Principles of data integrity](#principles-of-data-integrity)
4. [Data cleaning](#data-cleaning)
   - [Common techniques](#common-techniques)
   - [Common mistakes to avoid](#common-mistakes-to-avoid)
   - [Common tasks](#common-tasks)
5. [Activity: Cleaning data with spreadsheets](#activity-cleaning-data-with-spreadsheets)
6. [Data-cleaning features in spreadsheets](#data-cleaning-features-in-spreadsheets)
7. [Workflow automation](#workflow-automation)
8. [Activity: Clean data with spreadsheet functions](#activity-clean-data-with-spreadsheet-functions)
9. [Your cleaning checklist](#your-cleaning-checklist)
10. [Module 2 Glossary](#module-2-glossary)

---

## Clean data

***Clean data*** is accurate, complete, and relevant, ensuring reliable and trustworthy data analysis results. It enables analysts to uncover valuable patterns, make connections, and derive actionable insights. Working with clean data streamlines data projects and leads to more accurate insights.

---

## Dirty data

***Dirty data*** is plagued by inconsistencies, errors, and irrelevant information, which undermines the reliability of data analysis. Inaccurate data can cost businesses trillions of dollars annually, with human error being the leading cause. Types of dirty data:

### Duplicate data

| Description | Possible causes | Potential harm to businesses |
| --- | --- | --- |
| Any data record that shows up more than once | Manual data entry, batch data imports, or data migration | Skewed metrics or analyses, inflated or inaccurate counts or predictions, or confusion during data retrieval |

### Outdated data

| Description | Possible causes | Potential harm to businesses |
| --- | --- | --- |
| Any data that is old which should be replaced with newer and more accurate information | People changing roles or companies, or software and systems becoming obsolete | Inaccurate insights, decision-making, and analytics |

### Incomplete data

| Description | Possible causes | Potential harm to businesses |
| --- | --- | --- |
| Any data that is missing important fields | Improper data collection or incorrect data entry | Decreased productivity, inaccurate insights, or inability to complete essential services |

### Incorrect/inaccurate data

| Description | Possible causes | Potential harm to businesses |
| --- | --- | --- |
| Any data that is complete but inaccurate | Human error inserted during data input, fake information, or mock data | Inaccurate insights or decision-making based on bad information resulting in revenue loss |

### Inconsistent data

| Description | Possible causes | Potential harm to businesses |
| --- | --- | --- |
| Any data that uses different formats to represent the same thing | Data stored incorrectly or errors inserted during data transfer | Contradictory data points leading to confusion or inability to classify or segment customers |

---

## Principles of data integrity

| Principle | Definition | Example |
| --- | --- | --- |
| **Consistency** | The degree to which a set of measures is equivalent across systems | Date of store opening stored in both MM/DD/YYYY and MM/YY formats |
| **Completeness** | The degree to which all required measures are known | NULL/missing value for the item “Number of employees per store” |
| **Accuracy** | The degree of conformity of a measure to a standard or a true value | Addresses in the business database are identified as incorrect when compared to the public postal service database |
| **Validity** | The concept of using data integrity principles to ensure measures conform to defined business rules or constraints | Data collected five years ago used technology that is not approved or supported by the business |

---

## Data cleaning

### Common techniques

- Make a copy of the dataset
- Get rid of duplicates or data that isn't relevant to the problem you're trying to solve
- Remove extra spaces and blanks
- Fix misspellings, inconsistent capitalization, incorrect punctuation, and other typos
- Assess data compatibility before merging data

### Common mistakes to avoid

- Not checking for spelling errors
- Forgetting to document errors
- Not checking for values entered into the wrong field
- Overlooking missing values
- Only looking at a subset of the data
- Losing track of business objectives
- Not fixing the source of the error
- Not analyzing the system prior to data cleaning
- Not backing up your data prior to data cleaning
- Not accounting for data cleaning in your deadlines/process

### Common tasks

- **Determine the size of the dataset:** Large datasets may have more data quality issues and take longer to process. This may impact your choice of data cleaning techniques and how much time to allocate to the project.
- **Determine the number of categories or labels:** By understanding the number and nature of categories and labels in a dataset, you can better understand the diversity of the dataset. This understanding also helps inform data merging and migration strategies.
- **Identify missing data:** Recognizing missing data helps you understand data quality so you can take appropriate steps to remediate the problem. Data integrity is important for accurate and unbiased analysis.
- **Identify unformatted data:** Identifying improperly or inconsistently formatted data helps analysts ensure data uniformity. This is essential for accurate analysis and visualization.
- **Explore the different data types:** Understanding the types of data in your dataset (for instance, numerical, categorical, text) helps you select appropriate cleaning methods and apply relevant data analysis techniques.

---

## Activity: Cleaning data with spreadsheets

In this activity, I am guided through some steps to do data cleaning with spreadsheets, whereafter the data is transposed. I received a spreadsheet containing dirty data that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1lMYD9PHV-06u6ylP-dlX5UrBt4vofaBUg6RURx6TTvU/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c04m02-cleaning-with-spreadsheets/c04m02-cleaning-with-spreadsheets-data.xlsx). Below is a preview of the raw data before cleaning:

![Dirty Data Preview](/activities/spreadsheets/c04m02-cleaning-with-spreadsheets/c04m02-cleaning-with-spreadsheets-data.png 'Dirty Data Preview')

In Google Sheets, I took a slightly different approach to the one suggested and followed these steps to clean the data:

- Selected the entire sheet and cleared all formatting
- Select the range A1:H51 and used the *Convert to table* feature to apply automatic formatting
- Identify rows with blank values: 2, 8, 10, 16, 19 and 23
- Delete rows 2, 8 and 23
- Unit Cost in G10 is blank, but this can be calculated by dividing the Total by Units or `=H10/F10`. Insert the value 4.99 in G10
- Units in F16 is blank, but this can be calculated by dividing the Total by Unit Cost or `=H10/G10`. Insert the value 35 in F16
- Total in H19 is blank, but this can be calculated by multiplying the Units by Unit Cost or `=F19*G19`. Insert the value 251.72 in H19
- Select the entire sheet and select "Trim whitespace" from the Data tab, Data cleanup option
- Apply date formatting to column B to verify all cells contain valid dates
- Insert a new column F and used the function `=PROPER(C2)` to change all values in column C to Proper Case
- Insert a new column G and used the function `=PROPER(D2)` to change all values in column D to Proper Case
- Insert a new column H and used the function `=PROPER(E2)` to change all values in column E to Proper Case
- Copy columns F, G and H, and use paste special to paste values only remove the functions to convert to Proper Case
- Delete columns C, D and E
- Give column C (previously F) the heading **Region**
- Give column D (previously G) the heading **Name**
- Give column E (previously H) the heading **Item**
- Rename the sheet and table to **Long**
- Copy the table and use paste special to transpose the data to wide format in a new sheet and table named **Wide**

The cleaned data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1BYT0t9ptZtgtZ9AAoVsSAKBLZRr3vuBvQPuzx2gKUEA/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c04m02-cleaning-with-spreadsheets/c04m02-cleaning-with-spreadsheets-activity.xlsx). Below is a preview of the clean data:

![Clean Data Preview](/activities/spreadsheets/c04m02-cleaning-with-spreadsheets/c04m02-cleaning-with-spreadsheets-activity.png 'Clean Data Preview')

---

## Data-cleaning features in spreadsheets

Handy spreadsheet features to use for data cleaning:

1. ***Conditional formatting*** to highlight blank cells, data that is outside a range, etc
2. ***Remove duplicates*** using the Data cleanup option on the Data tab
3. Date formatting to make all the data consistent
4. ***Split text to columns*** option on the Data tab to separate data into columns
5. ***Split text to columns*** option on the Data tab to fix numbers stored as text
6. `COUNTIF` function to find outliers in your data range
7. `LEN` function to determine the length of information in your spreadsheet that must be of a certain length
8. `LEFT`, `MID` and `RIGHT` functions to return segments of a string
9. `CONCATENATE` function to combine strings
10. `TRIM` function to remove leading, trailing, and repeated spaces in data
11. ***Pivot tables*** to sort, reorganize, group, count, total, or average data, giving you a clear view of your dataset for identifying patterns or issues
12. `VLOOKUP` function to search for a specific value in a column and return corresponding information from another column, is helpful for consolidating data from multiple sources
13. ***Plotting*** data through graphs or charts helps visualize the information and identify outliers or skewed data points that need attention or correction
14. `CONCATENATE` function to join together two or more text strings to clean data after two datasets have been combined
15. ***Importing .csv files*** into spreadsheets enables efficient data cleaning through visual inspection, built-in functions, and formatting tools

---

## Workflow automation

***Workflow automation*** involves automating repetitive tasks to save time and reduce errors. For data analysts, this could mean automating data cleaning, visualization, or even parts of the modeling process, which in turn frees up time for more critical aspects of the job, such as data exploration and analysis. By automating repetitive processes, data analysts can achieve higher accuracy and consistency in their work.

While automation is incredibly valuable, tasks requiring human judgment, such as communication and presenting findings, cannot be automated. Data exploration may be enhanced by automation tools, but the core insights and interpretations still rely on human analysts.

---

## Activity: Clean data with spreadsheet functions

As a data analyst working for a marketing agency based in San Francisco, I am asked to review external data related to ratings and locations of boba tea shops in San Francisco. Before this can be done, however, I need to identify the dirty elements in the dataset and clean them up. I am supplied with a .csv file containing dirty data that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1BoSS0KCRhBdlBn5WBWYXKCpuLJfjj-FsKZIlseZY2wA/edit?usp=sharing) or the [.csv File](/activities/spreadsheets/c04m02-clean-data-functions/c04m02-boba-teashop-data.csv). Below is a preview of the raw data before cleaning:

![Dirty Data Preview](/activities/spreadsheets/c04m02-clean-data-functions/c04m02-boba-teashop-data.png 'Dirty Data Preview')

In Google Sheets, I take the following steps to clean the data:

- Selected the entire sheet and cleared all formatting
- Select the range A1:H51 and used the "Convert to table" feature to apply automatic formatting
- Apply conditional formatting using the custom formula `=COUNTIF($A$2:$A$1000, $A2) > 1` to highlight duplicates in column A
- Apply conditional formatting using the custom formula `=COUNTIF($B$2:$B$1000, $B2) > 1` to highlight duplicates in column B
- Filter column A and B by the color assigned to duplicates using conditional formatting
- Identify rows with duplicate data as rows 8, 9, 20, 21, 25 and 26
- Delete row 8 as the rating 6.7 is out of range, whilst row 9 has a valid rating of 4
- Delete rows 21 and 26
- As ratings should fall between 0 and 5, I filter column C to show all values outside this range
- Proceed to delete rows now numbered 25, 67, 90, 135, 162, 220, 245, and 273
- Add new column G **lat** and new column H **long**
- Enter the `=SPLIT(F2,"-")` function in column G to split column F into columns G and H
- Copy columns G and H and paste special, paste values only to paste the data without the function
- Delete column F
- Change all longitude values to negative using the formula `=G2*-1`
- Copy the now negative values in column G and use paste special, paste values only to paste the data without the formula in column G with the longitude values
- Delete column H

The cleaned data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1R4dFXvuqbeo2qiGtaBnPo_XkYu3RGnFXHXaWCcW4XDI/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c04m02-clean-data-functions/c04m02-boba-teashop-activity.xlsx). Below is a preview of the clean data:

![Clean Data Preview](/activities/spreadsheets/c04m02-clean-data-functions/c04m02-boba-teashop-activity.png 'Clean Data Preview')

It should be noted that other than the steps above:

- the option Data, then Data cleanup and the Remove duplicates option can also be used to identify and automatically remove duplicate rows, and
- the option Data, then the Split Text to Columns option selecting a dash(-) as custom separator can also be used to automatically split column F into 2 columns

---

## Your cleaning checklist

Before diving into cleaning, create a checklist of tasks to help you quickly identify potential data issues. Some examples of common data cleaning tasks to include in your checklist:

- **Determine the size of the dataset:** Large datasets may have more data quality issues and take longer to process. This may impact your choice of data cleaning techniques and how much time to allocate to the project.
- **Determine the number of categories or labels:** By understanding the number and nature of categories and labels in a dataset, you can better understand the diversity of the dataset. This understanding also helps inform data merging and migration strategies.
- **Identify missing data:** Recognizing missing data helps you understand data quality so you can take appropriate steps to remediate the problem. Data integrity is important for accurate and unbiased analysis.
- **Identify unformatted data:** Identifying improperly or inconsistently formatted data helps analysts ensure data uniformity. This is essential for accurate analysis and visualization.
- **Explore the different data types:** Understanding the types of data in your dataset (for instance, numerical, categorical, text) helps you select appropriate cleaning methods and apply relevant data analysis techniques.

---

## Module 2 Glossary

| Term | Definition |
| --- | --- |
| **Clean data** | Data that is complete, correct, and relevant to the problem being solved |
| **Compatibility** | How well two or more datasets are able to work together |
| **CONCATENATE** | A spreadsheet function that joins together two or more text strings |
| **Conditional formatting** | A spreadsheet tool that changes how cells appear when values meet specific conditions |
| **Data engineer** | A professional who transforms data into a useful format for analysis and gives it a reliable infrastructure |
| **Data mapping** | The process of matching fields from one data source to another |
| **Data merging** | The process of combining two or more datasets into a single dataset |
| **Data validation** | A tool for checking the accuracy and quality of data |
| **Data warehousing specialist** | A professional who develops processes and procedures to effectively store and organize data |
| **Delimiter** | A character that indicates the beginning or end of a data item |
| **Dirty data** | Data that is incomplete, incorrect, or irrelevant to the problem to be solved |
| **Duplicate data** | Any record that inadvertently shares data with another record |
| **Field length** | A tool for determining how many characters can be keyed into a spreadsheet field |
| **Incomplete data** | Data that is missing important fields |
| **Inconsistent data** | Data that uses different formats to represent the same thing |
| **Incorrect/inaccurate data** | Data that is complete but inaccurate |
| **LEFT** | A function that returns a set number of characters from the left side of a text string |
| **LEN** | A function that returns the length of a text string by counting the number of characters it contains |
| **Length** | The number of characters in a text string |
| **Merger** | An agreement that unites two organizations into a single new one |
| **MID** | A function that returns a segment from the middle of a text string |
| **Null** | An indication that a value does not exist in a dataset |
| **Outdated data** | Any data that has been superseded by newer and more accurate information |
| **Remove duplicates** | A spreadsheet tool that automatically searches for and eliminates duplicate entries from a spreadsheet |
| **Split** | A function that divides text around a specified character and puts each fragment into a new, separate cell |
| **Substring** | A smaller subset of a text string |
| **Text string** | A group of characters within a cell, most often composed of letters |
| **TRIM** | A function that removes leading, trailing, and repeated spaces in data |
| **Unique** | A value that can’t have a duplicate |

---

Continue to next module: [Data cleaning with SQL](/4-Process-Data-from-Dirty-to-Clean/3-Data-cleaning-with-sql.md)
