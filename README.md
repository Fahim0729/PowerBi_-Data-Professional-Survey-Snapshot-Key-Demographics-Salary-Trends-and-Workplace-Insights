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

🗄️ Initially, three datasets—Demography, Career & Compensation, and Job Satisfaction & Survey—were loaded into Power BI. These datasets are connected using a Unique ID. The figure below illustrates the data model.
<p align="center">
  <img src="https://github.com/Fahim0729/PowerBi_-Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/a9b0aba0c9a0e960bdaad406e8a066decc8629fc/Data_Modeling.png" alt="Histogram" width="600"/>
  <br>
  <em>Figure: Conceptual Data Model and Relationships </em>
</p>


📊 The Power BI dashboard, shown below, includes the following visualizations: Card, Area Chart, Line Chart, Stacked Column Chart, Pie Chart, Gauge, and Treemap.

<p align="center">
  <img src="https://github.com/Fahim0729/PowerBi_-Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/a9b0aba0c9a0e960bdaad406e8a066decc8629fc/DashBoard.png" alt="Histogram" width="600"/>
  <br>
  <em>Figure: Power BI Dashboard for Data Visualization </em>
</p>

---

## 📝 Key Findings: Q&A Summary

Here are the main insights derived from the 630 survey respondents.

🟩 survey respondents:  A total of 630 data professionals from various countries participated in this survey.

🟩 average age of responds: The average age of a survey respondent is **29.87 years**, indicating a relatively young workforce.

🟩 Salary Insights: 
- **Data Scientists:** $94.04k
- **Data Engineers:** $65.29k
- **Data Architects:** $64.00k

🟩 Country Participation: The **United States** was the most responsive country, contributing **261** responses. **Canada** had the fewest respondents.

🟩 gender pay gap: While the gender split is nearly even (Male: 50.81%, Female: 49.19%), males earn a slightly higher average salary, pointing to a small but present gender pay gap within this survey group.

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

### 1. Salary Range Processing and Average Salary Calculation

The raw data contained salary information as text ranges (e.g., "50k-65k"). To perform numerical analysis, this column was processed to calculate a single average salary figure for each respondent.

- **💾 Preservation:** The original salary range column was duplicated to maintain the raw data's integrity.
- **✂️ Splitting:** The duplicated column was split to extract the minimum and maximum salary values. This was achieved by separating the string based on the transition from a digit to a non-digit character (the hyphen).
- **🧹 Cleaning:**
    - Textual characters like "k" (representing thousands) and hyphens ("-") were removed.
    - The plus symbol ("+"), used in ranges like "150k+", was replaced with a value of **225** to serve as a standardized estimated upper bound (representing 225k).
- **🔢 Type Conversion:** The cleaned minimum and maximum salary columns were converted from text to numeric data types to enable mathematical operations.
- **➗ Average Calculation:** A new custom column was created to calculate the average salary for each respondent using the following formula:
    ```
    (Minimum Salary + Maximum Salary) / 2
    ```
- **📈 Result:** This new `Average Salary` column was used for all salary-related analysis in the report.

---

### 2. Handling "Other" Categories with Subsections

Several categorical columns, such as "Favorite Programming Language" or "Industry," contained an "Other" option where respondents could provide a specific write-in answer within parentheses `()` or after a colon `:`. To maintain categorical consistency while preserving the original response, the following steps were taken:

- **🧩 Isolation:** The column was split using a delimiter (specifically, `(` or `:`) to separate the main "Other" category from the respondent's specific, descriptive text.
- **📂 Temporary Storage:** The extracted descriptive text was placed into a new temporary column.
- **🧹 Cleanup:** The temporary column containing the specific details was reviewed and then deleted, as it was not needed for high-level categorical aggregation.
- **✅ Standardization:** The original target column was retained with all values standardized to the main category (e.g., all entries became simply "Other" instead of "Other (specific reason)").

---

## 📌 Conclusion

This analysis provides key insights into data professionals’ demographics, salaries, programming preferences, and workplace satisfaction. The cleaned and standardized data ensures accurate results, offering a valuable reference for industry trends and decision-making.


<div align="center">
  
**[⬆ Back to Top](#top)**

</div>
