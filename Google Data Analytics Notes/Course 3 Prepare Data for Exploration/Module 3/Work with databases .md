# Work with databases

---

# All about databases

### **Key Points**

- **Databases:**
    - Definition: A collection of data stored in a computer system.
    - Importance: Enables efficient storage and retrieval of data for analysis.
    - Functionality: Allows users to find specific information needed for analysis.
    - Sorting: Enables organization of data for generating insightful reports.
- **Metadata:**
    - Definition: Data about data.
    - Importance: Provides context and understanding of the data.
    - Content: Includes information about the data's origin, creation, and purpose.
- **Data Import:**
    - Methods: Importing data directly or using SQL queries.
    - Importance: Brings data from various sources into a spreadsheet for analysis.
- **Data Preparation:**
    - Importance: Crucial step in data analysis for identifying relevant data.
    - Impact: Increases the likelihood of successful problem-solving.

### **Conclusion**

- The video emphasizes the importance of databases and data preparation in the data analysis process.
- It encourages viewers to explore the power of databases for effective data analysis.

### **Definitions**

- **Database:** A structured collection of data organized for efficient access, management, and manipulation.
- **Metadata:** Data that provides information about other data, such as its origin, format, and structure.
- **SQL:** A programming language designed for managing data in relational databases.
- **Data Import:** The process of transferring data from one source to another, such as from a database to a spreadsheet.
- **Data Preparation:** The process of cleaning, transforming, and organizing data for analysis.

---

# Database features and components

### **Key Points**

- **Databases are essential tools for data analysts.** They store and organize data, making it easier to manage, access, and analyze.
- **Databases help data analysts gain insights faster, make data-driven decisions, and solve problems.**
- **The video introduces the concept of a relational database.** This type of database contains related tables connected through shared fields.
- **Primary keys and foreign keys are crucial for connecting tables.** A primary key uniquely identifies each row in a table, while a foreign key references the primary key of another table, establishing a relationship between them.
- **Understanding primary and foreign keys is essential for working with databases.** The video provides a clear explanation of these concepts and their importance.

### **Definitions**

- **Database:** A structured collection of data organized in a way that allows for easy access, management, and analysis.
- **Relational Database:** A type of database that stores data in related tables connected through shared fields.
- **Table:** A collection of related data organized in rows and columns.
- **Primary Key:** A unique identifier for each row in a table.
- **Foreign Key:** A field in a table that references the primary key of another table, establishing a relationship between them.

### **Additional Notes**

- The video emphasizes the importance of understanding primary and foreign keys for effectively working with databases.
- The video provides a foundation for further exploration of databases and their applications in data analysis.

### **Real-Life Examples**

- **E-commerce websites:** Databases store product information, customer data, and order details.
- **Financial institutions:** Databases store account information, transaction history, and customer data.
- **Healthcare organizations:** Databases store patient records, medical history, and treatment information.

---

# Maximize databases in data analytics

- Databases enable analysts to manipulate, store, and process data. This helps them search through data a lot more efficiently to get the best insights.

## Relational databases

- A **relational database** is a database that contains a series of tables that can be connected to form relationships.
- Basically, they allow data analysts to organize and link data based on what the data has in common.
- In a non-relational table, you will find all of the possible variables you might be interested in analyzing all grouped together.
    - This can make it really hard to sort through. This is one reason why relational databases are so common in data analysis: they simplify a lot of analysis processes and make data easier to find and use across an entire database.
- **Normalization** is a process of organizing data in a relational database.
    - For example, creating tables and establishing relationships between those tables. It is applied to eliminate data redundancy, increase data integrity, and reduce complexity in a database.

## **The key to relational databases**

- Tables in a relational database are connected by the fields they have in common. You might remember learning about primary and foreign keys before. As a quick refresher, a **primary key** is an identifier that references a column in which each value is unique. In other words, it's a column of a table that is used to uniquely identify each record within that table. The value assigned to the primary key in a particular row must be unique within the entire table. For example, if customer_id is the primary key for the customer table, no two customers will ever have the same customer_id.
- By contrast, a **foreign key** is a field within a table that is a primary key in another table. A table can have only one primary key, but it can have multiple foreign keys. These keys are what create the relationships between tables in a relational database, which helps organize and connect data across multiple tables in the database.
- Some tables don't require a primary key. For example, a revenue table can have multiple foreign keys and not have a primary key. A primary key may also be constructed using multiple columns of a table. This type of primary key is called a **composite key**. For example, if customer_id and location_id are two columns of a composite key for a customer table, the values assigned to those fields in any given row must be unique within the entire table.
    
    ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/syB_f3KVRrOgf39ylaaznA_45b04edc1ba243d8b5b6d869c61a21f1_Screenshot-2021-04-29-5.11.22-PM.png?expiry=1716768000000&hmac=uPFAGjewZgo8mNqPGHDNsj5EVZDV-Y8i19D6rF_6bmo)
    

## SQL? You’re speaking my language

- As you've been learning, **Structured Query Language** (SQL) is a type of query language that enables data analysts to communicate with a database. So, a data analyst will use SQL to create a query to view the specific data that they want from within a larger dataset. In a relational database, data analysts can write queries to get data from the related tables. SQL is a powerful tool for working with databases—which is why you are going to learn more about it coming up!

---

# Inspect a dataset: A guided, hands-on tour

As a data analyst, you'll use data to answer questions and solve problems. When you analyze data and draw conclusions, you are generating insights that can influence business decisions, drive positive change, and help your stakeholders meet their goals.

Before you begin an analysis, it’s important to inspect your data to determine if it contains the specific information you need to answer your stakeholders’ questions. In any given dataset, it may be the case that:

- The data is not there (you have sandwich data, but you need pizza data)
- The data is insufficient (you have pizza data for June 1-7, but you need data for the entire month of June)
- The data is incorrect (your pizza data lists the cost of a slice as $250, which makes you question the validity of the dataset)

Inspecting your dataset will help you pinpoint what questions are answerable and what data is still missing. You may be able to recover this data from an external source or at least recommend to your stakeholders that another data source be used.

In this reading, imagine you’re a data analyst inspecting spreadsheet data to determine if it’s possible to answer your stakeholders’ questions.

## The scenario

You are a data analyst working for an ice cream company. Management is interested in improving the company's ice cream sales.

The company has been collecting data about its sales—but not a lot. The available data is from an internal data source and is based on sales for 2019. You’ve been asked to review the data and provide some insight into the company’s ice cream sales. Ideally, management would like answers to the following questions:

1. What is the most popular flavor of ice cream?
2. How does temperature affect sales?
3. How do weekends and holidays affect sales?
4. How does profitability differ for new versus returning customers?

## Download the data

You can download the data to follow along with this reading. To use the template for the sales data, click the link below and select “Use Template.”

Link to template: [Ice Cream Sales](https://docs.google.com/spreadsheets/d/1NgiKb8wCnJbUTuUkDUiNRpx9NhwncEmoKuPvgfYfOIY/template/preview?resourcekey=0-X3e7NzehG2Y74MIBhOaqeQ#gid=653912415)

OR

If you don’t have a Google account, you can download the spreadsheets directly from the attachments below:

[SalesByTempXLSX File](https://d3c33hcgiwev3.cloudfront.net/jmigEulNR7yooBLpTYe8Cw_9ecaf818f1a74b7987fe6a7d9af3c1f1_SalesByTemp.xlsx?Expires=1716768000&Signature=RUHFFK1QqMv3A~ns~KORxVnnYkCHWx5AISjgQWWZYV3L6ErddHJxEoRofzDIJXh0ZuNWNWnj81eCezQJ1PWkjKX9ei4uYJhOshX2DtteZ1vWQPoB7zrPUu-DFixvsVBPzz1iwNFibwjVkbSvF4vDu8sP-DOsi4dZedAnihkECd8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[SalesByDayXLSX File](https://d3c33hcgiwev3.cloudfront.net/B3ofmLtERPq6H5i7RFT6Pg_1ca5eec9c08941518e2c16034a2e65f1_SalesByDay.xlsx?Expires=1716768000&Signature=D8zB94GAseYCp7qmIBeUOSwvgb8NwPzkn1BGnuvUvrp3QSxf4NA83V9gXv2JO7tx77A4ozyEC6EqiwuD5z7nJFHbx5~gKQClaFyTBxgSEvlSoLfiAqDw201~j7hLoNQarlfZnYNdy8nmtBk5IZ8Vc22jVYxno1ycaSe3PGXpaZE_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[SalesByFlavorXLSX File](https://d3c33hcgiwev3.cloudfront.net/DHN9hYWCSDCzfYWFgvgwgg_b0e0d35f6a4f4bde9c84ecd0dd69c0f1_SalesByFlavor.xlsx?Expires=1716768000&Signature=Xmg8HOAuJHVgTVQsHQLWRWO5ci2wR8htwRT2WU6Vwt7KpPRLixj39gT1eWJJOAqR~~6z2bZYRe3P5ap-BtFS5KVwpPq0J3Ief2WNvyhaRFxRMObqKG~CiJ5hri7vbnPWrGRVKDvIoijRZhoqJcLq4N~tALCI~aG7Cw7hWT7PbpM_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UTyvGwMrT_m8rxsDK8_5jw_96ec24ae7f614779b31750a6b11f8d2f_dotted-line-right.png?expiry=1716768000000&hmac=AWkmIS8J4s_LdePwFmaPWnB6meJigp7B6fAtTzsim0s)

## Inspect the data

### Question 1: What is the most popular flavor of ice cream?

To discover the most popular flavor, you first need to define what is meant by "popular." Is the most popular flavor the one that generated the most revenue in 2019? Or is it the flavor that had the largest number of units sold in 2019? Sometimes your measurement choices are limited by what data you have—you can review your spreadsheet to find out if either of these definitions of “popular” make sense based on the available data.

Click the **flavors** tab on your spreadsheet to view the relevant data. The **flavors** sheet has three columns and 209 rows of data. The column headers are **week**, **units sold***,* and **flavor**. This dataset did not come with a data description, so you have to figure out the significance of the columns on your own. Based on the data, you deduce that these columns provide information about the number of units sold for each ice cream flavor, by week, in 2019

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0U2StFwfQDKNkrRcH5Aycw_fa883ec0ed39454bbc15085d48cbbcf1_Screenshot-2021-06-30-1.27.38-PM.png?expiry=1716768000000&hmac=7gBnxAobpac5fv-MRLBBIJywQJF8cRdbnbDYzJfQ-3M)

In this case, you can discover what the most popular flavor is by using units sold as your measure. In particular, you can use the **units sold** column to calculate the total number of units sold during the year for each flavor*.* Unfortunately, the dataset does not provide the annual sales amount by flavor. In this case, your next step would be to ask your stakeholders if the annual sales per flavor data is available from another source. If not, you can add a statement about the current data’s limitations to your analysis.

### Question 2: How does temperature affect sales?

To explore your second question, you click the **temperatures** tab and check out the data. The **temperatures** sheet has two columns and 366 rows of data. The column headers are **temperature** and **sales**. The data may show total 2019 sales per temperature (for instance, the first entry might sum up $39.69 in sales for three separate days that each had a high of 60 degrees). Or, the data may show  a snapshot of sales and temperature for each day in 2019 (for instance, the first entry might refer to a single day with a high of 60 degrees and $39.69 in sales).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ogou_f1zTNGKLv39c4zR0g_bdec61a7a2314b8b9cbc9069d0c15cf1_Screenshot-2021-06-30-1.28.36-PM.png?expiry=1716768000000&hmac=n5fjXfBbIVbJu7ZdZ5EWEY38JMCQ3SMduBoIp-oXPCY)

So, which is it? It’s probably a daily snapshot because there are 365 entries for temperature, and multiple rows with the same temperature and different sales values. This implies that each entry is for a single day and not a summary of multiple days. However, without more information, you can’t be certain. Plus, you don’t know if the current data is listed in consecutive order by date or in a different order. Your next step would be to contact the owner of the dataset for clarification.

If it turns out that temperature does affect sales, you’ll be able to offer your stakeholders an insight such as the following: “When daily highs are above X degrees, average ice cream sales increase by Y amount. So the business should plan on increasing inventory during these times to maximize sales.”

### Question 3: How do weekends and holidays affect sales?

Next, you click on the **sales** tab to view the data about dates of sale. The **sales** sheet has two columns and 366 rows of data. The column headers are **date** and **sales**. This data is most likely total daily sales in 2019, as sales are recorded for each date in 2019.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/FqZv0vZjQoCmb9L2Y4KAcQ_68d789ed0152495387ddf9b4b68a6cf1_Screenshot-2021-06-30-1.29.37-PM.png?expiry=1716768000000&hmac=nBKdblV2QKV7GNiKtoiuG2idr97oAnKGju5Oy4OUCX0)

You can use this data to determine whether a specific date falls on a weekend or holiday and add a column to your sheet that reflects this information. Then, you can find out whether sales on the weekends and holidays are greater than sales on other days. This will be useful to know for inventory planning and marketing purposes.

### Question 4: How does profitability differ for new customers versus returning customers?

Your dataset does not contain sales data related to new customers. Without this data, you won’t be able to answer your final question. However, it may be the case that the company collects customer data and stores it in a different data table.

If so, your next step would be to find out how to access the company’s customer data. You can then join the revenue sales data to the customer data table to categorize each sale as from a new or returning customer and analyze the difference in profitability between the two sets of customers. This information will help your stakeholders develop marketing campaigns for specific types of customers to increase brand loyalty and overall profitability.

## Key takeaways

When working on analytics projects, you won’t always have all the necessary or relevant data at your disposal.  In many of these cases, you can turn to other data sources to fill in the gaps.

Despite the limitations of your dataset, it’s still possible to offer your stakeholders some valuable insights. For next steps, your best plan of action will be to take the initiative to ask questions, identify other relevant datasets, or do some research on your own.  No matter what data you’re working with, carefully inspecting your data makes a big impact on the overall quality of your analysis.

---