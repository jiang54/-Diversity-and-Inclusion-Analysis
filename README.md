# Pwc Switzerland Power BI virtual case experience - Diversity and Inclusion Analysis


---
![Snipaste_2023-03-21_22-26-10](https://user-images.githubusercontent.com/24377958/226601999-a4047f01-bc22-44d5-82d4-19034c14e3af.png)
![Snipaste_2023-03-21_22-26-26](https://user-images.githubusercontent.com/24377958/226602048-b8eb3f86-503c-44e4-abad-d6e9cfb4ea9c.png)


# Table of Contents

- [Problem Statement](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Problem-Statement)
- [Data Sourcing](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Data-Sourcing)
- [Data Preparation](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Data-Preparation)
- [Data Modeling](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Data-Modeling)
- [Data Visualization](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Data-Visualization)
- [Data Analysis](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Data-Analysis)
- [Insights](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Insights)
- [Shareable link](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Shareable-Link)


---

# Problem Statement

The purpose of this analysis is to: 
- Define proper KPIs in hiring, promotion, performance and turnover
- Create a visualisation for the HR manager that reflects all relevant Key Performance indicators(KPIs)
and metrics in the dataset.

The following measures could help to define proper KPIs:
- '#' of men
- '#' of women
- '#' of leavers
- % employees promoted (FY21)
- % of women promoted
- % of hires men
- % turnover
- Average performance rating: men
- Average performance rating: women

---

# Data Sourcing

The Dataset used for this analysis was presented by [Pwc Switzerland](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html) and available at:

- [Diversity Inclusion Dataset](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis/blob/main/03%20Diversity-Inclusion-Dataset.xlsx)


---

# Data Preparation

Data transformation was done in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.

The diversity and inclusion dataset is given by a table named:

- `HR Manager` which has `32 columns and 500 rows` of observation


The tabulation below shows the `HR Manager` table with its column names and their description:
| Column Name | Description |
| ----------- | ----------- |
| Employee ID |   Represents the unique number of the employee in the dataset |
| Gender |  Describes the gender of the employee |
| Job Level after FY20 promotions |  Describes the job level of the employee after being promoted in FY20 |
| New hire FY20? |  Describes if the employee is a new hire in FY20 |
| FY20 Performance Rating |  Represents the performance rating of the  employee  in FY20 |
| Promotion in FY21? |  Describes if the employee is being promoted in FY21 |
| In base group for Promotion FY21 |  Describes if the employee is being selected for promoted in FY21 |
| Target hire balance |  Describes the target hire balance of the employee |
| FY20 leaver? |  Describes if the employee is a leaver in FY20 |
| In base group for turnover FY20 |  Describes if the employee is in a group for turnover in FY20 |
| Department @01.07.2020  |  Describes the department each employee belongs to as at January 7, 2020 |
| Leaver FY |  Describes if the employee is a leaver in a FY |
| Job Level after FY21 promotions |  Describes the job level of the employee after being promoted in FY21 |
| Last Department in FY20 |  Describes the last department each employee belongs in FY20 |
| FTE group |  Describes if the employee belongs to a FTE group |
| Time type |  Describes the contract type employee |
| Department & JL group PRA status |  Describes the department and JL group PRA status of the employee |
| Department & JL group for PRA |  Describes the department and JL group PRA  of the employee |
| Job Level group PRA status |  Describes the job level group PRA status of the employee |
| Job Level group for PRA |  Describes the job level group PRA of the employee |
| Time in Job Level @01.07.2020  |  Describes the time in job level of the employee |
| Job Level before FY20 promotions |  Describes the job level employee before being promoted in FY20 |
| Promotion in FY20? |  Describes if the employee is being promoted in FY20 |
| FY19 Performance Rating |  Describes the performance rating of the employee in FY19 |
| Age group |  Describes the age group of the employee |
| Age @01.07.2020 |  Represents the age of the employee as at January 07, 2020 |
| Nationality 1 |  Describes the nationality of the employee in state level |
| Region group: nationality 1 |  Describes the nationality of the employee in country level|
| Broad region group: nationality 1 |  Describes the nationality of the employee in regional level|
| Last hire date |  Describes the last hire date of the employee |
| Years since last hire |  Represents the number of years since last hire of the employee |
| Rand | generates random number for each entry in the dataset |


Data Cleaning for the dataset was done in power query as follows:

- Rows with missing values may carry important information and should not be indiscriminately removed
- Each of the columns in the table were validated to have the correct data type 

---

# Dataset from the excel

After the dataset was cleaned and transformed, it was ready to be add measures(using Power BI Desktop).

- The fact and dimension have been combined into one table and is shown in the data model below
![Snipaste_2023-03-21_22-37-05](https://user-images.githubusercontent.com/24377958/226595183-3777883b-7f1e-42a2-8f40-505370728888.png)

# Data Analysis (Add Necessary Measures)
![image](https://user-images.githubusercontent.com/24377958/226596525-fd0cb486-4ae9-4201-a80b-4e155e7fafcd.png)

`# of leaver = calculate(COUNTROWS('Pharma Group AG'),'Pharma Group AG'[FY20 leaver?] = "Yes")`

`# of men = calculate(count('Pharma Group AG'[Gender]),'Pharma Group AG'[Gender] = "Male")`

`# of women = calculate(count('Pharma Group AG'[Gender]),'Pharma Group AG'[Gender] = "Female")`

`% of employees promoted(FY21) = [employees promoted in FY21]/[total rows]`

`% of hires men = DIVIDE([hires men],[total rows])`

`% of hires women = DIVIDE([hires women],[total rows])`

`% of turnover = DIVIDE([FY20 leaver],[turnover])`

`% of women promoted = [women promoted] / [employees promoted in FY21]`

`employees promoted in FY21 = calculate(COUNTROWS('Pharma Group AG'),'Pharma Group AG'[Promotion in FY21?] = "Yes")`

`hires men = CALCULATE([total rows],'Pharma Group AG'[Gender] = "Male")`

`hires women = CALCULATE([total rows],'Pharma Group AG'[Gender] = "Female")`

`total rows = COUNTROWS('Pharma Group AG')`

`turnover = CALCULATE([total rows],'Pharma Group AG'[In base group for turnover FY20] = "Y")`

`women promoted = CALCULATE([employees promoted in FY21],'Pharma Group AG'[Gender] = "Female")`



# Data Visualization

Data visualization for the dataset is done in 2 parts to ensure a clearer and more effective presentation of the data.
![Snipaste_2023-03-21_22-26-10](https://user-images.githubusercontent.com/24377958/226601999-a4047f01-bc22-44d5-82d4-19034c14e3af.png)
![Snipaste_2023-03-21_22-26-26](https://user-images.githubusercontent.com/24377958/226602048-b8eb3f86-503c-44e4-abad-d6e9cfb4ea9c.png)

# Insights

Shown in [Data Visualization](https://github.com/jiang54/-Diversity-and-Inclusion-Analysis#Data-Visualization):


- In most cases where male and female are balanced, it suggests that the company values gender diversity and is committed to creating an inclusive workplace environment.
- The fact that female representation in Internal Services is half that of male representation (48 compared to 24) suggests that there may be a gender imbalance or bias in the hiring or promotion practices within that department. This could be an area for the company to focus on in order to promote greater gender diversity and equity within its workforce.
- The significant difference in efficiency between women and men (37% compared to 63%) suggests a potential gender-based bias or inequality that the company should address. Steps such as offering equal opportunities for training and development, addressing potential biases in performance evaluations and promotions, and promoting a more inclusive workplace culture may help. The company may also need to conduct further analysis to identify the underlying factors contributing to these differences and develop targeted interventions to address them.
---



# Virtual Case Experience Link

Virtual Case Experience: 

[Virtual Case Experience Website](https://www.theforage.com/virtual-internships/prototype/a87GpgE6tiku7q3gu/PwC-Digital-Up-skilling-Virtual-Case-Experience?ref=38HZaFghHQngHaj8b)
