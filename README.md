# HIRING PROCESS ANALYTICS #
## PROJECT DESCRIPTION: ##
The objective of this project is to analyze the company's hiring process data and draw meaningful insights from it. The hiring process is a crucial function of any company, and understanding trends such as the number of rejections, interviews, job types, and vacancies can provide valuable insights for the hiring department. As a data analyst, we are given a dataset containing records of previous hires. Our job is to analyze this data and answer certain questions that can help the company improve its hiring process.

##  APPROACH: ##
The database file was provided in the attachment. The excel file was carefully observed for missing values, duplicate values and outliers for further analysis. With the help of Power Query editor these values were either altered or removed based on the context of analysis.

## TECH- STACK USED: ##
The software I am using to do the analysis is Microsoft Excel It is a very powerful tool to filter data and plot various graphs to get insights about hiring process of the organization. The Power Query Editor is very helpful to detect any anomalies in the data as well as correct them.

## DATASET OVERVIEW: ##
The dataset contains 7,168 records of candidates who were interviewed previously and the columns includes the following:
+ application_id: ID of the applicant
+ Interview Taken on: Date and time of the interview
+ Status: Hired/ rejected
+ event_name: Gender of the applicant
+ Department: Name of the department for which interview was conducted
+ Post Name: Name of the post offered
+ Offered Salary: Salary offered for the job

## DATA CLEANING: ##
#### Handling Missing Values: ####
+ Column event_name has 15 rows with ‘-‘ as its values. These can be termed as Null values. We replaced it with “Don’t want to say” as they both implies the same thing in context of this project.
+ Column Offered Salary has 1 row with null value. The corresponding value in Department column is “Sales Department” and Post Name is “i7”. So, we replaced it
with median of Offered Salary for Sales Department and i7 Post Name. The median came out to 45400.
+ Column Post Name has 1 row with “-“ as its value. It can be termed as Null value. The corresponding value in Department column is “Sales Department” and Offered Salary is “85914”. So we replaced it with majority count of Posts for candidates in Sales Department and whose Offered Salary is between 80,000 and 90,000, which is “c5”.
#### Handling Outliers: ####
I created a Box plot for column Offered Salary and found that three values can be termed as outliers. We replaced them with median value os Offered Salary for corresponding Department and Post Name.

#### Handling Duplicate Values: ####
Column application_id has 54 rows with duplicate values. As application_id is a unique id and can’t be repeated, we removed them from the dataset for the correct analysis.

## Data Analytics Tasks: ##
After downloading the dataset, use Excel to answer the below questions:
#### A. Hiring Analysis: ####
The hiring process involves bringing new individuals into the organization for various roles.
Your Task: Determine the gender distribution of hires. How many males and females have been hired by the company?
#### B. Salary Analysis: ####
The average salary is calculated by adding up the salaries of a group of employees and then dividing the total by the number of employees.
Your Task: What is the average salary offered by this company? Use Excel functions to calculate this.
#### C. Salary Distribution: ####
Class intervals represent ranges of values, in this case, salary ranges. The class interval is the difference between the upper and lower limits of a class.
Your Task: Create class intervals for the salaries in the company. This will help you understand the salary distribution.
#### D. Departmental Analysis: ####
Visualizing data through charts and plots is a crucial part of data analysis.
Your Task: Use a pie chart, bar graph, or any other suitable visualization to show the proportion of people working in different departments.
#### E. Position Tier Analysis: ####
Different positions within a company often have different tiers or levels.
Your Task: Use a chart or graph to represent the different position tiers within the company. This will help you understand the distribution of positions across different tiers.
