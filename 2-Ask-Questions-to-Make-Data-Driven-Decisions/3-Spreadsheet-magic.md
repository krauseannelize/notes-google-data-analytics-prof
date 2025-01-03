# Spreadsheet magic

## Table of contents

1. [Introduction](#introduction)
2. [Activity: Basic spreadsheet tasks](#activity-basic-spreadsheet-tasks)
3. [Activity: Formulas for success](#activity-formulas-for-success)
4. [Activity: Bakery sale insights](#activity-bakery-sale-insights)
5. [Activity: Resolve spreadsheet errors](#activity-resolve-spreadsheet-errors)
6. [Activity: Functions 101](#activity-functions-101)
7. [Activity: Custom data table](#activity-custom-data-table)
8. [Defining the problem](#defining-the-problem)
    - [Structured thinking](#structured-thinking)
    - [Scope of work](#scope-of-work)
    - [The importance of context](#the-importance-of-context)
9. [Module 3 Glossary](#module-3-glossary)

---

## Introduction

Spreadsheets are essential tools for data analysts, used to organize, analyze, and visualize data, forming the basis for data-driven decisions.
They can automate calculations, saving time and providing clear insights into how results are derived. Resources for more information:

- [Start Guide: Google Sheets](https://support.google.com/a/users/answer/9300311?hl=en&ref_topic=9296423)
- [Start Guide: Microsoft Excel](https://support.microsoft.com/en-us/office/office-quick-starts-25f909da-3e76-443d-94f4-6cdf7dedc51e#ID0EAADAAA=At_work_or_school)
- [Shortcuts: Google Sheets](https://support.google.com/docs/answer/181110)
- [Shortcuts: Microsoft Excel](https://support.microsoft.com/en-us/office/keyboard-shortcuts-in-excel-1798d9d5-842a-42b8-9c99-9b7213f0040f)
- [Errors and fixes: Google Sheets](https://www.benlcollins.com/spreadsheets/formula-parse-error/)
- [Errors and fixes: Microsoft Sheets](https://support.microsoft.com/en-us/office/Formulas-and-functions-294d9486-b332-48ed-b489-abe7d0f9eda9#ID0EAABAAA=Errors&ID0EBBD=Errors)
- [Differences between Google Sheets and Microsoft Excel](https://support.google.com/a/users/answer/9331278?hl=en)

---

## Activity: Basic spreadsheet tasks

To complete the activity, I received a sample dataset of the *Population of Latin and Caribbean countries from 2010 to 2019* that can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1HalKDAXk92cWjxfjAnLOAUwwPlRtzn5w2K_mJme0OAA/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c02m03-basic-tasks/c02m03-population-lac-countries-data.xlsx). I perform these basic spreadsheet activities:

- open a new spreadsheet
- create a new folder
- change cell size
- make attributes stand out
- add or delete columns
- add a border

As I am an advanced spreadsheet user, I used a new Google Sheets feature introduced in May 2024 **"Convert to table"** to apply automatic formatting to the table such as emphasized headers, filtering, resizing columns and naming the data range. The formatted spreadsheet can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/13eJDtozw4Y7w59CeRhKBw6z8A95KU25br7WvEQVHoDQ/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c02m03-basic-tasks/c02m03-population-lac-countries-activity.xlsx).

---

## Activity: Formulas for success

The sample dataset of *Monthly Sales* can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/125ahFIEOhVEmwSK0GYQeIqYuVcvYZgWNECzAtjb9_fo/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-formulas-success/c02m03-formulas-success-data.xlsx). This activity covers the basics of using spreadsheet formulas for calculations including correcting errors and I performed the following actions in Google Sheets:

- used the *Convert to table* tool to apply automatic formatting
- applied consistent formatting to all numbers
- added the headings **Average Sales** in cell G1 and **June to July changes** in cell H1
- in cell F2, enter the function `=SUM(B2:E2)` to calculate the total sales and copy the function down to cell F4
- in cell G2, enter the function `=AVERAGE(B2:E2)` to calculate the average sales and copy the function down to cell G4
- in cell H2, enter the formula `=(E2-D2)/D2` to calculate the June to July changes and copy the formula down to cell H4
- corrected the error by inserting the value 75866 for June 2019 in cell D4
- as the percentage change for June to July 2017 did not provide the expected result of 247.5%, I changed the June 2017 sales from 4002 to 47002
- applied percentage formatting to cells H2 to H4

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1yuHGrBhFNLR-Kaw6qXvGpzt26TDNj1HgQ-lXAawGrYw/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-formulas-success/c02m03-formulas-success-activity.xlsx).

---

## Activity: Bakery sale insights

The sample dataset of *Bakery Sales March 2020* can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1oBxZKfxhjIB9XwqKmPdsa6kDbMIjgKxQsG4xUWdO6NM/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-bakery-sales/c02m03-bakery-sales-202003-data.xlsx). This activity illustrates how to use formulas to calculate essential metrics that reveal the revenue generated by each product. To this end, I performed the following actions in Google Sheets:

- used the *Convert to table* tool to apply automatic formatting
- added the heading **Revenue** in cell E1
- in cell E2, enter the formula `=C2*D2` to calculate the revenue and copy this formula down to cell E22
- create a new "summary" table with the headings **Product** in cell G1, **Price** in cell H1, **Total Sold** in cell I1 and **Total Revenue** in cell J1
- created a visible break between the two tables by filling column F in a dark grey
- in cell G2, enter the function `=SORT(UNIQUE(B2:B))` to extract the individual product lines sorted in alphabetical order and copy the function down to cell G5
- in cell H2, enter the function `=VLOOKUP($G2,$B$2:$C$31, 2, FALSE)` to look-up the price of each product and copy the function down to cell H5
- in cell I2, enter the function `=SUMIF($B$2:$B,$G2,$D$2:$D)` to calculate the total units sold per product line and copy the function down to cell I5
- in cell J2, enter the formula `=H2*I2` to calculate the total revenue per product line and copy the formula down to cell J2
- added totals to the **Total Sold** and **Total Revenue** columns with the SUM function

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1qeQh2eOofs_kwiCFEKYxUIoF68P9gClfsC0aCDJXEhc/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-bakery-sales/c02m03-bakery-sales-202003-activity.xlsx).

---

## Activity: Resolve spreadsheet errors

This activity covers the how to identify and fix common errors in spreadsheets. A sample dataset *Resolve Spreadsheet Errors" was provided, which can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/15E1TJoGJP3A2Phrr1MgTIf9fJnvN-CCKWJqbSWpC49k/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-spreadsheet-errors-data.xlsx). This spreadsheet has 4 sheets:

- **Description:** A list of common errors and their meaning
- **Examples:** Sample data with errors
- **Fix the Examples Here:** Sample data for your to resolve the errors
- **Solution:** Sample data with the errors resolved and guiding notes on all affected cells

To resolve the errors, the following actions were taken:

| Cell | Error | Fix |
| --- | --- | --- |
| G3 | VALUE | Replace 'text' in B3 with 50 |
| G4 | ERROR | Insert missing comma |
| G5 | DIV | Replace 0 in B5 with 10 to not divide by zero |
| G6 | NAME | Correct function name SUMM to SUM |
| G7 | N/A | "Apples" doesn't exist, but "Apple" does |
| G8 | NUM | Cannot calculate square root on negative values |
| G9 | REF | Reference cell was deleted - updated to B2+B3 |

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1A4jvEj3bjJ7ZNeAGBFudgVY0t5xQrOszf0E1QyN17RE/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-spreadsheet-errors-activity.xlsx).

---

## Activity: Functions 101

This activity focus on using functions to perform calculations in a spreadsheet. A sample dataset *Monthly Sales* was provided, which can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1CaCFv4p0s2K_hQQnDDmVaroverg6OFjAFhAzQF3Elx8/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-functions-101-data.xlsx). I performed the following actions in Google Sheets:

- used the **"Convert to table"** feature to apply automatic formatting
- applied consistent formatting to all numbers
- added additional columns for "Lowest Monthly Sales" and "Highest Monthly Sales"
- calculated the "Total Sales" using the function `=SUM(B2:E2)`
- calculated the "Average Sales" using the function `=AVERAGE(B2:E2)`
- calculated the "June to July changes" using the formula `=(E2-D2)/D2`
- calculated the "Lowest Monthly Sales" using the function `=MIN(B2:E2)`
- calculated the "Highest Monthly Sales" using the function `=MAX(B2:E2)`
- apply color scale conditional formatting to "Lowest Monthly Sales" to highlight the lowest value
- apply color scale conditional formatting to "Highest Monthly Sales" to highlight the highest value

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1_Rqi0Z029yWANEfiv7Bw6GnVEstoJjY3dRGMubVb4lI/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c02m03-functions-101-activity.xlsx).

---

## Activity: Custom data table

In this activity, we are guided through the steps to use a spreadsheet to build a custom data table and analyze the job application data of a recruitment agency with functions to optimize the online application process. To highlight my analytical skills and visual communication abilities, I added aesthetic elements to the custom table, making the exercise more visually appealing and insightful.

My analysis of the activity **"Create a custom data table"** can be viewed [here](/activities/spreadsheets/c02m03-recruitment-agency-analysis.md).

---

## Defining the problem

The ***problem domain*** is the specific area you're analyzing, encompassing everything that affects or is affected by the problem. Understanding the problem domain involves identifying all its parts and relationships to grasp the complete story behind the data. Just like solving a jigsaw puzzle without knowing the final image is difficult, data analysis requires a clear understanding of the problem to be solved. Data analysts often start projects without a complete picture, making it crucial to define the problem domain and use ***structured thinking*** to find the best solution.

### Structured thinking

Structured thinking is the process of:

- recognizing the current problem or situation,
- organizing available information,
- revealing gaps and opportunities, and
- identifying the options.

It's having a clear list of:

- what you are expected to deliver,
- a timeline for major tasks and activities, and
- checkpoints so the team knows you're making progress.

Practice structured thinking and avoid mistakes is by using a ***scope of work***.

### Scope of work

A scope of work (SOW) is an agreed-upon outline of the work. It is project-based and sets the expectations and boundaries. It can includes things like:

- data preparation
- data validation
- analysis of quantitative and qualitative datasets
- initial results
- visuals to get the point across

A scope of work may be included in a statement of work to help define project outcomes, but it is not be confused. A statement of work is a document that clearly identifies the products and services a vendor or contractor will provide to an organization. It includes objectives, guidelines, deliverables, schedule, and costs.

A template to use when creating a scope of work can be accessed [here](/documents/template-scope-of-work.pdf). Some examples of scope of work activities:

#### Deliverable

- Estimated budget for the event
- Goals for the employee training event
- List of employees to invite

#### Timeline

- Hold the training event July 1
- Send event reminder email June 25
- Invite all attendees by June 1

#### Milestones

- Confirm list of employees who will attend
- Confirm budget
- Confirm staff trainers

#### Report

- Performance improvement one month after training
- Employee feedback after the training
- Final list of employees who attended

### The importance of context

Context can turn raw data into meaningful information. It is very important for data analysts to contextualize their data. This means giving the data perspective by defining it. To do this, you need to identify:

| Question | Context |
| --- | --- |
| **Who** | The person or organization that created, collected, and/or funded the data collection |
| **What** | The things in the world that data could have an impact on |
| **Where** | The origin of the data |
| **When** | The time when the data was created or collected |
| **Why** | The motivation behind the creation or collection |
| **How** | The method used to create or collect it |

Effective questions follow the SMART methodology and effective questions can lead to key insights you can use to solve all kinds of problems. In order to craft an SOW, the requirements of the project must be clarified and the expectations set. This can only be done by asking effective questions. It is important to analyze datasets to obtain insights that can solve business problems and turn it into actionable insights.

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
