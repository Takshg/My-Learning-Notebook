# VLOOKUP and Data Aggregation

---

# Aggregate data for analysis

**What is Data Aggregation?**

- **Definition:** Data aggregation is the process of collecting and combining data from multiple sources into a single, summarized collection.
- **Analogy:** Think of it like organizing puzzle pieces scattered across the floor. You gather the pieces belonging to each puzzle and put them back in their boxes.
- **Purpose:** Aggregation helps identify trends, make comparisons, and gain insights that wouldn't be possible by analyzing individual data points.

**Examples of Data Aggregation:**

- **High School Graduation Rates:** Individual student data is aggregated to calculate the graduation rate for an entire class.
- **Real Estate Sales:** Data on individual sales over 10 years is aggregated to find the average price and track value changes over time.

**Tools for Data Aggregation:**

- **Functions:** Learn how to use common functions to create summaries.
- **Subqueries:** Understand how to use subqueries (nested queries) for aggregation.

**Benefits of Data Aggregation:**

- **Identify Trends:** See patterns and relationships in the data that wouldn't be apparent otherwise.
- **Make Comparisons:** Compare different groups or time periods to understand changes and differences.
- **Gain Insights:** Discover valuable information that can inform decision-making.

**Next Steps:**

- Learn how to use functions for data aggregation.
- Understand how to use subqueries for aggregation.

**Key Takeaways:**

- Data aggregation is essential for effective data analysis.
- It allows you to see the bigger picture and gain valuable insights from your data.

---

# Prepare for VLOOKUP

[index (20).mp4](VLOOKUP%20and%20Data%20Aggregation%20767abec0afff47fe817fcb829bda8e74/index_(20).mp4)

**Key Points:**

- **Data aggregation:** The process of gathering data from multiple sources and combining it into a single summarized collection.
- **VLOOKUP:** A function that searches for a certain value in a column and returns a corresponding piece of information.
- **Data cleaning:** The process of preparing data for analysis by ensuring it is accurate, consistent, and free of errors.
- **Common data cleaning tasks:**
    - **Converting different data types:** Ensuring all data is in a consistent format that the spreadsheet application recognizes.
    - **Removing extra spaces:** Eliminating any leading or trailing spaces that may have been added during data entry or copying.
    - **Removing duplicates:** Identifying and eliminating duplicate rows in the data.
- **Tools for data cleaning:**
    - **VALUE function:** Converts a text string that represents a number to a numerical value.
    - **TRIM function:** Automatically deletes any extra spaces added to a cell.
    - **Remove duplicates tool:** Automatically searches for and eliminates duplicate entries from a spreadsheet.

**Definitions:**

- **Data aggregation:** The process of gathering data from multiple sources and combining it into a single summarized collection.
- **VLOOKUP:** A function that searches for a certain value in a column and returns a corresponding piece of information.
- **Data cleaning:** The process of preparing data for analysis by ensuring it is accurate, consistent, and free of errors.
- **VALUE function:** Converts a text string that represents a number to a numerical value.
- **TRIM function:** Automatically deletes any extra spaces added to a cell.
- **Remove duplicates tool:** Automatically searches for and eliminates duplicate entries from a spreadsheet.

---

# VLOOKUP in action

[index (21).mp4](VLOOKUP%20and%20Data%20Aggregation%20767abec0afff47fe817fcb829bda8e74/index_(21).mp4)

**Key Points:**

- **VLOOKUP Syntax:** The video reviews the syntax of VLOOKUP, emphasizing the importance of understanding each element:
    - **Value to search for:** The specific value you want to find in the first column of the lookup range.
    - **Lookup range:** The range of cells containing the data you want to search.
    - **Column index number:** The column number within the lookup range where the return value is located.
    - **Range lookup:** A logical value indicating whether to find an exact match (FALSE) or an approximate match (TRUE).
- **VLOOKUP in Action:** The video showcases two common use cases for VLOOKUP:
    - **Populating data from another spreadsheet:** The video demonstrates how to use VLOOKUP to combine data from two separate spreadsheets based on a shared identifier (e.g., employee ID). This allows for efficient data consolidation and analysis.
    - **Calculating values based on VLOOKUP results:** The video shows how to use VLOOKUP to retrieve data from another spreadsheet and then perform calculations on that data. In the example, VLOOKUP retrieves employee pay rates and then multiplies them by hours worked to calculate individual paychecks.
- **VLOOKUP Reminders and Resources:** The video concludes by reminding viewers that VLOOKUP is a powerful but complex function. It encourages viewers to access additional resources for further learning and practice.

**Definitions:**

- **VLOOKUP:** A spreadsheet function that searches for a specific value in a column and returns the corresponding value from another column in the same row.
- **Lookup range:** The range of cells containing the data you want to search.
- **Column index number:** The column number within the lookup range where the return value is located.
- **Range lookup:** A logical value indicating whether to find an exact match (FALSE) or an approximate match (TRUE).

---

# Identify and fix VLOOKUP errors

[index (22).mp4](VLOOKUP%20and%20Data%20Aggregation%20767abec0afff47fe817fcb829bda8e74/index_(22).mp4)

**Key Points:**

- **VLOOKUP limitations:**
    - Only returns the first match, even if multiple matches exist.
    - Can only look to the right of the lookup value.
- **Common VLOOKUP problems:**
    - Incorrect results due to unfixed table array (not absolute reference).
    - Version control issues (e.g., changes in referenced spreadsheet).
    - Inaccurate results due to approximate matching (using TRUE instead of FALSE).
- **Troubleshooting questions:**
    - How to prioritize issues?
    - What is the specific issue?
    - What resources can help solve the problem?
    - How to prevent future occurrences?
- **Solutions:**
    - Copy and paste the lookup value to the leftmost column.
    - Make the table array absolute using dollar signs ($).
    - Lock the spreadsheet or use the MATCH function for version control.
    - Use FALSE in VLOOKUP for exact matching.

**Definitions:**

- **VLOOKUP:** A function in spreadsheets that looks up a value in a table and returns a corresponding value from the same row.
- **Troubleshooting:** The process of identifying and solving problems.
- **Absolute reference:** A cell reference that remains constant when copied or moved.
- **Version control:** Managing changes made to a document or spreadsheet.
- **Approximate matching:** Finding the closest match to a lookup value.
- **Exact matching:** Finding the exact match to a lookup value.

---

# VLOOKUP Core Concepts

Spreadsheet functions can be used to quickly find information and perform calculations using specific values. **VLOOKUP**, or Vertical Lookup, is one such function that vertically searches for a certain value in a column to return a corresponding piece of information. In this reading, you’ll examine the intricacies of this extremely useful function so you understand how it works when you use it to analyze data.

## **VLOOKUP** functionality

**VLOOKUP** searches for a search term, called a **search_key**, in one column of a spreadsheet. When the **search_key** is found, the function returns the data from another column of the row from which it  was located. **VLOOKUP** returns only the value that corresponds to the first item it matches. So, if there are multiple matching values, the spreadsheet will return only data about the first one.

## **VLOOKUP** use cases

Here are two common reasons why you might use **VLOOKUP**:

- **Populating data in a spreadsheet.** Perhaps a store manager is tracking incoming shipments before a busy holiday. They could use **VLOOKUP** to look up product ID codes in a product spreadsheet and retrieve the corresponding product information from another spreadsheet. This would help the manager know how many stock clerks they need to schedule to work when the shipments arrive.
- **Merging data from one spreadsheet with data in another.** If a teacher keeps one spreadsheet for student grades and another for attendance, they could use **VLOOKUP** to combine the spreadsheets. That way, they could search for a particular student in the attendance sheet, and **VLOOKUP** would pull the corresponding attendance record into the grades spreadsheet.

## **VLOOKUP** syntax

**VLOOKUP** is available in both Microsoft Excel and Google Sheets. Here, you’ll explore its syntax in Google Sheets. Refer to the resources at the end of this reading for more information about **VLOOKUP** in Microsoft Excel.

**VLOOKUP**’s syntax is:

![Untitled](VLOOKUP%20and%20Data%20Aggregation%20767abec0afff47fe817fcb829bda8e74/Untitled.png)

The following sections explain each of the four parts of the syntax.

### **search_key**

This is the value the function will search for. It can be a number, text string, or cell reference.

### **range**

This is the range of cells over which the function will search and return information. The first column in the **range** is searched. When the search key is found, the index from that row is returned.

For example, if you search for the **search_key** in column B and return the data from column D, the range would need to include columns B through D, such as the range B2:D10. If you specified a range of A2:D10, the function would search for the search term in column A.

The **search_key** must be to the left of the information you want the function to return. This may require you to move columns around before you use **VLOOKUP**. For example, if you plan to search for the **search_key** column D, but the information you want the function to return is in column A, you must rearrange your columns before using **VLOOKUP**.

### **index**

This is the position of the column that contains the data to be returned. The first column in the range is column number 1, and each column is numbered sequentially to the right.

For example, if the range is B2:D10 and you want to return a value from column D, the index number would be 3. If the index is not between 1 and the number of columns in range, the error message **#VALUE!** will be returned.

### **is_sorted**

This indicates whether to return an approximate or exact match. For example, if you’re searching for Google, then google would not count as a match.

- To return an exact match, set **is_sorted** to **FALSE**. This is recommended.
- To return an approximate match, set **is_sorted** to **TRUE**. The nearest match (less than or equal to the **search_key**) is returned. To use this option to obtain accurate results, you must sort your data in ascending order. But, you could still find a value.
- If neither **TRUE** nor **FALSE** are selected, the function will default to **TRUE**.

## The **#N/A** error

**#N/A** indicates that a matching value can't be returned because no matches were found.

## Key takeaways

Use **VLOOKUP** to search for a value in a column and return a corresponding piece of information. It’s a very useful tool for data professionals, as it enables them to combine data from multiple sources and find information quickly. Keep in mind that the column that matches the **search_key** in a **VLOOKUP** formula should be on the left side of the data. The range must include both the column being searched and the column that contains the information being returned. **TRUE** means an approximate match, and **FALSE** means an exact match on the **search_key**.

## VLOOKUP resources for Microsoft Excel

**VLOOKUP** may slightly differ in Microsoft Excel, but the overall concepts can still be generally applied. Refer to the following resources if you’re working with Excel:

- [How to use VLOOKUP in Excel](https://support.microsoft.com/en-us/office/vlookup-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1): This tutorial includes a video to help you get a general understanding of how the **VLOOKUP** function works in Excel, as well as practical examples to look through.
- [VLOOKUP in Excel tutorial](https://www.youtube.com/watch?v=d3BYVQ6xIE4): Follow along in this video lesson and learn how to write a **VLOOKUP** formula in Excel and master time-saving useful tips and tricks.
- [23 things you should know about VLOOKUP in Excel](https://exceljet.net/things-you-should-know-about-vlookup): Explore this list of **VLOOKUP** facts, common challenges and their solutions.
- [How to use Excel's VLOOKUP function](https://edu.gcfglobal.org/en/excel-tips/how-to-use-excels-vlookup-function/1/): This article shares a specific example about applying **VLOOKUP** in your searches.
- [VLOOKUP in Excel vs Google Sheets](https://infoinspired.com/sheets-vs-excel-formula/vlookup-formula-in-excel-and-google-sheets/): This guide offers a **VLOOKUP** comparison of Excel and Google Sheets.

---

# Hands-On Activity: Use VLOOKUP to perform a task

## Activity Overview

You’ve been learning about **VLOOKUP**, a spreadsheet function that vertically searches for a certain value in a column to return a corresponding piece of information. In this activity, you’ll practice cleaning data and using **VLOOKUP** to consolidate information between two spreadsheet tabs. You’ll complete your analysis by creating a pivot table.

By the time you complete this activity, you will be able to use **VLOOKUP** to find information in one sheet and add it to the correct row in another spreadsheet. This is an important skill that can help you work with large datasets in your career as a data analyst.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

You’re the payroll manager at an accounting firm. To calculate payroll, you need to know how many hours each of your employees worked and their hourly rate of pay. This is easy to do manually in a small spreadsheet, but it becomes more difficult as the amount of information grows or is spread across multiple spreadsheets. You’d like to use the **VLOOKUP** function as a way to automate the information-gathering. So, follow the steps below to calculate the total weekly pay for your employees.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the template**

To get started, access the **VLOOKUP** Practice Worksheet. Select the link to the worksheet below and select **USE TEMPLATE** to create a copy. If you don’t have a Google account, you can download the **VLOOKUP** Practice Sheet directly from the attachment below.

Link to the worksheet: [VLOOKUP Practice Sheet](https://docs.google.com/spreadsheets/d/1Js6kRVYy6Nx6VENibaX9dmNOAP_7CXWuOqUjUz9cBtA/template/preview)

OR

[VLOOKUP Practice SheetXLSX File](https://d3c33hcgiwev3.cloudfront.net/MdQRf21-QWqt9OosQItIDw_643315a3efe649f88f5c30e2a6bf9be1_VLOOKUP-Practice-Sheet.xlsx?Expires=1716940800&Signature=OWZ0~~PtSjdC4kJlH2VEU6mAlkeYRBApnyzsxpgtm2DhVkEnCqxapK7vJ49LndVHO4YE6kGrv1IiifLEuGhSBAfFZ1xUG7S3yzNvnoV-r1DwtGg8I0EJFF3DMFhlG~GTKqu8aikQt3D5ZPChFyTAnV21a-to17~l7zMNxMkacWY_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

# **Step 2: Prepare the data**

Sheet1 of the **VLOOKUP** Practice Sheet contains a timesheet of hours worked by several employees. However, this data has not been cleaned. You'll create a clean version of the table in Sheet1 so you can manipulate the data without changing the data from the original table. Then, you’ll combine data from two sheets in the **VLOOKUP** Practice Sheet spreadsheet (Sheet1 and Sheet2) using the **VLOOKUP** function.

# **Step 3: Label the columns**

Working with data gets messy quickly, and it’s important to keep track of what your columns mean. First, add labels to the columns in your new table to help keep your data organized.

Add the following labels to the Sheet1:

1. In cell B14, enter: **Names**.

2. In cells C14 to H14, enter: **1/1/2020, 1/2/2020, 1/3/2020, 1/4/2020**, **1/5/2020**, and **1/6/2020**.

3. In cell **I14**, enter: **Hours**.

4. In cell **J14**, enter: **Pay Rate**.

5. In cell **K14**, enter: **Total Pay**.

# **Step 4: Clean the data**

Some of the employee names in column B have extra spaces. Use the following steps to remove the extra spaces and clean your data.

1. In cell **B15**, enter **=TRIM(B2)**.

2. Select and drag the fill handle to cell **B19**, then release it. This populates the names, with extra spaces removed, in these cells.

# **Step 5: Populate the daily employee hours**

Next, move employee hours to your new table with cleaned employee names. Perform the following steps to populate the daily hours for the employees:

1. In cell **C15**, type **=value(C2)**.

2. Select and drag the fill handle to cell **C19**. This populates the hours for the other employees.

Your new table should contain the following data in rows **15-19** of column **C**:

| **Row** | **C** |
| --- | --- |
| **15** | 8 |
| **16** | 8.5 |
| **17** | 7.5 |
| **18** | 8 |
| **19** | 6 |

Your table should have the values 8, 8.5, 7.5, 8, and 6 in the cells C15 through C19 respectively.

Use the populated cells from **C15** through **C19** to populate the remaining hours needed for each employee. To do this, perform the following steps:

3. Select and drag the fill handle for cell **C15** to cell **H15**. This populates the remaining hours for Daniel Chan. You should see the values 8, 8, 8.5, 7, 5, and 2.5 in cells C15 through H15.

4. Select and drag the fill handle for cell **C16** to cell **H16**. This populates the remaining hours for Dana Ali. You should see the values 8.5, 7, 8, 8, 9, and 5.5 in cells C16 through H16.

5. Repeat this process in **rows 17**, **18**, and **19** for the remaining employees.

a. In row 17, you should see the values 7.5, 6.5, 10, 8, 7, and 5 in cells C17 through H17.

b. In row 18, you should see the values 8, 8, 8, 7, 7, and 4 in cells C18 through H18.

c. In row 19, you should see the values 6, 5, 5, 5.5, 6, and 2 in cells C19 through H19.

Verify that your spreadsheet contains the following data:

| **Row** | **C** | **D** | **E** | **F** | **G** | **H** |
| --- | --- | --- | --- | --- | --- | --- |
| **15** | 8 | 8 | 8.5 | 7 | 5 | 2.5 |
| **16** | 8.5 | 7 | 8 | 8 | 9 | 5.5 |
| **17** | 7.5 | 6.5 | 10 | 8 | 7 | 5 |
| **18** | 8 | 8 | 8 | 7 | 7 | 4 |
| **19** | 6 | 5 | 5 | 5.5 | 6 | 2 |

# **Step 6: Sum the total hours for each employee**

Fill in the **Hours** column for the employees.

1. In cell **I15**, enter **=sum(C15:H15)**.

2. Select and drag the fill handle for cell **I15** to cell **H15**. This populates the sums for the remaining employees.

Column **I** in rows **15–19** should contain the following data:

| **Row** | **Column I** |
| --- | --- |
| **15** | 39 |
| **16** | 46 |
| **17** | 44 |
| **18** | 42 |
| **19** | 29.5 |

Your table should have the values 39, 46, 44, 42, and 29.5 in the cells I15 through I19 respectively.

# **Step 7: Import pay rate data**

You keep track of your employee’s hourly pay rate in Sheet2 of the **VLOOKUP** Practice Sheet. This sheet also includes employee ID, date of hire (DOH), and employee status.

Use **VLOOKUP** to import pay rate data from Sheet2 into Sheet1.

1. In cell **J15** on **Sheet1**, enter: **=VLOOKUP(A2, Sheet2!$A$2:$D$6, 4, false)**.

Consider the syntax for this **VLOOKUP** function:

"A2" refers to cell A2 in Sheet1.

**Note:** In Sheet2, the rate of pay and related fields are referenced by **ID** instead of employee name. You need to use employee ID to import the pay rate from Sheet2.

- "**Sheet2!**" refers to the sheet from which you want to access the data.
- "**$A$2:$D$6**" to the range of cells that make up the table array. The "**$**" placed in front of the column tabs and cell numbers locks the formula so that it can be copied by dragging cell J15 down to cell J19 to import the pay rate for the other employees.
- The "**4**" refers to the column from which the returned value will come. The "**4**" means that the returned value will come from the 4th column in the selected range.
- "**false**" signifies that you want an exact, character-for-character match to the lookup value. Using "**true**" will return an approximate match (or the closest match available) for the lookup value.

2. Select and drag the fill handle for cell **J15** to cell **J19**. This populates the pay rate for the remaining employees.

Rows **15–19** in column **J** should contain the following data:

| **Row** | **Column J** |
| --- | --- |
| **15** | 100.5 |
| **16** | 75 |
| **17** | 150 |
| **18** | 65 |
| **19** | 3000 |

Your table should have the values 100.5, 75, 150, 65, and 3,000 in the cells J15 through J19 respectively.

3. In cell **K15**, enter: **=PRODUCT(I15, J15)to calculate the total pay.**

4. Select and drag the fill handle of cell **K15** to cell **K19** to populate the total pay for the remaining employees.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Mg14dKXBSdG7pvxDH85Rrg_403ccf33e6bf4df1a7a2a5a8d18f8ae1_C5M3L1_A1_Image-7.png?expiry=1716940800000&hmac=7wPX-Z4E3wPhuaqBlIJu1l-HLNT_ckrMkHd6_JfAeJc)

Rows **15–19** in column **K** should contain the following data for Total Pay:

| **Row** | **Column K** |
| --- | --- |
| **15** | 3919.5 |
| **16** | 3450 |
| **17** | 6600 |
| **18** | 2730 |
| **19** | 88500 |

Your table should have the values 3919.5, 3450, 6600, 2730, and 88500 in the cells K15 through K19 respectively.

# **Step 8: Create a pivot table**

Now that the data is clean and includes the pay rate information, you can create a pivot table. This makes it easier to quickly identify trends and patterns and generate reports without having to search the raw data. This section demonstrates how to create a pivot table in **Google Sheets**. If you are using Excel, follow the [documentation for how to manually create a pivot table in Excel](https://support.microsoft.com/en-us/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

To create a table for data in cells **B14:K19**:

1. Select the data in cells **B14:K19**.

2. Select **Insert** from the menu, then select **Pivot Table**.

3. From the pop-up window, select **New Sheet**, then select **Create**.

A new tab titled Pivot Table 1 will appear between Sheet1 and Sheet2. A **Pivot table editor** will pop up on the screen. Use this editor to create a pivot table that contains each employee’s name, pay rate, and total pay:

1. Select **Add** for **Rows**. Then, select **Names** from the dropdown options.

2. Select **Add** for **Values**. Then, select **Pay Rate** from the dropdown options.

3. Select **Add** for **Values** again. Then, select **Total Pay** from the dropdown options.

4. Select cells **B2** through **C6**, then select the **$** symbol from the toolbar to reformat these cells as currency.

Rows **1-7** in columns **A**, **B**, and **C** in the sheet Pivot Table 1 should contain the following data:

| **Row** | **Names** | **SUM of Pay Rate** | **SUM of Total Pay** |
| --- | --- | --- | --- |
| **2** | Ali, Dana | $75.00 | $3,450.00 |
| **3** | Chan, Daniel | $100.50 | $3,919.00 |
| **4** | Fischer, Wolfgang | $65.00 | $2,730.00 |
| **5** | Patel, Anika | $3,000.00 | $88,500.00 |
| **6** | Sanchez, Alexis | $150.00 | $6,600.00 |
| **7** | **Grand Total** | **$3,390.50** | **$105,199.50** |

Your table should have the following values:

In row 2, you see the name Ali, Dana with a pay rate of $75.00 and a total pay of $3,450.00. In row 3, you see the name Chan, Daniel with a pay rate of $100.50 and a total pay of $3,919.00. In row 4, you see the name Fischer, Wolfgang with a pay rate of $65.00 and a total pay of $2,730.00. In row 5, you see the name Patel, Anika with a pay rate of $3,000.00 and a total pay of $88,500.00. In row 6, you see the name Sanchez, Alexis with a pay rate of $150.00 and a total pay of $6,600.00. In row 7 are the grand totals, which include the total combined pay rate of $3,390.50 and the total combined pay of $105,199.50.

Congratulations! You have now cleaned and labeled your data, used **VLOOKUP** to import data from another spreadsheet, and created a pivot table. Now you’ll be able to easily complete payroll for your employees.

---