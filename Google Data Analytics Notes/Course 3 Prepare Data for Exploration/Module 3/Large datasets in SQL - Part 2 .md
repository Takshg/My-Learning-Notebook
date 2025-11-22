# Large datasets in SQL - Part 2.

---

# In-Depth Guide: SQL Best Practices

[UwaGyGQoRLu9Dw_8BLUTiQ_4d31c4c09dc54520835973c4ac8240f1_DAC3-In-depth-guide_-SQL-best-practices.pdf](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/UwaGyGQoRLu9Dw_8BLUTiQ_4d31c4c09dc54520835973c4ac8240f1_DAC3-In-depth-guide_-SQL-best-practices.pdf)

---

# Guided Project

[world_cities.csv](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/world_cities.csv)

## Overview and Import Data in BigQuery

[Guided Project- Overview and Import Data in BigQuery.mp4](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/Guided_Project-_Overview_and_Import_Data_in_BigQuery.mp4)

## Identify the cities that match the temperature requirements

[ae9a47a1-db04-4f3c-be45-f67bee0ec3fb-20220715005501-3663122b-e160-4ed1-a191-2df78b7a3801-video.mp4](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/ae9a47a1-db04-4f3c-be45-f67bee0ec3fb-20220715005501-3663122b-e160-4ed1-a191-2df78b7a3801-video.mp4)

## Narrow down cities based on commute times

[bc3704e5-e075-481c-b219-1f2e4f309c2d-20220630081159-34661f6f-57b8-45bd-b1b2-819e9969481f-video.mp4](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/bc3704e5-e075-481c-b219-1f2e4f309c2d-20220630081159-34661f6f-57b8-45bd-b1b2-819e9969481f-video.mp4)

## Narrow down cities based on happiness average ranking

[57fa7e2d-b549-4413-aa18-a4b67ef0150b-20220630082959-f9d60a2b-3bde-4a45-8857-fd2b8b019de6-video.mp4](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/57fa7e2d-b549-4413-aa18-a4b67ef0150b-20220630082959-f9d60a2b-3bde-4a45-8857-fd2b8b019de6-video.mp4)

## Analyze alternative sources

[7ef3453d-3898-45c6-b212-f351c46b88ae-20220715004401-20e3030f-f427-4623-8cf7-a7cdbc6c94bd-video.mp4](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/7ef3453d-3898-45c6-b212-f351c46b88ae-20220715004401-20e3030f-f427-4623-8cf7-a7cdbc6c94bd-video.mp4)

---

# Hands-on Activity: Create a custom table in BigQuery

## Activity Overview

Recently, you’ve been thinking about identifying good data sources that would be useful for analysis. You also spent some time in a previous activity exploring a public dataset in BigQuery and writing some basic SQL queries. In addition to using public data in BigQuery, your future data career will involve importing data from other sources. In this activity, you will create a custom table and dataset that you’ll load into a new table and query.

By the time you complete this activity, you will be able to load your own data into BigQuery for analysis. This will enable you to import your own data sources into BigQuery, which is a skill that will enable you to more effectively analyze data from different sources.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the data source**

To get started, download the baby names data zip file. This file contains about 7 MB of data about popular baby names from the U.S. Social Security Administration website.

Select the link to the baby names data zip file to download it.

Link to baby names data: [names.zip](https://storage.googleapis.com/gwg-content/gdac006/names.zip)

# **Step 2: Unzip the file**

Unzip the file you downloaded onto your computer to access it on BigQuery. Once you have unzipped the file, find a .pdf file titled NationalReadMe that contains more information about the dataset. This dataset tracks the popularity of baby names for each year; you can find text files labeled by the year they contain. Open **yob2014.txt** to preview the data. You will notice that it’s a .csv file with three columns. Remember where you saved this folder so you can reference it later.

# **Step 3: Create a dataset**

Before uploading your .txt file and creating a table to query, you will need to create a dataset to upload your data into and store your tables.

1. From the BigQuery console, go to the **Explorer** pane in your workspace and **select** the three dots next to your project to open a menu. From here, select **Create dataset**. Note that unless you have already specified your own project name, a unique name is assigned to your project by BigQuery, typically in the format of two words and a number, separated by hyphens (e.g. loyal-glass-371423 in the image below).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G-8fKPNxSNugFEQNHK8uKQ_f77b37bcd01747d89888505ae8bb60e1_C3M3L5_A_03_Graphic01.jpg?expiry=1716768000000&hmac=zvPTk5LyB84PkjViekVheIIlXoWvmHUx9RrLDMLcGDk)

2. This will open the **Create dataset** menu. This is where you will fill out information about the dataset. Input the **Dataset ID** as **babynames** and set the **Data location** to **Multi-region (US)**. Once you have finished filling out this information, select the blue **CREATE DATASET** button at the bottom of the menu.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dGqcLb00RA-znOckm9rPnQ_64045ede39684651975678db460c0de1_C3M3L5_A_03_Graphic02.jpg?expiry=1716768000000&hmac=00hvsM1POQqDsOVkx4f6OURQ4CEOZBIhahD6zsL0xzk)

# **Step 4: Create a table**

Now that you have a custom database stored in your project space, this is where you will add your table.

1. Select the newly created babynames database. Check the tabs in your **Dataset info** window and select the first blue **+ CREATE TABLE** button. This will open another menu in your console.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NvqI9MlPRfy12eWbv4S-QQ_4510b10fcb144852a3f18a2191b6a8e1_C3M3L5_A_03_Graphic03.jpg?expiry=1716768000000&hmac=4jpY-tiVlfzGS6ODi_o2SrcN_heigbNXHOyo51aDbWo)

2. In the **Source** section, select the **Upload option** in **Create table from**. Then select **Browse** to open your files. Find and open the **yob2014.txt** file. Set the file format to **.csv**. In the **Destination** section, in the **Table data** box, name your table as **names_2014**. For **Schema**, select **Edit as text** and input the following code:

![Untitled](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/Untitled.png)

3. This will establish the data types of the three columns in the table. Leave the other parameters as they are, and select **Create table**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/H1Hs9EoBQ7W2OPmiS60ugQ_034df5f035d14c1aa75b79401033f9e1_C3M3L5_A_03_Graphic04.png?expiry=1716768000000&hmac=LAbpOryNh2se0H6aIKvahp6Tw6B61BA3iXiDFoAVpYU)

Once you have created your table titled **names_2014**, it will appear in your explorer pane under the database **babynames** that you created earlier.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/amrBg-lGSDaM-vcYDZdP9g_4041448e4d2348e594a5d1540afed4e1_C3M3L5_A_03_Graphic05.jpg?expiry=1716768000000&hmac=ZQe2v7yMlHvkag__LDwOOKxDlZSWZLXh30Y92uYRiOs)

4. Select the table to open it in your workspace. Here, you can check the table schema. Then, go to the **Preview** tab to explore your data. The table should have three columns: **name**, **gender**, and **count**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xzbqviAOS2SJov93oSTs_A_a906a2e0dfb043778efff173c08117e1_C3M3L5_A_03_Graphic06.png?expiry=1716768000000&hmac=pEeB5Vys1xJujS0Fph7TObubiyFUkwPDf0mUQtoQEwA)

# **Step 5: Query your custom table**

Now that your table is set up, you’re ready to start writing queries and answering questions about this data. For example, let’s say you were interested in the top five baby names for boys in the United States in 2014.

Select **COMPOSE NEW QUERY** to start a new query for this table. Then, enter this code:

![Untitled](Large%20datasets%20in%20SQL%20-%20Part%202%201c1f70208c454d4e9c2538fe266403fc/Untitled%201.png)

**NOTE:** Making sure that your **FROM** statement is correct is key to making this query run! The database needs the query to tell it the location of the table you just uploaded so that it can fetch the data. It’s like giving the query a map to your table. That map will include your unique BigQuery project name (replace **your-project** in the code above with your unique project name), the database name (**babynames**), and the table name (**names_2014**). The location names for each of these elements are separated by periods. The final result will be something like this:

**loyal-glass-371423.babynames.names_2014**

Note that **loyal-glass-371423** is just an example of a project name. You must use your project’s name in your **FROM** statement.

This query selects the **name** and **count** columns from the **names_2014** table. Using the **WHERE** clause, you are filtering for a specific gender for your results. Then, you’re sorting how you want your results to appear with **ORDER BY**. Because you are ordering by the **count** in descending order, you will get names and the corresponding count from largest to smallest. Finally, **LIMIT** tells SQL to only return the top five most popular names and their counts.

Once you have input this in your console, select **RUN** to get your query results.

---

# Hands-on Activity: Choose the right took for the job

## Q1: Identify top 10 pet supply products

You are a junior data analyst at a major online pet supplies business. The product development department has asked you to identify the top 10 products with the highest sales in the last month so that they can decide what types of products to develop next. These products come from multiple tables within the company’s database: one containing product details and another with sales data.

### Reflection

Consider whether you would use a spreadsheet or SQL in the scenario above.

- Which tool would provide the desired output?
- Which tool is appropriate considering the dataset’s size and complexity?
- How will you access the data?

Now, write 2-3 sentences (40-60 words) in response to these questions. Identify which tool you would use and then justify your thinking. Enter your response in the text box below.

Ans: 

In this case, I would use SQL to determine which pet supply products sold the most in the previous month—the top ten. Given the size and complexity of the dataset, SQL is suitable because it makes searching and merging numerous tables quickly possible. Since SQL retrieves data straight from the company's database, it guarantees accurate and scalable analysis.

## Q2: Determine new store location

In this scenario, you work for a small fitness tech company. Your manager has asked you to determine which cities have a large population of customers; this will help them decide where to build the next retail store. You have a .csv file with 300 names, phone numbers, and addresses. The manager also requested a quick, simple visualization, such as a bar chart, so the team can make some quick comparisons.

### Reflection

Consider whether you would use a spreadsheet or SQL in the scenario above.

- Which tool would provide the desired output?
- Which tool is appropriate considering the dataset’s size and complexity?
- How will you access the data?

Now, write 2-3 sentences (40-60 words) in response to these questions. Identify which tool you would use and then justify your thinking. Enter your response in the text box below.

Ans: 

In this case, I would identify the cities with a large customer population using a spreadsheet. With only 300 entries in the dataset, a spreadsheet is suitable for rapid analysis and visualization. The .csv file imports into the spreadsheet easily, allowing me to use built-in functions to aggregate the data by city and quickly construct a bar chart for comparisons.

## Q3: Customer satisfaction survey results

The marketing team of a fashion retailer conducted a survey on customer satisfaction. The results are in a .csv file. The team wants to calculate the average satisfaction score and compare it to the average score from their last survey. They also want to segment responses based on demographic data such as age, gender, and location. This segmentation will enable the marketing team to tailor their marketing strategies to meet the specific needs and preferences of various customer groups.

### Reflection

Consider whether you would use a spreadsheet or database in the scenario above.

- Which tool would provide the desired output?
- Which tool is appropriate considering the dataset’s size and complexity?
- How will you access the data?

Now, write 2-3 sentences (40-60 words) in response to these questions. Identify which tool you would use and then justify your thinking. Enter your response in the text box below.

Ans 

In this case, I would examine the findings of the customer satisfaction survey using a spreadsheet. Since the dataset is probably small in size, segmenting the data based on demographics and computing average scores should be done using a spreadsheet. By importing the.csv file into the spreadsheet, I can quickly access the data and utilize pivot tables and the spreadsheet's built-in features for in-depth analysis and comparison.

## Q4: Calculate course completion rates

The manager of an online education platform wants to know which courses have the lowest completion rates so that they can invest in course enhancements and more targeted student support for those courses. The data is stored in a relational database with separate tables for user registration, course enrollment, and course completion.

### Reflection

Consider whether you would use a spreadsheet or database in the scenario above.

- Which tool would provide the desired output?
- Which tool is appropriate considering the dataset’s size and complexity?
- How will you access the data?

Now, write 2-3 sentences (40-60 words) in response to these questions. Identify which tool you would use and then justify your thinking. Enter your response in the text box below.

Ans 

In this case, I would calculate course completion rates using a database. Because of the quantity and complexity of the dataset, which consists of several connected tables, a database is suitable for effectively joining and querying the data. To extract and analyze completion rates from the data, I would use SQL queries. I would then identify the courses with the lowest completion rates so that they might be improved.

---

# Hands-on Activity: More practice with SQL

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G-KePoi0R2Sinj6ItBdkMg_2d69ab4b929f40f2b472a78fdd5ed880_line-y.png?expiry=1716768000000&hmac=CeqQp9OlOJjkjSa1uMgNmoqdrr_9m1kfNF3jy5KL9CA)

In previous lessons, you learned how to work with data in spreadsheets. Now, you’ll practice using SQL to work with data in databases. By the time you complete this activity, you’ll be able to use SQL to write queries that retrieve data from databases. Further, you’ll practice navigating large public datasets in BigQuery in order to become proficient in SQL queries—an essential skill for your future career as a data analyst.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

In this activity, you’ll query a public dataset that contains information about the trees in New York City in 2005. You’ll also use the **AVG** function to determine the average diameter of all NYC trees in 2005. You’ll then have the opportunity to write queries using the data for 1995 and 2015 to compare the average tree diameters.

# **Step-By-Step Instructions**

# **Step 1: Set up your Data**

1. Log in to [BigQuery Sandbox](https://cloud.google.com/bigquery/docs/sandbox). On the BigQuery page, click the **Go to BigQuery** button.

If you have a [free-of-charge trial version of BigQuery](https://cloud.google.com/bigquery), you can use that instead.

**Note:** BigQuery Sandbox frequently updates its user interface. The latest changes may not be reflected in the screenshots presented in this activity, but the principles remain the same. Adapting to changes in software updates is an essential skill for data analysts, and it’s helpful for you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.

2. If you haven’t done so already, **create a BigQuery project**. (If you have a project, select it in the **Explorer** pane.)

a. In the BigQuery console, select the dropdown list to the right of the Google Cloud logo to open the **Select a project** dialog box.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/U9FyR-WYTM-kzqpn1SNPqg_e46ca36da11f4b2d8c641ac8e451a2e1_Create-a-Project.png?expiry=1716768000000&hmac=QwySWQs7my3LIefakLRRsobId9AB9pi40VYpH7XAI20)

b. In the **Select a project** dialog box, select the **CREATE PROJECT** button.

c. Give your project a name that will help you identify it later. This can be a unique project ID or use an auto-generated one. You do not need to select an organization.

d. Select the **CREATE** button to create the project.

3. The three main sections of BigQuery are now onscreen: the **BigQuery navigation menu**; the **Explorer** pane, which you can use to search for public datasets and open projects; and the **Details** pane, which shows details of the database or dataset you’ve selected in the **Explorer** pane and displays windows for you to enter queries.

Notice that you can use the <| symbol in the BigQuery **navigation** menu section to collapse it. There is a similar symbol to collapse the **Explorer** pane.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z_MK2nFQQfStUyMhqKBNXQ_6395321552a14d84b27c927132c1fce1_BigQuery-UI.png?expiry=1716768000000&hmac=OUFwSh1mIWw2qDrEzqAVpk0L-WpssGBEaDUpoJvOlPU)

# **Step 2: Choose a dataset**

Follow these steps to find and select the NYC Trees dataset for this activity:

1. In the **Explorer** pane, select the **+ ADD** button.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/b0GUyPFlQiW4JIiydNYuXw_068cb7be5bc34538a48274e2bb36cfe1_C3M3L5_A_06_Graphic01.png?expiry=1716768000000&hmac=tH5q8_GVb5Boh_gjVPko1ilrkiiy8XiZ002fNeqCqAE)

2. In the **Add** box that pops up, scroll down the **Additional sources** list. Select **Public Datasets**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/BQENLEA_R5G71s0HJV5mgA_a70b98bc7b534b74be5078bd7efaffe1_C3M3L5_A_06_Graphic02.png?expiry=1716768000000&hmac=2fbWBvB8ybUart02hCv0M5ySGIEPQSbyl9KabZSMh-M)

3. A new box opens where you can search public datasets that are available through Google Cloud. In the **Search Marketplace** text box, search for **New York City Trees**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GV4XC3W6R0qZ-sSYSGfENQ_6412255d4c5a4f16b7de3f6b134c87e1_C3M3L5_A_06_Graphic03.png?expiry=1716768000000&hmac=DEdJ8g5rosrj2nAWzoM-A5XGaVi6u8fH1C3MgsWE3-g)

4. Select the search result **NYC Street Trees**, then select the **View Dataset** button.

Heading is NYC Street Trees. Link to City of New York provided. Subheading is New York City Street Tree Census data. Select View dataset button to link to dataset.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6V5S_XljQg2coHIt-lGZFQ_01808006f12c44c4a214e4a87c58fae1_C3M3L5_A_06_Graphic04.png?expiry=1716768000000&hmac=RPVR_Ld1Xidlnt7zO2yeACJm6h9OIv7f-kFN0wtUJsA)

5. Google Cloud opens a new browser tab displaying BigQuery with the **bigquery-public-data** collection open in the **Explorer** pane. To ensure the **bigquery-public-data** database remains in your project’s **Explorer** pane, select the star next to the dataset.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4W4pRv_HT86PsYAGCEVLgg_d4d3c7364f98469795b5148f062852e1_Explorer-with-public-data-favorited.png?expiry=1716768000000&hmac=K11X_ksyYJHR6NAv-GhPiGCfmlCUIa1j0UPk9JuNlQQ)

6. The BigQuery **Details** pane contains information about the **new_york_trees** dataset. This information includes the date the dataset was created, when it was last modified, and the Dataset ID.

The Details pane displaying the new_york_trees data description including the dataset ID, when it was created, default table expiration, when it was last modified, the data location, description, the default collation, the default rounding mode, case insensitive, the labels, and the tags.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Vwbic18kRsWpHEeg41hPWg_576f156c648a45ccb785c0ade458d3e1_C3M3L5_A_06_Graphic05.png?expiry=1716768000000&hmac=_2WIzULgIIglHPAID0BApSo6FU8lXORg4oaV98T6cm8)

# **Step 3: Choose a table**

1. In the **Explorer** pane, select the arrow next to the **new_york_trees** dataset to display the tables it contains.

**Note:** If the **new_york_trees** dataset is not in the **Explorer** pane, type **new_york_trees** into the **Search** text box in the **Explorer** pane. (This will work if you have pinned **bigquery-public-data** in the **Explorer** pane.) If search doesn’t return the needed results, follow the steps above to search for the **new_york_trees** dataset.

2. Notice that the **new_york_trees** dataset contains three tree census tables from 1995, 2005, and 2015. It also contains a table that lists the tree species.

In the Explorer pane, bigquery-public-data is open and the new_york_trees dataset is expanded to show the tables in the dataset are:  tree_census_1995, tree_census_2005, tree_census_2015, and tree_species.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TYZPqcmURpmVdV5nsu-_bg_2c0a9ab93d5c48f8adfe12f6fa09eae1_C3M3L5_A_06_Graphic06.png?expiry=1716768000000&hmac=KV223v1-Hu8XFsTFbRJzA6Zj8WNxZ7KaBWRYs0uzupE)

These are all tables contained in the dataset. Now, examine the data for all trees cataloged in New York City for three specific years.

3. Select the **tree_census_2005** table. BigQuery displays the table’s structure in the **Details** pane.

4. In the **Details** pane, select **Query > In new tab** to open a new query window.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Av1SBx3_SqatZCt2rJFuiw_1eaedff42b30487db6bc92aeba4221e1_C3M3L5_A_06_Graphic07.png?expiry=1716768000000&hmac=K4Wfv3orSe8SiNcHtzzI3KII-CKY3Wb7yKDEfdVizxU)

5. Notice that BigQuery populates the **Query Window** with a **SELECT** query. This query is incomplete because it doesn’t contain anything in between **SELECT**and **FROM**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9v1v9v9ARi2y3C-W-tue4g_d4b2945296c34d3ea5f132f2dcc86de1_C3M3L5_A_06_Graphic08.png?expiry=1716768000000&hmac=EGl6nalz0HrFfy3Z8ir4kc27HZzQaO2GEA0MssdaWVc)

# **Step 4: Query the data**

This **SELECT** statement in the **Details** pane is incomplete because the columns to display have not been specified. So, either list the columns separated by commas or use the asterisk to have BigQuery return all columns in the table.

1. Type an asterisk ***** after the **SELECT** command in line one of the **Query Editor**. Your query should now read **SELECT * FROM** followed by your table location. This command tells BigQuery to return all of the columns in the **tree_census_2005** table.

2. In the **Query Editor**, select the **Run** button to run the query. The results will be displayed as a table in the **Query Results** pane below the **Query Editor**.

Results in the preview mode with columns with data populated including the row, object ID, cen_year, tree_dbh, tree_loc, pit_type, soil_lvl, status, spc_latin, and spc_common.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/79Vn1YGXTXWeXPBlj4DIVQ_40091e9555e5496e823586b7f3cfece1_C3M3L5_A_06_Graphic09.png?expiry=1716768000000&hmac=AsWOE4LjjOUhBZMTCwxOFL4v_ERMkElDsWVaJVlTNa8)

This query returns all columns for the first 1,000 rows from the table. BigQuery returns only the first 1,000 rows because the **SELECT** query includes a **LIMIT 1000** clause. This limits the rows returned to reduce the processing time required.

3. Next, write a query to find out the average diameter of all NYC trees in 2005. On line 1, replace the ***** after the **SELECT** command with **AVG(tree_dbh)**. Select the **Run** button to execute the query.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CqycV6zMRxOy4pg8D77w_w_6a441444839045dcb90e6819cc1532e1_C3M3L5_A_06_Graphic10.png?expiry=1716768000000&hmac=NwIgQtBElSFqxNlXq6f15XGwRCrvAv8J7f-JvKCVf9U)

This returns your answer, **12.833** (which means the average diameter of NYC trees in 2005 was 12.833 inches).

# **Step 5: Write your own queries**

Now, come up with some questions and answer them with your own SQL queries. For example, query the 1995 and the 2015 tables to find the average diameter of trees. You can then compare the average diameter of the trees in all three datasets to determine whether the trees in NYC have grown on average. Note that the field name for tree diameter in the **tree_census_1995** table is diameter.

You are also free to choose another publicly available dataset in BigQuery and write your own queries for extra practice—there are many interesting choices!

---