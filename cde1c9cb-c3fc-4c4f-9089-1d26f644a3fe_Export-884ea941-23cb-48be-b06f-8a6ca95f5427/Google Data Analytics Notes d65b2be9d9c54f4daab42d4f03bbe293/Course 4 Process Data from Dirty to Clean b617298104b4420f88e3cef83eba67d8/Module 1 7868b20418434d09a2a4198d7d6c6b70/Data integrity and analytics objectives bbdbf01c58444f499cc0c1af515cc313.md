# Data integrity and analytics objectives

---

# Why data integrity is important

### **Key Points**

- **Data integrity** is crucial for accurate data analysis.
- Compromised data integrity can lead to inaccurate analysis and potentially harmful consequences.
- Data integrity can be compromised through various factors like replication, transfer, manipulation, human error, viruses, malware, hacking, and system failures.
- Checking data integrity is a vital step before analysis to ensure accurate conclusions.
- In many companies, data warehouses or data engineering teams handle data integrity.

### **Definitions**

- **Data integrity:** Accuracy, completeness, consistency, and trustworthiness of data throughout its lifecycle.
- **Data replication:** Storing data in multiple locations.
- **Data transfer:** Copying data from one storage device to another or from one computer to another.
- **Data manipulation:** Changing data to make it more organized and easier to read.

### **Additional Points**

- The video emphasizes the importance of data integrity for reliable data analysis.
- It highlights the potential risks associated with compromised data integrity.
- It provides an overview of factors that can compromise data integrity.
- It emphasizes the importance of checking data integrity before analysis.
- It mentions that data warehouses or data engineering teams often handle data integrity in companies.

---

# More about data integrity and compliance

This reading illustrates the importance of data integrity using an example of a global company’s data. Definitions of terms that are relevant to data integrity will be provided at the end.

## Scenario: calendar dates for a global company

Calendar dates are represented in a lot of different short forms. Depending on where you live, a different format might be used.

- In some countries, **12/10/20** (DD/MM/YY) stands for October 12, 2020.
- In other countries, the national standard is YYYY-MM-DD so October 12, 2020 becomes **2020-10-12**.
- In the United States, (MM/DD/YY) is the accepted format so October 12, 2020 is going to be **10/12/20**.

Now, think about what would happen if you were working as a data analyst for a global company and didn’t check date formats. Well, your data integrity would probably be questionable. Any analysis of the data would be inaccurate. Imagine ordering extra inventory for December when it was actually needed in October!

A good analysis depends on the integrity of the data, and data integrity usually depends on using a common format. So it is important to double-check how dates are formatted to make sure what you think is December 10, 2020 isn’t really October 12, 2020, and vice versa.

Here are some other things to watch out for:

- **Data replication compromising data integrity:** Continuing with the example, imagine you ask your international counterparts to verify dates and stick to one format. One analyst copies a large dataset to check the dates. But because of memory issues, only part of the dataset is actually copied. The analyst would be verifying and standardizing incomplete data. That partial dataset would be certified as compliant but the full dataset would still contain dates that weren't verified. Two versions of a dataset can introduce inconsistent results. A final audit of results would be essential to reveal what happened and correct all dates.
- **Data transfer compromising data integrity:** Another analyst checks the dates in a spreadsheet and chooses to import the validated and standardized data back to the database. But suppose the date field from the spreadsheet was incorrectly classified as a text field during the data import (transfer) process. Now some of the dates in the database are stored as text strings. At this point, the data needs to be cleaned to restore its integrity.
- **Data manipulation compromising data integrity:** When checking dates, another analyst notices what appears to be a duplicate record in the database and removes it. But it turns out that the analyst removed a unique record for a company’s subsidiary and not a duplicate record for the company. Your dataset is now missing data and the data must be restored for completeness.

## Conclusion

Fortunately, with a standard date format and compliance by all people and systems that work with the data, data integrity can be maintained. But no matter where your data comes from, always be sure to check that it is valid, complete, and clean before you begin any analysis.

## Reference: Data constraints and examples

As you progress in your data journey, you'll come across many types of data constraints (or criteria that determine validity). The  table below offers definitions and examples of data constraint terms you might come across.

| **Data constraint** | **Definition** | **Examples** |
| --- | --- | --- |
| **Data type** | Values must be of a certain type: date, number, percentage, Boolean, etc. | If the data type is a date, a single number like 30 would fail the constraint and be invalid |
| **Data range** | Values must fall between predefined maximum and minimum values | If the data range is 10-20, a value of 30 would fail the constraint and be invalid |
| **Mandatory** | Values can’t be left blank or empty | If age is mandatory, that value must be filled in |
| **Unique** | Values can’t have a duplicate | Two people can’t have the same mobile phone number within the same service area |
| **Regular expression (regex) patterns** | Values must match a prescribed pattern | A phone number must match ###-###-#### (no other characters allowed) |
| **Cross-field validation** | Certain conditions for multiple fields must be satisfied | Values are percentages and values from multiple fields must add up to 100% |
| **Primary-key** | (Databases only) value must be unique per column | A database table can’t have two rows with the same primary key value. A primary key is an identifier in a database that references a column in which each value is unique. More information about primary and foreign keys is provided later in the program. |
| **Set-membership** | (Databases only) values for a column must come from a set of discrete values | Value for a column must be set to Yes, No, or Not Applicable |
| **Foreign-key** | (Databases only) values for a column must be unique values coming from a column in another table | In a U.S. taxpayer database, the State column must be a valid state or territory with the set of acceptable values defined in a separate States table |
| **Accuracy** | The degree to which the data conforms to the actual entity being measured or described | If values for zip codes are validated by street location, the accuracy of the data goes up. |
| **Completeness** | The degree to which the data contains all desired components or measures | If data for personal profiles required hair and eye color, and both are collected, the data is complete. |
| **Consistency** | The degree to which the data is repeatable from different points of entry or collection | If a customer has the same address in the sales and repair databases, the data is consistent. |

---

# Balance objectives with data integrity

### **Key Points**

- **Data integrity** is crucial for accurate insights and reliable analysis.
- **Business objectives** should guide data selection and analysis.
- **Data limitations** can affect analysis and require adjustments.
- **Incomplete data** can lead to misleading conclusions.
- **Data cleaning** is essential before analysis.
- **Duplicate data** can skew results and require correction.
- **Insufficient data** may necessitate alternative approaches or data sources.

### **Definitions**

- **Data integrity:** Ensuring data is accurate, consistent, and reliable.
- **Business objectives:** Specific goals or outcomes a business aims to achieve.
- **Data limitations:** Restrictions or constraints inherent in data that can affect analysis.
- **Incomplete data:** Missing or unavailable data points that hinder comprehensive analysis.
- **Data cleaning:** Process of identifying and correcting errors or inconsistencies in data.
- **Duplicate data:** Multiple entries for the same entity or information in a dataset.
- **Insufficient data:** Lack of sufficient data points to draw meaningful conclusions.

### **Additional Points**

- The video uses an analogy of a picture to illustrate the importance of complete data.
- The speaker shares a personal experience of dealing with insufficient data and finding solutions.
- The video emphasizes the importance of data integrity for success in data analysis careers.

---

# Well-aligned objectives and data

You can gain powerful insights and make accurate conclusions when data is well-aligned to business objectives. As a data analyst, alignment is something you will need to judge. Good alignment means that the data is relevant and can help you solve a business problem or determine a course of action to achieve a given business objective.

In this reading, you will review the business objectives associated with three scenarios. You will explore how clean data and well-aligned business objectives can help you come up with accurate conclusions. On top of that, you will learn how new variables discovered during data analysis can cause you to set up data constraints so you can keep the data aligned to a business objective.

## Clean data + alignment to business objective = accurate conclusions

### **Business objective**

Account managers at Impress Me, an online content subscription service, want to know how soon users view content after their subscriptions are activated.

To start off, the data analyst verifies that the data exported to spreadsheets is clean and confirms that the data needed (when users access content) is available. Knowing this, the analyst decides there is good alignment of the data to the business objective. All that is missing is figuring out exactly how long it takes each user to view content after their subscription has been activated.

Here are the data processing steps the analyst takes for a user from an account called V&L Consulting. (These steps would be repeated for each subscribing account, and for each user associated with that account.)

### **Step 1**

| **Data-processing step** | **Source of data** |
| --- | --- |
| Look up the activation date for V&L Consulting | Account spreadsheet |

**Relevant data in spreadsheet:**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GnNRQZl4QkSzUUGZeBJEzg_90d6857f15ac4d24ae9df6e5c5b4e0fa_Screen-Shot-2021-01-18-at-6.29.11-PM.png?expiry=1716854400000&hmac=YTFOva3Nz6n7ZVPTvnFGJ_x4ZiTmt-moEiZT4947WwA)

**Result**: October 21, 2019

### **Step 2**

| **Data-processing step** | **Source of data** |
| --- | --- |
| Look up the name of a user belonging to the V&L Consulting account | Account spreadsheet (users tab) |

**Relevant data in spreadsheet**:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/R-nkA9w1Riep5APcNSYnRA_7480900c4f204ffb9421199fd8bf32c8_Screen-Shot-2021-01-18-at-6.27.24-PM.png?expiry=1716854400000&hmac=PfqtJuVCXbluusBGkVVhVaUkJbBH41JnNEHGsvWibjc)

**Result**: Maria Ballantyne

### **Step 3**

| **Data-processing step** | **Source of data** |
| --- | --- |
| Find the first content access date for Maria B. | Content usage spreadsheet |

**Relevant data in spreadsheet:**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_Mn53wNpR0aJ-d8DaedG4w_ecc7521519ea4b4c810dd80bc0f54b9d_Screen-Shot-2021-01-18-at-6.35.48-PM.png?expiry=1716854400000&hmac=YdO0U-QncuC9NwiF-xcbZ1KK_7-zx74Hb0P6PbqxwFc)

**Result**: October 31, 2019

### **Step 4**

| **Data-processing step** | **Source of data** |
| --- | --- |
| Calculate the time between activation and first content usage for Maria B. | New spreadsheet calculation |

**Relevant data in spreadsheet**:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jV8hcatCTq2fIXGrQr6ttw_b4f3452496b543bd9e46716485d5175e_Screen-Shot-2021-01-18-at-6.41.56-PM.png?expiry=1716854400000&hmac=zAFYtU3TgsKf4vrTej9FmqwaMLm3hLNtUQjWutL3gB4)

**Result**: 10 days

### **Pro tip 1**

In the above process, the analyst could use **VLOOKUP** to look up the data in Steps 1, 2, and 3 to populate the values in the spreadsheet in Step 4. [VLOOKUP](https://support.microsoft.com/en-us/office/vlookup-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1) is a spreadsheet function that searches for a certain value in a column to return a related piece of information. Using **VLOOKUP** can save a lot of time; without it, you have to look up dates and names manually.

Refer to the [VLOOKUP](https://support.google.com/docs/answer/3093318?hl=en) page in the Google Help Center for how to use the function in Google Sheets.

### **Pro tip 2**

In Step 4 of the above process, the analyst could use ****the **DATEDIF** function to automatically calculate the difference between the dates in column C and column D. The function can calculate the number of days between two dates.

Refer to the Microsoft Support [DATEDIF](https://support.microsoft.com/en-us/office/datedif-function-25dba1a4-2812-480b-84dd-8b32a451b35c) page for how to use the function in Excel. The [DAYS360](https://support.microsoft.com/en-us/office/days360-function-b9a509fd-49ef-407e-94df-0cbda5718c2a) function does the same thing in  accounting spreadsheets that use a 360-day year (twelve 30-day months).

Refer to the [DATEDIF](https://support.google.com/docs/answer/6055612?hl=en) page in the Google Help Center for how to use the function in Google Sheets.

## Alignment to business objective + additional data cleaning = accurate conclusions

### **Business objective**

Cloud Gate, a software company, recently hosted a series of public webinars as free product introductions. The data analyst and webinar program manager want to identify companies that had five or more people attend these sessions. They want to give this list of companies to sales managers who can follow up for potential sales.

The webinar attendance data includes the fields and data shown below.

| **Name** | **<*First name*> <*Last name*>** | **This was required information attendees had to submit** |
| --- | --- | --- |
| **Email Address** | xxxxx@*company*.com | This was required information attendees had to submit |
| **Company** | <*Company name*> | This was optional information attendees could provide |

### **Data cleaning**

The webinar attendance data seems to align with the business objective. But the data analyst and program manager decide that some data cleaning is needed before the analysis. They think data cleaning is required because:

- The company name wasn’t a mandatory field. If the company name is blank, it might be found from the email address. For example, if the email address is username@google.com, the company field could be filled in with Google for the data analysis. This data cleaning step assumes that people with company-assigned email addresses attended a webinar for business purposes.
- Attendees could enter any name. Since attendance across a series of webinars is being looked at, they need to validate names against unique email addresses. For example, if Joe Cox attended two webinars but signed in as Joe Cox for one and Joseph Cox for the other, he would be counted as two different people. To prevent this, they need to check his unique email address to determine that he was the same person. After the validation, Joseph Cox could be changed to Joe Cox to match the other instance.

## Alignment to business objective + newly discovered variables + constraints = accurate conclusions

### **Business objective**

An after-school tutoring company, A+ Education,  wants to know if there is a minimum number of tutoring hours needed before students have at least a 10% improvement in their assessment scores.

The data analyst thinks there is good alignment between the data available and the business objective because:

- Students log in and out of a system for each tutoring session, and the number of hours is tracked
- Assessment scores are regularly recorded

### **Data constraints for new variables**

After looking at the data, the data analyst discovers that there are other variables to consider. Some students had consistent weekly sessions while other students had scheduled sessions more randomly even though their total number of tutoring hours was the same. The data doesn’t align as well with the original business objective as first thought, so the analyst adds a data constraint to focus only on the students with consistent weekly sessions. This modification helps to get a more accurate picture about the enrollment time needed to achieve a 10% improvement in assessment scores.

## Key takeaways

Hopefully these examples give you a sense of what to look for to know if your data aligns with your business objective.

- When there is clean data and good alignment, you can get accurate insights and make conclusions the data supports.
- If there is good alignment but the data needs to be cleaned, clean the data before you perform your analysis.
- If the data only partially aligns with an objective, think about how you could modify the objective, or use data constraints to make sure that the subset of data better aligns with the business objective.

---