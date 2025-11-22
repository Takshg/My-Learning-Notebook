# Continue cleaning data in spreadsheet - Part 2.

---

# Step-by-Step: Even more data-cleaning techniques

This reading outlines the steps the instructor performs in the next video, [Even more data-cleaning techniques](https://www.coursera.org/learn/process-data/lecture/Ei2IH/even-more-data-cleaning-techniques). This video teaches you different methods data analysts use in data mapping. Data mapping is the process of matching fields from one database to another. It’s critical to the success of data migration, data integration, and many other data-management activities. This video contains one activity for you to practice.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skill demonstrated in the video.

### **What you’ll need**

If you’d like to follow along with the example in this video, choose a spreadsheet tool, such as Google Sheets or Excel.

To access the spreadsheet the instructor uses in this video, click the link to the template to create a copy of the dataset. If you don’t have a Google account, download the data directly from the attachments below.

Link to templates:

[International Logistics Association memberships](https://docs.google.com/spreadsheets/d/1th1mvhFtcg7hW_pDfWv1GaOxFCoIQLOyH7l3ab_W8a4/template/preview#gid=1764281342)

[Global Logistics Association](https://docs.google.com/spreadsheets/d/186Yx3S-ejZr1cJunsal2tUV9J1abixhBUDjXbUtQT7I/template/preview)

[Logistics Association Merger](https://docs.google.com/spreadsheets/d/16tkN0wpaSC3PlxQTGnOGyHWZy9Ui0C2NOIWxBY_gAv8/template/preview#gid=1764281342)

Downloads:

[International Logistics Association membershipsXLSX File](https://d3c33hcgiwev3.cloudfront.net/xSEEsOv6TRa77FfljFKFyQ_c0b53b24e0b54f6fa5d83c5c8683a1e1_International-Logistics-Association-memberships.xlsx?Expires=1716854400&Signature=VJW37VCrWOX7PYwst7xDs9rp1kRnNytCBXFPxUXMO339e7mq-VYY2qFfDMC5geLL2sT0OhxKN0Ni4FHqMnpf~LnUKVx9N0oeCADs1jzm6BRRABPfpSx1~U52TmdQs9tqjXUCqJxx-W0-w-02ag9ek4HDM9kvalnJnHGvbdN2Ek0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Global Logistics AssociationXLSX File](https://d3c33hcgiwev3.cloudfront.net/tMtjHQztTiesjo8vTKb8UA_a5b6cb5cf2404d9abe4b7c3797da94e1_Global-Logistics-Association.xlsx?Expires=1716854400&Signature=IF2HK~xe-czv1QH95-f3n5yuLWKbY-zXq8lgmPBVaf4eVPJDsdiD5KUza3csoLEAD98QX1ofXrFGIh8ooiTAg7fYaX7Bb08GrYXJ0QVv5Hc0xO5tW0x~FLj8YyIYS20t0LZv9g6bD6mwKjfhdoSjpJXYTMjcLdvXmLvuDQNNvJw_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Logistics Association MergerXLSX File](https://d3c33hcgiwev3.cloudfront.net/rCJ95nZHTpCqGu0S0vglvg_a244e9e881604d688bef52d5388febe1_Logistics-Association-Merger.xlsx?Expires=1716854400&Signature=M~UbG3K-w6tdyjoXQEhbS-jhX0~3t9sfw3mM3pS0u~e2wnksNXB1Qt1ux0LjuK~hVQJ6cZPHfhdOip87P8xJiPqnyreMzdgLwjZDTuj71EGy~H1SMV4Ss40AdzRn7l97zbJPtyzAJCIitIoRuR722~UkuE4t6UJ7pj70HcqiQ3M_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3UWxlyqNRxaFsZcqjZcWgQ_3fd91ae61ce04caaa755c3477a337947_line-y.png?expiry=1716854400000&hmac=yjCSowGMfy4MFIfUa2He6nVGJ4klUlOx0-hTmys7Dkk)

## Example: **CONCATENATE**

**CONCATENATE** is a function that joins together two or more text strings. In the video, you’ll learn how to use **CONCATENATE** to clean data after two datasets have been combined.

1. Open the dataset spreadsheet titled **Global Logistics Association**. When prompted, select **USE TEMPLATE**.
2. **Insert** a new column to the right of column **E**. Label it **New Address** in cell **F1**.
3. In the second row of the new column (cell **F2**), enter **=CONCATENATE (D2,E2)** and press **Enter**.
    1. You will notice that some results need a space between the street address and the unit or suite number, such as: 25 Dyas RdSte. 101.
    2. You could manually clean the data later to add a space between Rd and Ste., but **CONCATENATE** can actually do it for you.
    3. The **CONCATENATE** formula can help you format the data as it is merged by entering an additional string to insert a space between Rd and Ste.
    4. Enter **=CONCATENATE(D2, " ", E2)** and you will have an address that is formatted like this: 25 Dyas Rd Ste. 101. Much better!
4. Ensure the new data in the cell accurately reflects the merging of the two previous columns.
5. **Select cell F2** and **drag down** to apply the formula to all rows in the column.

---

# Working with .csv files

In an earlier course in this certificate program, you worked with .csv files. Data analysts use .csv files often, so throughout this course you will continue to use .csv files to transfer data into data analysis programs for further analysis and visualization. .csv files are plain text files with an organized table structure that includes rows and columns. The values in each row are separated by commas. This table structure makes them easy to understand, edit, manipulate, and use for data analysis.

A major advantage of .csv files is their widespread compatibility.  They can be imported and exported by a vast range of data analysis tools and software programs.

## **Download .csv files**

To use .csv files and upload them to data analysis programs you will first need to download them to your local device. Downloading a .csv file from a website can vary depending on your operating system or internet browser. Here are some ways you can download a .csv file:

- **Click the download link or .csv attachment:** Locate the link for the .csv file or attachment on the website. Click on it, and the download process will start.
- **Right-click and Save:** **Right-click** on the data table or element containing the .csv data. Choose **Save as…** or a similar option. Name the file and make sure the extension on the file is “.csv”.
- **Force download:** You can use the **Alt** key on your keyboard while clicking the link. This will trigger the download, and you will be able to find the .csv file in your Downloads folder.

**Note:** When using the Chrome browser or ChromeOS, .csv files may open in a new tab instead of downloading to your machine. If this happens, follow these instructions:

- Select **File** from the menu bar, then select **Save as Google Sheets**. This will open the .csv file as a Google Sheet.
- Select **File** from the menu bar, then select **Download** from the dropdown menu, then select **Comma Separated Values (.csv)**.

## **Upload .csv files**

You will often need to upload .csv files during the data analysis process. Here is how you do this:

- **Locate the upload option:** Each data analysis platform will have a designated button, menu option, or drag and drop area labeled **Upload** or **Import**. This is where you will upload your .csv file.
- **Choose your .csv file:** Click **Upload** or **Import** on the platform you are using to open your file explorer. **Select** your .csv file. If you just downloaded a .csv file from the web, it will be located in your computer’s **Downloads** folder.
- **Initiate the upload:** Once you've selected your .csv file, click **Upload** or **Import.**The platform may display a progress bar or message indicating that the upload is complete.

**Note:** Some platforms have restrictions on the file size or format of .csv files. Make sure your .csv files adhere to these requirements before uploading.

## **Key takeaways**

Data analysis programs help us extract insights and knowledge from data. Using .csv files is essential in data analysis. Understanding how to easily download data from the web or add your data to these programs will allow you to complete data cleaning, visualizations, analysis, and so much more!

---

# Hands-On Activity: Clean data with spreadsheet functions

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GU2UCaWoQBOSJwd0Ab9xNA_a6787cd9089c407199d74ab8631539f1_csGNknJIT4SBjZJySA-ETQ_90b7a3e21cc64ba8a6a65ceee8a162f1_LongBar.png?expiry=1716854400000&hmac=Bqb8KHygInEZ8VreoZPpWBt2q1BQCjK7nY_gX4Dmah4)

By now, you’ve been introduced to some useful techniques for cleaning spreadsheet data, such as sorting and filtering. In this activity, you'll continue to develop your data-cleaning skills by using spreadsheet functions.

# **Scenario**

Review the following scenario. Then complete the step-by-step instructions.

Imagine you are a data analyst working for a marketing agency based in San Francisco. The marketing agency wants to contact local boba tea shops to inquire about a potential collaboration for a new marketing campaign. The agency plans to visit the top-rated shops within a 10-mile radius of the center of their target area. To assist with planning, the agency asks your team to review external data related to ratings and locations of boba tea shops in San Francisco. One of your teammates has created a spreadsheet from an online source. However, the data is not in the greatest shape.

Your assignment is to identify the dirty elements in the dataset and clean them up.

By the time you complete this activity, you will be able to identify dirty elements in a dataset, remove duplicate data, and use the **COUNTIF** and **SPLIT** functions to help clean data.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Access the template**

To get started, access the spreadsheet that contains the data. Click the link and make a copy of the [spreadsheet](https://docs.google.com/spreadsheets/d/1ETb45bbtIn-q3Z-eps9cw66GgS2Gye8cOfKIoFi65DU/template/preview).

Or, if you don’t have a Google account, you may download the dataset directly from the attachment below:

[San Francisco Boba Tea Shop Location InfoCSV File](https://d3c33hcgiwev3.cloudfront.net/1G5STeL7RCeuUk3i-0QnEg_026c7c0c9f3b47efbd599d534b0937f1_San-Francisco-Boba-Tea-Shop-Location-Info.csv?Expires=1716854400&Signature=CnD38T67rRdRmSuBKmff0P1fwi52oLN87jL3qAMh2muTsf0qCXUVuOdygOpZv2odlsIST8h6eh304jzyxfKg4g9t9Dz8LAeyv-GKDmJKvYksZtG41m5FYC4gz9thUj1qSEM-AKfrLQBFz1fChz72TD0SbhplUc8lyjFfZMnSu0A_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

The dataset includes the following column headers:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z3SanT1xR1-0mp09cWdfMw_25e39bb6e92f4139849fa295f0213cf1_Screenshot-2021-06-30-2.26.50-PM.png?expiry=1716854400000&hmac=q13jbRu91whlMHkRwN7Uq4xJP37PY8tjCzwKHBr5oYo)

# **Step 2: Identify the dirty elements in your data**

As a data analyst, your job is to present data that is readable, accurate, and visually appealing. Cleaning your data helps you achieve this goal. The first step is to identify the dirty elements in your data.

1. Rename your spreadsheet. Click **Untitled Spreadsheet** and enter a new name. You can use the name **sf_boba_tea_shop_data** or a similar name that describes the data your spreadsheet contains.
2. If you want to get a better view of your data, you can make the columns wider by dragging the right boundary of the column heading. This may apply to the **name** (B), **address** (D), and **lat-long** (F) columns.
3. Now, review your data and consider any problems you may need to address. The following are examples of errors that you can quickly identify and fix. This is not a comprehensive list of every potential problem, but is a great starting point for data cleaning.
- First, there is at least one duplicate line (rows 20 and 21) in your dataset.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vgC08QcbSBeAtPEHG1gXxA_ff53f013d8d145368f14cc5efbfd22f1_Screenshot-2021-07-15-10.23.54-AM.png?expiry=1716854400000&hmac=hfVnm0wGycwS8X0nC2z17sHMCdng1dolJcTkJExaLuQ)

- Second, all Yelp ratings should fall between 0 and 5. However, at least one rating (in cell C8) falls outside of that range.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lgkdZJ6IT4aJHWSeiN-GSw_71c37eed17ee4598adef014a54bbfcf1_Screenshot-2021-07-15-10.26.12-AM.png?expiry=1716854400000&hmac=UKdzA09MmXHaYxWH7FSw2LKAtrOeRFqYxT0hzmfaxVc)

- Finally, the data for latitude and longitude is contained in a single column (F). In order for someone to be able to use this data for analysis, the two values should be in separate columns.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NEiZs-ZmQCaImbPmZlAmJQ_cf51dde76ccd4bd7821357a6d912f6f1_Screenshot-2021-06-30-2.31.35-PM.png?expiry=1716854400000&hmac=SFrbfP29Qgz3UM3wuF-lDd6fyn425Hi98XCgP0ZaVkY)

Now you know what issues to focus your attention on during the cleaning process.

Your goal is to fix these errors and help create a clean dataset for analysis. You can address each issue in turn.

# **Step 3: Remove duplicates**

The first step is to eliminate any duplicate entries from your dataset. As a best practice, duplicates should be removed even if they are not readily apparent.

1. To start, select columns A through F.
2. Then, in the menu bar, choose **Data,** then **Data Cleanup,** and select **Remove duplicates.**
3. In the pop-up window, click **Data has header row.** You want to remove duplicate boba shop id's and boba shop names**.** In the **Columns to analyze** section, make sure the relevant columns (**id, name**) are selected.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/stxNigsHRymcTYoLB9cpUg_76f9c12c45b745c8929202ea8acafff1_Screenshot-2021-07-15-11.02.45-AM.png?expiry=1716854400000&hmac=W_GKV_cBPY_ZyABrMrro-JFLPV1odTcxem9zdhfgguM)

4. Once everything has been selected, click **Remove duplicates.**

5.  If done correctly, 3 duplicate rows will be found and removed and 604 rows will remain.

# **Step 4: Correct the ratings data**

Next, clean up any data that does not make sense. Yelp ratings should be less than 5 and greater than 0. Now, you will determine how many entries are inaccurate and correct them. You can use the **COUNTIF** function to perform this task.

1. The **COUNTIF** function quickly counts how many items in a range of cells meet a given criterion. In cell I2, enter **=COUNTIF(C:C,">5")**. The first entry (**C:C**) refers to the range where you are counting the data. In this case, the range is the entire **rating** column (C), which contains the Yelp ratings. The second entry refers to the criterion (**>5**), and tells the function to count all the values greater than 5.
2. Press **Enter**. You’ll notice that the function returns a value of 9. This tells you that your dataset contains 9 entries that have a rating greater than 5.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Jf8mhZISRri_JoWSEra4dA_c73549e7506a4efa83cf6ed7f6ed21f1_Screenshot-2021-06-30-2.38.08-PM.png?expiry=1716854400000&hmac=i1F5-2XqcysRLUZUbj7GzOJkycrHx2djY-kTAb92DNA)

As a data analyst, it's your job to decide what to do with incorrect values or to ask the dataset owner for advice if you’re unsure. In this case, one effective approach would be to search on Yelp for the actual ratings. For this activity, you can just replace the incorrect ratings with the number 5. An efficient way to replace the ratings is to sort the data numerically from largest to smallest rating.

3. Select columns A through F.

4. Then, from the menu bar, choose **Data,** then **Sort range,** and select **Advanced range sorting options**.

5. In the pop-up window, check the box next to **Data has header row.** Sort by **rating** from **Z →A.** This way, the highest ratings will be listed first.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pvoPt_PkSba6D7fz5Hm2OQ_376639396af44a30b48ead45ed9dd8f1_Screenshot-2021-06-30-2.39.21-PM.png?expiry=1716854400000&hmac=Mfgp9o21N4txAKk2--0ix0n3kgYD8NwhQ1n9SPWe6Iw)

6. Click **Sort**. Check out your spreadsheet. At the start of the **rating** column, you should now find the 9 rows that have incorrect values (rating > 5).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pPk8ejNsSZO5PHozbNmTQA_88214bfc74464d62b40bed78ff6145f1_Screenshot-2021-06-30-2.40.18-PM.png?expiry=1716854400000&hmac=FDl0BW4F6imN-6uEjF1jVOZeyKLeHyRC--t3Yrpy380)

7. Next, select the range of cells **C2:C10**. Press **delete** to delete the values that are greater than 5.

8. Replace all the values with the number **5**. In cell C2, enter **5**. Then, drag the fill handle down to cell C10 to fill the remaining cells with **5.**

9. After replacing the incorrect ratings with the number 5, you may notice that the new value in cell I2 is 0. The output of the **COUNTIF** function now reflects the changes in your dataset. This confirms that the **rating** column no longer contains any values greater than 5.

10. FInally, delete the formula from cell I2 since you don’t need this information anymore.

# **Step 5: Clean up the latitude and longitude data**

Next, clean up the latitude and longitude data by placing each value in a separate column. You can use the **SPLIT** function to accomplish this task.

1. The **SPLIT** function divides text around a specified character or string, and puts each fragment of text into a separate cell in the row. The **SPLIT** function will split the single **lat-long** column into two separate columns, one for latitude and the other for longitude. In cell G2, enter **=SPLIT(F2,"-")**. The first entry (**F2**) refers to the cell where the text is located. The second entry (**“-”**) refers to the fact that you are dividing the text based on the minus sign.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ln7G6OF_SSq-xujhfykqfg_6c0b145b4ba146b8b1d47996d57116f1_Screenshot-2021-06-30-2.42.26-PM.png?expiry=1716854400000&hmac=ngPBY05T5jC8JdVaiwgDf_rI_ZcvacdGl7TUzurPYkA)

2. Press **Enter**. The result shows each fragment of text in a different cell.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/o7HEj_-oQMyxxI__qFDMBg_968abf1e70e945858978b76cea3899f1_Screenshot-2021-06-30-2.43.09-PM.png?expiry=1716854400000&hmac=dgKtCl5VUMeohzSpOOjamlrV_30t16zuapdtQzB-KP8)

3. Select cell G2 again. In cell G2, double-click on the fill handle to split all the remaining **lat-long** entries.

4. Now add column headers to the two new columns (G and H). In cell G1, enter **lat**. In cell H1, enter **long**.

5. Next, replace the original **lat-long** data in column F with the new split entries in columns G and H. Select columns G and H, right-click, and choose **Copy.**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8aKXdyYBQrmil3cmAeK5Kg_1d0fb3eacea345da80f242acc00a4bf1_Screenshot-2021-06-30-2.46.26-PM.png?expiry=1716854400000&hmac=uCgYA6HVpiF1U0DdLIrw0wtB1tmY_NvIzDJubWpUd-M)

6. Then, select Column F, right-click, and choose **Paste special** and **Paste values only**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yJGweVJzSFORsHlSc-hTkA_9248bb8f70394c328746110472257df1_Screenshot-2021-06-30-2.47.25-PM.png?expiry=1716854400000&hmac=53om7CmxSQHsUhrKyHgdL4Z_QXtr7OQOuYaJqdY02WI)

7. Now the new **lat** column is column F, and the new **long** column is column G. Adjust the width of the **lat** column (F) to fit the data by dragging the right boundary of the column heading.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/k3MDFEqsTeuzAxRKrE3rhg_1f7c0a33bc8742c8a82046f3d49ed3f1_Screenshot-2021-07-15-10.40.25-AM.png?expiry=1716854400000&hmac=NBEUmEJT3V6pMYUvG1e1KkgJUnOsdt75VEcW3h60MuY)

8. Next, select column H, right-click, and choose **Delete column.**

9. Finally, the longitude values should be negative so that they are accurate coordinates for mapping. To make the values in the **long** column negative, multiply them ****by **-1.** In cell H2, enter **=G2*-1**. ****The asterisk is the operator for multiplication. Press **Enter.**

10. Still in cell H2, double-click on the fill handle to fill in the rest of the values.

11. Next, add a column header. In cell H1, enter: **long**.

12. Now, replace the longitude data in column G with the new data in column H. Select column H, right-click, and choose **Copy.**

13. Select Column G, right-click, and choose **Paste special** and **Paste values only**.

14. Then, select column H, right-click, and choose **Delete column.**

Columns F and G should look like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QtTRldIMTzmU0ZXSDB85JQ_2b668ecb9c8e4a12b0279a73275027f1_Screenshot-2021-07-15-10.42.23-AM.png?expiry=1716854400000&hmac=5SMTMTpcMOPywA1VkCjtAAjX3IWUcBXEaS1Vo30ePok)

Now your data is cleaner, clearer, and easier to use.

---

# Develop your approach to cleaning data

As you continue on your data journey, you’re likely discovering that data is often messy—and you can expect raw, primary data to be imperfect. In this reading, you’ll consider how to develop your personal approach to cleaning data. You will explore the idea of a cleaning checklist, which you can use to guide your cleaning process. Then, you’ll define your preferred methods for cleaning data. By the time you complete this reading, you’ll have a better understanding of how to methodically approach the data cleaning process. This will save you time when cleaning data and help you ensure that your data is clean and usable.

## Consider your approach to cleaning data

Data cleaning usually requires a lot of time, energy, and attention. But there are two steps you can take before you begin to help streamline your process: creating a cleaning checklist and deciding on your preferred methods. This will help ensure that you know exactly how you want to approach data cleaning and what you need to do to be confident in the integrity of your data.

### **Your cleaning checklist**

Start developing your personal approach to cleaning data by creating a checklist to help you identify problems in your data efficiently and identify the scale and scope of your dataset. Think of this checklist as your default “what to search for” list.

Here are some examples of common data cleaning tasks you could include in your checklist:

- **Determine the size of the dataset:** Large datasets may have more data quality issues and take longer to process. This may impact your choice of data cleaning techniques and how much time to allocate to the project.
- **Determine the number of categories or labels:** By understanding the number and nature of categories and labels in a dataset, you can better understand the diversity of the dataset. This understanding also helps inform data merging and migration strategies.
- **Identify missing data:** Recognizing missing data helps you understand data quality so you can take appropriate steps to remediate the problem. Data integrity is important for accurate and unbiased analysis.
- **Identify unformatted data:** Identifying improperly or inconsistently formatted data helps analysts ensure data uniformity. This is essential for accurate analysis and visualization.
- **Explore the different data types:** Understanding the types of data in your dataset (for instance, numerical, categorical, text) helps you select appropriate cleaning methods and apply relevant data analysis techniques.

There might be other data cleaning tasks you’ve been learning about that you also want to prioritize in your checklist. Your checklist is an opportunity for you to define exactly what you want to remember about cleaning your data; feel free to make it your own.

### **Your preferred cleaning methods**

In addition to creating a checklist, identify which actions or tools you prefer using when cleaning data. You’ll use these tools and techniques with each new dataset—or whenever you encounter issues in a dataset—so this list should be compatible with your checklist.

For example, suppose you have a large dataset with missing data. You’ll want to know how to check for missing data in larger datasets, and how you plan to handle any missing data, before you start cleaning. Outlining your preferred methods can save you lots of time and energy.

## Key takeaways

The data you encounter as an analyst won’t always conform to your checklist or your preferred actions and tools. But having these things can make common data cleaning tasks much easier to complete. As is so often the case, thoughtful planning sets up any project for success!

---