# Introducing data analytics and analytical thinking

> “Data! Data! Data!" he cried impatiently. "I can't make bricks without clay.”  
> *- Arthur Conan Doyle, The Adventure of the Copper Beeches - a Sherlock Holmes Short Story*

The foundation on which data analysis is built is data. Data analysts need data to draw conclusions, make predictions, and inform decisions.

## Data analytics knowledge

Data analysts must have a comprehensive understanding of the data analytics process, which is evidence by:

- a thorough understanding of data-driven decision-making and how it helps organizations guide their business strategy based on facts,
- knowing how to ask questions and make hypotheses about business problems, and how to use them as guidance through the data analysis process,
- the ability to verify data credibility and perform data validation,
- an understanding of data modeling and know how organizations use it as a tool to understand their data, and
- effectively communicate analysis insights to stakeholders by selecting and designing visualization.

## Data analytics technical skills

Data analyst must have the technical skills that allow them to complete the data analysis process. They use a variety of tools to analyze data such as spreadsheets, SQL, Tableau, and R to:

- join data from multiple sources to use for data analysis,
- sort data in both spreadsheets and databases,
- clean data by ensuring it contains no duplicate or incorrect entries, and that it is in the correct format,
- create data visualizations using spreadsheets, Tableau, and R,
- write SQL commands to select several columns from a table,
- select and install packages in R to complete specific tasks.

## Data Analysis Process

```mermaid
---
config:
  theme: dark
  look: classic
---

flowchart LR
%% Nodes
step1>"`**Ask**`"]:::pink
step2>"`**Prepare**`"]:::orange
step3>"`**Process**`"]:::yellow
step4>"`**Analyze**`"]:::green
step5>"`**Share**`"]:::blue
step6>"`**Act**`"]:::purple

%% Flow
step1 --> step2 --> step3 --> step4 --> step5 --> step6

%% Styling
classDef pink stroke:#C2185B,stroke-width:2px;
classDef orange stroke:#FB8C00,stroke-width:2px;
classDef yellow stroke:#FBC02D,stroke-width:2px;
classDef green stroke:#00897B,stroke-width:2px;
classDef blue stroke:#1976D2,stroke-width:2px;
classDef purple stroke:#8E24AA,stroke-width:2px;
```

By using **structured thinking**, we can break the data analysis process into smaller, more manageable parts by following this process:

| Step | Task | Meaning |
| --- | --- | --- |
| 1 | **Ask** | Define the problem and confirm stakeholder expectations |
| 2 | **Prepare** | Collect and store data for analysis |
| 3 | **Process** | Clean and transform data to ensure integrity |
| 4 | **Analyze** | Use data analysis tools to draw conclusions |
| 5 | **Share** | Interpret and communicate results to others to make data-driven decisions |
| 6 | **Act** | Put your insights to work in order to solve the original problem |

The data analysis process is designed to build on itself, so the results from each step are the inputs for the next step. This process involves four basic activities:

- recognizing the current problem or situation,
- organizing available information,
- revealing gaps and opportunities, and
- identifying available options

Aside from this data analysis process taught in during the course of the Google Data Analytics Professional Certificate, there are a few other variations of the data analysis process:

1. [EMC data analysis process](https://onlinelibrary.wiley.com/doi/pdf/10.1002/9781119183686)
2. [SAS iterative process](https://www.sas.com/content/dam/SAS/documents/marketing-whitepapers-ebooks/sas-whitepapers/en/manage-analytical-life-cycle-continuous-innovation-106179.pdf)
3. [Project-based data analytics process](https://pingax.com/Data%20Analyst/understanding-data-analytics-project-life-cycle/)
4. [Big data analytics process](https://www.informit.com/articles/article.aspx?p=2473128&seqNum=11&ranMID=24808)

## Analytical skills

Analytical skills are qualities and characteristics associated with solving problems using facts. Five essential aspects to analytical skills are:

| Aspect | Meaning |
| --- | --- |
| **Curiosity** | Seek out new challenges and experiences, which leads to knowledge |
| **Understanding context** | How you group things into categories |
| **Technical mindset** | Breaking processes down into smaller steps and working with them in an orderly, logical way |
| **Data Design** | How you organize information |
| **Data Strategy** | Managing the processes and tools used in data analysis |

## Analytical thinking

Analytical thinking involves identifying and defining a problem and then solving it by using data in an organized, step-by-step manner.

| Aspect | Meaning |
| --- | --- |
| **Visualization** | The graphical representation of information |
| **Strategy** | Key to staying focused and on track, determining what needs to be achieved the data and how to get there to improve the quality and usefulness of the data we collect |
| **Problem-orientation** | Used to identify, describe, and solve problems |
| **Correlation** | Recognizing relationships between data sets while understanding that correlation does not imply causation |
| **Big-Picture and Detail-Oriented Thinking** | Balancing the ability to see the overall view and the intricate details to innovate and execute plans |

## Root Cause

A **root cause** is the reason why a problem occurs. If we can identify and get rid of a root cause, we can prevent that problem from happening again. A question data analysts ask a lot is: *What is the root cause of a problem?*.  The process called **the Five Whys** can help us reveal to the root cause and to gain useful insights by simply asking "why" five times. An example of the Five Whys in action:

```mermaid
---
config:
    theme: dark
    look: classic
---

flowchart TB
%% Nodes
A([Complaint: Poor grocery deliveries])
B([Products arriving damaged])
C([Products not packaged properly])
D([Packers not adequately trained])
E([Packers not completed training])
root([**HR didn't provide training to new hires**])

%% Flow
A --Why?--> B
B --Why?--> C
C --Why?--> D
D --Why?--> E
E ==Why?==> root

%% Styling
style A stroke:#C2185B, stroke-width:2px;
style B stroke:#FB8C00,stroke-width:2px;
style C stroke:#FBC02D,stroke-width:2px;
style D stroke:#00897B,stroke-width:2px;
style E stroke:#1976D2,stroke-width:2px;
style root stroke:#8E24AA,stroke-width:2px;
```
