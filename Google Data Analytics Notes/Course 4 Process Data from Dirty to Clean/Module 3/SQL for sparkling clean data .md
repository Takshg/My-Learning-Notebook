# SQL for sparkling clean data

---

# Use SQL to clean data

**Key Points:**

- **Importance of Data Cleaning:** Dirty data can lead to inaccurate insights and poor decision-making. Cleaning your data is essential for ensuring the quality of your analysis.
- **Data Cleaning with SQL:** SQL is a powerful tool for cleaning large datasets. It offers a variety of functions for transforming data, cleaning strings, and verifying results.
- **Basic SQL Functions:** The video introduces basic SQL functions for data cleaning, including:
    - `SELECT`: Retrieves specific data from a table.
    - `WHERE`: Filters data based on specific conditions.
    - `ORDER BY`: Sorts data in ascending or descending order.
    - `GROUP BY`: Groups data based on specific criteria.
    - `HAVING`: Filters grouped data based on specific conditions.
    - `DISTINCT`: Removes duplicate rows from a table.
    - `REPLACE`: Replaces specific characters or strings in a column.
    - `TRIM`: Removes leading and trailing spaces from a string.
    - `SUBSTRING`: Extracts a specific substring from a string.
    - `LENGTH`: Returns the length of a string.
- **Developing Basic Search Queries:** The video demonstrates how to develop basic search queries for databases using SQL.
- **Applying Basic SQL Functions:** The video shows how to apply basic SQL functions for transforming data and cleaning strings.

**Definitions:**

- **Data Cleaning:** The process of identifying and correcting errors, inconsistencies, and missing values in a dataset.
- **SQL:** Structured Query Language, a programming language used to manage and manipulate data in relational databases.
- **Data Transformation:** The process of converting data from one format to another.
- **String Cleaning:** The process of removing unwanted characters or formatting from text data.
- **Search Query:** A statement used to retrieve specific data from a database.

---

# How a junior data analyst use SQL

In this reading, you will learn more about how to decide when to use SQL, or Structured Query Language. As a data analyst, you will be tasked with handling a lot of data, and SQL is one of the tools that can help make your work a lot easier. SQL is the primary way data analysts extract data from databases. As a data analyst, you will work with databases all the time, which is why SQL is such a key skill. Let’s follow along as a junior data analyst uses SQL to solve a business task.

## The business task and context

The junior data analyst in this example works for a social media company. A new business model was implemented on February 15, 2020 and the company wants to understand how their user-growth compares to the previous year. Specifically, the data analyst was asked to find out how many users have joined since February 15, 2020.

## Spreadsheets functions and formulas or SQL queries?

Before they can address this question, this data analyst needs to choose what tool to use. First, they have to think about where the data lives. If it is stored in a database, then SQL is the best tool for the job. But if it is stored in a spreadsheet, then they will have to perform their analysis in that spreadsheet. In that scenario, they could create a pivot table of the data and then apply specific formulas and filters to their data until they were given the number of users that joined after February 15th. It isn’t a really complicated process, but it would involve a lot of steps.

In this case, the data is stored in a database, so they will have to work with SQL. And this data analyst knows they could get the same results with a single SQL query:

![Untitled](SQL%20for%20sparkling%20clean%20data%20bd98508494c94ef88e2f657e145add0b/Untitled.png)

Spreadsheets and SQL both have their advantages and disadvantages:

| **Features of Spreadsheets** | **Features of SQL Databases** |
| --- | --- |
| Smaller data sets | Larger datasets |
| Enter data manually | Access tables across a database |
| Create graphs and visualizations in the same program | Prepare data for further analysis in another software |
| Built-in spell check and other useful functions | Fast and powerful functionality |
| Best when working solo on a project | Great for collaborative work and tracking queries run by all users |

## Key takeaways

When it comes down to it, where the data lives will decide which tool you use. If you are working with data that is already in a spreadsheet, that is most likely where you will perform your analysis. And if you are working with data stored in a database, SQL will be the best tool for you to use for your analysis. You will learn more about SQL coming up, so that you will be ready to tackle any business problem with the best tool possible.

---

# Spreadsheet vs. SQL

**Key Points:**

- **Similarities:**
    - Both spreadsheets and SQL can be used for data cleaning and analysis.
    - Both offer tools for performing arithmetic, using formulas, and joining data.
    - Both can be used to find specific information in large datasets.
- **Differences:**
    - Spreadsheets are programs like Excel or Google Sheets, while SQL is a language used to interact with databases.
    - Spreadsheets are better for smaller datasets, while SQL is better for larger datasets (millions of rows or more).
    - Spreadsheets are stored locally, while SQL data is stored in a database and can be accessed by multiple users.
    - Spreadsheets have built-in functionalities like spell check, while SQL offers version control and change tracking.
- **Use Cases:**
    - Spreadsheets are good for individual work with small datasets.
    - SQL is good for collaborative work with large datasets.

---

# SQL dialects and their uses

In this reading, you will learn more about SQL dialects and some of their different uses. As a quick refresher, **Structured Query Language**, or SQL, is a language used to talk to databases. Learning SQL can be a lot like learning a new language—including the fact that languages usually have different dialects within them. Some database products have their own variant of SQL, and these different varieties of SQL dialects are what help you communicate with each database product.

These dialects will be different from company to company and might change over time if the company moves to another database system. So, a lot of analysts start with Standard SQL and then adjust the dialect they use based on what database they are working with. Standard SQL works with a majority of databases and requires a small number of syntax changes to adapt to other dialects.

As a junior data analyst, it is important to know that there are slight differences between dialects. But by mastering Standard SQL, which is the dialect you will be working with in this program, you will be prepared to use SQL in any database.

## More information

You may not need to know every SQL dialect, but it is useful to know that these different dialects exist. If you are interested in learning more about SQL dialects and when they are used, you can check out these resources for more information:

- LearnSQL’s blog, [**What Is a SQL Dialect, and Which One Should You Learn?**](https://learnsql.com/blog/what-sql-dialect-to-learn/)
- Software Testing Help’s article, [**Differences Between SQL Vs MySQL vs SQL Server**](https://www.softwaretestinghelp.com/sql-vs-mysql-vs-sql-server/)
- Datacamp’s blog, [**SQL Server, PostgreSQL, MySQL... what's the difference? Where do I start?**](https://www.datacamp.com/community/blog/sql-differences)Note that there is an error in this blog article. The comparison table incorrectly states that SQlite uses subqueries instead of window functions. Refer to the [**SQLite Window Functions](https://sqlite.org/windowfunctions.html)** documentation for proper clarification.
- SQL Tutorial’s tutorial, [**What is SQL**](https://www.sqltutorial.org/what-is-sql/)

---

# Hands-On Activity: Processing time with SQL

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RwryPQ36Q3GK8j0N-oNxVQ_a85206e9a37d4efe82540bc35a71c0ca_line-y.png?expiry=1716854400000&hmac=Bo06ijApwmUKWgLHV_vM6eYQJ_-xKhWTp3h_6NdJu1c)

In this activity, you’ll explore how the amount of data processed by a SQL query affects how long it takes the query to run.

By the time you complete this activity, you’ll be familiar with the different units used to measure data quantity. This will help you understand how dataset size affects the amount of time queries take to run and how valuable tools like SQL can be to data analysts.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Understand how data is measured**

All information in a computer is represented as a binary number consisting solely of 0’s and 1’s. Each 0 or 1 in a number is a bit, which is the smallest unit of storage in computers. Data is measured by the number of bits it takes to represent it. This is then described in bytes, which are equal to 8 bits.

Take a moment to examine the table below to understand each data measurement and its size relative to the others..

| **Unit** | **Abbreviation** | **Equivalent to** | **Example (with approximate size)** |
| --- | --- | --- | --- |
| Byte | B | 8 bits | 1 character in a string (1 byte) |
| Kilobyte | KB | 1024 bytes | A page of text (4 kilobytes) |
| Megabyte | MB | 1024 Kilobytes | 1 song in MP3 format (2-3 megabytes) |
| Gigabyte | GB | 1024 Megabytes | 300 songs in MP3 format (1 gigabyte) |
| Terabyte | TB | 1024 Gigabytes | 500 hours of HD video (1 terabyte) |
| Petabyte | PB | 1024 Terabytes | 10 billion Facebook photos (1 petabyte) |
| Exabyte | EB | 1024 Petabytes | 500 million hours of HD video (1 exabyte) |
| Zettabyte | ZB | 1024 Exabytes | All the data on the internet in 2019 (4.5 ZB) |

# **Step 2: Relate to the amount of data in the world**

Now that you’ve explored data measurements, think about the amount of data in the world. It’s growing at an incredible pace largely due to the more than 5.3 billion people in the world connected to the internet (as of November 2023). Smartphones and other internet-connected devices generate a staggering amount of new data. Many experts believe that the amount of all the data on the internet will swell to 175 ZB by the end of 2025!

**Dataset size is important**

The size of the dataset you’re working with usually determines which tool—spreadsheets or SQL—is best suited for the task. Spreadsheets often start to have performance issues as dataset sizes increase beyond a few megabytes. SQL databases are much better at working with larger datasets that have billions of rows with sizes measured in gigabytes. Yet the dataset’s size still matters here: Even in SQL, it takes longer for queries to complete when they’re run on longer datasets, depending on the query’s content and the number of rows SQL has to process.

# **Step 3: Prepare to query large datasets**

You’ll now discover for yourself how query runtimes change with dataset size by running some queries on a huge dataset—Wikipedia!

1. On the [Enable the BigQuery sandbox](https://cloud.google.com/bigquery/docs/sandbox) page, select **Go to BigQuery**. If you have a free trial version of BigQuery, you can use that instead.
    1. **Note:** BigQuery Sandbox frequently updates its user interface. The latest changes may not be reflected in the screenshots presented in this activity, but the principles remain the same. Adapting to changes in software updates is an essential skill for data analysts, and it’s helpful for you to practice troubleshooting. You can also reach out to your community of learners on the discussion forum for help.
2. The main section is the home screen from which you can access the Query Editor. You can navigate to different projects and data sets available to you using the Explorer menu.
3. Select **Compose a new query** so that you can work through an example query.

# **Step 4: Run a large query**

1. The query below sorts and filters data from the dataset **bigquery-samples.wikipedia_benchmark.Wiki10B**, which is a sample from the Wikipedia public dataset that contains 10 billion rows. To access the dataset, all you need to do is run the query.

Copy and paste the following query into the Query editor then select **Run** to run it. The formatting improves readability, but it’s okay if it changes when copied over—it won’t affect how your code runs. If you choose to type out the query, make sure you use backticks around the table, rather than quotation marks.

![Untitled](SQL%20for%20sparkling%20clean%20data%20bd98508494c94ef88e2f657e145add0b/Untitled%201.png)

**Note:** Later in this course and program, you will learn what each part of this query means and how to use its functions in your own work.

After the query finishes, you will get a table that displays the total number of times each Wikipedia page with “Google” in the title has been viewed in each language.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Qu2Z_5aQSr2tmf-WkBq9PA_b40dcde067da40c6a4cbf0a170d45add_DAC4M3L2HO1-ss1.png?expiry=1716854400000&hmac=2AR-i0YksIVyaTpvPcshGIkr-eGwTIrmcIh4KObwRtg)

2. Note the information that BigQuery provides on the query you just ran. (Remember, many of the public databases on BigQuery are living records and, as such, are periodically updated with new data. Throughout this course (and others in this certificate program), if your results differ from those you encounter in videos or screenshots, there's a good chance it is due to a data refresh.)

You’ll find that the query processes more than 415 gigabytes of data when run—very impressive for 15 seconds! If you run the query on this dataset again, the runtime will be almost instant (as long as you haven’t changed the default caching settings). This is because BigQuery caches (stores in the background) the query results to avoid extra work if the query needs to be rerun.

# **Step 5: Run a larger query**

Now, run the same query on a 100-billion-row version of the Wikipedia dataset. Copy and paste the following query into the editor and run it:

**Note:** This query will only run in the free trial account, not in the sandbox version of BigQuery. If you use a sandbox account, use the results presented below.

![Untitled](SQL%20for%20sparkling%20clean%20data%20bd98508494c94ef88e2f657e145add0b/Untitled%202.png)

After the query finishes, you will get a table that displays the total number of times each Wikipedia page with “Google” in the title has been viewed in each language.

Image of the query results indicating that the query was completed in 27.6 seconds and processed 4.1 TB of data. The table returned by the query includes the rows language, title, and views.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Q3F9EuY2Q2az8vkrB0NYjg_1e003c963e6e4ad6a548e4a10b634be1_4EA6V-1Vx-Eu-2vpd7tjkHR1jVoORu0-NJ75mgv8pSZKHyQ2xKpC6hf-S2TkVI-uhDnQAFoxuzMc2ET949433DbUC7FdwNotcPU1Ngog3O3CNJVAmUxHPtTx94nEInEHpcUG5G1rG9p5HA3-inJIG4irkf_sBZRsLM-hh1j67sdAkgFf8s_FYcSKeiAeBOY?expiry=1716854400000&hmac=-ll8vBSpjOf2pSstzCydXPDl8Rvy-wKzIgcFxJ1YTsE)

Notice that this query takes longer to run than the first query, at least 25-30 seconds. At 100 billion rows, the query processed 4.1 terabytes of data!

---