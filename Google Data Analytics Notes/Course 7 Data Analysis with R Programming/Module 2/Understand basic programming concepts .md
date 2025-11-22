# Understand basic programming concepts

---

# Programming using RStudio

[index (62).mp4](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/index_(62).mp4)

**Introduction:**

- The video welcomes you back to the course and introduces the topic of programming and coding using RStudio.
- The instructor emphasizes the importance of learning new skills and shares their personal experience with learning R.

**Fundamentals of Programming in RStudio:**

- RStudio is compared to a car's engine, while RStudio is likened to the accelerator, steering wheel, and dashboard.
- The video highlights the importance of understanding programming fundamentals for working effectively with RStudio.
- These fundamentals are compared and contrasted with other analysis platforms like spreadsheets and SQL.

**Coding in RStudio:**

- The video discusses the syntax for performing calculations in R.
- It introduces standards and naming conventions for code.
- The concept of "pipes" in R is explained as a way to make code sequences easier to work with and read.

**R Packages:**

- R packages are described as reusable functions and tools created by the R community for users.
- The Tidyverse collection of packages is introduced, including ggplot2 for visualization.
- Learners are guided on how to install and use the Tidyverse in RStudio.

**Key Points:**

- Programming fundamentals are essential for working effectively with RStudio.
- R packages offer reusable functions and tools created by the R community.
- The Tidyverse collection of packages is valuable for data analysis and visualization.
- Learners will be using RStudio Cloud for the program.

**Definitions:**

- **RStudio:** An integrated development environment (IDE) for R programming.
- **Syntax:** The rules and structure of a programming language.
- **Pipes:** A way to connect multiple functions in R, making code more readable and efficient.
- **R Packages:** Collections of reusable functions and tools created by the R community.
- **Tidyverse:** A collection of R packages for data analysis and visualization.
- **RStudio Cloud:** A web-based version of RStudio.

**Additional Notes:**

- The video emphasizes the importance of being open to learning new skills.
- It encourages learners to reach out to more experienced R users for help.
- The video provides a clear overview of the topics that will be covered in the next part of the program.

---

# Programming fundamentals

[index (63).mp4](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/index_(63).mp4)

**Key Points:**

- **Fundamentals of R:**
    - Functions: Reusable code blocks for specific tasks.
    - Comments: Explanatory notes within code.
    - Variables: Named values for storing data.
    - Data Types: Different categories of data (e.g., numeric, character).
    - Vectors: Ordered collections of data elements.
    - Pipes: Operators for chaining multiple functions.
- **Function Example:**
    - `print("Coding in R")` displays the text "Coding in R".
- **Variable Example:**
    - `first_variable <- "This is my variable."` assigns the text "This is my variable." to the variable `first_variable`.
- **Vector Example:**
    - `vec_1 <- c(1, 2, 3, 4, 5)` creates a vector named `vec_1` containing the numbers 1 to 5.
- **Pipe Example:**
    - `data %>% filter(condition) %>% sort(variable)` filters data based on a condition and then sorts it by a variable.

**Definitions:**

- **Function:** A named block of code that performs a specific task.
- **Comment:** A line of text within code that is ignored by the interpreter but provides explanation for humans.
- **Variable:** A named container that stores a value.
- **Data Type:** A classification of data (e.g., numeric, character, logical).
- **Vector:** An ordered collection of data elements of the same type.
- **Pipe:** An operator in R that allows chaining multiple functions together.

---

# Vectors and lists in R

*You can save this reading for future reference. Feel free to download a PDF version of this reading below:*

In programming, a **data structure** is a format for organizing and storing data. Data structures are important to understand because you will work with them frequently when you use R for data analysis. The most common data structures in the R programming language include:

- Vectors
- Data frames
- Matrices
- Arrays

Think of a data structure like a house that contains your data.

This reading will focus on vectors. Later on, you’ll learn more about data frames, matrices, and arrays.

There are two types of vectors: **atomic vectors** and **lists**. Coming up, you’ll learn about the basic properties of atomic vectors and lists, and how to use R code to create them.

## Atomic vectors

First, we will go through the different types of atomic vectors. Then, you will learn how to use R code to create, identify, and name the vectors.

Earlier, you learned that a **vector** is a group of data elements of the *same* type, stored in a sequence in R. You cannot have a vector that contains both logicals and numerics.

There are six primary types of atomic vectors: logical, integer, double, character (which contains strings), complex, and raw. The last two–complex and raw–aren’t as common in data analysis, so we will focus on the first four. Together, integer and double vectors are known as numeric vectors because they both contain numbers. This table summarizes the four primary types:

| **Type** | **Description** | **Example** |
| --- | --- | --- |
| Logical | True/False | **TRUE** |
| Integer | Positive and negative whole values | **3** |
| Double | Decimal values | **101.175** |
| Character | String/character values | **“Coding”** |

This diagram illustrates the hierarchy of relationships among these four main types of vectors:

Bottom: logical (arrow points to atomic), integer (arrow points to numeric), double (arrow points to numeric), character (arrow points to atomic)
Second to bottom: numeric (arrow points to atomic)
second level: atomic (arrow points to vector)
top: vector

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UplCKfO6Qo6ZQinzunKOew_19acadeec69a4cfaa8197b18525a4c44_Screen-Shot-2021-03-02-at-2.02.18-PM.png?expiry=1717113600000&hmac=-p4ymcNA8Fjj82LjIL2RVtF4UtsG6So15fFqHm6FCNg)

### **Creating vectors**

One way to create a vector is by using the **c()** function (called the “combine” function). The c() function in R combines multiple values into a vector. In R, this function is just the letter “c” followed by the values you want in your vector inside the parentheses, separated by a comma: c(x, y, z, …).

For example, you can use the c() function to store numeric data in a vector.

**c(2.5, 48.5, 101.5)**

To create a vector of integers using the c() function, you must place the letter "L" directly after each number.

**c(1L, 5L, 15L)**

You can also create a vector containing characters or logicals.

**c(“Sara” , “Lisa” , “Anna”)**

**c(TRUE, FALSE, TRUE)**

### **Determining the properties of vectors**

Every vector you create will have two key properties: type and length.

You can determine what type of vector you are working with by using the **typeof()** function. Place the code for the vector inside the parentheses of the function. When you run the function, R will tell you the type. For example:

**typeof(c(“a” , “b”))**

**#> [1] "character"**

Notice that the output of the typeof function in this example is **“character”**. Similarly, if you use the typeof function on a vector with integer values, then the output will include **“integer”** instead:

**typeof(c(1L , 3L))**

**#> [1] "integer"**

You can determine the length of an existing vector–meaning the number of elements it contains–by using the **length()** function. In this example, we use an assignment operator to assign the vector to the variable *x*. Then, we apply the length() function to the variable. When we run the function, R tells us the length is **3**.

**x <- c(33.5, 57.75, 120.05)**

**length(x)**

**#> [1] 3**

You can also check if a vector is a specific type by using an **is** function: **is.logical(), is.double(), is.integer(), is.character()**. In this example, R returns a value of **TRUE** because the vector contains integers.

**x <- c(2L, 5L, 11L)**

**is.integer(x)**

**#> [1] TRUE**

In this example, R returns a value of **FALSE** because the vector does *not* contain characters, rather it contains logicals.

**y <- c(TRUE, TRUE, FALSE)**

**is.character(y)**

**#> [1] FALSE**

### **Naming vectors**

All types of vectors can be named. Names are useful for writing readable code and describing objects in R. You can name the elements of a vector with the **names()** function. As an example, let’s assign the variable x to a new vector with three elements.

**x <- c(1, 3, 5)**

You can use the names() function to assign a different name to each element of the vector.

**names(x) <- c("a", "b", "c")**

Now, when you run the code, R shows that the first element of the vector is named **a**, the second **b**, and the third **c**.

**x**

**#> a b c**

**#> 1 3 5**

Remember that an atomic vector can only contain elements of the same type. If you want to store elements of different types in the same data structure, you can use a list.

## Creating lists

**Lists** are different from atomic vectors because their elements can be of any type—like dates, data frames, vectors, matrices, and more. Lists can even contain other lists.

You can create a list with the **list()** function. Similar to the c() function, the list() function is just **list** followed by the values you want in your list inside parentheses: **list(x, y, z, …)**. In this example, we create a list that contains four different kinds of elements: character (**"a"**), integer (**1L**), double (**1.5**), and logical (**TRUE**).

**list("a", 1L, 1.5, TRUE)**

Like we already mentioned, lists can contain other lists. If you want, you can even store a list inside a list inside a list—and so on.

**list(list(list(1 , 3, 5)))**

### **Determining the structure of lists**

If you want to find out what types of elements a list contains, you can use the **str()** function. To do so, place the code for the list inside the parentheses of the function. When you run the function, R will display the data structure of the list by describing its elements and their types.

Let’s apply the str() function to our first example of a list.

**str(list("a", 1L, 1.5, TRUE))**

We run the function, then R tells us that the list contains four elements, and that the elements consist of four different types: character (**chr**), integer (**int**), number (**num**), and logical (**logi**).

**#> List of 4**

**#>  $ : chr "a"**

**#>  $ : int 1**

**#>  $ : num 1.5**

**#>  $ : logi TRUE**

Let’s use the str() function to discover the structure of our second example.  First, let’s assign the list to the variable *z* to make it easier to input in the str() function.

**z <- list(list(list(1 , 3, 5)))**

Let’s run the function.

**str(z)**

**#> List of 1**

**#>  $ :List of 1**

**#>   ..$ :List of 3**

**#>   .. ..$ : num 1**

**#>   .. ..$ : num 3**

**#>   .. ..$ : num 5**

The indentation of the **$** symbols reflect the nested structure of this list. Here, there are three levels (so there is a list within a list within a list).

### **Naming lists**

Lists, like vectors, can be named. You can name the elements of a list when you first create it with the list() function:

**list('Chicago' = 1, 'New York' = 2, 'Los Angeles' = 3)**

**$`Chicago`**

**[1] 1**

**$`New York`**

**[1] 2**

**$`Los Angeles`**

**[1] 3**

## Additional resource

To learn more about vectors and lists, check out [R for Data Science, Chapter 20: Vectors](https://r4ds.had.co.nz/vectors.html#vectors). R for Data Science is a classic resource for learning how to use R for data science and data analysis. It covers everything from cleaning to visualizing to communicating your data. If you want to get more details about the topic of vectors and lists, this chapter is a great place to start.

---

# Dates and times in R

In this reading, you will learn how to work with dates and times in R using the **lubridate** package. Coming up, you will use tools in the lubridate package to convert different types of data in R into date and date-time formats.

## Loading tidyverse and lubridate packages

Before you get started working with dates and times, you should load both **tidyverse** and **lubridate**. Lubridate is part of tidyverse.

First, open RStudio.

If you haven't already installed tidyverse, you can use the **install.packages()** function to do so:

- **install.packages("tidyverse")**

Next, load the tidyverse and lubridate packages using the **library()** function. First, load the core tidyverse to make it available in your current R session:

- **library(tidyverse)**

Then, load the lubridate package:

- **library(lubridate)**

Now you’re ready to be introduced to the tools in the lubridate package.

## Working with dates and times

This section covers the data types for dates and times in R and how to convert strings to date-time formats.

### **Types**

In R, there are three types of data that refer to an instant in time:

- A date **("2016-08-16")**
- A time within a day **(“20:11:59 UTC")**
- And a date-time. This is a date plus a time **("2018-03-31 18:15:48 UTC")**

The time is given in UTC, which stands for Universal Time Coordinated, more commonly called Universal Coordinated Time. This is the primary standard by which the world regulates clocks and time.

For example, to get the current date you can run the **today()** function. The date appears as year, month, and day.

**today()**

**#> [1] "2021-01-20"**

To get the current date-time you can run the **now()** function. Note that the time appears to the nearest second.

**now()**

**#> [1] "2021-01-20 16:25:05 UTC"**

When working with R, there are three ways you are likely to create date-time formats:

- From a string
- From an individual date
- From an existing date/time object

R creates dates in the standard yyyy-mm-dd format by default.

Let's go over each.

### **Converting from strings**

Date/time data often comes as strings. You can convert strings into dates and date-times using the tools provided by lubridate. These tools automatically work out the date/time format. First, identify the order in which the year, month, and day appear in your dates. Then, arrange the letters *y*, *m*, and *d* in the same order. That gives you the name of the lubridate function that will parse your date. For example, for the date *2021-01-20,* you use the order *ymd*:

**ymd("2021-01-20")**

When you run the function, R returns the date in yyyy-mm-dd format.

**#> [1] "2021-01-20"**

It works the same way for any order. For example, month, day, and year. R still returns the date in yyyy-mm-dd format.

**mdy("January 20th, 2021")**

**#> [1] "2021-01-20"**

Or, day, month, and year. R still returns the date in yyyy-mm-dd format.

**dmy("20-Jan-2021")**

**#> [1] "2021-01-20"**

These functions also take unquoted numbers and convert them into the yyyy-mm-dd format.

**ymd(20210120)**

**#> [1] "2021-01-20"**

### **Creating date-time components**

The ymd() function and its variations create dates. To create a date-time from a date*,* add an underscore and one or more of the letters *h*, *m*, and s (hours, minutes, seconds) to the name of the function:

**ymd_hms("2021-01-20 20:11:59")**

**#> [1] "2021-01-20 20:11:59 UTC"**

**mdy_hm("01/20/2021 08:01")**

**#> [1] "2021-01-20 08:01:00 UTC"**

### **Optional: Switching between existing date-time objects**

Finally, you might want to switch between a date-time and a date.

You can use the function **as_date()** to convert a date-time to a date. For example, put the current date-time—now()—in the parentheses of the function.

**as_date(now())**

**#> [1] "2021-01-20"**

## Additional resources

To learn more about working with dates and times in R, check out the following resources:

- [lubridate.tidyverse](https://lubridate.tidyverse.org/index.html): This is the “lubridate” entry from the official tidyverse documentation, which offers a comprehensive reference guide to the various tidyverse packages. Check out this link for an overview of key concepts and functions.
- [Dates and times with lubridate: Cheat Sheet](https://rawgit.com/rstudio/cheatsheets/master/lubridate.pdf): This “cheat sheet” gives you a detailed map of all the different things you can do with the lubridate package. You don’t need to know all of this information, but the cheat sheet is a useful reference for any questions you might have about working with dates and times in R.

---

# Other common data structures

In this reading, you’ll continue exploring data structures through an introduction to data frames and matrices. You will learn about the basic properties of each structure, and simple ways to create them with R code. You’ll also briefly examine **files**, which are often used to access and store data and related information. The files and matrices sections of this reading are optional.

## Data structures

Recall that a data structure is like a house that contains your data, helping you to bring data elements together in a structured way that enables you to draw conclusions.

### **Data frames**

Data frames are the most common way of storing and analyzing data in R, so it’s important to understand what they are and how to create them. A **data frame** is a collection of columns containing data, similar to a spreadsheet or SQL table. Each column has a name that represents a variable and includes one observation per row. Data frames summarize data and organize it into a format that is easy to read and use.

For example, the data frame below shows the **diamonds** dataset, which is one of the preloaded datasets in R. Each column contains a single variable that is related to diamonds: carat, cut, color, clarity, depth, and so on. Each row represents a single observation.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UMetQpA6SJ23h1AE6AoKhA_6ed0b70941554625807632943c03d0f1_Screenshot-2023-11-27-1.39.10-PM.png?expiry=1717113600000&hmac=3E1JZd0noavApAh2mj06CxfFOqRD0ylNvS5JkGMag90)

There are a few key things to keep in mind when working with data frames:

- Data frames can include many different types of data, including numeric, logical, or character.
- Data frames can have only one element in each cell.
- Each column should be named.
- Each column should consist of elements of the same data type.

You will learn more about data frames later on in the program, but this is a great starting point.

If you need to manually create a data frame in R, you can use the **data.frame()** function. The **data.frame()** function takes vectors as input. In the parentheses, enter the name of the column, followed by an equals sign, and then the vector you want to input for that column. In this example, the **x** column is a vector with elements 1, 2, 3, and the **y** column is a vector with elements 1.5, 5.5, 7.5. Run the following code to create the data frame.

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled.png)

When you run the code, R displays the data frame in ordered rows and columns.

Use the extract operator to extract a subset from a data frame. When you use this operator on a data frame, it takes two arguments: the row(s) and column(s) you’d like to extract, separated by a comma. As an example, name the data frame above z. Then, to extract the element from the second row and the first column, use the code **z[2,1]**, which returns a value of 2:

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%201.png)

You’ll learn more about data frames later on in the course, but this is enough to get you started!

## Optional: Files

When you’re doing data analysis, you won’t usually create a data frame yourself. Instead, you’ll import data from another source, such as  a .csv file, a relational database, or a software program. For this reason, it’s essential to be able to work with files in R. In this section, you’ll explore a few of the most useful functions for working with files, including commands to create, copy, and delete files in R.

### Create a file

Use the **file.create()** function to create a blank file. Place the name and the type of the file in the parentheses of the function. Your file types will usually be something like .txt, .docx, or .csv.

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%202.png)

If the file is successfully created when you run the function, R will return a value of **TRUE**. Otherwise, R will return a value of **FALSE**.

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%203.png)

### Copy a file

Copy a file with the **file.copy()** function. In the parentheses, add the name of the file to be copied. Then, enter a comma, and add the name of the destination folder that you want to copy the file to.

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%204.png)

If you check the **Files** tab in RStudio, a copy of the file appears in the relevant folder:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6AVUXMXZT56FVFzF2V-eLw_bd3aab8ba09942b6bf45a8ddb8b8e991_unnamed-6-.png?expiry=1717113600000&hmac=ZB7LeaaEOvic68LODsLRVmX-0XOx_aUDaf_pXSKYuEk)

You can delete R files with the **unlink()** function. Enter the file’s name in the parentheses of the function.

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%205.png)

You’ll learn techniques for importing files into R later in this course.

## Optional: Matrices

A **matrix** is a two-dimensional collection of data elements. This means it has both rows and columns. By contrast, a vector is a one-dimensional sequence of data elements. But like vectors, matrices can only contain a single data type. For example, you can’t have both logicals and numerics in a matrix.

To create a matrix in R, you can use the **matrix()** function. The **matrix()** function has two main arguments that you enter in the parentheses. First, add a vector. The vector contains the values you want to place in the matrix. Next, add at least one matrix dimension. You can choose to specify the number of rows or the number of columns by using the code **nrow =** or **ncol =**.

For example, to create a 2x3 (two rows by three columns) matrix containing the values 3-8, enter a vector containing that series of numbers: **c(3:8)**. Then, enter a comma. Finally, enter **nrow = 2** to specify the number of rows. Run the code:

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%206.png)

R displays a matrix with three columns and two rows (typically referred to as a “2x3”) that contain the numeric values 3, 4, 5, 6, 7, 8. R places the first value (3) of the vector in the uppermost row, and the leftmost column of the matrix, and continues the sequence from left to right.

You can also choose to specify the number of columns (**ncol =** ) instead of the number of rows (**nrow =** ). Run the code:

![Untitled](Understand%20basic%20programming%20concepts%205bfaff23dac943a0b0386092b86b5e1d/Untitled%207.png)

R infers the number of rows automatically.

Similar to data frames, you can extract an element from a matrix with the extract operator, **[]**.

## Key takeaways

As a data analyst, you’ll work with data frames often. Data frames in R are a collection of columns containing data, similar to a spreadsheet or SQL table. Data frames can contain data of different types, although each column must be of the same data type. By contrast, matrices are a collection of two-dimensional data elements that can only contain one data type. Usually, you’ll import data into R before you analyze it, so knowing how to use R to work with files is critical. You’ll learn techniques to import files later in this course, but you can also use R functions to create, copy, and delete files.

## Resources for more information

For more information on working with files in R, check out [R documentation: files](https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/files). It’s a useful reference guide for functions in R code.

---