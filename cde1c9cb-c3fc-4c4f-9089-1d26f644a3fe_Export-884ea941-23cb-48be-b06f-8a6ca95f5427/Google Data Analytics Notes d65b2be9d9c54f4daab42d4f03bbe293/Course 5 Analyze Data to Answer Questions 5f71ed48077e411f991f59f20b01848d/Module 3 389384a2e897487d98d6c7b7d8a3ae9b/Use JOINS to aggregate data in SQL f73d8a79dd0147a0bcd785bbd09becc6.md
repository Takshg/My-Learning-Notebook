# Use JOINS to aggregate data in SQL

---

# Upload the employee dataset to BigQuery

This reading outlines the steps you need to perform before watching the video and following along in the step-by-step guide, [Explore how JOINs work](https://www.coursera.org/learn/analyze-data/lecture/uLZJH/how-joins-work).

**What you will need**

Download the two .csv files from the attachments below:

[Employees Table - Understanding JOINSCSV File](https://d3c33hcgiwev3.cloudfront.net/TMwinKTQQ2aYTZGdcL0Fog_84586bd2265a4888af22e8060747c8e1_Employees-Table---Understanding-JOINS.csv?Expires=1716940800&Signature=LR0eLelKeo5Oo6WP2c5a~2zLpXMWcbqjC4dOUCJHLs3LeWlZR~C0lTCEhQinezbhGAj1qmeecWR3787vz0fsandZOI8lJY~lpi1YW3IQXpwQFoMojcH4EdZbi9UoQDkqUVNOTrKHgiIAOFDoKyHIp9lAVHeWuwVmvcNe9Bus-9Q_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Departments Table - Understanding JOINSCSV File](https://d3c33hcgiwev3.cloudfront.net/9vVSOuERRjusAUScVM-rOw_d98f88a17db84f198dee412210c13ae1_Departments-Table---Understanding-JOINS.csv?Expires=1716940800&Signature=GX8eFex9uvB0wyAThvtlHb4JB40RYB4yeHKyy7286~HzrW8xVI13KC549qjIaIYArqGJrQliij0femFdnApuK6UCfwp4KcfOVtU5-pvsetP-gwVz35ASr~Df2ZISHj6whx44VY5zGGHIQGIIts4ob0Vj7Mi5gCIrSej8sqKI9Ok_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

Then, log in to your BigQuery account and follow along with this reading to upload the employee data provided as two new tables.

## Prepare for the next video

### **Create a new dataset**

1. Open your BigQuery console and select the project to which you’ll upload data. For the purpose of this reading, the example project is named **dac5bigquery**. Your project will have a different name.

2. From the **Explorer** pane, select the **Actions** icon (the three vertical dots) next to your project name. Then select **Create dataset**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NR_QFZ3BQhqcygpaDyEh9g_9f5351d966d64325a818c3a407b8cee1_DAC5M3L1_R1_Image1-Create-new-dataset.png?expiry=1716940800000&hmac=GPstC3TWRwWO9W9qmAXC5V4bpmZMrOdmpVPqsP89HrI)

3. In the **Create dataset** window, enter **employee_data** for the **Dataset ID**.

4. Make sure the **Location type** is set to **Multi-region** with **US(multiple regions in the United States)** selected.

5. Leave the **Advanced options** set to their default settings.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/gcm5KisNRJ6_y3WoFp1p-w_50d5329b61d14bf9a6d1ba3447cd7fe1_DAC5M3L1_R1_Image2-Create-new-dataset-details.png?expiry=1716940800000&hmac=N0igNZEn0EgRwVhhD4QeRyZcPFj3kiiPRlnlWJm8wdU)

6. Select **CREATE DATASET** to add the dataset to your project. It will now appear under your project in the **Explorer** pane. If you don’t see the new dataset listed, select the arrow next to your project in the **Explorer** pane to expand its contents.

7. In the **Explorer** pane, select the **employee_data** dataset you just created. The **Dataset info** window opens in the **Details** pane.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VkfDh92vROORr820wecgTQ_4ff9a132ab7e445e80fa36c7104350e1_DAC5M3L1_R1_Image3-Dataset-info.png?expiry=1716940800000&hmac=nN4f_QgTU6vOruvmiKY9cyVlkvWzasVCArLGEPWbkeE)

### **Create the employees table**

Create a table for the employees within your employee_data dataset. To do this:

1. Select **+ CREATE TABLE** from the options in the **Details** pane. Under **Source**:

- From the dropdown in the field **Create table from**, select **Upload**.
- From the **Select file** field, select **BROWSE**. Then, find and select the [Employees Table - Understanding JOINS](https://d3c33hcgiwev3.cloudfront.net/TMwinKTQQ2aYTZGdcL0Fog_84586bd2265a4888af22e8060747c8e1_Employees-Table---Understanding-JOINS.csv?Expires=1700006400&Signature=XeqsCQhRu8D7cS7Ew8kaS3ySfbc2aYOuk~bTZZ8eBdF07KQtiMu4sAgRB4V1xboPLvCry4H61bXFNjqBT1PmbKFo8dgzPbmOUsS0msC6Fca6c-gj95HVM1PJq5pRctkQiC8OaBKml3T9KRs0lctwoqeJI-HKUo5e7hs2dF-q~EA_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A).csv File you downloaded previously.
- The file format should be automatically detected after selecting the Employee Table .csv file. If it’s not, select **CSV** from the **File format** drop-down.

2. Under Destination:

- Enter **employees** in the **Table** field.
- **Project**, **Dataset**, and **Table type** will be automatically filled. You do not need to update these fields.

3. Under **Schema**, select the **Auto detect** checkbox.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HoSUNGOYRDyFC3XZlkCN6A_73f1a090cbcc4a90ab2cc2693a8bf1e1_DAC5M3L1_R1_Image4-Create-new-table-employees.png?expiry=1716940800000&hmac=5EAXvyDk6mlE8Qqip9aAv_PjfD3U-ULRJgINfk993Pk)

4. Select **CREATE TABLE**. The employees table will be nested under **employee_data** in the **Explorer** pane.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/t7OrRLVgSgaY0huRvtqXmQ_b26cbce0b8f7494094cd44c6072effe1_DAC5M3L1_R1_Image5-Explorer-with-employee-table.png?expiry=1716940800000&hmac=MkFCivQdJ6AWFW1iTEzzkl_B4WW0Goofpo01w07bpc8)

### **Create a departments table**

Next, create a table for the departments within the employee_data dataset. To do this:

1. Select the **employee_data** dataset from the **Explorer** panel.

2. Select **+ CREATE TABLE** from the options located in the main editor window.

3. Under **Source**:

- From the dropdown in the field **Create table from**, select **Upload** from the list of options.
- From the **Select file** field, select **BROWSE**. Find and select the [Departments Table - Understanding JOINS](https://d3c33hcgiwev3.cloudfront.net/9vVSOuERRjusAUScVM-rOw_d98f88a17db84f198dee412210c13ae1_Departments-Table---Understanding-JOINS.csv?Expires=1700006400&Signature=BTJ2YLesayzmJfmfNXNbbpPk1iw5Gtn-S5VuVwvjSBrHHVcx43MzcGPWP6skOxWPQZATx2JVKw2x0aR9HKbxe80VLIK9enqXKETlIOcPYpxjDw52KFdA-Ugi4gpqegDFSl8E1bqumIk-tPxDwRe9SKnBDAeTxXGgroVc~ssKB88_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A).csv File you downloaded previously.

4. The file format may be automatically detected after selecting the Departments Table .csv file. If it’s not, select **CSV** from the **File format** drop-down.

5. Under the **Destination** section:

- Enter **departments** in the **Table** field.
- **Project**, **Dataset**, and **Table type** will be automatically filled out so you do not need to update these fields.

6. Under **Schema**, select the **Auto detect** checkbox.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/z6d408hLSxu1XDADpZrpag_151c9d401ee742c784a72fa1828657e1_DAC5M3L1_R1_Image6-Create-new-table-departments.png?expiry=1716940800000&hmac=S-qyffGR-ZPAhH8WkifBAAZg1k62NTZC_7FkK23859E)

7. Select **CREATE TABLE** in the **Create Table** window. The **departments** table will appear under the **employee_data** dataset listed within your project.

### **Verify the data**

Make sure that you’ve uploaded the tables correctly by previewing the tables you just created.

1. From the **Explorer** pane, select the **employees** table.

2. Select the **Preview** tab to verify that you have the following data:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cNscvo98SZyuEgoB5jU4Bg_d5c1c249cc1e400897c712c8bb2930e1_DAC5M3L1_R1_Image7-Preview-employees-table.png?expiry=1716940800000&hmac=hbE9G9uILKfIK4rkOSN7abCzFLkqQ7ENfWWsuu59gW0)

3. Select the **departments** table.

4. Select the **Preview** tab to verify that you have the following data:

There are six rows in the table. In Row 1: name: Dave Smith; department_id: 1; role: Product Marketing Manager. In Row 2: name: Scott Tanner; department_id: 1; role: Director of Demand Gen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WIpa8MEhTXWxIQtwpQCHgw_e23a296daaed4a998041a76859c431e1_DAC5M3L1_R1_Image8-Preview-departments-table.png?expiry=1716940800000&hmac=-NhW0gR0l7kmvFK_rXu2c0pOyH0uLpXMmMwCxZ7rtYw)

When your data previews match these instructions, you are ready to follow along with the step-by-step guide and video on [Explore how JOINs work](https://www.coursera.org/learn/analyze-data/lecture/uLZJH/how-joins-work).

---

# Step-by-Step: Explore how JOINs work

This reading provides you with the steps the instructor performs in the following video, [Explore how JOINs work](https://www.coursera.org/learn/analyze-data/lecture/uLZJH/how-joins-work). The video teaches you how to use **JOIN** in SQL to aggregate data in databases.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

In order to follow along with the instructor, you will need the employee dataset uploaded into your project space. If you haven’t already uploaded this data, follow the instructions in the [Upload the employee dataset to BigQuery](https://www.coursera.org/learn/analyze-data/supplement/13KQO/optional-upload-the-employee-dataset-to-bigquery) reading.

## Common **JOIN**s

This video explores exactly how **JOIN**s work. A **JOIN** is a SQL clause that is used to combine rows from two or more tables based on a related column. The instructor discusses the different types of **JOIN**s in more detail in the video; here’s a quick reference you can review as you follow along:

- **INNER JOIN:** a function that returns records with matching values in both tables
- **LEFT JOIN:** a function that returns all the records from the left table (first mentioned) and only the matching records from the right table (second mentioned)
- **RIGHT JOIN:** a function that returns all records from the right table (second mentioned) and only the matching records from the left table (first mentioned).
- **OUTER JOIN:** a function that combines the **RIGHT JOIN** and **LEFT JOIN** to return all matching records in both tables.

## Example 1: **INNER JOIN**

In the video, the instructor uses BigQuery to join the employees and departments tables. The following steps take you through typing the query into the query window. If you prefer, you can copy and paste the following query into the query window instead.

1. In BigQuery, select the **COMPOSE A NEW QUERY** button. BigQuery opens a query window where you can enter your query. The instructor has already executed some queries so their starting line number may be different from yours. If you’ve just opened BigQuery, your line number will be 1. It’s okay if your line numbers aren’t the same as what’s in the video.
2. In line 1 of the query window, enter **SELECT** and then press **Enter**.
3. Press Tab and then in line 2 enter **employees.name AS employee_name**, then press **Enter**.
4. In line 3, enter **employees.role AS employee_role**, then press **Enter**.
5. In line 4, enter **departments.name AS department_name**, then press **Enter**.
6. In line 5, press **Backspace** to stop indenting, enter **FROM**, then press **Enter**.
7. In line 6, press **Tab**, then enter **[your-project-name].employee_data.employees**, replacing **[your-project-name]** with the name of the BigQuery project to which you added the **employee_data** dataset.
8. Continuing in line 6, enter **AS employees**. Press **Enter**.
9. In line 7, press **Backspace** to stop indenting, enter **INNER JOIN**, then press **Enter**.
10. In line 8, press **Tab**, then enter **[your-project-name].employee_data.departments**, replacing **[your-project-name]** with the name of the BigQuery project to which you added the **employee_data** dataset.
11. Continuing in line 8, add **AS departments**. Press **Enter**.
12. In line 9, enter **ON** **employees.department_id = departments.department_id**.
13. Run the query by selecting the **Run** button.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled.png)

## Example 2: **LEFT JOIN**

Start a new query in BigQuery by opening a new query window. To open a new query window, select the **+** button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MR6Wz3ZVR4-ambdVuUvmEw_12208000529f4295b3a83631e0679ef1_Screenshot-2024-04-12-3.54.28-PM.png?expiry=1716940800000&hmac=hfAynNalQwrOzH4tZ_XbNerzfjPz84_psTrUYYssLig)

Now, you'll create a new query that uses **LEFT JOIN**.

1. Using the query window tabs to navigate between queries, copy and paste the query from Example 1 into the new query window.
2. In line 7, replace **INNER JOIN** with **LEFT JOIN**.
3. Run the query by selecting the **Run** button.

If you prefer, you can copy and paste the following query into the query window in BigQuery.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%201.png)

## Example 3: **RIGHT JOIN**

Now, you'll create a new query that uses **RIGHT JOIN**. Open a new query window.

1. Using the query window tabs to navigate between queries, copy and paste the query from Example 2 into the new query window.
2. In line 7, replace **LEFT JOIN** with **RIGHT JOIN**.
3. Run the query by selecting the **Run** button.

If you prefer, you can copy and paste the following query into the query window in BigQuery.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%202.png)

## Example 4: **FULL OUTER JOIN**

Now, you’ll create a new query that uses **FULL OUTER JOIN**.

1. Using the query window tabs to navigate between queries, copy and paste the query from Example 3 into the new query window.
2. In line 7, replace **RIGHT JOIN** with **FULL OUTER JOIN**.
3. Run the query by selecting the **Run** button.

If you prefer, you can copy and paste the following query into the query window in BigQuery.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%203.png)

---

# Explore how JOINs work

[index (23).mp4](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/index_(23).mp4)

---

# The importance of aliases

In this reading, you will learn about using aliasing to simplify your SQL queries. **Aliases** are used in SQL queries to create temporary names for a column or table. Aliases make referencing tables and columns in your SQL queries much simpler when you have table or column names that are too long or complex to make use of in queries. Imagine a table name like **special_projects_customer_negotiation_mileages**. That would be difficult to re-enter every time you use that table. With an alias, you can create a meaningful nickname that you can use for your analysis. In this case **special_projects_customer_negotiation_mileages** can be aliased to simply **mileage**. Instead of having to write out the long table name, you can use a meaningful nickname that you decide.

## Basic syntax for aliasing

**Aliasing** is the process of using aliases. In SQL queries, aliases are implemented by making use of the **AS** command. The basic syntax for the **AS** command can be seen in the following query for aliasing a table:

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%204.png)

Notice that **AS** is preceded by the table name and followed by the new nickname. It is a similar approach to aliasing a column:

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%205.png)

In both cases, you now have a new name that you can use to refer to the column or table that was aliased.

### **Alternate syntax for aliases**

If using **AS** results in an error when running a query because the SQL database you are working with doesn't support it, you can leave it out. In the previous examples, the alternate syntax for aliasing a table or column would be:

- **FROM table_name alias_name**
- **SELECT column_name alias_name**

The key takeaway is that queries can run with or without using **AS** for aliasing, but using **AS** has the benefit of making queries more readable. It helps to make aliases stand out more clearly.

## Aliasing in action

Let’s check out an example of a SQL query that uses aliasing. Let’s say that you are working with two tables: one of them has employee data and the other one has department data. The **FROM** statement to alias those tables could be:

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%206.png)

These aliases still let you know exactly what is in these tables, but now you don’t have to manually input those long table names. Aliases can be really helpful for long, complicated queries. It is easier to read and write your queries when you have aliases that tell you what is included within your tables.

## For more information

If you are interested in learning more about aliasing, here are some resources to help you get started:

- [**SQL Aliases](https://www.w3schools.com/sql/sql_alias.asp):** This tutorial on aliasing is a really useful resource to have when you start practicing writing queries and aliasing tables on your own. It also demonstrates how aliasing works with real tables.
- [**SQL Alias](https://www.sqltutorial.org/sql-alias/):** This detailed introduction to aliasing includes multiple examples. This is another great resource to reference if you need more examples.
- [**Using Column Aliasing](https://documentation.sas.com/?cdcId=pgmsascdc&cdcVersion=9.4_3.5&docsetId=sqlproc&docsetTarget=p0aymxwsvbt5wcn1lncugwjtf758.htm&locale=en):** This is a guide that focuses on column aliasing specifically. Generally, you will be aliasing entire tables, but if you find yourself needing to alias just a column, this is a great resource to have bookmarked.

---

# Use JOINS effectively

In this reading, you will review how **JOIN**s are used and will be introduced to some resources that you can use to learn more about them. A **JOIN** combines tables by using a primary or foreign key to align the information coming from both tables in the combination process. **JOIN**s use these keys to identify relationships and corresponding values across tables.

If you need a refresher on primary and foreign keys, refer to the [glossary](https://www.coursera.org/learn/analyze-data/supplement/0p8b6/glossary-terms-and-definitions) for this course, or go back to [Databases in data analytics](https://www.coursera.org/learn/data-preparation/supplement/uXqEX/databases-in-data-analytics).

## The general **JOIN** syntax

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%207.png)

As you can see from the syntax, the **JOIN** statement is part of the FROM clause of the query. **JOIN** in SQL indicates that you are going to combine data from two tables. **ON** in SQL identifies how the tables are to be matched for the correct information to be combined from both.

## Type of **JOIN**s

There are four general ways in which to conduct **JOIN**s in SQL queries: **INNER**, **LEFT**, **RIGHT**, and **FULL OUTER**.

The circles represent left and right tables, and where they are joined is highlighted in blue

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/V3K80lLeRfayvNJS3tX2DQ_c5371083976944c7808132ca392f419d_Screen-Shot-2021-02-07-at-5.14.41-PM.png?expiry=1716940800000&hmac=n5u1k11AHSUrQZyO7iotx1kFyqpK_wzex2JtVJDg2-M)

Here is what these different **JOIN** queries do.

### **INNER JOIN**

INNER is *optional* in this SQL query because it is the default as well as the most commonly used **JOIN** operation. You may see this as **JOIN** only. **INNER JOIN** returns records if the data lives in both tables. For example, if you use **INNER JOIN** for the **customers** and **orders** tables and match the data using the **customer_id** key, you would combine the data for each **customer_id** that exists in both tables. If a **customer_id** exists in the **customers** table but not the **orders** table, data for that **customer_id** isn’t joined or returned by the query.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%208.png)

The results from the query might look like the following, where customer_name is from the customers table and product_id and ship_date are from the orders table:

| **customer_name** | **product_id** | **ship_date** |
| --- | --- | --- |
| Martin's Ice Cream | 043998 | 2021-02-23 |
| Beachside Treats | 872012 | 2021-02-25 |
| Mona's Natural Flavors | 724956 | 2021-02-28 |
| ... etc. | ... etc. | ... etc. |

The data from both tables was joined together by matching the **customer_id** common to both tables. Notice that **customer_id** doesn’t show up in the query results. It is simply used to establish the relationship between the data in the two tables so the data can be joined and returned.

### **LEFT JOIN**

You may see this as **LEFT OUTER JOIN**, but most users prefer **LEFT JOIN**. Both are correct syntax. **LEFT JOIN** returns all the records from the left table and only the matching records from the right table. Use **LEFT JOIN** whenever you need the data from the entire first table and values from the second table, if they exist. For example, in the query below, **LEFT JOIN** will return **customer_name** with the corresponding **sales_rep**, if it is available. If there is a customer who did not interact with a sales representative, that customer would still show up in the query results but with a **NULL** value for **sales_rep**.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%209.png)

The results from the query might look like the following where **customer_name** is from the **customers** table and **sales_rep** is from the **sales** table. Again, the data from both tables was joined together by matching the **customer_id** common to both tables even though **customer_id** wasn't returned in the query results.

| **customer_name** | **sales_rep** |
| --- | --- |
| Martin's Ice Cream | Luis Reyes |
| Beachside Treats | NULL |
| Mona's Natural Flavors | Geri Hall |
| ...etc. | ...etc. |

### **RIGHT JOIN**

You may see this as **RIGHT OUTER JOIN** or **RIGHT JOIN**. **RIGHT JOIN** returns all records from the right table and the corresponding records from the left table. Practically speaking, **RIGHT JOIN** is rarely used. Most people simply switch the tables and stick with **LEFT JOIN**. But using the previous example for **LEFT JOIN**, the query using **RIGHT JOIN** would look like the following:

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%2010.png)

The query results are the same as the previous **LEFT JOIN** example.

| **customer_name** | **sales_rep** |
| --- | --- |
| Martin's Ice Cream | Luis Reyes |
| Beachside Treats | NULL |
| Mona's Natural Flavors | Geri Hall |
| ...etc. | ...etc. |

### **FULL OUTER JOIN**

You may sometimes see this as **FULL JOIN**. **FULL OUTER JOIN** returns all records from the specified tables. You can combine tables this way, but remember that this can potentially be a large data pull as a result. **FULL OUTER JOIN** returns all records from *both* tables even if data isn’t populated in one of the tables. For example, in the query below, you will get all customers and their products’ shipping dates. Because you are using a **FULL OUTER JOIN**, you may get customers returned without corresponding shipping dates or shipping dates without corresponding customers. A **NULL** value is returned if corresponding data doesn’t exist in either table.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%2011.png)

The results from the query might look like the following.

| **customer_name** | **ship_date** |
| --- | --- |
| Martin's Ice Cream | 2021-02-23 |
| Beachside Treats | 2021-02-25 |
| NULL | 2021-02-25 |
| The Daily Scoop | NULL |
| Mountain Ice Cream | NULL |
| Mona's Natural Flavors | 2021-02-28 |
| ...etc. | ...etc. |

## For more information

**JOIN**s are going to be useful for working with relational databases and SQL—and you will have plenty of opportunities to practice them on your own. Here are a few other resources that can give you more information about **JOIN**s and how to use them:

- [**SQL JOINs](https://www.w3schools.com/sql/sql_join.asp):** This is a good basic explanation of **JOIN**s with examples. If you need a quick reminder of what the different **JOIN**s do, this is a great resource to bookmark and come back to later.
- [**Database JOINs - Introduction to JOIN Types and Concepts](https://www.essentialsql.com/introduction-database-joins/):** This is a really thorough introduction to **JOIN**s. Not only does this article explain what **JOIN**s are and how to use them, but it also explains the various scenarios in more detail of when and why you would use the different **JOIN**s. This is a great resource if you are interested in learning more about the logic behind **JOIN**ing.
- [**SQL JOIN Types Explained in Visuals](https://dataschool.com/how-to-teach-people-sql/sql-join-types-explained-visually/):** This resource has a visual representation of the different **JOIN**s. This is a really useful way to think about **JOIN**s if you are a visual learner, and it can be a really useful way to remember the different **JOIN**s.
- [**SQL JOINs: Bringing Data Together One Join at a Time](https://towardsdatascience.com/sql-join-8212e3eb9fde):** Not only does this resource have a detailed explanation of **JOIN**s with examples, but it also provides example data that you can use to follow along with their step-by-step guide. This is a useful way to practice **JOIN**s with some real data.
- [**SQL JOIN:**](https://www.dofactory.com/sql/join) This is another resource that provides a clear explanation of **JOINs** and uses examples to demonstrate how they work. The examples also combine **JOIN**s with aliasing. This is a great opportunity to see how **JOIN**s can be combined with other SQL concepts that you have been learning about in this course.

---

# Hands-On Activity: Queries for JOINS

## Activity Overview

You’ve just learned about **JOIN**s and aliasing. Now, you’ll practice writing queries that join multiple tables to build more robust datasets and use aliasing to make your SQL queries clearer. In this activity, you will load and examine two tables from the World Bank’s International Education dataset in order to identify and understand their keys. You will also review **JOIN**s and write your own query that includes **JOIN**s and aliases. Finally, you’ll use a **JOIN** to answer a specific question about the data.

By learning how to apply **JOIN** statements and aliasing, you’ll be able to fully harness the power of relational databases by combining data from tables linked by keys.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Load the dataset**

1. Log in to [BigQuery Sandbox](https://cloud.google.com/bigquery/docs/sandbox). If you have a free trial version of BigQuery, you can use that instead. On the BigQuery page, select the **Go to BigQuery** button.

**Note:** BigQuery Sandbox frequently updates its user interface. The latest changes may not be reflected in the screenshots presented in this activity, but the principles remain the same. Adapting to changes in software updates is an essential skill for data analysts, and it’s helpful for you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.

2. Now, you’ll find the **Editor** interface. There are three major menus: the BigQuery navigation menu, the **Explorer** pane where you can search for datasets, and the details pane.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_RlRGkuJTkyF0wZjeILSHw_3885164e8d994ee0976264e04fd8ece1_C5M3L2A1-1.png?expiry=1716940800000&hmac=MNlSXIm9qWVCByVRiHSCxufqHMb-8uP4NXL2wfDJiEU)

3. Select the **+ ADD** button in the Explorer pane, then scroll down and select the **Public Datasets** option.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5bew0TQgTReSZk3qxjubvA_4646f87cb54a472aa0d1e34aa9ffe7e1_C5M3L2A1-2.png?expiry=1716940800000&hmac=HOnCgGRkBnKE5XweaFrF9vILnRmrKgz-5HzcS3ETi3Q)

4. In the **Search Marketplace** text box, enter **international education** and press Return to find the search results.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4t8EUiWkTuGPALDHYRQbpg_6a16f7f69ee546ef9b799feb251abae1_C5M3L2A1-3.png?expiry=1716940800000&hmac=MHfmM5luCLEj7H_3MDW7p_ix9PdHqxhY1WrWrR2Zmq8)

5. Select the World Bank's **International Education** dataset, which is the first result.

6. Select the **View Dataset** button to open the dataset in BigQuery in a new tab.

**Note:** You may want to star the **bigquery-public-data** resource in the **Explorer** pane. That way, you can access and browse the public datasets and tables more easily without having to navigate to the marketplace in the future.

7. In the Explorer pane, search for **world_bank_intl_education**. Expand the dataset to explore the tables it contains. You may also need to click on the **SHOW MORE** button for the additional tables to display.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pQTc5hCmRx6nJdT2NraBYg_27730982c91344c397fac17f9e1ecae1_C5M3L2A1-4.png?expiry=1716940800000&hmac=5cPJeFnXjIjxKgJGWFDTwdmzxaOUN20RGbz9iXUU-vo)

# **Step 2: Identify and understand keys**

Before you begin joining tables together, take a moment to consider how JOINs work: Two tables must be connected by their primary and foreign keys in order to join them. Keys are the most important elements of **JOIN**s—**JOIN**s function by combining tables based on those shared fields.

When designing a **JOIN** statement, these keys are listed in the **ON** statements as references to specific columns or fields within each table from the join: primary and foreign keys.

Consider two tables in the world_bank_intl_education dataset: **international_education** and **country_summary**. In order to understand how you might join these tables, take a moment to identify which columns you could use to combine them from each table. You can do that by examining the table schemas.

1. In the **Explorer** pane, select the **international_education** table. This will bring up the table’s schema in the details pane. If the schema doesn’t appear, select the **Schema** tab in the details pane. You might also check out the preview to view the data in the table.
2. Next, select the **country_summary** table and examine its schema. You’ll find that the country_code column appears in both table schemas. You might also check out the preview.

**What do you notice about the columns from each table?**

Both of these tables share a field name: **country_code**. As you continue with this activity, you will use this common field for your JOIN as both your primary and foreign key. It’s important to understand that foreign keys don't always have the same names across tables. If you’re ever unsure if the columns are the same, you can always double-check. To do so, select the **Details** tab for each table and confirm that they contain the same kinds of information.

# **Step 3: Review JOINs**

Now that you have identified the key field for joining these tables, take a moment to review the various kinds of **JOIN** statements.

Circles represent table 1 and table 2. In the inner join, where the tables are joined is highlighted in blue, which means the results will display only the rows from the two tables where the primary key in table 1 matches the foreign key in table 2. In the full join, tables 1 and 2 are completely green. This means the query results will display all rows from both tables regardless of whether their primary key and foreign key match.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9GPSmQOfRxa9zpxqURCIrw_402f37beb4d445a1bedf9888e77392e1_C5M3L2A1-5.png?expiry=1716940800000&hmac=2CqwCfMkkV3nG1nln4IN11GwWUzVv4H_NQbzcmY1ofo)

Circles represent table 1 and table 2. In the left join, table 1 is highlighted in blue and the overlap indicates that the join will show all rows in table 1 and only the related rows from table 2.  In the  right join, table 2 is highlighted green. The overlap shows that the results will contain all rows from table 2 and only the related rows from table 1.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cPGU_iKVR_-fBetVYR6jFQ_bccc32309587490a96089f8bef9e0ce1_C5M3L2A1-6.png?expiry=1716940800000&hmac=t4XKw-0trLe94yPpUY1SxiUoaPn76qPZ9eH8VKRWoSQ)

The two most common kinds of JOIN statements are **INNER JOIN** and **OUTER LEFT JOIN** (also known simply as **LEFT JOIN**). As a review:

- **INNER JOIN**: Returns only the rows where the target appears in both tables.
- **LEFT JOIN**: Returns every row from the left table, as well as any rows from the right table with matching keys found in the left table.

Before you work with the BigQuery sample dataset, here’s an example to help solidify your understanding of how to select the appropriate **type** of **JOIN**.

Imagine that you have one table with a list of customers (**Table 1 = CUSTOMER**) and another with a list of sales (**Table 2 = SALES**). You want to return all of the **SALES** fields, plus the customer name (**field_name = CUST_NAME**) and the state (**field_name = STATE**) that the customer lives in. The query final query should appear like this:

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%2012.png)

In this case, **SALES.CUST_ID** is the primary key and **CUSTOMER.CUST_ID** is the foreign key. This will show you all sales, regardless of whether there is an associated customer ID (**CUST_ID**).

Now, consider the following: If you only want to query SALES where there is a corresponding customer ID in the CUSTOMER table, how might you change the previous query?

One way to accomplish this is to simply change the **type** of **JOIN**. **LEFT JOIN CUSTOMER to INNER JOIN CUSTOMER**.

With that simple change, all of the rows from the SALES table that were missing a corresponding customer ID from the table would NOT show.

The type of **JOIN** you use is important. You can inadvertently add or lose records with a simple incorrect selection of your **JOIN** type. When writing a query, it can help to draw out a Venn diagram like the example graphic above to help you decide which sort of **JOIN** you need.

# **Step 4: Query the dataset and incorporate aliases**

Now, it’s time to actually query the dataset. In this section, you’re going to practice using **JOIN**s and explore how aliasing can help develop complex queries.

As a starting point, this is a  **JOIN** that does not use any aliasing. In the details pane, compose a new query to open a query window. In the query window, copy, paste, and run the following query:

```sql
SELECT `bigquery-public-data.world_bank_intl_education.international_education`.country_name,
    `bigquery-public-data.world_bank_intl_education.country_summary`.country_code,
    `bigquery-public-data.world_bank_intl_education.international_education`.value
FROM `bigquery-public-data.world_bank_intl_education.international_education`
INNER JOIN `bigquery-public-data.world_bank_intl_education.country_summary`
ON `bigquery-public-data.world_bank_intl_education.country_summary`.country_code = `bigquery-public-data.world_bank_intl_education.international_education`.country_code
```

This basic query joins the **'country_summary'** and **'international_education'** tables on the **'country_code'** key and returns the country name, country code, and value column. It’s a lot of effort to write out the full schema, table, field names every time you want to reference them. You can make these much easier to work with by using aliasing.

Here is the exact same query, but this time it uses an alias for each table:

```sql
SELECT
    edu.country_name,
    summary.country_code,
    edu.value
FROM
    `bigquery-public-data.world_bank_intl_education.international_education` AS edu
INNER JOIN
    `bigquery-public-data.world_bank_intl_education.country_summary` AS summary
ON edu.country_code = summary.country_code
```

This query is much easier to read and understand. You can set aliases for tables and fields by specifying the alias for the table after the table’s name in **FROM** or **JOIN** statements. In this case, the international_education table was renamed as **edu**, and the country_summary table as **summary**. Using descriptive aliases is a best practice and will help you keep your queries clean, readable, and easy to work with.

# **Step 5: Use a JOIN to answer a question**

Now that you’ve confirmed that the **JOIN** statement works, answer the following question: In 2015, how many people were of the official age for secondary education broken down by region of the world?

For this query, you will need to perform some additional tasks before returning the result:

- Exclude rows with a missing region.
- Use the **SUM(value)** to calculate the total population for a given grain size.
- Sort by highest population region first.

In a query window, copy, paste, and run the following query:

```sql
SELECT
summary.region,
SUM(edu.value) secondary_edu_population
FROM
    `bigquery-public-data.world_bank_intl_education.international_education` AS edu
INNER JOIN
    `bigquery-public-data.world_bank_intl_education.country_summary` AS summary
ON edu.country_code = summary.country_code --country_code is our key
    WHERE summary.region IS NOT NULL
    AND edu.indicator_name = 'Population of the official age for secondary education, both sexes (number)'
    AND edu.year = 2015
GROUP BY summary.region
ORDER BY secondary_edu_population DESC
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pDFPPK1LRQ-XmS2KippguA_736f3ec00f78435b8ee316c975c0eee1_C5M3L2A1-7.png?expiry=1716940800000&hmac=YAKe06Y_NrseR2T577CXn9-cCzMK8MJIw0K2sFF16NY)

Notice how, in this query, an alias is also set to give the **SUM(edu.value)** a more descriptive name for the temporary table the query returns.

Also note that the **WHERE** statement excludes rows with any null information. This is necessary to present the data succinctly and display only seven rows for the seven regions present in the data. However, this **WHERE** statement means that the results will return the same regardless of which **JOIN** you use. In the next section, you’ll explore a situation where you need to use a specific kind of join in your query.

# **Step 6: Decide when to use INNER JOINs versus OUTER JOINs**

In the last query, you used an **INNER JOIN** to find the total population of the official age for secondary education in 2015 broken down by region. Because of the **WHERE** statement that removed null values in our previous query, using any other **JOIN** methods (left outer join, right outer join, full outer) would have produced the same result.

Now, you will write a **LEFT JOIN**, a type of **OUTER JOIN**, for a situation where the type of query you use will change the result you return.

Consider this scenario: You have been tasked to provide data for a feature sports article on NCAA basketball in the 1990s. The writer wants to include a funny twist about which Division 1 team mascots were the winningest.

You’ll need a list of all NCAA Division I colleges and universities; their mascots, if applicable; and their number of wins and losses. You can find this information by typing **ncaa_basketball** in the Explorer tab dataset search bar on BigQuery.

Next, start a new query tab by clicking on the **blue +** button. Your query should join the season statistics from one table with the mascot information from another. You need to use a **LEFT JOIN** instead of an **INNER JOIN** because not all teams have mascots. If you use an **INNER JOIN**, you would exclude teams with no mascot.

To demonstrate this, copy, paste, and run the following query:

```sql
SELECT
 seasons.market AS university,
 seasons.name AS team_name,
 mascots.mascot AS team_mascot,
 AVG(seasons.wins) AS avg_wins,
 AVG(seasons.losses) AS avg_losses,
 AVG(seasons.ties) AS avg_ties
FROM `bigquery-public-data.ncaa_basketball.mbb_historical_teams_seasons` AS seasons
LEFT JOIN `bigquery-public-data.ncaa_basketball.mascots` AS mascots
ON seasons.team_id = mascots.id
WHERE seasons.season BETWEEN 1990 AND 1999
 AND seasons.division = 1
 GROUP BY 1,2,3
ORDER BY avg_wins DESC, university
```

This is an example of when a **LEFT JOIN** is more helpful than an **INNER JOIN**. With this query, you can review college basketball statistics to get a better sense of which teams (and mascots) were winning most in the 1990s.

---

# Upload the warehouse dataset to BigQuery

Coming up, you’re going to learn more about how to use **COUNT** and **COUNT DISTINCT** in SQL to count and return the number of certain values in a dataset.

To prepare for these activities, you will need to log in to your BigQuery account and upload the warehouse data provided below as two .csv files.

## Upload the data

To begin, download the two .csv files from the attachments below:

[Warehouse Orders - WarehouseCSV File](https://d3c33hcgiwev3.cloudfront.net/PcJNDf5ySCqk7V2xQoiu2Q_90874562d5cd4e7c9ba848fd44d512e1_Warehouse-Orders---Warehouse.csv?Expires=1716940800&Signature=MnTu9nJ3yRAtF5rzGjqVZmUk8pQFFShw6rxkm6u5m-~Lg6wzlf1AVqpwtXjMtXQfS2B3YwpNkw4Y3rIlNqhyIht7aPIPxoUYFgNgFvHHpL8a0YOrP-KozMG4j9nvWI947b4Syno8Wvhw79gWnNrQ1cCQcrdW9Xy4BZeUH09bfvo_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Warehouse Orders - OrdersCSV File](https://d3c33hcgiwev3.cloudfront.net/helGYTW6Tv-vyOH0l-yIPA_1a019ecb2cce49f48fd69d85f7dadce1_Warehouse-Orders---Orders.csv?Expires=1716940800&Signature=BnVliy3TKUQCo2FD6EVwAnE3KoIokDxv4BPSoJixDqHxP289RiR41p9iqgAASSqzDhtjAOHuEbMRshytuVMWOsN1T7Vvy2yOZ8dV69-cUWrPrWrsEfNxG53oJBtQFcfGy27Niqs53tp4e3Tv36lzPoSEN6OkUigVb~A5Q0Il0-M_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

Next, complete the following steps in your BigQuery console to upload the Warehouse Orders dataset with the two Warehouse and Orders tables.

1. Open your [BigQuery console](https://console.cloud.google.com/bigquery) and select the project you want to upload the data to.

2. In the Explorer pane, select the Actions icon (three vertical dots) and select **Create dataset**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/utTs756ORJaNziHoBTLbLA_1f4e02359fc84f379f99fd65b218d6e1_C1M3L2-1.png?expiry=1716940800000&hmac=p_A8p0qigYePrcItfmcFLznbJEZZEgC1JgbRz8neSBI)

3. The name "warehouse_orders" will be used for the dataset. Enter **warehouse_orders** for the Dataset ID in the Create dataset pane. Make sure the **Location type** is set to **Multi-region** and that the region selected is **US (multiple regions in the United States)**. Leave the **Advanced options** at their default settings.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1OPxHYP8SO2tDqVubJZXLQ_7361cde0acf74893926e30405394f6e1_C1M3L2-2.png?expiry=1716940800000&hmac=Anwp3anyW0Bvw5OeGu17pFgbezDoeaAYFGMOsp2ogHE)

4. Select the **CREATE DATASET** button to add the dataset to your project.

5. In the Explorer, select the **warehouse_orders** dataset you just created. You will then view the dataset info window in the main editor window.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9HBIeKkLT3yL085vWdb-DQ_0083727e14474a149940aa45bec66de1_C1M3L2-3.png?expiry=1716940800000&hmac=4VoEUXL5vQWQA4qCiD7WNFK8dSf5w4XuGTGp8UvVD9Q)

6. Navigate to the  **+ CREATE TABLE** button to open the **Create table** pane.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pmI3FucsR_eZQnXh5Ab9Gg_306ab6fd3c79403bb29574344f54efe1_C1M3L2-4.png?expiry=1716940800000&hmac=UUlYtPXmfXwStrQDV6ytLtfLPGmtmJKu6zvaHjCFfnw)

7. From the **Create table from dropdown list**, choose where the data will be coming from.

- Select **Upload**.
- Select the **Browse** button to select the **Warehouse Orders - Orders.csv** file you downloaded.
- Choose **CSV** from the file format dropdown list (file type may automatically be detected).

8. In the **Table** text box, enter **orders** if you plan to follow along with the video.

9. Below **Schema**, select the **Auto detect** checkbox.

10. Select **CREATE TABLE**. You will now find the **orders** table below your **warehouse_orders** dataset in your project.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iDmCnAD5SUuMHOo_dM9nnQ_ea974b12f8b6438c8185539fe2bf5ee1_C1M3L2-5.png?expiry=1716940800000&hmac=fLdh5RoztxxrJ0ZlEpoK9wskH69k3BJGgcBHz8tYitc)

11. Select the **warehouse_orders** dataset again.

12. Navigate to the **+ CREATE TABLE** button to open the **Create table pane** again.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xb1KqYu-T4OVjFj4Hily9g_fe926a39e18645c88399f3e15f90fae1_C1M3L2-6.png?expiry=1716940800000&hmac=Wf6iiMzTi_Qqse51Z_GAw4UbQ9kHBQamEpJZe9qpD2k)

13. For the Create table from selection, choose where the data will be coming from.

- Select **Upload**.
- Select **Browse** to select the **Warehouse Orders - Warehouse.csv** file you downloaded.
- Choose **CSV** from the **File format** dropdown list.

14. For Table name, enter **warehouse** if you plan to follow along with the video.

15. For Schema, select the **Auto detect** checkbox.

16. Select the **CREATE TABLE** button. You will now find the **warehouse** table under your **warehouse_orders** dataset in your project.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WoO10M6zQUOZ3YFXklnV6w_a31a5e50657f4708affed3b569df47e1_C1M3L2-7.png?expiry=1716940800000&hmac=mpvHYVZQ9D9sFzb22N3SbrHerE1rFwHnmcMtTMntD0M)

17. In the Explorer pane, select the **orders** table and then select the **Preview** tab to verify that you retrieve the first 50 rows of data. You may have to scroll down the page to view all 50 rows (there are 9999 pages total).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/q0vDZT-6RS2guDp1zhegbw_08450e68588d45f69cebd61502029be1_C1M3L2-8.png?expiry=1716940800000&hmac=eUrqrEew3EkKFqfF03I7BxKR6PjX8heljhnGL4Sbqws)

18. Select the **warehouse** table and select the **Preview** tab to verify that you can view 10 rows of data. If both your data previews match, you are ready to move along to the [COUNT and COUNT DISTINCT](https://www.coursera.org/teach/analyze-data/authoringBranch~4f7eJX9NEe6L0QpSVaIh4Q/content/item/project/3K5St) activity.

---

# Hands-On Activity: COUNT and COUNT DISTINCT

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/KNwt-Tj-T5iH1pjM5dSjow_dce8253353664d109b77ad40087478f1_Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716940800000&hmac=PggasvW6VX0h1pS9iSXXhWoN-nbYOVcT5zMNpT-uJXI)

You have learned that spreadsheets and SQL have a lot in common. In a spreadsheet, the **COUNT** function is used to count the number of cells that contain numerical values in a specified range or in an array of cells. In SQL, **COUNT** and **COUNT DISTINCT** are similar tools. The **COUNT** function returns the number of records that are returned by a query. **COUNT DISTINCT** performs the same function as **COUNT**, but it also removes both duplicate rows of the same data and null values from the result set. In this activity, you will practice using both **COUNT** and **COUNT DISTINCT** in your queries.

By the time you complete this activity, you will be able to use **COUNT** and **COUNT DISTINCT** in your queries to determine the amounts of things. Remember, **COUNT** and **COUNT DISTINCT** will return numerical values found within a dataset, helping you answer questions like, “How many customers did this?” Or, “How many transactions were there this month?” Or, “How many dates are in this dataset?”

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the dataset**

For this activity, you will need the warehouse dataset uploaded into your BigQuery project space. If you haven’t already uploaded this data, follow the instructions in the [Upload the warehouse dataset to BigQuery](https://www.coursera.org/learn/analyze-data/supplement/HuXCc/optional-upload-the-warehouse-dataset-to-bigquery) reading.

# **Step 2: Examine the warehouse_orders.warehouse table**

In this scenario, you are a junior data analyst working for a company that manufactures socks. You have access to data on the company’s customers, orders, warehouses, and products. Within the dataset, there are two tables: **warehouse** and **orders**. Begin by examining the **warehouse** table:

1. In line 1, enter **SELECT**, then press **Enter/Return** on your keyboard.
2. In line 2, press **Tab** on your keyboard. Then, add an asterisk (****), then press **Enter/Return**.
3. In line 3, press **Backspace** to remove the indentation, then enter **FROM**. Then, press **Enter/Return**.
4. In line 4, press **Tab**, then enter **`your-project-name.warehouse_orders.warehouse`**. (Replace **your-project-name** with the unique name of your project).
5. Select **RUN**.

You can also copy and paste the following query into the query window instead, making sure to replace **your-project-name** with your unique project name.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%2013.png)

After running the query, the five columns from the warehouse table will load in the **Query results** window:

- **warehouse_id:** indicates the ID number of each warehouse
- **warehouse_alias:** indicates the alias, or name, of each warehouse
- **maximum_capacity:** indicates the maximum capacity at each warehouse
- **employee_total:** indicates the total number of employees at each warehouse
- **state:** indicates the postal abbreviation for the U.S. state each warehouse is located in

# **Step 3: Examine the warehouse_orders.order table**

Next, create a new query to retrieve the first 100 rows of the orders ****table. Use LIMIT ****to limit the number of rows returned. This is useful if you're working with large datasets, especially if you just want to explore a small sample of that dataset.

1. Start a new query.
2. In line 1, enter **SELECT**, then press **Enter/Return**.
3. In line 2, press Tab on your keyboard. Then, add an asterisk (****), then press **Enter/Return**.
4. In line 3, press **Backspace** to remove the indentation, then enter **FROM**. Then, press **Enter/Return**.
5. In line 4, press **Tab**, then enter **`your-project-name.warehouse_orders.orders`**. (Replace **your-project-name** with the unique name of your project). Then press **Enter/Return**.
6. In line 5, press **Backspace** to remove the indentation, then enter **LIMIT 100**.
7. Select **RUN**.

You can also copy and paste the following query into the query window instead, making sure to replace **your-project-name** with your unique project name.

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%2014.png)

After running the query, the five columns from the orders table will load in the **Query results** window:

- **order_id:** indicates the ID number of each order
- **customer_id:** indicates the ID number of each customer
- **warehouse_id:** indicates the ID number of each warehouse
- **order_date:** indicates the date on which the order was placed
- **shipper_date:** indicates the date on which the order was shipped

Also notice the number of results returned in the query: 100 results.

# **Step 4: Create aliases and JOIN the tables**

Aliasing involves temporarily naming a table or column in your query to make it easier to read and write. Because these names are temporary, they only last for the given query. Use a **FROM** statement to write in what the tables' aliases are going to be. This will save time in other parts of the query. To alias the **warehouse_orders.orders** table as **orders**:

1. 
2. In line 1, enter **SELECT**, then press **Enter/Return**.
3. In line 2, press **Tab** on your keyboard. Then add an asterisk (****), then press **Enter/Return**.
4. In line 3, press **Backspace** to remove the indentation, then enter **FROM**. Then press **Enter/Return**.
5. In line 4, press **Tab**, then enter **`your-project-name.warehouse_orders.orders` orders**. (Replace **your-project-name** with the unique name of your project). Then press **Enter/Return**.

**Note:** An alternate syntax uses the **AS** keyword to assign an alias name:

![Untitled](Use%20JOINS%20to%20aggregate%20data%20in%20SQL%20f73d8a79dd0147a0bcd785bbd09becc6/Untitled%2015.png)

Queries can run with or without the **AS** keyword, but using **AS** enables an alias to stand out so the query is easier to read.

Perhaps you need both the warehouse details and the order details so you can report on the distribution of orders by state. Use **JOIN** to join the two tables together to get data from both of them and alias the warehouse table in the process. In this case, use **JOIN** as shorthand for **INNER JOIN** to get corresponding data from both tables.

6. In line 5, press **Backspace**, then enter **JOIN**, then press **Enter/Return**.

7. In line 6, press **Tab**, then enter **warehouse_orders.warehouse warehouse ON orders.warehouse_id = warehouse.warehouse_id**.

Your query text should read as follows:

```sql
SELECT
	*
FROM
	`your-project-name.warehouse_orders.orders` AS orders
JOIN
    `your-project-name.warehouse_orders.warehouse` warehouse ON orders.warehouse_id = warehouse.warehouse_id
```

With the aliases in place and the two tables joined, circle back and update the **SELECT** statement at the beginning of the query:

8. In line 1, press **Enter/Return** to create a new line after **SELECT**.

9. In line 2, press Tab, then enter **orders.*,** (that is, “orders” followed by a **period**, **asterisk**, and **comma**). Press **Enter/Return**.

10. In line 3, enter **warehouse.warehouse_alias** followed by a **comma**, then press **Enter/Return**.

11. In line 4, enter **warehouse.state**.

12. Line 5 should now contain a single **asterisk**. **Delete** this line before running the query.

13. Select **RUN**.

After running the query, the data from both tables are now joined together in the **Query results** window with these seven columns:

- **order_id:** indicates the ID number of each order.
- **customer_id:** indicates the ID number of each customer.
- **warehouse_id:** indicates the ID number of each warehouse.
- **order_date:** indicates the date on which the order was placed.
- **shipper_date:** indicates the date on which the order was shipped.
- **warehouse_alias:** indicates the names given to each warehouse as an alias.
- **state:** indicates which state the warehouse is located in.

You can also copy and paste the completed query text below into the query window. Just remember to replace **your-project-name** with your unique project name.

```sql
SELECT
	orders.*,
	warehouse.warehouse_alias,
	warehouse.state
FROM
	`your-project-name.warehouse_orders.orders` AS orders
JOIN
    `your-project-name.warehouse_orders.warehouse` warehouse ON orders.warehouse_id = warehouse.warehouse_id
```

# **Step 5: Find the number of states with warehouses that shipped orders with COUNT DISTINCT**

As a data analyst, you might be interested in finding the number of states with warehouses that have shipped orders.

First, you'll try to do this with the COUNT function. Begin by modifying the query you wrote in the previous step to create aliases and **JOIN** the tables.

1. Delete lines 2-4. Line 2 should be blank, in between **SELECT** in line 1 and **FROM** in line 3.
2. In line 2, press **Tab** to create an indentation. Then enter **COUNT(warehouse.state) as num_states**.
3. Select **RUN**.

Your query text should read as follows:

```sql
SELECT
	orders.*,
	warehouse.warehouse_alias,
	warehouse.state
FROM
	`your-project-name.warehouse_orders.orders` AS orders
JOIN
    `your-project-name.warehouse_orders.warehouse` warehouse ON orders.warehouse_id = warehouse.warehouse_id
```

Notice how the query returned more than 9,000 results. There are only 50 states, so this is clearly not the answer you're looking for! This is because the query counted every single record (row) that included a state, regardless of duplicates or null values.

Don't worry! You can modify the existing query to remove duplicates and null values, and only count the distinct states with **COUNT DISTINCT**:

1. In line 2, enter **DISTINCT** after the open parenthesis and add a space before **warehouse.state** so that line 2 reads: **COUNT (DISTINCT warehouse.state) as num_states** . This will modify **COUNT** to operate as **COUNT DISTINCT**, and it will remove all the repeated instances from the results.
2. Select **RUN**.

According to the results, there are three distinct states in the **orders** data. Nice work! You've successfully used **COUNT DISTINCT**.

# **Step 6: Use GROUP BY to group the number of orders by state**

Next, you might want to find the number of orders shipped from warehouses in each state, instead of the number that shipped orders. You can find this information by using **GROUP BY** to group the **state** column in the warehouse table. Use **JOIN** and **GROUP BY** in the **FROM** statement.

1. 
2. In line 7, enter **GROUP BY**, then press **Enter/Return**.
3. In line 8, press **Tab** to create an indentation, then enter **warehouse.state**.
4. Select **RUN**.

The complete query text should read as follows:

```sql
SELECT
	state,
	COUNT(DISTINCT order_id) as num_orders
FROM
	`your-project-name.warehouse_orders.orders` AS orders
JOIN
  `your-project-name.warehouse_orders.warehouse` warehouse ON orders.warehouse_id = warehouse.warehouse_id
GROUP BY
	warehouse.state
```

After running the query, there are now three rows listed in the results table: one for each state represented within the **orders** data. The **Query results** window now displays two columns:

- Column one is **state**, which indicates which state the warehouse is located in.
- Column two is **num_orders**, which indicates the number of orders. These three numbers add up to the count that you ran previously—9,999.

Congratulations! You have successfully executed queries using **COUNT** and **COUNT DISTINCT**, as well as **SELECT**, **FROM**, and **GROUP BY** statements to create aliases and **JOIN** tables, return numerical values within a specific range, and group by specific columns within a table.

You'll find yourself using **COUNT** and **COUNT DISTINCT** during every stage of the data analysis process. Understanding what these queries are and how they are different is crucial in your role as a data analyst.

---