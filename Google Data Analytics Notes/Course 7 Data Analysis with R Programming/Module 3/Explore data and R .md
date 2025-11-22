# Explore data and R

---

# Data in R

**1. Data Frames:**

- **Definition:** A data frame is a two-dimensional structure that stores data in a tabular format, similar to a spreadsheet. Each column represents a variable, and each row represents an observation.
- **Key Points:**
    - Data frames are fundamental to data analysis in R.
    - They allow you to organize and manipulate data efficiently.
    - You'll learn how to create, access, and modify data frames in this module.

**2. Tidyverse Packages:**

- **Definition:** Tidyverse is a collection of R packages designed for data manipulation and visualization. It provides a consistent and user-friendly interface for working with data.
- **Key Points:**
    - Tidyverse packages streamline common data analysis tasks.
    - They make your code more readable and efficient.
    - You'll explore various tidyverse packages and their functionalities.

**3. Checking for Bias in R:**

- **Definition:** Bias in data analysis refers to systematic errors that can lead to inaccurate conclusions. It's crucial to identify and address potential biases to ensure reliable results.
- **Key Points:**
    - R provides tools and techniques for detecting and correcting bias.
    - You'll learn how to identify different types of bias and apply appropriate methods to mitigate them.

**4. R Community:**

- **Definition:** The R community is a global network of R users who share knowledge, resources, and support.
- **Key Points:**
    - The R community is a valuable resource for learning and troubleshooting.
    - You can participate in forums, discussions, and workshops to connect with other R users.
    - The community can help you improve your R skills and knowledge.

**5. Data Cleaning:**

- **Definition:** Data cleaning involves identifying and correcting errors, inconsistencies, and missing values in your data.
- **Key Points:**
    - R offers powerful tools for data cleaning.
    - You'll learn how to use these tools to improve the quality of your data.
    - Effective data cleaning is essential for accurate analysis.

**6. Code Review:**

- **Definition:** Code review involves examining and evaluating your code for correctness, efficiency, and best practices.
- **Key Points:**
    - Code review can help you identify and fix errors in your code.
    - It can also improve the readability and maintainability of your code.
    - The R community provides opportunities for code review and collaboration.

**7. Putting it all together:**

- This video emphasizes the practical application of R skills for data analysis.
- You'll learn how to use R to clean, manipulate, and visualize data effectively.
- By leveraging the tidyverse packages and the R community, you can enhance your data analysis capabilities and gain valuable insights from your data.

---

# R data frames

[index (69).mp4](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/index_(69).mp4)

**Key Points:**

- **Data Frames:**
    - A collection of columns, similar to spreadsheets or SQL tables.
    - Used to summarize and organize data for easy analysis.
    - Each column represents a variable, and each row contains a set of values for each variable.
    - Important characteristics:
        - Named columns.
        - Data types can be numeric, factor, character, dates, time stamps, or logical vectors.
        - Same number of data items in each column.
- **Tibbles:**
    - Streamlined data frames within the tidyverse.
    - Easier to work with than standard data frames.
    - Key differences:
        - Never change data types of inputs.
        - Never change variable names or create row names.
        - Automatically set to display only the first 10 rows and fitting columns for easier printing.
- **Importance:**
    - Data frames and tibbles are the building blocks for analysis in R.
    - Consistent data structures facilitate communication, collaboration, and reproducibility of analysis.
    - Enable easier data sharing and operation on entire datasets.
- **Tidy Data Principles:**
    - Variables in columns, observations in rows, each value in its own cell.
    - Standardizes data organization within R for better understanding and analysis.

**Definitions:**

- **Data Frame:** A two-dimensional data structure with rows and columns, similar to a spreadsheet or SQL table.
- **Tibble:** A specialized data frame within the tidyverse, designed for easier data manipulation and analysis.
- **Variable:** A characteristic or attribute being measured or observed.
- **Data Type:** The format of data, such as numeric, character, or logical.
- **Tidy Data:** Data organized according to specific principles for better analysis and understanding.

**Additional Notes:**

- The video emphasizes the importance of consistent data structures for effective communication and collaboration in data analysis.
- It introduces the concept of tidy data, which promotes clear and organized data structures for easier analysis.
- The video provides a foundation for understanding and working with data frames and tibbles in R, which are essential tools for data analysis.

**Further Resources:**

- For more information on data frames and tibbles, you can refer to the following resources:
    - RStudio Data Import documentation: https://r4ds.had.co.nz/data-import.html
    - Tidyverse documentation: https://www.tidyverse.org/
    - R for Data Science book: https://r4ds.had.co.nz/

---

# Working with data frames

[index (70).mp4](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/index_(70).mp4)

**Key Points:**

- Data frames are the fundamental structure for working with data in R.
- They are similar to spreadsheets with rows and columns.
- R has many built-in datasets for practice, including the "diamonds" dataset used in this video.
- You can use the `head()` function to view the first few rows of a data frame.
- The `str()` function shows the structure of a data frame, including column names and data types.
- The `colnames()` function returns only the column names of a data frame.
- The `mutate()` function allows you to add new columns to a data frame based on calculations or transformations of existing columns.

**Definitions:**

- **Data frame:** A two-dimensional data structure with rows and columns, similar to a spreadsheet.
- **Head function:** A function that returns the first few rows of a data frame.
- **Structure function:** A function that shows the structure of a data frame, including column names and data types.
- **Column names function:** A function that returns the names of the columns in a data frame.
- **Mutate function:** A function that adds new columns to a data frame based on calculations or transformations of existing columns.

**Detailed Summary:**

The video begins by highlighting the importance of data frames in data analysis. It explains that data frames are the primary way data analysts interact with data and are essential for performing various tasks.

The video then introduces the "diamonds" dataset, which is built-in to R and provides a good example for practicing data manipulation techniques. It demonstrates how to load the dataset using the `data()` function and how to view the first few rows using the `head()` function.

Next, the video explains how to examine the structure of a data frame using the `str()` and `colnames()` functions. These functions provide information about the column names and data types, which is crucial for understanding the data.

Finally, the video introduces the `mutate()` function, which allows users to add new columns to a data frame based on calculations or transformations of existing columns. The video demonstrates how to create a new column called "carat_2" by multiplying the existing "carat" column by 100.

---

# Hands On Activity: Create your own data frame

Earlier, you learned that a data frame is a collection of columns containing data, similar to a spreadsheet or SQL table. Data frames are one of the basic tools you will use to work with data in R. You can create data frames manually, or from different data sources. In this activity, you will create and use data frames in R.

By the time you complete this activity, you will be able to create data frames with the **data.frame()** function to summarize and organize data in R, which will help you better understand data.

Follow the instructions to complete each step of the activity. Then answer the questions at the end of the activity before going to the next course item.

# **Step 1: Work in RStudio or RStudio Desktop**

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, Save a Permanent Copy, and the project will be saved in your main dashboard for use with future lessons. Once that is completed, navigate to the file explorer in the bottom right and click on the following: Course 7 -> Week 3 -> Lesson2_Dataframe.Rmd.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

[Lesson2_Dataframe.txt](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/RSYCoU88Q66mAqFPPNOuKQ_4d3ab0b8fa0547f6996a66ab05babcf1_Lesson2_Dataframe.txt)

You can also find the Rmd file with the solutions for this activity here:

[Lesson2_Dataframe_Solutions.txt](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/MUc2CUiKRM6HNglIiqTOSg_875c2debff6649828daca8a409d9c7f1_Lesson2_Dataframe_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.

# **Step 2: Complete the activity**

Carefully read the instructions in the comments of the .Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the .Rmd file, return here to confirm that your work is complete.

---

# More about tibbles

In this reading, you will learn about tibbles, which are a super useful tool for organizing data in R. You will get a review of what tibbles are, how they differ from standard data frames, and how to create them in R.

## Tibbles

Tibbles are a little different from standard data frames. A data frame is a collection of columns, like a spreadsheet or a SQL table. Tibbles are like streamlined data frames that are automatically set to pull up only the first 10 rows of a dataset, and only as many columns as can fit on the screen. This is really useful when you’re working with large sets of data. Unlike data frames, tibbles never change the names of your variables, or the data types of your inputs. Overall, you can make more changes to data frames, but tibbles are easier to use. The tibble package is part of the core tidyverse. So, if you’ve already installed the tidyverse, you have what you need to start working with tibbles.

### **Creating tibbles**

Now, let’s go through an example of how to create a tibble in R. You can use the pre-loaded *diamonds* dataset that you’re familiar with from earlier videos. As a reminder, the *diamonds* dataset includes information about different diamond qualities, like carat, cut, color, clarity, and more.

You can load the dataset with the **data()** function using the following code:

**library(tidyverse)**

**data(diamonds)**

Then, let’s add the data frame to our data viewer in RStudio with the **View()** function.

**View(diamonds)**

The dataset has 10 columns and thousands of rows. This image displays part of the data frame:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vRf33YfiS_yX992H4qv8Mw_6a91eeac27a544c684de8f57d906764e_Screenshot-2020-11-02-at-9.43.48-AM-1-.png?expiry=1717113600000&hmac=sIGvhwR08ZrVqXT9IK1yyXM5y2_6y1wGHjZ0qNDbd60)

Now let’s create a tibble from the same dataset. You can create a tibble from existing data with the **as_tibble()** function. Indicate what data you’d like to use in the parentheses of the function. In this case, you will put the word “diamonds."

**as_tibble(diamonds)**

### **Results**

When you run the function, you get a tibble of the *diamonds* dataset.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ykUrci7HS4KFK3Iux9uCpg_f0d7cc49563347b49d4dd322b80ae11a_Screen-Shot-2021-03-15-at-1.58.27-PM.png?expiry=1717113600000&hmac=JlVkJ8UekF-dHJgZ-85BrirkKIdeZ8vU7LA1fBuPF_g)

While RStudio’s built-in data frame tool returns thousands of rows in the *diamonds* dataset, the tibble only returns the first 10 rows in a neatly organized table. That makes it easier to view and print.

## Additional resources

For more information on tibbles, check out the following resources:

- The entry for [Tibble](https://tibble.tidyverse.org/) in the tidyverse documentation summarizes what a tibble is and how it works in R code. If you want a quick overview of the essentials, this is the place to go.
- The [Tidy chapter](https://rstudio-education.github.io/tidyverse-cookbook/tidy.html#) in "A Tidyverse Cookbook" is a great resource if you want to learn more about how to work with tibbles using R code. The chapter explores a variety of R functions that can help you create and transform tibbles to organize and tidy your data.

---

# Data-import basics

*You can save this reading for future reference. Feel free to download a PDF version of this reading below:*

[Data-import-basics.pdf](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/Data-import-basics.pdf)

## **The data() function**

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XbxlyImrQgu8ZciJq0ILuA_c3ff7fa1744d497e9267078d16058e2c_Screen-Shot-2021-02-11-at-1.41.31-PM.png?expiry=1717113600000&hmac=QDIVXR0ILEi52n_tl26acxoGRyKKtUp-UxMogGJ7Nr0)

The default installation of R comes with a number of preloaded datasets that you can practice with. This is a great way to develop your R skills and learn about some important data analysis functions. Plus, many online resources and tutorials use these sample datasets to teach coding concepts in R.

You can use the **data()** function to load these datasets in R. If you run the data function without an argument, R will display a list of the available datasets.

**data()**

This includes the list of preloaded datasets from the *datasets* package.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/PhGaBTlcTqORmgU5XP6jSg_ebb5d20662444ab2bca76352ee5a256e_Screen-Shot-2021-01-22-at-11.39.53-AM.png?expiry=1717113600000&hmac=z2q1Fs0DedY0oXI-OVkwHgThjGPFULX2S0u_4LnFU3I)

If you want to load a specific dataset, just enter its name in the parentheses of the data() function. For example, let’s load the *mtcars* dataset, which has information about cars that have been featured in past issues of *Motor Trend* magazine.

**data(mtcars)**

When you run the function, R will load the dataset. The dataset will also appear in the Environment pane of your RStudio. The Environment pane displays the names of the data objects, such as data frames and variables, that you have in your current workspace. In this image, *mtcars* appears in the fifth row of the pane. R tells us that it contains 32 observations and 11 variables.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/7R_zhy6aSKKf84cumgiiOQ_6fbbeda64ee1472691965bc9bb309cee_Screen-Shot-2021-01-22-at-12.27.39-PM.png?expiry=1717113600000&hmac=HE6q9VTGfSZ2mfsiP5nh4iCW22jCrETfkcABIGle05Y)

Now that the dataset is loaded, you can get a preview of it in the R console pane. Just type its name...

**mtcars**

...and then press ctrl (or cmnd) and enter.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yh5xum5tSnKecbpubbpyxg_d7e1505d50fd4d73aa0ef186cd2d56d5_Screen-Shot-2021-03-15-at-3.36.50-PM.png?expiry=1717113600000&hmac=n-BEJwUPPQIFtmalBo9fTWfC-7JYhZdbu5q4D7mFwkM)

You can also display the dataset by clicking directly on the name of the dataset in the Environment pane. So, if you click on **mtcars** in the Environment pane, R automatically runs the View() function and displays the dataset in the RStudio data viewer.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/32SAqnVYSw-kgKp1WJsPeg_a22883468a134223b74b1f39c5f61655_Screen-Shot-2021-01-22-at-12.10.49-PM.png?expiry=1717113600000&hmac=-cLjg91IJnO2Zfga9V2ojc8jhVewCNRkJkIbMJaFJv0)

Try experimenting with other datasets in the list if you want some more practice.

## **The readr package**

In addition to using R’s built-in datasets, it is also helpful to import data from other sources to use for practice or analysis. The readr package in R is a great tool for reading rectangular data. Rectangular data is data that fits nicely inside a rectangle of rows and columns, with each column referring to a single variable and each row referring to a single observation.

Here are some examples of file types that store rectangular data:

- **.csv** **(comma separated values)**: a .csv file is a plain text file that contains a list of data. They mostly use commas to separate (or delimit) data, but sometimes they use other characters, like semicolons.
- **.tsv (tab separated values)**: a .tsv file stores a data table in which the columns of data are separated by tabs. For example, a database table or spreadsheet data.
- **.fwf** **(fixed width files)**: a .fwf file has a specific format that allows for the saving of textual data in an organized fashion.
- **.log:** a .log file is a computer-generated file that records events from operating systems and other software programs.

Base R also has functions for reading files, but the equivalent functions in readr are typically *much* faster. They also produce tibbles, which are easy to use and read.

The readr package is part of the core tidyverse. So, if you’ve already installed the tidyverse, you have what you need to start working with readr. If not, you can install the tidyverse now.

### **readr functions**

The goal of readr is to provide a fast and friendly way to read rectangular data. readr supports several read_ functions. Each function refers to a specific file format.

- **read_csv()**: comma-separated values (.csv) files
- **read_tsv()**: tab-separated values files
- **read_delim()**: general delimited files
- **read_fwf()**: fixed-width files
- **read_table()**: tabular files where columns are separated by white-space
- **read_log()**: web log files

These functions all have similar syntax, so once you learn how to use one of them, you can apply your knowledge to the others. This reading will focus on the read_csv() function, since .csv files are one of the most common forms of data storage and you will work with them frequently.

In most cases, these functions will work automatically: you supply the path to a file, run the function, and you get a tibble that displays the data in the file. Behind the scenes, readr parses the overall file and specifies how each column should be converted from a character vector to the most appropriate data type.

### **Reading a .csv file with readr**

The readr package comes with some sample files from built-in datasets that you can use for example code. To list the sample files, you can run the readr_example() function with no arguments.

**readr_example()**

**[1] "challenge.csv"     "epa78.txt"         "example.log"**

**[4] "fwf-sample.txt"    "massey-rating.txt" "mtcars.csv"**

**[7] "mtcars.csv.bz2"    "mtcars.csv.zip"**

The **“mtcars.csv”** file refers to the *mtcars* dataset that was mentioned earlier. Let’s use the **read_csv()** function to read the **“mtcars.csv”** file, as an example. In the parentheses, you need to supply the path to the file. In this case, it’s **“readr_example(“mtcars.csv”)**.

**read_csv(readr_example("mtcars.csv"))**

When you run the function, R prints out a column specification that gives the name and type of each column.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CMuq5sbuRZmLqubG7nWZ_g_44b244d4cac447e191fc0d59b94d205d_Screen-Shot-2021-03-15-at-3.42.43-PM.png?expiry=1717113600000&hmac=vmJZep0egT8r5E55E1IlbZ4-FrynGUjlBTRyubknvJs)

R also prints a tibble.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/PgvbBFMSRGCL2wRTEtRgsA_1d5362c17f2249dab6a936e09520d84a_Screen-Shot-2021-03-15-at-3.38.20-PM.png?expiry=1717113600000&hmac=3xpBt6ZUqZeCYiaLgX3ZhrG9a2Wx0KS47zWjn36CSwU)

- -----------------------------------------------------------------------------------------------------

## Optional: the readxl package

To import spreadsheet data into R, you can use the readxl package. The readxl package makes it easy to transfer data from Excel into R. Readxl supports both the legacy .xls file format and the modern xml-based .xlsx file format.

The readxl package is part of the tidyverse but is not a *core* tidyverse package, so you need to load readxl in R by using the library() function.

**library(readxl)**

### **Reading an .xlsx file with readxl**

Like the readr package, readxl comes with some sample files from built-in datasets that you can use for practice. You can run the code **readxl_example()** to see the list.

You can use the **read_excel()** function to read a spreadsheet file just like you used read_csv() function to read a  .csv file. The code for reading the example file **“type-me.xlsx”** includes the path to the file in the parentheses of the function.

**read_excel(readxl_example("type-me.xlsx"))**

You can use the [excel_sheets()](https://readxl.tidyverse.org/reference/excel_sheets.html) function to list the names of the individual sheets.

**excel_sheets(readxl_example("type-me.xlsx"))**

**[1] "logical_coercion" "numeric_coercion" "date_coercion" "text_coercion"**

You can also specify a sheet by name or number.  Just type **“sheet =”** followed by the name or number of the sheet. For example, you can use the sheet named **“numeric_coercion”** from the list above.

**read_excel(readxl_example("type-me.xlsx"), sheet = "numeric_coercion")**

When you run the function, R returns a tibble of the sheet.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zqCV7mPlQl-gle5j5ZJfEg_ecec2bacbde34a2caa93c8518c8f95a4_Screen-Shot-2021-03-15-at-3.40.40-PM.png?expiry=1717113600000&hmac=xybabizg6eVXxMjfsEgGBuSgkWAuP2eyDteXXGhqKns)

## Additional resources

- If you want to learn how to use readr functions to work with more complex files, check out the [Data Import chapter](https://r4ds.had.co.nz/data-import.html) of the R for Data Science book. It explores some of the common issues you might encounter when reading files, and how to use readr to manage those issues.
- The [readxl](https://readxl.tidyverse.org/) entry in the tidyverse documentation gives a good overview of the basic functions in readxl, provides a detailed explanation of how the package operates and the coding concepts behind them, and offers links to other useful resources.
- The R "datasets" package contains lots of useful preloaded datasets. Check out [The R Datasets Package](https://stat.ethz.ch/R-manual/R-devel/library/datasets/html/00Index.html) for a list. The list includes links to detailed descriptions of each dataset.

---

# Hands On Activity: Importing and working with data

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

By now, you have some experience manually entering data in R to create a data frame. In this activity you will import data from outside of R using the read_csv() function, then use R functions to manipulate and interact with that data.

Upon completing this activity, you will be able to import data into RStudio so you can analyze it. This will enable you to bring your own .csv files into RStudio and use this environment for personal projects, which will help you hone your data skills. As a data analyst, it will also be common for you to import data from external files into your R console and use it to create a data frame to analyze it.

## Work in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed,  navigate to the file explorer in the bottom right and click on the following: **Course 7 -> Week 3 -> Lesson2_Import.Rmd**.

The .csv file you will need, hotel_bookings.csv, is also located in this folder.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

[Lesson2_Import.txt](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/v3GhTu_5T1-xoU7v-S9fHg_2c69e32ffb9043eeb9ea5e423f6b7df1_Lesson2_Import.txt)

[hotel_bookings.csv](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings.csv)

You can also find the Rmd file with the solutions for this activity here:

[Lesson2_Import_Solutions.txt](Explore%20data%20and%20R%20d2c6633cedb947449cb2617b979a7352/J4rABg9TS26KwAYPU9tuXw_42aef80f650f4742b64835dc871ac4f1_Lesson2_Import_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.

If you have trouble completing the exercise or don't know how to proceed, navigate to Course 7 -> Week 3 -> Solutions -> Lesson2_Import_Solutions.Rmd in the exercise files.

---