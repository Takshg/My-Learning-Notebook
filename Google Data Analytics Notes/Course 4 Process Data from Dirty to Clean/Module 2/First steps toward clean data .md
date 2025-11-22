# First steps toward clean data

---

# Data-cleaning tools and techniques

**Key Points:**

- **Data Cleaning:** The process of removing unwanted data, cleaning up text, fixing typos, and making formatting consistent.
- **Importance of Data Cleaning:** Essential for data integrity, reliable solutions, and accurate decisions.
- **Data Cleaning Tools:** Spreadsheets offer various tools for data cleaning, including removing duplicates, irrelevant data, extra spaces, blanks, typos, and inconsistent formatting.
- **Making a Copy:** Always make a copy of the data set before cleaning to avoid losing important information.
- **Removing Duplicates:** Important to find and remove duplicates before analysis to avoid inaccurate results.
- **Removing Irrelevant Data:** Data that doesn't fit the specific problem being solved should be removed.
- **Removing Extra Spaces and Blanks:** Can cause unexpected results when sorting, filtering, or searching data.
- **Fixing Typos and Inconsistent Formatting:** Can lead to miscounts, misinterpretations, and incorrect decisions.
- **Formatting Consistency:** Creates a clean and valuable tool for decision-making.

**Definitions:**

- **Data Cleaning:** The process of preparing data for analysis by identifying and correcting errors, inconsistencies, and missing values.
- **Data Integrity:** The accuracy, completeness, and consistency of data.
- **Duplicates:** Identical or nearly identical records in a data set.
- **Irrelevant Data:** Data that is not relevant to the problem being solved.
- **Typos:** Misspellings, grammatical errors, and other typing mistakes.
- **Formatting:** The way data is presented, including font, size, color, and alignment.

**Additional Notes:**

- The video provides a basic overview of data cleaning tools and techniques.
- More advanced data cleaning techniques will be covered later in the course.
- Data cleaning is an essential skill for data analysts.

**Real-life Example:**

Imagine you are working for a company that sells online courses. You are tasked with analyzing data to identify trends in student enrollment. However, the data you are given is dirty. There are duplicates, irrelevant data, extra spaces, typos, and inconsistent formatting. Before you can analyze the data, you need to clean it up.

Using the data cleaning tools you learned in this video, you can remove the duplicates, irrelevant data, extra spaces, typos, and inconsistent formatting. Once the data is clean, you can analyze it to identify trends in student enrollment. This information can be used to improve the company's marketing and sales strategies.

---

# Clean data from multiple sources

**Key Points:**

- **Data merging:** Combining two or more datasets into a single dataset.
- **Challenges of data merging:**
    - Inconsistent and misaligned information.
    - Duplicate entries.
    - Different data structures and formats.
- **Importance of data merging:**
    - Gaining insights from multiple data sources.
    - Identifying customer buying patterns.
    - Improving data analysis and decision-making.
- **Steps in data merging:**
    - **Compatibility check:** Ensure datasets are compatible and have the necessary data.
    - **Data cleaning:** Clean and prepare datasets before merging.
    - **Merging process:** Combine datasets using tools like spreadsheets or SQL queries.
    - **Verification and reporting:** Verify the merged data and report on the cleaning process.
- **Tools for data merging:**
    - Spreadsheet tools (e.g., Excel, Google Sheets)
    - SQL queries
    - Programming languages like R
- **Real-world examples:**
    - Merging data from two logistics associations during a merger.
    - Combining customer purchase data from multiple sources to identify buying patterns.

**Definitions:**

- **Data merging:** The process of combining two or more datasets into a single dataset.
- **Compatibility:** How well two or more datasets are able to work together.
- **Data cleaning:** The process of identifying and correcting errors and inconsistencies in data.
- **Duplicate entries:** Records that contain the same information about the same entity.
- **Data structure:** The organization and arrangement of data within a dataset.
- **Data format:** The way data is represented and stored (e.g., text, numbers, dates).

**Additional Notes:**

- The video emphasizes the importance of asking key questions before merging datasets, such as:
    - Do I have all the data I need?
    - Does the data I need exist within these datasets?
    - Do the datasets need to be cleaned, or are they ready for me to use?
    - Are the datasets cleaned to the same standard?
- The video also mentions that the choice of tool for data merging depends on the specific situation and the complexity of the datasets.

---

# Common data-cleaning pitfalls

In this reading, you will learn the importance of data cleaning and how to identify common mistakes. Some of the errors you might come across while cleaning your data could include:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xKinzzFmTkKop88xZs5C2Q_5da922d4cbd349e7aeb60ace3e18393a_Screen-Shot-2021-01-18-at-8.03.48-PM.png?expiry=1716854400000&hmac=lhW8PLRjR06NXeGkjmj3cAl5asg2K8etDZt1rfp1eLk)

## Common mistakes to avoid

- **Not checking for spelling errors**: Misspellings can be as simple as typing or input errors. Most of the time the wrong spelling or common grammatical errors can be detected, but it gets harder with things like names or addresses. For example, if you are working with a spreadsheet table of customer data, you might come across a customer named “John” whose name has been input incorrectly as “Jon” in some places. The spreadsheet’s spellcheck probably won’t flag this, so if you don’t double-check for spelling errors and catch this, your analysis will have mistakes in it.
- **Forgetting to document errors**: Documenting your errors can be a big time saver, as it helps you avoid those errors in the future by showing you how you resolved them. For example, you might find an error in a formula in your spreadsheet. You discover that some of the dates in one of your columns haven’t been formatted correctly. If you make a note of this fix, you can reference it the next time your formula is broken, and get a head start on troubleshooting. Documenting your errors also helps you keep track of changes in your work, so that you can backtrack if a fix didn’t work.
- **Not checking for misfielded values**: A misfielded value happens when the values are entered into the wrong field. These values might still be formatted correctly, which makes them harder to catch if you aren’t careful. For example, you might have a dataset with columns for cities and countries. These are the same type of data, so they are easy to mix up. But if you were trying to find all of the instances of Spain in the country column, and Spain had mistakenly been entered into the city column, you would miss key data points. Making sure your data has been entered correctly is key to accurate, complete analysis.
- **Overlooking missing values**: Missing values in your dataset can create errors and give you inaccurate conclusions. For example, if you were trying to get the total number of sales from the last three months, but a week of transactions were missing, your calculations would be inaccurate. As a best practice, try to keep your data as clean as possible by maintaining completeness and consistency.
- **Only looking at a subset of the data**: It is important to think about all of the relevant data when you are cleaning. This helps make sure you understand the whole story the data is telling, and that you are paying attention to all possible errors. For example, if you are working with data about bird migration patterns from different sources, but you only clean one source, you might not realize that some of the data is being repeated. This will cause problems in your analysis later on. If you want to avoid common errors like duplicates, each field of your data requires equal attention.
- **Losing track of business objectives**: When you are cleaning data, you might make new and interesting discoveries about your dataset-- but you don’t want those discoveries to distract you from the task at hand. For example, if you were working with weather data to find the average number of rainy days in your city, you might notice some interesting patterns about snowfall, too. That is really interesting, but it isn’t related to the question you are trying to answer right now. Being curious is great! But try not to let it distract you from the task at hand.
- **Not fixing the source of the error:** Fixing the error itself is important. But if that error is actually part of a bigger problem, you need to find the source of the issue. Otherwise, you will have to keep fixing that same error over and over again. For example, imagine you have a team spreadsheet that tracks everyone’s progress. The table keeps breaking because different people are entering different values. You can keep fixing all of these problems one by one, or you can set up your table to streamline data entry so everyone is on the same page. Addressing the source of the errors in your data will save you a lot of time in the long run.
- **Not analyzing the system prior to data cleaning:** If we want to clean our data and avoid future errors, we need to understand the root cause of your dirty data. Imagine you are an auto mechanic. You would find the cause of the problem before you started fixing the car, right? The same goes for data. First, you figure out where the errors come from. Maybe it is from a data entry error, not setting up a spell check, lack of formats, or from duplicates. Then, once you understand where bad data comes from, you can control it and keep your data clean.
- **Not backing up your data prior to data cleaning**: It is always good to be proactive and create your data backup before you start your data clean-up. If your program crashes, or if your changes cause a problem in your dataset, you can always go back to the saved version and restore it. The simple procedure of backing up your data can save you hours of work-- and most importantly, a headache.
- **Not accounting for data cleaning in your deadlines/process**: All good things take time, and that includes data cleaning. It is important to keep that in mind when going through your process and looking at your deadlines. When you set aside time for data cleaning, it helps you get a more accurate estimate for ETAs for stakeholders, and can help you know when to request an adjusted ETA.

## Key takeaways

Data cleaning is essential for accurate analysis and decision-making. Common mistakes to avoid when cleaning data include spelling errors, misfielded values, missing values, only looking at a subset of the data, losing track of business objectives, not fixing the source of the error, not analyzing the system prior to data cleaning, not backing up your data prior to data cleaning, and not accounting for data cleaning in your deadlines/process. By avoiding these mistakes, you can ensure that your data is clean and accurate, leading to better outcomes for your business.

## Additional resources

Refer to these "top ten" lists for data cleaning in Microsoft Excel and Google Sheets to help you avoid the most common mistakes:

- [Top ten ways to clean your data](https://support.microsoft.com/en-us/office/top-ten-ways-to-clean-your-data-2844b620-677c-47a7-ac3e-c2e157d1db19): Review an orderly guide to data cleaning in Microsoft Excel.
- [10 Google Workspace tips to clean up data](https://support.google.com/a/users/answer/9604139?hl=en#zippy=): Learn best practices for data cleaning in Google Sheets.

---

# Hands-on Activity: Cleaning data with spreadsheet

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Rb5oWTcPRKGPQiTJ9cVJsQ_8909781fa34948b4b5236ca77124a8f1_3UWxlyqNRxaFsZcqjZcWgQ_3fd91ae61ce04caaa755c3477a337947_line-y.png?expiry=1716854400000&hmac=3GaXBBaNBp9v_eluGSCuQ5TamMWzcR6EJ-K4O1XxX5I)

You’ve learned about cleaning data and its importance in meeting good data science standards. In this activity, you’ll do some data cleaning with spreadsheets, then transpose the data.

By the time you complete this activity, you will be able to perform some basic cleaning methods in spreadsheets. This will enable you to clean and transpose data, which is important for making data more specific and accurate in your career as a data analyst.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the template**

To get started, first access the data spreadsheet.

To use the spreadsheet for this course item, click the link below and select “Use Template.”

Link to data spreadsheet: [Cleaning with spreadsheets](https://docs.google.com/spreadsheets/d/1PkAbgXC7C1g2dKzCCpaHBcAyPw-s1z7iUxIEJ0cCYWQ/template/preview)

OR

If you don’t have a Google account, you can download the template directly from the attachment below.

[Data Spreadsheet for Cleaning with SpreadsheetsXLSX File](https://d3c33hcgiwev3.cloudfront.net/9Ss-5kXlRP6rPuZF5VT-qA_d5c83c4e13d643cd87cb22632fcaa9c6_Data-Spreadsheet-for-Cleaning-with-Spreadsheets.xlsx?Expires=1716854400&Signature=HmfyQr03muANQIii4IFvZNrYGpvzktHm9vREy7FykJQFf7r1ud32es9MKspAsAuS~WtT-I0XuHDJVeyIB72l3N8pPXpKVen~8c263b75RuvQIbbKXU4dpmPlUaaTu~BAocaNUbxSwyEfMZxZ-c2BuCjwEuSzi4nhgcgF6Bxgku8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

# **Step 2: Select and remove blank ells**

The first technique we’ll use is to select and eliminate rows containing blank cells by using filters. To eliminate rows with blank cells:

1. ****Highlight all cells in the spreadsheet. You can highlight **Columns A-H** by clicking on the header of **Column A**, holding **Shift**, and clicking on the header of **Column H**.

2. ****Click on the **Data** tab and pick the **Create a filter** option. In Microsoft Excel, this is called **Filter**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2_bW59hoSv-BnmJP94IYLA_b531ced817624814afe6aded60c7c2f1_O9NNCnlDSnWTTQp5Q1p1XA_25d78d3867c8402da3bafff30662affe_DAC4M2L3HO1-ss1---Hands-on-Activity---Cleaning-with-Spreadsheets.png?expiry=1716854400000&hmac=oohx-QJ6wTUaGblxWJY8b3qCwR3kNmBN_x7s1gvmDyk)

Excel:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/mDHtyMVOQxSPsG4LiggSRQ_d89e0cee9aa544bc9a3701e377a893f1_rbruHkUVR2e67h5FFVdnIA_46544fd0693e4d54b0b48738dd7adef1_clean1.png?expiry=1716854400000&hmac=1pXJZtnWXN4V9il3bO_LYJDPbjj_UwUrtowo33ihKS0)

3. Every column now shows a green triangle in the first row next to the column title. Click the green triangle in **Column B** to access a new menu.

4. On that new menu, click **Filter by condition** and open the dropdown menu to select **Is empty.** Click **OK**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8VR7iiIdSU6KsLbRe8K6vA_ee488e9dd31843f19f9d425a5ba9e2f1_OnScbk09Sya0nG5NPSsmnw_3bd0ebe89bb54e78b77e287c57d84469_DAC4M2L3HO1-ss2---Hands-on-Activity---Cleaning-with-Spreadsheets.png?expiry=1716854400000&hmac=IdDZRyNP1Tk9IB07e9eVNAb6KiZNYvLY_2he5BKhROc)

In Excel, click the dropdown, then **Filter...** then make sure only **(Blanks)** is checked. Click **OK**.

Excel:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4_I-jjaFQG-QORWThpmhig_c9fd7cb5d3034aee9a507b58d50602f1_Uhm2BhPySXGZtgYT8nlxrw_665641702fca449eaa1d0d76780d93f1_clean2.png?expiry=1716854400000&hmac=lwl_ppoExR6Y9z_hgmu3wQcPZ5zAbMVIhsmyDGLxA0I)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_gwLiHxtTnO0uYhXjYxM3g_76a3d1f2722e48bea5b8e3c1da5fe1f1_fRE5xga-RnSROcYGvvZ0uw_899befc39c474834a28b47e8173acff1_image-1-.png?expiry=1716854400000&hmac=BTp5yygF8gNiN-eyKg7xk8qM2mLIrFfmrH45XE7GSVM)

You can then review a list of all the rows with blank cells in that column.

5. Select all these cells and delete the rows except the row of column headers.

6. Return to the **Filter by condition** and return it to **None**. In Excel, click **Clear Filter from ‘Column’**.

- **Note:** You will now notice that any row that had an empty cell in **Column A** will be removed (including the extra empty rows after the data).

7. Repeat this for **Columns B-H**.

8. **Note:** If you simply deleted the data from the row by tapping the backspace button, you will need to go a step further and *delete the empty row entirely* by left-clicking the row number located on the furthest left side of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iboFC5tORMmJ1-rUuP5CYg_9276e0cbad8b42fea8ea00ac374963f1_tw7qKgnVSL-qreDMxqqNVg_4c27bec8fb094e09b8ca6fe4852352f1_RowSelect.png?expiry=1716854400000&hmac=WAIBinJTORRVPefYtgPBjW3AGjZsZ9QdDShNztHjcXE)

9. Next, right click on the highlighted row to call up the drop down window, and select the **Delete row** option.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2ZacWmgbS7Of49zcjJzQJw_d516536e56924117a41cb1754b988df1_iAJUmDmQRDiRHQ69peqoiw_4f399ce0c6f1496c948c70141335bef1_DeleteRow.png?expiry=1716854400000&hmac=qTg9Uwu5QQnz5QFFeRHeXAyv15aO5oVJuhYTW3WN5rs)

10. Continue to do this same operation for the remaining empty rows in the data set.

All the rows that had blank cells are now removed from the spreadsheet.

# **Step 3: Transpose the data**

The second technique you will practice will help you convert the data from the current long format (more rows than columns) to the wide format (more columns than rows). This action is called **transposing**. To transpose your data:

1. Highlight and copy the data that you want to transpose including the column labels. You can do this by highlighting **Columns A-H**. In Excel, highlight only the relevant cells (**A1-H45**) instead of the headers.

2. Right-click on **cell I1**. This is where you want the transposed data to start.

3. Hover over **Paste Special** from the right-click menu. Select the **Transposed** option. In Excel, select the **Transpose** icon under the paste options.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/L3rm_PQ5S7SDY0tquCz2Zg_3b5dad0c3abc4193be95d258cae493f1_MTwQTUO9Sr28EE1Dvcq9TA_72cc515a56e74c5087f79f9f0a5c76f1_Screenshot-2021-08-01-11.09.05-PM.png?expiry=1716854400000&hmac=MXsgT8ztrOktLhUR4vKMhOZTEUnrgsmur_pCKWp-buo)

Excel:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/v6WsBwV6TB2w9I6-p9fz_w_21a1c608f1bc4a19959c1b403e16faf1_cZZMekh0R--WTHpIdIfvyQ_d00c1398f40f40c793f389815300b4f1_clean3.png?expiry=1716854400000&hmac=ykdj7-mv4Zjh1QksmBhTk9Ml79Ypc_h9YsC46msgwhE)

You should now find the data transformed into the new wide format. At this point, you should remove the original long data from the spreadsheet.

4. Delete the previous long data. The easiest way to do this is to click on **Column A**, so the entire column is highlighted. Then, hold down the **Shift** key and click on **Column H**. You should find these columns highlighted. Right-click on the highlighted area and select **Delete Columns A - H**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/X_4gvZKFR4qhaZN6mGxUag_fd1f497b4ac547a0bf35d983084c48f1_FFf0RtUlQHuX9EbVJdB7pQ_555c8bf1f03f493594dc266e0aeb64b7_cleaning1.png?expiry=1716854400000&hmac=tj9hwbrsQw658SpODxYmcZSzmPhjvHhzWWl_IsQIg5M)

Your screen should now appear like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HDFOtlHJTU2Lwy77SfrfZA_59e45f6fa3224755af35de41800c44f1_B-rP6lYRQiCqz-pWEWIg4g_0279fd307ac24ed5a9ad2687129d7757_cleaning2.png?expiry=1716854400000&hmac=yx9eygnClwHYABuqhcvD14ZJ9tBH1NuLGZ-WpTN3wFc)

# **Step 4: Get rid of extra spaces in cells with string data**

Now that you have transposed the data, eliminate the extra spaces in the values of the cells.

1. Highlight the data in the spreadsheet.

2. Click on the **Data** tab, then hover over **Data cleanup** and select **Trim whitespace**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/eKtpOFTMSdafQVjbUutfUg_20dbcc23349f4b9b922137fdbb5d4cf1_pq0CjzcvSMOtAo83L7jD1A_cc5e405f6d2a41098cce951e3eacc8f1_Screenshot-2021-08-02-12.08.23-AM.png?expiry=1716854400000&hmac=RzYTYrsAWUA28oo_R7_ZlEIeREUPo2h9Z-dxV_ZAb-Q)

In Excel, you can use the TRIM command to get rid of white spaces. In any space beneath your data (such as cell **A10**), enter **=TRIM(A1)**. Then, drag the auto-fill square handle at the bottom right corner of the cell and pull it downward to call the rest of the data in the column without the white spaces.

**Note:** It's important to carry out the **TRIM** formula for each column individually, as it may affect certain types of cell values (like dates) undesirably. One option is right-clicking the "Order Date" column at the top, and selecting the **Format Cells** option to change the dates to string values before applying the **TRIM** formula.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XiBEP9IuRSq1sXVnIZyvHw_a45357340b7949cdb3518defb2662ff1_byDBtpjHQmab_hzHTqEnKw_92a52d92f76d47d9852aad83835b60f1_1.jpg?expiry=1716854400000&hmac=z1ZLSj5otsb6_NfwplMCDW753pYSDT9LP3LjrPnWmto)

For additional understanding of using the TRIM formula in Excel, please explore the [Microsoft Excel guide](https://support.microsoft.com/en-au/office/trim-function-50b6f593-4801-4f06-81c5-3345e7f80ddd) on using the formula correctly.

Now all the extra spaces in the cells have been removed.

# **Step 5: Change lower/uppercase/proper case text**

Next, you’ll process string data. The easiest way to clean up string data will depend on the spreadsheet program you are using. If you are using Excel, you’ll use a simple formula. If you are using Google Sheets, you can use an Add-on to do this with a few clicks. Follow the steps in the relevant section below.

### Microsoft Excel

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uFX3SXLMSYWrtuDokxQp-g_a78785e301f44700a5833e13e35de6f1_m1U8W60bRHWVPFutG7R1Xg_6ccc659ce432491f86146109849dbf6b_shortline-y.png?expiry=1716854400000&hmac=Fy6N-f_bJUBmCq7ednQebNqTIS83EZurjyl3-uVJGwU)

If you are using Microsoft Excel, [this documentation](https://support.microsoft.com/en-us/office/change-the-case-of-text-in-excel-adc65f5b-958f-46a2-4d23-ab4d5faf48a8) explains how to use a formula to change the case of a text string. Follow these instructions to clean the string text and then move on to the confirmation and reflection section of this activity.

### Google sheets

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yKHQIr9LSKegPqWGn9SE-Q_cfce0f4e93084439a52b06ccc346d1f1_m1U8W60bRHWVPFutG7R1Xg_6ccc659ce432491f86146109849dbf6b_shortline-y.png?expiry=1716854400000&hmac=WgRs785Lur5n3YkCcv8HWix6Rx7HTxw1zDhn32AQtb8)

If you’re completing this exercise using Google Sheets, you’ll need to install an add-in that will give you the functionality needed to easily clean string data and change cases.

*Google Sheets Add-on Instructions:*

1. Click on the **Add-Ons** option at the top of Google Sheets.
2. Click on **Get add-ons**.
3. Search for **ChangeCase**. It should appear like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/5JU760Y9R3m0FSdjg9foSA_e79e38d216d94df4b1e5fe83b8e9daf1_RsIWudCiRKiCFrnQomSo4Q_a833e87b50d94bacaab8d47e49adef7b_DAC4M2L3SR1---image7.png?expiry=1716854400000&hmac=iC-8VmuLIglUXRvVey1Fpiwj_5X3kJTdgQs5dXV146Y)

4. Click on **Install** to install the dd-on. It may ask you to login or verify the installation permissions.

Once you have installed the add-on successfully, you can access it by clicking on the **Add-ons** menu again.

Now, you can change the case of text data that shows up. To change the text in Column C to all uppercase:

1. Click on **Column C**. Be sure to deselect the column header, unless you want to change the case of that as well (which you don't).

2. Click on the **Add-Ons** tab and select **ChangeCase**. Select the option **All uppercase**. Notice the other options that you could have chosen if needed.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_u_Q95WYTHS6RFLMKTOv0A_1d1a769673ec43b7a679d99f52f98df1_s0nWbQUzQ8WJ1m0FM8PF-w_08d52b8bd2864249b631b86dd41db56a_cleaning4.png?expiry=1716854400000&hmac=hGbotYPGQr2DyWl8WXCbp6MjqKlXVImny0ElJiC8p3Y)

# **Step 6: Delete all formatting**

If you want to clear the formatting for any or all cells, you can find the command in the **Format** tab. To clear formatting:

1. Select the data for which you want to delete the formatting. In this case, highlight all the data in the spreadsheet by clicking and dragging over **Rows 1-8.**

2. Click the **Format** tab and select the **Clear Formatting** option.

In Excel, go to the **Home** tab, then hover over **Clear** and select **Clear Formats**.

You will notice that all the cells have had their formatting removed.

---