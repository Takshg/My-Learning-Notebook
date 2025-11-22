# The data-validations process

---

# Check and recheck

[index (34).mp4](The%20data-validations%20process%202cf66f5d16f64ebeb1461a5f33d44117/index_(34).mp4)

**Key Points:**

- **Data validation** is a crucial process in data analysis that involves checking and rechecking the quality of your data to ensure it is complete, accurate, secure, and consistent.
- Data validation is not just a one-time process; it should be used throughout your analysis.
- Data validation helps you understand your data, check that it's clean, and make sure you're aligning with your business objectives.
- Data validation can be used to identify and correct errors, such as incorrect calculations or missing data.
- Data validation can also be used to identify patterns and trends in your data.
- There are many different ways to perform data validation, including using formulas, queries, and visual checks.
- It is important to choose the right data validation method for your specific needs.

**Definitions:**

- **Data validation:** The process of checking and rechecking the quality of your data to ensure it is complete, accurate, secure, and consistent.
- **Data cleaning:** The process of identifying and correcting errors in your data.
- **Data analysis:** The process of examining data to identify patterns, trends, and relationships.
- **Formula:** A set of instructions that tells a computer how to perform a calculation.
- **Query:** A question that is asked of a database.
- **Visual check:** A manual inspection of your data to identify errors or patterns.

---

# Types of data validation

This reading describes the purpose, examples, and limitations of six types of data validation. The first five are validation types associated with the data (type, range, constraint, consistency, and structure) and the sixth type focuses on the validation of application code used to accept data from user input.

As a junior data analyst, you might not perform all of these validations. But you could ask if and how the data was validated before you begin working with a dataset. Data validation helps to ensure the integrity of data. It also gives you confidence that the data you are using is clean. The following list outlines six types of data validation and the purpose of each, and includes examples and limitations.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bwKS3nJvQoqCkt5yb2KKtg_381561b0be794604bbab4b371ca61bc9_Screen-Shot-2021-02-08-at-5.22.06-PM.png?expiry=1716940800000&hmac=a7eVLSdHkFTQGj1kqIi-bjkCC_x2LFJhzo3DAcBodrc)

- **Purpose**: Check that the data matches the data type defined for a field.
- **Example**: Data values for school grades 1-12 must be a numeric data type.
- **Limitations**: The data value 13 would pass the data type validation but would be an unacceptable value. For this case, data range validation is also needed.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dPyj72GhQXS8o-9hoTF0Ag_839574976de44a4b9a3ec45f4e4e36e2_Screen-Shot-2021-02-08-at-5.25.03-PM.png?expiry=1716940800000&hmac=lGZNXkP-58coz14uFsE32riiFw1-0Uisbwvp-SX1CAY)

- **Purpose**: Check that the data falls within an acceptable range of values defined for the field.
- **Example**: Data values for school grades should be values between 1 and 12.
- **Limitations**: The data value 11.5 would be in the data range and would also pass as a numeric data type. But, it would be unacceptable because there aren't half grades. For this case, data constraint validation is also needed.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/DUa8GZEkTR6GvBmRJC0emw_a9e6271e8f1c4cb0820ec3d6ee34f4eb_Screen-Shot-2021-02-08-at-5.27.40-PM.png?expiry=1716940800000&hmac=wqQ7MpDIzTb0pXzDqN5cB73jyaFafArAXBUR4cBIAJ8)

- **Purpose**: Check that the data meets certain conditions or criteria for a field. This includes the type of data entered as well as other attributes of the field, such as number of characters.
- **Example**: Content constraint: Data values for school grades 1-12 must be whole numbers.
- **Limitations**: The data value 13 is a whole number and would pass the content constraint validation. But, it would be unacceptable since 13 isn’t a recognized school grade. For this case, data range validation is also needed.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Xlu9FFgIRDGbvRRYCFQx-w_6eaa5307239541e9a5e0c77a343f9c8b_Screen-Shot-2021-02-08-at-5.30.56-PM.png?expiry=1716940800000&hmac=yG9V9vlKIgJBtgoGaY-BdcFbYoCTZUTWkEzeS4ptvIs)

- **Purpose**: Check that the data makes sense in the context of other related data.
- **Example**: Data values for product shipping dates can’t be earlier than product production dates.
- **Limitations**: Data might be consistent but still incorrect or inaccurate. A shipping date could be later than a production date and still be wrong.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6kdSdq1vQfeHUnatbwH3Lg_02d9444056b340e58377aa792ecb0d43_Screen-Shot-2021-02-08-at-5.33.03-PM.png?expiry=1716940800000&hmac=uYUeQksV4ydgoi6RqG6ZBerSqmk85TrPgziKCkoMAe8)

- **Purpose**: Check that the data follows or conforms to a set structure.
- **Example**: Web pages must follow a prescribed structure to be displayed properly.
- **Limitations**: A data structure might be correct with the data still incorrect or inaccurate. Content on a web page could be displayed properly and still contain the wrong information.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Saof9D7aT8eqH_Q-2k_Hyg_d144822d70ac4ec3b22b5126c0b32e60_Screen-Shot-2021-02-08-at-5.34.42-PM.png?expiry=1716940800000&hmac=eHSFUW5RtwJiFDF6jr99tT-OAemkGEpJ0mlg7VMP3_I)

- **Purpose:** Check that the application code systematically performs any of the previously mentioned validations during user data input.
- **Example:** Common problems discovered during code validation include: more than one data type allowed, data range checking not done, or ending of text strings not well defined.
- **Limitations:** Code validation might not validate all possible variations with data input.

---

# Hands-ON Activity: From spreadsheets to BigQuery

## Activity Overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/oCbJiUcDSiWmyYlHA1olsA_f1117c8fa8064e1587388186d8712cb0_line-y.png?expiry=1716940800000&hmac=J-vIpON8FvdHkQMdqAYAiJqz76XwuXeVTyhdO3iSclM)

By now, you have worked with data using both spreadsheets and SQL. These tools operate very differently: In spreadsheets, you are able to observe and interact with data directly; with SQL, you interact with data through queries to the database. In this activity, you will use spreadsheets to clean your data before importing it into SQL for analysis.

In this scenario, you have been working for a national store chain as a data analyst. Management is interested in the amount of inventory being kept in storage at regional sites. Your supervisor has asked you to perform an analysis on inventory and sales data to make recommendations for changes to inventory management practices. You have been provided with three datasets containing information about inventory, products, and sales.

By the time you complete this activity, you will be able to combine tools to successfully analyze data. Switching between spreadsheets and SQL can be challenging because they’re so different, but once you’re more used to both tools, you’ll be able to use both more easily. This is important for tackling larger and more complex projects in your career as a data analyst.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/USm2_QwZQUGku0M6aZxZCA_18171f75590f4c67b84987ab0f5805f1_AD_4nXegopZXf4qklI41TpHcQd55y4BCpBNKrr6zeEbl-gFtISkeoihXn4i60sKxOfEt_YljGd36Zr_eP7Sr454BMBWZPMXV5LV9q36rpgLCOo7w7Aj3GWunf3CdWhOrq5ezzrEQ4ga7I7yfoDR08Ga3XB0Rsx3JrTw75rlta__Am3E?expiry=1716940800000&hmac=N1JjXRTgltZv80yA1kc1Nu6NL7X6hC765SY2KxIx9_Q)

To get started, first download the three store data CSV files: inventory, products, and sales.

[InventoryCSV File](https://d3c33hcgiwev3.cloudfront.net/R3bnJPVKQmmfNsDWPZLsbA_293e6b6eed384834bedb3db6a42b49f1_Inventory.csv?Expires=1716940800&Signature=jUPabri8lUN4hUlXmqkvAw2-T1fyotXPutGI79PLON3Q1n~pmtWconMrHdIQ-S-9Jy9o1Jb5KIp6TH2Y0DwSCczhga3fnfUD8RlgQ2wlqq7qU~1lMLTW0xmTSdIvWHzWNirM1dx5FvtVVsC~uHiDoW-I4M~FV55co9b1ajV9F~w_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[ProductsCSV File](https://d3c33hcgiwev3.cloudfront.net/nLwqt4vIR66im_bjkmD8yg_7430b25a7c1a4dd7adc95aaa4c3cdff1_Products.csv?Expires=1716940800&Signature=FtwwVOC4MJOGZR-RsxRqIcTHd~lYG71NepuLJQByJBVPreHwnSnWdbxYPQIFYmD1iQ3AtSXq-V7k4rmSmMOi~TtSDfRFK0J-kDXg~XwX4YMxZ~oWyhWQJp3tBmEzaQNjkzqrIz8u3Ea8WqLTbw4KSvgK9cqEcq2CP5JlkvGEht0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[SalesCSV File](https://d3c33hcgiwev3.cloudfront.net/I76udVpkSbuliDJZUuDRXQ_eff12ec557d94875a2d8a26fd7261bf1_Sales.csv?Expires=1716940800&Signature=Ep6cBwgFpL9Mq1ZAyBKhZxguAS2LVk60PxOChf0mkP63cxwWbb8Z7bLs-3OBrqbZaeoMFUWWeZn1QnywLvRWwYNf2qGmIOGVlu4z5jk~ZHHqbt05fy7jRGhVSDt9z9NKndgQnWiQsguGAQfMnk5-RmYQahIJ~EztACU-VF59zpQ_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

# **Cleaning the data**

Before you upload these files to SQL, you can import them into a spreadsheet in Sheets to get comfortable with the data before you start analyzing it in BigQuery. This might not always be possible with larger datasets you encounter in the future, but you should explore as much as possible within this exercise! You can also use this step to perform some data-cleaning tasks.

# **Step-By-Step Instructions**

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Import the data**

If you’re using Google Sheets, you’ll first need to import the data files into your spreadsheet . Open Sheets and navigate to the **File menu,** then **select Import** from the dropdown list.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UutVgFgHSxCghpXf_2mIbw_ff30e6777aa7434a8bb9ec0e0edb83f1_AD_4nXcux-UrX8FG4x07pi-K083jgLwmN-qAdTpMV8BfYlRMmwXiBa7_QFUc6_oE1byTmTbZJ1_2mk1-PJLn0HdU0D8AiL8OV5RyfGv98_GyuWoHvwaaOVRwqBEwW8KqnD4jd6RBQRLrWlTe7qD2gv_b_SxrsnwLoy-LaDASwqTClA?expiry=1716940800000&hmac=O5CE7rb9JH_whGWidj6yCL1YRvXX4DW9cBPysTLS8J8)

**Select the first file and upload it** to the spreadsheet. Choose **Replace spreadsheet** to insert it into the current sheet.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/asFLYgX0SXisYTLWquiJ7w_f66ccf2ef504490a8f909fd9e27143f1_AD_4nXewgNdagdx4hA_PkEdc2VvqX2jahJtTvjQyVFJllhypbva1NxRMP6G1LF6zUD3NTWFrQXd6Ckse3WNnmz34wevvXVlolxKrVijB2PQ4rv4xz5axvXQwqJpe1Y47_VFCbx4TLsQ_QaoAyp1p9QqjoPa1sOOlvqAK2eCbb7zwAw?expiry=1716940800000&hmac=kCvUf3SXKlv5b7oJSqxhC1r8QLhbKqNwLNVpn22fyy4)

Then **return to the Import menu** under the **File menu** and **upload the next file**. This time, however, **select Insert new sheet(s)** to create new worksheet tabs with this file.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Q468pzYGQB-AIJm4f1w2qA_f47882957b9946c189fc05ae54ea52f1_AD_4nXenZR5J5MhJzw8bremL1TWfxi6UuqUgf5zapoTzrgWhYOWypTTPc-LoCMFNl6h7fIgsNXDiQ2BteabsN-YhhbeN2P2Y_DXB94nwZyzW__KOM0OKYK7LJUd2u9qz5lFbbp0eNSovgU5c5clj8OU3xVp4Hg_q5bJhi1yUajiaQss?expiry=1716940800000&hmac=EiXcuGt8L3ZFPDIhBd2kVQ5CDp0ZaBdIW6kWL3bXQEE)

**Repeat these steps** until you have all three files added to your spreadsheet.

## 

# **Step 2: Inspect the data**

Applying filters in spreadsheets is a good way to identify any data that needs to be cleaned. You’ll inspect the Inventory sheet now.

**Navigate to the Inventory sheet** and **click any cell** in the spreadsheet. **Open the Data dropdown menu** and **select Create a filter**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZWftfcS7Rby5CY2Ak7nPvQ_e62e22f4a37d476c865e47ae8668c1f1_AD_4nXfNhId3OV3q9gY8eFQ9q6pul9opzHVnh4yctbOWvYOr8UdfcBxZ8RC2KPoeT67Yt9WDBsBTcnF6bqxQNUS8ZmuQaXm26KKLmIv8_OZx5qBe4mBUvH5Yp-5SuJuu6qoIOK-7ccyFgltz69y9jOJF3WDl1NL0NzuvVihRBrJgxQ?expiry=1716940800000&hmac=QjUKOCPFE32FOYSujSfdMUHzEWZQk7puqQlGN9HH49k)

Now you can click the filter icons for each column to inspect the values. **Start with the StoreID column.** As you scroll through, you’ll notice that there do not appear to be any blanks or incorrectly entered values. However, if you inspect the StoreName column, you’ll find a blank.

**Deselect all of the values except for the blank.**

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/99gUKnihSmORKQazvSQezA_f19c07cf13d54d8d9fa5ebba628256f1_AD_4nXeCKtQLDFaF-nJiJnW7DsyhOQ3WljgSOvSsJOCoyWLKQ8yXeK1DQ0cSGqYdJL9uYOqhx4kA55YNt0CIUw1STmBqXuiTrezS2Ky7NaZTWk5CQthgtuGgMYjmA93wgli3DxhDfaUPrHq3Bkyobm5F_-dR-Cz3-sestMIhWbm71pA?expiry=1716940800000&hmac=k22OhVEkQqKCAxBDxxaXyiTWmjFSBcqhn0s_LvNgr2Q)

This should return one row with a missing entry under the StoreName column.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0Hq1DZ7FQ1ObJvo576HumQ_539d5bc204c8445caba6b4b7cb3497f1_AD_4nXdEs652D-9NYe1DpHPmzlOh8u1zdjT2tp7rUbbyoYCn55sL-hp7QpB2u8l2xDK_KmfKEGkLfYx7JewCZNvjcrXuNwOehkIYhTqSjBnRrOwgqzz-azfKmTn0Go3WpFCnqhuuWE_eHoRApi2skysDese5kMIk_3rBNhxMkopcs7w?expiry=1716940800000&hmac=KzdoR-Q04vJGKJ8tGFg9vAcVgOKAeUcLLECQ4SrAYNA)

You might be able to find what the missing value is and input it correctly using the filter. **Clear the Storename filter** and **use the StoreId column filter** for other stores with the **ID 21791.**

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2UwElT1AQ_SQ_GIqqfSMsQ_359164fa824d4f748551f78fce70def1_AD_4nXefWrNo0q_eq4mC7tp8trjs_MBbRjrBKBiaw9EMlhni3DVe3ub_A_DbBz4Ivy3QUh5-QUsdVKWFclgLQ37ErrTzZEoABUklMPQ1_OTkn44XRZgJT8ovTIFGEwarnPfXtx4E9Z_F-TE99b5j0CcgdcIr76YPvH3TdoTsaxXBn9M?expiry=1716940800000&hmac=zA8yHvq213X7H5Nsc0doEBcdGj2qmbbi74QA6vBPXQw)

It appears that the other stores with this ID are all Dollar Tree, so it’s probably safe to **input that as the StoreName value in the blank cell.**

**Inspect the other columns** in this sheet, then **return to the Data menu** to **turn off the filters**. Next, **navigate to the Products sheet.**

Similarly to the last sheet, you can **repeat this process to inspect the Products data.** Go to the Data menu and select Create filter.

**Check the ProductID column**. You'll find that there is a NA value in this column, despite the fact that this column should only have numeric values. In this case, you’ve checked in with the dataset owner, who said you can **delete this row** because it was input by mistake and does not belong in this dataset**.** Turn off the filter and move on to the next step.

**From spreadsheets to BigQuery**

# **Step 3: Inspect the data in the spreadsheet**

Applying filters in spreadsheets is an effective way to identify any data that needs to be cleaned. Start by inspecting the Inventory sheet.

1. Navigate to the **Inventory** sheet.

2. Select any non-blank cell.

3. Open the **Data** dropdown menu and select **Create a filter**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/iOTUu8sASji-K-scfBhUJA_e2ff2c84b9bb489a832a82a972e708e1_C5M4L4_04.png?expiry=1716940800000&hmac=d000Aqn9RKAmwmuF_KAkSk_TI8ELGm5w-rgvFjYq5bw)

4. Now you can select the filter icons for each column to inspect the values. **Start with the StoreID column.** As you scroll through, you might notice that there do not appear to be any blanks or incorrectly entered values. However, if you inspect the StoreName column, you’ll find a blank.

5. Deselect all of the values except for the blank.

6. Select the **StoreName** filter dropdown

7. Select **Clear**.

8. Select the checkbox next to the **(Blanks)** value in the list.

9. Select **OK**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/eAeDGZMSSpy89pT7UeyRtg_8b4ca94ed71b4286b6be8b042e2c35e1_C5M4L4_05.png?expiry=1716940800000&hmac=Kk73MQVpuASC1kJRnIhy8xuczav9Q1ZQB7TSHiuwlXA)

This should return one row with a missing entry under the StoreName column.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/EL4kzOmwTNmWvAiAux95Xg_1435c58bc1414eb0b5982f885697d1e1_C5M4L4_06.png?expiry=1716940800000&hmac=q4IQ0BX4IinLEJ6W8YdryGoFa0yqrMvxNdPQS5Phc-I)

You might be able to find what the missing value is and input it correctly using the filter!

10. Clear the **Storename** filter and use the **StoreId** column filter for other stores with the **ID 21791**.

11. Copy the **StoreID** (21791)

12. Clear the StoreName Filter using the StoreName filter dropdown. Select **Select All** then **OK**.

13. Select the **StoreId** filter dropdown.

14. Select **Clear**.

15. Enter **21791** to the search bar which will pull up that StoreID.

16. Select the checkbox next to the **21791** value in the list

17. Select **OK**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/47uC07peQMGPqbIir2dr1w_1931101473d74c94a8c6260c8299eee1_C5M4L4_07.png?expiry=1716940800000&hmac=ye-QyW-lOGyRxp47O8LoJP-yyXC55sTPcmD8_bY5-K8)

Now that you have checked out your data in a tool that lets you observe and interact with your data directly, it’s time to transition to using SQL. With SQL, you can only observe the results of your query, which requires a different mindset than spreadsheets — but SQL is very powerful when you’re working with databases and larger datasets!

# **Step 3: Create a dataset and custom table**

Similar to previous activities, you will need to create a dataset and custom table to house this data before you can inspect it in BigQuery.

1. From the **Explorer pane** in your BigQuery console, click the three vertical dots next to your project space and select **Create dataset**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0Y_qshKCRta7Ey8420h_Rg_0a62031d1e2a443f92176c1404617bf1_AD_4nXeH88rdsCOqEVXnsTk3oZcfOUKlN1t5bnp280YQ89u-LadqEHTHuR-izcRIpUY44jXJvU1eLRR4aJ0BSZfpbpvwEAmh0T6ooEf8wxN4Pv1w7hbQjrXTha09M9DupmaDW_yn82sm5x-kog20HWV6FC0QD4ye57MpvHSNY1IxARM?expiry=1716940800000&hmac=ZoyUv8-YbN69TfrDewiVLn_HwYYAoXwnG8-4ceCNty8)

2. Name the new dataset sales and leave the other settings as their default. Then click **CREATE DATASET**. The new dataset should appear in your **Explorer pane**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yDe9u2dYSYWY9pngv8yQmQ_b1ddf176d55c44c4bb5a8b5ccb38f1f1_AD_4nXcpvmTiiv5-ncbKTMtxMvtbbuIwa1WPVI6Hu3wrlNZtTBranmQY7x86Q1MU3GqkLNmIxsgGsyBwxSN819wzxiE_pJ_YdMhzDcD3WDdu4IQk1t-VUV0adSYP-8KbNrcL15ShMu35X80bG-hL65dnX9cxUBYqpmxWdBSBqBpyi90?expiry=1716940800000&hmac=YxUc-6LlpANRw-GJqB6761I-LrOuxM3Z0qdRATIQIBg)

3. Open the new dataset. **Click CREATE TABLE**. This will open a Create table menu. **Select create table from upload** and import your sales data. Name the table **sales_info,** select **Auto detect** under **Schema,** and leave the rest of the options as default. Then select **Create table.**

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AjoL9qohROiI5QNCaMcc_Q_4149ee57951049e5a12f272357e5c4f1_AD_4nXdtnAUqh2Sd5zpFlmRurT-n1I7qqlI6CKIc3YRhzs3dQjY5WwZlIWgUpm_2jsyOP9js5EuDRQtH-d9TQ4auRe6Yle7qHWMwKAHdDa8atzu0oLWbRvF7PGA5KvzxioVzsflU_e5g9v41wVh8dWar5TiFg3iOZhIdWMfTDq1eYWY?expiry=1716940800000&hmac=dasizFQe_Tn1t8vLrT9VVO3ONdbZVS3KWj192_toNiE)

4. Open the new table to inspect the schema and preview your data.

# **Step 4: Inspect the data**

Next, you will need to inspect the data to determine how much of it will be useful for your final analysis.

1. Ensure that the import was successful by running this query:

![Untitled](The%20data-validations%20process%202cf66f5d16f64ebeb1461a5f33d44117/Untitled.png)

Your results should appear like this:

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3omlKUnTSkCjfjyNs46ZWA_455ab4c85ebc43f191c146d8efd204f1_AD_4nXddg6qpsx8RWhOnQn_r3EpKVMhMh9Cx71HfzL1JMAmBTl10V34V2gfKiGOe1imtLKs2AIem2rhPLPM8u6BJPDyjEkDCBRUdesKh3kSszYtzE6SOgmcDnVz1-tpufpBqpu7ugETPjPlQ_NmW1n-QTE9hGHoxeL9j6XU1pbgsN_Y?expiry=1716940800000&hmac=OrWzX20ksnBmjbaPmxjQ4aSX4t9wAnTbJ_Ujb6V-Vlk)

2. Next, inspect the data to find out how many years of sales data it includes.You can use the MIN and MAX functions to get the oldest and newest dates:

![Untitled](The%20data-validations%20process%202cf66f5d16f64ebeb1461a5f33d44117/Untitled%201.png)

sales.sales_info;

Now you know what years this data covers. In this case, you’ll want to group the data by month because management wants to see year-over-year changes to inventory by month.

3. Click **COMPOSE NEW QUERY** and run the following query, which will return the total quantity sold for each ProductId grouped by the month and year it was sold:

```sql
SELECT  EXTRACT(YEAR FROM date) AS Year,  EXTRACT(MONTH FROM date) AS Month,  ProductId,  ROUND(MAX(UnitPrice),2) AS UnitPrice,  SUM(Quantity) AS UnitsSold FROM  sales.sales_info GROUP BY  Year,  Month,  ProductId ORDER BY  Year,  Month,  ProductId;
```

# **Step 5: Export the results to spreadsheet**

The subset of data you queried is fewer than 50,000 rows. This means it can be easily exported to a spreadsheet, if your stakeholder requests the data in this form. Or, you can use this exported spreadsheet for visualization. First, however, you’ll need to save your results.

1. After running the query, click **SAVE RESULTS**. There will be a pop-up menu with the option to choose the file type for export. Select **CSV Google Drive**. Once it is downloaded, open the new CSV file in Drive.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nkHf2vFpSDOYpbJDFt_Rcg_8f894e95cd2745bb84db6c366c6eedf1_AD_4nXfNDqjZkCH0nENgyvPP21On79q6OIPOahsMivKou2TzmQo7MUtvhMc0ru8iMEIR4Uwk1Z_lIvQI00aXM25bWuBbk80sh88AmwiCRUTneeqOfd0k0gcxzE166sQ12jo1cVvETs1JQX2y9bSpDz-nvMgFOaST8VSByCsTXoo0Dgk?expiry=1716940800000&hmac=NlUBd8ZJ5NDpEKW4iV4VhvggVJmYOxToCpBmj6b0t44)

2. Open the CSV file with Google Sheets.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/akGwzA00Q7iPPAAm1R70VA_b51de60f45574a2f936feb7a0b2e01f1_AD_4nXcaovGPwLD7mknReAkTvwvyBGguyJpCR1byF-WVbf-oH3ZddIVU5YNbyiDqNTT8z44k6-1jEjpCp9wnVYd8W9hQQukmvUom_gCzrYPnuPLtKdB0n69zgdpSrZudwk5a71pXR2yDd3muQQhhD6-3KTAYAuFwKKS1yNXurtHDDEg?expiry=1716940800000&hmac=eO259hHmdxUCnancB6xIfT5lr-UEQ6f47Lp2ByaTsHg)

There should be about 47,000 rows. Right-click on the sheet tab and rename the sheet **Sales**.

3. Next, if you’re using Sheets, you can open these results by selecting the **File menu** and clicking **Import**.

This will open a pop-up menu. Click **Upload** and select the inventory CSV file.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VJqqzySMRcazUn1vBEaIXw_d4ed936511714f18a59a8055d3809bf1_AD_4nXe31jKpXSOFmiNAuWlJXa0GtFCvKvBOqsx8bhSU2BpYM1VCiIwj-zlnydbrpxyBTXH0JnsvLc8_BVWTpjWAnF5fRNYs8KxYzXmY7eR6HF0cmvYd99lttr61NEuW8MDauhdKBn8qKqJTCqF5aQFsXX4W8I9k4OIMheozXv_l-w?expiry=1716940800000&hmac=Fv3UBPasGCpBfgiSeuHd2-VmTVX5PvNeaGQ-YRYzq4E)

Select **Insert new sheet(s)** to add this data as a worksheet to your spreadsheet and choose **Comma** for **Separator type**.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ptEPkk-CQXmsw9D2IXc3AQ_dca90de24e0b4f4f94e50b90236abff1_AD_4nXeDgPilAboLACfvUhYbNhHvI9H7TVJDun47TZuQEH-yInMud-Ll-PTQDKLewoHLGWMX_OV_JHJgiqjAumN9wlI-XWtDGtdTFce5ngDma8-VUW26zKWauu69mHL99fxWY4QcxtFzr3FwRQcFRj4l_tT5RWz26ApGByQMS3uUkOg?expiry=1716940800000&hmac=ET_sMY3J6kUHcSq1DGP-Kc_82IbeHyX6_DUnR4ApzgM)

4. Repeat these steps for the productsCSV file.

---