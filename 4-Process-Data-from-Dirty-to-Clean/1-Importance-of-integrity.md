# The importance of integrity

## Table of contents

1. [Why is data integrity important?](#why-is-data-integrity-important)
2. [Data constraint terms](#data-constraint-terms)
3. [Well-aligned objectives and data](#well-aligned-objectives-and-data)
4. [Insufficient Data](#insufficient-data)
   - [Types of insufficient data](#types-of-insufficient-data)
   - [Ways to address insufficient data](#ways-to-address-insufficient-data)
   - [When you find an issue with your data](#when-you-find-an-issue-with-your-data)
5. [Sample size](#sample-size)
   - [Sample size terms](#sample-size)
   - [Things to remember when determining the size of your sample](#things-to-remember-when-determining-the-size-of-your-sample)
   - [Test your data using statistical power](#test-your-data-using-statistical-power)
   - [When data isn't readily available](#when-data-isnt-readily-available)
6. [Module 1 Glossary](#module-1-glossary)

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

## Insufficient data

### Types of insufficient data

- Data from only one source
- Data that keeps updating
- Outdated data
- Geographically-limited data

### Ways to address insufficient data

- Identify trends with the available data
- Wait for more data if time allows
- Talk with stakeholders and adjust your objective
- Look for a new data set

### When you find an issue with your data

![Data Errors Decision Tree](/images/data-errors-decision-tree.png 'Data Errors Decision Tree')

#### Data issue 1: no data

| Possible Solutions | Examples of solutions in real life |
| --- | --- |
| Gather the data on a small scale to perform a preliminary analysis and then request additional time to complete the analysis after you have collected more data. | If you are surveying employees about what they think about a new performance and bonus plan, use a sample for a preliminary analysis. Then, ask for another 3 weeks to collect the data from all employees. |
| If there isn’t time to collect data, perform the analysis using proxy data from other datasets. This is the most common workaround. | If you are analyzing peak travel times for commuters but don’t have the data for a particular city, use the data from another city with a similar size and demographic. |

#### Data issue 2: too little data

| Possible Solutions | Examples of solutions in real life |
| --- | --- |
| Do the analysis using proxy data along with actual data. | If you are analyzing trends for owners of golden retrievers, make your dataset larger by including the data from owners of labradors. |
| Adjust your analysis to align with the data you already have. | If you are missing data for 18- to 24-year-olds, do the analysis but note the following limitation in your report: this conclusion applies to adults 25 years and older only. |

#### Data issue 3: wrong data, including data with errors

| Possible Solutions | Examples of solutions in real life |
| --- | --- |
| If you have the wrong data because requirements were misunderstood, communicate the requirements again | If you need the data for female voters and received the data for male voters, restate your needs |
| Identify errors in the data and, if possible, correct them at the source by looking for a pattern in the errors | If your data is in a spreadsheet and there is a conditional statement or boolean causing calculations to be wrong, change the conditional statement instead of just fixing the calculated values |
| If you can’t correct data errors yourself, you can ignore the wrong data and go ahead with the analysis if your sample size is still large enough and ignoring the data won’t cause systematic bias | If your dataset was translated from a different language and some of the translations don’t make sense, ignore the data with bad translation and go ahead with the analysis of the other data |

---

## Sample size

Studying an entire population might be impractical due to time and resource constraints. ***Sample size*** offers a practical solution by analyzing a smaller, representative group within the population to draw conclusions about the whole. This approach is more efficient and cost-effective. Terms and definitions used:

| Terminology | Definitions |
| --- | --- |
| **Population** | The entire group that you are interested in for your study. For example, if you are surveying people in your company, the population would be all the employees in your company. |
| **Sample** | A subset of your population. Just like a food sample, it is called a sample because it is only a taste. So if your company is too large to survey every individual, you can survey a representative sample of your population |
| **Sampling bias** | A sample isn't representative of the population as a whole. This means some members of the population are being over-represented or under-represented. |
| **Margin of error** | The maximum that the sample results are expected to differ from those of the actual population. The smaller the margin of error, the closer the results of the sample are to what the result would have been if you had surveyed the entire population. |
| **Confidence level** | How confident you are in the survey results. For example, a 95% confidence level means that if you were to run the same survey 100 times, you would get similar results 95 of those 100 times. Confidence level is targeted before you start your study because it will affect how big your margin of error is at the end of your study. |
| **Confidence interval** | The range of possible values that the population’s result would be at the confidence level of the study. This range is the sample result +/- the margin of error. |
| **Statistical significance** | The determination of whether your result could be due to random chance or not. The greater the significance, the less due to chance. Usually a statistical power of at least 0.8 or 80% is necessary to consider results statistically significant. |
| **Estimated response rate** | If you are running a survey of individuals, this is the percentage of people you expect will complete your survey out of those who received the survey. |

### Things to remember when determining the size of your sample

- Don’t use a sample size less than 30 - statistically proven (Central Limit Theorem (CLT)) that 30 is the smallest sample size where an average result starts to represent the average result of a population
- The confidence level most commonly used is 95%, but 90% can work in some cases
- Increase the sample size to meet specific needs of your project - use a larger sample size for a higher confidence level, to decrease the margin of error, or for greater statistical significance
- Sample sizes vary by business problem
- Weigh the cost against the benefits of more accurate results with a larger sample size

### Test your data using statistical power

:point_right: ***Statistical power*** is the probability of getting meaningful results from a test.

:point_right: ***Hypothesis testing*** is a way to see if a survey or experiment has meaningful results.

The larger the sample size, the greater the chance you'll have statistically significant results with your test. If a test is statistically significant, it means the results of the test are real and not an error caused by random chance. Usually, you need a statistical power of at least 0.8 or 80% to consider your results statistically significant.

### When data isn't readily available

Sometimes the data to support a business objective isn’t readily available, but ***proxy data*** can be used instead. You can also make use of open or public datasets.

| Business scenario | How proxy data can be used |
| --- | --- |
| A new car model was just launched a few days ago and the auto dealership can’t wait until the end of the month for sales data to come in. They want sales projections now | The analyst proxies the number of clicks to the car specifications on the dealership’s website as an estimate of potential sales at the dealership |
| A brand new plant-based meat product was only recently stocked in grocery stores and the supplier needs to estimate the demand over the next four years | The analyst proxies the sales data for a turkey substitute made out of tofu that has been on the market for several years |
| The Chamber of Commerce wants to know how a tourism campaign is going to impact travel to their city, but the results from the campaign aren’t publicly available yet | The analyst proxies the historical data for airline bookings to the city one to three months after a similar campaign was run six months earlier |

---

### Calculating sample size

To calculate sample size, you need:

- population size
- confidence level
- margin of error

The statistical method to calculate sample size is not a part of this course. For our purposes, an online sample size calculator can be used such as:

- [Sample size calculator by surveymonkey.com](https://www.surveymonkey.com/mp/sample-size-calculator/)
- [Sample size calculator by raosoft.com](http://www.raosoft.com/samplesize.html)

An example of a sample size calculation using an online calculator:

![Example Sample Size Calculator](/images/sample-size-calculator.png 'Example Sample Size Calculator')

### Consider the margin of Error

***Margin of error*** represents the maximum expected difference between sample results and the actual population data. It helps determine the accuracy of survey or test results by defining a range within which the true population average likely falls. A lower margin of error indicates that your sample's results are closer to what you would likely find by surveying the entire population. It can help you:

- understand how reliable the data from your hypothesis testing is
- determine how much you can generalize your findings from a sample to the entire population

> What does it mean?
>
>Once a drug study is complete and the results are in, the study finds the drug is 70% effective. By applying a *6% margin of error*, the actual effectiveness within the entire population is estimated to be between 64% and 76% (70% plus or minus 6%).

To calculate margin of error, you need:

- population size
- confidence level
- sample size

Again, this statistical method is not covered in this course and online calculators such as these can be used.

- [Margin of error calculator by Good Calculators (free online calculators)](https://goodcalculators.com/margin-of-error-calculator/)
- [Margin of error calculator by CheckMarket](https://www.checkmarket.com/sample-size-calculator/#sample-size-margin-of-error-calculator)

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
