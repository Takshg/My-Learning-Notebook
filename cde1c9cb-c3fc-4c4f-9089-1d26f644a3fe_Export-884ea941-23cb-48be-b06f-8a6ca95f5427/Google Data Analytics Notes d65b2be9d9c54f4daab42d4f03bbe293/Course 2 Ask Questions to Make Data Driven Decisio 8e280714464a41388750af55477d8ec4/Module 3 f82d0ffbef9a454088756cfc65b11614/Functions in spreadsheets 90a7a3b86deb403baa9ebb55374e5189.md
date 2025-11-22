# Functions in spreadsheets

---

# Step by Step: Functions 101

**What you’ll need**

If you’d like to access the other spreadsheet the instructor uses in this video, click the link to the dataset to create a copy. If you don’t have a Google account, you may download the data directly from the attachments below.

Link to sales data: [Monthly sales - Functions 101](https://docs.google.com/spreadsheets/d/1YINveZ3IpAPDJZh-FWzC7vhGl-I29QeZ9Khie84qUWY/template/preview?resourcekey=0-f5_V9Bq_9iJES6diyhIquA#gid=0)

OR

[Monthly Sales - Functions 101XLSX File](https://d3c33hcgiwev3.cloudfront.net/6H0TG5SwT-eRs7BMjVuP6g_235b110ee66f4eef96266005696784f1_Monthly-Sales---Functions-101.xlsx?Expires=1716508800&Signature=X5vkzi73JTSdCcCT4YXj6XI3z7f755YN8veBer90k0Qk2L61fjpIKOLirX5tGsUmSDwmhGgwtQbjFIwXW9ZCISE24R1t5crxtT3xV3v5ms5L8UclHTFB3vf8xB4FCPuqBumhxbfCmGGOXIPwwMsStp7G4iHSGs19IibkSTJ4-9I_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

## Example: Start with total sales

Use the **SUM** function to calculate the total value of a range of cells.

1. Open the [Monthly sales - Functions 101](https://docs.google.com/spreadsheets/d/1YINveZ3IpAPDJZh-FWzC7vhGl-I29QeZ9Khie84qUWY/template/preview?resourcekey=0-f5_V9Bq_9iJES6diyhIquA#gid=0) spreadsheet.
2. Select cell **F2**.
3. Enter **=SUM(B2:E2)** and press **Enter** to calculate the total sales for this time frame.

**Note:** The colon (:) between **B2** and **E2** in the formula indicates that you are specifying a range. In this case, it's the range of cells from **B2** to **E2**. The **SUM** function will add up the values in these cells to calculate the total sales for the specified time frame.

## Example: Copy functions using the fill handle

Use the fill handle to quickly copy a function to many cells.

1. In the **Monthly Sales** spreadsheet, select cell **F2** and click and hold the fill handle with your cursor. 	**Note:** The instructor refers to the fill handle as a “little box,” but in newer versions or interfaces, it is a circle.
2. Drag the fill handle to include cells **F3** and **F4** and release the fill handle.
3. The total sales for 2018 and 2019 are in the reference cells **F3** and **F4**, respectively. This happens because dragging the fill handle automatically updates the formula to account for the change in row, ensuring that the calculation remains accurate for each row you fill.
4. Click on cell **F3** to display its formula in the formula bar. This is a toolbar that shows information contained in a cell. It allows you to inspect the formula and ensure the formula is updated when it is copied from cell **F2** to cell **F3**.

## Example: Find the average sale

Use the **AVERAGE** function to find the average sale for each year.

1. In the **Monthly Sales** spreadsheet, select cell **G2**.
2. Enter **=AVERAGE(B2:E2)** and press **Enter** to calculate the average sales for 2017.
3. Use the fill handle or copy and paste the function from cell **G2** to cells **G3** and **G4** to calculate the average sales for 2018 and 2019, respectively.

## Example: Use formulas for special cases

Some calculations may not have dedicated functions. For example, to calculate the percent change from June to July, you’ll need to use the percent change formula you used earlier in the course.

1. In the **Monthly Sales** spreadsheet, select cell **H2** and enter **=(E2-D2)/D2**. Press **Enter** to calculate the percent change from June to July 2017.
2. Copy the function from cell **H2** and paste it to cells **H3** and **H4** to calculate the percent change from June to July of 2018 and 2019, respectively.
3. Select reference cells **H2**, **H3**, and **H4** and press the percentage (**%**) button to show the changes in percentages.

## Example: Find the lowest and highest sales

To find the lowest monthly sales (**MIN** function):

1. In the **Monthly Sales** spreadsheet, select cell **I1** and enter **Lowest Monthly Sales**.
2. Select cell **I2** and enter **=MIN(** , then use your cursor to select the values from all three rows, **B2:E4**, and then enter  **)**  to close the parenthetical. To select a block of cells:	a. Click and hold your cursor on cell **B2**.	b. While holding the cursor, drag it across all the values you want to include in the calculation (in this case, from **B2** to **E4**).	c. Release the cursor to select all the values and enter  **)**  . Your spreadsheet will automatically fill in the cell references for you.
3. This may be important information for your stakeholders, so fill the cell with a color to make it stand out:	a. Select cell **D2**.	b. From the toolbar, choose the paint bucket icon.	c. Select a color of your choice from the color palette that appears. That color will then fill cell **D2**.

To find the highest monthly sales (**MAX** function):

1. Select cell **J1** and enter **Highest Monthly Sales**.
2. Select cell **J2** and enter **=MAX(** , then use your cursor to select the values from all three rows, **B2:E4**, and then enter  **)**  to close the parenthetical.
3. This may be important information for your stakeholders, so select cell **E4** and fill the cell with a color of your choice to make it stand out.	a. Select cell **E4**.	b. From the toolbar, choose the paint bucket icon.	c. Select a color of your choice from the color palette that appears. That color will fill cell **E4**.

## Example: Fix errors

When you encounter errors, be sure to troubleshoot the format of your functions and formulas in the formula bar.

---

# Functions 101

**Key Points:**

- **Formulas:**
    - Combine data and perform calculations.
    - Can be copied and pasted for efficiency.
    - Useful for basic operations like addition, subtraction, multiplication, and division.
- **Functions:**
    - Preset commands that automate specific tasks.
    - Often have descriptive names indicating their purpose.
    - Examples include SUM, AVERAGE, MIN, and MAX.
    - Can be used to find specific values, calculate percentages, and more.
- **Fill Handle:**
    - A tool for copying formulas and functions across cells.
    - Automatically adjusts cell references to match the new location.
    - Saves time and reduces manual effort.

**Definitions:**

- **Formula:** A combination of operators, values, and cell references that performs a calculation.
- **Function:** A pre-built formula that performs a specific task.
- **Fill Handle:** A small square in the bottom right corner of a cell that allows you to copy formulas and functions to other cells.

**Additional Notes:**

- The video emphasizes the importance of checking the format of formulas and functions to avoid errors.
- It encourages learners to experiment with different formulas and functions to gain a deeper understanding of their capabilities.
- The video concludes by highlighting the power of spreadsheets and the exciting possibilities they offer for data analysis.

**Real-Life Example:**

Imagine you're a sales manager analyzing monthly sales data. You can use the SUM function to calculate total sales for each month, the AVERAGE function to find the average sale, and the MIN and MAX functions to identify the lowest and highest monthly sales. This information can be used to identify trends, set targets, and make informed decisions about sales strategies.

**Remember:**

- Practice using formulas and functions to become proficient in spreadsheet analysis.
- Explore the vast array of functions available to discover their potential for your specific needs.
- Utilize the fill handle to save time and effort when working with large datasets.

---

# Quick Reference: Functions in spreadsheets

As a quick refresher, a function is a preset command that automatically performs a specific process or task using the data in a spreadsheet. Functions give data analysts the ability to do calculations, which can be anything from simple arithmetic to complex equations. Use this reading to help you keep track of some of the most useful options.

## Functions

### **The basics**

- Just like formulas, start all of your functions with an equal sign; for example **=SUM**. The equal sign tells the spreadsheet that what follows is part of a function, not just a word or number in a cell.
- After you enter the equal sign, most spreadsheet applications will display an autocomplete menu that lists valid functions, names, and text strings. This is a great way to create and edit functions while avoiding typing and syntax errors.
- A fun way to learn new functions is by simply typing an equal sign and a single letter of the alphabet. Choose one of the options that pops up and learn what that function does.

### **Difference between formulas and functions**

- A formula is a set of instructions used to perform a calculation using the data in a spreadsheet.
- A function is a preset command that automatically performs a specific process or task using the data in a spreadsheet.

### **Popular functions**

A lot of people don’t realize that keyboard shortcuts like cut, save, and find are actually functions. These functions are built into an application and are amazing time-savers. Using shortcuts lets you do more with less effort. They can make you more efficient and productive because you are not constantly reaching for the mouse and navigating menus. Use these links to discover the most popular shortcuts, for [Chromebook](https://support.google.com/chromebook/answer/183101?hl=en), [PC](https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec), and [Mac](https://support.apple.com/en-us/HT201236).

### **Auto-filling**

The lower-right corner of each cell has a fill handle. It is a small green square in Microsoft Excel and a small blue circle in Google Sheets.

- Click the fill handle for a cell and drag it down a column to auto-fill other cells in the column with the same formula or function used in that cell.
- Click the fill handle for a cell and drag it across a row to auto-fill other cells in the row with the same formula or function used in that cell.

### **Relative, absolute, and mixed references**

- Relative references (cells referenced without a dollar sign, like **A2**) will change when you copy and paste the function into a different cell. With relative references, the location of the cell that contains the function determines the cells used by the function.
- Absolute references (cells fully referenced with a dollar sign, like **$A$2**) will not change when you copy and paste the function into a different cell. With absolute references, the cells referenced always remain the same.
- Mixed references (cells partially referenced with a dollar sign, like **$A2** or **A$2**) will change when you copy and paste the function into a different cell. With mixed references, the location of the cell that contains the function determines the cells used by the function, but only the row or column is relative (not both).
- In spreadsheets, you can press the **F4** key to toggle between relative, absolute, and mixed references in a function. Click the cell containing the function, highlight the referenced cells in the formula bar, and then press **F4** to toggle between and select relative, absolute, or mixed referencing.

### **Data ranges**

- When you click a cell that contains a function, colored data ranges in the formula bar indicate which cells are being used in the spreadsheet. There are different colors for each unique range in a function.
- Colored data ranges help prevent you from getting lost in complex functions.
- In spreadsheets, you can press the **F2** key to highlight the range of data used by a function. Click the cell containing the function, highlight the range of data used by the function in the formula bar, and then press **F2**. The spreadsheet will go to and highlight the cells specified by the range.

### **Data ranges evaluated for a condition**

**COUNTIF** is an example of a function that returns a value based on a condition that the data range is evaluated for. The function counts the number of cells that meet the criteria. For example, in an expense spreadsheet, use **COUNTIF** to count the number of cells that contain a reimbursement for "airfare."

For more information, refer to:

- [Microsoft Support's page for COUNTIF](https://support.microsoft.com/en-us/office/countif-function-e0de10c6-f885-4e71-abb4-1f464816df34)
- [Google Help Center's documentation for COUNTIF](https://support.google.com/docs/answer/3093480?hl=en) where you can copy a sheet with [COUNTIF examples](https://docs.google.com/spreadsheets/d/1PYoKCYZAkWSaMBsiTyvxZzCCt2WQ-QKOC763RWHMB7c/template/preview) (click "Use Template" if you click the COUNTIF link provided on this page)

## Key takeaways

There are a lot more functions that can help you make the most of your data. This is just the start. You can keep learning how to use functions to help you solve complex problems efficiently and accurately throughout your entire career.

---

# Hands-on Activity: Create a custom data table

Review the following scenario. Then complete the step-by-step instructions.

The agency has asked your team to optimize its online application process. Your assignment is to summarize the agency’s job application data. In particular, you want to answer the following questions:

- What was the total number of applications received each month?
- How many applications were received?
- In which months were the lowest and highest number of applications received?
- What was the average number of applications received per month?

To do this, you’ll work with a spreadsheet. You’ll use spreadsheet functions to make calculations based on your data and create a custom data table to summarize your results.

By the time you complete this activity, you will be able to import a spreadsheet file, sort data, create a custom data table, and use spreadsheet functions to work with your data. Spreadsheets are an essential tool for every data analyst. Using spreadsheets to organize and analyze data is an important skill that you will continue to develop throughout your career.

## Understanding the data

The agency’s data contains information about all of the data analytics job applications received. The data includes the following column headers: **Applicant ID**, **Date**, **Job Title**, **Job Location**, **Hired**, and **Easy** Apply. Below is a description of each column header and sample values.

| Column Name | Column Description | Sample Data |
| --- | --- | --- |
| Applicant ID | Unique identifier for the applicants | 11578773 |
| Date | The date and time each application was received | 1/1/2023 0:01:00 |
| Job Title | The data analytics position applied for | PHARMACEUTICAL DATA ANALYST |
| Job Location | Where the job is located | Lima, Peru |
| Hired | Indicates if an applicant was hired | TRUE |
| Easy Apply | TRUE if the application was submitted directly on the agency's website; FALSE if the application was downloaded and submitted via email | TRUE |

## Sort Your data

Because you want to answer questions based on a specific timeframe (in this case, applications received per month in 2023), start by sorting the data by date. **Sorting** involves arranging data into a meaningful order to make it easier to understand, analyze, and visualize. Considering the order in which each application was received can help you discover trends in data analytics job applications.

1. First, rename your spreadsheet. Select **Untitled Spreadsheet** and enter a new name. Use **data_analyst_jobs_2023** or a similar name that clearly describes the data your spreadsheet contains.
2. When you are working in a spreadsheet, you can have multiple sheets open. Currently, your spreadsheet contains one sheet labeled **2023_data_analyst_job**. Rename this sheet by selecting the sheet tab and choosing **Rename** from the menu. Then, enter **raw data**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rwECdYI7QPe_KJk1QC9Wsw_0a75e88132114dc591a9232a48cc67f1_g5MVO5kFSsSvEwUhiTB4hQ_2eb3ed103b624e369d19af433e75f4e1_C2M3L3A1-1.png?expiry=1716508800000&hmac=EjQL7WFFcM-5hTmmgnbiBqepDKKf-vnM4tYO2NuS2sM)

3. Make the columns **Job Title** (C) and **Job Location** (D) wider by dragging the right boundary of the column headings.

4. Select all the data in the spreadsheet by selecting the cell where the rows and columns intersect.

5. From the menu bar, select **Data > Sort range > Advanced range sorting options**.

6. In the pop-up window, select the **Data has header row** box.

7. In the **Sort by** dropdown, choose the header **Date**. Then, select **A to Z** to sort in ascending order.

8. Finally, select **Sort**.

Your spreadsheet now displays job applications received in chronological order.

## Create a custom data table

Now that you’ve sorted your data, you’re ready to create a custom data table to help you answer each of your questions. Your table will clearly summarize the data. Plus, if you want to share your results, your table will be well-organized and easy to understand.

**Count the number of applications received each month**

First, use spreadsheet functions to help you find the total number of applications received in each month.

1. To start, select the **Add sheet** icon (the plus sign) in the menu bar to add a new sheet to your spreadsheet. You’ll create your data table in this sheet

2. Rename the new sheet. Select the sheet tab and choose **Rename** on the menu. Then, enter **summary data**.

3. Next, add column headers to your table. In cell A1 of your **summary data** sheet, enter **Month**. In cell B1, enter **Applications**.

4. Underneath the **Month** label in cell A2, enter **January**. Press **Enter**.

5. Now, use autofill to add the rest of the months of the year. Select cell A2 again. The fill handle will appear in the cell. Select on the fill handle and drag it down to cell A13 to autofill all the months of the year.

6. Next, convert the number values in the **Date** column in the **raw data** sheet into text. Select the **raw data** tab to return to the **raw data** sheet. In cell G1, enter **Month**.

7. The **TEXT** function converts a number into text according to a specified format. In this case, list them in which an application was received. Use the format “mmmm” for the full name of the month. In cell G2, enter the following code (do not copy+paste):

**=TEXT(B2,"mmmm")**

The first entry **B2** refers to the cell you want to convert. The second entry **("mmmm")** refers to the specific format you want to use. Press **Enter**.

(**Note:** It is *very important* that you manually enter  all formulas and functions. They should not be copied and pasted from the activity, as this will result in an error message.)

8. If a box pops up with the option to autofill the column, select the check mark or enter **Ctrl + Enter** (Windows) or **Cmd + Return** (Mac). If this box does not pop up, select cell G2. Then, **double-click** on the fill handle to copy the function down the column. This will populate all the cells in the column with the corresponding month.

9. Now you're ready to total the applications by month. You could do this manually, by filtering the data and counting the number of entries for each month, but this would take a long time and be prone to errors. Instead, use the **COUNTIF** function.

10. The **COUNTIF** function quickly counts how many items in a range of cells meet a given criterion. First, select the **summary data** tab to return to your **summary data** sheet. Then, in cell B2, enter **=COUNTIF('raw data'!G:G,A2)**. The first entry **'raw data'!G:G** refers to the range where you are counting the data. The range is located on your **raw data** sheet **'raw data'!** and includes all column G **G:G** entries. This column contains the data for months. The second entry **A2** refers to the criterion you want to count. In this case, it’s “January,” the value in cell A2 of your **summary data** sheet. The function calculates how many times **January** (the criterion) appears in the **Month** column (the range).

11. Press **Enter**. You’ll notice the value 2387 appears in cell B2. This means that 2,387 job applications were submitted in January.

12. Select cell B2. **Double-click** the fill handle to copy the function down through cell B13.

Now your table lists the total number of applications submitted for each month:

| **Month** | **Applications** |
| --- | --- |
| January | 2387 |
| February | 2312 |
| March | 2536 |
| April | 2544 |
| May | 2954 |
| June | 2990 |
| July | 3138 |
| August | 2969 |
| September | 2865 |
| October | 2751 |
| November | 2508 |
| December | 2642 |

## Find the total number of applications received

Now that you’ve calculated the number of applications received in each month, use spreadsheet formulas to calculate the total number of applications received.

1. Label the cell in which you’ll calculate your result. In cell A14, enter **Total**.
2. In cell B14, enter **=SUM(B2:B13)**. This function calculates the number of applications received from January through December.
3. Cell B14 contains the total number of applications, 32596.

## Find the average number of applications received per month

Use the **AVERAGE** function to calculate this information.

1. First, make labels for your results. In cell A18, enter **Avg**.
2. The **AVERAGE** function returns the average value in a numeric dataset. In cell B18, enter **=AVERAGE(B2:B13)**. The result, 2716.33, is the average number of monthly applications received in 2023.

Your work will help your team discover important trends and patterns in the agency’s data and generate insights for optimizing the application process. For example, because your findings reveal that February was the slowest month, the agency can devote more of its advertising and outreach budget to February and less to the peak month of July. This is the strategic impact of data analysis.