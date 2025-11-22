# Data cleaning is a must

---

# Clean it up!

### **Key Points**

- **Dirty data is a major problem:** It costs businesses trillions of dollars annually and is often caused by human error.
- **Clean data is essential for reliable data analysis:** It ensures accurate and relevant results.
- **Data cleaning is a crucial process:** It involves identifying and correcting errors in data to make it usable for analysis.

### **Definitions**

- **Dirty data:** Incomplete, incorrect, or irrelevant data that can lead to inaccurate analysis results.
- **Clean data:** Complete, correct, and relevant data that is essential for reliable analysis.
- **Data integrity:** The accuracy and consistency of data, which is crucial for reliable analysis.

### **Content Summary**

The video begins by highlighting the significant cost of poor quality data to businesses, emphasizing the importance of data integrity for reliable analysis. It then defines dirty data and provides examples of how human error can lead to data inaccuracies. The video then introduces the concept of clean data and its importance for achieving data integrity.

The video concludes by emphasizing the importance of data cleaning and provides a preview of upcoming lessons that will teach learners how to identify and correct errors in data.

### **Additional Notes**

- The video emphasizes the importance of clean data for reliable data analysis.
- The video provides a clear definition of dirty data and its impact on businesses.
- The video introduces the concept of data cleaning and its importance for achieving data integrity.

---

# Why data cleaning is critical

### **Key Points**

- **Dirty data:** Incomplete, incorrect, or irrelevant data that hinders analysis.
- **Clean data:** Complete, correct, and relevant data that enables effective analysis.
- **Importance of data cleaning:**
    - Prevents inaccurate insights and costly mistakes.
    - Enables effective analysis and decision-making.
    - Improves data quality and reliability.
- **Data cleaning process:**
    - Identifying and correcting errors.
    - Removing duplicates and inconsistencies.
    - Filling in missing values.
    - Formatting data consistently.
- **Data cleaning tools:**
    - Spreadsheet software (e.g., Excel, Google Sheets)
    - SQL databases
    - Data cleaning libraries (e.g., Pandas in Python)
- **Benefits of data cleaning:**
    - Improved data quality and reliability.
    - More accurate analysis and insights.
    - Better decision-making.
    - Increased efficiency and productivity.

### **Definitions**

- **Data cleaning:** The process of identifying and correcting errors in data to make it more accurate and reliable.
- **Dirty data:** Data that is incomplete, incorrect, or irrelevant.
- **Clean data:** Data that is complete, correct, and relevant.
- **Data integrity:** The accuracy and consistency of data.
- **Data validation:** The process of checking data for errors.
- **Data transformation:** The process of converting data from one format to another.

### **Additional Notes**

- Data cleaning is an essential part of the data analysis process.
- There are many different data cleaning tools available.
- The specific data cleaning techniques used will vary depending on the type of data and the specific problem being addressed.

### **Real-life examples**

- A company that uses dirty data to make decisions about its marketing campaigns may waste money on ineffective campaigns.
- A hospital that uses dirty data to make decisions about patient care may put patients at risk.
- A financial institution that uses dirty data to make decisions about investments may lose money.

---

# What is dirty data?

Earlier, we discussed that **dirty data** is data that is incomplete, incorrect, or irrelevant to the problem you are trying to solve.  This reading summarizes:

- Types of dirty data you may encounter
- What may have caused the data to become dirty
- How dirty data is harmful to businesses

## Types of dirty data

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/apsqUaUcTWabKlGlHK1mGw_2d181a03a4c6408aa1b7be625c6f9c97_Screen-Shot-2021-01-24-at-11.51.49-PM.png?expiry=1716854400000&hmac=d8_pnaq8qdwYTYld7FFwzz90mw2ES9lfmkqzX-7Yus8)

### **Duplicate data**

| **Description** | **Possible causes** | **Potential harm to businesses** |
| --- | --- | --- |
| Any data record that shows up more than once | Manual data entry, batch data imports, or data migration | Skewed metrics or analyses, inflated or inaccurate counts or predictions, or confusion during data retrieval |

### **Outdated data**

| **Description** | **Possible causes** | **Potential harm to businesses** |
| --- | --- | --- |
| Any data that is old which should be replaced with newer and more accurate information | People changing roles or companies, or software and systems becoming obsolete | Inaccurate insights, decision-making, and analytics |

### **Incomplete data**

| **Description** | **Possible causes** | **Potential harm to businesses** |
| --- | --- | --- |
| Any data that is missing important fields | Improper data collection or incorrect data entry | Decreased productivity, inaccurate insights, or inability to complete essential services |

### **Incorrect/inaccurate data**

| **Description** | **Possible causes** | **Potential harm to businesses** |
| --- | --- | --- |
| Any data that is complete but inaccurate | Human error inserted during data input, fake information, or mock data | Inaccurate insights or decision-making based on bad information resulting in revenue loss |

### **Inconsistent data**

| **Description** | **Possible causes** | **Potential harm to businesses** |
| --- | --- | --- |
| Any data that uses different formats to represent the same thing | Data stored incorrectly or errors inserted during data transfer | Contradictory data points leading to confusion or inability to classify or segment customers |

### **Business impact of dirty data**

For further reading on the business impact of dirty data, enter the term “dirty data” into your preferred browser’s search bar to bring up numerous articles on the topic. Here are a few impacts cited for certain industries from a previous search:

- **Banking**: Inaccuracies cost companies between 15% and 25% of revenue ([source](https://sloanreview.mit.edu/article/seizing-opportunity-in-data-quality/)).
- **Digital commerce:** Up to 25% of B2B database contacts contain inaccuracies ([source](https://www.demandgen.com/dirty-data-what-is-it-costing-you/)).
- **Marketing and sales**: 99% of companies are actively tackling data quality in some way ([source](https://www.dqglobal.com/blog/why-bad-data-is-wasting-your-marketing-efforts/)).
- **Healthcare**: Duplicate records can be 10% and even up to 20% of a hospital’s electronic health records ([source](https://searchhealthit.techtarget.com/feature/Hospitals-battle-duplicate-medical-records-with-technology)).

## Key takeaways

Dirty data includes duplicate data, outdated data, incomplete data, incorrect or inaccurate data, and inconsistent data. Each type of dirty data can have a significant impact on analyses, leading to inaccurate insights, poor decision-making, and revenue loss. There are a number of causes of dirty data, including manual data entry errors, batch data imports, data migration, software obsolescence, improper data collection, and human errors during data input. As a data professional, you can take steps to mitigate the impact of dirty data by implementing effective data quality processes.

---

# Recognize and remedy dirty data

## **Introduction**

- This video focuses on common issues associated with dirty data, including spelling errors, inconsistent formats, missing data, and duplicates.
- Recognizing these problems will help you fix them during your own data analysis.

### **Types of Dirty Data**

- **Misspellings and Text Errors:**
    - Inconsistent spelling, punctuation, and typos.
    - Example: "Beverage" vs. "bevarage".
- **Inconsistent Formatting:**
    - Data displayed in the wrong format, like currency shown as a percentage.
    - Example: "$100" shown as "100%".
- **Missing Data (Nulls):**
    - Empty fields requiring research to fill in the missing information.
    - Example: Missing customer information for a specific date.
- **Duplicates:**
    - Identical data entries due to accidental copying or human error.
    - Example: Two entries for the same appointment.

### **Additional Types of Dirty Data**

- **Inconsistent Labeling:**
    - Incorrectly labeled data causing problems for analysis.
    - Example: Mislabeled images affecting machine learning algorithms.
- **Inconsistent Field Length:**
    - Fields not having a consistent number of characters.
    - Example: A field for birth year should always be four characters long.

**Data Validation:**

- A tool for checking data accuracy and quality before adding or importing it.
- Helps prevent dirty data from entering the system.

### **Key Points**

- Dirty data is a common problem in data analysis.
- Recognizing different types of dirty data is crucial for fixing them.
- Data validation can help prevent dirty data from entering the system.

### **Definitions**

- **Data Integrity:** The accuracy and consistency of data.
- **Data Cleaning:** The process of identifying and fixing dirty data.
- **Data Validation:** The process of checking data accuracy and quality before adding or importing it.

---