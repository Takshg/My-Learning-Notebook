# Learn basic SQL queries

---

# Widely used SQL queries

[index (1).mp4](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/index_(1).mp4)

**Key Points**

- **SELECT Query:** Used to extract specific data from a table.
- **FROM Clause:** Specifies the table from which data is extracted.
- **INSERT INTO Query:** Used to add new data to a table.
- **UPDATE Query:** Used to modify existing data in a table.
- **CREATE TABLE IF NOT EXISTS Statement:** Used to create a new table in a database.
- **DROP TABLE IF EXISTS Statement:** Used to delete a table from a database.

**Definitions**

- **Query:** A request to a database to perform a specific action.
- **Table:** A collection of data organized into rows and columns.
- **Database:** A collection of tables that store related data.
- **Data Cleaning:** The process of identifying and correcting errors in data.

---

# Clean string variables using SQL

[index (2).mp4](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/index_(2).mp4)

**Key Points:**

- **Importance of Data Cleaning:** Cleaning and completing data before analysis is crucial for accurate insights.
- **Removing Duplicates:** Use `SELECT DISTINCT` to remove duplicate entries based on a specific column.
- **Cleaning String Variables:**
    - **`LENGTH` Function:** Checks the number of characters in a string.
    - **`SUBSTRING` Function:** Extracts a specific portion of a string based on starting position and length.
    - **`TRIM` Function:** Removes leading and trailing spaces from a string.
- **Example:** Identifying and correcting inconsistencies in the `country` and `state` columns of the `customer_address` table.

**Definitions:**

- **String Variable:** A group of characters within a cell, typically composed of letters, numbers, or both.
- **Data Cleaning:** The process of identifying and correcting errors, inconsistencies, and missing values in data.
- **Duplicate Entries:** Multiple entries in a dataset that represent the same entity.
- **`SELECT DISTINCT`:** A SQL statement used to retrieve unique rows from a table based on a specified column.
- **`LENGTH` Function:** A SQL function that returns the number of characters in a string.
- **`SUBSTRING` Function:** A SQL function that extracts a substring from a string based on a starting position and length.
- **`TRIM` Function:** A SQL function that removes leading and trailing spaces from a string.

---

# Hands-On Activity: Clean data using SQL

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3UWxlyqNRxaFsZcqjZcWgQ_3fd91ae61ce04caaa755c3477a337947_line-y.png?expiry=1716854400000&hmac=yjCSowGMfy4MFIfUa2He6nVGJ4klUlOx0-hTmys7Dkk)

In previous lessons, you learned about the importance of being able to clean your data where it lives. When it comes to data stored in databases, that means using SQL queries. In this activity, you will create a custom dataset and table, import a .csv file, and use SQL queries to clean automobile data.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

In this scenario, you are a data analyst working with a used car dealership startup venture. The investors want you to find out which cars are most popular with customers so they can make sure to stock accordingly.

By the time you complete this activity, you will be able to clean data using SQL. This will enable you to process and analyze data in databases, which is a common task for data analysts.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the template**

To get started, download the *automobile_data.csv* file. This is data from an external source that contains historical sales data on car prices and their features.

Click the link to the *automobile_data.csv* file to download it. Or you may download the .csv file directly from the attachments below.

Link to data: [automobile_data](https://docs.google.com/spreadsheets/d/1U3ktsROmhoCZG3Yz5xFLnjJmzm-MgBYYxwt4xcb6d3o/template/preview)

OR

[automobile_dataCSV File](https://d3c33hcgiwev3.cloudfront.net/CHOsbSb3RYGzrG0m98WBiQ_f6e1579446f9464699fab3ea55ecb6f1_automobile_data.csv?Expires=1716854400&Signature=DjgHLpMCvobKHrr7XhgdPIm6S5iJIxzaGcQ4ohvhzJQIn4JaVlOPO1ZlFmYPlmUeYkYLC-5pwlAd1yBELQX4SmswSs-Eeql6LCWgictoKzf-abAkHqYbsw46T7DmUQHLO0TQkyINgzN6OMOLapGZc-IF2Ef086RERk7-xTOzBAs_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

# **Step 2: Create a dataset**

Once you’ve downloaded the **automobile_data.csv** file, create your dataset.

Go to the **Explorer** pane in your workspace and click the three dots next to your personal project name ****to open the drop-down menu. From here, select **Create dataset.**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_4H2g8bKReuWQbcc2nVVJQ_c0f83066fc634c4cb5d31829eb4a22f1_5.CreateDataset.jpg?expiry=1716854400000&hmac=8QlEkJ6wN23NLQ6K1UrayXcA2P3Q3MT7FdH0CIEy3Bo)

From the **Create dataset** menu, fill out some information about the dataset. Input the Dataset ID as **cars** you can keep the **Location type** as **Multi-region,** **US (multiple regions in United States),** and the **Encryption** as **Google-managed encryption key** default settings. Then, click the **CREATE DATASET**  button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qGvDTuZ4Q6i-0MWXoR8DQA_c5e10939d604439987327805fd8606f1_6.cratedataset_cars.jpg?expiry=1716854400000&hmac=Te_nbdu6cvzrWkSTO99hyueXeMv5EVaCMZwGWu2i1rg)

The **cars** dataset should appear under your project in the Explorer pane as shown below.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1yge3XOdQ6CL8AsoFl2ZFA_905a4407a002407697996045226f2bf1_7.cars_dataset.jpg?expiry=1716854400000&hmac=uICKXA9HX0oSxMpKbJLC-AOfqAdQkKIwFpSAEqBRM8g)

# **Step 3: Create a table**

Now that you've created a dataset. You'll create a custom table to house your data. This will enable you to use SQL queries to explore and clean data.

After clicking on **cars** to open your newly created dataset, you will be able to add a custom table for the insertion of your downloaded data.

From the **cars** dataset info window, ****click **CREATE TABLE**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/D8CMXWXPTXmAjF1lz815hw_8877de9f0c384e18a9fffe5ee34b5df1_Screenshot-2021-06-09-4.02.42-PM-1-.png?expiry=1716854400000&hmac=OGUgllPm_lAEkxEdl92yETQ_A9RpVzyRwsjm4_rw2uY)

Within the **Create table** window, upload the **automobile_data.csv** by clicking the drop-down arrow under **Source** and choosing the **Upload** option**.** Click the **BROWSE** button and navigate to the folder where your .csv document is located, and notice the **File format** will automatically change to **CSV.** Ensure the dataset name is **cars** and name your table **car_info.** Set the schema to Auto-detect, and finally click the **Create table** button.****

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fAQSvkaZT5-JORcNcOeSfA_14103dc6d8b14adb9f6fb19e7aa716f1_2.tabletable.jpg?expiry=1716854400000&hmac=tzG_cRgPAJClRrnif7UA8Ct7VByIz315-obrvl0ePzs)

After creating your table, it will appear in your Explorer pane. You can click on the newly created table, **car_info**, to explore the **SCHEMA** and **DETAILS** buttons within your data page. Once you have gotten familiar with your data, you can start querying it.

# **Step 4: Understand why you clean your data**

Your new dataset contains historical sales data, including details such as car features and prices. You can use this data to find the top 10 most popular cars and trims. But before you can perform your analysis, you’ll need to make sure your data is clean. If you analyze dirty data, you could end up presenting the wrong list of cars to the investors. That may cause them to lose money on their car inventory investment.

Continue below to clean your data.

# Step 5: Inspect the fuel_type column

The first thing you want to do is inspect the data in your table so you can find out if there is any specific cleaning that needs to be done. Get an initial understanding of the data table by clicking on the **PREVIEW** tab that sits below the **car_info** toolbar.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1LZvcpFpRwmtXhUCr12DNw_9243d00866e143328498809a64265bf1_3.preview.jpg?expiry=1716854400000&hmac=4KXEY8D5N2a66xkUVE7MZp2-Eqc2J2Ljp0LEmysLP28)

According to the [data’s description](https://archive.ics.uci.edu/ml/datasets/Automobile), the **fuel_type** column ****should only have two unique string values: **diesel** and **gas**. To check and make sure that’s true, run the following query. You can generate the default query setup by clicking on the **QUERY** button and selecting the **In split tab**. This will give you a dual view of the info window and the query.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Pw7fUI7oQUqnVEKs2BXifA_8a4858448fb64fe6934b9d5755a9c9f1_4.queryresult.jpg?expiry=1716854400000&hmac=RxPXXplKkDxws1G6e0KcmJJlju_FBvrmZAtg6rX_a0A)

Next, we can generate the first query in the workspace: ****

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled.png)

**NOTE**: Within the **FROM** clause of the syntax above, you will need to begin the **Table ID** line with your personalized project name,  period, the dataset name, period, and end with the table name. It's important to understand that the personal project name will be unique to each learner. You can also locate and copy the full **Table ID** filename by clicking on the **DETAIL** option tab in your **car_info** **Table info** window. Once copied, paste it after the **FROM** clause and run the above query.

This returns the following results:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2PvkmVqCR6q75Jlaghequw_572b7e9c7f6a435fa142ecbb57c090f1_Screenshot-2021-06-10-11.44.02-AM-1-.png?expiry=1716854400000&hmac=zatEdA6Lv-bCUAoVwIIrwyGz3WgmsIkhc_gmo2xr0B8)

This confirms that the **fuel_type** column doesn’t have any unexpected values. Also note that the default **LIMIT 1000** is added to your query, but in this case, BigQuery is only returning two distinct fuel types.

# **Step 6: Inspect the length column**

Next, you will inspect a column with numerical data. The

**length**

column should contain numeric measurements of the cars. So you will check that the minimum and maximum lengths in the dataset align with the [data description](https://archive.ics.uci.edu/ml/datasets/Automobile), which states that the lengths in this column should range from 141.1 to 208.1. Run this query to confirm:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%201.png)

Your results should confirm that 141.1 and 208.1 are the minimum and maximum values respectively in this column.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QkcK0ZKESoKHCtGShJqCig_957228fafc6a41bd888315b31193e8f1_Screenshot-2021-06-10-2.40.29-PM-1-.png?expiry=1716854400000&hmac=R5IOnTdyt8B_tDE57gZFLsGqp9YjwHR8wW9EkMc67oI)

# **Step 7: Fill in missing data**

Missing values can create errors or skew your results during analysis. You’re going to want to check your data for null or missing values. These values might appear as a blank cell or the word **null** in BigQuery.

You can check to see if the **num_of_doors** column contains null values using this query:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%202.png)

This will select any rows with missing data for the **num_of_doors** column and return them in your results table. You should get two results, one Mazda and one Dodge:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/FPn6Bs_GRwi5-gbPxocIrQ_84308aef483b49fb81d4670aa8cc84f1_unnamed-9-.png?expiry=1716854400000&hmac=_QyZOIeX_Ho64nzuQsq9Ior86nZ6zGk-XdAklWEXTx4)

In order to fill in these missing values, you check with the sales manager, who states that all Dodge gas sedans and all Mazda diesel sedans sold had four doors. If you are using the BigQuery free trial, you can use this query to update your table so that all Dodge gas sedans have four doors:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%203.png)

You should get a message telling you that three rows were modified in this table. To make sure, you can run the previous query again:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%204.png)

Now, you only have one row with a null value for **num_of_doors**. ****Repeat this process to replace the null value for the Mazda.

If you are using the BigQuery Sandbox, you can skip these **UPDATE** queries; they will not affect your ability to complete this activity.

# **Step 8: Identify potential errors**

Once you have finished ensuring that there aren’t any missing values in your data, you’ll want to check for other potential errors. You can use **SELECT DISTINCT** to check what values exist in a column. You can run this query to check the **num_of_cylinders** column:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%205.png)

After running this, you notice that there are one too many rows. ****There are two entries for two cylinders: rows 6 and 7. But the *two* in row 7 is misspelled.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VHPfXt8kRnSz317fJAZ0bQ_9257fefd395046c290c809d29c2e2ef1_Screenshot-2021-06-10-3.44.19-PM-1-.png?expiry=1716854400000&hmac=0lPFos0ZsPzyXC15uZ6SpYygPyYDMqqpE1ZEj4izKhs)

To correct the misspelling for all rows, you can run this query if you have the BigQuery free trial:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%206.png)

You will get a message alerting you that one row was modified after running this statement. To ****check that it worked, you can run the previous query again: 

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%207.png)

Next, you can check the **compression_ratio** column. According to the [data description](https://archive.ics.uci.edu/ml/datasets/Automobile), ****the **compression_ratio** column values should range from 7 to 23. Just like when you checked the length values , you can use **MIN** and **MAX** to check if that’s correct:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%208.png)

Notice that **this returns a maximum of 70**. But you know this is an error because the maximum value in this column should be 23, not 70. So the 70 is most likely a 7.0. Run the above query again without the row with 70 to make sure that the rest of the values fall within the expected range of 7 to 23.

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%209.png)

Now the highest value is 23, which aligns with the data description. So you’ll want to correct the 70 value. You check with the sales manager again, who says that this row was made in error and should be removed. Before you delete anything, you should check to see how many rows contain this erroneous value as a precaution so that you don’t end up deleting 50% of your data. If there are too many (for instance, 20% of your rows have the incorrect 70 value), then you would want to check back in with the sales manager to inquire if these should be deleted or if the 70 should be updated to another value. Use the query below to count how many rows you would be deleting:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%2010.png)

Turns out there is only one row with the erroneous 70 value. So you can delete that row using this query:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%2011.png)

If you are using the BigQuery sandbox, you can replace **DELETE** with **SELECT** to see which row would be deleted.

# **Step 9: Ensure consistency**

Finally, you want to check your data for any inconsistencies that might cause errors. These inconsistencies can be tricky to spot—sometimes even something as simple as an extra space can cause a problem.

Check the **drive_wheels** column for inconsistencies by running a query with a **SELECT DISTINCT** statement:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%2012.png)

It appears that 4wd appears twice in results. However, because you used a **SELECT DISTINCT** statement to return unique values, this probably means there’s an extra space in one of the 4wd entries that makes it different from the other 4wd.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G9XjLN_ITf6V4yzfyB3-sg_1e7dda7421dc4fe089fd53a4a7d09af1_unnamed-10-.png?expiry=1716854400000&hmac=H_iJQo9F2Rhzxy35fTAvwpbsI_YZgxIyj8rA6OduDnY)

To check if this is the case, you can use a **LENGTH** statement ****to determine the length of how long each of these string variables:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%2013.png)

According to these results, some instances of the 4wd string have four characters instead of the expected three (4wd has 3 characters). In that case, you can use the **TRIM** function to remove all extra spaces in the **drive_wheels** column if you are using the BigQuery free trial:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%2014.png)

Then, you run the **SELECT DISTINCT** statement again ****to ensure that there are only three distinct values in the drive_wheels column:

![Untitled](Learn%20basic%20SQL%20queries%20c48bc8311d194301b9e4a1e1faddbb39/Untitled%2015.png)

And now there should only be three unique values in this column! Which means your data is clean,  consistent, and ready for analysis!

---