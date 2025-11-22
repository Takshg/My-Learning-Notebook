# SQL and temporary tables

---

# Temporary tables

[index (35).mp4](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/index_(35).mp4)

- **Temporary tables** are database tables that exist temporarily on a server and are automatically deleted when the SQL session ends.
- They are useful for:
    - Performing calculations on subsets of data from standard tables.
    - Joining multiple tables with a large number of rows.
    - Running queries on data from multiple databases.
    - Working with a small subset of records repeatedly.
- **Creating temporary tables in BigQuery:**
    - Use the `WITH` clause to create a temporary table.
    - The `WITH` clause creates a temporary table that can be queried multiple times.
    - The temporary table is not stored permanently in the database.
- **Example:**
    - Create a temporary table called `trips_over_1_hr` that contains data for bike trips over 60 minutes.
    - Run queries on the temporary table to analyze the data.

**Definitions:**

- **Temporary table:** A database table that exists temporarily on a server and is automatically deleted when the SQL session ends.
- **`WITH` clause:** A clause in SQL that creates a temporary table.
- **Subquery:** A query that is nested within another query.
- **`COUNT` function:** A function that returns the number of rows in a table or query result.

---

# Hands-On Activity: Create temporary tables

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G-KePoi0R2Sinj6ItBdkMg_2d69ab4b929f40f2b472a78fdd5ed880_line-y.png?expiry=1716940800000&hmac=SEphjdYBdoz0TRm7EByd3ssnqoR5bANw6SL-vCmMzHc)

As data calculations become more complicated, there are many components to keep track of, such as range, cost, time elements, products, and more. Some people use sticky notes for this, while others use checklists. In the data profession, a temporary table is just like a sticky note.

You learned about temporary tables in SQL in earlier lessons, so take a moment to review. **Temporary tables**, or **temp tables**, store subsets of data from standard data tables for a certain period of time. Temp tables allow you to run calculations in temporary data tables without needing to make modifications to the primary tables in your database. Because they are temporary, they are automatically deleted at the end of your SQL session.

By the end of this activity, you will have gained more experience creating temp tables and using them to run queries.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

A bikeshare company has reached a milestone, and their marketing team wants to write a blog post announcing the popularity of their most-used bike. They want to include the name of the station where that bike can most likely be found, so they ask you to determine which bike is used most often.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Import your data**

The first step is to import your data. For this activity, you will use a BigQuery dataset on bikesharing in Austin, Texas, which contains details about each public bike ride’s duration, starting station, and ending station.

To load your data, follow these steps:

1. Log into BigQuery and open your [Console](https://console.cloud.google.com/bigquery).

- **Note:** BigQuery frequently updates its user interface. The latest changes may not be reflected in the screenshots presented in this activity, but the principles remain the same. Adapting to changes in software updates is an essential skill for data analysts, and it’s helpful for you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.

2. Select the project dropdown list to open the Select a project dialog box.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/7mPanKcKSKCca_OnJktjYQ_cfad66f002a24ce98f3eec77f120d8e1_C5M4L5-Create-a-Project.png?expiry=1716940800000&hmac=Qn4CsvwLbp82NjSRh-V5imFfKVKGRxihoWL0xVduNZk)

3. In the **Select a project** dialog box, select the **NEW PROJECT** button.

4. Name your project something that will help you identify it later. You can give it a unique project ID or use an auto-generated one.

5. Now, access the Editor interface. You will use the Explorer menu to search for datasets.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_BrodM5iSQGB18wXnZOi3g_44cb0042eb514d218ea14fcb744d6ce1_C5M4L5-Explorer-pane.png?expiry=1716940800000&hmac=Xw6vuS1vZEvDfjTmdsP-DJdcI5iPziBSN0CqhfDJJAI)

# **Step 2: Pin the dataset**

**Note:** Before you can load the **austin_bikeshare** dataset, you need to have the bigquery-public-data pinned in the Explorer menu of your SQL Workspace. Follow these steps to pin the dataset:

1. Enter **public** in the Explorer menu search box and press the **Enter** key.

2. Select **SEARCH ALL PROJECTS**.

3. Scroll to find **bigquery-public-data** and select the star to pin it.

After you’ve highlighted the star and pinned the bigquery-public-data to the Explorer menu, you’ll need to add the Austin bike dataset. Follow these steps:

1. Select the arrow to the left of bigquery-public-data to expand its contents and scroll to find **austin_bikeshare**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/-hi_UzY7Qg-MjW1Fw9Uezw_87a9dfaaaa824d3e8f97035883dc6ae1_niEWY6ZxbiHz5qp90NqWCzj_m9HA9gWKF2m-loJjFuKY0uc33XqzvRDaDYx98fu9l6KWv1GIjAHvmM51UbvT7_mMo-dqYMN4lRuBUR-DyfhCwTwhH7g0Os7euU9Wx4TSMkxecfR6lH3o-U2O3ZoWOvyZZDK4Ie7o2raya5Bd-OHWUAn3rHyBFLCltiKox8jQpyvf1F6QNKEm8mja3_7rkApEOR5eR7PCiTJgaQ?expiry=1716940800000&hmac=N3CxjArPg40DzZIJTbNpMDcZVq3qM1dsM5ARvL-mTfA)

2. Expand **austin_bikeshare** and select **bikeshare_trips**.

3. Select the **Preview** tab in the viewer on the right to examine the dataset.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/-fV4SUHkSx2gqY-afqxGeA_137d417849e8483c9a1c076b4855f2e1_C5M4L5-Bikeshare-Trips.png?expiry=1716940800000&hmac=aPwDgdpoayUvcvOjPZJhCZaYWA1CyL8_htacE8rucJQ)

**Note:** Many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.

# **Step 3: Create a temporary table**

Now search the data to give the bikeshare company the information it needs for its blog post. Make sure it includes the name of the station where the bike is used most often.

You will need to create a temp table to find the ID number of the bike that has taken the longest total trips (in minutes). You will take a sum of the minutes of each trip for each bike, then sort by descending order to find the bike that was used for the most minutes. Follow these steps:

1. Return to your Editor tab or select **Compose new query** to open a query window.

2. Use **WITH** at the start of your query to set up a temp table and name your table **longest_used_bike** on a new indented line. Note: Always be sure to use the proper snake case (underscores between each word).

3. Add a space.

4. Enter **AS** and an open parenthesis [**(**]. Press **Enter** (Windows) or **Return** (Mac) to create a new indented line.

5. Enter **SELECT**, then press **Enter/Return**, then **Tab** to create a new indented line.

6. Enter **bike_id** followed by a comma and press **Enter/Return** to create a new line.

7. Enter **SUM(duration_minutes) AS trip_duration**. This creates a column in the temp table that contains the sum of the total minutes a bike has been used. Press **Enter/Return**.

8. Press **Backspace** to align the cursor with **SELECT**, then enter **FROM**. Press **Enter/Return**, then **Tab** to create a new indented line.

9. Enter **bigquery-public-data.austin_bikeshare.bikeshare_trips** to specify the dataset you’ll be using.

10. Press **Enter/Return**, then **Backspace** to align the cursor with **SELECT**. Currently, your query should be something like this:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled.png)

11. Continue writing your query by entering **GROUP BY**, then press **Enter/Return**, followed by **Tab** to create a new indented line.

12. Enter **bike_id** to group the data by the bike_id column and press **Enter/Return**.

13. Press **Backspace** to align the cursor with **SELECT** and enter **ORDER BY**. Then press **Enter/Return** followed by **Tab** to create a new indented line.

14. Enter **trip_duration DESC** to sort the data in descending order by the column trip_duration.

15. Press **Enter/Return**, followed by **Backspace** to align the cursor with **SELECT**.

16. Enter **LIMIT 1** and **Enter/Return**.

17. Press **Backspace**, then add a closed parenthesis [**)**] if there isn’t one already on the next line. Now your text should be as follows:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%201.png)

This is how you set up your temporary table to identify the specific bike (bike_id) with the longest trip duration. However, if you run it now, it will return an error because you haven’t written any queries for the temp table yet.

# **Step 4: Write your query**

Now that you have written the portion of the query to createa temp table that will show the bike ID of the bike that was used most often, you need to write a query to find the station. To do this, join your temp table with the original table and return the station ID with the highest number of trips started.

But first, create a comment describing the purpose of the query. This will help you remember it as you’re writing it, and it enables others to understand your work if you share it.

On a new line, enter two hashtags (**##**) to begin the comment and enter something like, **find station where the longest-used bike leaves most often.** Press **Enter/Return** to make a new line and follow these steps to write your query:

1. Enter **SELECT**, then **Enter/Return** followed by **Tab** to create a new indented line.

2. Enter **trips.start_station_id** followed by a comma. Then press **Enter/Return** to create a new line.

3. Enter **COUNT(*) AS trip_ct**. This will count the number of times the bike has left each station.

4. Press **Enter/Return**, followed by **Backspace** to align the cursor with **SELECT**.

5. Enter **FROM**, then press **Enter/Return** followed by **Tab** to create a new indented line.

6. Enter **longest_used_bike AS longest** to rename your temp table with an alias.

7. Press **Enter/Return** followed by **Backspace** to align the cursor with **SELECT**. At this point, your query should be this:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%202.png)

Next, write an **INNER JOIN** to pick out the station ID that corresponds to the bike you identified in the temporary table. Follow these steps:

1. Enter **INNER JOIN**. Press **Enter/Return**, then **Tab** to create a new indented line.

2. Enter **bigquery-public-data.austin_bikeshare.bikeshare_trips AS trips**.

3. Press **Enter/Return** followed by **Backspace** to align the cursor with **SELECT**.

4. Enter **ON longest.bike_id = trips.bike_id**. This specifies that the **JOIN** is on the bike_id column in the temp table you created and in the original dataset. Press **Enter/Return** to create a new line.

5. Enter **GROUP BY**, then press **Enter/Return** followed by **Tab** to create a new indented line.

6. Enter **trips.start_station_id** to group by the start_station_id column in the original dataset.

7. Press **Enter/Return** followed by **Backspace** to align the cursor with **SELECT**.

8. Enter **ORDER BY,** then press **Enter/Return** followed by **Tab** to create a new indented line.

9. Enter **trip_ct DESC** to sort by the trip_ct column in descending order.

10. Press **Enter/Return** followed by **Backspace** to align the cursor with **SELECT**.

11. Enter **LIMIT 1**. And with that, you’ve completed the query! The full query that creates a temporary table and then queries it should be this:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%203.png)

Now, select **Run**. The dataset is substantial, so the query might take a few seconds before showing you the count.

Your query should return 3798 in the start_station_id column and 177 in the trip_ct column.  If your query returned a different result, review your steps, comparing them to the reading and checking for typos. Note, however, that this public dataset is updated from time to time and the results may change!

# **Step 5: Review other types of temp tables**

There are even more ways to create a temp table. Instead of using the **WITH** clause, you can use the **SELECT INTO** or the **CREATE TABLE** clauses.

The **SELECT INTO** clause copies data from one table into a new table, but doesn’t add the new table to the database. It’s useful if you want to make a copy of a table with a specific condition.

The **CREATE TABLE** clause is a good option when several people need to access the same temp table. This statement adds the table into the database.

Different clauses have their own strengths, so understanding how they work is helpful for using them effectively. The specific clause you use will depend on your preferences and one the project’s demands.

---

# Multiple table variations

[index (36).mp4](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/index_(36).mp4)

**Key Points:**

- **Temporary tables** are a valuable tool for organizing and streamlining your SQL analysis.
- There are three main ways to create temporary tables:
    - **WITH clause:** Creates a temporary table within a specific query.
    - **SELECT INTO statement:** Copies data from one table into a new temporary table.
    - **CREATE TABLE statement:** Creates a temporary table that is added to the database.
- **Pros and Cons of each method:**
    - **WITH clause:**
        - **Pros:** Easy to use, efficient for short-term analysis.
        - **Cons:** Not persistent, cannot be accessed outside the query.
    - **SELECT INTO statement:**
        - **Pros:** Creates a copy of data with specific conditions, keeps the database uncluttered.
        - **Cons:** Not persistent, cannot be accessed by other users.
    - **CREATE TABLE statement:**
        - **Pros:** Persistent, can be accessed by other users, allows for metadata addition.
        - **Cons:** More complex syntax, may interrupt workflow.
- **Choosing the right method:** Depends on your specific needs and preferences.
- **Additional notes:**
    - Syntax for creating temporary tables may vary depending on the RDBMS you are using.
    - Temporary tables are generally safe and efficient, but can interrupt workflow in some cases.
    - Consider alternatives like repeating code if temporary tables are not necessary.

**Definitions:**

- **Temporary table:** A table that exists only for the duration of a specific SQL session.
- **WITH clause:** A clause used to create a temporary table within a specific query.
- **SELECT INTO statement:** A statement used to copy data from one table into a new temporary table.
- **CREATE TABLE statement:** A statement used to create a new table, which can be temporary or permanent.
- **Metadata:** Data that describes other data, such as the structure and contents of a table.
- **RDBMS:** Relational Database Management System, such as BigQuery.

**Real-life Example:**

Imagine you are analyzing sales data for a company. You want to create a temporary table that includes only sales from the African region. You could use the `SELECT INTO` statement to create a temporary table called `Africa_Sales` that contains this data. This would allow you to analyze the data without cluttering up your main sales table.

---

# Work with temporary tables

**Temporary tables** are exactly what they sound like—temporary tables in a SQL database that aren’t stored permanently. In this reading, you will learn the methods to create temporary tables using SQL commands. You will also learn a few best practices to follow when working with temporary tables.

## A quick refresher on what you have already learned about temporary tables

- They are automatically deleted from the database when you end your SQL session.
- They can be used as a holding area for storing values if you are making a series of calculations. This is sometimes referred to as **pre-processing** of the data.
- They can collect the results of multiple, separate queries. This is sometimes referred to as data **staging**. Staging is useful if you need to perform a query on the collected data or merge the collected data.
- They can store a filtered subset of the database. You don’t need to select and filter the data each time you work with it. In addition, using fewer SQL commands helps to keep your data clean.

It is important to point out that each database has its own unique set of commands to create and manage temporary tables. We have been working with BigQuery, so we will focus on the commands that work well in that environment. The rest of this reading will go over the ways to create temporary tables, primarily in BigQuery.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/T82tTwpcR8qNrU8KXKfKbQ_3e11a9ce213440b082100988550ce040_Screen-Shot-2021-02-08-at-4.33.14-PM.png?expiry=1716940800000&hmac=B81kCqqZbi1U9w9T5WbF5o2IEIbMRPCZcD5Dixuufz8)

## Temporary table creation in BigQuery

Temporary tables can be created using different clauses. In BigQuery, the **WITH** clause can be used to create a temporary table. The general syntax for this method is as follows:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%204.png)

Breaking down this query a bit, notice the following:

- The statement begins with the **WITH** clause followed by the name of the new temporary table you want to create
- The **AS** clause appears after the name of the new table. This clause instructs the database to put all of the data identified in the next part of the statement into the new table.
- The opening parenthesis after the **AS** clause creates the subquery that filters the data from an existing table. The subquery is a regular **SELECT** statement along with a **WHERE** clause to specify the data to be filtered.
- The closing parenthesis ends the subquery created by the **AS** clause.

When the database executes this query, it will first complete the subquery and assign the values that result from that subquery to **new_table_data**, which is the temporary table. You can then run multiple queries on this filtered data without having to filter the data every time.

## Temporary table creation in other databases (not supported in BigQuery)

The following method isn’t supported in BigQuery, but most other versions of SQL databases support it, including SQL Server and mySQL. Using **SELECT** and **INTO**, you can create a temporary table based on conditions defined by a **WHERE** clause to locate the information you need for the temporary table. The general syntax for this method is as follows:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%205.png)

This **SELECT** statement uses the standard clauses like **FROM** and **WHERE**, but the **INTO** clause tells the database to store the data that is being requested in a new temporary table named, in this case, **AfricaSales**.

## User-managed temporary table creation

So far, we have explored ways of creating temporary tables that the database is responsible for managing. But, you can also create temporary tables that you can manage as a user. As an analyst, you might decide to create a temporary table for your analysis that you can manage yourself. You would use the **CREATE TABLE** statement to create this kind of temporary table. After you have finished working with the table, you would then delete or drop it from the database at the end of your session.

**Note:** BigQuery uses **CREATE TEMP TABLE** instead of **CREATE TABLE**, but the general syntax is the same.

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%206.png)

After you have completed working with your temporary table, you can remove the table from the database using the **DROP TABLE** clause. The general syntax is as follows:

![Untitled](SQL%20and%20temporary%20tables%20faf9f29206e94beea45b04580c9390be/Untitled%207.png)

## Best practices when working with temporary tables

- **Global vs. local temporary tables:** Global temporary tables are made available to all database users and are deleted when all connections that use them have closed. Local temporary tables are made available only to the user whose query or connection established the temporary table. You will most likely be working with local temporary tables. If you have created a local temporary table and are the only person using it, you can drop the temporary table after you are done using it.
- **Dropping temporary tables after use:** Dropping a temporary table is a little different from deleting a temporary table. Dropping a temporary table not only removes the information contained in the rows of the table, but removes the table variable definitions (columns) themselves. Deleting a temporary table removes the rows of the table but leaves the table definition and columns ready to be used again. Although local temporary tables are dropped after you end your SQL session, it may not happen immediately. If a lot of processing is happening in the database, dropping your temporary tables after using them is a good practice to keep the database running smoothly.

## For more information

- [BigQuery Documentation for Temporary Tables](https://cloud.google.com/bigquery/docs/reference/standard-sql/data-definition-language#temporary_tables)**:** Documentation has the syntax to create temporary tables in BigQuery
- [How to use temporary tables via WITH in Google BigQuery](https://www.pascallandau.com/bigquery-snippets/use-temporary-tables-with-named-subquery/?utm_source=blog&utm_medium=rss&utm_campaign=development-feed)**:** Article describes how to use **WITH**
- [Introduction to Temporary Tables in SQL Server](https://codingsight.com/introduction-to-temporary-tables-in-sql-server/)**:** Article describes how to use **SELECT INTO** and **CREATE TABLE**
- [SQL Server Temporary Tables](https://www.sqlservertutorial.net/sql-server-basics/sql-server-temporary-tables/)**:** Article describes temporary table creation and removal
- [Choosing Between Table Variables and Temporary Tables](https://www.red-gate.com/hub/product-learning/sql-prompt/choosing-table-variables-temporary-tables)**:** Article describes the differences between passing variables in SQL statements vs. using temporary tables

---

# Use Connected Sheets with BigQuery

In this reading, you will learn about Connected Sheets, a tool that allows data professionals to use basic spreadsheet functions to analyze large datasets housed in BigQuery. With Connected Sheets users don’t need to know SQL. Instead, anyone, not just data professionals, can generate insights with basic spreadsheet operations such as formulas, charts, and pivot tables.

# What is Connected Sheets?

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/oxN7Zm9DQGGjrYd5-3sWkg_e50ca8713b8f408489ceef8a15dc2ff1_oF-N6izP0wLZbug9Jol_fmcrUvE8PXFrNNlAWtMc5RvYAbNcT__u8lo5anTJe6oaUpee-7cQ3CZrc261axCaYVVOMYFzA2kpiXK0s5ltT_QwCbkhCs5O7cy_Lc5XBbWTa__sCvmXqzaG1QH_X0cZ2IM?expiry=1716940800000&hmac=3EKZoeb4BcGmAPda912c2JcwPBpkLRN8JEuf10d_g40)

Recall that BigQuery allows users to analyze petabytes (a million gigabytes) of data using complex queries. A benefit of BigQuery is that it reduces the time needed to develop insights from large datasets.

Google Sheets, on the other hand, is a spreadsheet tool that is easy to use and shareable with a familiar interface. It also allows simple and flexible analysis with tools like pivot tables, charts, and formulas.

Connected Sheets integrates both BigQuery and Google Sheets, allowing the user to analyze billions of rows of data in Sheets without any need for specialized knowledge, such as SQL.

Additionally, Connected Sheets is built to handle big data. Users won’t experience the same limitations or performance issues they’ve had in the past (such as data loss) when working with large data sets in spreadsheets.

# Why would a data analytics professional use Connected Sheets?

As a data analytics professional, Connected Sheets can help with several tasks, such as:

- Collaborating with partners, analysts, or other stakeholders in a familiar spreadsheet interface;
- Ensuring a single source of truth for data analysis without additional .csv exports;
- Defining variables so that all users are working with the same data;
- Sharing insights with your team in a secure environment; and
- Streamlining your reporting and dashboard workflows.

Many teams and industries benefit from Connected Sheets such as finance, marketing, and operations teams.

A few example use cases of Connected Sheets include:

- **Business planning:** A user can build and prepare datasets, and then find insights from the data. For example, a data analyst can analyze sales data to determine which products sell better in different locations.
- **Customer service:** A user can find out which stores have the most complaints per 10,000 customers.
- **Sales:** A user can create internal finance and sales reports. After completing, they can share revenue reports with sales reps.
- **Logistics, fulfillment, and delivery:** A user can run real-time inventory management and intelligent analytics tools.

# Connected Sheets benefits

## Collaborate with teammates and stakeholders

Since Connects Sheets lives in Google Workspace, you can easily collaborate with other teammates and stakeholders in your company. If you’d like to limit access, you also control permissions for who can view, edit, or share the data.

## Do more with familiar tools

With Connected Sheets, you can access billions of rows of BigQuery data directly in Sheets. This direct access makes it easier for all employees to track, forecast, and analyze their data to get to better decisions faster.

## Easily visualize data

You can unlock insights from your BigQuery datasets using features you’re already familiar with in Sheets, such as pivot tables, charts, and formulas. These features help visualize large datasets more easily than using a more advanced language such as SQL. However, if you know SQL, you may prefer to use it in certain situations.

## Up to date data

With Connected Sheets, data professionals can ensure they are making decisions based on a single source of truth by setting up automatic refreshes of BigQuery data in Sheets.

## Less data integrity and security risk

While users can access big data with Connected Sheets, they won’t be able to accidentally manipulate or jeopardize the integrity of the data. There’s less security risk because data isn’t stored on individual workstations, it’s stored in the cloud.

# Connected Sheets shortcomings

## Limited free pricing tier

A shortcoming of Connected Sheets is that for the free pricing tier, users only receive 1 terabyte (TB) of processed query data each month. To process more data, you will need to move to a paid tier.

## Data must be housed in BigQuery

Another shortcoming is that you will need access to your data set in BigQuery. Without access to BigQuery, you won’t be able to analyze data in Connected Sheets.

## Query will fail with large results

A third shortcoming is that the Connected Sheets query will fail if the results are too large. Your query will fail if your pivot table has a significant amount of results, which could be anywhere from 30,000 to 50,000. To reduce your results, you can use filters or limit the number of rows per breakout.

# Key takeaways

Connected Sheets provides a tremendous opportunity to analyze large data sets without specialized skills like SQL. Use familiar spreadsheet skills such as pivot tables, charts, and formulas to analyze the data. For junior data analysts in particular, Connected Sheets can help them perform key tasks within BigQuery and increase their marketable skills.

## Resources for more information

- [Get started with BigQuery data in Google Sheets](https://support.google.com/docs/answer/9702507)
- [Insights at scale with Google Sheets](https://www.youtube.com/watch?v=jMKxhOJogEE)
- [Connected Sheets product announcement](https://workspace.google.com/blog/product-announcements/connected-sheets-is-generally-available)

---