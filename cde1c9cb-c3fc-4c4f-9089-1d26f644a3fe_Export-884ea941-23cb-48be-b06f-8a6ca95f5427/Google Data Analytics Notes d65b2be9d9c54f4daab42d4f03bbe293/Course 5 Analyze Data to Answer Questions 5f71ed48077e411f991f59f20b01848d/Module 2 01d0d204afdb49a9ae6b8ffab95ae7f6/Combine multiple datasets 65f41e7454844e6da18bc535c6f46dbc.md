# Combine multiple datasets

---

# Import and combine data in spreadsheets and databases

In earlier lessons, you discovered how to use the **IMPORTRANGE** and **CONCATENATE** functions in spreadsheets. In this reading, you will have the opportunity to extend your knowledge about these concepts to SQL queries.

## Import data

As a data analyst, there are many occasions where you will need to import data from one file or location to another. Both spreadsheets and SQL include functionality that enables you to import data.

### **Import data in spreadsheets**

As you learned earlier, in spreadsheets you use the **IMPORTRANGE** function to import a range of cells from another spreadsheet into your current spreadsheet. The syntax is: **=IMPORTRANGE(spreadsheet_url, range_string)**.

In this formula, **spreadsheet_url** is the URL of the spreadsheet from which you want to import data. The specific cells you want to import, such as A2:B6, are specified by **range_string**. If the spreadsheet has multiple tabs, you also need to specify the name of the tab as part of the range.

An example of this is a company that needs to track who made retirement contributions so that it can make sure the company match is correctly distributed. The analysts would use **IMPORTRANGE** to pull all retirement contribution information into a spreadsheet that contains all of the employees year-end salaries and bonuses. This enables them to determine which employees made contributions and are eligible for matching funds.

### **Import data in SQL**

In contrast to spreadsheets, SQL does not include a function for importing data. Instead, a method you can use to import data from one table to another is to use the **INSERT INTO** command together with a **SELECT** statement. The syntax is:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled.png)

In this syntax, the SQL query inserts rows from a source table into a destination table based on the **WHERE** clause.

For example, imagine you work for a retail company that stores its sales and customer information in a SQL database. The marketing director asks you to provide them with a table containing the names and addresses of customers who have not made a purchase this year and who live in specific postal codes. One way you could gather this information is to use the **INSERT INTO** along with the **SELECT** and **WHERE** commands, as follows:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%201.png)

## Combine data

Another tool in your data analyst toolkit is your ability to join together two or more text strings that are stored in separate columns or fields. For example, you might want to combine a customer’s first and last name to create mailing labels for a marketing promotion. In both spreadsheets and SQL, joining together text strings is referred to as *concatenation*.

### **Combine data in spreadsheets**

In spreadsheets, you use the **CONCATENATE** function to join together two or more text strings, such as combining street addresses and primary contacts in a business’ vendor database.

The basic syntax is **=CONCATENATE(item 1, item 2)**. You can add multiple items by separating them with commas. Where appropriate, such as when you’re combining a customer’s first and last name, you should add a space between the items you’re combining by typing quotation marks space quotation marks [“ ”] between the items. Separate this information by a comma as well. This would change the formula to: **=CONCATENATE(item 1, " ", item 2)**.

### **Combine data in SQL**

In SQL, use the **CONCAT** function to join strings together to create new text strings. You might combine data simply to improve the readability of reports (such as combining a customer’s first and last name when generating a customer list). Or, you might combine data to generate a unique identifier for the rows in a table. Here is the basic syntax:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%202.png)

Notice that this syntax includes " " so that there is a space between the combined fields. With this syntax, SQL combines field1 and field2 with a space between them.

By default, SQL includes the field names as headers when you run a query. However, if you use the **CONCAT** function, SQL doesn’t know what to use as a header. For this reason, you should include an alias for the combined fields to help with readability. You give the combined fields an alias by using **AS**:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%203.png)

For example, if you plan to use **CONCAT** to combine the first and last names of your company’s customers into a single expression, you could use this query:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%204.png)

## Key takeaways

Data can be imported and combined in both spreadsheets and SQL databases. To import data into a spreadsheet, use the **IMPORTRANGE** function. To import data into a SQL table, use the **INSERT INTO**, **SELECT**, and **WHERE** commands. Use **CONCATENATE** to combine two or more data strings in spreadsheets. In SQL, use the **CONCAT** function to combine fields.

---

# Step-by-Step: Merge text strings to gain insights

[index (16).mp4](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/index_(16).mp4)

This reading outlines the steps the instructor performs in the following video, [Merge text strings to gain insights](https://www.coursera.org/learn/analyze-data/lecture/9V6L5). In the video, the instructor uses SQL’s **CONCAT** function to combine strings from multiple columns to create a new column. Additionally, the instructor uses other SQL commands such as **AVG**, **GROUP BY**, and **ORDER BY** to gain insights about the new column.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

## What you’ll need

If you would like to follow along with the instructor, you will need to log in to your BigQuery account to use the open (public) dataset called **new_york**. To access the dataset, make sure you have the **bigquery-public-data** project starred in your BigQuery Explorer pane. Then, scroll through the datasets in the **bigquery-public-data** project to find the **new_york** dataset. The table you will use is called **citibike_trips**. Select this table and then select the **Query** button.

**Important note:** BigQuery has two different databases that contain very similar information: **new_york** and **new_york_citibike**. Both of these databases contain tables called **citibike_trips**. However, these tables are not exactly the same between both databases. This step-by-step and the subsequent video use the **new_york** database. You will need to scroll to find this dataset under the **bigquery_public_data** project in the Explorer pane; it does not come up in a search.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zzv9vE0bT16_Ztab42MffQ_51911f95aafa44a198b679c17a3ce1f1_DA_C5_M2_SbS_Merge-text-strings.png?expiry=1716940800000&hmac=IOe5wNcE3Pfyhh5YsISmpAzz5ipXxNx1oFGTXBoOPUI)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716940800000&hmac=UN0tlF7lkA95qCr5MP0pe0_funmKbzc9reSo7V0cU3E)

## Example: Use **CONCAT** on the bike sharing dataset

The **CONCAT** function can combine data from separate columns to provide new insights.

- In the BigQuery editor, enter **SELECT** and press Enter (Windows) or Return (Mac).
- Enter **usertype,** on line 2.
- On line 3, enter **CONCAT(start_station_name," to ", end_station_name)** to combine the names of the beginning and ending stations for each trip in a new column. This will create one column of routes.
- Enter **AS route,** at the end of line 3 to name the column route.
- On line 4, enter **COUNT (*) as num_trips,** to count the number of trips. The asterisk tells SQL to count the number of rows you’re selecting. Each row represents a trip, so you can count all of the rows you’ve selected to count the number of trips.
- Next, calculate the average trip duration for each route. On line 5, enter:
**ROUND(AVG(cast(tripduration as int64)/60),2) AS duration**

This line of code accomplishes several tasks:

- It uses the **CAST** function to cast **tripduration** as an integer and divides that number by 60 to convert the number from seconds to minutes.
- It uses the **AVG** function to find the average duration of each route.
- It uses the **ROUND** function to round the output to 2 decimal places.
- It uses the **AS** command to give this output the alias **duration**.

**Note 1:** BigQuery stores numbers in a 64-bit memory system, which is why there's a 64 after integer in this case.

**Note 2:** While explaining this code, the instructor says "divide by the number of rows." Instead, they meant "divide by 60."

- Enter **FROM** on line 6 and press return.
- Enter **`bigquery-public-data.new_york.citibike_trips`** on line 7 (enclosed in back-ticks).
- Enter **GROUP BY** on line 8.
- Enter **start_station_name, end_station_name, usertype** on line 9.
- Enter **ORDER BY** on line 10 to tell SQL how to organize this data.
- Enter **num_trips DESC** on line 11 to sort it in descending order.
- Enter **LIMIT 10** on line 12.
- Your completed query should match the following code:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%205.png)

- Select **RUN** to view the results.

Now you can easily read these route names and trace them back to real places. You can also explore the types of customers taking each route. This type of information can help decision-makers at the bike-sharing company understand their user base in different parts of the city and where to keep more bikes for people to rent.

---

# Hands-On Activity: Combine multiple pieces of data

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/G-KePoi0R2Sinj6ItBdkMg_2d69ab4b929f40f2b472a78fdd5ed880_line-y.png?expiry=1716940800000&hmac=SEphjdYBdoz0TRm7EByd3ssnqoR5bANw6SL-vCmMzHc)

In previous activities, you gained experience using spreadsheet functions for manipulating and cleaning data. In this activity, you’ll use the **CONCAT** and **CONCATENATE** functions to help you quickly and efficiently combine multiple pieces of raw data into new data.

By the time you complete this activity, you will be able to use these functions to combine data. This will enable you to simplify and condense data, which is important for processing and cleaning data in your career as a data analyst.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the template**

To get started, you will need the **CONCAT** function exercise spreadsheet.

To use the template for the spreadsheet, click the link below and select “Use Template.”

Link to template: [CONCAT Function Exercise Spreadsheet](https://docs.google.com/spreadsheets/d/1Na9M4xb-3CA746BHECX75n3B9V04pxLo0xNs9i8jMNo/template/preview)

OR

If you don’t have a Google account, you can download the spreadsheet directly from the attachment below.

[Dataset for Project_ CONCAT functionXLSX File](https://d3c33hcgiwev3.cloudfront.net/s7PLxn9URlSzy8Z_VDZUqQ_90e1fe6271aa400cb7a05c5ba5c40a56_Dataset-for-Project_-CONCAT-function.xlsx?Expires=1716940800&Signature=MWDHZK6q-~wBGBKbdJLWXuw9aK7U4lnz7Kbt0gXnpF7oMdNk4P~jXJSeaMNr0v5vCW7BhAJNrKz0jxI9fRg8gKoXf2qJYMjozqkT7H435d2JgUzSEWMgg-xFLXrjJ-Hu5B9Z9WP5EVFcPC9WXHp1peV1iPIP9fOFVD5iGlwaJc4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qtHf29c3TVmR39vXNw1Zsw_b9d515d45f0a44c08b08eff39d062ac4_dotted-line-right.png?expiry=1716940800000&hmac=SPR6Cdk81cbVcff4HwIg5ucwDFabLPQkYkDva12GM6Y)

# **Step 2: Why Use the CONCAT and CONCATENATE functions**

Occasionally, you will encounter a dataset with data values in separate cells that you want to combine as a single value in a single cell. This is common when dealing with names and dates. The dataset may have separate columns for first names and last names, but you may want a column with the full names.

City / state and month / year combinations are also often desirable to have together, as they are likely to be recorded together.

The **CONCAT** function in spreadsheets can combine these kinds of data.

# **Step 3: Combine data from two cells**

First, using the spreadsheet you downloaded, you’ll combine the two sets of names in columns **First Name** and **Last Name** in a new column called **Full Name**.

To do this, follow these steps:

1. Click on cell **F2**. This is where you start the data for the new column. After you click on the cell, enter **=CONCAT(A2,B2)** into the function bar and hit **Enter (Windows)** or **Return (Mac)**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VJmHYl-ZRPuZh2JfmaT70A_089105fc9fd14fa1866242b5e30e4f4a_DAC5M2L3SR1-ss1.png?expiry=1716940800000&hmac=6TSgDf0l1wWmwL9GF8BYiNGWmRSqRYqmFbudMRGV80o)

Once you press enter, the following data should appear in the cell:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sON7YRbeRT2je2EW3uU9Jg_dc23817e34c249bab9a931c63b0999f1_Screen-Shot-2021-05-04-at-11.25.52-PM.png?expiry=1716940800000&hmac=5Grg-BJ_zr1MpMIgSQdVkckXulBKYRlijoY-IDSPfho)

You have merged or, technically, **concatenated** the two data values from cells **A2** and **B2**. Because you listed A2 first in the **CONCAT** function argument, it comes first in the final result.

Notice that the two names were combined without a space between them.

If you want to put the space in between, you need to use the full **CONCATENATE** function, which allows you to combine multiple strings.

2. Click again on the cell **F2**. In the function call, place a space in quotes between **A2** and **B2** separated by commas.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qgDwfeUdTH-A8H3lHRx_ug_51b01fa1bb06482aa39057a85b854a28_Screenshot-2021-03-04-3.00.47-PM.png?expiry=1716940800000&hmac=2zrYmgEY2kg3ScOgbeAZeULEpG040i2CMOKk_xx3xmk)

Once you press enter or return, your screen should appear like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/BVGEUlAWQ2mRhFJQFkNpIA_7e300aff4df64fa7a03628aafac3bc41_DAC5M2L3SR1-ss4.png?expiry=1716940800000&hmac=koJDNkL4KJyoPi3RvaDHJpY0f3_c8QIS3xF4BV3YUIc)

Now there is a space between the first name and the last name.

3. Next, repeat this process for all the remaining cells in **Column F**. Of course, you don't want to do this manually for each cell. (Especially if the dataset were larger, it would be laborious to do this cell-by-cell.) Luckily, you can fill out the data in the column by using your mouse.

4. Click on the cell **F2**. Locate the small square in the lower-right corner of the highlighted boundary of the cell.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xae5rCNOSBmnuawjTvgZOg_af0d136c5a5943cfbc27c70c17fbb45e_Screenshot-2021-03-04-3.12.50-PM.png?expiry=1716940800000&hmac=1T1anzlRXeMkADu36s0D20VnQir2SHocdXQhrvVAMsA)

5. Click on this square, drag your mouse to the bottom of the column, and release. All the cells in the column should populate with the full name of the appropriate president.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QUYtzlWeTeGGLc5Vnr3hbw_ed5444b9c5ac4ae68038693bec94ad58_DAC5M2L3SR1-ss6.png?expiry=1716940800000&hmac=FPX9kaZudROfWWxx8yhhRtsKNMnzLhM9G2GrXjroiOA)

- Note: While it does not happen in this dataset, you may have extra spaces in your result after you **CONCAT**. If you notice you have extra spaces, you can use the **TRIM** function to remove them.

## 

# **Step 4: Combine data from three cells**

The procedure for combining three pieces of data from different cells is almost identical to what you just did. The only difference is that you include a third cell in the full **CONCATENATE** argument.

Now, combine the month, day, and year into a single data value: **Date**. This will occupy column **G**.

1. Click on the cell where you would like the new data to start. Here, this is cell **G2**. 

2. Enter the **CONCAT** command as **=CONCATENATE(C2," ",D2,", ",E2)**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/OlnWlsu6TO-Z1pbLuszv3Q_549d3c7ab0d74a3683a9db7c1ca7f4cc_DAC5M2L3SR1-ss7.png?expiry=1716940800000&hmac=1lw9wftVEy3B0RISlNm3c8DYgtnWaxRZcXFEHx-VwTM)

Pay particular attention to the extra strings you added between the month and the day, and between the day and the year. This is how you get the spaces and comma in your final result.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tbuZ6pnGTvy7meqZxq78wQ_88d70db0716442dbb7704110dd1e3d88_DAC5M2L3SR1-ss8.png?expiry=1716940800000&hmac=Bio_7YTw983wonlziFSGytnqnieW1VG3RBdBDrDbYXo)

3. Fill out the rest of the column using the same click-and-drag technique as before. Your screen should appear like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MY4hBsQdTRWOIQbEHe0VGQ_5eec4344a4354f98813c4ae792802065_DAC5M2L3SR1-ss9.png?expiry=1716940800000&hmac=avJvbXJ-NfQphPmYzA1-jQSHtpj5zVygR0tedpZ3Slw)

Congratulations! You’ve combined data in spreadsheets using the **CONCAT** and **CONCATENATE** functions.

---

# Step-by-Step: Strings in spreadsheets

[index (17).mp4](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/index_(17).mp4)

This reading outlines the steps the instructor performs in the next video, [Strings in spreadsheets](https://www.coursera.org/learn/analyze-data/lecture/syKyK/strings-in-spreadsheets). In this video, the instructor demonstrates the **LEN**, **LEFT**, **RIGHT**, and **FIND** functions and discusses how you can use them to better understand your data.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

If you’d like to access the spreadsheet the instructor uses in this video, click the link to the dataset to create a copy. If you don’t have a Google account, you may download the data directly from the attachments below. Note that this is a larger database so it may take a moment or two to load.

Link to the Citi Bike dataset: [Citi Bike Trip Data](https://docs.google.com/spreadsheets/d/1ZetYs2n7csR1pI92hOuMfV_RXmxbOh1UOOxx1KdDv0E/template/preview?usp=sharing&resourcekey=0-qpI7g9md35n648x5jgNwaQ).

OR

[Citi Bike Trip DataXLSX File](https://d3c33hcgiwev3.cloudfront.net/-eSTMJ-bSD2WQNV_8mQn2A_f258cf38d2ad4f90baf1ad10e7bf3be1_Citi-Bike-Trip-Data.xlsx?Expires=1716940800&Signature=k~vynUtUz3VfeDz9zhWlXBzWLYkVECBvSgDSPdtaQz3p0FUGuUZ~7xNVncgDAivsGGkI92C~um7thY2fvN-elVfm-bZerPdcJd8k~FZdbyZW89~qVMw3BDjY-jrvndx1uDyMsvr3uj3UGK2IsBkmhZaYBOq2gJLWPtVop9JgYnQ_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

**Note:** If the directions in the video do not work for the version of Excel you have, visit the free online training center [Microsoft Excel for Windows Training](https://support.microsoft.com/en-us/office/excel-video-training-9bc05390-e94c-46af-a5b3-d7c22f6990bb), and search for these functions to learn how to use them in Excel.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716940800000&hmac=UN0tlF7lkA95qCr5MP0pe0_funmKbzc9reSo7V0cU3E)

## Example 1: The **LEN** function

The **LEN** function calculates a string’s length. Use this formula to check the length of the datetime strings in column C.

1. Open the [Citi Bike Trip Data](https://docs.google.com/spreadsheets/d/1ZetYs2n7csR1pI92hOuMfV_RXmxbOh1UOOxx1KdDv0E/template/preview?usp=sharing&resourcekey=0-qpI7g9md35n648x5jgNwaQ) spreadsheet.
2. In cell **B2**, enter the equals sign [**=**] to begin the function.
3. Enter **LEN**, followed by an open parenthesis [**(**].
4. Select cell **C2**. Then add a close parenthesis [**)**].
5. Press **Enter**. The result, 19, indicates the string in cell **C2** is 19 characters.

## Example 2: The **FIND** function

The **FIND** function locates specific characters and substrings in a string. All of the start-time (column C) and stop-time (column D) strings in the spreadsheet have a space between the date and the time. Use the **FIND** function to determine where in the string this space is located.

1. Select cell **B3** and enter the equals sign[**=**].
2. Enter **FIND** followed by an open parenthesis [**(**].
3. Enter quotation mark, then space, then close quotation mark [**" "**] to specify that you want to find a space, then comma [**,**].
4. Select cell **C3** and add a close parenthesis [**)**].
5. Press **Enter** to run the formula. This function returns 11, indicating that the space is the 11th character in the string.

**Note: FIND** is case sensitive, so always make sure you input the substring correctly.

## Example 3: The **RIGHT** function

Use the **RIGHT** function to select a specific number of characters on the right side of a cell. Here, you want to return the substring that represents time, which is contained within the eight characters to the right of the space.

1. Reopen the spreadsheet so you are working with an unaltered version of the document [Citi Bike Trip Data](https://docs.google.com/spreadsheets/d/1ZetYs2n7csR1pI92hOuMfV_RXmxbOh1UOOxx1KdDv0E/template/preview?usp=sharing&resourcekey=0-qpI7g9md35n648x5jgNwaQ).
2. In cell **B2**, enter the equals sign [**=**].
3. Enter **RIGHT** followed by an open parenthesis [**(**].
4. Select cell **C2** then enter a comma [**,**].
5. Enter **8** to specify that you want the function to return the eight rightmost characters in the string.
6. Add a close parenthesis [**)**] to complete the formula.
7. Press **Enter** to run the formula. The time stamp from the start-time data string has now been isolated in cell **B2**.
8. Double-click the fill handle in cell **B2** to fill the rest of the column.
9. Enter **Time** in cell **B1** to add a column header.

## Example 4: The **LEFT** function

Use the **LEFT** function to select a specific number of characters on the left side of a cell. Here, you want to return the date substring, which is the 10 characters to the left of the space. These characters represent the start date.

1. Right-click cell B.
2. Select **Insert 1 column left** to create a new column **B** for the date substring.
3. Enter **Date** in cell **B1** to add a column header.
4. Enter the equals sign [**=**] in cell **B2**.
5. Enter **LEFT** followed by an open parenthesis [**(**].
6. Select cell **D2** then enter a comma [**,**]. **Note:** You added a column, so the start time column is now column **D**.
7. **Add a comma** [**,**] after **D2** in the formula.
8. Enter **10**, to indicate that you want to return the first 10 characters in the date string.
9. Add a close parenthesis [**)**] to complete the formula. **Note:** The instructor enters 11, which will return the date substring and the space.
10. Press **Enter**. The date from the start-time data string has now been isolated in the new cell **B2**.
11. Double-click the fill handle in cell **B2** to fill the rest of the column.

---

# Manipulate strings with SQL

An important part of a data analyst’s job is knowing how to convert and manipulate data for analysis. One way data analysts manipulate strings is to concatenate them, which means to join together two or more text strings. Once strings are concatenated, they form a new, longer text string for analysis. In this reading, you'll learn about different SQL functions that can be used to concatenate strings.

## **CONCAT** in action

Here are some examples of how you might use **CONCAT** as you work with data.

### **CONCAT**

You’re working with the marketing team on an email campaign, and you need to generate full names from your database’s first and last name columns. SQL's **CONCAT** function allows you to join together two or more string values, simplifying this task, as follows:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%206.png)

In this example, **CONCAT** merges the **first_name** and **last_name** fields to create a new field called **full_name**. The space (**' '**) separator ensures the full name appears properly.

### **CONCAT_WS**

Now, you're tasked with creating a report that includes a website's URL components: the protocol (http), domain name (**your_company**), and domain (**com**). You'd use **CONCAT_WS**, which stands for **CONCAT With Separator**, to achieve this. It's similar to **CONCAT**, but it includes a separator, such as a space or period, between the strings.

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%207.png)

Here, **CONCAT_WS** adds a period (**'.'**) between each part of the website URL, ensuring the URL is in the correct, navigable format.

### **CONCAT with ||**

In BigQuery, you can use the **||** operator to concatenate strings. For instance, if you're working with a dataset of book information and want to create a full title by combining the book's name and its edition, you could use **||**, like so:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%208.png)

This script combines the book name and edition, separated by a hyphen for clarity, providing a complete, informative title for your records.

**Note:** In some other SQL environments, you cannot use the **||** operator to concatenate strings. You must use **+** instead. For example, to concatenate the strings **'Google'** and **'.com'** in Microsoft SQL server, you would use:

![Untitled](Combine%20multiple%20datasets%2065f41e7454844e6da18bc535c6f46dbc/Untitled%209.png)

Always ensure you're using the correct syntax for the specific SQL environment you're working in!

## Concatenate strings with SQL

Review the table below as a summary of the **CONCAT** function and its variations in SQL.

| **Function/ operator** | **Use** | **Example** | **Result** |
| --- | --- | --- | --- |
| **CONCAT** | Concatenate strings to create new text strings | **CONCAT('Google', '.com')** | **Google.com** |
| **CONCAT_WS** | Concatenate two or more strings together with a separator between each string | **CONCAT_WS(' . ', 'www', 'google', 'com')** | **www.google.com** |
| **||** | Concatenate two or more strings together with the **||** operator | **'Google' || '.com'** | **Google.com** |

## Key takeaways

In SQL, **CONCAT** is a function that joins strings together to create new text strings. This is useful for creating new variables or features for data analysis, as well as more readable and informative output. In this way, **CONCAT** can simplify your data analysis and make you more efficient.

---