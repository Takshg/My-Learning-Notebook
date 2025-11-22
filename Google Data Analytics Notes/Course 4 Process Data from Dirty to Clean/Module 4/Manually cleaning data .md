# Manually cleaning data

---

# Verify and report results

### **Key Points**

- **Verification:**
    - Confirms that data cleaning was thorough and accurate.
    - Involves rechecking the clean dataset, manual cleanups if needed, and reflecting on the project's original purpose.
    - Ensures data credibility and appropriateness for your goals.
- **Importance of Verification:**
    - Prevents errors and misinterpretations.
    - Protects against misrepresenting populations or damaging product outcomes.
    - Example: Removing a semicolon that could have significantly altered results and business decisions.
- **Reporting:**
    - Demonstrates transparency and accountability to your team.
    - Builds trust and ensures everyone is on the same page.
    - Strategies:
        - Data cleaning reports
        - Documenting the cleaning process
        - Using changelogs (chronological lists of project modifications)
- **Benefits of Reporting:**
    - Avoids repeating mistakes.
    - Saves time for you and your team.

### **Definitions**

- **Verification:** The process of confirming the accuracy and completeness of data cleaning efforts.
- **Data cleaning report:** A document that details the steps taken to clean the data, the challenges encountered, and the solutions implemented.
- **Changelog:** A file that tracks changes made to a project over time, including the date, author, and description of each change.

---

# Confirm data-cleaning meets business expectations

This video focuses on the crucial step of verifying your data cleaning efforts. This ensures the insights you gain from analysis are reliable and trustworthy.

**Key Points:**

- **Verification is essential:** Without it, you can't be confident in your data-driven decisions. It's like a stamp of approval for your cleaned data.
- **Verification involves:**
    - **Comparing cleaned data to the original:** Look for discrepancies and ensure issues like null values or misspellings are addressed.
    - **Taking a big-picture view:** Confirm you're solving the intended business problem and your data is capable of doing so.
    - **Considering the project goal:** Ensure your data analysis aligns with the desired outcome.
    - **Checking data sources and processes:** Test your data collection and cleaning methods to identify potential errors.
    - **Seeking feedback:** Get a fresh perspective on your data from colleagues or others.
    - **Identifying suspicious patterns:** Look for inconsistencies or anomalies that might indicate problems.
    - **Asking yourself: "Do the numbers make sense?"** This helps catch potential errors.

**Example:**

An e-commerce company surveys 1,000 customers for product feedback. After cleaning the data, the analyst finds more than 1,000 responses. This signals a potential issue, either duplicate entries or a data cleaning error. This needs to be investigated and corrected.

**Benefits of Verification:**

- Ensures data accuracy and reliability.
- Prevents costly mistakes based on inaccurate data.
- Builds trust in data-driven decisions.

**Next Steps:**

The video mentions further steps in the data cleaning process, which will be covered in subsequent lectures.

**Definitions:**

- **Verification:** The process of confirming that data cleaning was done correctly and the resulting data is accurate and reliable.
- **Data-driven decision-making:** Making decisions based on insights derived from data analysis.
- **Big-picture view:** Considering the overall context and goals of your project when analyzing data.
- **Data integrity:** Ensuring data is accurate, consistent, and reliable.

**Remember:**

Verification is a crucial step in data cleaning. By taking the time to verify your data, you can be confident in the insights you gain and make better decisions.

---

# Step-by-Step: Verification of data cleaning

This reading outlines the steps the instructor performs in the following video, [Verification of data cleaning](https://www.coursera.org/learn/process-data/lecture/Hx69i/the-final-step-in-data-cleaning). The video demonstrates how to verify cleaned data in both spreadsheets and SQL.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

### **What you’ll need**

If you’d like to follow along with the examples in this video, choose a spreadsheet tool. Google Sheets or Excel are recommended.

To access the spreadsheet the instructor uses in this video, click the link to the template to create a copy of the dataset.  If you don’t have a Google account, download the data directly from the attachments below.

Link to dataset: [Jeff’s Party Planet - Data for Cleaning](https://docs.google.com/spreadsheets/d/1RaDdSEp2V6D09FE6LOFkiJGv9CMT83GIV_U9YnY2rvI/template/preview?resourcekey=0-IU2-k90CX0mrt0ebwrvwDw)

OR [Jeff's Party Planet - Data for CleaningXLSX File](https://d3c33hcgiwev3.cloudfront.net/ve64rJeHTTylDeO1R6V-YQ_3611b683e1844cb5a165b96ea68f71e1_Jeff-s-Party-Planet---Data-for-Cleaning.xlsx?Expires=1716854400&Signature=Vg3IrkFFXh6pa9qG9twa0toPcpXWytz7iWcZjtFxRDsSNsBAuDl5rhyykfTnwBvExcqJsGdQod01X2uhLapse1SC4p45GDSpRQHTxBbNDiGkxOAcDMrcLOMiRRhWiDgoWb4wflUhwLWSaqkB4cRqXlMEiJYvz1kwlCPkzKBLiLE_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

**Note:** The SQL table used in this example is not available for this activity.

## Example 1: Verify data with spreadsheets

Use spreadsheet tools such as Find and Replace and pivot tables to find, understand, and fix errors in your spreadsheet.

### **Use Find and Replace to replace all instances of a mistake**

1. Use the [Jeff’s Party Planet - Data for Cleaning](https://docs.google.com/spreadsheets/d/1RaDdSEp2V6D09FE6LOFkiJGv9CMT83GIV_U9YnY2rvI/template/preview?resourcekey=0-IU2-k90CX0mrt0ebwrvwDw#gid=0) dataset.
2. From the **Edit** menu, choose **Find and Replace** to open the **Find and replace** dialog box.
3. In the **Find** field, enter the misspelled word in the supplier name, **Plos**.
4. In the **Replace with** field, enter **Plus**.
5. Click **Replace all** to replace all instances of "Plos" with "Plus". Click **Done** to close the **Find and replace** dialog box.
6. Select the **Undo** button to use a different method to correct this misspelling. This can also be done with **Ctrl** (Windows) or **Command** (Mac) **Z**.

### **Use a pivot table to understand errors in a spreadsheet**

1. Select the **Suppliers** column.
2. Select **Insert > Pivot Table**. In the **Create pivot table** dialog box, choose **New Sheet** then **Create**.
3. This creates a new tab that is mostly blank.
4. Additionally, the **Pivot table editor** pane is in the window.
5. Next to **Rows**. Select **Add**, then the **Suppliers** column.
6. Next to **Values**, select **Add** then select **Suppliers**. This adds a value for the **Suppliers** column.
7. By default, Google Sheets sets the value to summarize by **COUNTA** (the total number of values in a range). This will show how many times each supplier name comes up. It’s a great way to check for misspellings and other anomalies. **Note:** Don’t use **COUNT**, because **COUNT** counts only numerical values.
8. When there is only one instance of the misspelled name, manually change it to the correct spelling.
9. To return to the original sheet, select the **Sheet1** tab.

## Example 2: Use a CASE statement to verify data in SQL

Use **CASE** statements to correct misspellings in SQL.

1. The SQL table used in this example is not available for download, but if you were performing a similar query you’d first make sure to load the data in BigQuery.

2. Start your SQL query with the basic structure:

**SELECT**

**FROM**

**WHERE**

3. In the **FROM** clause,  specify the table you're pulling data from after **FROM**. For example, **project-id.customer_data.customer_name**

4. In the **SELEC**T clause, specify the columns you want to return. In this example, you want  **customer_id** and **first_name**.

5. However, there is a misspelling in a customer’s first name.

i. To correct the misspelled name "Tnoy" to "Tony", use a **CASE** statement.

ii. Enter **CASE**. On the next line, enter **WHEN first_name = 'Tnoy'THEN 'Tony'**. This tells SQL to replace any instances of **Tnoy** in the **first_name** column with **Tony**.

iii. On the next line, add the **statement ELSE first_name** to keep other names as they are.

iv. End the statement with **END AS cleaned_name**.This creates a new column called **cleaned_name** that will contain the data cleaned with the **CASE** statement.

6. Delete the **WHERE** clause because you don’t want to filter the query.

7. The final statement should be:

![Untitled](Manually%20cleaning%20data%2075250d75adc245e7bb35ecf3d5e414b4/Untitled.png)

8. This SQL query will correct the misspelled name and leave other names unchanged in a new column called **cleaned_name**. Note that this query corrects only the display of the name; it does not update the table’s data.

---

# Verification of data cleaning

[index (5).mp4](Manually%20cleaning%20data%2075250d75adc245e7bb35ecf3d5e414b4/index_(5).mp4)

**Key Points:**

- **Verification:** The process of ensuring data cleaning was done correctly and the results are reliable.
- **Importance of Verification:** Like car companies testing vehicles before release, data needs verification to be 100% ready for use.
- **Verification Steps:**
    1. Compare cleaned data to the original, unclean dataset.
    2. Manually fix common problems (e.g., extra spaces, unwanted quotation marks).
    3. Use tools for automatic fixes (e.g., TRIM, remove duplicates).
    4. Create a pivot table to identify and address recurring errors.
- **Pivot Table:** A data summarization tool used to sort, reorganize, group, count, total, or average data.
- **Find and Replace:** A tool to search for specific terms and replace them with something else.
- **COUNTA Function:** Counts the total number of values within a specified range.
- **COUNT Function:** Counts only the numerical values within a specified range.
- **CASE Statement:** Used in SQL to evaluate multiple conditions and return a value when a condition is met.
- **Example:** Correcting a customer's misspelled name in a database using a CASE statement.

**Definitions:**

- **Data Cleaning:** The process of identifying and correcting errors in data.
- **Data Verification:** The process of ensuring data cleaning was done correctly and the results are reliable.
- **Pivot Table:** A data summarization tool used to sort, reorganize, group, count, total, or average data.
- **Find and Replace:** A tool to search for specific terms and replace them with something else.
- **COUNTA Function:** Counts the total number of values within a specified range.
- **COUNT Function:** Counts only the numerical values within a specified range.
- **CASE Statement:** Used in SQL to evaluate multiple conditions and return a value when a condition is met.

---