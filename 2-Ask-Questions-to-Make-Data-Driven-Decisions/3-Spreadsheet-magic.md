# Spreadsheet magic

## Table of contents

1. [Introduction](#introduction)
2. [Spreadsheet hands-on activities](#spreadsheet-hands-on-activities)
    - [Basic spreadsheet tasks](#basic-spreadsheet-tasks)
    - [Formulas for success](#formulas-for-success)
3. [Module 3 Glossary](#module-3-glossary)

---

## Introduction

Spreadsheets are essential tools for data analysts, used to organize, analyze, and visualize data, forming the basis for data-driven decisions.
They can automate calculations, saving time and providing clear insights into how results are derived. Resources for more information:

- [Google Sheet Shortcuts](https://support.google.com/docs/answer/181110)
- [Microsoft Excel Shortcuts](https://support.microsoft.com/en-us/office/keyboard-shortcuts-in-excel-1798d9d5-842a-42b8-9c99-9b7213f0040f)

---

## Spreadsheet hands-on activities

### Basic spreadsheet tasks

We received a sample dataset of the *Population of Latin and Caribbean countries from 2010 to 2019* that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1HalKDAXk92cWjxfjAnLOAUwwPlRtzn5w2K_mJme0OAA/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c02m03-population-lac-countries-data.xlsx). We were tasked with performing these basic spreadsheet activities:

- open a new spreadsheet
- create a new folder
- change cell size
- make attributes stand out
- add or delete columns
- add a border

As I am an advanced spreadsheet user, I used a new Google Sheets feature introduced in May 2024 **"Covert to table"** to apply automatic formatting to the table such as emphasized headers, filtering, resizing columns and naming the data range. The formatted spreadsheet can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/13eJDtozw4Y7w59CeRhKBw6z8A95KU25br7WvEQVHoDQ/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c02m03-population-lac-countries-activity.xlsx).

### Formulas for success

We received a sample dataset of *Monthly Sales* that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/125ahFIEOhVEmwSK0GYQeIqYuVcvYZgWNECzAtjb9_fo/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-formulas-success-data.xlsx). This activity covers the basics of using spreadsheet formulas for calculations including correcting errors and I performed the following actions in Google Sheets:

- used the **"Convert to table"** feature to apply automatic formatting
- applied consistent formatting to all numbers
- added additional columns for "Average Sales" and "June to July changes"
- calculated the "Total Sales" using the formula `=SUM(B3:E3)` instead of `=B3+C3+D3+E3`
- calculated the "Average Sales" using the formula `=AVERAGE(B2:E2)` instead of `=(B2+C2+D2+E2)/4`
- calculated the "June to July changes" using the formula `=(E2-D2)/D2`
- corrected the formula error by inserting the value 75866 for June 2019
- as the percentage change for June to July 2017 did not provide the expected result of 247.5%, I changed the June 2017 sales from 4002 to 47002
- applied percentage formatting to "June to July changes"

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1yuHGrBhFNLR-Kaw6qXvGpzt26TDNj1HgQ-lXAawGrYw/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-formulas-success-activity.xlsx).

---

## Module 3 Glossary

| Term | Definition |
| --- | --- |
| **AVERAGE** | A spreadsheet function that returns an average of the values from a selected range |
| **Borders** | Lines that can be added around two or more cells on a spreadsheet |
| **Cell reference** | A cell or a range of cells in a worksheet typically used in formulas and functions |
| **COUNT** | A spreadsheet function that counts the number of cells in a range that meet a specific criteria |
| **Equation** | A calculation that involves addition, subtraction, multiplication, or division (also called a math expression) |
| **Fill handle** | A box in the lower-right-hand corner of a selected spreadsheet cell that can be dragged through neighboring cells in order to continue an instruction |
| **Filtering** | The process of showing only the data that meets a specified criteria while hiding the rest |
| **Header** | The first row in a spreadsheet that labels the type of data in each column |
| **Math expression** | A calculation that involves addition, subtraction, multiplication, or division (also called an equation) |
| **Math function** | A function that is used as part of a mathematical formula |
| **MAX** | A spreadsheet function that returns the largest numeric value from a range of cells |
| **MIN** | A spreadsheet function that returns the smallest numeric value from a range of cells |
| **Open data** | Data that is available to the public |
| **Operator** | A symbol that names the operation or calculation to be performed |
| **Order of operations** | Using parentheses to group together spreadsheet values in order to clarify the order in which operations should be performed |
| **Problem domain** | The area of analysis that encompasses every activity affecting or affected by a problem |
| **Range** | A collection of two or more cells in a spreadsheet |
| **Report** | A static collection of data periodically given to stakeholders |
| **Return on investment (ROI)** | A formula that uses the metrics of investment and profit to evaluate the success of an investment |
| **Revenue** | The total amount of income generated by the sale of goods or services |
| **Scope of work (SOW)** | An agreed-upon outline of the tasks to be performed during a project |
| **Sorting** | The process of arranging data into a meaningful order to make it easier to understand, analyze, and visualize |
| **SUM** | A spreadsheet function that adds the values of a selected range of cells |

---

Continue to next module: [Always remember the stakeholder](/2-Ask-Questions-to-Make-Data-Driven-Decisions/4-Always-remember-stakeholders.md)
