# Team Project

## Description
The team project consists of two modules. Each module requires participants to apply the skills they have learned to date, and explore a dataset of their choosing. The first part of the team project involves creating a simple program with a database in order to analyze a dataset from an open source, such as Kaggle. In the second part of the team project, teams will come together again and apply the skills developed in each of the data science or machine learning foundations certificate streams. Teams will either create a data visualization or a machine learning model.

Participants will work in assigned teams of 4-5. 

#### Project Descriptions

* [First Team Project Description](./team_project_1.md)
* [Second Team Project Description](./team_project_2.md)

## Learning Outcomes
By the end of Team Project Module 1, participants will be able to:
* Resolve merge conflicts
* Describe common problems or challenges a team encounters when working collaboratively using Git and GitHub
* Create a program to analyze a dataset with contributions from multiple team members

By the end of Team Project Module 2, participants will be able to:
* Create a data visualization as a team
* Create a machine learning model as a team

### Contacts
**Questions can be submitted to the _#cohort-3-help_ channel on Slack**

* Technical Facilitator: 
  * **Kamilah Ebrahim**(she/her)
  kamilah.ebrahim@mail.utoronto.ca

* Learning Support Staff:

  * **Farzaneh Hashemi** (she/her )
  fhashemi.ma@gmail.com
  * **Tong Su** (she/her)
  tong.su@mail.utoronto.ca

### Delivery of Team Project Modules

Each Team Project module will include two live learning sessions and one case study presentation. During live learning sessions, facilitators will introduce the project, walk through relevant examples, and introduce various team skills that support project success. The remaining time will be used for teams to assemble and work on their projects, as well as get help from the facilitator or the learning support to troubleshoot any issues a team may be encountering. 

Work periods will also be used as opportunities for teams to collaborate and work together, while accessing learning support. 

### Schedule

|Day 1|Day 2|Day 3|Day 4|Day 5|
|-----|-----|-----|-----|-----|
|Live Learning Session |Live Learning Session|Case Study|Work Period|Work Period|

## Requirements
* Participants are expected to attend live learning sessions and the case study as part of the learning experience. Participants are encouraged to use the scheduled work period time to complete their projects.
* Participants are encouraged to ask questions and collaborate with others to enhance learning.
* Participants must have a computer and an internet connection to participate in online activities.
* Participants must not use generative AI such as ChatGPT to generate code to complete assignments. It should be used as a supportive tool to seek out answers to questions you may have.
* We expect participants to have completed the [onboarding repo](https://github.com/UofT-DSI/onboarding/tree/main/onboarding_documents).
* We encourage participants to default to having their camera on at all times, and turning the camera off only as needed. This will greatly enhance the learning experience for all participants and provides real-time feedback for the instructional team. 

### How to get help
![image](/steps-to-ask-for-help.png)

## Folder Structure

### Project 1
```markdown
|-- data
|---- processed
|---- raw
|---- sql
|-- reports
|-- src
|-- README.md
|-- .gitignore
```

### Project 2
```markdown
|-- data
|---- processed
|---- raw
|---- sql
|-- experiments
|-- models
|-- reports
|-- src
|-- README.md
|-- .gitignore
```

* **Data:** Contains the raw, processed and final data. For any data living in a database, make sure to export the tables out into the `sql` folder, so it can be used by anyone else.
* **Experiments:** A folder for experiments
* **Models:** A folder containing trained models or model predictions
* **Reports:** Generated HTML, PDF etc. of your report
* **src:** Project source code
* README: This file!
* .gitignore: Files to exclude from this folder, specified by the Technical Facilitator







Objective
The objective of this analysis is to guide the Toronto Police Services on how best to allocate
resources to manage auto theft in the Toronto region. This involves examining the dataset for
biases, potential errors, and patterns that can inform resource allocation strategies.
Data Cleaning and Preparation. More precisely, I investigated and generated writeup on the dataset to investigate biases potential errors.

1. Handling Old Data
o Deleted Rows: Rows where OCC_DATE is 2000 and 2001 were removed from the
dataset. These dates were considered too old and likely less relevant for current
analysis. Additionally, specific rows (1994, 3081, 17362, 56052) were deleted
due to the same reason. These rows were identified as potentially erroneous or
outdated data.

2. Handling Missing Geographic Data
o Rows with Zero Coordinates: A total of 717 rows contained zeros in both
LONG_WGS84 and LAT_WGS84 columns. These values are geographically
nonsensical for Toronto. Given the high number of such rows, they have been
retained in the dataset but flagged as containing missing or potentially erroneous
geographic data. They have not been deleted to preserve the dataset's
completeness. It is noted that these rows show "NSA" (Not Specified/Available)
in other columns, which reinforces their questionable reliability.
Data Analysis
1. Temporal Analysis

o Day of the Week (REPORT_DOW):
A pivot table was created with REPORT_DOW in Rows and
EVENT_UNIQUE_ID in Values. The analysis revealed that the number of
reports is significantly lower on Sundays compared to other days of the
week. This suggests that auto theft incidents might be less reported or
occur less frequently on Sundays.

o Time of Day (REPORT_HOUR):
Another pivot table was created with REPORT_HOUR in Rows and
EVENT_UNIQUE_ID in Values. The analysis indicated that the number of
reports peaks in the early morning hours, specifically at 6, 7, and 8 AM.
This pattern could suggest that auto theft incidents are more frequently
reported or occur during these early morning hours.

2. Geographic Analysis

o Neighborhood Analysis (NEIGHBOURHOOD_158):
A pivot table was created to examine the number of thefts across different
neighborhoods. It was observed that the neighborhood of West Humber-
Clairville has a disproportionately high number of reports compared to
other neighborhoods. This indicates a higher incidence of auto theft in this
area, which may require increased resources or targeted intervention.
Conclusion and Recommendations

Data Integrity: The dataset has been cleaned to remove outdated data and to flag rows
with missing geographic information. These rows have not been deleted to avoid loss of
valuable data but should be considered carefully in any further analysis.

Resource Allocation: Based on the analysis:
o Temporal Resource Allocation: Consider focusing resources on early morning
hours (6-8 AM) and reviewing reporting patterns on Sundays.
o Geographic Resource Allocation: Allocate additional resources to the West
Humber-Clairville neighborhood due to its high number of reported auto theft
incidents.






