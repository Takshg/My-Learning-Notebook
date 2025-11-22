# Continue cleaning data in spreadsheet - Part 1.

---

# Step-by-Step guide: Data-cleaning features in spreadsheets

This reading outlines the steps the instructor performs in the next video, [Data-cleaning features in spreadsheets](https://www.coursera.org/learn/process-data/lecture/Ez3u5/data-cleaning-features-in-spreadsheets). In the video, the instructor explains how to use menu options in spreadsheets to fix errors.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

If you’d like to follow along with the examples in this video, choose a spreadsheet tool. Google Sheets or Excel are recommended.

To access the spreadsheet the instructor uses in this video, click the link to the template to create a copy of the dataset. If you don’t have a Google account, download the data directly from the attachments below.

Link to logistics data:  [International Logistics Association Memberships - Data for Cleaning](https://docs.google.com/spreadsheets/d/1jmxXS6ZJEMtaoli5__qApb9LE_nXkU2ysf5c8N1tiQA/template/preview)

Link to cosmetics data: [Cosmetics Inc. - Data for Cleaning](https://docs.google.com/spreadsheets/d/12U9Y4IVAGwml7XWBBgC4j9l0cCjqIZlqJc9vu3jr6Ig/template/preview?resourcekey=0-ds9iuh8tsuB7PwGd2dHMDA#gid=0)

OR

[International Logistics Association Memberships - Data for CleaningXLSX File](https://d3c33hcgiwev3.cloudfront.net/5zlIemyvQtKsj4BGZQEdxA_7f286fde512b4f14b3246a6e68b333e1_International-Logistics-Association-Memberships---Data-for-Cleaning.xlsx?Expires=1716854400&Signature=bE1kBck2NG7c9F8IfDBWAxk1GfYVxzGos8zMefWLRNHi8B94M72GVh~mc92IWwPNI7XTtLFsHhgriII0peXdN3nn1nH3fcuHZyBZwJFoGQsLDjala~VXVzOzgwe5bRmBbqdZPpIR3FQeeGafNspmQDqug5fO7A4ZKPiJpPeD16w_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Cosmetics Inc. - Data for CleaningXLSX File](https://d3c33hcgiwev3.cloudfront.net/t3_O7KI_Rp6KVfCyGvTxGA_26e91b3aa1d44284956a4ae860d114e1_Cosmetics-Inc.---Data-for-Cleaning.xlsx?Expires=1716854400&Signature=KwadKtQIrjiTY-W2K7EeP49xl8A8glSI8SAWRtAQH8HbxnMiWnmTzxhVAZpZNBKlTyV0iEwqmvRFh5hpZ~Z59SiDOwBd1w2WckTIdVlkZEl5Bek4QnpLg4G1lR3O25UQMh9Tgx17iK~cZpc-3i3qzq~rHuphchNynmv7qLlc-hI_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3UWxlyqNRxaFsZcqjZcWgQ_3fd91ae61ce04caaa755c3477a337947_line-y.png?expiry=1716854400000&hmac=yjCSowGMfy4MFIfUa2He6nVGJ4klUlOx0-hTmys7Dkk)

## Example 1: Use conditional formatting to highlight blank cells

Conditional formatting is a spreadsheet tool that changes how cells appear when values meet specific conditions.

1. Open the spreadsheet [International Logistics Association Memberships - Data for Cleaning](https://docs.google.com/spreadsheets/d/1jmxXS6ZJEMtaoli5__qApb9LE_nXkU2ysf5c8N1tiQA/template/preview).
2. Select the range of cells to which you’ll apply conditional formatting. In this example, you’ll select **columns A** through **L**, except for **columns F** and **H**. To select all columns except for **F** and **H**:	a. Select cell **A** to highlight **column A**.	b. Hold down the SHIFT key and at the same time use your mouse to select cell **E**. This will highlight all the columns between **A** and **E**.	c. To select the remainder of the columns, hold down the CONTROL (Windows) or COMMAND (Mac) key while you select cells **G**, **I**, **J**, **K**, and **L**.	d. **Columns A** through **L** in your spreadsheet should be highlighted except **Column F** and **Column H**.
3. From the menu, select **Format**, then **Conditional formatting**. The columns you’ve selected should turn a light shade of green, and a new **Conditional format rules** tool will appear. Additionally, the **Apply to range** field should indicate the cells you’ve selected.
4. Next, apply a condition to these cells to change the cell color if the cell is empty. In the **Format cells if** drop-down, select **Cell is empty**.
5. Select the **Formatting style** field. Select a bright color from the drop-down to make the blank cells stand out.
6. Select **Done**.

## Example 2: Remove duplicates

Remove duplicates is a spreadsheet tool that automatically searches for and eliminates duplicate entries from a spreadsheet. This is faster and easier than searching the data by scrolling through it.

1. Create a copy of your dataset by right clicking the **Association ABC membership** tab and selecting **Duplicate**. This is a good practice, as it protects against accidentally deleting important data. Continue working in the new sheet, **Copy of Association ABC memberships**.
2. In the menu, select **Data**, then **Data cleanup**, then **Remove duplicates**.
3. Check the box next to **Data has header row**.
4. Check the box next to **Select All** to inspect the entire spreadsheet.
5. Select **Remove duplicates**.

## Example 3: Format dates consistently

Format dates to make all of the data in your spreadsheet consistent. This makes items easier to find and manipulate.

1. Select **column J** (Membership valid through), which contains dates.
2. From the menu, select **Format**, then **Number**, then **Date**.

## Example 4: Use split to separate data into columns

The split menu option is helpful when you have more than one piece of data in a cell and you want to separate those pieces of data into different cells.

1. Select **column L** (Certification).
2. In the menu, select **Data**, then **Split text to columns**.
3. The delimiter (for example, a comma) will be automatically detected.
4. If needed, specify the separator manually in the dropdown that appears in your spreadsheet.

## Example 5: Use split to fix numbers stored as text

**SPLIT** is a spreadsheet function that divides text around a specified character and puts each fragment into a new, separate cell.

1. Open the spreadsheet [Cosmetics Inc. - Data for Cleaning](https://docs.google.com/spreadsheets/d/12U9Y4IVAGwml7XWBBgC4j9l0cCjqIZlqJc9vu3jr6Ig/template/preview?resourcekey=0-ds9iuh8tsuB7PwGd2dHMDA#gid=0).
2. Notice that cell **F12** contains an error.
3. Select **column E** (Orders).
4. In the menu select **Data**, then select **Split text to columns**.
5. This removes the quotation marks from cell **E12** so the spreadsheet recognizes the data in the cell as a number. This resolves the error in cell **F12**.

---

# Data-cleaning feature in spreadsheet

**Key Points:**

- **Conditional Formatting:** This tool highlights cells based on specific conditions, making it easier to identify missing information or data that doesn't meet certain criteria.
- **Remove Duplicates:** This tool automatically eliminates duplicate entries from a spreadsheet, ensuring data accuracy and consistency.
- **Format Dates:** This tool ensures all dates in a spreadsheet have a consistent format, making it easier to analyze temporal trends and patterns.
- **Split Text to Columns:** This tool separates text strings into individual columns based on a specified delimiter, allowing for easier analysis of individual data points.
- **Text String & Substring:** A text string is a group of characters within a cell, while a substring is a smaller subset of a text string. Understanding these concepts is crucial for using the Split Text to Columns tool effectively.
- **CONCATENATE:** This function joins multiple text strings into a single string, which can be useful for combining data points or creating new variables.

**Definitions:**

- **Data Cleaning:** The process of identifying and correcting errors, inconsistencies, and missing values in a dataset.
- **Spreadsheet Tools:** Software features designed to manipulate and analyze data within spreadsheets.
- **Delimiter:** A specific character used to separate data points within a text string.
- **Data Analysis:** The process of examining and interpreting data to extract meaningful insights and patterns.

**Real-Life Examples:**

- **Analyzing Association Memberships:** Using conditional formatting to identify missing information in member data, removing duplicate entries, and formatting dates to analyze membership trends.
- **Analyzing Professional Certifications:** Using the Split Text to Columns tool to separate certifications listed in a single cell and analyze the distribution of different certifications among members.
- **Calculating Total Profits:** Using the Split Text to Columns tool to convert text values to numbers and perform calculations on financial data.

---

# Step-by-Step: Optimize the data-cleaning process

This reading outlines steps the instructor performs in the following video, [Optimize the data-cleaning process](https://www.coursera.org/learn/process-data/lecture/ohiCl/optimize-the-data-cleaning-process). The video teaches some useful spreadsheet functions, which can make your data-cleaning even more successful.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

### **What you’ll need**

If you would like to access the spreadsheet the instructor uses in this video, click the link to the dataset to create a copy. If you don’t have a Google account, you may download the data directly from the attachments below.

Link to logistics data:  [International Logistics Association Memberships - Data for Cleaning](https://docs.google.com/spreadsheets/d/1jmxXS6ZJEMtaoli5__qApb9LE_nXkU2ysf5c8N1tiQA/template/preview)

Link to cosmetics data: [Cosmetics Inc. - Data for Cleaning](https://docs.google.com/spreadsheets/d/12U9Y4IVAGwml7XWBBgC4j9l0cCjqIZlqJc9vu3jr6Ig/template/preview?resourcekey=0-ds9iuh8tsuB7PwGd2dHMDA#gid=0)

OR

[International Logistics Association Memberships - Data for CleaningXLSX File](https://d3c33hcgiwev3.cloudfront.net/p1JSr3UeTOOi_2-3Yr67dg_2e42a0117ecc42978ff39c15b0fbd3f1_International-Logistics-Association-Memberships---Data-for-Cleaning.xlsx?Expires=1716854400&Signature=XsEwMUqtzVtafqjVm76XKN6bvbHTHj4~uSxWmOZoFx5qffYhTFDG2w9gG8QMqrnZgjqLOuHRV9J501~pfIUAVxfCyS-n~ETg6nCbcJ4rR5pju2CSXGs3r9me6OqYDRIwRKWsG5CEXSM93GwdIBrNQcugGkcEL6hxCD0roQmxWh4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Cosmetics Inc. - Data for CleaningXLSX File](https://d3c33hcgiwev3.cloudfront.net/htYeVDpXRHCUSNSclnWcqQ_06ea60f3250b4ba2a59e4fc7d2e2a5e1_Cosmetics-Inc.---Data-for-Cleaning.xlsx?Expires=1716854400&Signature=i3z3T-BdFADA-vfzy9SeyRjf69-9Pwk8RA-UApdB6kW09ry55vJL1irqfInCyCHocGvOLVRoyZt0lJeQhCsTYSVoVC5td1aXgG2vWtozIlWMx0XuB-U9uAjYZZQ-HZwDnNb6pXDsJ-ntTX0~ibfVR88DdnP~UKmChUklGsyZ79g_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3UWxlyqNRxaFsZcqjZcWgQ_3fd91ae61ce04caaa755c3477a337947_line-y.png?expiry=1716854400000&hmac=yjCSowGMfy4MFIfUa2He6nVGJ4klUlOx0-hTmys7Dkk)

## Example 1: The **COUNTIF** function

**COUNTIF** is a spreadsheet function that returns the number of cells within a range that match a specified value.

### **Use COUNTIF to find numbers lower than 100**

1. Open the International [Logistics Association Memberships - Data for Cleaning](https://docs.google.com/spreadsheets/d/1jmxXS6ZJEMtaoli5__qApb9LE_nXkU2ysf5c8N1tiQA/template/preview) dataset, and scroll down to row 74.
    1. **Note:** The dataset has 72 rows, and row 73 is left blank for separation.
2. In cell **H74**, enter **Member Dues < 100** to label the calculation.
3. In cell **I74**, enter the formula **=COUNTIF(I2:I72,"<100")** to count how many members in the cell range **I2:I72** pay dues of less than $100. This formula returns a value of 1, indicating one value is below $100.
4. In cell **I55**, change -$200 to $200. Cell **I74** should now display the value 0.

### **Use COUNTIF to find numbers higher than 500**

1. In cell **H75**, enter **Member Dues > 500**.
2. In cell **I75**, enter the formula **=COUNTIF(I2:I72,">500")** to count how many members in cell range **I2:I72** pay dues of greater than 500. This formula returns a value of 1, indicating one value is above 500.
3. In cell **I44**, change $1,000 to $100. Cell **I75** should now display the value 0.

## Example 2: The **LEN** function

The **LEN** function is useful if you have a certain piece of information in your spreadsheet that you know must contain a certain length.

1. Right click cell **A**.
2. Select **+ Insert one column right** to create a new, empty column.
3. Select cell **B1** and enter **LEN** to name the new column.
4. In cell **B2**, enter **=LEN(A2)**. This function references the value of cell **A2** and returns its length, 6.
5. Double-click on the lower right corner of cell **B2**. This will copy the function through the rest of the column. Each cell will show the length of the Member ID in that row.

## Example 3: Use conditional formatting

Conditional formatting is a spreadsheet tool that changes how cells appear when values meet specific conditions.

1. To highlight all of column **B** except for the header, select cell **B**. Then press CONTROL (Windows) or COMMAND (MAC) and select cell **B1**.
2. Navigate to the **Format** menu, and choose **Conditional Formatting**.
3. Set the **Format rules** field to **Is not equal to** and enter **6** as the value.
4. Select **Done**.
5. Notice cell **B36** is highlighted because its value is 7.

## Example 4: The **LEFT** and **RIGHT** functions

**LEFT** is a function that returns a set number of characters from the left side of a text string. **RIGHT** is a function that returns a set number of characters from the right side of a text string.

### **The LEFT function**

1. Use the [Cosmetics Inc. - Data for Cleaning](https://docs.google.com/spreadsheets/d/12U9Y4IVAGwml7XWBBgC4j9l0cCjqIZlqJc9vu3jr6Ig/template/preview?resourcekey=0-ds9iuh8tsuB7PwGd2dHMDA#gid=0) dataset.
2. Select cell **H1**, and enter **Left**.
3. In cell **H2**, enter **=LEFT(A2, 5)** to extract the first five characters from cell **A2**. This function will show the substring 51993.
4. Select cell **H2**.
5. Select and hold the fill handle, the small circle in the corner of a selected cell, then drag this formula down to populate the rest of this column.

### **The RIGHT function**

1. Select cell **I1**, and enter **Right**.
2. In cell **I2**, enter **=RIGHT(A2, 4)** to extract the last four characters from cell **A2**. This function will show the substring Masc.
3. Select cell **I2**.
4. Select and hold the fill handle and drag this formula down to populate the rest of this column.

## Example 5: The **MID** function

MID is a function that returns a segment from the middle of a text string.

1. Select cell **J1**, and enter **Mid**.
2. In cell **J2**, enter **=MID(D2, 4, 2)** to extract the two-letter state code that starts at character four in cell **D2**.
3. Double-click the fill handle and to automatically populate the rest of this column.

## Example 6: The **CONCATENATE** function

**CONCATENATE** is a spreadsheet function that joins together two or more text strings.

1. Select cell **K1**, and enter **Concatenate**.
2. In cell **K2**, enter **=CONCATENATE(H2, I2)** to combine the values from columns ****H and I.
3. Double-click the fill handle and to automatically populate the rest of this column.

## Example 7: **TRIM function**

**TRIM** is a function that removes leading, trailing, and repeated spaces in data.

1. Select cell **L1**, and enter **Trim**.
2. In cell **L2**, enter **=TRIM(C2)** to remove any leading, trailing, or repeated spaces.
3. Double-click the fill handle and to automatically populate the rest of this column.

---

# Optimize the data-cleaning process

**Functions Covered:**

- **COUNTIF:** Counts the number of cells that match a specified value.
- **LEN:** Returns the length of a text string.
- **LEFT:** Extracts a specified number of characters from the left side of a text string.
- **RIGHT:** Extracts a specified number of characters from the right side of a text string.
- **MID:** Extracts a specified number of characters from the middle of a text string.
- **CONCATENATE:** Joins two or more text strings together.
- **TRIM:** Removes leading, trailing, and repeated spaces in data.

**Key Points:**

- **COUNTIF:** Useful for identifying data errors like negative values or outliers.
- **LEN:** Useful for ensuring data consistency, like verifying ID codes have the correct number of digits.
- **LEFT/RIGHT:** Useful for extracting specific parts of text strings, like separating product codes from identifiers.
- **MID:** Useful for extracting specific parts of text strings, like extracting state abbreviations from client codes.
- **CONCATENATE:** Useful for combining separate parts of text strings back together.
- **TRIM:** Useful for removing extra spaces that can interfere with data analysis.

**Definitions:**

- **Function:** A set of instructions that performs a specific calculation using data in a spreadsheet.
- **Syntax:** The predetermined structure of a function, including required information and its placement.
- **Text string:** A group of characters within a cell, commonly composed of letters, numbers, or both.
- **Substring:** A part of a text string.

**Additional Notes:**

- The video demonstrates each function with practical examples using spreadsheet data.
- Conditional formatting can be used to highlight cells that meet specific criteria based on functions.
- These functions can be combined with other data cleaning techniques to improve data quality.

---

# Workflow automation

In this reading, you will learn about workflow automation and how it can help you work faster and more efficiently. Basically, workflow automation is the process of automating parts of your work. That could mean creating an event trigger that sends a notification when a system is updated. Or it could mean automating parts of the data cleaning process. As you can probably imagine, automating different parts of your work can save you tons of time, increase productivity, and give you more bandwidth to focus on other important aspects of the job.

## What can be automated?

Automation sounds amazing, doesn’t it? But as convenient as it is, there are still some parts of the job that can’t be automated. Let's take a look at some things we can automate and some things that we can’t.

| **Task** | **Can it be automated?** | **Why?** |
| --- | --- | --- |
| Communicating with your team and stakeholders | No | Communication is key to understanding the needs of your team and stakeholders as you complete the tasks you are working on. There is no replacement for person-to-person communications. |
| Presenting your findings | No | Presenting your data is a big part of your job as a data analyst. Making data accessible and understandable to stakeholders and creating data visualizations can’t be automated for the same reasons that communications can’t be automated. |
| Preparing and cleaning data | Partially | Some tasks in data preparation and cleaning can be automated by setting up specific processes, like using a programming script to automatically detect missing values. |
| Data exploration | Partially | Sometimes the best way to understand data is to see it. Luckily, there are plenty of tools available that can help automate the process of visualizing data. These tools can speed up the process of visualizing and understanding the data, but the exploration itself still needs to be done by a data analyst. |
| Modeling the data | Yes | Data modeling is a difficult process that involves lots of different factors; luckily there are tools that can completely automate the different stages. |

## More about automating data cleaning

One of the most important ways you can streamline your data cleaning is to clean data where it lives. This will benefit your whole team, and it also means you don’t have to repeat the process over and over. For example, you could create a programming script that counted the number of words in each spreadsheet file stored in a specific folder. Using tools that can be used where your data is stored means that you don’t have to repeat your cleaning steps, saving you and your team time and energy.

## More resources

There are a lot of tools out there that can help automate your processes, and those tools are improving all the time. Here are a few articles or blogs you can check out if you want to learn more about workflow automation and the different tools out there for you to use:

- Towards Data Science’s [**Automating Scientific Data Analysis**](https://towardsdatascience.com/automating-scientific-data-analysis-part-1-c9979cd0817e)
- MIT News’ [**Automating Big-Data Analysis**](https://news.mit.edu/2016/automating-big-data-analysis-1021)
- TechnologyAdvice’s [**10 of the Best Options for Workflow Automation Software**](https://technologyadvice.com/blog/information-technology/top-10-workflow-automation-software/)

## Key takeaways

As a data analyst, automation can save you a lot of time and energy, and free you up to focus more on other parts of your project. The more analysis you do, the more ways you will find to make your processes simpler and more streamlined.

---

# Step-by-Step: Different data perspectives

This reading outlines the steps the instructor performs in the next video, [Different data perspectives](https://www.coursera.org/learn/process-data/lecture/BcY0L/different-data-perspectives). The video teaches you different methods data analysts use to view data differently and how looking at different views leads to more efficient and effective data cleaning.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

### **What you’ll need**

If you’d like to follow along with the examples in this video, choose a spreadsheet tool. Google Sheets or Excel are recommended.

To access the spreadsheet the instructor uses in this video, click the link to the template to create a copy of the dataset. If you don’t have a Google account, download the data directly from the attachments below.

Link to template: [Cosmetics, Inc](https://docs.google.com/spreadsheets/d/1J8wiEi7R9Jt3kNOjV1Bp-w1Zw1GvIbXgd78EeoXT9Mg/template/preview).

OR

[Cosmetics Inc. - Data for Pivot Table and VLOOKUPXLSX File](https://d3c33hcgiwev3.cloudfront.net/mjJpNpPfRiC7blak2QdsSA_f5269cdfb2da42ddb06577759b173be1_Cosmetics-Inc.---Data-for-Pivot-Table-and-VLOOKUP.xlsx?Expires=1716854400&Signature=AgRBxID3fUCpxVto54S4TaeLZLoLhatugKGvnq59V805DOSFpBqdzMKK~BRx5Yne~Jo8LyPqX6YjBRkEh070Ue9DLdZ9JEDeK819c8l7PDXuSeZV4dfxQGgEVu-19FK3rK77Wbqd-aBxrL8zbeKa2QXbVOe6Apw5UHzAEaSxj58_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3UWxlyqNRxaFsZcqjZcWgQ_3fd91ae61ce04caaa755c3477a337947_line-y.png?expiry=1716854400000&hmac=yjCSowGMfy4MFIfUa2He6nVGJ4klUlOx0-hTmys7Dkk)

## Example 1: Pivot tables

A pivot table is a data summarization tool. It can be used in data processing and in data cleaning, for which pivot tables offer a quick, clutter-free view of your data. Pivot tables help sort, reorganize, group, count, total, or average data in a dataset.

1. In the Cosmetics Inc. **spreadsheet, select the data you'll include. In this case, select all of the data in Sheet 1 of the spreadsheet by selecting cell **A1** then dragging your cursor to cell **F31**.
2. Select **Insert**, then **Pivot Table**. Choose **New sheet** and **Create**. Google Sheets creates a new sheet where you can define the pivot table.
3. Use the **Pivot table editor** to add specific data to your pivot table.

a. In the **Pivot table editor** panel, next to **Rows**, select **Add**.

b. From the columns list, select **Total**.

c. Below **Rows**, from the **Order** dropdown list, select **Descending** to put the most profitable items at the top.

d. Next to **Rows**, select **Add**.

e. From the column list, select **Products**.

f. Notice that the top two most ordered products are **15143Exfo** and **32729Masc**. The rest of the orders total less than $10,000.

## Example 2: **VLOOKUP**

**VLOOKUP** is a spreadsheet function that vertically searches for a certain value in a column to return a corresponding piece of information. It's rare for all of the data an analyst will need to be in the same place. Usually, you'll have to search across multiple sheets or even different databases. **VLOOKUP** helps bring the information together.

In the previous example, you found the product codes of the most ordered products. Now, you’ll use **VLOOKUP** to find the names of these products.

1. Select the Sheet 1 tab to navigate to Sheet 1 of the spreadsheet.
2. Select cell **H2**.
3. Enter **=VLOOKUP(A2, 'Sheet 2'!A1:B31, 2, false)**
    1. **Note:** This references information in another sheet. Make sure you have Sheet 2 in your workbook.
    2. This formula will take the value in cell **A2** of **Sheet 1** and check for that value in **Sheet 2** among the cells from **A1:B31** in the 2nd column (which corresponds with the 2 in the formula). Because the formula includes “**false**,” it will search only for an exact match. It will then output the value of column **B** in Sheet 2 as the result.
4. Press **Enter** to input the formula. The result is LashX Mascara.
5. Next, **select the cell** and **drag** the fill handle in the lower-right corner down to populate the other cells in the sheet with the formula.
6. To find the names of the two most profitable products you identified in the previous example use the find and replace tool.
    1. Select **Edit > Find and Replace**.
    2. In the **Find** text box, enter the product code for the most profitable product, **15143Exfo**.
    3. Select **This sheet** from the dropdown list next to **Search**.
    4. Select **Find** to find any cells in this sheet that contain this product code.
    5. Notice that cell **A31** is a match. This means the VLOOKUP search you ran in Column **H31** contains the name of the most profitable product: **SoSoft Exfoliator**.
    6. Repeat steps a-d with the product code **32729Masc** to find the product name of the second most profitable product. Cell **A27** contains **32729Masc**, so the product name is **Darkest Lashes Mascara**.

## Example 3: Plotting

The plotting tool allows analysts to quickly create a graph, chart, table, or other visual from data. Plotting is useful for identifying skewed data or outliers.

1. In **Sheet 1** of the *Cosmetics, Inc.* spreadsheet, **select column B**, which contains the prices.
2. **Select Insert > Chart**.
    1. If the chart created is not a column chart, select **Column chart** from the dropdown menu under **Chart type** in the **Chart editor**.
    2. Select and drag the chart to the right so you can view the data in the sheet.
3. Check for obvious outliers and fix them in the spreadsheet. For example, you might notice that an item in the middle of the chart has an extremely low price of $0.73. The decimal point is in the wrong place. In cell **B14**, correct this price to $7.30, and notice that Google Sheets automatically updates the chart.

---

# Different data perspectives

- **Data integrity is crucial for accurate insights and efficient data cleaning.**
- **Different data analytics projects require different approaches to data cleaning.**
- **Data analysts use various methods to look at data differently, including:**
    - **Sorting and filtering:** Arranging data in a meaningful order to find specific information or identify duplicates.
    - **Pivot tables:** Summarizing and reorganizing data for a quick, clutter-free view.
    - **VLOOKUP:** Searching for a specific value in a column to return corresponding information from another location.
    - **Plotting:** Visualizing data in charts or graphs to identify skewed data or outliers.

**Definitions:**

- **Data integrity:** Ensuring data is accurate, complete, consistent, and reliable.
- **Data cleaning:** Identifying and correcting errors, inconsistencies, and missing values in data.
- **Sorting:** Arranging data in a specific order (e.g., alphabetical, numerical).
- **Filtering:** Showing only data that meets specific criteria while hiding the rest.
- **Pivot table:** A data summarization tool that sorts, reorganizes, groups, counts, totals, or averages data.
- **VLOOKUP:** A function that searches for a specific value in a column and returns corresponding information from another location.
- **Plotting:** Representing data visually in charts or graphs.

---