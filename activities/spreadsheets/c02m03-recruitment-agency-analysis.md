# Analysis to optimize job application process

## Scenario

A recruitment agency helps all sorts of companies find skilled people to fill open data analytics jobs. The agency has collected data about job applications for opportunities posted on its website over the course of a year. The agency wants to optimize its online application process and wants answers to the following questions:

- What was the total number of applications received each month?
- How many applications were received?
- In which months were the lowest and highest number of applications received?
- What was the average number of applications received per month?

## Data

The job application data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1LYWzuQIUgfwi19fXt756EnuLYpeZTXs76ywPG6HbAK0/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-recruitment-agency-data.xlsx). This spreadsheet contains data for the period January to December 2023 and an extract of the raw data is shown below.

![Job Application Data](/activities/spreadsheets/c02m03-recruitment-agency-data.png 'Job Application Data')

## Preparation

Before I continued with the analysis, I needed to prepare the data by following these steps in Google Sheets:

- renamed the sheet containing the data "raw-data"
- used the **"Convert to table"** feature to apply automatic formatting
- sorted the data by date
- inserted a new column "Month" and extract the name of the month using the function =TEXT(B3,"mmmm")

After some basic cleaning and organizing, the raw data now looked like shown below.

![Job Application Data cleaned](/activities/spreadsheets/c02m03-recruitment-agency-data-prep.png 'Job Application Data cleaned')

## Create summary table

To answer the questions posed by the recruitment agency, I first created a custom table in Google Sheets following these steps:

- added a new sheet named "summary" to contain the custom data table
- added a heading "2023 Job Applications in range A1:C1 using merge cells
- enter "Month" in A2, "Applications" in B2 and "Visualization" in C2 as sub-headers
- enter "January" in A3 and use autofill to enter the remaining 11 months
- calculate the number of applications received in each month using the function `=COUNTIF('raw-data'!$G$2:$G, A3)`
- enter "Total" in A15
- calculate the total number of applications received using the function `=SUM(B3:B14)` in B15
- to create an inline visualization of the number of applications using a bar chart, I used the function `=SPARKLINE($B3, {"charttype", "bar"; "max", $F$4; "min", 0; "color1", IF($B3=$F$4, "#3f8f29", IF($B3=$F$6, "#de1a24", "#0080ff"))})` - this creates a bar chart based on the number of application in a blue color, highlighting the month with the most applications in green and the month with the lowest applications in red
- formatted the custom table with borders, cell colors and adding emphasis using bold text and larger font sizes, and rounding numbers to 2 decimals

Then I created a second custom table in the same sheet to summarize the key questions:

- enter "Key Insights" as heading in the range E1:F2 using merge cells
- enter "Most applications received in" in cell E3
- extract the month with the highest applications number using the function `=INDEX($A$3:$B$14, MATCH(MAX($B$3:$B$14), $B$3:$B$14, 0), 1)` in cell F3
- enter "Highest number of applications" in cell E4
- calculate the highest number of applications received per month using the function `=MAX($B$3:$B$14)` in cell F4
- enter "Least applications received in" in cell E5
- extract the month with the lowest applications number using the function `=INDEX($A$3:$B$14, MATCH(MIN($B$3:$B$14), $B$3:$B$14, 0), 1)` in cell F5
- enter "Lowest number of applications" in cell E6
- calculate the lowest number of applications received per month using the function `=MIN($B$3:$B$14)` in cell F6
- enter "Average number of applications per month" in cell E7
- calculate the average number of applications received per month using the function `=AVERAGE($B$3:$B$14)` in cell F7
- formatted the custom table with borders, cell colors and adding emphasis using bold text and larger font sizes, and rounding numbers to 2 decimals
- removed gridlines from the view to create a dashboard-like effect

The spreadsheet containing the prepared and analyzed data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1uZfHQZqDhgQCk3I6cxulgwnRyPszvs9_o9N1HJUk7pU/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-recruitment-agency-analysis.xlsx).

## Visualization

The job applications received by the recruitment agency have been summarized in a dashboard and utilizes an inline bar graph to visualize the number of applications received:

![Job Application Analysis](/activities/spreadsheets/c02m03-recruitment-agency-analysis.png 'Job Application Analysis')

## Conclusion

From the analysis and visualization it is revealed that February was the slowest month and July the peak month. Strategically, the agency can allocate more of its advertising and outreach budget to February and less to July to optimize the application process.
