# Transforming data

---

# Upload the store transactions dataset to BigQuery

In the next video, the instructor uses a specific dataset. The instructions in this reading are provided for you to upload the same dataset in your BigQuery console so you can follow along.

You must have a BigQuery account to follow along.

## Prepare for the next video

- First, download the .csv file from the attachment below.

[Lauren's Furniture Store Transaction TableCSV File](https://d3c33hcgiwev3.cloudfront.net/0cvJS5ocTSu-77CVZvn6kw_55078d160a924e49aca0837f03d995f1_Lauren-s-Furniture-Store-Transaction-Table.csv?Expires=1716854400&Signature=jAaZLH11qPqG-m1Dx3ND3pSiQLGzR37hKHwldrsD4tlE5q-8nPBo4p6aWdiAVgf8JC~1um~3B410PrcXEy2MX9mgH9LA8I5fge~vNHSu7n1EsIQguFAK7VaJUs4FV58BzEbZYLTPUuAmjSbsX3g8Fbate7vYTJ8dus6z5yCFvx4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

- Next, complete the steps below in your BigQuery console to upload the Store Transaction dataset.

**Note:** These steps will be different from what you performed before. In previous instances, you selected the **Auto detect** check box to allow BigQuery to auto-detect the schema. This time, you will choose to create the schema by editing it as text. This method can be used when BigQuery doesn't automatically set the desired type for a particular field. In this case, you will specify **STRING** instead of **FLOAT** as the type for the purchase_price field.

**Step 1**: Open your BigQuery console and select the expansion arrow next to the project you'll upload the data to. Examine the datasets listed under your project. If a **customer_data** dataset is listed, go to step 5; otherwise, continue with step 2.

**Step 2:** In the **Explorer** on the left, click the **Actions** icon (three vertical dots) next to your project name and select **Create dataset**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/k5V2rK4RSGyF1FegTvWrcg_3eb52d7d82414b599a5da107b654cdf1_5.CreateDataset.jpg?expiry=1716854400000&hmac=gULUGljeGYpXB0e_p0SLhdVI6ieNCgzS4FehQkHq1pA)

**Step 3:** In the **Create dataset** window, enter **customer_data** for the Dataset ID. Make sure the *Location type* is set to **Multi-region, US (Multiple regions in United States),** and all the default *Advanced options* remain set to the **Google-managed encryption key** option.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Vi4AMrXYSTKamxpgCbyhJw_df92fa5c794e4416a927fd81c75425f1_1.create_dataset.jpg?expiry=1716854400000&hmac=LboISXw3gtcSlz9gy6uhheVxp4LeHvAeb4F_NeLjdmI)

**Step 4:** Click **CREATE DATASET** (blue button) to add the dataset to your project.

**Step 5:** In the **Explorer** pane, click on the expansion arrow under your project name, and then click the **customer_data** dataset.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EUkPC9veR-6OuxIfQHJfSw_6964c4de086f4277af8151b2490e26f1_2.data_info.jpg?expiry=1716854400000&hmac=cMOeOU3-wbRr4-bYnf8NMpBBhYQC3wcUwKvsIwoHZ_Q)

**Step 6:** In the **Dataset info** page, click the blue **+ CREATE TABLE** button to open the **Create table** window.

**Step 7:** Under **Source**, for the **Create table from** selection, choose where the data will be coming from.

- Select **Upload**.
- Click **Browse** to select the Store Transaction Table .csv file you downloaded.
- Choose **CSV** from the file format drop-down.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JlRSacCNRaWCErQkRSjDag_f4ca2ae11d4a49cfb4a34ab4366ad5f1_3.createtablewindow.jpg?expiry=1716854400000&hmac=cN2jcisgwtlIYHATV4cPghmXhxPLsfxRadMLx3OkvDk)

**Step 8:** For Table name, enter **customer_purchase**.

**Step 9:** For Schema, click the toggle switch for **Edit as text**. This opens up a box for the text.

**Step 10:** Copy and paste the following text into the box. Be sure to include the opening and closing brackets. They are required.

[
  {
    "description": "date",
    "mode": "NULLABLE",
    "name": "date",
    "type": "DATETIME"
  },
  {
    "description": "transaction id",
    "mode": "NULLABLE",
    "name": "transaction_id",
    "type": "INTEGER"
  },
  {
    "description": "customer id",
    "mode": "NULLABLE",
    "name": "customer_id",
    "type": "INTEGER"
  },
  {
    "description": "product name",
    "mode": "NULLABLE",
    "name": "product",
    "type": "STRING"
  },
  {
    "description": "product_code",
    "mode": "NULLABLE",
    "name": "product_code",
    "type": "STRING"
  },
  {
    "description": "product color",
    "mode": "NULLABLE",
    "name": "product_color",
    "type": "STRING"
  },
  {
    "description": "product price",
    "mode": "NULLABLE",
    "name": "product_price",
    "type": "FLOAT"
  },
  {
    "description": "quantity purchased",
    "mode": "NULLABLE",
    "name": "purchase_size",
    "type": "INTEGER"
  },
  {
    "description": "purchase price",
    "mode": "NULLABLE",
    "name": "purchase_price",
    "type": "STRING"
  },
  {
    "description": "revenue",
    "mode": "NULLABLE",
    "name": "revenue",
    "type": "FLOAT"
  }
]

**Step 11:** Scroll down and expand the **Advanced options** section.

**Step 12:** For the **Header rows to skip** field, enter **1**.

**NOTE**: It is very important that you don't skip the last step, or you will receive 'parsing' errors, as BigQuery will try to apply the schema editing functions to the title row.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Q0OCeG0jQ8i6kqiuPuAPtg_20acb2255a37442fbb35572b4bf0a9f1_4.advancedsettings.jpg?expiry=1716854400000&hmac=Fll6xpFFBN0z3kIrJFGvEYfHqJ8a-aqmqbA5fqSaXdc)

**Step 13:** Click **Create** **table** (blue button). You will now see the **customer_purchase** table under your **customer_data** dataset in your **Explorer** pane.

**Step 14:** Click the **customer_purchase** table and in the **Schema** tab, confirm that the schema matches the schema shown below.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NhJwePeoT3WScHj3qJ91dw_5d1344c89b0e4a528fee3326f84bdbf1_schema.png?expiry=1716854400000&hmac=1eSmgDc80rUpoypvf_jQhTcf901JIa0gIcVtWzkrFVo)

**Step 15:** Click the **Preview** tab and confirm that your data matches the data shown below.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HxvsqoMeQQWb7KqDHiEFXg_f3fb8115d0004f1eacc45d2cb8cee4f1_preview.png?expiry=1716854400000&hmac=jjuMzA0YhWOl5-4anLEwtJghv18ovtymLGmf9Qpgp-w)

---

# Advanced data-cleaning functions Part 1

[index (3).mp4](Transforming%20data%202317490983f0447eb0f9e5d6b4dca626/index_(3).mp4)

**Key Points:**

- **Importance of Data Cleaning:** Clean data is crucial for accurate analysis and insights.
- **CAST Function:** This function converts data from one type to another, ensuring proper formatting and analysis.
- **Example:** Converting string data to numerical data for correct sorting and analysis.
- **Benefits of CAST Function:**
    - Enables accurate data analysis.
    - Allows for proper data sorting and filtering.
    - Makes data usable for various tasks.
- **Real-world Application:** Lauren's Furniture Store uses CAST to convert purchase price data from string to numerical format, allowing for accurate analysis and sorting.
- **Additional Functions:** The video mentions other advanced functions for data cleaning, which will be covered in future lessons.

**Definitions:**

- **CAST Function:** A function in SQL that converts data from one data type to another.
- **Data Type:** The format of data, such as string, number, date, or time.
- **Typecasting:** The process of converting data from one type to another.
- **Data Analysis:** The process of examining and interpreting data to extract meaningful insights.

---

# Advanced data-cleaning functions Part 2

[index (4).mp4](Transforming%20data%202317490983f0447eb0f9e5d6b4dca626/index_(4).mp4)

**Key Points:**

- **CAST Function:**
    - Used to change the data type of a column.
    - Example: Converting a date-time field to a date field.
    - Syntax: `CAST(column_name AS data_type)`
- **CONCAT Function:**
    - Used to combine multiple text strings into a single string.
    - Example: Creating a unique key by combining product code and color.
    - Syntax: `CONCAT(string1, string2, ...)`
- **COALESCE Function:**
    - Used to return the first non-null value from a list of columns.
    - Example: Displaying product name if available, otherwise displaying product code.
    - Syntax: `COALESCE(column1, column2, ...)`

**Definitions:**

- **Data Cleaning:** The process of identifying and correcting errors, inconsistencies, and missing values in data.
- **Data Type:** The format of data in a column, such as text, number, date, or time.
- **Null Value:** A missing value in a database table.
- **Unique Key:** A combination of columns that uniquely identifies a row in a table.

---