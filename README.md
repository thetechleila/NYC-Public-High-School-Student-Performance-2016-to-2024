# NYC Public High School Student Performance and Educational Outcomes Across the 5 Boroughs from 2016-2024

## Project Overview

The goal of this project is to find insights, trends and patterns among the NYC Public High School Student performance to determine which demographic and socio-economic factors/combinations of factors may have impacted educational outcomes such as attendance, absenteeism, Regents Exam results, dropout rates, and high school graduation rates.

Data from before (pre-2020) and after the Covid-19 Lockdown was compared and analyzed to establish a baseline from which to evaluate changes from school year to school year (2016-2024).

## Data Sources

Information about the NYC Public High School Student population and its educational outcomes was obtained from _[NYC Open Data](https://opendata.cityofnewyork.us/)_ - free public data published by New York City agencies and other partners - and other official NYC Government data resources.

The following datasets were used:

  - **[2016-17 - 2020-21 End-of-Year Borough Attendance and Chronic Absenteeism Data](https://data.cityofnewyork.us/Education/2016-17-2020-21-End-of-Year-Borough-Attendance-and/peyw-qepe/about_data)** 
    - Starts during the 2016-17 school year and ends with the 2020-21 school year organized by borough
    - Overall attendance data include students in (school) Districts 1-32
    - District 75 (Special Education) and Students in District 79 (Alternative Schools & Programs), charter schools, home schooling, and home and hospital instruction are excluded.

  - **[2018-19 - 2023-24 End-of-Year Borough Attendance and Chronic Absenteeism Data](https://infohub.nyced.org/reports/students-and-schools/school-quality/information-and-data-overview/end-of-year-attendance-and-chronic-absenteeism-data)** 
    - Available as an Excel Workbook through NYC Public Schools InfoHub 
    - Starts during the 2018-19 school year and ends with the 2022-23 school year organized by borough

  - **[Graduation Results for Cohorts 2012 to 2019 (Classes of 2016 to 2023)](https://data.cityofnewyork.us/Education/Graduation-results-for-Cohorts-2012-to-2019-Classe/mjm3-8dw8/about_data)**
    - The cohort consists of all students who first entered 9th grade in a given school year (e.g., the Cohort of 2006 entered 9th grade in the 2006-2007 school year). 
    - Graduates are defined as those students earning either a Local or Regents diploma.
    - Available as an Excel Workbook through NYC Public Schools InfoHub 

  - **[2015 - 2023 Regents Exam Results](https://infohub.nyced.org/reports/academics/test-results)**
    - Available as an Excel Workbook through NYC Public Schools InfoHub 
    - Results include all administrations of Regents exams in each school year and reports the highest score for each student for each Regents exam taken in each school year. 
    - The Regents Excel file contains results for all students tested, as well as results by student characteristics including disability status, English Language Learner (ELL) status, race/ethnicity, and gender


## Project Phases

The project was completed in 3 Phases:

_**Phase 1: Research & Exploratory Data Analysis**_

  - Researched foundational and contextual information about the NYC Public School system and how student data is measured and categorized.
  - Identification and examination of relevant verified datasets regarding the topic in the preferred formats (CSV or Excel).
  - Conducted multivariate exploratory data analyses into trends and patterns occurring across all chosen datasets to compile a complex evidence based data story on the educational outcomes for high school students 2016-2024 across selected demographics.
  - Created visualizations of data trends in NYC Public HS Student info from 2016-2024

_**Phase 2: ETL Pipeline & PostgreSQL Data Models**_

  - Creation of Conceptual and Logical PostgreSQL Data Models:
    - Designed high level conceptual data model that identified the main entities and their relationships to each other in general terms
    - Constructed logical data model that detailed primary keys, ID values, and constraints to ensure uniqueness and guarantee no null values

  - Creation of an ETL Pipeline that:
    - Extracted locally stored dataset csv files and Excel Workbooks
    - Cleaned, standardized and amalgamated the 4 source datasets into one consistent source of truth, merged using 3 common traits
    - Loaded this Single Source of Truth table into the PostgreSQL database specifically for the project utilizing psycopg2 to transport data from VSCode to PostgreSQL
    - Saving of Single Source of Truth Table as CSV file


_**Phase 3: Creation of Interactive Tableau Dashboard**_

Utilize final Single Source of Truth table to create an informative and interactive dashboard in Tableau that visualizes answers how NYC Public High School Performance, Educational Outcomes and Demographics have changed pre and post Covid-19 (2016-2024)

## Tools

- Python
- Psycopg2
- NumPy for mathematical & statistical operations
- Pandas for data manipulation
- Matplotlib & Seaborn for data visualization
- Microsoft Excel & Pages for Mac
- Jupyter Notebooks
- VSCode
- PostgreSQL
- Tableau Public for Desktop


