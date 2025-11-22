# Explore data types, fields, and values - Part 1

---

# Know the type of data you’re working with

### **Data Types:**

- A data type defines the kind of value a data attribute holds.
- Different data types exist depending on the query language or software used.
- This video focuses on data types commonly used in spreadsheets: numbers, text/strings, and Booleans.

### **Number Data Type:**

- Represents numerical values used for calculations.
- Examples: search interest values in columns B, D, and F.
- Can be formatted as percentages or currency.

### **Text/String Data Type:**

- Represents sequences of characters and punctuation containing textual information.
- Examples: treat names in column H, phone numbers, street addresses (when treated as text).
- Numbers within text are not used for calculations.

### **Boolean Data Type:**

- Represents values with only two possibilities: true or false.
- Examples: values in columns C, E, and G indicating whether search interest exceeds 50.
- Can be used with formulas to evaluate conditions.

### **Key Points:**

- Understanding data types helps avoid errors when working with data.
- Choosing the correct data type ensures accurate calculations and analysis.
- Data types can be combined using formulas to create new information.

### **Additional Notes:**

- The video mentions the relationship between data types, fields, and values, which will be covered in future lessons.
- It emphasizes the importance of knowing your data types to minimize errors.

### **Real-Life Example:**

Imagine you're analyzing sales data for an online store. You might have columns for product names (text), prices (numbers), and purchase dates (dates). Understanding the data types allows you to calculate total revenue, analyze trends over time, and identify popular products.

---

# Use Boolean Logic

- In this reading, you will explore the basics of Boolean logic and learn how to use single and multiple conditions in a Boolean statement.
- These conditions are created with Boolean operators, including **AND**, **OR**, and **NOT**.
- These operators are similar to mathematical operators and can be used to create logical statements that filter your results.
- Data analysts use Boolean statements to do a wide range of data analysis tasks, such as writing queries for searches and checking for conditions when writing programming code.

## Boolean logic example

- Imagine you are shopping for shoes, and are considering certain preferences:
    - You will buy the shoes only if they are any combination of pink and grey
    - You will buy the shoes if they are entirely pink, entirely grey, or if they are pink and grey
    - You will buy the shoes if they are grey, but not if they have any pink
- These Venn diagrams illustrate your shoe preferences. **AND** is the center of the Venn diagram, where two conditions overlap. **OR** includes either condition. **NOT** includes only the part of the Venn diagram that doesn't contain the exception.
- The intersection of these circles is highlighted to indicate the AND condition requires shoes to be both grey and pink.The Venn diagram that represents OR includes a circle labeled grey shoes overlapping with a circle labeled pink shoes. The entirety of both circles is highlighted to indicate the OR condition means any shoe with grey, pink, or some combination satisfies the requirement. The Venn diagram that represents NOT includes a circle labeled grey shoes overlapping with a circle labeled pink shoes. The portion of the grey shoes circle that does not intersect with the pink shoes circle is highlighted to indicate the NOT condition requires shoes to not include pink.
    
    ![Untitled](Explore%20data%20types,%20fields,%20and%20values%20-%20Part%201%207b50f01833fc4b6681e70dba0c7fc8ae/Untitled.png)
    

## Use Boolean logic in statements

- In queries, Boolean logic is represented in a statement written with Boolean operators. An **operator** is a symbol that names the operation or calculation to be performed. Read on to discover how you can convert your shoe preferences into Boolean statements.

### **The AND operator**

- Your condition is “If the color of the shoe has any combination of grey and pink, you will buy them.” The Boolean statement would break down the logic of that statement to filter your results by both colors. It would say **IF (Color="Grey") AND (Color="Pink") then buy them**
    - The **AND** operator lets you stack both of your conditions.
- Below is a simple truth table that outlines the Boolean logic at work in this statement. In the **Color is Grey** column, there are two pairs of shoes that meet the color condition. And in the **Color is Pink** column, there are two pairs that meet that condition. But in the **If Grey AND Pink** column, only one pair of shoes meets both conditions. So, according to the Boolean logic of the statement, there is only one pair marked true. In other words, there is one pair of shoes that you would buy.
    
    
    | **Color is Grey** | **Color is Pink** | **If Grey AND Pink, then Buy** | **Boolean Logic** |
    | --- | --- | --- | --- |
    | Grey/True | Pink/True | True/Buy | True AND True = True |
    | Grey/True | Black/False | False/Don't buy | True AND False = False |
    | Red/False | Pink/True | False/Don't buy | False AND True = False |
    | Red/False | Green/False | False/Don't buy | False AND False = False |

### **The OR operator**

- The **OR** operator lets you move forward if either one of your two conditions is met. Your condition is “If the shoes are grey or pink, you will buy them.” The Boolean statement would be **IF (Color="Grey") OR (Color="Pink") then buy them**.
- Notice that any shoe that meets either the **Color is Grey** or the **Color is Pink** condition is marked as true by the Boolean logic. According to the truth table below, there are three pairs of shoes that you can buy.
    
    
    | **Color is Grey** | **Color is Pink** | **If Grey OR Pink, then Buy** | **Boolean Logic** |
    | --- | --- | --- | --- |
    | Red/False | Black/False | False/Don't buy | False OR False = False |
    | Black/False | Pink/True | True/Buy | False OR True = True |
    | Grey/True | Green/False | True/Buy | True OR False = True |
    | Grey/True | Pink/True | True/Buy | True OR True = True |

### **The NOT operator**

- Finally, the **NOT** operator lets you filter by subtracting specific conditions from the results. Your condition is "You will buy any grey shoe except for those with any traces of pink in them." Your Boolean statement would be **IF (Color="Grey") AND (Color=NOT "Pink") then buy them**
- Now, all of the grey shoes that aren't pink are marked true by the Boolean logic for the **NOT** Pink condition. The pink shoes are marked false by the Boolean logic for the **NOT** Pink condition. Only one pair of shoes is excluded in the truth table below.
    
    
    | **Color is Grey** | **Color is Pink** | **Boolean Logic for NOT Pink** | **If Grey AND (NOT Pink), then Buy** | **Boolean Logic** |
    | --- | --- | --- | --- | --- |
    | Grey/True | Red/False | Not False = True | True/Buy | True AND True = True |
    | Grey/True | Black/False | Not False = True | True/Buy | True AND True = True |
    | Grey/True | Green/False | Not False = True | True/Buy | True AND True = True |
    | Grey/True | Pink/True | Not True = False | False/Don't buy | True AND False = False |

## The power of multiple conditions

- For data analysts, the real power of Boolean logic comes from being able to combine multiple conditions in a single statement. For example, if you wanted to filter for shoes that were grey or pink, and waterproof, you could construct a Boolean statement such as: “**IF ((Color = "Grey") OR (Color = "Pink")) AND (Waterproof="True")**
- Notice that you can use parentheses to group your conditions together.

## Key takeaways

- Operators are symbols that name the operation or calculation to be performed. The operators **AND**, **OR**, and **NOT** can be used to write Boolean statements in programming languages. Whether you are doing a search for new shoes or applying this logic to queries, Boolean logic lets you create multiple conditions to filter your results. Now that you know a little more about Boolean logic, you can start using it!

---

# Data table components

## Data Types and Structures

### Key Points

- Data is everywhere, and it comes in many different forms.
- Data can be structured or unstructured.
- Structured data is organized in a way that makes it easy to search and analyze.
- Unstructured data is not organized in a way that makes it easy to search and analyze.
- Data types are the different ways that data can be represented.
- Common data types include numbers, strings, dates, and times.
- Data structures are the ways that data is organized.
- Common data structures include arrays, lists, and dictionaries.

### Definitions

- **Data:** Facts and statistics collected together for reference or analysis.
- **Structured data:** Data that is organized in a way that makes it easy to search and analyze.
- **Unstructured data:** Data that is not organized in a way that makes it easy to search and analyze.
- **Data type:** The way that data is represented.
- **Data structure:** The way that data is organized.

## Data Responsibility

### Key Points

- Data is a powerful tool that can be used for good or bad.
- It is important to use data responsibly.
- Data should be used in a way that is fair, accurate, and transparent.
- Data should not be used to discriminate against or harm others.

### Definitions

- **Data responsibility:** The ethical use of data.

## Database Essentials

### Key Points

- A database is a collection of data that is organized in a way that makes it easy to access, manage, and update.
- Databases are used to store and retrieve data.
- There are many different types of databases.
- The most common type of database is a relational database.

### Definitions

- **Database:** A collection of data that is organized in a way that makes it easy to access, manage, and update.
- **Relational database:** A type of database that stores data in tables.

## Organize and Protect Data

### Key Points

- Data should be organized in a way that makes it easy to find and use.
- Data should be protected from unauthorized access.
- There are many different ways to organize and protect data.

### Definitions

- **Data organization:** The process of organizing data in a way that makes it easy to find and use.
- **Data protection:** The process of protecting data from unauthorized access.

## Engage in the Data Community

### Key Points

- There is a large and active data community.
- The data community is a great resource for learning about data and data science.
- There are many ways to get involved in the data community.

### Definitions

- **Data community:** A group of people who are interested in data and data science.

---

# Step-by-Step: Meet wide and long data

This reading outlines the steps the instructor performs in the following video, [Meet wide and long data](https://www.coursera.org/learn/data-preparation/lecture/IbvwD/meet-wide-and-long-data). In this video, the instructor presents wide and long data formats and discusses the types of questions each format can help you answer.

Keep this guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

### **What you’ll need**

If you would like to access the spreadsheets the instructor uses in this video, select the link to a dataset to create a copy. If you don’t have a Google account, download the data directly from the attachments below.

Link to population datasets:

- [Population, Latin, and Caribbean Countries, 2010–2019, wide format](https://docs.google.com/spreadsheets/d/1aOcGeD7_8NvtEcVj2LD_79DaG2lwXrJC/template/preview#gid=2129150126)
- [Population, Latin, and Caribbean Countries, 2010–2019, long format](https://docs.google.com/spreadsheets/d/1NYjSNhjISWa6GUVlBifkPKStbrRzCot12BTYLo5kpqc/template/preview?resourcekey=0-Pyk5PUaVE1gYzlQtMiiHNQ#gid=932264330)

OR

Download data:

[Population, Latin, and Caribbean Countries, 2010–2019, wide formatXLSX File](https://d3c33hcgiwev3.cloudfront.net/MBhn3splQCKL8Lr2UTHRMg_3f9a14fdd3f947a2b978de8aee8804e1_Population-Latin-and-Caribbean-Countries-2010-2019-wide-format.xlsx?Expires=1716681600&Signature=VHlLvuoStTBcwxDFLhicXZIMom5CfotoHiW85iogjX7E6KUOaEO4F-UdOqiw9I4ZIhcguauAKw9sHLZ1Rxy027CMOiLbED~rqDWSe16qnIPGCHnDm9UdrLdRTxtCBcKtfK4IcYqiscyJPr6F3RbUGS4wyfl7D22~WH3pqQVQApQ_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

[Population, Latin, and Caribbean Countries, 2010–2019, long formatXLSX File](https://d3c33hcgiwev3.cloudfront.net/pAsDEZsvSpSwJDegUqvaGQ_5f34ed78cdcd494b821e4d8b29fdf8e1_Population-Latin-and-Caribbean-Countries-2010-2019-long-format-.xlsx?Expires=1716681600&Signature=Hrk0uBvaxTgCZZ~mSzj~SlWXHMOBJO2l3S4pptRjVgomdoyi~b9DYaqdC3O054rMeCkT98KKz0m~fY-VC-vINuaAwzBmk0F-RaoVdtrD-pwuOTG8IRRjXS~pQZ0k04iqBxElnHmxKLkWdNAj02yI6aYcO65V3Yg2YxNitFGXTRA_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

## Example 1: Examine wide data

Wide data is a dataset in which every data subject has a single row with multiple columns to hold the values of various attributes of the subject. It is helpful for comparing specific attributes across different subjects.

1. Open the [Population, Latin, and Caribbean Countries, 2010–2019, wide format](https://docs.google.com/spreadsheets/d/1ZlhSF9X-E-7LgIBXdEEgyw1Czm0dQvjJ/template/preview) spreadsheet.
2. Each row contains all population data for one country.
3. The population data for each year is contained in a column.
4. Find the annual population of Argentina in row 3.
5. In this wide format, you can quickly compare the annual population of Argentina to the annual populations of Antigua and Barbuda, Aruba, the Bahamas, or any other country.

### **Find the country with the highest population in 2010**

1. Select column **E**, which contains each country’s 2010 population data.
2. Right-click column header **E** and choose **Sort Z to A**.
3. Notice that Brazil is now at the top of the list because it had the highest population in the year 2010.

### **Find the country with the lowest population in 2013**

1. Select column **H**.
2. Right-click column header **H** and choose **Sort A to Z**.
3. Notice that the British Virgin Islands are now at the top because they had the lowest population of all countries in 2013.

## Example 2: Examine long data

Long data is data in which each row represents one observation per subject, so each subject will be represented by multiple rows. This data format is useful for comparing changes over time or making other comparisons across subjects.

1. Open the [Population, Latin, and Caribbean Countries, 2010–2019, long format](https://docs.google.com/spreadsheets/d/1NYjSNhjISWa6GUVlBifkPKStbrRzCot12BTYLo5kpqc/template/preview?pli=1&resourcekey=0-Pyk5PUaVE1gYzlQtMiiHNQ) spreadsheet.
2. Notice the data is no longer organized into columns by year. All of the years are now in one column.
3. Find Argentina’s population data in rows 12-21. Each row contains one year of Argentina’s population data.

---