# Learn more SQL calculations

---

# Queries and calculations

[index (31).mp4](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/index_(31).mp4)

**Key Points:**

- **Arithmetic Operators:** Both SQL and spreadsheets use the same arithmetic operators for addition (+), subtraction (-), multiplication (*), and division (/).
- **Query Syntax:** SQL calculations are embedded within queries, specifying the columns and operations to be performed.
- **Parentheses:** Parentheses are used to control the order of operations in both SQL and spreadsheets.
- **Modulo Operator:** The modulo operator (%) returns the remainder of a division calculation.
- **Functions:** Both SQL and spreadsheets offer functions for calculations, such as SUM and AVERAGE.
- **Aggregate Functions:** Aggregate functions perform calculations on multiple values and return a single value. Examples include SUM, AVG, and COUNT.

**Definitions:**

- **Operator:** A symbol that represents a specific mathematical operation.
- **Query:** A statement in SQL that retrieves data from a database.
- **Syntax:** The structure of a query, including specific keywords and commands.
- **Function:** A predefined block of code that performs a specific task.
- **Aggregate Function:** A function that performs a calculation on a group of values and returns a single value.

---

# Upload the avocado dataset to BigQuery

Using public datasets is a great way to practice working with SQL. Later in the course, you are going to use historical data on avocado prices to perform calculations in BigQuery. This is a step-by-step guide to help you load this data into your own BigQuery console so that you can follow along with the upcoming video.

## Upload the avocado dataset to BigQuery

In an upcoming video, the instructor demonstrates how to embed simple calculations in SQL. For this example, they use a publicly available Avocado Prices dataset from Kaggle. Follow the directions below to upload the avocado dataset to BigQuery. Once you’ve uploaded this data, you’ll be able to practice with this data on your own!

**Step 1:** Download the publicly available dataset [Avocado Prices from Kaggle.](https://www.kaggle.com/datasets/neuromusic/avocado-prices) This data has been made available by [Justin Kiggins](https://www.kaggle.com/neuromusic) under an [Open Data Commons](https://opendatacommons.org/licenses/odbl/1-0/) license. Kaggle is a great resource for all types of data analytics resources, and there are also other public datasets on the platform that you can download and use.

**Note:** You will need to create a free account before downloading the zipped data files.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VQ_upBbzS8GXuyISts5etw_21166c7518ca4127b5259bc1bca26bf1_7Ux7C3vkJz2XyEtOYvCjyQsOFOauR-5BGRsFi5E54S9zrzd7oEJduih9MlMhev23yCyBSzpa6G53GefdF8TeaBD3auC5mc6WhcuhR7cAgZ3IM1AbV_gBamN6L4tG_--GL7Nq07ebh1soKHGCbiiSBQ?expiry=1716940800000&hmac=1qIEBQoHiub_JHHMJePgUuDcsKPijyS5A6aOA77rQrI)

You will find some more information about the avocado dataset, including the context, content, and original source on this page. For now, you can simply download the file.

**Step 2:** Create the dataset.

1. After you have downloaded the dataset from Kaggle, extract the **zipped folder**. Remember where you save the avocado .csv file for upload into your BigQuery console.

2. Open your **BigQuery Console** and create a new dataset.

3. In the **Explorer** pane on the left side of your console, **select the project** where you want to add a dataset. Note that your project will have a unique name and won't be the same as the one in the example pictured below (loyal-glass-371423). If you already have it starred, don't choose bigquery-public-data as your project because that's a public project that you can't change.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/74w4hL1wRsahVDra1ftM0Q_203b3bfaaa994d05a16908151d5a2ff1_04wRStqiTc1T8PFxygEqbCeymb8LeDoeuQn6B25LIKzuMfjCiFYwhdbLCaaKF_MV6WTDeNLYfDH7_DSrhKrQyPWAwl3X1OSjUL5BDLdHGkOu7jqDVmL8d18gU6NXltcfaOngNQr9ylpBlZsbKmWMEw?expiry=1716940800000&hmac=O3UmSLlZ8YtulA_zxJCCugxz2wwJrF_OLcdkV18IvOg)

4. Select the **Actions** icon (three vertical dots) next to your project and select **Create dataset**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0Bc9Q9IrQ0Ovs8N-rbQ3tw_aedc7e029561445fb1b189f1d47ae0f1_50g1NXflV2z1EmXM_MlhD2T5e5cdbkUraOES6s-GZ9zCnj2G2WuIYBoNvN2yQU1hHXNI3jFHWFL3n5y3Bn4ah0y13Znd5IAld_fnnD7lzwmYSUw7s0CNxEDnVWUcC0_WpcNTU8UefKWrAxlGqs5wzA?expiry=1716940800000&hmac=Gb1Bm9PWG8mtGna8MwsQ2k3XMJN-1hNHBssDHS_akVo)

5. Name the dataset **avocado_data**. In the **Location type** section, select **Multi-region,** then select **US (multiple regions in United States**, and make sure the default **Encryption** method within the **Advanced options** is set to the **Google_managed encryption key**. Then, select **Create dataset** (blue button) to create your new dataset. This will add data in the **Explorer** on the left of your console.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jpq-PIqFTpe0CYz3fLllRA_136e40c8ba244563b66ab838d3eee1f1_Owme8LNQmXSV8O_S-7LccW_ADNdO2cP1EL0Mu1Vp1PQoSEjHZmdKYanf6gvvDp2o7-sLWu1gQpj9dibetsGQKxZn7pWCU_WOY-57g2oUpT8A6StZNzWZIPC-6PzY9WnhkKXl3znpKegXRRAmEkbk8Q?expiry=1716940800000&hmac=lz4EZaQEPpHWSx_Ri9bijUFV6xNCwXP7fgHGcpVbSKQ)

6. Navigate to the dataset in your console by expanding your project and selecting the correct dataset listed. In this case, it will be **avocado_data**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yuJtYAJrRpiUBxPW5nWHog_4266b30899024e669856d5d0537a9af1_pAJcUHIn4nrfLedq2oUKiUiVf0PsH80uE3Y1-l0IL5lMtmhoKfFVqC_Gvktban-IEdA3OWPr9V_4CMyOD_dH8ojolZUvqVsxA46SWxQiU4dvxM46eUAhGsCWoiJmt9IWnRDl8ikiM0gIP4zdHg0evA?expiry=1716940800000&hmac=uYACO4nSwYVNlI_qhPu116h3GGz9vH9GYH01xUb8Nzc)

7. On the far right of the screen, select the blue **+ CREATE TABLE** button to open the Create table window. To fill out this window:

- Under **Source**, for the Create table from selection, select **Upload**.
- Click **Browse** to select the unzipped .csv file titled avocado you just downloaded to your computer from Kaggle. The **File format** should automatically change from **Avro** to **CSV** when you select the file.
- For **Table** name, enter **avocado_prices.**
- For **Schema,** click the **Auto detect** checkbox.
- Finally, to create the table, select **Create table** (blue button).

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/eDo_6E6KSFqpnWUTxupyGw_e1fd04335fb24eeb8f88fbcb5ab968f1_XogZ-aqGyc8doDbJ9x_jlWI0yg-96bwV90jNwY27eVW7xWRy51P4FCv_xy1KkZ62JdQomRdFP7u5qgaXXou7pzG_gjm9gq4U0q2oL2p_OgPIvep1IU58ffcV58p34Dc1uZLO8xLsCHXTZWIOZieAtQ?expiry=1716940800000&hmac=sXLBkPJ1JYVMpjX-9N83dgUIbScywRNBANQwFK6yvwA)

**Step 3:**  Review the table information.

1. In the **Explorer**, the **avocado_prices** table will appear under the dataset you created.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/OwLOZTMySSuQejywkPtNLQ_8f21c885863641499aaf284b7b98f1f1_9jqzuQ6yzHVNrkc3NeB9EyZtk58GG5oVv_zkCGS80FRRvleUrBvB7-Z5Iie-6Tm3lqXUthHosFtrpDmGD4Nn-HL8pE5ASgcT8oUIJ7Dai9Lmii2THT6Xs2-XHibA0PLoYQhIMvRVMBbDFx4J6IuqEg?expiry=1716940800000&hmac=kIkmduZ7oIDR_qwgns7pBIZzNIeJye6dvrueIBQdzWY)

2. Select the table you created to develop a greater understanding of the table schema, details, and the data preview in the main editor window.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ALAi3iL_Sg2dikRxhJ6ZTg_89566e3d5fde4ab0b711072e9b0ffdf1_SwqTYcMuFw0SNdlLvn6JS9azcS334AhjQ6c4wGe3mfEv47GWO4EDbHczNCJqgmuniMQc5hcrPn1MVHc5HInQri3mxyoh5NBYCcQGBtgfkScBW0CoOaGIlIK4kVMH5cyBgciTQEoXaE8fJPrSKYSDrA?expiry=1716940800000&hmac=E5tJHF4uEQtbWEGH7wmgyior5L6WTG3X4YTbXlRbpjw)

Well done! You are now ready to follow along with the video and learn more about performing calculations with queries!

---

# Step-by-Step: Embed simple calculations with SQL

[index (32).mp4](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/index_(32).mp4)

This reading outlines the steps the instructor performs in the next video, [Embed simple calculations with SQL](https://www.coursera.org/learn/analyze-data/lecture/RlnmJ/embed-simple-calculations-in-sql). In this video, the goal is to find out the total number of bags of avocados sold on each date at each location using the dataset you loaded to BigQuery.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

In order to follow along with the instructor, you will need the [avocado dataset](https://www.kaggle.com/datasets/neuromusic/avocado-prices) uploaded into your project space. If you haven’t already uploaded this data, follow the instructions in the [Upload the avocado dataset to BigQuery](https://www.coursera.org/learn/analyze-data/supplement/Y6c0d/upload-the-avocado-dataset-to-bigquery) reading.

## Example 1: Verify the total number of bags

Use the following steps to perform some simple calculations with SQL and verify the total number of bags.

1. Open the BigQuery editor.

2. On line 1, enter **SELECT** and press **Enter**. You'll use the **SELECT** command to pull certain columns from the table. Because you are selecting several columns, press **Enter** after **SELECT** and after the comma after each column name.

3. Enter the following column names into your editor:

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled.png)

4. Note the use of underscores in this example. Spaces can confuse certain servers and applications. Using underscores helps avoid potential issues while keeping the names readable.

5. Now add the calculation to the query using the names of the three columns with plus signs between them, as shown below. Add **_Calc** to your new column to compare the columns to each other after you calculate your results.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%201.png)

6. Finally, finish the query with **FROM** and the names of your project, database, and table: **your-project.avocado_data.avocado_prices**. Note that **your-project** is unique to you. If you haven't named it yourself, BigQuery assigns a name for you, typically in the form of two words and a six-digit number, each separated by a hyphen (for example, **loyal-glass-371423**). In the code examples throughout this reading, be sure to replace **your-project** with your unique project name. 

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%202.png)

7. Select **RUN** to run the query. Your query should return a table containing seven columns, as pictured here.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ueHMTZf7QvWFPfVu2diRiw_a082241b27e043f494d770f545c580f1_DA_C5M4_step-by-step_embed_simple_calculations_1.png?expiry=1716940800000&hmac=uNZdr7Bxpn32CmMEDPJdMq-eb65z5pW3mTpb9ScvaB4)

## Example 2: Calculate the percentage of small bags

Now that you have verified the total number of bags, you can use those values in another query. You need to find what percent of the total number of bags were small bags. This information might help stakeholders make decisions about how to package avocados or which size bag to run a sale on. Run a new query to calculate the percentage of small bags:

1. Create a new query.

2. Use the **SELECT** command to select the **Date**, **Region**, **Total_Bags**, and **Small_Bags** columns.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%203.png)

3. To find the percentage of small bags, divide the number of small bags by the number of total bags using a slash (**/**) as the operator. Put this part of the calculation in parentheses to let the server know that this calculation should be performed first. Then add ***100** to give a percentage versus a decimal.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%204.png)

4. Use the **AS** command to name this new column **Small_Bags_Percent**.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%205.png)

5. Add **FROM** and the dataset.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%206.png)

6. Select **RUN** to run the query.

7. The "division by zero" error is the result of values of zero in the **Total_Bags** column when used to calculate the percentage in line 6. Add a step to solve this. Use the **WHERE** command. **WHERE** lets you add a condition to your calculation. In this case, specify to perform the selection only on rows where the total number of bags does not equal zero: **WHERE Total_Bags <> 0**.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%207.png)

8. Select **RUN** to run the query again. Your query should return a table containing five columns, the last one being the one you created: **Small_Bags_Percent**, as depicted in the following screenshot. Notice your new column shows the percentage of the total bag count that is made up of small bags.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WPIfIJOfQiGCUlzfN5uazA_20afbb88a3c046c18cafc166ed2cdaf1_DA_C5M4_step-by-step_embed_simple_calculations_2.png?expiry=1716940800000&hmac=pTtYyX0cqkYae6JP3580Hknm0FNIXcwd37nz1Ih4M8o)

With SQL, you can complete just about any calculation you want during your analysis. Embedding the calculations in your queries will help you keep your analysis organized while getting your results. The methods shown here are just the beginning!

---

# Calculations with other statements

[index (33).mp4](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/index_(33).mp4)

**Key Points:**

- **Grouping Data:**
    - The `GROUP BY` command groups rows with the same values from a table into summary rows.
    - It is used with `SELECT` statements and comes after the `WHERE` clause (if present).
- **Organizing Data:**
    - The `EXTRACT` command extracts a specific part of a date (e.g., year, month, day).
    - The `ORDER BY` command sorts the results of a query in ascending or descending order.
- **Calculating Data:**
    - Aggregate functions like `COUNT` and `SUM` are used to perform calculations on grouped data.
    - Calculations can be included in the `SELECT` statement along with the grouped columns.

**Example:**

The video uses the example of analyzing bike-sharing data to demonstrate these concepts. The goal is to find the total number of rides taken each year.

**Code:**

```sql
SELECT
    EXTRACT(YEAR FROM start_time) AS year,
    COUNT(*) AS number_of_rides
FROM
    bigquery-public-data.new_york.citybike_trips
GROUP BY
    year
ORDER BY
    year;

```

**Explanation:**

1. `EXTRACT(YEAR FROM start_time) AS year`: Extracts the year from the `start_time` column and creates a new column named `year`.
2. `COUNT(*) AS number_of_rides`: Counts all rows in the `start_time` column and creates a new column named `number_of_rides`.
3. `FROM bigquery-public-data.new_york.citybike_trips`: Specifies the table from which the data is retrieved.
4. `GROUP BY year`: Groups the data by the `year` column.
5. `ORDER BY year`: Orders the results by the `year` column in ascending order.

**Output:**

The query returns a table with two columns: `year` and `number_of_rides`. Each row represents the total number of rides taken in a specific year.

**Additional Notes:**

- The video also mentions the importance of data validation and how SQL can help ensure data accuracy.
- This is just one example of how to use `GROUP BY` and `ORDER BY` in SQL. There are many other ways to use these commands to analyze data.

**Definitions:**

- **Aggregate function:** A function that performs a calculation on a group of values.
- **Data validation:** The process of ensuring that data is accurate and complete.
- **Group by:** A command that groups rows with the same values from a table into summary rows.
- **Order by:** A command that sorts the results of a query in ascending or descending order.
- **SQL:** A programming language used to manage and analyze data in relational databases.

---

# Hands-On Activity: Calculations with SQL

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/eC7zcJs_R3KJ6f97UY7_Cg_626dcd1cc90249bfa8d70d080088d4f1_Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716940800000&hmac=J26DyKMw7k3cwE8veR3xWtJUjRliD7_W-MMdW4xGpXk)

Previously, you learned about basic calculations with SQL. Just like spreadsheets, you can use the four basic arithmetic operations to perform addition, subtraction, multiplication, and division. Now, you’ll practice writing basic calculations using single and multiple operators in Bigquery. This will enable you to combine multiple arithmetic operations in a single query, allowing you to quickly and efficiently discover significant patterns in  your data.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the question at the end of the activity before going to the next course item.

# **Step 1: Access the dataset**

For this activity, you’ll analyze subway ridership data to help improve the quality of the city’s public transportation. To do this, you’ll use data that describes the average weekly subway ridership in New York City from 2013-2018.

1. Navigate to your [BigQuery console](https://console.cloud.google.com/bigquery).

- **Note:** BigQuery Sandbox frequently updates its user interface. The latest changes may not be reflected in the screenshots presented in this activity, but the principles remain the same. Adapting to changes in software updates is an essential skill for data analysts, and it’s helpful for you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.

# **Step 2: Examine the dataset**

1. Locate the public data by **typing** the word public in the **search bar**. Select **SEARCH ALL PROJECTS** and **SHOW MORE** to access all of the public datasets.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Hv2RUEKTQcutTyrMnRMdpA_5bfacd11bf4a40809f012490d56686e1_QnRh_eJwgXpSlby7Jq2pv1--4L-bUz3WhQl3nbPzzXKYRtG1-WVlCoIiY5eyFPFLfbgCXmd19nnJBYXtlAR4jMXA9BR75Mvve2Snc1HOvqGwLQb7fz7KvZiPNI-JdWS0zeHlQ1u-A7MHMSjiur4x3ZnXEhmnwVDzE5qioyPC_3TeJEl2XbveE9D1NL3LNA?expiry=1716940800000&hmac=b1nTDYCm5DaxcUj8qLDnJFmAwJuT1M7CmZNHDo_Z6N4)

2. Select the **star icon** next to bigquery-public-data. This will pin it to the Explorer menu.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EO0J0t6ETe2Ck9A4X2qJsA_9860d8eefafd4dc98ef114e7e91b63e1_3U0WdsiCcpeUr2kHVMGw1AOcHQf13BrPtULwCsh_ZCTga13rHdIBUVabJ4Q-clHWHDsy1-3UVui9xt7tWlPhh3MISlNv0TF-8W4_RhxUKn2x4jElf4VYFomGkKVjOGGsNlPHQqx7qotNUZ8wW49ClKjGuHoc2SXKH_iQw5Y_c2Jb6kaKdxs-P0LlUe2SN4c?expiry=1716940800000&hmac=8hNOmV2MjbKcuens5-7fG7ZtY1ix-oFBE-8ef3vQ5xc)

3. Select the **dropdown arrow** next to the bigquery-public-data to expand all the available datasets.

4. Navigate down the list until you find the **new_york_subway** dataset. **Note:** You may have to select the **SHOW MORE** button twice to reach the correct dataset. Now, select the **dropdown arrow** next to new_york_subway and select **subway_ridership_2013_present**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/chaTD_XJThCKgzTTGNCMnQ_bd4487b5160740179bdc2897fdbd21e1_cgCuTR4nBqGwZOEk9oJnjgRfYWJBuZsHfh4VE8f78cy-MPxhMw5RhDM-lFixqmYrBaoeQ_URL4J18H1qIgYaTMh0HCBfcXqKhBDBEA9IHeUhOsHslK2zINuxRuOteqXTHXFpqXszJb0ktVHVtkd1xrI8bq3VQMKiZmsO42JssA-oHqSGYbVH86CYm2S39VI?expiry=1716940800000&hmac=IX7iTh8UMo-UbpXi4eBaHohS7sENDa7CculTLyg3itg)

**Note:** This dataset may not be accessible through other search methods. Follow the previous steps to locate the correct data for this activity.

Note also that any of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.

# **Step 3: Use a calculation with a single operator**

First, identify data exploring the change in weekly ridership from 2013 to 2014. Use SQL to subtract the number of riders in 2013 from the number of riders in 2014.

1. Select the **dropdown arrow next to QUERY** and select **In split tab**. You will then be able to see the Query editor and the datasets. If you prefer to only see the Query editor, you could select **In new tab**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uklRfGhRTG2VD8VpVYNw8w_67a27c6219984a2e99ffec424bc7a8e1_oCFj-UQfq8tnR_fRj2S3Ad4CdfgnYvyA7ruq5DeG2hOknh0RvUdmCfg3I_ULDvINrmhImdWWv91r9g3L7BJQ1OTZPThAMMSwqDMzLSxvFQTbVtNpOo9XEEfXTUBfxbg3-78zyci3qGEcVLNskjpPLbz4K-kjY-bARtgDNRWjY4lPY_oZGZJ-BYOm8gbR-gg?expiry=1716940800000&hmac=4wypsA84pRdhq7LhWr3Ym6kKl5Uypk3EqNfeMark0Ac)

2. In the Query editor, add the names of the columns you want to use in your calculations in your **SELECT** statement. In this case,  select the following columns:

- station_name
- ridership_2013
- ridership_2014

Be sure to add a comma after each column name. 2. Add the calculation to the query by adding the names of the two columns with a minus sign between them.

- ridership_2014 - ridership_2013

3. List the result in a new column. To do this, enter **AS** followed by the new column’s name. Name it **change_2014_raw** because it represents the change in ridership from 2013 to 2014 in raw numbers.

4. End your query with the **FROM** command and the name of the dataset and subset you’re pulling data from. After **FROM**, select **Enter** or **Return** and enter **bigquery-public-data.new_york_subway.subway_ridership_2013_present**.

![Untitled](Learn%20more%20SQL%20calculations%20ac1bba709fdc41078b0e35a82d5ba5a9/Untitled%208.png)

5. Select **RUN** to get the results.

The results show the change in ridership from 2013 to 2014 at different stations. For example, the Atlantic Av - Barclays Ctr station gained an average of 1,774 riders per week. The 4 Av station lost 321 riders.

By including a basic calculation in your query, you can quickly gain important knowledge about your data. In this example, you now have insights into the change in ridership for each subway station in any given year.

Query results showing Row 1, Atlantic Av - Barclays Ctr, ridership 2013 is 39871, ridership 2014 is 41645, change 2014 raw is 1774; Row 2, 4 Av, ridership 2013 is 13156, ridership 2014 is 12835, change 2014 raw is -321; Row 3, 14 St/6Av, ridership 2013 is 49316, ridership 2014 is 49990, change 2014 raw is 674; Row 4, Jamaica - Van Wyck, ridership 2013 is 4992, ridership 2014 is 5121, change 2014 raw is 129; Row 5, Crown Hts - Utica Av, ridership 2013 is 27780, ridership 2014 is 28287, change 2014 raw is 507.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9H7_IQk7Sa6uPk32eKPxcw_e8424af28dee4f05a76a9c5c64c3d4e1_htB4q0zpcWBrR9Ykzkm32R76NtCodoYS86W1I078m8EhSupRVQkc0DffNtO3K0vYNFIB8z7tpTsgTnKOyyKgbhQToA2aOHIZF5OT6hgmF-_OyLLXX9Wq04aMuN9d0j72Sn-cTqINu-uhc0m4TNBPABTVUsu3zkHl-M3dCJFKROGJ_k8t2TYc1F5UiuSxvoA?expiry=1716940800000&hmac=s77iAuqsqymxggUFQ3uOv1cNfPnwbK25ELkDEulUDEo)

# **Step 4: Use a calculation with multiple operators**

Next, find the average weekly ridership for a longer period of time, such as the multi-year period from 2013-2016.

To do this, combine multiple arithmetic operations in a query. The average of a set of numbers is the sum of the numbers divided by the total number of values in the set. There are four values in your new set (ridership data for 2013, 2014, 2015, 2016). Use SQL to sum the numbers for each year and divide that sum by 4.

1. Select the **COMPOSE NEW QUERY** button to refresh the query editor.

2. Enter **SELECT** to select the columns you want to pull from the table. You’re selecting several columns, so press **Enter** or **Return** after **SELECT** and add a comma after each column name. The columns selected for this query will be:

- enter station_name
- ridership_2013
- ridership_2014
- ridership_2015
- ridership_2016

3. Add the calculation to the query. Use parentheses to control the order of the operations if you use more than one arithmetic operator in a calculation. In this case, sum the years, then divide the sum by 4. Put parentheses around the sum of the four column names. Enter **(ridership_2013 + ridership_2014 + ridership_2015 + ridership_2016)**. Then enter a division operator **/** and the number **4**.

4. List the result in a new column by entering **AS** followed by the new column’s name. Name the new **average** because it represents average weekly ridership for the period 2013-2016.

5. End your query with the **FROM** command and the name of the dataset and subset that you’re pulling data from. After **FROM**, select **Enter** and type **bigquery-public-data.new_york_subway.subway_ridership_2013_present**.

Query data listed as 1. SELECT; 2. Station_name; 3. ridership_2013; 4. ridership_2014; 5. ridership_2015; 6. ridership_2016; 7. (ridership_2013 + ridership_2014 + ridership_2015 + ridership_2016) / 4 AS average; 8. FROM; 9. bigquery-public-data.new_york_subway.subway_ridership_2013_present

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hlExe2qbQESE59LnIH-ecw_cac74a838af24b619fdeb45f29c6b8e1_3B2yTSkmeyBdOISuzuQjWNeGgvohlJ5kq0fMOn_bYS1G75kP2BkPmGXsGfZuNo0yS5nvby-6FnjdlCuF0FXQ-2v68vKPktOQHLlDX5ARcPpy0vQqs85Vmik7iBgK20jK3nsq0uSVjz_SfwyDEe4wxKAPfwxL_4FmJtR4eBMONQcRI7IMCHBn-P00JAe24qU?expiry=1716940800000&hmac=LJTT5SMPtm4X2SKn2K31zScjHlTfH7JKBXjQ8jPg-0o)

6. Select **RUN** to get the results. The results clearly show the trend in ridership at each station from 2013 to 2016. For example, weekly ridership at the Atlantic Av - Barclays Ctr station increased every year since 2013. Further, for the years 2014, 2015, and 2016, weekly ridership at Atlantic Av - Barclays Ctr exceeded the overall average for the period 2013-2016 (listed in the average column).

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MJ1YsDR2RAyu7IN9eMLgHw_b980b3213dfb42358480e9f4ea1366e1_biYNO-dvj7_rCx-PBpD-SI6LmWY2Ey3ym0KrcgeVYw3LIKQD_YyNMRC_Z4er_9DJLayK8f6Fsh151W1LV7lSGPhh90OS4DZhQX4aAUTch9CWISkBqOGUzmrqrglLiHGb3JHyUYq8vFXFQKol79uqRlAXLAOGXIPxjFVWF2CLuDGyDUcfZCM8jO7EphaL9mk?expiry=1716940800000&hmac=qRBeE1wF8AwtfdcYX0CUDwxZVBmM_OiAorNChuOR48w)

This kind of data is useful for managing public transportation. It can help you determine which stations or routes to expand due to increased ridership. Using basic calculations in your query allows you to quickly discover significant patterns in your data.

---