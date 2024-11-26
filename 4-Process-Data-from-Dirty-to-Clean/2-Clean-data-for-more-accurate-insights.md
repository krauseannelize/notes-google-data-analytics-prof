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
6. [Module 2 Glossary](#module-2-glossary)

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

In this activity, we are guided through some steps to do data cleaning with spreadsheets, whereafter the data is transposed. We were supplied with dirty data that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1lMYD9PHV-06u6ylP-dlX5UrBt4vofaBUg6RURx6TTvU/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c04m02-cleaning-with-spreadsheets-data.xlsx).

In Google Sheets, I took a slightly different approach to the one suggested and followed these steps to clean the data:

- Selected the entire sheet and cleared all formatting
- Select the range A1:H51 and used the "Convert to table" feature to apply automatic formatting
- Identify rows with blank values: 2, 8, 10, 16, 19 and 23
- Delete rows 2, 8 and 23
- Unit Cost in G10 is blank, but this can be calculated by dividing the Total by Units or `=H10/F10`. Insert the value 4.99 in G10
- Units in F16 is blank, but this can be calculated by dividing the Total by Unit Cost or `=H10/G10`. Insert the value 35 in F16
- Total in H19 is blank, but this can be calculated by multiplying the Units by Unit Cost or `=F19*G19`. Insert the value 251.72 in H19
- Select the entire sheet and select "Trim whitespace" from the Data tab, Data cleanup section
- Apply date formatting to column B to verify all cells contain valid dates
- Insert a new column F and used the function `=PROPER(C2)` to change all values in column C to Proper Case
- Insert a new column G and used the function `=PROPER(D2)` to change all values in column D to Proper Case
- Insert a new column H and used the function `=PROPER(E2)` to change all values in column E to Proper Case
- Copy columns F, G and H, and use paste special to paste values only remove the functions to convert to Proper Case
- Delete columns C, D and E
- Give column C (previously F) the heading "Region"
- Give column D (previously G) the heading "Name"
- Give column E (previously H) the heading "Item"
- Rename the sheet and table to "Long"
- Copy the table and use paste special to transpose the data to wide format in a new sheet and table named "Wide"

The cleaned data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1BYT0t9ptZtgtZ9AAoVsSAKBLZRr3vuBvQPuzx2gKUEA/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c04m02-cleaning-with-spreadsheets-activity.xlsx).

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
