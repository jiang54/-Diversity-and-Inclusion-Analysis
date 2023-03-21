# Pwc Switzerland Power BI virtual case experience - Diversity and Inclusion Analysis

![Snipaste_2023-03-21_22-26-10](https://user-images.githubusercontent.com/24377958/226592829-58e7834c-53e4-4487-8c02-3a397db7b97f.png)
![Snipaste_2023-03-21_22-26-26](https://user-images.githubusercontent.com/24377958/226592838-b170c744-e35d-406c-a6a1-148c2ec39878.png)
---


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

- Unnecessary columns were removed
- Unnecessary rows were filtered 
- Each of the columns in the table were validated to have the correct data type 

---

# Data Modeling

After the dataset was cleaned and transformed, it was ready to be modeled(using Power BI Desktop).

- The fact and dimension have been combined into one table and is shown in the data model below
