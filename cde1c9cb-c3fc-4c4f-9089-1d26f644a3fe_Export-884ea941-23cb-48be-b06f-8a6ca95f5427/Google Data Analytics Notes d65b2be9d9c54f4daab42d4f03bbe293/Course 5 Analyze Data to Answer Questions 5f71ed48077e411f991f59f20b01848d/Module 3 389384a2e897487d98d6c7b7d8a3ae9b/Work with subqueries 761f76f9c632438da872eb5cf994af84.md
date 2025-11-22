# Work with subqueries

---

# Step-by-Step: Queries within queries

This reading outlines the steps the instructor performs in the next video, [Queries within queries](https://www.coursera.org/learn/analyze-data/lecture/yVQoh/queries-within-queries). In the video, the instructor introduces subqueries, another type of SQL query, and demonstrates how to use them to build more complex queries.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you will need**

In order to follow along with the instructor, you will  need to log in to your BigQuery account and access the public database called **new_york**. To find this dataset, scroll through the datasets in the **bigquery-public-data** project. From this database, you will use the tables called **citibike_stations** and **citibike_trips**.

**Important!**

BigQuery has two different databases that contain very similar information: **new_york** is one database and **new_york_citibike** is another. Both of these databases contain tables called **citibike_stations** and **citibike_trips**. However, these tables are not exactly the same between both databases. This step-by-step uses the **new_york** database. You will need to scroll to find this dataset under the **bigquery-public-data** project in the Explorer pane; it does not come up in a search.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZsJaKYy9SwKGJcV9jqi_fA_13de8e2de6c44af4b22c78cd86a2cff1_DA_C5M3_step-by-step_queries_within_queries_0.png?expiry=1716940800000&hmac=zaQ02BQcPoU7mnD4hSRxmZ8-03L3_BvF_0gdSaWk2kQ)

Further, as with many of the public databases in BigQuery, these tables are regularly updated, so if you find that your results do not exactly match the results in the video, this is one probable explanation why.

## Example 1: Use a subquery in a **SELECT** statement

In this query, you will compare the number of bikes available at a particular station to the overall average number of bikes available at all stations.

Type or copy and paste the following query into a new BigQuery query window.

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled.png)

In this example, the subquery was used in a **SELECT** statement. The outer **SELECT** statement (beginning on line 1) lists column names to be retrieved from the **citibike_stations** table. The inner **SELECT** statement (beginning on line 4) is the subquery, which is used to make a new column that is not already available in the table.

Notice that in the video the **SELECT** statement in lines 4–6 was written first. This is a subquery to calculate the average of the **num_bikes_available** column and alias the results as a new column in the results called **avg_num_bikes_available**. The subquery is enclosed in parentheses, which mark it as a subquery.

Then, the whole subquery is incorporated into an outer query. The subquery is indented to the same level as **station_id** and **num_bikes_available**, which are the other columns to be returned in the query results.

So, the final query should return a table containing columns for **station_id**, **num_bikes_available**, and **avg_num_bikes_available**. Here is an example output, but remember, your results might differ due to table updates.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/64kLJr5ESZCaTXvmkuWGng_8da15723b5b948cea0ce5ad12a2f4ff1_DA_C5M3_step-by-step_queries_within_queries_1.png?expiry=1716940800000&hmac=4VJcCp9m8QrSfYqnlVIPURNrGUDEtxv5CVL3RRiJLvE)

## Example 2: Use a subquery in a **FROM** statement

In this query, you will use the **citibike_trips** table to calculate the total number of rides that started at each station and return this as a column called **number_of_rides_starting_at_station** along with the columns **station_id** and **name** from the **citibike_stations** table.

Type or copy and paste the following query into a new BigQuery query window.

**Note:** The lines tagged with **#**** differ from the code in the accompanying video. This is due to changes to the data tables that resulted in a mismatched data type (**Int64** & **STRING**) between the **start_station_id** column and the **station_id** column in the respective tables. To make them the same datatype, the **start_station_id** column is converted to **STRING** using the **CAST** keyword.

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%201.png)

Here's what's happening in this example. Lines 1–5 are the outer query. They begin with a **SELECT** statement followed by the names of the columns you want returned in the final query results table: **station_id**, **name**, and **number_of_rides_starting_at_station**.

The problem is that the **number_of_rides_starting_at_station** column doesn't exist in either table. It must be created. Adding further complication is the fact that the **station_id** and **name** columns exist in the **citibike_stations** table, while the information needed to create the **number_of_rides_starting_at_station** is in the **citibike_trips** table.

Lines 6–19 solve this problem. First, notice the subquery from lines 6–14. This subquery is taking the **citibike_trips** table (line 11) and grouping it by **start_station_id** (converted to **STRING**, lines 12–13).

From that grouped data, it's selecting (line 7) the **start_station_id** column (converted to string and aliased as **start_station_id_str**, line 8) and the **COUNT** of all rows that begin with each **start_station_id**. The count is aliased as a new column called **number_of_rides** (line 9). The entire subquery is enclosed in parentheses (lines 6 and 14) and the resulting table is aliased as **station_num_trips** (line 15).

**station_num_trips** is a helper table. By itself, it contains two columns: **start_station_id** and **number_of_rides**. There is one ID for each unique station and the corresponding number of rides from that station.

All the data in that subquery came from the **citibike_trips** table. You still need to connect it to the **citibike_stations** table. Lines 16–19 make the connection. You **INNER JOIN** (line 16) the **station_num_trips** helper table with the **citibike_stations** table (line 17) using the **station_id** column in the **citibike_stations** table and the **start_station_id_str** column in the **station_num_trips** helper table as common keys (lines 18–19).

This results in a big table that contains *all* the columns in the **citibike_stations** table as well as the **start_station_id** and **number_of_rides** columns from the **station_num_trips** helper table. However, you don't need all these columns. You only need three: **station_id**, **name**, and **number_of_rides_starting_at_station**. These are the columns that are selected in lines 1–4.

The final query results should contain these three columns, with rows in descending order by number of rides. Here is an example output, but remember, your results might differ due to table updates.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/PjfgMtzNQS6nJQfOEPGdag_9f96e056dcbb4ad5be6c1e673267dff1_DA_C5M3_step-by-step_queries_within_queries_2.png?expiry=1716940800000&hmac=TGhafHo7msVb_nlm51jHfl11OCPzRKD__3aulsPhsiY)

## Example 3: Use a subquery in a **WHERE** statement

Finally, you will write a query that returns a table containing two columns: the **station_id** and **name** (from the **citibike_stations** table) of only those stations that were used by people classified as subscribers, which is information found in the **citibike_trips** table.

Type or copy and paste the following query into a new BigQuery query window.

**Note:** Line 10 (tagged with **#****) differs from the code in the accompanying video. This is due to changes to the data tables that resulted in a mismatched data type (**Int64** & **STRING**) between the **start_station_id** column and the **station_id** column in the respective tables. To make them the same datatype, the **start_station_id** column is converted to **STRING** using the **CAST** keyword.

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%202.png)

To understand this query, break it into three sections.

### Section 1:****

The first section begins with lines 8–15. This is the subquery, which is indicated by the parentheses in lines 8 and 15. This segment takes the **citibike_trips** table (lines 11–12) and filters it using the **WHERE** clause (line 13) so it only contains rows where the **usertype** column contains **Subscriber** as a value (line 14).

From this filtered table, you select the **start_station_id**, which is converted to string and aliased as **start_station_id_str** (lines 9–10).

At this point, you have an intermediary table with just a single column—**start_station_id_str**—containing the IDs of every row that had **Subscriber** in the **usertype** column of the original table.

### Section 2:

The second section of the query is in lines 4–7. This part uses the information in the intermediary table from section 1 to filter the **citibike_stations** table. It begins with the full **citibike_stations** table (line 5). Then, it filters this table using a **WHERE** clause (line 6) so it only contains rows where the values in its **station_id** column also are found in the list of **start_station_id_str**s that resulted from section 1.

At this point, you now have an intermediary table containing all the columns of the **citibike_stations** table, but only the rows of stations that were the starting station of a subscriber.

### Section 3:

The last part is the simplest. You just need to select the relevant columns from the intermediary table from section 2. This happens in lines 1–4, where you select the **station_id** and **name** columns and add the **FROM** clause in line 5. Everything you're selecting from follows, which was explained in sections 1 and 2.

The final query results should contain two columns: **station_id** and **name**. Here is an example output, but remember, your specific results might differ due to table updates.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/x7a4Yy0VTbCS-8uuACXYGQ_478d3dfa94f246378e8b8a4ed7c326f1_DA_C5M3_step-by-step_queries_within_queries_3.png?expiry=1716940800000&hmac=oLPURMgaKMn61g3uG0sSEUe6XkpHWbzhjxpQNpuyziQ)

---

# Queries within queries

[index (24).mp4](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/index_(24).mp4)

---

# Hands-On Activity: Use subqueries to refine data

## Activity Overview

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CL08w116QWqFCBP0Nq2KUg_5fa155e1a30d4b6295d124b3e9b743f1_IGKj8ItfbIM4JUe7QtixqBT7nQ_4plv6psIttRlXnMAyHXUvYKHaJd_zVWCr0f7y-Ye_Q5FLtun5rqJ04P6tRtmavrUB6T7lAHUoJtpCNETdgb1c5GfhzsjBpTjUrDyj2HRU3DPQ5NdbT0DilhX2QzUYJasvbQWPkoJFzI5N88gTa1NZxBQF9u7RCFegbo8?expiry=1716940800000&hmac=qGYjutKlkds9xuwxbksXLbkyYvGqllFBPLCQbjkZFh8)

As you’ve learned, a subquery is a query that is nested inside of another query. The subquery filters or sorts data to prepare it to be used by the outer query to produce its final result. This allows data professionals to create more nuanced queries that provide specific insights from the data!

For example, perhaps a data analyst working in human resources has been asked to determine the average salary of employees working within a specific department. The analyst can use a subquery to first find the total salary and number of employees within the department. Then, the outer query will use these numbers to calculate the average salary within a department. It's a step-by-step process, each step relying on the one before it.

In this activity, you will practice using **SELECT** statements with **FROM**, **WHERE**, and **GROUP BY** clauses to build your subqueries. By the time you complete this activity, you will be able to create a subquery using **SELECT** statements with **FROM**, **WHERE**, and **GROUP BY** clauses and analyze the query’s results.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

You work for an organization that is responsible for the safety, efficiency, and maintenance of transportation systems in your city. You have been asked to gather information around the use of Citi Bikes in New York City. This information will be used to convince the mayor and other city officials to invest in a bike sharing and rental system to help push the city toward its environmental and sustainability goals.

To complete this task, you will create three different subqueries, which will allow you to gather information about the average trip duration by station, compare trip duration by station, and determine the five stations with the longest mean trip durations.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the dataset**

For this activity, you will need to log in to your BigQuery account to use the public **new_york_citibike** dataset. Then, use the table called **citibike_trips**. For a refresher on how to access this data, refer to the optional reading [Prepare to use the bike sharing dataset in BigQuery](https://www.coursera.org/learn/analyze-data/supplement/vYBY0/optional-prepare-to-use-the-bike-sharing-dataset-in-bigquery).

**Note:** Many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.

# **Step 2: Create a subquery to find the average trip duration by station**

First, find the average trip duration for a particular station. This subquery will be applied to the **SELECT** statement, but first you need to build the outer query:

1. Select **COMPOSE A NEW QUERY** from the SQL workspace in BigQuery. Or, if you have the **new_york_citibike.citibike_trips** table open, select **Query** from the table's menu to compose a new query.

2. In line 1, enter **SELECT**, then press **Enter/Return**.

3. In line 2, press **Tab**, then enter **subquery.start_station_id** followed by a **comma**. Then press **Enter/Return**.

4. In line 3, enter **subquery.avg_duration**, then press **Enter/Return**.

Lines 1–3 in the query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%203.png)

This **SELECT** statement is used to create the outer query. The fields identified in lines 2 and 3 allow the **SELECT** statement to function similarly to a table with an alias, e.g. **SELECT alias.column_name1, alias.column_name2**. This relies on the subquery below to populate the Query results table.

5. In line 4, press **Backspace** to remove the indentation to align the text with the SELECT statement. Enter **FROM**, then press **Enter/Return**.

6. In line 5, press **Tab**, then enter an open parenthesis [**(**]. Then press **Enter/Return**.

7. In line 6, press **Tab**, then enter **SELECT**. Then press **Enter/Return**.

8. In line 7, press **Tab**, then enter **start_station_id** followed by a **comma**. Then press **Enter/Return**.

9. In line 8, enter **AVG(tripduration) as avg_duration**. Then press **Enter/Return**.

Lines 4–8 in the query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%204.png)

The subquery is created by using another **SELECT** statement, located within a **FROM** clause. It is used to determine the average trip duration by station. The station is indicated by the **start_station_id**. The average is calculated using the **AVG** function and is given the alias **avg_duration** using **AS**. This will appear as a column title in the results table after you run the query.

10. In line 9, press **Backspace** to remove the indentation to align the text with the **SELECT** statement.

11. Still in line 9, enter **FROM bigquery-public-data.new_york_citibike.citibike_trips**, then press **Enter/Return**.

12. In line 10, enter **GROUP BY start_station_id) as subquery;** Notice that this line closes the parentheses that opened in line 5.

13. In line 11, add **ORDER BY avg_duration DESC;**.

Lines 9, 10, and 11 in the query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%205.png)

**FROM** will tell the subquery where to pull the data from. In this case, it’s pulling from the **citibike_trips** table. **GROUP BY** will group the rows by columns. Notice how it has the alias, **subquery**. This is what links to the two fields designated to be the titles of the results columns, as indicated in the outer query.

The complete query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%206.png)

13. Select **RUN**. The results will appear in the **Query results** window.

**Note:** Your results should contain two columns: **start_station_id** and **avg_duration**, however, the specific rows may differ from what is depicted here due to periodic refreshes of the source tables on BigQuery.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LE0oez4tT6Cf_gbGzmGeHA_b341b7ddd1a8489d97d9755f2e6ad6f1_C5M3L3_A1_first_query_results.png?expiry=1716940800000&hmac=ius0htIPrjI-sdU83lqZGWfxJ21UasX1EWVP2v1gqFY)

Take some time to examine the query results. In this case there are 882 lines of data that you can use to analyze and compare the average trip durations between each station. You will continue to work with the average trip duration per station in the next query.

# **Step 3: Create a subquery to compare trip duration by station**

Create a new query to compare the average trip duration per station to the overall average trip duration from all stations. This will provide insights about how long people typically use the bikes that they get from a particular station in comparison to the overall average. This subquery will be applied to the FROM clause in a SELECT statement. To begin:

1. Select the **blue plus sign** tab to compose a new query.

2. In line 1, enter **SELECT**, then press **Enter/Return**.

3. In line 2, press **Tab**, then enter **starttime** followed by a **comma**. Then press **Enter/Return**.

4. In line 3, enter **start_station_id** followed by a **comma**, then press **Enter/Return**.

5. In line 4, enter **tripduration** followed by a **comma**, then press **Enter/Return**.

Lines 1–4 in the query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%207.png)

To begin the query, note there are three fields from which to gather data  in order to request the average trip durations. Here, use **starttime** (a somewhat unique identifier for the results) to mark when trips from a particular station started; the **start_station_id**, which identifies the station ID for each trip; and the **tripduration**, which measures the length of each trip in seconds. These will be the first three columns in your results table.

You'll generate two additional columns in the results table: **avg_duration_for_station** and **difference_from_average**. Begin with the subquery for **avg_duration_for_station**:

6. In line 5, enter an open parentheses **(**

7. In line 6, enter **SELECT ROUND(AVG(tripduration), 2)**

8. In line 7, enter **FROM bigquery-public-data.new_york_citibike.citibike_trips**.

8. In line 8, enter **WHERE start_station_id = outer_trips.start_station_id**.

9. In line 9, close the parentheses **)** that were opened in line 5, making sure that both align in indentation. Then, on the same line, name the column by typing **AS avg_duration_for_station,**

Lines 5–9 in the query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%208.png)

A **SELECT** statement is used to begin a subquery that will return the average trip duration for each station. Notice that the **ROUND** function is used to round the numerical value of each trip duration to the nearest hundredth of a second. (Remember: trip duration is measured in seconds.) **FROM** indicates that you want the query to pull from the **citibike_trips** table within the **new_york_citibike** dataset inside the **bigquery-public-data** database. **WHERE** tells the query to link the **start_station_id** with the output of the query: a new column labeled **avg_duration_for_station**.

Now, begin the subquery to create the second new column in the results table: **difference_from_avg**.

10. In line 10, enter **ROUND(tripduration - (**. Make sure it begins on the same indentation level as the previous columns that you selected.

11. In lines 11, 12, and 13 enter:
**SELECT AVG(tripduration)    
FROM bigquery-public-data.new_york_citibike.citibike_trips    
WHERE start_station_id = outer_trips.start_station_id), 2) AS difference_from_avg**

This closes the subquery that creates the **difference_from_avg** column. Now, what remains is to close out the outer query.

12. In lines 14, 15, and 16 outdent all the way back to the left and enter:
**FROM bigquery-public-data.new_york_citibike.citibike_trips AS outer_trips
ORDER BY difference_from_avg DESC
LIMIT 25;**

Lines 10–16 in the query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%209.png)

A second **SELECT** statement is used to return the difference between the specific station's average trip duration and the overall average trip duration. Notice that the **ROUND** function is used again to round to the nearest hundredth of a second. The average trip duration is gathered from the **citibike_trips** table using a second **FROM** clause. **WHERE** tells the query to link the **start_station_id** with the output of the query: a new column labeled **difference_from_avg**.

This will contain the difference between the overall average trip duration and the average trip duration per station. The third **FROM** clause pulls the data from the **citibike_trips** table and labels it as **outer_trips**. **LIMIT** is used to limit the output in the results table to 25 results. Depending on the amount of information you need from the dataset, you can change this number as needed to increase or decrease the results, or you can remove it completely to see all results.

**Note**: If you remove the limit, it may take longer for the query to run. You may also have to perform another query to find specific data.

The complete query should read as follows:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%2010.png)

13. Select **RUN**. The results will appear in the **Query results** window.

**Note:** Your results should contain five columns: **starttime**, **start_station_id**, **tripduration**, **avg_duration_for_station**, and **difference_from_avg**, however, the specific rows may differ from what is depicted here due to periodic refreshes of the source tables on BigQuery.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5FRjoqjLSlma2L6YKbNsTA_b8b90f960b6a4b41875ffc78706d59f1_C5M3L3_A1_second_query_results.png?expiry=1716940800000&hmac=eLY-yr4pnCjTX_VG--HwQu9uB0zoAmu-9h1sgKgZ37I)

14. Examine the results table. In the last column, **difference_from_avg**, there are some very large differences from the average duration, indicating that these stations have some significant outliers. It would probably be worthwhile to examine that further.

15. To continue with this activity, you can **save** this query so you can come back to it later, then **create a new query**. Alternatively, you can overwrite the existing query.

### 

# **Step 4: Create a subquery to determine the five stations with the longest mean trip duration**

Now, you'll compose a new query to filter the data to include only the trips from the five stations with the longest mean trip duration.

Write the following code and consider what it's doing:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%2011.png)

Lines 1–4: This query begins by identifying the columns that will appear in the query results table: **tripduration** and **start_station_id**.

However, you don't want all of the records to be selected. You only want those records where the **start_station_id** matches one of the top five stations with the greatest average **tripduration**. To find this, you need a subquery.

Line 5: This is the beginning of the subquery. It uses an **IN** operator to filter records based on whether the **start_station_id** is in a list of **start_station_id**s produced by the subquery.

Lines 6–19: This is an inner subquery. It creates a derived table called **top_five** by performing the following steps:

1. It selects **start_station_id** from the main table.
2. For each **start_station_id**, it calculates the average **tripduration** and labels this average as **avg_duration**.
3. It groups the results by **start_station_id**, meaning the average trip duration is calculated separately for each unique **start_station_id**.
4. From this grouped and aggregated data, it orders the results by **avg_duration** in descending order.
5. It limits the results to the top five. In other words, it only keeps the records for the five **start_station_id**s with the highest average trip durations.

The result of the entire query is a list of records from the main table—specifically the **tripduration** and **start_station_id** for each record, but only those for records where the **start_station_id** is among the five stations with the greatest average trip durations. If you examine the query results, you will discover that only five of the **start_station_id** values are listed in column two. The output of the query should appear similar to this:

**Note:** Your results should contain two columns: **tripduration** and **start_station_id**, however, the specific rows may differ from what is depicted here due to periodic refreshes of the source tables on BigQuery.

Column one is tripduration; column two is start_station_id.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/81oV20nqSWOhRi0yZ9sS1g_27cf9ada0c1b4bb3b04f58270392e3f1_C5M3L3_A1_Image3.png?expiry=1716940800000&hmac=4xDAOTQV8GB1a8cKQvldzzPSFWv5Bv2pVRXqKg2mv_M)

Congratulations! You successfully built and ran three different sets of queries with subqueries.

---

# Step-by-Step: Use subqueries to aggregate data

[index (25).mp4](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/index_(25).mp4)

This reading provides you with the steps the instructor performs in the following video, [Use subqueries to aggregate data](https://www.coursera.org/learn/analyze-data/lecture/JjPZ5/using-subqueries-to-aggregate-data). The video teaches you how to aggregate or combine data using subqueries in SQL.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

In order to follow along with the instructor, you will need the **warehouse_orders** dataset uploaded into your project space. From that dataset, you'll need the **warehouse** and **orders** tables. If you haven’t already uploaded this data, follow the instructions in the [Upload the warehouse dataset to BigQuery](https://www.coursera.org/learn/analyze-data/supplement/HuXCc/optional-upload-the-warehouse-dataset-to-bigquery) reading.

## Objective

The objective of this query is to aggregate the data into a table containing each warehouse's ID, state and alias, and  number of orders; as well as the grand total of orders for all warehouses combined; and finally a column that classifies each warehouse by the percentage of grand total orders that it fulfilled: 0–20%, 21-60%, or > 60%.

**Note:** This activity breaks out the steps into manageable chunks. The final query is only intended to be run at the end. If you try to run the query before reaching the end of this guide you will likely get an error.

## Example: Combine and alias the tables

As a refresher, aliasing is when you temporarily name a table or column in your query to make it easier to read and write. To alias the **warehouse** and **orders** tables and join the tables, follow these steps. Remember, these statements require that you enter your unique individual project name or else they won't run. Be sure to substitute your project name in the code wherever you encounter **your-project** written. If you haven't explicitly assigned a project name, BigQuery generates one for you automatically. It typically looks like two words and a number, each separated by a hyphen, for example **august-west-100777**.

Begin with the **FROM** statement a few rows down. Later, you'll return to the top of the query to fill it in.

1. In row 3, enter **FROM your-project.warehouse_orders.warehouse AS Warehouse**
2. In row 4, enter **LEFT JOIN your-project.warehouse_orders.orders AS Orders**
3. In row 5, enter **ON Orders.warehouse_id = Warehouse.warehouse_id**

These statements will combine the two tables (**warehouse** and **orders**) using **warehouse_id** as the common key (the column shared by both tables).

## Example: Organize your new table

Use the **GROUP BY** clause in SQL to group rows that have the same values in specified columns into aggregated data, such as sum, count, average, maximum, or minimum, based on the values in another column. This operation is particularly useful in databases where there is a need to analyze data based on certain criteria.

1. In row 6, enter **GROUP BY**
2. In row 7, enter **Warehouse.warehouse_id,**
3. In row 8, enter **warehouse_name**

Here, the combined table is grouped first by the warehouse ID and then by its name.

## Example: Build subquery logic

Now that you have the **FROM** statement and **JOIN**, go back up to the first lines and define the rows to select and operations to perform on them. From the objective, you know you want to return **five columns**: each warehouse's ID (**warehouse_id**—column 1), state and alias (this info will be combined into a single column: **warehouse_name**— column 2), and number of orders (**number_of_orders**—column 3); as well as the grand total of orders for all warehouses combined (**total_orders**—column 4); and finally a column that classifies each warehouse by the percentage of grand total orders that it fulfilled: 0–20%, 21-60%, or > 60% (**fulfillment_summary**—column 5).

Above everything you've written so far, write:

1. In row 1, enter **SELECT**
2. In row 2, enter **Warehouse.warehouse_id,** # (This is the first column.)
3. In row 3, enter **CONCAT(Warehouse.state, ': ', Warehouse.warehouse_alias) AS warehouse_name,** # (This is the second column. Notice you're concatenating two existing columns into a new one)
4. In row 4, enter **COUNT(Orders.order_id) AS number_of_orders,** # (This is the third column.)
5. In row 5, enter **(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) AS total_orders,** # (This is the fourth column.)

To create the final column, you'll need to use a special keyword.

## Example: Create categories using **CASE**

Use the **CASE** keyword in SQL to create categories or group data based on specific conditions. This is valuable when dealing with numerical or textual data that needs to be segmented into different groups or categories for analysis, reporting, or visualization purposes.

For the final column, you'll use **CASE** to define which label to apply to each warehouse's fulfillment percentage (the percentage of the grand total of orders that it fulfilled). There will be three conditions, and thus three possible labels: "Fulfilled 0–20% of Orders", "Fulfilled 21–60% of Orders", or "Fulfilled more than 60% of Orders".

1. In row 6, enter **CASE**
2. In row 7, enter **WHEN COUNT(Orders.order_id)/(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) <= 0.20** # (This defines the first possible condition.)
3. In row 8, enter **THEN 'Fulfilled 0-20% of Orders'** # (**THEN** defines the label to apply when the first condition is true.)
4. In row 9, enter **WHEN COUNT(Orders.order_id)/(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) > 0.20** # (This is the first part of the second condition.)
5. In row 10, enter **AND COUNT(Orders.order_id)/(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) <= 0.60** # (This is the second part of the second condition.)
6. In row 11, enter **THEN 'Fulfilled 21-60% of Orders'** # (This defines the label to apply when the second condition is true.)
7. In row 12, enter **ELSE 'Fulfilled more than 60% of Orders'** # (This defines the label to apply when neither of the first two conditions is true.)
8. In row 13, enter **END AS fulfillment_summary** # (The **END** keyword terminates the **CASE** declaration. Then the **AS** keyword indicates what the resulting column should be named.)

## Example: Filter using **HAVING**

Use the **HAVING** clause in SQL in combination with the **GROUP BY** clause to filter the results of aggregate functions in a query. While the **WHERE** clause filters individual rows *before* they are grouped, the **HAVING** clause filters groups of rows *after* they have been grouped. To filter out the warehouses that are currently being built (and therefore have no orders), enter the following lines below everything you've written so far:

1. In row 20, enter **HAVING**
2. In row 21, enter **COUNT(Orders.order_id) > 0**

Here is the final query:

```sql
SELECT
  Warehouse.warehouse_id,
  CONCAT(Warehouse.state, ': ', Warehouse.warehouse_alias) AS warehouse_name,
  COUNT(Orders.order_id) AS number_of_orders,
  (SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) AS total_orders,
  CASE
    WHEN COUNT(Orders.order_id)/(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) <= 0.20
    THEN 'Fulfilled 0-20% of Orders'
    WHEN COUNT(Orders.order_id)/(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) > 0.20
    AND COUNT(Orders.order_id)/(SELECT COUNT(*) FROM your-project.warehouse_orders.orders AS Orders) <= 0.60
    THEN 'Fulfilled 21-60% of Orders'
    ELSE 'Fulfilled more than 60% of Orders'
  END AS fulfillment_summary
FROM your-project.warehouse_orders.warehouse AS Warehouse
LEFT JOIN your-project.warehouse_orders.orders AS Orders
ON Orders.warehouse_id = Warehouse.warehouse_id
GROUP BY
  Warehouse.warehouse_id,
  warehouse_name
HAVING
  COUNT(Orders.order_id) > 0
```

## Example: Run the new query

It’s important to run the new queries that you write to test that they are working correctly.

1. Select the **Run** button
2. Now, you can identify what percent of our company’s total orders are being fulfilled by each warehouse

The query results should be:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/j1x3VEpuRVizCJAQ4BzQDQ_fd7aed1508994362b851c8aafd4f68f1_DA_C5M3L3R2_Use_subqueries_to_aggregate_data_query_result.png?expiry=1716940800000&hmac=Gbos-RodFykjEiU-xiun83lzLL3RLZq7vsMKbb0MHVg)

---

# SQL functions and subqueries: A functional friendship

As you’ve been learning, **SQL functions** are tools built into SQL to facilitate performing calculations. For example, you could use the **AVG()** function to calculate the average salary of employees in a table so management knows what to budget for next year. Another example might be using the **COUNT()** function to count the number of orders in a table to track daily order inventory.

A **subquery**, also called an inner or nested query, is a SQL query that is nested inside a larger query. Going back to the previous example, you could add a subquery to your average calculation to identify the names of employees who earn more or less than the average salary to include that information in performance reviews. Subqueries allow more complex questions to be answered in a single query, making data retrieval more efficient. In this reading, you will learn about SQL functions and how they might be used with subqueries.

## How do SQL functions function?

SQL functions help make data aggregation possible. As a refresher, data aggregation is the process of gathering data from multiple sources in order to combine it into a single, summarized collection. Take a moment to review some of these functions to better understand how to run these queries:

- **HAVING:** The **HAVING** clause filters the results of a SQL query based on conditions applied after the grouping. Check out [W3School’s HAVING overview](http://www-db.deis.unibo.it/courses/TW/DOCS/w3schools/sql/sql_having.asp.html) for a tutorial on this clause
- **CASE: CASE** provides conditional logic in SQL queries, similar to an 'if-else' structure in programming languages. The [W3School’s CASE overview](https://www.w3schools.com/sql/sql_case.asp) explores the use of the **CASE** statement and how it works.
- **IF:** IF ****performs a simple conditional test and returns a value depending on the outcome. Review [W3School’s IF overview](https://www.w3schools.com/sql/func_mysql_if.asp) for a tutorial of the **IF** function and examples that you can practice with.
- **COUNT: COUNT** performs a simple conditional test and returns a value depending on the outcome. Though it seems simple, the **COUNT** function is just as important as all the rest. The [W3School’s COUNT overview](http://www-db.deis.unibo.it/courses/TW/DOCS/w3schools/sql/sql_func_count.asp.html) provides a tutorial and examples.

## Subqueries

Subqueries can make projects easier and more efficient by allowing complex operations to be performed in a single query, reducing the need for multiple trips to the database. Subqueries also make your code more readable and maintainable. Take the employee salary example mentioned before.:The original query was used to find the average employee salary. By adding a subquery, you can learn this plus identify employees who earn more than the average—all in a single query.

Usually, you will find subqueries nested in the **SELECT**, **FROM**, and/or **WHERE** clauses. There is no general syntax for subqueries, but the syntax for a basic subquery follows a similar pattern:

![Untitled](Work%20with%20subqueries%20761f76f9c632438da872eb5cf994af84/Untitled%2012.png)

Basically, there’s another **SELECT** clause inside the first **SELECT** clause. The second **SELECT** clause marks the start of the subquery in this statement. There are many different ways in which you can use subqueries, but there are a few rules to follow:

- Subqueries must be enclosed within parentheses.
- A subquery can have one or more columns specified in the **SELECT** clause.
- Subqueries that return more than one row can only be used with multiple value operators, such as the **IN** operator which allows you to specify multiple values in a **WHERE** clause.
- A subquery can’t be nested in a **SET** command. The **SET** command is used with **UPDATE** to specify which columns (and values) are to be updated in a table.

### **Additional resources**

The following resources offer more guidance into subqueries and their usage:

- [**SQL subqueries**](https://www.w3resource.com/sql/subqueries/understanding-sql-subqueries.php): ****This detailed introduction includes the definition of a subquery, its purpose in SQL, when and how to use it, and what the results will be.
- [**Writing subqueries in SQL**](https://mode.com/sql-tutorial/sql-sub-queries/): Explore the basics of subqueries in this interactive tutorial, including examples and practice problems that you can work through.

As you continue to learn more about using SQL, functions, and subqueries, you will realize how much time you can truly save when memorizing these tips and tricks.

---

# Hands-On Activity: Use subqueries

## Activity Overview

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bwV79Fv_RMm5AkrFRElxTw_0c7d804cfa434aaaa2cf274a291cacf1_CL08w116QWqFCBP0Nq2KUg_5fa155e1a30d4b6295d124b3e9b743f1_IGKj8ItfbIM4JUe7QtixqBT7nQ_4plv6psIttRlXnMAyHXUvYKHaJd_zVWCr0f7y-Ye_Q5FLtun5rqJ04P6tRtmavrUB6T7lAHUoJtpCNETdgb1c5GfhzsjBpTjUrDyj2HRU3DPQ5NdbT0DilhX2QzUYJasvbQWPkoJFzI5N88gTa1NZxBQF9u7RCFegbo8?expiry=1716940800000&hmac=r_JUsHbhAZ7RT5BQFk7ZhiHk99b1koqRvNT7ZZfERcM)

As a data analyst, you will sometimes want to analyze a small subset of data that is contained within a much larger dataset. This is when subqueries can be really useful. As you’ve been learning, subqueries are queries that are nested inside of another query. Some queries can have many subqueries, while others may have only one. It’s important to know how subqueries function and to understand the different components you can use to create them.

In this activity, you will work with queries and subqueries to examine a public health dataset. You will create subqueries to discover which industries receive an unusual number of complaints and, more importantly, which industries are connected to serious health issues. This will allow you to allocate your resources more effectively to safeguard public health.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

In this scenario, you are a junior data analyst for a multinational food and beverage manufacturer. You and your team are responsible for maintaining the safety of a wide array of food products. Because of the overwhelming number of products on the market, you have been asked to prioritize which products need to be reviewed by your stakeholders.

While it's useful to know which food industries receive the most complaints, the more critical aspect to consider is identifying the complaints that lead to severe health consequences, such as hospital visits.

To complete this task, you'll analyze food event reports for targeted health interventions.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the question at the end of the activity before going to the next course item.

# **Step 1: Access the public dataset**

The first step is to access the public dataset. For this activity, you will use a BigQuery public dataset titled **fda_food**, which contains details about food recalls, consumer reactions, product descriptions, and product distribution and quantities.

1. Log in to BigQuery and open the [BigQuery Console](https://console.cloud.google.com/bigquery).

**Note:** BigQuery frequently updates its user interface. The latest changes may not be reflected in the screenshots presented in this activity, but the principles remain the same. Adapting to changes in software updates is an essential skill for data analysts, and it’s helpful for you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.

2. Before you can load the **fda_food** dataset, you need to have **bigquery-public-data** pinned in the Explorer menu of your SQL Workspace. Follow these steps to pin the dataset:

a. Enter **public** in the Explorer menu search box, and press the **Enter**/**Return** on your keyboard.

b. Select **SEARCH ALL PROJECTS**.

c. Scroll to find **bigquery-public-data** and select the **star** to pin it.

3. Add the FDA food dataset. Follow these steps:

a. Select the **arrow** next to the bigquery-public-data to expand its contents. T

b. Scroll to find **fda_food**. You may have to select **SHOW MORE** to view the dataset listed.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vTnOG3JfSy6idiS4-z9o7Q_8c4ccd17babf46709e9a265dd616c8f1_C5M3L3_UsingSubqueries_Image3.png?expiry=1716940800000&hmac=1hIL2XVxFv2ipbXf1XJfAMBGsNpBni3_LypJDp5Q4f8)

c. Expand **fda_food** and select **food_enforcement**.

d. Select the **Preview** tab in the viewer to examine the table data.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jQVGdp_lRtu06Jnha_uydA_63e9981a11c741b69ab28a03e7c412f1_fda_food-preview.png?expiry=1716940800000&hmac=w-B3Oa14coe1CqAAkBADi0CGVM4wABL-E4ZQaf3opx0)

4. Next, select the **food_events** table from the **fda_food** dataset, then select **Preview** to examine the table data.

Once you have taken some time to explore the tables within the fda_food dataset, you are ready to begin working with subqueries!

**Note:** Many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.

# **Step 2: Gather an initial overview**

To get an initial overview, run a SQL query to identify which food industries have the highest number of complaints. This will provide an initial dataset to work from. To find the top industries for recalls, perform the following steps:

1. Create a new query.

2. Enter the following in the query editor:

```sql
SELECT 
products_industry_name, 
COUNT(report_number) AS count_reports
--SELECT is used to identify the product industries by name. COUNT will count the number of reports and label them as count_reports.
FROM bigquery-public-data.fda_food.food_events
GROUP BY products_industry_name
ORDER BY count_reports DESC
LIMIT 10;
--The query will group the product industries by name so the report results will fall under each industry title. ORDER BY and DESC will tell the query to order the output by count_reports in descending order so, the industry with the most amount of reports will appear at the top of the output table. LIMIT will limit the results to ten industries with the highest numbers of reports. 
```

**Note**: Depending on the type of web browser you are using, you may have issues conducting a direct copy + paste of the above syntax directly from this assignment to your BigQuery workspace. If you are experiencing this issue, open two separate windows on your screen to manually enter the above information into the BigQuery workspace area.

3. You have the option to save your query as a table. To do this, select the **MORE** menu from the Query Editor and open the Query Settings menu. In the Query Settings menu, select **Set a destination table** for query results. Set the dataset option to **demos** and name the table **reports_by_industry**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/N0eLL-PRR96EbtLk1rhlxA_8a963bb346c341988949e7c4bf68f3f1_C5M3L3_UsingSubqueries_Image5.png?expiry=1716940800000&hmac=agfJ5LwL4JlpTWYn_RQWCoUeHuSAwu4bWuYX8HKMsng)

4.  Select **RUN**. The query will save as a new table in your demos dataset.

The **Query results** window will populate with a table containing two columns and 10 rows.  The first column is **products_industry_name**, and the second is **count_reports**. The 10 different industries are listed in descending order in the rows.

Take some time to check the different industries and the differences in report numbers. You can modify your search to examine the different symptoms that consumers experienced (**reactions**) based on products (**products_brand_name**) as well as the **outcomes**, or consequences, from each food event.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9DlKlzdaRqerw3YapSC60g_5f4962522e724fd3980c81f12b9d28f1_C5M3L3_UsingSubqueries_Image6.png?expiry=1716940800000&hmac=ZANZAHIDA1cxW-oJTzHeBlO62cUe0Y9QErLZFlE0aWQ)

### 

# **Step 3: Determine the number of hospitalizations**

With a list of the industries receiving the most complaints, your next step is to find out which of these complaints led to hospitalizations. Filter the initial list accordingly and focus solely on complaints that resulted in hospital visits. To do this:

1. Create a new query.

2. Enter the following into the editor:

```sql
SELECT 
products_industry_name, 
COUNT(report_number) AS count_hospitalizations
FROM
bigquery-public-data.fda_food.food_events
WHERE products_industry_name IN
(SELECT 
products_industry_name
FROM 
bigquery-public-data.fda_food.food_events
GROUP BY products_industry_name
ORDER BY COUNT(report_number) DESC LIMIT 10)
AND outcomes LIKE '%Hospitalization%'
--The AND operator displays a record if all the conditions are TRUE.
--The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.
GROUP BY products_industry_name
ORDER BY count_hospitalizations DESC;
```

The outer query used here is just like the previous query. **SELECT** calls the product industry names, and **COUNT** counts the number of reports and labels them as count_hospitalizations.  The query is told to pull this data from the **food_events** table.

The subquery begins with a **WHERE** clause and an **IN** operator—these will allow the subquery to specify multiple values. The second **SELECT** statement tells the subquery to pull the product industry names **FROM** the **food_events** table in the **FDA_food** dataset. Results are then grouped by product industry name and ordered in descending order. **LIMIT** tells the query to limit the number of results to 10. **AND** and **LIKE** are used to indicate if hospitalizations are present within the **outcomes** field.

The outer query is then closed by grouping results by **product_industry_name** and ordered in descending order by the number of hospitalizations recorded.

3. You can also save this query as a table. Before running the query, select the **MORE** menu from the Query Editor and open the Query Settings menu. In the Query Settings menu, select **Set a destination table** for query results. Set the dataset option to

4. Select **RUN**. The query will save as a new table in your demos dataset.

The **Query results** window will populate with a table containing two columns and ten rows.  The first column is **products_industry_name**, and the second is **count_hospitalizations**. The 10 different industries are listed in descending order in the rows.

Take some time to review the different industries and the differences in reported hospitalizations. You can modify your search to examine the different symptoms that consumers experienced (**reactions**) based on products (**products_brand_name**); the dates in which the food events occurred (**date_started**); and the **outcomes**, or consequences, from each food event. These modifications will allow you to find and analyze any links among fields within the datasets for your research.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4JfvIOpjR7-lkaKdB5lQpw_2c5beb40fbb742ec92f9fd1e179ddff1_C5M3L3_UsingSubqueries_Image7.png?expiry=1716940800000&hmac=rztchRypQfYcsqMLToIAslbdn0SOsQRRfg9NWAafsGM)

Great work! Through this process, you discovered which industries receive an unusual number of complaints and, more importantly, which are connected to serious health issues. This knowledge allows you to allocate your resources more effectively to safeguard public health. By completing this activity, you have created subqueries using **SELECT** statements with **FROM, GROUP BY, WHERE, IN, AS, COUNT**, and **ORDER BY** clauses, as well as **AND** and **LIKE** operators to search and analyze the query results relating to reports of food events by industry.

---