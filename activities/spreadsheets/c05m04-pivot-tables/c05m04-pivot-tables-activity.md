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
