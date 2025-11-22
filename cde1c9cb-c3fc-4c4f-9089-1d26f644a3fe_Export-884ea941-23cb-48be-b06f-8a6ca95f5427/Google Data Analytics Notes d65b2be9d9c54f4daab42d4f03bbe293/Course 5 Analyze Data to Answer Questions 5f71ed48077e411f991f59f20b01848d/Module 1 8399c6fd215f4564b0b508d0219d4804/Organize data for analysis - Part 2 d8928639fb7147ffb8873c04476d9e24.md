# Organize data for analysis - Part 2

---

# Sort and filter data to keep it organized

The first two phases of data analysis, **Organize data** and **Format and adjust data**, are important for data analysts because they can use these phases to manipulate their data in ways that make important patterns and trends more obvious. Most of the datasets you’ll use as a data analyst will be organized as tables. Tables are helpful because they let you manipulate and categorize your data. Having distinct categories and classifications lets you focus on, and differentiate between, the groups in your data quickly and easily.

Sorting and filtering are two methods you can use to organize, format, and adjust data. For example, a filter can help you find errors or outliers so you can fix or flag them before your analysis. Outliers are data points that are very different from similarly collected data and might not be reliable values. The benefit of filtering the data is that after you fix errors or identify outliers, you can remove the filter and return the data to its original organization.

In this reading, you’ll review sorting and filtering and consider how they can be used together. You’ll also be introduced to how a particular form of sorting is done in a pivot table.

## Sort data

Sorting is the process of arranging data into a meaningful order to make it easier to understand, analyze, and visualize. It ranks your data based on a specific metric you choose. You can sort data in spreadsheets, SQL databases (when your dataset is too large for spreadsheets), and tables in documents.

To rank items or create chronological lists, you can sort by ascending or descending order. Sorting arranges the data in a meaningful way and gives you immediate insights. Sorting also helps you to group similar data together by a classification. For example, if a ski resort design company wants to evaluate the resorts designed by a competitor, a data analyst can sort competitive resorts by locations, runs, acreage, and other factors. This way, the firm’s designers can visit the types of resorts they also design and gather information that could be used in its own future designs.

An example of sorting a spreadsheet of ski resorts, including information about resort name, state/territory/country, lifts, runs, and acres. The image taker has clicked into the Data menu option, selected Sort sheet, and is hovering over Sort sheet by column A (A to Z).

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WHXvpntATfChQSG-exnbwg_e40c6a897b7c4ea4ac6a0f22ca5519e1_8TzqPKTZMV1MQRHlSr1s6VQr4vY-ue5B1d3ZRqEKT6snfVRczMT2ifLAd88PvoRCjYaTPZXs3RGgUM038_KcUaNpr7_jyNfr7UL-ULQqd2GVA1QerJeQCh27wE2xFu0miLqQnlTMnXaiKjioEwG5LKaUK2IfGqbgByOGk138tCLheDpY8rnVdVP5Z76QZKT6OQWk81U3ocPO6Byo8foTyYaYZwp2qqjOzaDs6g?expiry=1716854400000&hmac=Sure--LAcR5ssmhnlHg086CCsAmv8XncEaZxkCJqJps)

## Filter data

Sometimes, an analysis may require only a subset of the data in your dataset. You can use a filter to show only the data that meets a specified criteria while hiding the rest. Filtering is useful when you have lots of data. You can save time by zeroing in on the data that’s important for your current analysis or the data that contains errors. Most spreadsheets and SQL databases allow you to filter your data in a variety of ways. Filtering gives you the ability to find what you are looking for without too much effort.

For example, if the ski resort design company wants to inspect specific criteria for the competitive ski resorts they intend to visit and evaluate, a data analyst can filter the competitive resort database to extract information about the number of runs compared to acreage to identify design trends or other insights.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Xw7QVKG2R-Gc7QoyTFQtIw_ac0089354a1346bb97df4d2655ec1fe1_noY6fYMsWg8nJS64kDUZDX3myITNIPdCDXicuml2syAjA1i3RtOpoYHJHl-pWSOiRTCFMy-7l-UH6oHUC1lW_h6hG3OwuEYnuIZrEc1Dc5fjPjzYcdRE6xeceU6-jutaS0c_zUNQe9xJoRwTOkhWG81_RTsNuwHQhTpkZJNh66OwiRgc-qj83ehfRyppr0uqF6IZKwhcVTp0Z29nrOTqqz9B1waGe9H5IJyVaQ?expiry=1716854400000&hmac=uH8go7rjHKH5B3n5XzQnKyBRbX93waWyuU4S3_voePg)

An example of filtering data in a spreadsheet of ski resort information by specific evaluation criteria such as location, acreage, or number of runs

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SgDPUoXIQ7WhGtKTTCKZ-A_c23a1eebc7c64d89ba00b73a9533f4e1_0ePn0aa78jdfZwx2C1SIDV0amIKtd-39qUhrWQhvejNFvTDB8-mto-zVDet0ZjJq7fZh4HCRXpIFs5Q4iI1-7qqaVMYCbPu1YUf5oKUjjPhx2uNdcfIqdNOWgnLoYpTUhK4qmxRf3jqdE0ZuRbRnmR2U2HW7nt258gT5gP0CmCYsbLoQVwzH8XZnIDUJIRmq1qnjCJ9YcGzJEPzyH3eTgrf4pgNMWCBYcvqNvA?expiry=1716854400000&hmac=XK30J6AIDoYdGewLakhtKxN6Fj_NQvsGKMn0Y05jB7M)

### **Sort a pivot table**

A pivot table is a data summarization tool used to sort, reorganize, group, count, total, or average data. Items in the row and column areas of a pivot table are sorted in ascending order by any custom list first. If the items aren’t in a custom list, they will be sorted in ascending order by default. But, if you sort in descending order, you are setting up a rule that controls how the field is sorted even after new data points are added. For example, in the ski resort dataset, the pivot table allows locations to be sorted alphabetically by state, territory, or country.

Image of a pivot table of the ski resort data, with the pivot table editor open and ready for parameters to be entered. The data is grouped by state, territory, or country.

[](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/u3lRUIlqQ-KPIMIOURQy6A_5b0dd2ad1f264272963ea7e7b044dbe1_EuU1DP1DQYMB3tgzFZHANoDEGmEHWf55zjxwjC3PRHG6lSOslfUvEGYNB3sIesFvTyyFjhauzllGbVNjbewnWwhbriZodN-uZ7a5xG_YThe64gW4QA4-Z-Bt_PqoAfH6H2n6SVBXg2RGRgQPAysQH5BYlitBTuR98ul2fC9xPbY81Ps1sLB2LCgoNY1bz7MnSKGqtIDgjwstEjaBgwUKoz54DAjDZ93Gu80zqA?expiry=1716854400000&hmac=KmQcKjpw2wVTgVaG8Ee-EtECn1OfpBGgVLgQmJcq_X4)

## Key takeaways

Data analysts filter and sort data to organize it for better understanding, analysis, and visualization. Sorting arranges data in a meaningful order, while filtering displays only data that meets specific criteria. Combining filtering and sorting allows for organizing only relevant data for analysis. Both spreadsheets and SQL databases allow for data filtering and sorting data.

---

# Upload the movie dataset to BigQuery

The next video demonstrates how to use SQL to filter data in a large dataset in BigQuery.

If you would like to follow along with the instructor, you will need to log in to your BigQuery account and upload the movie dataset provided as a .csv file.

## Prepare for the next video

First, download the .csv file from the attachment below:

[Movie DataCSV File](https://d3c33hcgiwev3.cloudfront.net/KNFbyUKxRKiRW8lCsQSo8A_8adeac50825b4df68daaf6055c404ef1_Movie-Data.csv?Expires=1716854400&Signature=MCQnOtECuJEaYnWSojT-vFfiy84wHdVgmFoAD6Rs4AO2i7BcMqxVtAjINFES7~iBG9V8fxWhnSK-Gnth4gj2Fs3tiHk7--l9qRw5rZlw6GjRBKzn81y7voZT-164mqPYGuf-1RhPTqT3oDnR9B1sPVTnWGl4l8YT1Th0c3EmaLg_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

- **Note:** If the .csv files open in a new tab instead of downloading to your machine, follow these instructions:
    - Select **File** from the menu bar, then select **Save as Google Sheets**. This will open the .csv file as a Google Sheet.
    - Select **File** from the menu bar, then select **Download** from the dropdown menu, then select **Comma Separated Values (.csv)**.

Next, complete the following steps in your BigQuery console to upload the movie dataset.

**Step 1:** Open your BigQuery console and click on the project you want to upload the data to.

**Step 2:**  In the **Explorer** on the left, click the **Actions** icon (three vertical dots) next to your project name and select **Create dataset**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/WLc3wB8cSgyt42QStAfdbA_6f332382a41c4a388c36f8caab7141f1_5.CreateDataset.jpg?expiry=1716854400000&hmac=tfEp2y2uP1p0no44rJ23GV3xPX_cqEC6XyHVXfSyY5o)

**Step 3:** In the upcoming video, the name **movie_data** will be used for the dataset. If you plan to follow along with the video, enter **movie_data** for the Dataset ID. In the *Location Type* section, select **Multi-region,** then from the *Multi-region* dropdown select **US (multiple regions in United States)**, and make sure the default *Encryption* method within the Advanced options is set to the **Google_managed encryption key**.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uqPortPlQzaPLJKTCuOEEg_e401815349df4df5b99aaaa288c98cf1_1.createdataset.jpg?expiry=1716854400000&hmac=fv2rJt9ghF88Af4ccFWiut79GpDuPuj6UGlXfdti3j8)

**Step 4:** Click **CREATE DATASET** (blue button) to add the dataset to your project.

**Step 5:** In the **Explorer** on the left, click to expand your project and then click the **movie_data** dataset you just created.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vwu6KLCHSPS_-_TNzueXKg_8a18939893714a6b9594d09d4f1787f1_2.moviedata.jpg?expiry=1716854400000&hmac=MeM9L_jJAAWCnp7ufxTvvQc3qWO3GmoSumNAJjrvWqE)

**Step 6:** A new window will appear titled **movie_data,** and make a note of the **Dataset ID.**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/BVGWY9N8SeaE-f6G8mZlFQ_104e7ebd497b44b68ee4ac23908cc8f1_3.datasetinfo.jpg?expiry=1716854400000&hmac=Fy9UHRkkhgSJnwep8Fj069yF6NsSwEf20L_Ph7H5Nvk)

**Step 7**: Towards the right hand side of the page, you will see a tab row of additional commands. Click the first blue button titled **+ CREATE TABLE** at the top right. A new window titled *Create table* will appear.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/U56fBwrYRW6GnJMmG38zSw_025b33c23f1d4bc881678d17951c98f1_4.createtable.jpg?expiry=1716854400000&hmac=O72jVbtCkH-9mF4WovSBxNsOkcojx1yXsUTupWko5KQ)

**Step 8:** Under *Source,* for the *Create table from* dropdown, select the data source.

- Select **Upload**.
- Click **Browse** to select the **movie_data.csv** file you downloaded.
- Select **CSV** from the file format dropdown, but BigQuery should automatically change the format.

**Step 9:** Under *Destination,* for the *Table* name, enter **movies** to match the table in the video.

**Step 10:** Under *Schema,* click the **Auto detect** checkbox.

**Step 11**: Once all of the settings have matched the image above, click the **CREATE TABLE** (blue button) at the bottom. You will now see the **movies** table under your **movie_data** dataset in your project.

**Step 12:** Click **movies** and then select the **Preview** tab. Confirm that you have access to the appropriate table.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xm1YofnxQuClZWAZwImSFQ_e174535d7af549b69e75bf6ed48261f1_5.movieswindow.jpg?expiry=1716854400000&hmac=zox65pPWG9FSttwUWAwaNwb8cbpgR6Spj_nFAwD9P9A)

---

# Step-by-Step: Filter data with SQL

[index.mp4](Organize%20data%20for%20analysis%20-%20Part%202%20d8928639fb7147ffb8873c04476d9e24/index.mp4)

This reading outlines the steps the instructor performs in the following video, [Filter data with SQL](https://www.coursera.org/learn/analyze-data/lecture/Y5Nmb/more-on-sorting-and-filtering). In the video, the instructor demonstrates filtering data with SQL using **WHERE** clauses.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

If you’d like to follow along with the instructor, you will need to log in to your BigQuery account and upload the Movies dataset. To do this, follow the instructions in the reading [**Upload the movie dataset to BigQuery**](https://www.coursera.org/learn/analyze-data/supplement/sBFZn/optional-upload-the-movie-dataset-to-bigquery).

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716854400000&hmac=27km6Ra9-l9jyGnKFs9mjrEEy41ZOo2-8wHCwg08J1M)

## Example 1: Filter data in SQL

Complete the following steps to use the **WHERE** clause to filter the database and narrow down the list to movies in the comedy genre.

1. In the BigQuery **Explorer pane**, select the **movie** dataset then the **movies** table.

2. Select the **Preview** tab from the **Details pane**.

3. Select **Query** then **In new tab** and enter the following code into the query editor:

![Untitled](Organize%20data%20for%20analysis%20-%20Part%202%20d8928639fb7147ffb8873c04476d9e24/Untitled.png)

**Note:** If you’re completing this code in BigQuery, replace **projectID** in the code block to your own projectID.

4. Use the **WHERE** clause to filter the data. Enter **WHERE Genre = 'Comedy';** to filter for and select rows with 'Comedy' in the Genre column.

5. Your code should now match this code block:

![Untitled](Organize%20data%20for%20analysis%20-%20Part%202%20d8928639fb7147ffb8873c04476d9e24/Untitled%201.png)

6. Select **RUN** to run the query. The results display a shorter list of movies, all in the comedy genre.

---