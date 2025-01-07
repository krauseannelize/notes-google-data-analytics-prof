# Calculate weekly pay for employees

## Scenario

I am the payroll manager at an accounting firm. To calculate payroll, I need to know how many hours each of the employees worked and their hourly rate of pay to calculate the total weekly pay for the employees.

## Data

The spreadsheet used for this activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/16MG7HDJf8GHAVdbFQzOHMKMYTsb34Uqay6JGB19SrEo/edit?usp=sharing) of the [Excel File](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-data.xlsx). The first sheet in the spreadsheet contains a timesheet of hours worked by the employees as shown below:

![Timesheet of hours worked](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-data-timesheet.png 'Timesheet of hours worked')

The second sheet in the spreadsheet contains the hourly pay rates of each employee that will be used in the VLOOKUP function to import the pay rates to my calculation of the total weekly pay for the employees. Below is a preview of this sheet:

![Employee hourly rates](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-data-hourly-rates.png 'Employee hourly rates')

## Preparation and processing

The data in the timesheet has not been cleaned so I need to prepare the data before I can proceed with the analysis. I cannot change the data from the original timesheet table, so I will create a clean version of the timesheet to manipulate. In Google Sheets, I first rename Sheet 1 to "timesheet" and Sheet 2 to "pay-rate" for ease of reference. I further use the *Convert to table* tool to assign the name "payrate" to the table in the "pay-rate" sheet for convenience with the VLOOKUP function. To create a clean copy of the timesheet in the "timesheet" sheet, I take the following steps:

- in cell B14, enter: **Names**
- in cells C14 to H14, enter: **1/1/2020**, **1/2/2020**, **1/3/2020**, **1/4/2020**, **1/5/2020**, and **1/6/2020**
- in cell I14, enter: **Hours**
- in cell J14, enter: **Pay Rate**
- in cell K14, enter: **Total Pay**
- apply bold and a background color to the headings in row 14
- in cell A15, enter the function `=TRIM(A2)` to remove extra spaces from the employee ID and copy this function down to A19
- in cell B15, enter the function `=TRIM(B2)` to remove extra spaces from the employee names and copy this function down to B19
- in cell C15, enter the function `=VALUE(C2)` to ensure that the daily hours of each employee is entered as numbers and copy this function down to C19
- highlight cells C15 to C19 and use the fill handle to copy this function for columns D, E, F, G and H

## Analyze

With this clean copy of the timesheet table, I will now perform basic calculations and data aggregation to obtain meaningful information. In Google Sheet, I continue with the following steps:

- in cell I15, enter the function `=SUM(C15:H15)` to calculate the total number of hours worked by each employee for the week 1 to 6 January 2020, and copy this function down to I19
- in cell J15, enter the function `=VLOOKUP(A15,payrate,4,FALSE)` to import the pay rate of each employee from the "pay-rate" sheet into column J, and copy the function down to J19
- in cell K15, enter the function `=PRODUCT(I15,J15)` to calculate the total pay of each employee, which is the total hours worked times the employee hourly rate, and copy the function down to K19

A preview of the clean copy of the timesheet table is shown below:

![Clean timesheet of hours worked](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-clean-timesheet.png 'Clean timesheet of hours worked')

I continue to create a pivot table to summarize the timesheet table as follows:

- highlight cells B14 to K19 and select *Pivot Table* from the **Insert** menu
- select the "New Sheet" option and then "Create"
- rename the newly created sheet Pivot Table 1 to "summary"
- in the pivot table, I add **Names** for "Rows", **Pay Rate** and **Total Pay** for "Values"
- highlight cells B2 to C6 in the "summary" sheet and apply a currency format by selecting the $ symbol from the toolbar

The total weekly pay for each employee has been summarized with their weekly rate in the pivot table as shown below:

![Weekly pay pivot table](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-pivot-table.png 'Weekly pay pivot table')

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1ZcaI4dVbW0ltQwjKaCpTdLE59mRp3f6RrVtP6GwQpKs/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c05m03-vlookup-practice/c05m03-weekly-pay-activity.xlsx).
