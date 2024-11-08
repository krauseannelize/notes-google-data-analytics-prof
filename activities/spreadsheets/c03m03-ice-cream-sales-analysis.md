# Data inspection and sufficiency analysis

## Project overview

An ice cream company is interested in improving the company's ice cream sales. Some internal data about its sales for 2019 has been collected. Ideally, management would like answers to the following questions:

1. What is the most popular flavor of ice cream?
2. How does temperature affect sales?
3. How do weekends and holidays affect sales?
4. How does profitability differ for new versus returning customers?

Inspect the data to determine if it contains the specific information needed to answer your stakeholders’ questions.

## Data source

The available data for the 2019 sales was collected in 3 separate tables: flavors, temperatures, sales. The raw data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1gmy-RnbZRRjRIrZUYZRI2XH4TY2yGFVuaTL09lsItEk/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c03m03-ice-cream-sales-data.xlsx). A preview of each table in the dataset is shown below:

![Ice Cream Sales Data](/activities/spreadsheets/c03m03-ice-cream-sales-data.png 'Ice Cream Sales Data')

## Data exploration

### Question 1: What is the most popular flavor of ice cream?

Firstly, it needs to be determined whether popular means that:

- the flavor had the largest number of units sold in 2019, or
- the flavor generated the most revenue in 2019.

In the case of the former, the flavor table provides enough information to calculate the total number of units sold during the year for each flavor. By following these steps in Google Sheets, I was quickly able to determine that ***Lemon*** is the most popular flavor:

1. used the **"Convert to table"** feature to apply automatic formatting
2. insert a **pivot table** in cell E2 grouping by flavor names with the sum of units sold

A preview of the summarized data is shown below:

![Question 1 Data](/activities/spreadsheets/c03m03-ice-cream-sales-analysis-q1.png 'Question 1 Data')

However, in the case of the latter:

- the flavors table does not contain the unit price to enable us to calculate revenue per flavor, and
- the sales table does not provide information on the flavor.

Unless this information is available from another sources, the data currently available is limited and a conclusion cannot be drawn.

### Question 2: How does temperature affect sales?

When inspecting the temperatures table, it is unclear whether the data represents:

- the temperature for a specific date with the corresponding sales revenue for the day,
- a summary of sales revenue for multiple days corresponding to a temperature, or
- temperature data for a consecutive date range.

As there are 365 entries and duplicate temperature values, it likely is a daily snapshot but further clarification is still required. Contact the owner of the dataset.

### Question 3: How do weekends and holidays affect sales?

By doing some manipulation, this data can be obtained from the sales table. In Google Sheets, I followed the following steps:

1. used the **"Convert to table"** feature to apply automatic formatting
2. insert a new column B 'weekday'
3. enter the function `=TEXT(A2, "dddd")` in cell B2 to determine the name of the day
4. use autofill to determine the name of the day for the entire dataset
5. insert a **pivot table** in cell E2 grouping by weekday name with the sum of sales sorted descending

Although sales over the weekend are significant, it would appear that sales on ***Tuesdays*** are the best followed by ***Monday***. The location of the ice cream company is not provided or the data of the holidays applicable to its location. Therefore, holiday data cannot be included in this analysis. A preview of the summarized data is show below:

![Question 3 Data](/activities/spreadsheets/c03m03-ice-cream-sales-analysis-q3.png 'Questions 3 Data')

### Question 4: How does profitability differ for new versus returning customers?

The data provided contains no customer information and the sales data cannot be related to customers in its current format. Without additional data, the answer cannot be answered.

---

## Conclusion

Despite the limitations of the dataset, it is still possible to provide stakeholders with some value insights relating to questions 1 and 3, respectively. Relevant datasets need to be identified and data collected for further analysis. With more data to analyze, inventory planning can be optimized and targeted marketing campaigns undertaken to increase the company's overall profitability.

The analyzed data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1gmy-RnbZRRjRIrZUYZRI2XH4TY2yGFVuaTL09lsItEk/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c03m03-ice-cream-sales-analysis.xlsx).
