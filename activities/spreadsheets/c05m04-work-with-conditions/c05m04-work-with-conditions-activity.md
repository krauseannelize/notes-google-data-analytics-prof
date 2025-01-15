# Work with conditions

## Scenario

The company stakeholders have asked me to answer a number of questions pertaining specifically to NY state such as:

- How many sales representatives does the company have?
- What is the total of sales?
- What is the average number of sales?
- What is the total of sales exceeding $500?
- What is the most sales for any sales representative?
- How many sales representatives have only one client?

## Dataset

For this analysis, I have a spreadsheet containing a table with the names of the company's sales representatives, in which states they are based, how many clients they have, the value of sales they made, and so forth. The spreadsheet used can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1yp0yytXnxbME4sa-GiK52rJ-zVhvD9qr3xNTienoo5g/edit?usp=drive_link) of the [Excel file](/activities/spreadsheets/c05m04-work-with-conditions/c05m04-work-with-conditions-data.xlsx).

## Summary table

I believe the stakeholders would in future want to ask the same questions about the other states that the company have sales representatives in, so I aim to build a dynamic summary table where the state can be selected and information updated automatically. I also add additional questions and ranges to provide a better overview of each state. To do this, I take the following steps in Google Sheets:

- used the *Convert to table* feature to apply automatic formatting
- in cell A23, enter: **States**
- in cell A24, I enter the function `=SORT(Unique(B2:B21),1,1)` to create a reference table to use for a dynamic drop-down list
- apply dark grey background to column H to create a visual separation between the data and the summary table
- in the merged cell range I1:J1, enter: **Summary**
- in cell I2, enter: "Select a state to summarize"
- in cell J2, I select "Data validation" from the Data menu and create a new validation rule using a Drop-down (from a range) using the range `=Sheet1!$A$24:$A$31`, which creates a list of states the company has sales representatives in
- in cell I4, enter: "Total sales"
- in cell J4, I enter the function `=SUMIF(B2:B21,$J$2,D2:D21)` to calculate the total sales for the state selected in J2
- in cell I5, enter: "Average sales"
- in cell J5, I enter the function `=AVERAGEIF(B2:B21,$J$2,D2:D21)` to calculate the average sales for the state selected in J2
- in cell I6, enter: "Total sales over $500"
- in cell J6, I enter the function `=SUMIFS($D$2:$D$21,$B$2:$B$21,$J$2,$D$2:$D$21,">500")` to calculate the totals sales for the state selected in J2 that exceed $500
- in cell I7, enter: "Total sales over $1000"
- in cell J7, I enter the function `=SUMIFS($D$2:$D$21,$B$2:$B$21,$J$2,$D$2:$D$21,">1000")` to calculate the totals sales for the state selected in J2 that exceed $1000
- in cell I8, enter: "Total sales over $1500"
- in cell J8, I enter the function `=SUMIFS($D$2:$D$21,$B$2:$B$21,$J$2,$D$2:$D$21,">1500")` to calculate the totals sales for the state selected in J2 that exceed $1500
- in cell I9, enter: "Total sales over $2000"
- in cell J9, I enter the function `=SUMIFS($D$2:$D$21,$B$2:$B$21,$J$2,$D$2:$D$21,">2000")` to calculate the totals sales for the state selected in J2 that exceed $2000
- in cell I10, enter: "Number of clients"
- in cell J10, I enter the function `=SUMIF($B$2:$B$21,$J$2,$C$2:$C$21)` to calculate the total number of clients for the state selected in J2
- in cell I11, enter: "Number of sales representatives"
- in cell J11, I enter the function `=COUNTIF($B$2:$B$21,$J$2)` to count the number of sales representatives for the state selected in J2
- in cell I12, enter: "Most sales"
- in cell J12, I enter the function `=MAXIFS($D$2:$D$21,$B$2:$B$21,$J$2)` to calculate the maximum sales from any sales representative for the state selected in J2
- in cell I13, enter: "Sales representative with most sales"
- in cell J13, I enter the function `=INDEX($A$2:$A$21,MATCH($J$12,$D$2:$D$21,0))` to identify the sales representative with the most sales, the amount of which was calculated in cell J12
- in cell I14, enter: "Sales representatives with only 1 client:"
- in cell J14, I enter the function `=COUNTIFS($B$2:$B$21,$J$2,$C$2:$C$21,"1")` to count the number of sales representatives for the state selected in J2 that have only 1 client each
- in cell I15, I enter the function `=IF(ISNA(filter($A$2:$A$21,$B$2:$B$21=$J$2,$C$2:$C$21=1)),"",SORT(filter($A$2:$A$21,$B$2:$B$21=$J$2,$C$2:$C$21=1),1,1))` to extract the names of the sales representatives that have only 1 client each in the state selected in J2 - I include a function to check whether the filter will results in an error, as some states may not have any sales representatives with only 1 client

I now have a summary table that answers all the stakeholders questions regarding the state of NY as shown below:

![Summary table NY](c05m04-summary-ny.png 'Summary table NY')

To illustrate the dynamic nature of the summary table, I also include the information for the state of CA below:

![Summary table CA](c05m04-summary-ca.png 'Summary table CA')

The spreadsheet with the summary table can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1mwT5HkZdKp1kLfVBjjxxdnVa9czs7HZ6Wk3S9l26_uU/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c05m04-work-with-conditions/c05m04-work-with-conditions-activity.xlsx).
