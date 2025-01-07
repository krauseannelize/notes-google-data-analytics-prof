# Clear data with in spreadsheets with sorting and filtering

## Scenario

The superintendent of a large public school district in Portugal wants to know what factors affect student grades in core subjects and what changes can be made to improve student performance. Our purview is to clean the data for analysis.

## Data

For the analysis, we have performance data on high school student achievement in two Portuguese public schools, Gabriel Pereira (GP) and Mouzinho da Silveira (MS). The data was collected by the school district by means of academic reports and student surveys. The data includes information such as:

- Student grades
- Student background information
- Student study time
- Student participation in extracurricular activities

The raw data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/1mMTAxS1XHFKfnZ43L61zCiMHLAN5A4GDqXUA36tUz9k/edit?usp=sharing) or the [.csv File](/activities/spreadsheets/c03m03-clean-data-spreadsheets/c03m03-student-performance-data.csv). A preview of the data is shown below:

![Student Performance Data](/activities/spreadsheets/c03m03-clean-data-spreadsheets/c03m03-student-performance-data.png 'Student Performance Data')

## Preparation

Before analyzing the data, however, it is important to make sure the data is clean as analyses using bad or dirty data could lead to wrong conclusions. The following steps were followed:

- created a duplicate of the raw data sheet **student-performance-data** in the same workbook named **clean-data**
- used the *Convert to table* feature to apply automatic formatting to the **clean-data** sheet
- the data was then sorted first by school, and then by age

The age range of the students at Gabriel Pereira (GP) is 15-22 years, while the age range of the students at Mouzinho da Silveira (MS) is 15-20 years. The dataset focussed on high school students and this age range poses a potential problem. We consult the superintendent who informs us that the the age range should be 15-19 for both schools. The age range 20-22 years can, therefore, be excluded from this analysis. We continue with these steps:

- filter the age column for the values 20, 21 and 22
- delete the 9 rows filtered out and reset the filter
- filter the reason column for blank values
- replace all blank values with "none-given"
- reset filter on the reason column

As the parent’s education level could be a significant factor in student performance, we replace the current relevant text data in the Medu and Fedu columns as follows for ranking purposes:

| Level of Education | Code |
| --- | --- |
| none | 0 |
| primary education (4th grade) | 1 |
| 5th to 9th grade | 2 |
| secondary education | 3 |
| higher education | 4 |

I use *find and replace* to replace all the education levels with the numerical values. Below is a preview of the cleaned data:

![Student Performance Data Cleaned](/activities/spreadsheets/c03m03-clean-data-spreadsheets/c03m03-student-performance-data-clean.png 'Student performance Data Cleaned')

## Conclusion

As my purview for this activity only extended to the cleaning, sorting and filtering of the dataset, this activity is concluded and the cleaned data can be viewed in [Google Sheets](https://docs.google.com/spreadsheets/d/17djYZnyryXeB5quONQXCgNaKLTdOVsxLmvvjvrZVwww/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c03m03-clean-data-spreadsheets/c03m03-student-performance-data-clean.xlsx).
