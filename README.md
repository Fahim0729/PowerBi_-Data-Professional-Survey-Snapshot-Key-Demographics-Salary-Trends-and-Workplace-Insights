## 📊 Data Professional Survey Analysis: Key Demographics, Salary Trends, and Workplace Insights

##### 🟩 This survey provides a comprehensive overview of data professionals, exploring their demographics, salary patterns, programming preferences, and overall work satisfaction to reveal key trends and insights within the industry.

---

🛠️ **Tools Used**

- **Power BI:** Dashboarding and visual analysis (Card, Line, Area, Stacked Column, Pie, Gauge, Treemap)

- **Power Query & DAX:** Data cleaning, transformation, and calculated metrics (e.g., Average Salary)

- **Excel / CSV:**  Raw data storage and inspection

- **Data Modeling:** Linking datasets via Unique ID for relational analysis

**Purpose:** Enabled clean, standardized data and actionable insights for reporting.

---

📊 **Data Overview**

<div align="center">

| Attribute       | Value                                                                                                                                                         |
|:---------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Survey Size     | 630                                                                                                                                                           |
| Missing Values  | None                                                                                                                                                          |
| Data Sources    | [Demographics](Demographics.xlsx), [Career & Compensation](https://github.com/Fahim-Hossain-Data/PowerBi_Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/f5c5e75b524661b01b47b8d0badcb696b88d873d/Career%20%26%20Compensation.xlsx), [Job Satisfaction & Survey](https://github.com/Fahim-Hossain-Data/PowerBi_Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/f5c5e75b524661b01b47b8d0badcb696b88d873d/Job%20Satisfaction%20%26%20Survey.xlsx) |

</div>

---

🗄️ **Data Modeling & Dashboard**

Initially, three dataset were loaded into Power BI. These datasets are connected using a Unique ID. The figure below illustrates the data model.
<p align="center">
  <img src="https://github.com/Fahim0729/PowerBi_-Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/a9b0aba0c9a0e960bdaad406e8a066decc8629fc/Data_Modeling.png" alt="Histogram" width="600"/>
  <br>
  <em>Figure: Conceptual Data Model and Relationships </em>
</p>


📊 The dashboard includes interactive visualizations such as Card, Area Chart, Line Chart, Stacked Column Chart, Pie Chart, Gauge, and Treemap to explore demographics, salaries, programming preferences, and workplace satisfaction is shown below:

<p align="center">
  <img src="https://github.com/Fahim0729/PowerBi_-Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/a9b0aba0c9a0e960bdaad406e8a066decc8629fc/DashBoard.png" alt="Histogram" width="600"/>
  <br>
  <em>Figure: Power BI Dashboard for Data Visualization </em>
</p>

---

## 📝 Key Findings

Here are the main insights derived from the survey:

🟩 Survey respondents:  A total of 630 data professionals from various countries participated in this survey.

🟩 Average age of responds: The average age of a survey respondent is **29.87 years**, indicating a relatively young workforce.

🟩 Salary Insights:  Data Scientists earn the highest salaries among the surveyed roles. The top three roles are:
- **Data Scientists:** $94.04k
- **Data Engineers:** $65.29k
- **Data Architects:** $64.00k

🟩 Country Participation: The **United States** was the most responsive country, contributing **261** responses. **Canada** had the fewest respondents.

🟩 Gender pay gap: While the gender split is nearly even (Male: 50.81%, Female: 49.19%), males earn a slightly higher average salary, pointing to a small but present gender pay gap within this survey group.

🟩 Age vs Salary Satisfaction: 
- **Younger and mid-career professionals** experience the most significant **fluctuations** in happiness, with ratings ranging from 3 to 8 out of 10.
- **Older respondents (aged 66 and above)** report a much more stable outlook, with happiness consistently rating around a **5 out of 10**.

🟩 Programming Language Preferences: **Python** is the overwhelming favorite. On the other end of the spectrum, **Java** was identified as the least popular language in this survey.

🟩 Workplace Satisfaction: 
- **Work/Life Balance:** Received a moderate average rating of **5.74/10**.

- **Coworker Relationships:** Was rated slightly higher, at **5.86/10**.

---

## 🔧 Data Preprocessing

This section outlines the data cleaning and transformation steps applied to prepare the raw survey data for analysis. 

📝 **Salary Range → Average Salary**

- Converted ranges (e.g., “50k-65k”) to numeric values

- Handled “150k+” as 225k

- Calculated Average Salary:
    ```
    (Minimum Salary + Maximum Salary) / 2
    ```


📝 **Standardizing “Other” Categories**

- Split write-ins in columns like Favorite Programming Language or Industry using "(" or ":" as delimiters

- Kept only the main category **Other**, removing any attached text or descriptions in parentheses or after a colon

---

## 📌 Conclusion

This analysis provides key insights into data professionals’ demographics, salaries, programming preferences, and workplace satisfaction. The cleaned and standardized data ensures accurate results, offering a valuable reference for industry trends and decision-making.

---

## 🌐 I’d Love to Connect!

- **LinkedIn:** [Md Fahim Hossain](https://www.linkedin.com/in/yourprofile)  
- **Email:** [fahimhossain0729@gmail.com](mailto:fahimhossain0729@gmail.com)


<div align="center">
  
**[⬆ Back to Top](#top)**

</div>
