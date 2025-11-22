# Get started with data calculations

---

# Common calculation formulas

[index (26).mp4](Get%20started%20with%20data%20calculations%206df15f33478a431381a2047690cd4468/index_(26).mp4)

**Key Points:**

- **Data analysis involves performing calculations on large datasets.**
- **Formulas in spreadsheets are powerful tools for data analysis.**
- **This video demonstrates how to use formulas to calculate annual sales, growth rate, average sales, minimum and maximum values.**
- **Conditional formatting can be used to visualize data and identify trends.**

**Definitions:**

- **Formula:** A set of instructions that tells a spreadsheet program how to perform a calculation.
- **Function:** A pre-built formula that performs a specific calculation.
- **Cell reference:** The address of a cell in a spreadsheet.
- **Fill handle:** A small box in the corner of a cell that can be used to copy formulas or patterns across multiple cells.
- **Conditional formatting:** A spreadsheet tool that changes how cells appear when values meet specific conditions.

**Step-by-Step Guide:**

1. **Calculate annual sales:** Use the SUM function to add up the sales for each year.
2. **Calculate growth rate:** Subtract the annual sales from the previous year from the current year's sales and divide by the previous year's sales.
3. **Calculate average sales:** Use the AVERAGE function to calculate the average sales for each month.
4. **Apply conditional formatting:** Use a color scale to highlight the highest and lowest average sales.
5. **Calculate minimum and maximum values:** Use the MIN and MAX functions to find the minimum and maximum average sales.

**Additional Notes:**

- The video uses Google Sheets, but the same steps can be applied to Excel.
- The video provides a good overview of basic data analysis techniques.
- More advanced data analysis techniques will be covered in later videos.

**Real-Life Examples:**

- A retail store could use these techniques to analyze sales data and identify trends.
- A financial analyst could use these techniques to analyze stock market data.
- A data scientist could use these techniques to analyze large datasets of any kind.

---

# Functions and conditions

[index (27).mp4](Get%20started%20with%20data%20calculations%206df15f33478a431381a2047690cd4468/index_(27).mp4)

**Key Points:**

- **Counting and Adding:** Data analysts frequently use counting and adding functions to analyze large datasets.
- **COUNTIF Function:** This function counts the number of cells that meet a specific criteria.
- **SUMIF Function:** This function adds numeric data based on a specific criteria.
- **Creating a Summary Table:** This table summarizes statistical information about data, making it easier to understand.
- **Analyzing Transactions:** The video uses the COUNTIF and SUMIF functions to analyze transactions based on the number of items purchased.
- **Calculating Average Revenue:** The video demonstrates how to calculate the average revenue per transaction for different categories.

**Definitions:**

- **COUNTIF:** A function that counts the number of cells that meet a specific criteria.
- **SUMIF:** A function that adds numeric data based on a specific criteria.
- **Summary Table:** A table that summarizes statistical information about data.
- **Criteria:** A condition that must be met for a cell to be counted or added.
- **Range:** A group of cells that are evaluated by a function.
- **Average Revenue:** The total revenue divided by the number of transactions.

**Key Steps:**

1. **Identify the questions you need to answer.**
2. **Create a summary table with the relevant attributes.**
3. **Use COUNTIF to count the number of cells that meet a specific criteria.**
4. **Use SUMIF to add numeric data based on a specific criteria.**
5. **Calculate the average revenue per transaction.**

**Real-Life Example:**

Imagine you work for an online kitchen supplies retailer. Your stakeholders want to know more about customer transactions, including the revenue they're bringing in. You can use the COUNTIF and SUMIF functions to analyze the data and create a summary table that shows the number of transactions with one item, the number of transactions with more than one item, the total revenue for each category, and the average revenue per transaction. This information can help your stakeholders make informed decisions about pricing, promotions, and other business strategies.

---

# Functions with multiple conditions

As you’ve been learning, conditional functions and formulas perform calculations according to specific conditions. In addition, functions including **SUMIF** and **COUNTIF** only work in cases where there is one condition. However, if you have more than one condition, you would need to use the **SUMIFS** or the **COUNTIFS** function instead. These functions enable you to perform calculations if you have two or more conditions. In this reading, you will learn more about conditional functions and how to construct functions with multiple conditions by exploring their basic syntax and checking out an example. You will also be able to access resources for similar functions in Excel.

## SUMIF to SUMIFS

Previously, you learned that the **SUMIF** function adds values in a particular range based on a single condition. The basic syntax is **=SUMIF(range, criterion, sum_range)**.

The first range is where the function will search for the condition that you have set. The criterion is the condition you are applying and the sum_range is the range of cells that will be included in the calculation. For example, in an accounting spreadsheet, you could use **SUMIF** to calculate the total expenses for a specific category, like Travel expenses, within a given month.

Or, you could find the total sales for automotive fuel treatment products– in this table, the ProductA is high octane fuel and ProductB is standard octane. Table 1 includes columns for Product, Region, Quarter, and Sales.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/aYBo3GwtQlqQ_nD-BYv_wQ_7136d536c2654707a21cd5b3afc60ae1_C5M4L1_R09_Functions-with-multiple-conditions.png?expiry=1716940800000&hmac=SXbgiDpCHCptltX9HIMVh03cfqxPYsZzT8Cpdzn0zoA)

You could use **SUMIF** to calculate the total sales for Product A using a formula like this:

**=SUMIF(A2:A8, "ProductA", D2:D8)**

But, you could also build in multiple conditions by using the **SUMIFS** function. **SUMIF** and **SUMIFS** are very similar: They add up values in a range. But SUMIFS can include multiple conditions. This gives you more control over your summing criteria, which, in turn, allows  you to perform more complex data analysis easily.

The basic syntax is: **=SUMIFS(sum_range, criteria_range1, criterion1, [criteria_range2, criterion2, ...])**

The square brackets let you know that this is optional. The ellipsis at the end of the statement enables as many repetitions of these parameters as needed. For example, if you wanted to calculate the sum of sales for ProductA in the East district in the first quarter, you could create a **SUMIFS** statement with multiple conditions, like this:

**=SUMIFS(D2:D8, A2:A8, "ProductA", B2:B8, "East", C2:C8, "Q1")**

In this example, B2:B8 is the second criterion_range and East is the second condition. The third criterion_range is C2:C8 and the third condition is Q1. As long as you follow the basic syntax, you can add up to 127 conditions to a **SUMIFS** statement!

## **COUNTIF** to **COUNTIFS**

Just like the **SUMIFS** function, **COUNTIFS** allows you to create a **COUNTIF** function with multiple conditions. The definition for **COUNTIF** is a function that counts the number of cells in a range that meet a single condition. For example, using **COUNTIF** to track the number of days an temporary employee was absent in an attendance record.

The basic syntax is: **=COUNTIF(range, criterion)**

Just like **SUMIF**, you set the range and then the condition that needs to be met. For example, in Table 1, if you wanted to count the number of transactions for ProductA, you could use a **COUNTIF** function like this:

**=COUNTIF(A2:A8, "ProductA")**

**COUNTIFS** has the same basic syntax as **SUMIFS**: **=COUNTIFS(criteria_range1, criterion1, [criteria_range2, criterion2, ...])**

The criteria_range and criterion are in the same order, and you can add more conditions to the end of the function. So, if you wanted to find the number of sales transactions for ProductA in the East region in the first quarter, you could use **COUNTIFS** to apply those conditions, like this:

**=COUNTIFS(A2:A8, "ProductA", B2:B8, "East", C2:C8, "Q2")**

This enables you to find every instance where both of conditions (East and Q1) are true.

## For more information

**SUMIFS** and **COUNTIFS** are just two examples of functions with multiple conditions. They help demonstrate how multiple conditions can be built into the basic syntax of a function. There are other functions with multiple conditions that you can use in your data analysis and many resources available online to help you get started:

- [**How to use the Excel IFS function**](https://exceljet.net/excel-functions/excel-ifs-function): This includes an explanation and example of the **IFS** function in Excel. It’s a great reference if you’re interested in learning more about **IFS**. The example is a useful way to understand this function and how it can be used.
- [**VLOOKUP in Excel with multiple criteria**](https://exceljet.net/formula/vlookup-with-multiple-criteria): Similar to the previous resource, this resource goes into more detail about how to use **VLOOKUP** with multiple criteria. Being able to apply **VLOOKUP** with multiple criteria will be a useful skill, so check out this resource for more guidance on how you can start using it on your own spreadsheet data.
- [**INDEX and MATCH in Excel with multiple criteria**](https:): This resource explains how to use the **INDEX** and **MATCH** functions with multiple criteria. It also includes an example, which demonstrates how these functions work with multiple criteria and actual data.
- [**Using IF with AND, OR, and NOT functions in Excel**](https://support.microsoft.com/en-us/office/using-if-with-and-or-and-not-functions-d895f58c-b36c-419e-b1f2-5c193a236d97): This resource combines IF with AND, OR, and NOT functions to create more complex functions. By combining these functions, you can perform your tasks more efficiently and cover more criteria at once.

---

# Hands-On Activity: Work with conditions

## Activity Overview

In previous activities, you used basic spreadsheet functions such as **COUNT**, **SUM**, **AVERAGE**, and **MAX**. In this activity, you will work with the conditional versions of these functions: **COUNTIF**, **SUMIF**, **AVERAGEIF**, and **MAXIFS**.

Conditional functions are functions that perform a specific task, but only on cells that satisfy some defined criteria. They are usually identified with an **IF** suffix adjoined to the desired operation. They are frequently used when constructing more complex queries that cannot be accomplished using more basic functions.

By the time you complete this activity, you will be able to use conditional functions and understand when and why they are appropriate. This will enable you to do more complex analysis with spreadsheets as you continue to develop your data analyst skill set.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the question at the end of the activity before going to the next course item.

# **Step 1: Access the template**

To get started, you will need to access the Working with Conditions spreadsheet.

Click the link to the spreadsheet to create a copy. If you don’t have a Google account, you may download the spreadsheet directly from the attachments below. Make sure to select “Use Template” on the downloadable item.

Link to spreadsheet: [Working with Conditions](https://docs.google.com/spreadsheets/d/1sKNqBzV63Na76jjoKLukjTtDyDMwVW0Vjz4mM-sJDEM/template/preview#gid=895883562)

OR

[Working with ConditionsXLSX File](https://d3c33hcgiwev3.cloudfront.net/qLRKJmPJTR6yRiMQRNIcfg_918c1ebc887045bba3c61fcdfdc080e1_Working-with-Conditions.xlsx?Expires=1716940800&Signature=jdUVYWIVz-VfQuxbqI4hRAHmKu345np92-7BttWS7ZLNU8E3GOyx2MSBXrCz1qDd3lHmsNGdHQ6n8who6K4~Zca3smrUNVIMnxIO95YogiukMVJn4-jyX3a17yEeopZw-zvbKJ3Z6MHTAoW2IOUrLZJ2ME~3K9IvRh62BD50pNs_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

# **Step 2: Use the COUNTIF function**

First, open the Working with Conditions spreadsheet.

In this scenario, your stakeholders have asked you to calculate the number of salespeople that the company has in New York state. The **COUNTIF** function allows you to do this easily. **COUNTIF** counts and returns the number of records in a table that meet a certain criteria—in this case, the number of salespeople a company has in the state of New York. The syntax is **=COUNTIF(**range, criteria).

The range is the array (or collection) of cells that you are checking and the criteria is what you are checking for. All cells in the array that match the provided criteria will be counted and this number returned as the value of the function.

To use this function to count the number of salespeople working from “NY,” click on an open cell. In the function bar, enter **=COUNTIF(B2:B21, "NY").**

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fN32pf_DQ0mYUTIPr1KE6g_e7ae4383c0c14a7ab6abdc7072668de1_mqOtHMh7Ui-mmA9vSsQc4rXSTYWubS94aHgkUzqC5gF3eU1JrRhwYwI2bzF3KWJocIu4XONyxRJjSH_fPLdcMbqABPms9RLquGFSZFvJUoZ98RObXC4m6ugXFqhmEXNvmB_wlBkIkOzQDMINwyp5SplvGFsVKjZnBQ8sPY-3x88_SSpGU-n38VhbepT_XXHuTVFI9BQym-nWRykR431yUbE482h7jC8YMfgwsQ?expiry=1716940800000&hmac=fbdlKBSftkpYljtV426Mh83jTz04X4lQP65mK4izT-E)

The range is the array of cells from B2 to B21. This is all from column B with the exception of the column header. The function checks all cells in this array against the value “NY” (entered in quotes) which is the criteria. Every cell in this array with a value of “NY” will be counted, and the result is returned in the cell. It is 6 in this case.

Press **Enter/Return**. The result should display like this:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LL_An_fwS1eNfTpuOIcdPw_5edf000f764c4575af43d316f55057e1_bP8mZkdMQzs85SbXDpQQ88UWDDQ1zkHeEJgyCYnqC_dRV_NFbqhwOTMNPg20r62ec487cE4P10l3fUbI7O4xsJsO94_cbCJPA-ejS1UoB8TtkFzmHdwzKgXzmWKPQ-z0U_t6Z9ub3iPmXe9XsEvKWZvhrU0q27Fx4daj6hpmDou1j107hpOraMkV8NGS7zur-LhZE35uerQrj5gJFkeY4HYQvvjufFNmaSIuHw?expiry=1716940800000&hmac=KEvU_jfwbH0KE7SPd1drdkW91JiBx9n-IXgfkghCD9c)

You can achieve the same result by entering a cell address as the criteria. For example, the cell J10 has the value "NY." If you enter this in the function bar the **COUNTIF** function will seek out the value in cell J10 and use it as the criteria. This gives the same result as before:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sGnb6Vp4TgKr3oJZAErlkA_1a8dadb89c6a470dbce5533e8de0f2e1_PG1j0Alq2ruetbl3grXUGInIw7dpb4ZEhBWGWjG7HRrQybyUnQofvSAKLVWsja488KNI-J0TicnCShoIeoKgb-JLAbcMUxHyWqjZtEd9sjCb8V2mXEERffarnS-iRWkrni_o0zPSGZ0n0LXANAGh3LJqu4J_t7EQpxxWj6w1mtBcjwpnh-9z38oBd2ZSaLsptoKyndXUfmXuZKdIVgYRMcW7A1sLH_ttA4K5hg?expiry=1716940800000&hmac=4XEwO5O8jMYVeJXgPMyj-qFa_QP4vawrTKzAbiLUQnY)

Other examples of using **COUNTIF** include a hotel manager checking on how many rooms are currently occupied for staffing and inventory, or it could be used in a factory to count the number of defective items in a batch.

## 

# **Step 3: Use the SUMIF function**

The **SUMIF** function is used to create a sum of the values of cells that meet a specific criteria. **SUMIF** supports the logical operators (>, <, <>, =). The syntax for this function is **=SUMIF(range, criteria, [sum_range] )**.

The range, also called the input range, is the array of cells that you check against the value of criteria. The **sum_range** is the array of values that you will sum up if the criteria is met. In this syntax above, the square brackets around **sum_range** indicate that this input is optional. However, you do not add square brackets when writing the function. If the argument **sum_range** is absent, then the **SUMIF** will sum the values in range by default.

As an example of this function, suppose that you want to create a sum of all sales more than $500.00. This can be executed as **=SUMIF(D2:D21, ">500")**.

The result is 19007.61:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/r_-ql46ZRbe4iEb5LOp-gQ_3ed728c2ec1446d9b1349c8565d919e1_kG8P-KYFdm5Tsc8EKLwOGNS_56hwcHHJsVhSyL7eoesXy5YiC4wWvAKCJdPsQec6pqJP2F4Ui1licCFNV9P6DYq_-WPy0vBhnSncsrsuqFDotv_KNNT5O5wwCJO3N28J6r4aDRP1Vc651YSCiTQ-k9W_bZTch11efD-ARRM4pDMsgzTvMcJzpWHpCIupDfQw5HEndLJB1vqDpZCeUJZOvxV7FpBWmIFxsvQJYQ?expiry=1716940800000&hmac=Q1rJiZPNFFVJRfzLAI-W0ChGkmOTIiO2g00o_MHtd34)

Because you didn't include the **sum_range** input, all the values in the cells D2 to D21 that match the criteria were summed by default. To sum only the sales from New York, but not restrict to those greater than $500, enter the following function: **=SUMIF(B2:B21, "NY", D2:D21)**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/y1Vvbq4-SJqjXgx8QaKAtw_d83181cc66e5476ab7e9164946bad4e1_A7n8drW7sht7KFBcl7y2LJFUXnNTg6QWbtOjpwQZ44DayI4dVIgoOmNbsZhGvFaAUaWsLfJM2VKAPO9BmgHOE8Hz2_N3CudarV5HNuy0mOYG5tm6OrRbKjyWkt9J6yUSO5ym_9xm-YjJRTBuw8svWUkSTC2xZUQMCWgGX28NVPfKCfXQrggkweVaupjaRucbzTfz3_TD6W7W-reVrE2e17XCAwLY1f9dBVy2NA?expiry=1716940800000&hmac=_vyqrmfQRpA8872mvnm3jYGqRrM0CfSGWvjdO4Y3r1w)

This results in 5417.3:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qe3EYZLRRQe8nC0QOKS70g_2bba1c36548743268cf3fa635d2d82e1_ga4N-6GhKgHdGk-zsRpNSSH9HcQjKz4DuMP-5mOzKf6t3cbrH_I1Qmq7nn04f_nsENc47Rlu3kgoZC_4t4WyJOaMnoi593_uaho4kuuWn6lKitp39Lb_rogrz7W2LNse5BCOsyXlkPPYyCxq4QyEKXIiTdIE0Un_1s8R_tLpSv_OCNNikatztNLBbkGQO6YUX2ic8xTGWcKBcQt1uIzzNg6FxlTJmIa-pKbgDg?expiry=1716940800000&hmac=79uP5PoJK85SCWEyS6FB58fZ3KzWq9k9oUPXot1den8)

The first input, B2:B21, is the range of cells that are checked for the criteria "NY" and the summing is done across the **sum_range** of cells D2:D21 that have the state meeting the criteria "NY." This is different than in the first case. In that case, the array that you check is the same array that you sum across.

Other examples of using **SUMIF** include tracking the total value of a specific product to better manage inventory. A medical accountant might use **SUMIF** to total the expenses related to a particular department or piece of equipment, such as an MRI machine.

## 

# **Step 4: Use the AVERAGEIF function**

Just like the previous two functions, the **AVERAGEIF** function will average the values in an array based on a specific criteria. The syntax is **=AVERAGEIF(range, criteria, [sum_range])**.

The inputs to this function—**range**, **criteria**, and **sum_range**—work in exactly the same manner as in the **SUMIF** function. Again, the **sum_range** is optional.

You know from your previous queries that there are six salespeople in New York. To find the average sales per for these salespeople, enter the following function: **=AVERAGEIF(B2:B21, "NY", D2:D21)**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dcLPWj9yQEK10sbLaADsVQ_1a79e899db3548fabb6deff608d9e8e1_x8Xq3bGYZT8HeH1G7E6BL1BuGN1Cl5k3He-HXqODo2n1pYyTJ9PHzEia0Mz3Q14lXBqlpnNvsNMS1wqYSsxh6XitwI3yda_cZXu-bu-QCOQ3RUbcZMTCDJePuzwDVtqlgbXazXC2hF6ttPugBWtsXZ82TqzIT3JvEqL9gfKYjcd-34NxrapHl3_bHQQAO4ADWqIE3mjQE_Vg0Vol0XOBnwFnvCO3JvpHwaICLw?expiry=1716940800000&hmac=crFI_CS9mQ-r-Unwq5VDty8whjYc7xQN2mi3-KZQxiQ)

The result is 902.83333, which means that the average salesperson for this company in New York state sells $902.83 worth of merchandise.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Tz1bxnhEQe2asOJpX99TTw_dd6390fd805447c49bcc29e0eba788e1_lG30JuJsRpQI8k2MCd6c1OafcfiWobpVmCrdrbhHWUwCaDZxKt-pAUdP9cN9_EktlwWDACIwjVaea2QeF4P9yUBIqoJGnDeXuFNwdSS1PRi_DaU9pvecpu7rRnLciEretlPtaHbL2nSLoW01zOkQIjn-Zx4HcCxtB_uf6MXGimtpwuz2WQmbs1AzhArEhVtQwCvTzz9lxWSlJy4j8jYrrQbhqxeng_znUWXcUA?expiry=1716940800000&hmac=8vd5c7Gwh0t0je6FtHGINFy4wqNGjELQ_vY1JsPIpGw)

Averaging data conditionally allows you to get more specific insights into your dataset. For example, you might want to know the average sales that are made on weekends to plan promotional events more effectively.

## 

# **Step 5: Use the MAXIFS function**

The **MAXIFS** function is slightly different from the other three functions—it returns the maximum value in a range based on one or more conditions. The easiest way to observe the difference is to examine the syntax: **=MAXIFS(max_range, range1, criteria1, [range2], [criteria2], ...)**.

**Note for Microsoft Excel: MAXIFS** can only be used with an Office 365 subscription on Excel 2016 or newer. If you cannot use a version of Excel that allows the function **MAXIFS**, use Google Sheets for this part of the activity.

The first argument, **max_range**, is the array for which you want to find the maximum value. The second argument **(range1)** is the array you are checking. The third argument **(criteria1)** is the value that you are checking for. The inputs in the square brackets are for optional additional constraints.

To use **MAXIFS** to find the maximum sales from any salesperson in New York, enter the following: **=MAXIFS(D2:D21, B2:B21, "NY")**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9MMVqvMYRaqWpAgrpNqdKg_62174db85be24ea2a981a640b243b6e1_3QZFxCPdSmjgMItW9zmfvVD7F3SD7QtH39eYhNEq6mUHaQGVvgd1hSg7rqmd0ZcFpleXbejoTJEvu3HWfczGeIgYr5iHYF9d2OIexAVoN0l3Z8-j0tXvpdFVdSrwzL9_FLW4xezlTqXouLisHn6Rz5ji0A8pTttSEKAczX_ECDT6IXZScvFj3XaxlDrMPaxu9q7kVuzlDTYMeUafgXSt5qDnESKcE_3GQKc-9w?expiry=1716940800000&hmac=U6fS5ryogmU390zNeyCvxFdyUyy7R16VBB-I9I7za8A)

The resulting calculation is 1666.61. It’s important to keep in mind that the order in which you enter the inputs matters. If you reverse the position of the arrays and enter **=MAXIFS(B2:B21, D2:D21, "NY")** the result is 0.

This is because you are now asking the function to find the maximum of the array B2:B21 where the sales equal "NY". This is impossible because the values in the array D2:D21 (the sales array) are numerical—none of them equals "NY." The function returns 0 when nothing in the range meets the criteria.

The **MAXIFS** function can input more than one constraint. This is where the optional **range2** and **constraint2** come into play. For example, to find the maximum sales in New York where the Max Item Cost is below $400, enter the following into the function bar: **=MAXIFS(D2:D21, B2:B21, "NY", E2:E21, "<400")**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8ePeOW5HR1uZmdhAM7atUw_d01a14893c3c4752bf9189d6512174e1_12P9MllmTaKZQ9vFJeH4m1mc5v2u-EZ6KvpY9GThEvhkESWSkSQA-lIIJNN5Dycbwc7yM4uazPqg66T0_TDwoRVT_i3jJ1sxYnOSzRRQOH2C9dNxJ5YyVN-ui46s31Nnr6IxiMHeXWfAWAspdkkaXYgbJjZY0-kQpp6P0rs0nh5Cr5sUYSPGdD73-9X96oNgilFb1KwRhAJ0SWY0M1wDu5IA85c-tJiXS1dYLw?expiry=1716940800000&hmac=YY7n45fXra-X-THgU6xDqvx1nfdCXq7cgVDywTA53IA)

Additional constraints follow the logic that every constraint must be satisfied for a cell in the **max_range** to be considered.

The first three inputs are the same as above, but now you've added the additional constraint that Max Item Value must be less than $400. The array E2:E21 is the Max Item array and its cells are checked against the criteria <400. The function returns the following, which is the maximum sales of any New York salesperson who did not sell any single item over (or equal to) $400.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Tbbp63nZSTmboS1zGvEtHQ_b27da27713bf4da884683478c7f623e1_ADGAGXb7zAzIkZfIhswrbhht_d2SEWZiPfJCcknGl2TfVg3P7aAXHCt0-B-1pz8yw14i8EZGBq9IlbdKKDADnFydpQBJAn-bMtPFZ5hCZmdIxS3Tbv_3bzkrAMOtfVYB381ykqa51hxDO29XKCme6voCFR6YbFo1XMZNXm7pxe2J2VIV6kTVmVjdIGyf0-spn60ntZLRxQHbF1TytdHrOxFhBw6k_3rjiiQk8Q?expiry=1716940800000&hmac=0rtItzHO3LlgtEo6s9HS5fhyHJv1qQz0QdZN2G6HYQI)

# **Step 6: Compare the conditional functions**

Each of the previous functions—**COUNTIF**, **SUMIF**, and **AVERAGEIF**—have equivalents that work similarly to **MAXIFS**. These include **COUNTIFS**, **SUMIFS**, and **AVERAGEIFS**. The syntax and functionality of these functions, apart from the specific calculation, are identical to **MAXIFS**. For example, the **SUMIFS** function will give the sum for single and multiple constraints just like **MAXIFS** function does for the maximum. It also has the same syntax as **MAXIFS**.

---

# Composite Functions

[index (28).mp4](Get%20started%20with%20data%20calculations%206df15f33478a431381a2047690cd4468/index_(28).mp4)

**Key Points:**

- **What is SUMPRODUCT?**
    - A function that multiplies corresponding values in two or more arrays and returns the sum of those products.
    - Useful for simplifying complex calculations involving multiplication and addition.
- **Syntax:** `=SUMPRODUCT(array1, [array2], [...])`
    - Each array is separated by a comma.
    - Arrays can be ranges of cells or individual values.
- **Example:**
    - Calculating total revenue from an order:
        - Multiply quantity of each item by its unit price.
        - Sum the resulting products.
    - Calculating profit margin:
        - Multiply revenue by profit margin percentage.
        - Sum the resulting products.
- **Benefits of using SUMPRODUCT:**
    - Saves time and effort compared to manual calculations.
    - Reduces the risk of errors.
    - Makes formulas easier to read and understand.

**Definitions:**

- **Array:** A collection of values in cells.
- **Revenue:** The total amount of money earned from sales.
- **Profit margin:** The percentage of profit earned on each dollar of sale.

---