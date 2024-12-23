# Format and adjust data

## Table of contents

1. [Activity: From one type to another](#activity-from-one-type-to-another)
   - [Check and change data type](#check-and-change-data-type)
   - [Convert temperatures from Fahrenheit to Celsius](#convert-temperatures-from-fahrenheit-to-celsius)
2. [Module 2 Glossary](#module-2-glossary)

---

## Activity: From one type to another

### Check and change data type

For this activity, we received the Movie Data Start Project spreadsheet, which can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1y-QBpy_q4mQuFM2nJhIROBKAn6fkPZ7pKo6KxQF8k0Q/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c05m02-movie-project-data.xlsx). In Google Sheets, I performed the following actions to check and change the data type:

- selected column M `[Budget ($)]` and column N `[Box Office Revenue ($)]`,
- in the Format menu, confirmed that both these columns were formatted as a number type,
- select the currency shortcut key `$` from the toolbar.

Columns M and N are now formatted as a currency type. The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/19SPXE3fn6MOuw1kk7RkWbbeReOombH_Z4og88vuPV4s/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c05m02-movie-project-activity.xlsx).

### Convert temperatures from Fahrenheit to Celsius

We will use the CONVERT function to change units of measurement. The supplied weather data table can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1PLS2GIP2S4KMKXcAb_QKNpGAIgcr2ycZQHrPBweJ1io/edit?usp=sharing) or in the [Excel file](/activities/spreadsheets/c05m02-weather-convert-data.xlsx). In Google Sheets, I followed the following steps:

- update the heading in B1 to `Temperature (F)`,
- add the heading `Temperature (C)` in F1,
- enter the formula `=CONVERT(B2, "F", "C")` in F2, where start_unit is Fahrenheit (F) and end_unit is Celsius (C),
- fill the formula down in column F,
- update the heading in D1 to `Wind Speed (mph)`,
- add the heading `Wind Speed (m/s)` in G1,
- enter the formula `=CONVERT(D2, "mph", "m/s")` in G2, where start_unit is miles per hour (mph) and end_unit is meters per second (m/s),
- fill the formula down in column G.

The completed activity can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1_sHMu_OrtmZ-kebC25cCbONU3LG4PVan0xHMnxEtHhQ/edit?usp=sharing) or the [Excel file](/activities/spreadsheets/c05m02-weather-convert-activity.xlsx).

---

## Module 2 Glossary

| Term | Definition |
| --- | --- |
| **ROUND** | A SQL function that returns a number rounded to a certain number of decimal places |

---

Continue to next module: [Aggregate data for analysis](/5-Analyze-Data-to-Answer-Questions/3-Aggregate-data-for-analysis.md)
