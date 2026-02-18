## 📊 Data Professional Survey Analysis: Key Demographics, Salary Trends, and Workplace Insights

##### This survey provides a comprehensive overview of data professionals, exploring their demographics, salary patterns, programming preferences, and overall work satisfaction to reveal key trends and insights within the industry.


![Data_Modeling](https://github.com/Fahim0729/PowerBi_-Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/a9b0aba0c9a0e960bdaad406e8a066decc8629fc/Data_Modeling.png)



![Dashboard](https://github.com/Fahim0729/PowerBi_-Data-Professional-Survey-Snapshot-Key-Demographics-Salary-Trends-and-Workplace-Insights/blob/a9b0aba0c9a0e960bdaad406e8a066decc8629fc/DashBoard.png)



## 📝 Key Findings: Q&A Summary

Here are the main insights derived from the 630 survey respondents.

**👥 1. How many professionals participated in this survey?**
A total of **630** data professionals from around the globe took part in this survey.

**📅 2. What is the average age of the survey respondents?**
The average age of a survey respondent is **29.87 years**, indicating a relatively young workforce.

**💰 3. Which occupation commands the highest salary, and what are the top earners?**
**Data Scientists** are the highest-paid professionals in this survey, earning an impressive average salary of **$94.04k**. They are followed by:
- **Data Engineers:** $65.29k
- **Data Architects:** $64.00k

**🌍 4. Which countries had the highest and lowest representation in the survey?**
The **United States** was the most responsive country, contributing **261** responses. **Canada** had the fewest respondents.

**⚥ 5. Is there a gender pay gap among respondents?**
While the gender split is nearly even (Male: 50.81%, Female: 49.19%), males earn a slightly higher average salary, pointing to a small but present gender pay gap within this survey group.

**📈 6. How does satisfaction with salary change as professionals age?**
- **Younger and mid-career professionals** experience the most significant **fluctuations** in happiness, with ratings ranging from 3 to 8 out of 10.
- **Older respondents (aged 66 and above)** report a much more stable outlook, with happiness consistently rating around a **5 out of 10**.

**💻 7. Which programming languages are the most and least popular?**
**Python** is the overwhelming favorite. On the other end of the spectrum, **Java** was identified as the least popular language in this survey.

**⚖️ 8. How do professionals rate their workplace satisfaction?**
- **Work/Life Balance:** Received a moderate average rating of **5.74/10**.
- **Coworker Relationships:** Was rated slightly higher, at **5.86/10**.

---

## 🔧 Data Preprocessing

This section outlines the data cleaning and transformation steps applied to prepare the raw survey data for analysis. The primary tools used were Power Query (or a similar data transformation tool) to ensure accuracy and consistency.

### 1. Salary Range Processing and Average Salary Calculation

The raw data contained salary information as text ranges (e.g., "50k-65k"). To perform numerical analysis, this column was processed to calculate a single average salary figure for each respondent.

- **Preservation:** The original salary range column was duplicated to maintain the raw data's integrity.
- **Splitting:** The duplicated column was split to extract the minimum and maximum salary values. This was achieved by separating the string based on the transition from a digit to a non-digit character (the hyphen).
- **Cleaning:**
    - Textual characters like "k" (representing thousands) and hyphens ("-") were removed.
    - The plus symbol ("+"), used in ranges like "150k+", was replaced with a value of **225** to serve as a standardized estimated upper bound (representing 225k).
- **Type Conversion:** The cleaned minimum and maximum salary columns were converted from text to numeric data types to enable mathematical operations.
- **Average Calculation:** A new custom column was created to calculate the average salary for each respondent using the following formula:
    ```
    (Minimum Salary + Maximum Salary) / 2
    ```
- **Result:** This new `Average Salary` column was used for all salary-related analysis in the report.

### 2. Handling "Other" Categories with Subsections

Several categorical columns, such as "Favorite Programming Language" or "Industry," contained an "Other" option where respondents could provide a specific write-in answer within parentheses `()` or after a colon `:`. To maintain categorical consistency while preserving the original response, the following steps were taken:

- **Isolation:** The column was split using a delimiter (specifically, `(` or `:`) to separate the main "Other" category from the respondent's specific, descriptive text.
- **Temporary Storage:** The extracted descriptive text was placed into a new temporary column.
- **Cleanup:** The temporary column containing the specific details was reviewed and then deleted, as it was not needed for high-level categorical aggregation.
- **Standardization:** The original target column was retained with all values standardized to the main category (e.g., all entries became simply "Other" instead of "Other (specific reason)").

**Benefit:** This process improved data cleanliness and ensured accuracy in aggregations and visual analysis by preventing each unique write-in response from being treated as its own separate category.

---

## 📂 Files in this Repository

- `data/` - Contains the raw and processed survey data.
- `notebooks/` - Jupyter notebooks or Power BI files used for analysis.
- `README.md` - This file, containing the project summary and documentation.

## 🛠️ Tools Used

- **Data Processing:** Power Query (Excel / Power BI)
- **Analysis & Visualization:** [e.g., Power BI Desktop, Python, etc.]
