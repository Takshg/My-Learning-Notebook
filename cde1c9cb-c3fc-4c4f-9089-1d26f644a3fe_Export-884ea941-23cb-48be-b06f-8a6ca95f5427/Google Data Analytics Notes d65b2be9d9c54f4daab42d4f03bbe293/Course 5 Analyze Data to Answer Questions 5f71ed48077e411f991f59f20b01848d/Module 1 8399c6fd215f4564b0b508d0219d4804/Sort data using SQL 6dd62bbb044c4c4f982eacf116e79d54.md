# Sort data using SQL

---

# Step-by-Step: Sort data with SQL

[index (12).mp4](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/index_(12).mp4)

This reading outlines the steps the instructor performs in the following video, [Sort data with SQL](https://www.coursera.org/learn/analyze-data/lecture/P6Yu3/sorting-queries-in-sql). In the video, the instructor sorts data with SQL using the **ORDER BY** command. Then, the instructor uses **WHERE** and **ORDER BY** together to filter and sort data.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

## What you’ll need

If you’d like to follow along with the instructor, you will need to log in to your BigQuery account and upload the Movies dataset. To do this, follow the instructions in the reading [**Upload the movie dataset to BigQuery**](https://www.coursera.org/learn/analyze-data/supplement/sBFZn/optional-upload-the-movie-dataset-to-bigquery).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716940800000&hmac=UN0tlF7lkA95qCr5MP0pe0_funmKbzc9reSo7V0cU3E)

## Example 1: Sort data by one column

The **ORDER BY** command sorts data by column in a database. By default, the data is sorted in ascending order.

1. In the BigQuery **Explorer pane**, select the movie **dataset**, then the **movies** table.

2. Select the **Preview** tab from the **Details pane**.

3. Select **Query** then **In new tab** and enter the following code into the query editor:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled.png)

**Note:** If you’re completing this code in BigQuery, replace **projectID** in the code block to your own projectID.

4. Use the **ORDER BY** command to sort the data. Enter **ORDER BY Release_Date;** to sort by the **Release_Date** column.

5. Your code should now match this code block:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%201.png)

6. Select **RUN**. The results return all the movies in the database sorted from oldest to newest.

## Example 2: Sort data in descending order

To use the  **ORDER BY** command to sort data by descending order, specify **DESC** at the end of the **ORDER BY** command.

1. Enter **DESC** after **ORDER BY Release_Date** in the query editor.

2. Your code should now match this code block:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%202.png)

3. Select **RUN**. The results include the same list of movies, this time sorted from newest to oldest.

## Example 3: Filter and sort data in descending order

Use **WHERE** and **ORDER BY** together to filter, then sort, data.

1. Select the beginning of the **ORDER BY** line and press Enter (Windows) or Return (Mac) to add a line between the **FROM** and **ORDER BY** clauses. The **ORDER BY** command is written on the last line to ensure all data is sorted.

2. Select the line you added. Enter **WHERE Genre = "Comedy"** to filter for rows in which the Genre column exactly matches **"Comedy"**.

3. Your code should now match this code block:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%203.png)

4. Select **RUN** to run the query. The results include only comedy movies sorted from newest to oldest.

## Example 4: Filter on two conditions, then sort data in descending order

Use **WHERE**, **AND**, and **ORDER BY** to filter data on two conditions and then sort it.

1. Select the beginning of the **ORDER BY** line and press Enter (Windows) or Return (Mac) to add a line between the **WHERE** and **ORDER BY** clauses.

2. Select the line you added. Enter **AND Revenue > 300000000** to add a condition to your query to return only rows where the Revenue column is greater than 300,000,000.

3. Your code should now match this code block:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%204.png)

4. Select **RUN**. The results are sorted from newest to oldest and include only comedy movies with revenues greater than $300,000,000.

---

# Hands-On Activity: SQL sorting queries

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G-KePoi0R2Sinj6ItBdkMg_2d69ab4b929f40f2b472a78fdd5ed880_line-y.png?expiry=1716940800000&hmac=SEphjdYBdoz0TRm7EByd3ssnqoR5bANw6SL-vCmMzHc)

So far, you’ve learned about SQL and how it’s used to retrieve data from databases. In this activity, you’ll practice sorting data with the **ORDER BY** clause in SQL. Sorting is a powerful tool for a data analyst. It enables you to:

- Organize and analyze your data in a meaningful way
- Find highest or lowest values in a dataset
- Compare data across different dimensions

By the time you complete this activity, you will be able to write SQL queries that sort data depending on your needs.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

You’re a public health researcher with a state government agency. For your current project, you need to identify counties in the United States that have the most and least births in the 2016-2018 time frame. To do this, you’ll complete the following steps:

- Load the dataset.
- Query the data to explore its structure.
- Use **ORDER BY** to sort relevant data.
- Use sorted data to answer questions.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Load the CDC Births Data dataset**

1. Open the BigQuery console.

2. Select **+ADD** from the **Explorer** pane.

3. In the **Add** window, navigate to and then select **Public Datasets**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WPBn30fBQLW0145i6ZjYNw_5bf521ef660240fb851f04b8bc06e0e1_05.png?expiry=1716940800000&hmac=X_FMmkWC1DomLdr13uA2ibG-a5zGdHfe6PBnFskkIKM)

4. In the Marketplace search bar, enter **sdoh_cdc_wonder_natality** and press enter.

5. Select the result **Births Data Summary** from the CDC.

6. Select **VIEW DATASET**. This will bring you back to the console and open a **Dataset info** tab about the CDC dataset in the **Details** pane.

7. Select **sdoh_cdc_wonder_natality** in the **Explorer** pane to examine the tables available within the dataset.

8. Select the table **county_natality** and explore this table’s schema, details, and preview.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XEtzUNkWRtW4uwPVNrUy9w_7d594f5b71974002b6c8a1114546c9e1_08.png?expiry=1716940800000&hmac=XneAHVyjTqSNKe2V2sjCyEf8DyZdHMveWDSZFV0PSow)

# **Step 2: Query the data to explore its structure**

Now, it’s time to start working with the CDC births data. First, run a query to examine the dataset without sorting it.

1. Select **Query**, then **In new tab**.

2. Enter the following query into the Query Editor to display the first 1,000 rows of the **county_natality** table.

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%205.png)

3. Select **RUN**.

A screenshot of the Query results pane. The data returned include Year, County_of_Residence, County_of_Residence_FIPS, Births, Avg_Age_of_Mother, Ave_OE_Gestationa, and Ave_LMP_Gestational.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uuEoFMnGQqePxNLi5X3YqA_aa9c7978b6d34df1a184b567c4e8f6e1_10.png?expiry=1716940800000&hmac=ZeobmKyn5kUjNiixgMFaTZVxKSuhU0imt61GgfaD4m0)

Examine the dataset you just loaded. Take a moment to familiarize yourself with the columns and fields available.

**Note:** Many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.

# **Step 3: Use ORDER BY to sort relevant data**

Now, sort the data with SQL’s **ORDER BY** function. Enter the following query into the Query Editor. The text preceded by two hyphens (--) are comments that explain the code. Run the Query.

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%206.png)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5Yma0imFQde92sAK8WhMYw_23906c7ebcb3439591a5172d958338e1_11.png?expiry=1716940800000&hmac=YTspM6ymW_8ucnzx9jMQmn40bSceUGZc9_phzHOCJag)

Examine the Births column. Notice that it’s sorted from smallest to largest. When the **ORDER BY** function is applied to sort a given column, SQL will default to sorting in ascending order, which orders items from smallest to largest.

If you want the largest number to appear first, then you’d want to specify the sort order to be descending by adding a command to the **ORDER BY** clause. You can make your code easier to read by using a command to specify either sort order.  Here are the corresponding commands:

- **ASC** = Ascending
- **DESC** = Descending

Next, you’ll use the same query, but this time you’ll explicitly state the order of your **ORDER BY** function using **ASC**. Enter and run the following SQL query:

```sql
SELECT
  *
FROM
  bigquery-public-data.sdoh_cdc_wonder_natality.county_natality
ORDER BY
  Births ASC --Place the ASC or DESC specifier directly after the column name separated by a space (no other punctuation)
LIMIT
  10
```

Notice that the results did not change. Tompkins County, NY, had just 735 births in 2018—the lowest birth count of any county in the US between 2016-2018.

Now, change the order from ascending (**ASC**) to descending (**DESC**) to find the most births. Enter and run this query:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%207.png)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cqUM9BCFTG-lxHfNSpaXUg_e0f3ac71462b4d70806d57ae5907a9e1_13.png?expiry=1716940800000&hmac=AJ0zBmdYoLeoc7IzKd_fdoZSPjamItCCVFnoOtQcSC4)

The query returns the 10 rows with the largest values in the Births column. Los Angeles County takes up the top three spots.

# **Step 4: Use sorted data to answer questions**

Now that you've become familiar with the basics of sorting functions, use them to answer questions about your data. This exercise will require you to apply both your previous learnings (especially filtering with the WHERE clause) and your new understanding of sorting.

In your work as a public health researcher, you’re exploring whether the birth rate trends in several counties in upstate New York have been increasing or decreasing—and whether they follow the same pattern.

To answer this, you’ll need the following information:

- Results from Erie, Niagara, and Chautauqua counties in New York state
- Results ordered by county of residence and year to find the trend

The following query will filter the results by county and sort the results byear and county. This will allow you to determine if the number of births is increasing or decreasing in each county.

Enter the following query into the Query Editor, then select **RUN**.

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%208.png)

You’ve now successfully used both **ORDER BY** (sort) and **WHERE** (filter) clauses in the same query. Based on the results of this query, are births in these three counties following the same trend?

---

# Hands-On Activity: Analyze weather data in BigQuery

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SL8Kv9EMTV-_Cr_RDB1fXA_2f5ff69dcea8417983fab756eabb1870_line-y.png?expiry=1716940800000&hmac=i4qJyMaXNGuz9e2k1YpZdVbkLTZgXAotDhBQZMeBako)

So far, you’ve learned how to use BigQuery to clean, prepare, and analyze data. Now, you’ll query a dataset and save the results as a new table. This is a useful skill when the original, dynamic data source changes continuously and you need to preserve a specific dataset for continued analysis. It’s also valuable when you have access to a large dataset and know you’ll be doing more than one analysis on a subset of the dataset. By the time you complete this activity, you will be able to use SQL queries to create new tables when dealing with complex datasets.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

You’re a data analyst at a news station in New York City. You’ve been tasked with answering questions about the weather for meteorologists. You’ll work with a public dataset that contains global summaries of the day (GSOD) from the National Oceanic and Atmospheric Administration (NOAA). The GSOD dataset includes information about daily weather elements, such as mean temperature and wind speed, from more than 9,000 weather stations across the globe. This dataset is updated daily, so in addition to being large, this dataset is constantly changing. So, you’ll save a subset of the data about the New York region in a new table to make your analysis easier.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Add the NOAA weather data to BigQuery**

Log in to your BigQuery account (or [BigQuery sandbox](https://cloud.google.com/bigquery/docs/sandbox)) and initiate a new project or locate an existing project that you already created.

First, add the NOAA weather data from BigQuery’s public datasets.

1. Select the **+ ADD** button in the **Explorer** pane.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JRUouIYhTHiP8sC30H1Tfw_f9862f76281440e68f4fac7819fa86e1_TaqJ-nTuYWL6zPMB4FaULADOpIedkCdh4vLn5ucxi7mDrRzGe-KbyRSv6lxki3wUTPynXdU7vp7XSoEDkKyVbCJh3NBaF5clFFRmtN4SOV5IacAQOYnQDnwIP3pkB4BkVHTJVq2794PbSnu6kS05vwY?expiry=1716940800000&hmac=JxkqYzBYkf7LwLTvzFwn-6HQJxqUcBtOeLqVqNy9E54)

2. This opens a new **Add menu** where you can search public datasets available through Google Cloud. Scroll down the list and select **Public Datasets**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/N720hHAdRiijKLYSwZuXwg_5203b8fda6ea4139920a7d96b8501ce1_bIwK0IygSLf6lOJ29EztKcv9ZdTGiVPG4rVf9fMka9UTp3qDjGyvW5cBaVraWtWGjGIgOAuTneHsPqLefQSHjiWUIw5uFuyKPszr1MfJiyr89T4Hsu-2FV27d2U1A6igtCSahjJseWdBDmZiYyVxGnA?expiry=1716940800000&hmac=JAOshxWIS0BOeUD-p6VVz7uKs1ez9-K51fOMueHSS2U)

3. This opens the **Marketplace** menu. In the search bar, enter the acronym **gsod** and press enter.

4. Select the search result titled **GSOD**.

5. Select **VIEW DATASET** to return to the main workspace with the NOAA dataset tables in the **Explorer** pane. The **Details** pane now contains details about this dataset.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LLGoueF8QASTyn1MhZnDaA_3cff2f05095b4429b48410f16ab8e2e1_gLDm6lf1fM77XMb113lGaNQSwizfhYEDIr9AwC1SQxVQs_3uYcAq4mqhhW6vMOVYFrF-m9KJRtqPbIl9h90Phf41pHlth6RezQVuhb2wA-XUEsb5q8WQ2ycaWt9cXdbBmqfQstx7zxCVitUx8z6mVvs?expiry=1716940800000&hmac=ssyQr87zuXIJF9h1-EBvupWGDQFT8maN8KZeF-bjcIU)

**Note:** Many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.

# **Step 2: Query the data**

The meteorologists you’re working with have asked you to obtain the temperature, wind speed, and precipitation for stations La Guardia and JFK, for every day in 2020. They’ve also requested the data be presented to them in descending order by date and ascending order by Station ID. To return this information:

1. Select the **QUERY** button in the row of tab functions

2. Select the In **split tab** option in the drop-down menu.

3. Enter the following query into the Query Editor:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%209.png)

**Note:** This query uses the **IF** function to replace values 9999, 999.9, and 99.99 with **NULL**. The dataset description explains that these are the default values when the measurement is missing.

4. Select **RUN**.

Now you’ve run the query and gotten results. But these results aren’t saved anywhere, so each time you want to examine them, you would have to run this query again.

## 

# **Step 3: Save a new table**

In addition to the data the meteorologists requested, they also asked you some questions while preparing for the nightly news: They want to know the average temperature in June 2020 and the average wind speed in December 2020.

Instead of rewriting similar, but slightly different, queries over and over again, there is an easier approach: Save the results from the original query as a table for future queries.

To make this subset of data easier to query from, you’ll save this query as a table. First, though, you’ll create a new dataset to store the table.

1. From the **Explorer** pane, **select the three vertical dots** next to your project and select **Create dataset**. Note that unless you have specified your own project name, a unique name is assigned to your project by BigQuery, typically in the format of two words and a number, separated by hyphens (e.g., loyal-glass-371423 in the image below). You are not allowed to create a new dataset in the **bigquery-public-data** project.

A screenshot of the results of selecting the three vertical dots next to the project. The menu options are Create dataset and Refresh contents.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9Jt4u0FLQ4S3UHVXy6FwLw_12f81d0812d5446bb571a2c861b9f4e1_q2TNGlz_7xAAon8FGqa5HYSFcci-CXybKX6b1PixFZ7axnFz6-jXIwFB95gJdqBQxWrrnU2f-77ZCLFxtPdyK6NyQbisRWDxUHbXSu263Tn7XCzs2OZEDlPog01REL1gR_KON42HUVWUWORSVBlIXvc?expiry=1716940800000&hmac=shiUVGq_Yw7XJyxCSS0-XdkG1rdNT1GJKUWRFUuAH_M)

2. Enter **demos** into the Data ID box and set the **Location type** to **Multi-region,** then select **US (multiple regions in United States)**. Leave the rest of the **Advanced Options** as the default. Once you have done this, select **CREATE DATASET**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/YdzXsbm4TQy0WJOBGoOTXg_a64dbb7960ce4fbe87e3b21969012de1_dPxOZivTPoReQ-Zs_bjo4c2osocvb-PtGKk3DZwTGijA40Ou6R46xXL9GEUuJ6FfQpF8iE7WIFtPliQfon3JWi016itNZakRAoyVlY207ykRxkC2eOsN1eMkIpUxrB9sSkIudiO178GtDBE8udQONBM?expiry=1716940800000&hmac=FMx5jh6RNzcGzR1cufrAePGr8WTuc5x0SUT-XAyU-kc)

3. Open the new dataset.

4. Click on the **+ button** in the **Details** pane.

5. If needed, re-enter the query you ran in the previous section:

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%2010.png)

**Note:** Use the **IF** function to replace values 9999, 999.9, and 99.99 with **NULL**. The dataset description explains that these are the default values when the measurement is missing.

6. **Before** you run the query, select the **MORE** menu from the Query Editor and open the **Query Settings** menu.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ilYxpGXfRb6NLmCQFfDsWA_16d92c4f92854a67a15d0d23e90c93e1_sQjKqZ3Yl1GmmE7q8shyF8d2j-UbTyimjpH6W1HQLXfQa2jpgeX9qLoaPlpEUNAR8PV_GCZAh5Jhciy163iA3I1gO_AbtBwpL961QozpZuQKhyCuKJGW03EQWbWFQizdKxh2yWtXU9EwohOJeK150b0?expiry=1716940800000&hmac=BlpYHj9X2kC0QVfqqJTrV55KoUTSZZ-3lV5m7n2GvDo)

7. From the **Query Settings** menu, select the button next to **Set a destination table for query results**.

8. Set the dataset option to **demos** and name the table **nyc_weather**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G3EvV6JbRR6Wsg2IcCHqeQ_2419ebaa04dc4f3994cdb7b94a4ecfe1_9jalGmFfgJs59iNUaASWaDSjNo1Rszo09Zl0G1guP2td2hDKIKDrQ6p_LNQ7tujdCvPF65szYzI6qQq_VXTbl_mwW-Dh8HY5JhFV9Z9vdbRJ47tkN-Uv6X65xd4ce9P8Y2pW9uTLSGHz4Gzwoiqw-Ws?expiry=1716940800000&hmac=TYSDZG1qPnJHCSMtqE37tJ-3TEGXCgzm7UXz19HmZH4)

9. Run the query to save the results as a new table in the **demos** dataset.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AgtPKlZ_QAipty45LeK79w_b0cf4b485d9b4474888093d80ddf09e1_VPFLOz_GxxeVBOnkpFOF-5oC8bbB3lvdSpCZFMetNjwXuIDNqpnvuOecDcYUMz2GntFadPiARFsn-dC-5XUfXjLIUIu1HKxPibnVa_25zwFV7xd_cu8IOg-b8QK6VjBR61Ldn-YrJJpQxpHSQ9bEMO4?expiry=1716940800000&hmac=fUzVtFoXOxXcDzSH_sYLHwrw5QtrAvsFiGkkPVQ7GC8)

Before:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/c-zecsgCQKWxgVxnje7Ywg_02107a17cfe54bcb881cc674c20e9ce1_kHNZXLA8hKAm3aZEBEHCYFEUzAWU6_vhxm-MpoqYqRnB7y_nFQqQeHTjGGAnxsBdvTXsivcD8CXVBM3tIcCmu9--ncaMZZay6SpkZOSaZnEGBEqnRC4tw5LLjFaqH6E8qFl-8R9Y7Hw5dffcZrYcMeE?expiry=1716940800000&hmac=wMl4tReO7-jkrh1vx2rEUfWYPLbTzNVNWXGs87EwVCY)

After:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SFRsIhu_SD606NHx4Xx-AA_b66d09e0c8914c968ff0c8412f8295e1_WB-WPNCZQV_xPFkAUr2pz5el7TNAVwCREwnU91FnSS2J1CKrzgbYq2lWeli8-oWu8RUkzNpQYLU9nfsGCfJ80EwbTzs_nl7yNmMwONP5WiJ9dbCFS5QtfNbAEAV2uaqpG8mkS5xt9xndD5CogCga6bk?expiry=1716940800000&hmac=Ia15cP99FNL09llwVBD1akhgArqA1eb-I86C4T76fUI)

10. Return to the **Query settings menu** by selecting the **MORE** dropdown menu.

11. Reset the settings to **Save query results in a temporary table**. This will prevent you from accidentally adding every query as a table to your new dataset.

# **Step 4: Query the new table**

Now that you have the subset of this data saved in a new table, you can use the following query to find the average temperature in June 2020. First, replace **your_project_name** with your project name in BigQuery.

![Untitled](Sort%20data%20using%20SQL%206dd62bbb044c4c4f982eacf116e79d54/Untitled%2011.png)

**Note:** Format the beginning syntax to your project name before running this query. View the full Table ID by selecting on the **Details** tab of your new **nyc_weather** data table.

You can also use this syntax to find the average wind speed or any other information from this subset of data. Try writing a few more queries to answer the meteorologists’ questions.

The ability to save your results into a new table is helpful when you know you're only interested in a subset of a larger complex dataset that you plan on querying multiple times, such as the weather data for just La Guardia and JFK. This also helps minimize errors during your analysis.

---