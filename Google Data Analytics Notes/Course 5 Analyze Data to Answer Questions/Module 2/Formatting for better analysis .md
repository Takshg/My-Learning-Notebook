# Formatting for better analysis

---

# Step-by-Step: From one type to another

[index (13).mp4](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/index_(13).mp4)

This reading provides you with the steps the instructor performs in the following video, [From one type to another](https://www.coursera.org/learn/analyze-data/lecture/FOAwr/from-one-type-to-another). Watch as the instructor demonstrates how to format numbers and convert units of measurement in your spreadsheets.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

If you’d like to access the spreadsheets the instructor uses in this video, click the links to the dataset to create a copy. If you don’t have a Google account, you may download the data directly from the attachments below.

Link to movie data starter project: [Movie data starter project](https://docs.google.com/spreadsheets/d/1FLaUmMn62YlHYihV6pK1DJqWcFYCnuoqoxFWmm_o5b0/template/preview).

Link to weather table - data for convert: [Weather Table - Data for CONVERT](https://docs.google.com/spreadsheets/d/15VeWQLQ5lUKvywYJL-0cGqmehvE8OH8W9cOlJ2P0J_I/template/preview).

OR

[Movie Data Starter ProjectXLSX File](https://d3c33hcgiwev3.cloudfront.net/7rkSg1b6TCeiM37bJ_iPQA_cc9c5dd03dbe4e09bc83a3c244e4d6e1_Movie-Data-Starter-Project.xlsx?Expires=1716940800&Signature=WIZVxQ1b79u7yzR0P7bYZLQ8aBQwp5qG0Q7m4p6cmDXTLfHlCvgrFIE9gT8jj-YNHes3KxHMmzFcSO5Hlt3Q2BNtyKzipKosRSCWLOrsaq6Pcib8AWae-MkV8ehKcqpLcRjAjXWBlyZhNqkiyn7lTElnyrO7IKq1emVH2RO2Jpw_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Weather Table - Data for CONVERTXLSX File](https://d3c33hcgiwev3.cloudfront.net/dtqtPkiTSV27NcIQALH5gw_e797db6bf7374b11b5e41841e34d71e1_Weather-Table---Data-for-CONVERT.xlsx?Expires=1716940800&Signature=TQCIduwZy65LrsBy~ACwlEKxxBVuPmUnKN3X0MFJxnxLYupljARR2XAjZ-g-yGdoY0qOgTAPMebaM8aU087CwbCJFUqgMRVGt97mlOUu8WXt28nTEPtrkN9De6kmukuNzLU7VNkw47owuHoFZE4HT8ZXM95h0TA3n7P4dOhTY1U_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716940800000&hmac=UN0tlF7lkA95qCr5MP0pe0_funmKbzc9reSo7V0cU3E)

## Example 1: Check and change data type

Check your data for inconsistent units of measurement to prevent problems during data analysis.

1. Open the [**Movie Data Starter Project**](https://docs.google.com/spreadsheets/d/1FLaUmMn62YlHYihV6pK1DJqWcFYCnuoqoxFWmm_o5b0/template/preview) spreadsheet using the link in the video.
2. Select **Column M** [Budget ($)] and **Column N** [Box Office Revenue ($)].
3. From the menu, select **$**, the currency shortcut key.
4. Notice that the currency in **Columns M** and **N** are now formatted correctly.

## Example 2: Convert temperatures from Fahrenheit to Celsius

Use the **CONVERT** function to change units of measurement.

1. Open the [**Weather Table - Data for CONVERT**](https://docs.google.com/spreadsheets/d/15VeWQLQ5lUKvywYJL-0cGqmehvE8OH8W9cOlJ2P0J_I/template/preview) spreadsheet using the link in the video.
2. Select cell **F2** and begin typing the Convert function formula as **=CONVERT**.
3. Indicate the cell you want to convert. After **=CONVERT**, enter **(B2,**.
4. Indicate the conversion you’d like to make: from Fahrenheit to Celsius. Enter **"F", "C")**.
5. The formula in its entirety should look like this: **=CONVERT (B2, "F", “C”)**.
6. Cell **F2** now contains the temperature from cell **B2** in Celsius.
7. Calculate temperature in Celsius for the rest of the column. Hover over cell **F2** and select the fill handle, a small circle on a corner of the cell. Drag the fill handle to cell **F193** to convert the other cells in the column to Celsius.

**Note**: Would you like more practice? Try converting the wind speed in Column **D** from miles per hour (mph) to meters per second (m/s) using **CONVERT**.  In cell **H2**, enter: **=CONVERT(D2, "mph", "m/s")**.

You can check if your conversion is correct by entering 8.5248 in a metric conversion tool, [metric-conversions.org/speed/miles-per-hour-to-meters-per-second.htm](https://www.metric-conversions.org/speed/miles-per-hour-to-meters-per-second.htm).

## Example 3: Lock data in a table

Using functions to convert data can lead to problems, which data professionals must be prepared to fix. For example, if a reference value changes, the calculated value also changes. Locking data in a table by changing it from a function to a value ensures a cell stays consistent even if the data around it changes.

1. Select cell **F2**. In the formula bar, notice that the contents of this cell are the function you entered in the previous example.
2. Right-click cell **F** and select **Copy** from the drop-down menu.
3. Right-click cell **G** and select **Paste special** from the drop-down menu. Then, select **Paste values only**. This option pastes only the values from the original selection, removing any formatting, functions, or other information.
4. Select cell **G2**.
5. In the formula bar, notice that the contents of this cell is a value. This means that the value won’t change when other cells change.

---

# Convert data in spreadsheets

n this reading, you will learn about converting data from one format to another. One of the ways to help ensure that you have an accurate analysis of your data is by putting all of it in the correct format. This is true even if you have already cleaned and processed your data. As a part of getting your data ready for analysis, you will need to convert and format your data early on in the process.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uk8iw8DURr2PIsPA1Ha9lA_dce6d0ad92a447fa8978106d9e3ab578_Screen-Shot-2021-02-08-at-4.23.47-PM.png?expiry=1716940800000&hmac=_zAN8wVtLudsbnMuEvZlnsU6u0A2GGGBjgQfQxZXNXU)

As a data analyst, there are lots of scenarios when you might need to convert data in a spreadsheet:

### **String to date**

- [**How to convert text to date in Excel**](https://www.ablebits.com/office-addins-blog/2015/03/26/excel-convert-text-date/#:~:text=Excel%20DATEVALUE%20function%20%2D%20change%20text,Excel%20recognizes%20as%20a%20date.&text=So%2C%20the%20formula%20to%20convert,stored%20as%20a%20text%20string.): Transforming a series of numbers into dates is a common scenario you will encounter. This resource will help you learn how to use Excel functions to convert text and numbers to dates, and how to turn text strings into dates without a formula.
- [**Google Sheets: Change date format:**](https://www.ablebits.com/office-addins-blog/2019/08/13/google-sheets-change-date-format/) If you are working with Google Sheets, this resource will demonstrate how to convert your text strings to dates and how to apply the different date formats available in Google Sheets.

### **String to numbers**

- [**How to convert text to number in Excel:**](https://www.ablebits.com/office-addins-blog/2018/07/18/excel-convert-text-to-number/) Even though you will have values in your spreadsheet that resemble numbers, they may not actually be numbers. This conversion is important because it will allow your numbers to add up and be used in formulas without errors in Excel.
- [**How to convert text to numbers in Google Sheets:**](https://productivityspot.com/convert-text-to-numbers-google-sheets/) This resource is useful if you are working in Google Sheets; it will demonstrate how to convert text strings to numbers in Google Sheets. It also includes multiple formulas you can apply to your own sheets, so you can find the method that works best for you.

### **Combining columns**

- [**Convert text from two or more cells:**](https://support.microsoft.com/en-us/office/combine-text-from-two-or-more-cells-into-one-cell-81ba0946-ce78-42ed-b3c3-21340eb164a6) Sometimes you may need to merge text from two or more cells. This Microsoft Support page guides you through two distinct ways you can accomplish this task without losing or altering your data. It also includes a step-by-step video tutorial to help guide you through the process.
- [**How to split or combine cells in Google Sheets:**](https://www.techrepublic.com/article/how-to-split-or-combine-text-cells-with-google-sheets/) This guide will demonstrate how to to split or combine cells using Google Sheets specifically. If you are using Google Sheets, this is a useful resource to reference if you need to combine cells. It includes an example using real data.

### **Number to percentage**

- [**Format numbers as percentages:**](https://support.microsoft.com/en-us/office/format-numbers-as-percentages-de49167b-d603-4450-bcaa-31fba6c7b6b4) Formatting numbers as percentages is a useful skill to have on any project. This Microsoft Support page will provide several techniques and tips for how to display your numbers as percentages.
- [**TO_PERCENT:**](https://support.google.com/docs/answer/3094284?hl=en) This Google Sheets support page demonstrates how to use the **TO_PERCENT** formula to convert numbers to percentages. It also includes links to other formulas that can help you convert strings.

**Pro tip:** Keep in mind that you may have lots of columns of data that require different formats. Consistency is key, and best practice is to make sure an entire column has the same format.

## Additional resources

If you find yourself needing to convert other types of data, you can find resources on [**Microsoft Support**](https://support.microsoft.com/) for Excel or [**Google Docs Editor Help**](https://support.google.com/docs/?hl=en#topic=1382883) for Google Sheets.

Converting data is quick and easy, and the same functions can be used again and again. You can also keep these links bookmarked for future use, so you will always have them ready in case any of these issues arise. Now that you know how to convert data, you are on your way to becoming a successful data analyst.

---

# Data validation

[index (14).mp4](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/index_(14).mp4)

**Key Points:**

- **What is data validation?**
    - A feature that allows you to control what can and can't be entered in your spreadsheet.
    - Helps to:
        - Reduce errors
        - Improve data consistency
        - Streamline data entry
- **Common uses of data validation:**
    - **Adding drop-down lists:**
        - Provides users with predetermined options to choose from.
        - Makes data entry easier and more consistent.
        - Example: Creating a "Status" column with options like "Not Yet Started," "In Progress," and "Ready."
    - **Creating custom checkboxes:**
        - Allows users to mark items with a simple checkbox.
        - Useful for tasks like approvals or completion status.
        - Example: Creating a "Review" column with checkboxes for "Approved" and "Not approved."
    - **Protecting structured data and formulas:**
        - Prevents accidental changes to formulas or data.
        - Ensures the integrity of your spreadsheet.
        - Example: Using data validation to reject invalid inputs in a formula-driven column.

**Benefits of using data validation:**

- **Improved data quality:** Reduces errors and ensures consistency.
- **Increased efficiency:** Makes data entry faster and easier.
- **Enhanced collaboration:** Makes it easier for multiple users to work on the same spreadsheet.
- **Reduced data cleaning:** Minimizes the need for manual data correction

---

# Conditional formatting

[index (15).mp4](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/index_(15).mp4)

**Key Points:**

- **Data Validation:**
    - Allows users to create drop-down menus in spreadsheets to ensure data accuracy and consistency.
    - Can be used to restrict the type of data that can be entered into a cell (e.g., numbers, dates, text).
    - Helps prevent errors and makes data entry more efficient.
- **Conditional Formatting:**
    - Changes the appearance of cells based on specific conditions.
    - Can be used to highlight important information, identify trends, and make data easier to understand.
    - Works in conjunction with data validation to create custom tools for spreadsheets.

**Example:**

- **Task Scheduling Table:**
    - Uses data validation to create drop-down menus for the "Status" column, ensuring users select from predefined options ("Not Yet Started", "In Progress", "Ready").
    - Uses conditional formatting to color-code cells based on the selected status:
        - "Not Yet Started" - Red
        - "In Progress" - Yellow
        - "Ready" - Green
    - This visual cue makes it easier to see how many tasks are in each stage of completion.
- **Upcoming Deadlines:**
    - Uses data validation to ensure users enter valid dates in the "Review By This Date" column.
    - Uses conditional formatting to highlight cells with dates after today in orange, providing a clear visual reminder of upcoming deadlines.

**Benefits of Combining Data Validation and Conditional Formatting:**

- **Improved data accuracy and consistency.**
- **Enhanced data visualization and analysis.**
- **Increased efficiency and productivity.**
- **Creation of custom tools tailored to specific needs.**

**Additional Notes:**

- The video demonstrates how to use these features in Google Sheets, but the concepts are applicable to other spreadsheet programs as well.
- Experimenting with different combinations of data validation and conditional formatting can lead to powerful and creative solutions for your spreadsheets.

---

# Transform data with SQL

Data analysts usually need to convert data from one format to another to complete an analysis. But what if you are using SQL rather than a spreadsheet? Just like spreadsheets, SQL uses standard rules to convert one type of data to another. If you are wondering why data transformation is an important skill to have as a data analyst, think of it like being a driver who is able to change a flat tire. Being able to convert data to the right format speeds you along in your analysis. You don’t have to wait for someone else to convert the data for you.

In this reading, you will go over the conversions that can be done using the **CAST** function. There are also more specialized functions like **COERCION** to work with big numbers, and **UNIX_DATE** to work with dates. **UNIX_DATE** returns the number of days that have passed since January 1, 1970 and is used to compare and work with dates across multiple time zones. You will likely use **CAST** most often.

## Common conversions

The following table summarizes some of the more common conversions made with the **CAST** function. Refer to [Conversion Rules in Standard SQL](https://cloud.google.com/bigquery/docs/reference/standard-sql/conversion_rules) for a full list of functions and associated rules.

| **Starting with** | **CAST function can convert to:** |
| --- | --- |
| Numeric (number) | - Integer
- Numeric (number)
- Big number
- Floating integer
- String |
| String | - Boolean
- Integer
- Numeric (number)
- Big number
- Floating integer
- String
- Bytes
- Date
- Date time
- Time
- Timestamp |
| Date | - String
- Date
- Date time
- Timestamp |

## The **CAST** function (syntax and examples)

**CAST** is an American National Standards Institute (ANSI) function used in lots of programming languages, including BigQuery. This section provides the BigQuery syntax and examples of converting the data types in the first column of the previous table. The syntax for the **CAST** function is as follows:

![Untitled](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/Untitled.png)

Where **expression** is the data to be converted and **typename** is the data type to be returned.

### **Converting a number to a string**

The following **CAST** statement returns a string from a numeric identified by the variable **MyCount** in the table called **MyTable**.

![Untitled](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/Untitled%201.png)

In the above SQL statement, the following occurs:

- **SELECT** indicates that you will be selecting data from a table
- **CAST** indicates that you will be converting the data you select to a different data type
- **AS** comes before and identifies the data type which you are casting to
- **STRING** indicates that you are converting the data to a string
- **FROM** indicates which table you are selecting the data from

### **Converting a string to a number**

The following **CAST** statement returns an integer from a string identified by the variable **MyVarcharCol** in the table called **MyTable**. (An integer is any whole number.)

![Untitled](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/Untitled%202.png)

In the above SQL statement, the following occurs:

- **SELECT** indicates that you will be selecting data from a table
- **CAST** indicates that you will be converting the data you select to a different data type
- **AS** comes before and identifies the data type which you are casting to
- **INT** indicates that you are converting the data to an integer
- **FROM** indicates which table you are selecting the data from

### **Converting a date to a string**

The following **CAST** statement returns a string from a date identified by the variable **MyDate** in the table called **MyTable**.

![Untitled](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/Untitled%203.png)

In the above SQL statement, the following occurs:

- **SELECT** indicates that you will be selecting data from a table
- **CAST** indicates that you will be converting the data you select to a different data type
- **AS** comes before and identifies the data type which you are casting to
- **STRING** indicates that you are converting the data to a string
- **FROM** indicates which table you are selecting the data from

### **Converting a date to a datetime**

Datetime values have the format of YYYY-MM-DD hh: mm: ss format, so date and time are retained together. The following **CAST** statement returns a datetime value from a date.

![Untitled](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/Untitled%204.png)

In the above SQL statement, the following occurs:

- **SELECT** indicates that you will be selecting data from a table
- **CAST** indicates that you will be converting the data you select to a different data type
- **AS** comes before and identifies the data type which you are casting to
- **DATETIME** indicates that you are converting the data to a datetime value
- **FROM** indicates which table you are selecting the data from

## The **SAFE_CAST** function

Using the **CAST** function in a query that fails returns an error in BigQuery. To avoid errors in the event of a failed query, use the **SAFE_CAST** function instead. The **SAFE_CAST** function returns a value of Null instead of an error when a query fails.

The syntax for **SAFE_CAST** is the same as for **CAST**. Simply substitute the function directly in your queries. The following **SAFE_CAST** statement returns a string from a date.

![Untitled](Formatting%20for%20better%20analysis%20da28e53f4a7c40fea3b9ba756904f63d/Untitled%205.png)

## More information

Browse these resources for more information about data conversion using other SQL dialects (instead of BigQuery):

- [CAST and CONVERT](https://docs.microsoft.com/en-us/sql/t-sql/functions/cast-and-convert-transact-sql?view=sql-server-ver15): SQL Server reference documentation
- [MySQL CAST Functions and Operators](https://dev.mysql.com/doc/refman/8.0/en/cast-functions.html): MySQL reference documentation
- [How to: SQL Type Casting](https://www.blendo.co/blog/how-to-sql-type-casting/): Blog about type casting that has links to other SQL short guides

---