# Cleaning data

---

# Cleaning up with the basics

[index (71).mp4](Cleaning%20data%20726999571afb4923bb88b9dde00ab222/index_(71).mp4)

**Key Points:**

- **Packages:**
    - **Here:** Simplifies file referencing.
    - **Skimr:** Makes data summarization easier.
    - **Janitor:** Provides functions for data cleaning.
    - **dplyr:** Used for data manipulation.
- **Data Cleaning Functions:**
    - **skim_without_charts():** Provides a comprehensive summary of a dataset.
    - **glimpse():** Shows a quick overview of the data.
    - **head():** Displays the first few rows of a dataset.
    - **select():** Selects specific columns or excludes unwanted ones.
- **Data Manipulation Functions:**
    - **rename():** Changes column names.
    - **rename_with():** Applies a function to change column names (e.g., uppercase, lowercase).
    - **clean_names():** Ensures column names are unique and consistent.

**Definitions:**

- **Data frame:** A two-dimensional data structure with rows and columns.
- **Column:** A vertical section of a data frame containing data of a specific variable.
- **Data cleaning:** The process of identifying and correcting errors or inconsistencies in data.
- **Data manipulation:** The process of transforming or modifying data to meet specific needs.

**Additional Notes:**

- The video demonstrates how to install and load the necessary packages.
- The palmer penguins dataset is used as an example for practicing data cleaning and manipulation functions.
- The video encourages learners to practice these functions on their own with the provided dataset.

---

# File-naming conventions

An important part of cleaning data is making sure that all of your files are accurately named. Although individual preferences will vary a bit, most analysts generally agree that file names should be accurate, consistent, and easy to read. This reading provides some general guidelines for you to follow when naming or renaming your data files.

## What’s in a (file)name?

When you first start working with R (or any other programming language, analysis tool, or platform, for that matter), you or your company should establish naming conventions for your files. This helps ensure that anyone reviewing your analysis–yourself included–can quickly and easily find what they need. Next are some helpful “do’s” and “don’ts” to keep in mind when naming your files.

### **Do**

- Keep your filenames to a reasonable length
- Use underscores and hyphens for readability
- Start or end your filename with a letter or number
- Use a standard date format when applicable; example: YYYY-MM-DD
- Use filenames for related files that work well with default ordering; example: in chronological order, or logical order using numbers first

Examples of good filenames

---

2020-04-10_march-attendance.R

---

2021_03_20_new_customer_ids.csv

---

01_data-sales.html

---

02_data-sales.html

---

### **Don't**

- Use unnecessary additional characters in filenames
- Use spaces or “illegal” characters; examples: &, %, #, <, or >
- Start or end your filename with a symbol
- Use incomplete or inconsistent date formats; example: M-D-YY
- Use filenames for related files that do not work well with default ordering; examples: a random system of numbers or date formats, or using letters first

Examples of filenames to avoid

---

4102020marchattendance<workinprogress>.R

---

_20210320*newcustomeridsforfebonly.csv

---

firstfile_for_datasales/1-25-2020.html

---

secondfile_for_datasales/2-5-2020.html

---

## Additional resources

These resources include more info about some of the file naming standards discussed here, and provide additional insights into best practices.

- [**How to name files**](https://speakerdeck.com/jennybc/how-to-name-files): this resource from Speaker Deck is a playful take on file naming. It includes several slides with tips and examples for how to accurately name lots of different types of files. You will learn why filenames should be both machine readable and human readable.
- [**File naming and structure**](https://www.tikar.or.id/?q=node/205): this resource from the Princeton University Library provides an easy-to-scan list of best practices, considerations, and examples for developing file naming conventions.

---

# More on R operators

You might remember that an **operator** is a symbol that identifies the type of operation or calculation to be performed in a formula. In an earlier video, you learned how to use the assignment and arithmetic operators to assign variables and perform calculations. In this reading, you will review a detailed summary of the main types of operators in R, and learn how to use specific operators in R code.

## Operators

In R, there are four main types of operators:

1. Arithmetic
2. Relational
3. Logical
4. Assignment

Review the specific operators in each category and check out some examples of how to use them in R code.

### **Arithmetic operators**

**Arithmetic operators** let you perform basic math operations like addition, subtraction, multiplication, and division.

The table below summarizes the different arithmetic operators in R. The examples used in the table are based on the creation of two variables: : *x* equals 2 and *y* equals 5. Note that you use the assignment operator to store these values:

**x <- 2**

**y <- 5**

| **Operator** | **Description** | **Example Code** | **Result/ Output** |
| --- | --- | --- | --- |
| + | Addition | x + y | [1] 7 |
| - | Subtraction | x - y | [1] -3 |
| * | Multiplication | x * y | [1] 10 |
| / | Division | x / y | [1] 0.4 |
| %% | Modulus (returns the remainder after division) | y %% x | [1] 1 |
| %/% | Integer division (returns an integer value after division) | y%/% x | [1] 2 |
| ^ | Exponent | y ^ x | [1]25 |

**Relational operators**

**Relational operators,** also known as comparators, allow you to compare values. Relational operators identify how one R object relates to another—like whether an object is less than, equal to, or greater than another object. The output for relational operators is either TRUE or FALSE (which is a logical data type, or boolean).

The table below summarizes the six relational operators in R. The examples used in the table are based on the creation of two variables: *x* equals 2 and *y* equals 5. Note that you use the assignment operator to store these values.

**x <- 2**

**y <- 5**

If you perform calculations with each operator, you get the following results. In this case, the output is boolean: TRUE or FALSE. Note that the [1] that appears before each output is used to represent how output is displayed in RStudio.

| **Operator** | **Description** | **Example Code** | **Result/Output** |
| --- | --- | --- | --- |
| < | Less than | x < y | [1] TRUE |
| > | Greater than | x > y | [1] FALSE |
| <= | Less than or equal to | x < = 2 | [1] TRUE |
| >= | Greater than or equal to | y >= 10 | [1] FALSE |
| == | Equal to | y == 5 | [1] TRUE |
| != | Not equal to | x != 2 | [1] FALSE |

**Logical operators**

**Logical operators** allow you to combine logical values. Logical operators return a logical data type or boolean (TRUE or FALSE)**.** You encountered logical operators in an earlier reading, [Logical operators and conditional statements](https://www.coursera.org/learn/data-analysis-r/supplement/I39VT/logical-operators-and-conditional-statements), but here is a quick refresher.

The table below summarizes the logical operators in R.

| **Operator** | **Description** |
| --- | --- |
| & | Element-wise logical AND |
| && | Logical AND |
| | | Element-wise logical OR |
| || | Logical OR |
| ! | Logical NOT |

Next, check out some examples of how logical operators work in R code.

**Element-wise logical AND (&) and OR (|)**

You can illustrate logical AND (&) and OR (|) by comparing numerical values. Create a variable *x* that is equal to 10.

**x <- 10**

The AND operator returns TRUE only if *both* individual values are TRUE.

**x > 2 & x < 12**

[1] TRUE

10 is greater than 2 *and* 10 is less than 12. So, the operation evaluates to **TRUE**.

The OR operator (|) works in a similar way to the AND operator (&). The main difference is that just *one* of the values of the OR operation needs to be TRUE for the entire OR operation to evaluate to TRUE. Only if *both* values are FALSE will the entire OR operation evaluate to **FALSE**.

Now try an example with the same variable **(x <- 10)**:

**x > 2 | x < 8**

**[1] TRUE**

10 is greater than 2, but 10 is not less than 8. But since at least one of the values (10>2) is TRUE, the OR operation evaluates to **TRUE**.

**Logical NOT (!)**

The NOT operator simply negates the logical value, and evaluates to its opposite. In R, zero is considered FALSE and all non-zero numbers are considered TRUE.

For example, apply the NOT operator to your variable **(x <- 10)**:

**!(x < 15)**

**[1] FALSE**

The NOT operation evaluates to **FALSE** because it takes the opposite logical value of the statement **x < 15**, which is TRUE (10 is less than 15).

### **Assignment operators**

**Assignment operators** let you assign values to variables.

In many scripting programming languages you can just use the equal sign (=) to assign a variable. For R, the best practice is to use the arrow assignment (<-). Technically, the single arrow assignment can be used in the left or right direction. But the rightward assignment is not generally used in R code.

You can also use the double arrow assignment, known as a scoping assignment. But the scoping assignment is for advanced R users, so you won’t learn about it in this reading.

The table below summarizes the assignment operators and example code in R. Notice that the output for each variable is its assigned value.

| **Operator** | **Description** | **Example Code (after the sample code below, typing x will generate the output in the next column)** | **Result/ Output** |
| --- | --- | --- | --- |
| <- | Leftwards assignment | x <- 2 | [1] 2 |
| <<- | Leftwards assignment | x <<- 7 | [1] 7 |
| = | Leftwards assignment | x = 9 | [1] 9 |
| -> | Rightwards assignment | 11 -> x | [1] 11 |
| ->> | Rightwards assignment | 21 ->> x | [1] 21 |

The operators you learned about in this reading are a great foundation for using operators in R.

## Additional resource

Check out the article about [R Operators](https://r-coder.com/operators-r/#Assignment_operators_in_R) on the R Coder website for a comprehensive guide to the different types of operators in R. The article includes lots of useful coding examples, and information about miscellaneous operators, the infix operator, and the pipe operator.

---

# Organize your data

[index (72).mp4](Cleaning%20data%20726999571afb4923bb88b9dde00ab222/index_(72).mp4)

**Key Points:**

- **Organizing data is crucial for turning information into knowledge.**
- R provides functions like `arrange`, `group_by`, and `filter` to organize and filter data.
- These functions help us find new insights and make our data useful.

**Definitions:**

- **`arrange`:** Sorts data by a specified variable in ascending or descending order.
- **`group_by`:** Groups data by a specified variable for further analysis.
- **`filter`:** Selects specific rows from a data frame based on a condition.

**Key Points and Examples:**

- **`arrange`:**
    - Sorts data by bill length in ascending order: `penguins %>% arrange(bill_length_mm)`
    - Sorts data by bill length in descending order: `penguins %>% arrange(desc(bill_length_mm))`
- **`group_by`:**
    - Groups data by island and calculates mean bill length: `penguins %>% group_by(island) %>% summarize(mean_bill_length_mm = mean(bill_length_mm))`
    - Groups data by island and species, calculates mean and max bill length: `penguins %>% group_by(island, species) %>% summarize(mean_bill_length_mm = mean(bill_length_mm), max_bill_length_mm = max(bill_length_mm))`
- **`filter`:**
    - Selects data on Adelie penguins: `penguins %>% filter(species == "Adelie")`

**Additional Notes:**

- The video emphasizes the importance of data organization and cleaning for effective analysis.
- R provides powerful tools for data manipulation, making it a valuable tool for data analysts.
- The video introduces the concept of piping, which allows chaining multiple functions together for efficient data manipulation.

---

# Hands On Activity: Cleaning data in R

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

So far, you’ve learned a lot about the importance of cleaning data and how to do it in spreadsheets and SQL. In this activity, you’ll follow a scenario and clean real data in R.

By the time you complete this activity, you will learn more about data cleaning functions in R and apply this know-how to import, preview, and perform calculations on different data sets. You can use these techniques to gain initial insights into your data, which will help you analyze data throughout your career.

## Working in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed,  navigate to the file explorer in the bottom right and click on the following: **Course 7 -> Week 3 -> Lesson3_Clean.Rmd**.

The .csv file, hotel_bookings.csv, is also located in this folder.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

[Lesson3_Clean.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/cc4C4lPXSj-OAuJT10o_nA_65a4b2b0f4964a6fa1bbd680e2489ef1_Lesson3_Clean.txt)

[hotel_bookings (1).csv](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings_(1).csv)

You can also find the Rmd file with the solutions for this activity here:

[Lesson3_Clean_Solutions.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/tgiRg5UPSrOIkYOVD5qzjQ_52c64d0b9565407fbb92d0836cbc21f1_Lesson3_Clean_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.

---

# Transforming data

[index (73).mp4](Cleaning%20data%20726999571afb4923bb88b9dde00ab222/index_(73).mp4)

**Key Points:**

- **Transforming data:** Sometimes you need to manipulate your data to make it more usable for analysis. This can involve splitting columns, combining columns, or adding new columns.
- **Separate function:** This function splits a column into multiple columns based on a delimiter. In the video, the `separate` function was used to split the `name` column into `first_name` and `last_name` columns based on the space delimiter.
- **Unite function:** This function combines multiple columns into a single column. In the video, the `unite` function was used to combine the `first_name` and `last_name` columns into a single `name` column.
- **Mutate function:** This function adds new columns to a data frame based on calculations or transformations. In the video, the `mutate` function was used to add two new columns: `body_mass_kg` (converted from grams to kilograms) and `flipper_length_cm` (converted from millimeters to centimeters).

**Definitions:**

- **Delimiter:** A character that separates values in a string. In the video, the space character was used as the delimiter to split the `name` column.
- **Data frame:** A two-dimensional data structure with rows and columns. Each column represents a variable, and each row represents an observation.
- **Variable:** A characteristic or attribute of an observation. In the video, the `name`, `first_name`, `last_name`, `body_mass`, `body_mass_kg`, `flipper_length`, and `flipper_length_cm` are all variables.
- **Observation:** A single instance of data in a data frame. In the video, each row represents an employee observation.

**Additional Notes:**

- The video also mentioned the `tribble` function, which is used to create data frames by manually entering data.
- The video emphasized the importance of using the `mutate` function to add new variables based on calculations, as this can be a powerful tool for data analysis.

---

# Wide to long with tidyr

When organizing or tidying your data using R, you might need to convert wide data to long data or long to wide. Recall that this is what data looks like in a wide format spreadsheet:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/m9JdRN6aTQCSXUTemq0AVA_4909c4cc120d496c99895460c2ca27f4_Screenshot-2021-01-27-at-2.26.11-PM.png?expiry=1717113600000&hmac=y9MRDjMjjFi0Ytz0H-nsPKQZ-zlsjbngR4k7Cyckixs)

**Wide data** has observations across several columns. Each column contains data from a different condition of the variable. In this example the columns are different years.

Now check out the same data in a long format:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AKr0lJTgSaCq9JSU4CmgtA_7608bba87aa04ab4b1695c3b3a22325a_Screenshot-2021-01-27-at-2.29.39-PM.png?expiry=1717113600000&hmac=n9sotcjtoX79fGyimpconNtyg_ienLcUguvYDEJfBSw)

To review what you already learned about the difference, **long data** has all the observations in a single column, and the variable conditions are placed into separate rows.

## The pivot_longer and pivot_wider functions

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/v4UKiGjHQtqFCohox5LaVw_2b7b38924ef349e184ea326b58cba225_Screen-Shot-2021-03-02-at-9.35.23-AM.png?expiry=1717113600000&hmac=pbN8XCoMBWOiot97sm4WUM8uMScvmxl0CM2iDurVvpE)

There are compelling reasons to use both formats. But as an analyst, it is important to know how to tidy data when you need to. In R, you may have a data frame in a wide format that has several variables and conditions for each variable. It might feel a bit messy.

That’s where pivot_longer()comes in. As part of the tidyr package, you can use this R function to lengthen the data in a data frame by increasing the number of rows and decreasing the number of columns. Similarly, if you want to convert your data to have more columns and fewer rows, you would use the pivot_wider() function.

## Additional resources

To learn more about these two functions and how to apply them in your R programming, check out these resources:

- [**Pivoting**](https://tidyr.tidyverse.org/articles/pivot.html): Consider this a starting point for tidying data through wide and long conversions. This web page is taken directly from tidyr package information at [**tidyverse.org**](https://www.tidyverse.org/). It explores the components of the pivot_longer and pivot_wider functions using specific details, examples, and definitions.
- [**CleanItUp 5: R-Ladies Sydney: Wide to Long to Wide to…PIVOT**](https://rladiessydney.org/courses/ryouwithme/02-cleanitup-5/): This resource gives you additional details about the pivot_longer and pivot_wider functions. The examples provided use interesting datasets to illustrate how to convert data from wide to long and back to wide.
- [**Plotting multiple variables](https://scc.ms.unimelb.edu.au/resources-list/simple-r-scripts-for-analysis/r-scripts)[:](https://www.datamentor.io/r-programming/saving-plot/)** This resource explains how to visualize wide and long data, with ggplot2 to help tidy it. The focus is on using pivot_longer to restructure data and make similar plots of a number of variables at once. You can apply what you learn from the other resources here for a broader understanding of the pivot functions.

---