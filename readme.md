**Name:** Areeba\
**Roll no:** SU92-BSDSM-F24-068\
[Github](https://github.com/areeba-18/PF_FINAL_PROJECT.git)

Student Depression Analysis Project
===================================

_A comprehensive analysis of student depression data to uncover trends and insights for educational and mental health improvements._

Table of Contents
-----------------

- [Student Depression Analysis Project](#student-depression-analysis-project)
  - [Table of Contents](#table-of-contents)
- [Overview](#overview)
    - [Project Highlights:](#project-highlights)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Data Cleaning \& Preprocessing](#data-cleaning--preprocessing)
    - [Handling Missing Values:](#handling-missing-values)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
    - [Summary Statistics](#summary-statistics)
    - [Distribution of Key Variables](#distribution-of-key-variables)
- [Visualizations](#visualizations)
    - [1. **Bar Chart**: Depression Count by Gender](#1-bar-chart-depression-count-by-gender)
    - [2. **Pie Chart**: Depression Status Distribution](#2-pie-chart-depression-status-distribution)
    - [3. **Histogram**: Age Distribution](#3-histogram-age-distribution)
- [Grouping \& Aggregation](#grouping--aggregation)
- [Exporting Data](#exporting-data)
- [Insights and Recommendations](#insights-and-recommendations)
- [Images](#images)
  - [Age Distribution Analysis](#age-distribution-analysis)
  - [Blood Pressure Distribution](#blood-pressure-distribution)
  - [Gender Distribution](#gender-distribution)
  - [Age Group Distribution](#age-group-distribution)
- [Contact](#contact)

    

# Overview
--------

Welcome to the **Student Depression Analysis** project! This project analyzes a dataset containing various factors associated with student depression, including academic pressure, work pressure, mental health status, and lifestyle habits.

The primary goal is to identify patterns related to depression in students based on these factors and provide actionable insights that can aid in mental health interventions.

### Project Highlights:

*   **Data Cleaning**: Handling missing values and preprocessing data for better analysis.
    
*   **Exploratory Data Analysis (EDA)**: Visualizing trends, distributions, and relationships within the data.
    
*   **Insights**: Extracting key trends related to depression, work, and academic stress.
    

_Exploring the factors contributing to student depression to suggest ways to improve student mental health._

# Dataset
-------

The dataset used in this analysis contains key information about student depression. The columns in the dataset are as follows:

*   **id**: Unique identifier for each student.
    
*   **Gender**: Gender of the student (Male/Female).
    
*   **Age**: Age of the student.
    
*   **City**: The city where the student is based.
    
*   **Profession**: The student's profession (e.g., Student, Part-time Worker).
    
*   **Academic Pressure**: Level of pressure felt by the student in academics.
    
*   **Work Pressure**: Level of pressure felt by the student due to work.
    
*   **CGPA**: Cumulative Grade Point Average of the student.
    
*   **Study Satisfaction**: Satisfaction level regarding the student's study experience.
    
*   **Job Satisfaction**: Satisfaction level regarding the student's job, if applicable.
    
*   **Sleep Duration**: The average hours of sleep per night.
    
*   **Dietary Habits**: Type of diet followed by the student.
    
*   **Degree**: Type of academic degree being pursued.
    
*   **Suicidal Thoughts**: Whether the student has ever had suicidal thoughts.
    
*   **Work/Study Hours**: Total hours spent on work and study.
    
*   **Financial Stress**: Level of financial stress.
    
*   **Family History of Mental Illness**: Whether there is a family history of mental illness.
    
*   **Depression**: Whether the student is experiencing depression (Yes/No).
    

# Technologies Used
-----------------

*   **Python 3.x**: The primary programming language for data analysis.
    
*   **Pandas**: For data manipulation and cleaning.
    
*   **Matplotlib**: For generating plots and visualizations.
    
*   **Jupyter Notebook**: Interactive environment for conducting analysis and generating visual outputs.
    

# Data Cleaning & Preprocessing
-----------------------------

In this project, we performed data cleaning by handling missing values and renaming columns for better clarity.

### Handling Missing Values:

Missing values in the **Depression** column were filled using the mean value for that column. This ensured that we didn't lose data during analysis:

`   data["Depression %"] = data["Depression"].fillna(data["Depression"].mean())   `

Additionally, columns were renamed to enhance clarity:

*   **Work/Study Hours** → **Working hours**
    
*   **Have you ever had suicidal thoughts?** → **Suicidal thoughts?**
    

# Exploratory Data Analysis (EDA)
-------------------------------

### Summary Statistics

We started by generating summary statistics for numerical columns to understand the data distribution:
`   data.describe()   `

### Distribution of Key Variables

We explored the distribution of key variables such as **Age**, **Gender**, **Depression**, and **Academic Pressure**. For example, we used **value\_counts** to explore the distribution of gender and depression status:

`   data['Gender'].value_counts()   `

# Visualizations
--------------

### 1\. **Bar Chart**: Depression Count by Gender

We visualized the count of depression cases by gender using a stacked bar chart.

### 2\. **Pie Chart**: Depression Status Distribution

A pie chart was created to visualize the proportion of students with and without depression.

### 3\. **Histogram**: Age Distribution

A histogram was plotted to understand the distribution of students' ages.

# Grouping & Aggregation
----------------------

We grouped the data based on key features such as **City** and **Gender** to gain deeper insights into the data:

*   **Depression by City**: Analyzing depression counts by city.
    

```   data.groupby("City")['Depression'].value_counts()   ```

*   **Depression by Gender**: Analyzing depression counts by gender.
    
```   data.groupby("Gender")['Depression'].value_counts()   ```

# Exporting Data
--------------

After completing the data analysis, we exported the cleaned and processed dataset to a new CSV file for further use:

```   data.to_csv("Processed_Student_Data.csv")  ```

This file contains the cleaned and modified dataset, ready for reporting or sharing.

# Insights and Recommendations
----------------------------

1.  **Gender and Depression**: Male students had a higher incidence of depression compared to females. Further investigation into societal pressures may be required.
    
2.  **Academic Pressure**: Students reporting high academic pressure showed higher rates of depression. Stress management programs could help.
    
3.  **Sleep Duration**: Students with lower sleep duration had higher rates of depression. Adequate sleep needs to be encouraged.
    
4.  **Financial Stress**: Financial difficulties correlate with higher depression rates. Solutions to reduce financial stress could aid in reducing depression.
    

# Images
------

![Depression count by gender](/age_distibution.png)
Age Distribution Analysis
-------------------------

**Observations:**

*   The histogram displays a unimodal distribution with a peak around 55 years old.
    
*   The distribution is slightly skewed to the right.
    
*   The age range is from 20 to 75 years old.
    
*   Most people in the sample are in their 50s, with a significant number of individuals in their 40s and 60s.
    
*   There is a smaller number of individuals in their 20s and 70s.
--------------------------- 
![Bp](/bp.png)
Blood Pressure Distribution
---------------------------


This bar chart shows the frequency distribution of blood pressure (BP) readings.

**Key Findings:**

*   **High Frequency:** The most common BP readings are in the range of 90.6 to 140.9, with a peak around 90.6 and 120.8. This indicates a concentration of readings in the normal to slightly elevated range.
    
*   **Decreasing Trend:** As the BP readings increase, their frequency decreases. This is a general trend observed in BP distributions, suggesting a lower prevalence of higher BP levels.
    
*   **Wide Range:** The chart covers a broad range of BP values, indicating a diverse sample or population.
--------------
![Gender](/Gender.png) \
Gender Distribution
-------------------

The pie chart shows the distribution of genders in a dataset.

*   **Male:** The majority of the dataset is male.
    
*   **Female:** A smaller portion of the dataset is female.
--------------
![Age_distibution](/age_group.png) \
Age Group Distribution
-------------------------------


*   The graph depicts the distribution of individuals across different age groups.
    
*   The x-axis represents the age groups, and the y-axis represents the count of individuals in each group.
    
*   The highest number of individuals falls within the 51-60 age group, indicating a higher concentration of individuals in this range.
    
*   As age increases, the count of individuals generally decreases, suggesting a trend of fewer individuals in older age groups.
    
*   The trend suggests a typical population distribution with a higher density of younger individuals and a gradual decline in older age groups.
# Contact
-------

For any inquiries or collaborations, feel free to reach out:

*   **Github**: [Github](https://www.linkedin.com/in/ahmed-rasheed-7123701b6/)
    
*   **Email**: [areebazahid467@gmail.com](mailto:areebazahid467@gmail.com)
    

This is a clean and clear README for your project. Let me know if you'd like me to modify any section!