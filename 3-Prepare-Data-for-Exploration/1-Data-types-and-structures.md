# Data types and structures

## Table of contents

1. [Selecting the right data](#selecting-the-right-data)
2. [Data formats](#data-formats)
    - [Primary & Secondary](#primary--secondary)
    - [Internal & External](#internal--external)
    - [Continuous & Discrete](#continuous--discrete)
    - [Qualitative & Quantitative](#qualitative--quantitative)
    - [Nominal & Ordinal](#nominal--ordinal)
    - [Structured & Unstructured](#structured--unstructured)
    - [Long & Wide](#long--wide)
3. [Data modeling](#data-modeling)
    - [Types of data modeling](#types-of-data-modeling)
    - [Levels of data modeling](#levels-of-data-modeling)
    - [Data modeling techniques](#data-modeling-techniques)
4. [Data types](#data-types)
5. [Data transformation](#data-transformation)
6. [Module 1 Glossary](#module-1-glossary)

---

## Selecting the right data

Some data collection considerations to keep in mind:

- How will the data be collected?
- Which data sources will you use?
- Will it help you solve your business problem?
- How much data needs to be collected?
- What is your time frame?

Different data sources:

| Data type | Data source |
| --- | --- |
| **First-party data** | Data that you collect yourself |
| **Second-party data** | Collected directly by another group and then sold |
| **Third-party data** | Sold by a provider that didn’t collect the data themselves and might come from a number of different sources |

Use the flowchart below if data collection relies heavily on how much time you have:

![Data Selection Considerations](/images/data-selection-considerstions.png 'Data Selection Considerations')

---

## Data formats

### Primary & Secondary

:arrow_forward: ***Primary*** data is collected by a researcher from first-hand sources. Examples:

- Interviews conducted by you
- Customer survey results
- Employee questionnaires

:arrow_forward: ***Secondary*** data is gathered by other people or from other research. Examples:

- Data bought from a companies customer profiles
- Demographic data collected by a university
- Census data gathered by the federal government

### Internal & External

:arrow_forward: ***Internal*** data is stored inside a company’s own systems. Examples:

- Wages tracked by HR
- Sales data by store location
- Product inventory levels

:arrow_forward: ***External*** data is stored outside of a company or organization. Examples:

- National average wages
- Credit reports for customers of an auto dealership

### Continuous & Discrete

:arrow_forward: ***Continuous*** data is measured and can have almost any numeric value. Examples:

- Height (158.5cm, 6ft 2in)
- Runtime markers in a video
- Temperature

:arrow_forward: ***Discrete*** data is counted and has a limited number of values. Examples:

- Number of visitors on a daily basis (10, 20, 200)
- Maximum capacity allowed
- Tickets sold in the current month

### Qualitative & Quantitative

:arrow_forward: ***Qualitative*** data is subjective and an explanatory measure of a quality or characteristic. Example:

- Favorite exercise activity
- Brand with best customer service
- Fashion preferences

:arrow_forward: ***Quantitative*** data is specific and an objective measure, such as a number, quantity, or range. Examples:

- Percentage of board certified doctors who are women
- Population size of elephants
- Distance from Earth to Mars

### Nominal & Ordinal

:arrow_forward: ***Nominal*** data is a type of qualitative data that is categorized without a set order. Example:

- First time customer, returning customer, regular customer
- New job applicant, existing applicant, internal applicant
- New listing, reduced price listing, foreclosure

:arrow_forward: ***Ordinal*** data is a type of qualitative data with a set order or scale. Examples:

- Movie ratings (number of stars)
- Ranked-choice voting selections (1st, 2nd, 3rd)
- Satisfaction level measured in a survey

### Structured & Unstructured

:arrow_forward: ***Structured*** data is organized in a certain format, like rows and columns. Examples:

- Expense reports
- Tax returns
- Store inventory

:arrow_forward: ***Unstructured*** data cannot be stored as columns and rows in a relational database. Examples:

- Social media posts
- Emails
- Videos

The characteristics of structured and unstructured data:

![Structured and Unstructured Data](/images/data-structured-unstructured.png 'Structured and Unstructured data')

### Long & Wide

:arrow_forward: ***Wide data*** is preferred when:

- Creating tables and charts with a few variables about each subject
- Comparing straightforward line graphs

Here is an example of stock prices in wide format:

![Wide Data](/images/data-wide.png 'Wide Data')

An example dataset with data in wide format can be examined in [Google Sheets](https://docs.google.com/spreadsheets/d/1Ur1TiJn3KWtNgcnckxYXGt2ZPeOvduqCbP15eQrvhgQ/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c03m01-wide-long-data/c03m01-population-lac-data-wide.xlsx).

:arrow_forward: ***Long data*** is preferred when:

- Storing a lot of variables about each subject, e.g. 60 years worth of interest rates for each bank
- Performing advanced statistical analysis or graphing

Here is an example of stock prices in long format:

![Long Data](/images/data-long.png 'Long Data')

The same dataset used above, can be examined in long format in [Google Sheets](https://docs.google.com/spreadsheets/d/1Q7KbJrY7VQhOC4eiOOXcljPEpl7HVXaQu5sSOEiPv_4/edit?usp=sharing) or the [Excel File](/activities/spreadsheets/c03m01-wide-long-data/c03m01-population-lac-data-long.xlsx).

---

## Data modeling

***Data modeling*** is the process of creating diagrams that visually represent how data is organized and structured.  These visual representations are called ***data models***.

### Types of data modeling

| Type | Definition |
| --- | --- |
| **Conceptual** | High-level view of the data structure, i.e. how data interacts across an organization. Used to define the business requirements for a new database and doesn't contain technical details |
| **Logical** | Focuses on the technical details of a database such as relationships, attributes, and entities. Defines how individual records are uniquely identified in a database, but doesn't spell out actual names of database tables |
| **Physical** | Depicts how a database operates and defines all entities and attributes used, for example it includes table names, column names, and data types for the database |

### Levels of data modeling

Each level of data modeling has a different level of detail:

![Data Modeling Levels](/images/data-modeling-levels.png 'Data Modeling Levels')

### Data-modeling techniques

There are a lot of approaches. Common methods are:

:arrow_forward: ***Entity Relationship Diagram (ERD):*** a visual way to understand the relationship between entities in the data model

:arrow_forward: ***Unified Modeling Language (UML):*** very detailed diagrams that describe the structure of a system by showing the system's entities, attributes, operations, and their relationships

---

## Data types

A data type in a spreadsheet can be one of 3 things:

- a number,
- a text or string, or
- a Boolean.

Boolean data types have only two possible values: true or false. We can use Boolean operators to create single or multiple conditions in a Boolean statement. This creates a logical statements that filter results and can be used to a wide range of data analysis tasks. The Venn diagrams below illustrate how Boolean operators can be used to filter results.

![Boolean Logic](/images/boolean-logic.png 'Boolean Logic')

---

## Data transformation

Data transformation usually involves:

- Adding, copying, or replicating data
- Deleting fields or records
- Standardizing the names of variables
- Renaming, moving, or combining columns in a database
- Joining one set of data with another
- Saving a file in a different format

Why transform data?

| Goal | Why? |
| --- | --- |
| **Organization** | Better organized data is easier to use |
| **Compatibility** | Different applications or systems can then use the same data |
| **Migration** | Data with matching formats can be moved from one system to another |
| **Merging** | Data with the same organization can be merged together |
| **Enhancement** | Data can be displayed with more detailed fields |
| **Comparison** | Apples-to-apples comparisons of the data can then be made |

---

## Module 1 Glossary

| Term | Definition |
| --- | --- |
| **Agenda** | A list of scheduled appointments |
| **Audio file** | Digitized audio storage usually in an MP3, AAC, or other compressed format |
| **Boolean data** | A data type with only two possible values, usually true or false |
| **Continuous data** | Data that is measured and can have almost any numeric value |
| **Cookie** | A small file stored on a computer that contains information about its users |
| **Data element** | A piece of information in a dataset |
| **Data model** | A tool for organizing data elements and how they relate to one another |
| **Digital photo** | An electronic or computer-based image usually in BMP or JPG format |
| **Discrete data** | Data that is counted and has a limited number of values |
| **External data** | Data that lives, and is generated, outside of an organization |
| **Field** | A single piece of information from a row or column of a spreadsheet; in a data table, typically a column in the table |
| **First-party data** | Data collected by an individual or group using their own resources |
| **Long data** | A dataset in which each row is one time point per subject, so each subject has data in multiple rows |
| **Nominal data** | A type of qualitative data that is categorized without a set order |
| **Ordinal data** | Qualitative data with a set order or scale |
| **Ownership** | The aspect of data ethics that presumes individuals own the raw data they provide and have primary control over its usage, processing, and sharing |
| **Pixel** | In digital imaging, a small area of illumination on a display screen that, when combined with other adjacent areas, forms a digital image |
| **Population** | In data analytics, all possible data values in a dataset |
| **Record** | A collection of related data in a data table, usually synonymous with row |
| **Sample** | In data analytics, a segment of a population that is representative of the entire population |
| **Second-party data** | Data collected by a group directly from its audience and then sold |
| **Social media** | Websites and applications through which users create and share content or participate in social networking |
| **String data type** | A sequence of characters and punctuation that contains textual information (Refer to Text data type) |
| **Structured data** | Data organized in a certain format such as rows and columns |
| **Text data type** | A sequence of characters and punctuation that contains textual information (also called string data type) |
| **United States Census Bureau** | An agency in the U.S. Department of Commerce that serves as the nation’s leading provider of quality data about its people and economy |
| **Unstructured data** | Data that is not organized in any easily identifiable manner |
| **Video file** | A collection of images, audio files, and other data usually encoded in a compressed format such as MP4, MV4, MOV, AVI, or FLV |
| **Wide data** | A dataset in which every data subject has a single row with multiple columns to hold the values of various attributes of the subject |

---

Continue to next module: [Data responsibility](/3-Prepare-Data-for-Exploration/2-Data-responsibility.md)
