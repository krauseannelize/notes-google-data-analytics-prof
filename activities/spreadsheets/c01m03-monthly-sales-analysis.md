# Analyze patterns in monthly sales

## Scenario

The company relies on tourists for the bulk of its sales. The tourist season has a direct impact on the demand for inventory and staffing requirements. To help determine optimal inventory and staffing levels, leadership requires an analysis of total sales trends for the last three years to help with the forecasting for next year.

## Data

The monthly sales data used can viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1G2r8RuzynC7pc3tVFh6VtRARigpM5Oq3JQLhUXun74g/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c01m03-monthly-sales-data.xlsx). This spreadsheet contains total sales data for each month beginning in January 2021 and ending in December 2023. A portion of the spreadsheet is shown below.

![Monthly Sales Data](/activities/spreadsheets/c01m03-monthly-sales-data.png 'Monthly Sales Data')

## Preparation

As the dates (**column A**) was in date format, I needed to manipulate the data so that I can extract the graph that I had in mind for this visualization. Here is the steps I followed:

1. Added **column B** to extract the year from the date column using the formula `=YEAR(A2)`. This will be used for look-up purposes in **column F**.
2. Added **column C** to extract the month and year from the date column in string format using the formula `=TEXT(A2,"mmm yyyy")`. This column will be used to display all the months neatly formatted in the graph.
3. Added **column E** to assign a value to the cell based on its yearly rank calculated in **column F** using the formula `=IF(OR(F2=1,F2=2,F2=3),100000,0)`. This will assign a value of 100000 to the 3 months with the highest sales in any given year and 0 to any other months. This column will be used for shading in the graph to highlight the months with the most sales.
4. Added **column F** to assign a rank for each month of the year based on the amount of sales in that specific year using the formula `=RANK(D2, FILTER(D:D, B:B=B2), 0)`. **Column D** contains the total sales for the month and the formula determines it's rank descending so that the month with the most sales will be 1 and the month with the least will be 12. It uses a filter to ensure that the year in **column B** is the same for the range being ranked.
5. Inserted a combo graph in a separate sheet using the data in **columns C, D and E**. The total sales in **column D** is indicated using a line graph, and an area graph for the values assigned for shading purposes in **column E** to highlight the top 3 sales months.

The spreadsheet containing the analyzed data after preparation and with the graph visualization can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1AjwcXVJLBfLqIksQ4Q1VRIia4kbJ2dTjCmJyD1KLHzc/edit?usp=sharing) or in the [Excel File](/activities/spreadsheets/c01m03-monthly-sales-analysis.xlsx).

## Visualization

The total monthly sales for the period January 2021 to December 2023 is visualized in the graph below:

![Monthly Sales Graph](/activities/spreadsheets/c01m03-monthly-sales-analysis.png 'Monthly Sales Graph')

## Conclusion

From the analysis and visualization, it can be concluded that the months of December, January and February are the peak tourist season. To anticipate the increased demand in tourist season and to ensure optimal inventory and staffing levels, it is recommended that more inventory is added and additional staff recruited for the months of December to February.
