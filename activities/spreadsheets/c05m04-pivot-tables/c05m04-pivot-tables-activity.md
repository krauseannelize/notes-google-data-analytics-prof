# Explore movie data with pivot tables

## Scenario

I am a data analyst working with a filmmaking company. The company is trying to identify what genre of film they should make next. In order to help them make this decision, my manager has asked me to answer the following questions:

- On average, how much money do movies make in each genre?
- On average, how much money is spent on a movie broken by genre?
- On average, which genre has the most profitable movies?

## Dataset

For my analysis, I will use a spreadsheet containing data of approximately 500 movies. The spreadsheet can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1UPVcBkJrvxF6gi_jaBJa94M6hTKCQ6EHtm7nRE63xUw/edit?usp=sharing) of the [Excel file](/activities/spreadsheets/c05m04-pivot-tables/c05m04-movie-data.xlsx).

## Create a pivot table

In Google Sheets, I take the following steps to create a pivot table for my analysis:

- in the sheet named "Movie Data", I select the *Pivot Table* option from the **Insert** menu and use the following settings:
  - Data range: `'Movie Data'!A1:N509`
  - Insert to: *New Sheet*
- I rename the new sheet to **Summary** and confirm that the *Pivot table editor* is open

## Question: Average amount of money movies make in each genre

To create this pivot table, the following field arrangement was used:

| Part | Field |
| --- | --- |
| **Rows** | Genre (1) |
| **Columns** | - |
| **Values** | Box Office Revenue ($) |
| **Values summarized by** | AVERAGE |
| **Filters** | - |

Below is a screenshot of the pivot table that shows the average money movies make in each genre:

![Average money made per movie genre](/activities/spreadsheets/c05m04-pivot-tables/c05m04-pivot-genre-revenue-avg.png "Average money made per movie genre")

## Question: Average amount of money spent on a movie in each genre

Using the pivot table from the previous question, I add an additional field to the arrangement:

| Part | Field |
| --- | --- |
| **Values** | Budget ($) |
| **Values summarized by** | AVERAGE |

Below is a screenshot of the pivot table that shows the average money spent on a movie in each genre:

![Average money spent per movie genre](/activities/spreadsheets/c05m04-pivot-tables/c05m04-pivot-genre-budget-avg.png "Average money spent per movie genre")

## Question: Most profitable movie genre on average

I now add a *Calculated Field* to the previous arrangement by following these steps:

- click the *Add* button to the right of the **Values** section
- select *Calculated Field*
- enter the following formula: `=AVERAGE('Box Office Revenue ($)')-AVERAGE('Budget ($)')`
- change the *Summarize by* selection from "SUM" to "Custom"
- enter **Average Profit** as the name of the newly calculated field
- to show the most profitable genres first, I go to the **Rows** section and
  - change the *Sort by* drop-down to **Average Profit**
  - change the *Order* drop-down to "Descending"

I now have a complete table showing the average money made, average money spent and the average profit made per movie genre as shown below:

![Average profit per movie](/activities/spreadsheets/c05m04-pivot-tables/c05m04-pivot-profit-avg.png 'Average profit per movie genre')

## Data visualization with pivot tables

With an existing pivot table, I can easily create a data visualization to more effectively communicate data insights. To this end, I take these steps:

- with the pivot table selected, I select *Chart* from the **Insert** menu that inserts a chart in the same sheet as the pivot table
- after moving the chart to the side of the pivot table, I make the following changes in the *Chart editor*:
  - **Setup** menu:
    - change the *Chart type* to "Bar Chart"
    - remove **AVERAGE of Budget ($)** and **Average Profit** from the **Series** section
  - **Customize** menu:
    - change the *Chart title* to "Average of Box Office Revenue ($) by Genre"
    - change the *Vertical axis title* to "Movie Genre"
- I would like movie genres' average box office revenue to appear from highest to lowest and I make the following changes in the *Pivot table editor* in the **Rows** section:
  - change the *Sort by* drop-down to **Average of Box Office Revenue ($)**
  - change the *Order* drop-down to "Descending"
  - uncheck the **Show totals** box

The chart now shows the average amount of money movies make in each genre from highest grossing to lowest as shown below:

![Pivot chart of average movie genre revenue](/activities/spreadsheets/c05m04-pivot-tables/c05m04-pivot-chart-revenue.png 'Pivot chart of average movie genre revenue')

The spreadsheet containing the completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1nI4ItLggVPtN7CVPTx16JrYkwZqGw0NChdPpk2nCyDY/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c05m04-pivot-tables/c05m04-movie-activity.xlsx).
