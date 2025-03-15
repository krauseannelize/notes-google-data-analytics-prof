# Visualize data

## Table of contents

1. [Why data visualization matters](#why-data-visualization-matters)
2. [Effective data visualizations](#effective-data-visualizations)
   - [Frameworks](#frameworks)
   - [Pre-attentive attributes](#pre-attentive-attributes)
3. [Connect images with data](#connect-images-with-data)
4. [Differentiate between correlation and causation](#correlation-and-causation)
5. [Evaluate patterns in data](#evaluate-patterns-in-data)
6. [Visualization decision tree](#visualization-decision-tree)
7. [Module 1 Glossary](#module-1-glossary)

---

## Why data visualization matters

***Data visualization*** is the graphic representation and presentation of data. It is crucial for presenting data insights in an understandable and compelling way. A good data visualization should be understandable within *five seconds*, allowing the audience to quickly grasp the message.

---

## Effective data visualizations

### Frameworks

Frameworks help organize your thoughts about data visualization, give you a useful checklist to reference as you plan and evaluate your data visualization, and are intended to improve the quality of your visuals.

#### The McCandless methods

[The McCandless method](https://www.informationisbeautiful.net/visualizations/what-makes-a-good-data-visualization/) lists four elements of good data visualization:

- **Information:** the data with which you’re working
- **Story:** a clear and compelling narrative or concept
- **Goal:** a specific objective or function for the visual
- **Visual form:** an effective use of metaphor or visual expression

An effective data visualizations combine all these elements to tell a story, leading viewers to the same conclusions drawn from the data analysis.

![McCandless method](/images/viz-framework-mccandless.png 'McCandless method')

#### Kaiser Fung's Junk Charts trifecta checkup

[Kaiser Fung's Junk Charts Trifecta checkup](https://junkcharts.typepad.com/junk_charts/junk-charts-trifecta-checkup-the-definitive-guide.html) encourages critical evaluation of visualizations by asking three questions:

- What is the practical question?
- What does the data say?
- What does the visual say?

![Junk Charts Trifecta checkup](/images/viz-framework-junk-chart.png 'Junk Charts Trifecta checkup')

### Pre-attentive attributes

Pre-attentive attributes are the elements of a data visualization that people recognize automatically and without conscious effort. The basic building blocks that make visuals immediately understandable are:

| MARKS: Basic visual objects such as points, lines, and shapes. Marks can be broken down into 4 qualities: |
| --- |
- *Position* | Where is a specific mark in space relative to a scale or to other marks?
- *Size* | How big, small, long, or tall is a mark?
- *Shape* | Does the shape of a specific object communicate something about it?
- *Color* | What color is a mark?

| CHANNELS: Visual aspects or variables that represent characteristics of the data in a visualization. It’s important to understand that channels vary in terms of how effective they are at communicating data based on 3 elements: |
| ---|
- *Accuracy* | Are the channels helpful in accurately estimating the values being represented?
- *Popout* | How easy is it to distinguish certain values from others?
- *Grouping* | How effective is a channel at communicating groups that exist in the data?

---

## Connect images with data

Choosing the right visualization is crucial for effectively communicating your analysis. Different visualizations are better suited for specific types of data and messages, such as:

| Visualization | Function |
| --- | --- |
| **Bar/Column graphs** | Uses rectangular bars (horizontal or vertical) to compare values across different categories |
| **Pie charts** | A circular graph showing proportions of a whole, where each slice represents a category |
| **Maps** | Presents data geographically, using colors, shading, or symbols to represent values in different locations |
| **Time series charts** | Tracks changes in data over time, with line graphs being a common type |
| **Distribution Graph** | A general term for visualizations that show the spread, frequency, or pattern of data, including histograms and density plots |
| **Histograms** | A type of distribution graph that displays the distribution of numerical data over a set range, using bars to represent frequency |
| **Correlation Chart** | A broad category of visualizations used to examine the relationship between two or more variables, with scatterplots being a common example |
| **Scatterplot** | Visualizes the relationship between two numerical variables by plotting individual data points on a grid |
| **Heatmap** | Uses color variations within a grid to represent data values, often showing the relationship between two variables or the distribution of a variable across multiple categories |

The [data visualization catalogue](https://datavizcatalogue.com/#google_vignette) features a range of different diagrams, charts, and graphs to help you find the best fit for your project. 

---

## Differentiate between correlation and causation

***Correlation*** is the measure of the degree to which two variables move in relationship to each other. Change in one variable tends to change in the other.

***Causation*** refers to the idea that an event leads to a specific outcome. Change in on variable directly cause change in the other.

For example, early mornings may cause people to drink more coffee and be in more car accidents. However, even though coffee drinking and car accidents might be correlated (meaning they tend to happen together), drinking coffee doesn't cause car accidents.

![Correlation vs Causation](/images/correlation-vs-causation.png 'Correlation vs Causation')

:warning: **Correlation doesn’t always imply causation, but causation always implies correlation.**

---

## Evaluate patterns in data

Meaningful patterns can take many forms, such as:

| Form | Pattern |
| --- | --- |
| **Change** | This is a trend or instance of observations that become different over time. A great way to measure change in data is through a line or column chart |
| **Clustering** | A collection of data points with similar or different values. This is best represented through a distribution graph |
| **Relativity** | These are observations considered in relation or in proportion to something else. You have probably seen examples of relativity data in a pie chart |
| **Ranking** | This is a position in a scale of achievement or status. Data that requires ranking is best represented by a column chart |
| **Correlation** | This shows a mutual relationship or connection between two or more things. A scatterplot is an excellent way to represent this type of data pattern |

---

## Visualization decision tree

![Visualization decision tree](/images/viz-decision-tree.png 'Visualization decision tree')

Key questions to determine the best visual source:

1. Does your data have only one numeric variable?
2. Are there multiple datasets?
3. Are you measuring changes over time?
4. Do relationships between the data need to be shown?

---

## Module 1 Glossary

| Term | Definition |
| --- | --- |
| **Alternative text** | Text that provides an alternative to non-text content, such as images and videos |
| **Annotation** | Text that briefly explains data or helps focus the audience on a particular aspect of the data in a visualization |
| **AVERAGEIF** | A spreadsheet function that returns the average of all cell values from a given range that meet a specified condition |
| **Balance** | The design principle of creating aesthetic appeal and clarity in a data visualization by evenly distributing visual elements |
| **Bar graph** | A data visualization that uses size to contrast and compare two or more values |
| **Calculus** | A branch of mathematics that involves the study of rates of change and the changes between values that are related by a function |
| **Causation** | When an action directly leads to an outcome, such as a cause-effect relationship |
| **Channel** | A visual aspect or variable that represents characteristics of the data in a visualization |
| **Chart** | A graphical representation of data from a worksheet |
| **Cluster** | A collection of data points on a data visualization with similar values |
| **CONVERT** | A SQL function that changes the unit of measurement of a value in data |
| **Correlation** | The measure of the degree to which two variables change in relationship to each other |
| **CREATE TABLE** | A SQL clause that adds a temporary table to a database that can be used by multiple people |
| **Data composition** | The process of combining the individual parts in a visualization and displaying them together as a whole |
| **Decision tree** | A tool that helps analysts make decisions about critical features of a visualization |
| **Design thinking** | A process used to solve complex problems in a user-centric way |
| **Distribution graph** | A data visualization that displays the frequency of various outcomes in a sample |
| **DROP TABLE** | A SQL clause that removes a temporary table from a database |
| **Dynamic visualizations** | Data visualizations that are interactive or change over time |
| **Emphasis** | The design principle of arranging visual elements to focus the audience’s attention on important information in a data visualization |
| **HAVING** | A SQL clause that adds a filter to a query instead of the underlying table that can only be used with aggregate functions |
| **Headline** | Text at the top of a visualization that communicates the data being presented |
| **Heat map** | A data visualization that uses color contrast to compare categories in a dataset |
| **Histogram** | A data visualization that shows how often data values fall into certain ranges |
| **Inner query** | A SQL subquery that is inside of another SQL statement |
| **Label** | Text in a visualization that identifies a value or describes a scale |
| **Legend** | A tool that identifies the meaning of various elements in a data visualization |
| **Line graph** | A data visualization that uses one or more lines to display shifts or changes in data over time |
| **Map** | A data visualization that organizes data geographically |
| **Mark** | A visual object in a data visualization such as a point, line, or shape |
| **MAXIFS** | A spreadsheet function that returns the maximum value from a given range that meets a specified condition |
| **Mental model** | A data analyst’s thought process and approach to a problem |
| **Movement** | The design principle of arranging visual elements to guide the audience’s eyes from one part of a data visualization to another |
| **MINIFS** | A spreadsheet function that returns the minimum value from a given range that meets a specified condition |
| **Narrative** | (Refer to story) |
| **Ordinal data** | Qualitative data with a set order or scale |
| **Pattern** | The design principle of using similar visual elements to demonstrate trends and relationships in a data visualization |
| **Pie chart** | A data visualization that uses segments of a circle to represent the proportions of each data category compared to the whole |
| **Pre-attentive attributes** | The elements of a data visualization that an audience recognizes automatically without conscious effort |
| **Proportion** | The design principle of using the relative size and arrangement of visual elements to demonstrate information in a data visualization |
| **R** | A programming language used for statistical analysis, visualization, and other data analysis |
| **Ranking** | A system to position values of a dataset within a scale of achievement or status |
| **Relativity** | The process of considering observations in relation or proportion to something else |
| **Repetition** | The design principle of repeating visual elements to demonstrate meaning in a data visualization |
| **Rhythm** | The design principle of creating movement and flow in a data visualization to engage an audience |
| **Scatterplot** | A data visualization that represents relationships between different variables with individual data points without a connecting line |
| **SELECT INTO** | A SQL clause that copies data from one table into a temporary table without adding the new table to the database |
| **Sort range** | A spreadsheet menu function that sorts a specified range and preserves the cells outside the range |
| **Sort sheet** | A spreadsheet menu function that sorts all data by the ranking of a specific sorted column and keeps data together across rows |
| **Static visualization** | A data visualization that does not change over time unless it is edited |
| **Story** | The narrative of a data presentation that makes it meaningful and interesting |
| **Subtitle** | Text that supports a headline by adding context and description |
| **Tableau** | A business intelligence and analytics platform that helps people visualize, understand, and make decisions with data |
| **Unity** | The design principle of using visual elements that complement each other to create aesthetic appeal and clarity in a data visualization |
| **Variety** | The design principle of using different kinds of visual elements in a data visualization to engage an audience |
| **Visual form** | The appearance of a data visualization that gives it structure and aesthetic appeal |
| **X-axis** | The horizontal line of a graph usually placed at the bottom, which is often used to represent time scales and discrete categories |
| **Y-axis** | The vertical line of a graph usually placed to the left, which is often used to represent frequencies and other numerical variables |

---

Continue to next course: [Create data visualization with Tableau](/6-Share-Data-Through-the-Art-of-Visualization/2-Create-data-visualizations-in-Tableau.md)
