# The importance of integrity

## Table of contents

1. [Why is data integrity important?](#why-is-data-integrity-important)
2. [Data constraint terms](#data-constraint-terms)
3. [Well-aligned objectives and data](#well-aligned-objectives-and-data)
4. [Module 1 Glossary](#module-1-glossary)

---

## Why is data integrity important?

Data integrity is the accuracy, completeness, consistency, and trustworthiness of data throughout its lifecycle. Maintaining data integrity is crucial for reliable data analysis, as compromised data can lead to inaccurate and misleading results. Potential risks that can compromise data integrity:

| Risk | Details |
| --- | --- |
| **Data replication** | Process of storing data in multiple locations creating a chance that data will be out of sync, which can cause inconsistencies |
| **Data transfer** | Process of copying data from one storage device to another and if transfer is interrupted, it could result in an incomplete data set |
| **Data manipulation** | Process involves changing the data to make it more organized and easier to read, and an error during the process can compromise the efficiency |

Data can also be compromised through:

- human error
- viruses
- malware
- hacking, and
- system failures

---

## Data constraint terms

There are many types of data constraints or criteria that determine validity.

| Data constraint | Definition | Examples |
| --- | --- | --- |
| **Data type** | Values must be of a certain type: date, number, percentage, Boolean, etc. | If the data type is a date, a single number like 30 would fail the constraint and be invalid |
| **Data range** | Values must fall between predefined maximum and minimum values | If the data range is 10-20, a value of 30 would fail the constraint and be invalid |
| **Mandatory** | Values can’t be left blank or empty | If age is mandatory, that value must be filled in |
| **Unique** | Values can’t have a duplicate | Two people can’t have the same mobile phone number within the same service area |
| **Regular expression (regex) patterns** | Values must match a prescribed pattern | A phone number must match ###-###-#### (no other characters allowed) |
| **Cross-field validation** | Certain conditions for multiple fields must be satisfied | Values are percentages and values from multiple fields must add up to 100% |
| **Primary-key** | (Databases only) value must be unique per column | A database table can’t have two rows with the same primary key value. A primary key is an identifier in a database that references a column in which each value is unique. More information about primary and foreign keys is provided later in the program |
| **Set-membership** | (Databases only) values for a column must come from a set of discrete values | Value for a column must be set to Yes, No, or Not Applicable |
| **Foreign-key** | (Databases only) values for a column must be unique values coming from a column in another table | In a U.S. taxpayer database, the State column must be a valid state or territory with the set of acceptable values defined in a separate States table |
| **Accuracy** | The degree to which the data conforms to the actual entity being measured or described | If values for zip codes are validated by street location, the accuracy of the data goes up |
| **Completeness** | The degree to which the data contains all desired components or measures | If data for personal profiles required hair and eye color, and both are collected, the data is complete |
| **Consistency** | The degree to which the data is repeatable from different points of entry or collection | If a customer has the same address in the sales and repair databases, the data is consistent |

---

## Well-aligned objectives and data

Good alignment with business objectives means that the data is relevant and can help you solve a business problem or determine a course of action to achieve a given business objective. If the data:

- is well-aligned but needs to be cleaned, clean the data before you perform your analysis
- only partially aligns with an objective, think about how you could modify the objective, or use data constraints to make sure that the subset of data better aligns with the business objective

![Clean data lead to accurate conclusions](/images/clean-data-objectives.png 'Clean data lead to accurate conclusions')

---

## Module 1 Glossary

| Term | Definition |
| --- | --- |
| **Accuracy** | The degree to which the data conforms to the actual entity being measured or described |
| **Completeness** | The degree to which the data contains all desired components or measures |
| **Confidence interval** | A range of values that conveys how likely a statistical estimate reflects the population |
| **Confidence level** | The probability that a sample size accurately reflects the greater population |
| **Consistency** | The degree to which data is repeatable from different points of entry or collection |
| **Cross-field validation** | A process that ensures certain conditions for multiple data fields are satisfied |
| **Data constraints** | The criteria that determine whether a piece of a data is clean and valid |
| **Data integrity** | The accuracy, completeness, consistency, and trustworthiness of data throughout its life cycle |
| **Data manipulation** | The process of changing data to make it more organized and easier to read |
| **Data range** | Numerical values that fall between predefined maximum and minimum values |
| **Data replication** | The process of storing data in multiple locations |
| **DATEDIF** | A spreadsheet function that calculates the number of days, months, or years between two dates |
| **Estimated response rate** | The average number of people who typically complete a survey |
| **Hypothesis testing** | A process to determine if a survey or experiment has meaningful results |
| **Mandatory** | A data value that cannot be left blank or empty |
| **Margin of error** | The maximum amount that the sample results are expected to differ from those of the actual population |
| **Random sampling** | A way of selecting a sample from a population so that every possible type of the sample has an equal chance of being chosen |
| **Regular expression (RegEx)** | A rule that says the values in a table must match a prescribed pattern |

---

Continue to next module: [Clean data for more accurate insights](/4-Process-Data-from-Dirty-to-Clean/2-Clean-data-for-more-accurate-insights.md)
