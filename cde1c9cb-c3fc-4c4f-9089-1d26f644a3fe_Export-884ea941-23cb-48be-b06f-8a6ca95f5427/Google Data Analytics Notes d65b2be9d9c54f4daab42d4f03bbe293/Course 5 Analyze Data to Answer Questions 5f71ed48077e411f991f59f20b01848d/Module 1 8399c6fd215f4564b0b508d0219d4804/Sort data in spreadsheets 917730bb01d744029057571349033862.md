# Sort data in spreadsheets

---

# Step-by-step: Sort datasets in spreadsheets

[index (10).mp4](Sort%20data%20in%20spreadsheets%20917730bb01d744029057571349033862/index_(10).mp4)

This reading outlines the steps the instructor performs in the following video, [Sort datasets in spreadsheets](https://www.coursera.org/learn/analyze-data/lecture/6f6R0/sorting-datasets). In this video, the instructor demonstrates how to sort data in spreadsheets with the data menu.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference tool if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

If you’d like to access the spreadsheet the instructor uses in this video, click the link to the dataset to create a copy. If you don’t have a Google account, you may download the data directly from the attachments below.

Link to movie data starter project:  [Movie data starter project](https://docs.google.com/spreadsheets/d/1FLaUmMn62YlHYihV6pK1DJqWcFYCnuoqoxFWmm_o5b0/template/preview).

OR

[Movie Data Starter ProjectXLSX File](https://d3c33hcgiwev3.cloudfront.net/NrzEyoWGRhix-2gQUzoZag_31090f90399f4347b98b63d02b95a9e1_Movie-Data-Starter-Project.xlsx?Expires=1716854400&Signature=CfIzKnA8esgAs-NgatJ9T~cVm3XksFOxxhonFE1QTBQLqsl9XMM3BHAGc3pTVPNSHDrXKTO-jThzZa7iy8CsD7t900K~91L-U00nvEbtBCUW9LnVwfpqD7k~9iRfc8Qqd7~c0vilyhSaUj3sPRtvUUO1iA2BF9ok-EUNkf48dEM_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716854400000&hmac=27km6Ra9-l9jyGnKFs9mjrEEy41ZOo2-8wHCwg08J1M)

## Example 1: Sort a sheet with the menu

Use the menu to quickly and easily sort an entire sheet, keeping rows together.

1. Open the [Movie data starter project](https://docs.google.com/spreadsheets/d/1FLaUmMn62YlHYihV6pK1DJqWcFYCnuoqoxFWmm_o5b0/template/preview) spreadsheet.
2. Select cell **B** to highlight all of **column B**.
3. Select **Data** from the menu.
4. Select **Sort sheet**.
5. Select **Sort sheet by column B (A to Z)**.
6. Notice that the movies in your spreadsheet are now arranged in chronological order based on the release date.

**Note:** In the video, the sorted results are not entirely correct as shown. While the release dates appear to be sorted in ascending order, many of the movie titles are also in alphabetical order. As a data analyst, you may suspect that this is too much of a coincidence and that something is not quite right with the data. In this example, the movie titles in column A may have been previously sorted alphabetically and the data wasn’t restored to the original unsorted format.

## Example 2: Sort data in a specific column with the menu

Use the menu to sort one column without affecting how the rest of the sheet is arranged. Each row in a table describes a single observation, so if you sort only one column you can introduce errors throughout your dataset. Use caution when using this option!

1. Select cell **A** to highlight all of **column A**.
2. Select **Data** from the menu.
3. Select **Sort range**.
4. Select **Sort range by column A (A to Z)**.
5. Notice that the movie data across the rows is now jumbled because sorting a single column in a sheet doesn’t keep data in a row together.

**Note:** As you’ve learned, each row in a table describes a single observation. Here, the values in Column A (movie titles) were sorted in A-to-Z order, but the rest of the sheet wasn’t sorted. For example, before sorting by column A, *The Devil Inside* was listed as having a release date of 2012-01-06. After sorting only the movie titles in Column A in A-to-Z order, however, *The Devil Inside* is listed as having a release date of 2015-06-16. This is incorrect.

---

# Step-by-step: Use the SORT function in spreadsheets

[index (11).mp4](Sort%20data%20in%20spreadsheets%20917730bb01d744029057571349033862/index_(11).mp4)

This reading outlines the steps the instructor performs in the next video, [Use the SORT function im spreadsheets](https://www.coursera.org/learn/analyze-data/lecture/K6WB8/the-sort-function). In this video, the instructor demonstrates how you can use the **SORT** function to arrange data into a meaningful order to make it easier to understand, analyze, and visualize.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

**What you’ll need**

If you’d like to follow along with the examples in this video, choose a spreadsheet tool. Google Sheets or Excel are recommended.

To access the spreadsheet the instructor uses in this video, click the link to the template to create a copy of the dataset. If you don’t have a Google account, download the data directly from the attachments below.

Link to dataset: [Party plan spreadsheet](https://docs.google.com/spreadsheets/d/1L1Z6b3X9WCpwzisHcxvjC5-Qett-BOMo9yg8Cz36NME/template/preview)

OR

[Party Plan SpreadsheetXLSX File](https://d3c33hcgiwev3.cloudfront.net/SifBvA71QgKf-sX-0JyvSw_7a45f15631e54e65aa3541c76da0d3e1_Party-Plan-Spreadsheet.xlsx?Expires=1716854400&Signature=j~AXC2U7iVdtMBAdVh1L4VeaehlkzUN5gFi6~vwvcBNkWSKS0l89chyR8e~StiVkCGqdlRnj7hQfLmyoYLiKEjhD2Ywhbc9cBz89aRsdSbe7swxKXx8TTak0GkcqDP~r03vdL3qS0cC-~2szJEc2DZn3dSuUOtq9PRIB94becLU_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z65IW3QCSOmuSFt0Aijp8w_914270a3d2e84027b46e404f7a52007f_line-y.png?expiry=1716854400000&hmac=27km6Ra9-l9jyGnKFs9mjrEEy41ZOo2-8wHCwg08J1M)

## Example 1: Sort guests by table

Use a spreadsheet function to sort guests by the table to which they’re assigned.

1. Open the [Party plan spreadsheet](https://docs.google.com/spreadsheets/d/1L1Z6b3X9WCpwzisHcxvjC5-Qett-BOMo9yg8Cz36NME/template/preview).
2. Select cell G1 and enter the equal sign **=**.
3. Enter **SORT** followed by an open parenthesis **(** to begin the **SORT** function.
4. Enter the first cell from the Guest column of the spreadsheet, **A2**, followed by a colon [**:**], then enter the last cell from the Sent Invitation column, **D6**, followed by a comma. **A2:D6** is the range of cells over which this function will sort.
5. Enter **2** followed by a comma to specify the column by which to sort the data. Note that the function doesn't recognize letters, so use the column’s number. Column A corresponds to 1, B corresponds to 2, and so on.
6. Enter **TRUE** followed by a close parenthesis **)**. **TRUE** means the function will return results in ascending order, so the tables will be listed starting with table one. **Note:** To return results in descending order, enter **FALSE**.
7. Press **Enter** (Windows) or Return (Mac).

The party guests are now sorted by the table to which they’re assigned.

## Example 2: Customized sort order

When you sort data in a spreadsheet using multiple conditions with a customized sort order, data is sorted  based on the order in which the conditions are applied to the data. To sort party guests by whether or not they've been sent an invitation and to list the guests alphabetically:

1. Highlight all the data in the party plan spreadsheet: **cells A1 to D6**.
2. In the menu, select **Data > Sort range > Advanced range sorting options**. This opens the **Sort range** from A1 to D6 dialog box.
3. Check the **Data has a header row** checkbox to make sure column titles aren’t included in the sorted data.
4. From the **Sort by** drop-down list, select **Sent Invitation**.
5. Select the **A to Z** radio button to make sure the *No* responses are listed first and the *Yes* responses are listed second.
6. Select **Add another sort column** to add the additional sorting condition.
7. From the **Sort by** drop-down list, select **Guest Names** to list guests alphabetically.
8. Select the **A to Z** radio button.
9. Select **SORT**.

This returns your customized sort order, which lists the *No* invitations and those guests alphabetically, followed by the *Yes* invitations and those guests alphabetically.

---

# Sort and filter in Sheets and Excel

In this reading, you’ll examine the sorting and filtering options in Google Sheets and Microsoft Excel. Both offer basic sorting and filtering from set menu options. But if you need more advanced sorting and filtering capabilities, you can use their respective **SORT** and **FILTER** functions.

## Sort and filter in Sheets

Sorting in Google Sheets helps you quickly spot trends in numbers and text. For example, as the vice president of sales at a candy company, you want to improve chocolate sales in lower-performing regions—your company makes delicious chocolate and you know sales can improve. As a first step, you examine this by calculating gross (total) revenue of chocolate by sales region. In this case, you could sort the gross revenue column in **descending** (Z to A) order to find the top performing regions at the top, or sort the gross revenue column in **ascending** (A to Z) order to find the lowest performing regions at the top. Then, you can look at patterns in the best and worst regions to explore how to increase sales in the lower-performing regions.

If you want to learn more about the set menu options for sorting and filtering, start with these resources:

- [Sort and filter data](https://support.google.com/docs/answer/3540681) (Google Help Center): instructions to sort data in alphabetical or numerical order and create filter views
- [Sort data by selecting a range of data in a column](https://www.youtube.com/watch?v=VcRBHXBMKBU): video of steps to achieve the task
- [Sort a range of data using sort criteria for multiple columns](https://blog.sheetgo.com/google-sheets-formulas/sort-formula-google-sheets/): technical tip instructions by SheetGo company to sort data across multiple columns

In addition to the standard menu options, the **SORT** function allows you to do more advanced sorting. Use this function to create custom sorting rules. You can sort the rows of a given range of data by the values in one or more columns. And you can set the sort criteria for each column. Refer to the [SORT function](https://support.google.com/docs/answer/3093150?hl=en) page for the syntax.

Like the **SORT** function, use the [FILTER function](https://support.google.com/docs/answer/3093197?hl=en) to filter by any matching criteria you like. This creates a custom filter.

As you’ve learned, you can filter data and then sort the filtered results. Using the **FILTER** and **SORT** functions together in a range of cells can programmatically and automatically achieve these results for you.

## Sort and filter in Excel

You can also sort in ascending (A to Z) and descending (Z to A) order in Microsoft Excel. Excel offers **Smallest to Largest** and **Largest to Smallest** sorting options when you’re working with numbers.

Similar to the **SORT** function in Google Sheets, Excel includes custom sort capabilities that are available from the menu. After you select the data range, click the **Sort & Filter** button to select the criteria for sorting. You can even sort by the data in rows instead of by the data in columns if you select **Sort left to right** under **Options**. (**Sort top to bottom** is the default setting to sort the data in columns.)

If you want to learn more about sorting and filtering in Excel, start with these resources:

- [Sort data in a range or table](https://support.microsoft.com/en-us/office/sort-data-in-a-range-or-table-62d0b95d-2a90-4610-a6ae-2e545c4a4654) (Microsoft Support): instructions to perform sorting in a variety of use cases
- [Excel training: sort and filter data](https://support.microsoft.com/en-us/office/video-sort-data-in-a-range-or-table-ffb9fcb0-b9cb-48bf-a15c-8bec9fd3a472#ID0EAABAAA=Transcript) (Microsoft Support): sorting and filtering videos with transcripts
- [Excel: sorting data](https://www.youtube.com/watch?v=Ep5q1cUhQas): video of how to use the **Sort & Filter** and **Data** menu options for sorting

Excel also has [SORT](https://support.microsoft.com/en-us/office/sort-function-22f63bd0-ccc8-492f-953d-c20e8e44b86c), [SORTBY](https://support.microsoft.com/en-us/office/sortby-function-cd2d7a62-1b93-435c-b561-d6a35134f28f), and [FILTER](https://support.microsoft.com/en-us/office/filter-function-f4f7cb66-82eb-4767-8f7c-4877ad80c759) functions. Explore how you can use these functions to automatically sort and filter your data in spreadsheets without having to select any menu options at all.

## Sort and filter manually with menus and buttons

Both Sheets and Excel feature menu options designed to let you sort and filter without using functions. For example, after selecting the data you’d like to sort in Google Sheets, you can choose **Data > Sort sheet** or **Data > Sort range** to sort that data. To filter the data, select all the columns and rows and choose **Data > Create a filter**. In Excel, you can use the **Sort & filter** button to bring up a user-friendly interface that guides you through sorting or filtering.

Finally, when using menus or buttons, here are a couple of best practices:

- Back up or make a copy of your data before making major changes.
- When filtering data, keep in mind that other users may also be accessing the spreadsheet. For example: Filters in Google Sheets can affect all viewers, so you should use filter views for personal filtering.

## Key takeaways

As you’ve learned, you can sort and filter data in Google Sheets and Excel with functions or by using menus and buttons. Sorting data is the process of arranging data into a meaningful order to make it easier to understand, analyze, and visualize. This can help you identify trends in the data. Filtering is the process of showing only the data that meets a specified criteria while hiding the rest. Once you’ve filtered data, you can sort it to find trends within those criteria. Menus and buttons offer the ability to do basic sort and filter functions, but you’ll need to use a function for custom sorting and filtering.

---