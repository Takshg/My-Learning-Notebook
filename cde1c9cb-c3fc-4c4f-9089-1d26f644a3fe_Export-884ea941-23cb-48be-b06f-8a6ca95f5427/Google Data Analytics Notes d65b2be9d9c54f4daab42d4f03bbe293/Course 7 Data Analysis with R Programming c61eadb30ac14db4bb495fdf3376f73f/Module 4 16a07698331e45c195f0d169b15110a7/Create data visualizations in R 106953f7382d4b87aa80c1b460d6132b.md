# Create data visualizations in R

---

# Visualization in R

**Introduction:**

- Data visualization is a crucial part of data analysis, allowing you to communicate insights and trends in a clear and compelling way.
- ggplot2 is a user-friendly and versatile data visualization tool that helps you create a wide range of plots.

**Key Concepts:**

- **ggplot2 syntax:** The basic structure of ggplot2 code involves specifying the data, aesthetics (visual properties), and geoms (geometrical objects like points, lines, or bars).
- **Aesthetics:** These define the visual appearance of your plot, such as the color, size, and shape of data points.
- **Geoms:** These represent the different types of plots you can create, such as scatter plots, histograms, and boxplots.

**Creating Plots:**

- To create a basic scatter plot, you use the `geom_point()` function and specify the aesthetics for the x and y axes.
- You can customize the appearance of your plot by adjusting the aesthetics, adding labels, and changing the theme.

**Additional Features:**

- ggplot2 offers a wide range of features for creating complex and informative visualizations.
- You can use faceting to create multiple plots based on different subsets of your data.
- You can also add annotations and statistical summaries to your plots.

**Benefits of ggplot2:**

- ggplot2 is a powerful and flexible tool that allows you to create a wide variety of plots.
- It is also relatively easy to learn and use, making it a popular choice for data analysts of all levels.

**Next Steps:**

- The video provides a brief introduction to ggplot2. To learn more about the package and its features, you can refer to the official documentation or online tutorials.
- You can also practice creating your own plots using the exercises provided in the course.

**Definitions:**

- **Data visualization:** The process of representing data in a visual format, such as charts, graphs, and maps.
- **ggplot2:** A popular data visualization package in R that allows you to create a wide range of plots.
- **Aesthetics:** The visual properties of a plot, such as the color, size, and shape of data points.
- **Geoms:** The geometrical objects used to represent data in a plot, such as points, lines, or bars.

---

# Visualizations basics in R and tidyverse

[index (76).mp4](Create%20data%20visualizations%20in%20R%20106953f7382d4b87aa80c1b460d6132b/index_(76).mp4)

**1. Visualization Packages in R:**

- Base R has its own visualization package.
- Other useful packages include:
    - Plotly: General-purpose package for various visualizations.
    - RGL: Focuses on 3D visuals.
    - ggplot2: Popular choice for data analysis due to its power and flexibility.
    - Plotly, Lattice, RGL, Dygraphs, Leaflet, Highcharter, Patchwork, gganimate, ggridges.

**2. Why ggplot2?**

- Created by Hadley Wickham in 2005, inspired by "The Grammar of Graphics" by Leland Wilkinson.
- Follows the "grammar of graphics" principles, providing building blocks for creating diverse visualizations.
- Allows creating various plots like scatter plots, bar charts, line diagrams, and more.
- Offers customization options for colors, layout, dimensions, and text elements.
- Combines data manipulation and visualization using the pipe operator.
- Extensive function library for diverse data visualization needs.
- Popular reference guide: ggplot2 cheat sheet (covered in upcoming reading).

**3. Key Concepts in ggplot2:**

- **Aesthetics:** Visual properties of objects in a plot (e.g., size, shape, color of data points).
- **Geoms:** Geometric objects representing data (e.g., points, bars, lines).
- **Facets:** Displaying smaller groups or subsets of data in separate plots.
- **Labels and Annotations:** Adding text elements like titles, subtitles, captions, and highlights.

**4. Next Steps:**

- The next video will delve deeper into these concepts and demonstrate creating the first plot in ggplot2.

**Definitions:**

- **ggplot2:** A data visualization package in R known for its power and flexibility.
- **Grammar of Graphics:** A set of principles for creating effective data visualizations.
- **Aesthetics:** Visual properties of objects in a plot.
- **Geoms:** Geometric objects used to represent data in a plot.
- **Facets:** A way to display smaller groups or subsets of data in separate plots.
- **Labels and Annotations:** Text elements added to a plot for clarity and communication.

---

# Hands On Activity: Visualizing data with ggplot2

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

Earlier in this course, you encountered ggplot2, an R package for data visualization. In this activity, you’ll learn about the basic logic of data visualization in ggplot2 and how to create a plot using R code.

By the time you complete this activity, you’ll be able to write R functions that create data visualizations. This will enable you to create basic visualizations to demonstrate and share findings with your data and code.

## The basics of ggplot2

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

The ggplot2 package lets you make high quality, customizable plots of your data. As a refresher, ggplot2 is based on the grammar of graphics, which is a system for describing and building data visualizations. The essential idea behind the grammar of graphics is that you can build any plot from the same basic components, like building blocks.

These building blocks include:

- A dataset
- A set of geoms: A geom refers to the geometric object used to represent your data. For example, you can use points to create a scatterplot, bars to create a bar chart, lines to create a line diagram, etc.
- A set of aesthetic attributes: An aesthetic is a visual property of an object in your plot. You can think of an aesthetic as a connection, or mapping, between a visual feature in your plot and a variable in your data. For example, in a scatterplot, aesthetics include things like the size, shape, color, or location (x-axis, y-axis) of your data points.

To create a plot with ggplot2, you first choose a dataset. Then, you determine how to visually organize your data on a coordinate system by choosing a geom to represent your data points and aesthetics to map your variables.

## Prepare your data

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

The ggplot2 package lets you use R code to specify the dataset, geom, and aesthetics of your plot.

To do this, first choose a dataset to work with. For this activity, you will use the Palmer Penguins data that you’re already familiar with from earlier videos. However, you can also use another dataset instead.

Once you decide on your dataset, open RStudio and follow these steps:

1. If you have not done so before, use the install.packages() function to install both ggplot2 and the Palmer Penguins data set. Type **install.packages(“ggplot2”)** and **install.packages(“palmerpenguins”)**, then click **Run**.

2. Load ggplot2 and the dataset using the library() function. Type **library(ggplot2)** and **library(palmerpenguins)**.

3.  Now, examine the data frame for the penguins data. To do this, use the data() and View() functions. Use a capital “V” for the View() function since functions in R are case sensitive. Type **data(penguins)** and **View(penguins)**, then click **Run**.

The first 10 rows of the data frame should appear like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/OWK0QYSXRaaitEGElzWm9A_3a1c99cce66a4884b5e36b0bf6a4ad73_image2.png?expiry=1717113600000&hmac=l0PmQzMJVU1HP4NXiDFcSITUXxXgY_jmha4C5O2-k9s)

The penguins dataset contains size measurements for three penguin species (Adelie, Chinstrap, and Gentoo) that live on the Palmer Archipelago in Antarctica. The columns include information such as body mass, flipper length, and bill length.

## Create a plot in ggplot2

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

Suppose you want to plot the relationship between body mass and flipper length in the three penguin species. You can choose a specific geom that fits the type of data you have. Points show the relationship between two quantitative variables. A scatterplot of points would be an effective way to display the relationship between the two variables. You can put flipper length on the x-axis and body mass on the y-axis.

Type the following code to create the plot. But before you run it, review the code piece by piece:

**ggplot(data = penguins) + geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

**ggplot(data = penguins):** In ggplot2, you begin a plot with the ggplot() function. The ggplot() function creates a coordinate system that you can add layers to. The first argument of the ggplot() function is the dataset to use in the plot. In this case, it’s “penguins.”

**+**: Then, you add a “+” symbol to add a new layer to your plot. You complete your plot by adding one or more layers to ggplot().

**geom_point()**: Next, you choose a geom by adding a geom function. The geom_point() function uses points to create scatterplots, the geom_bar function uses bars to create bar charts, and so on. In this case, choose the geom_point function to create a scatter plot of points. The ggplot2 package comes with many different geom functions. You’ll learn more about geoms later in this course.

**(mapping = aes(x = flipper_length_mm, y = body_mass_g))**: Each geom function in ggplot2 takes a mapping argument. This defines how variables in your dataset are mapped to visual properties. The mapping argument is always paired with the aes() function. The x and y arguments of the aes() function specify which variables to map to the x-axis and the y-axis of the coordinate system. In this case, you want to map the variable “flipper_length_mm” to the x-axis, and the variable “body_mass_g” to the y-axis.

Now go ahead and run the code. When you do, you get the following plot:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bd3oykIoQMid6MpCKLDI7A_a310e470312243058fbe1ef6d730f602_image3.png?expiry=1717113600000&hmac=atoRM2hqwVJv0YPOBVysyS1Bv9Tp82qik2dUfuFp79w)

The plot shows a positive relationship between the two variables. In other words, the larger the penguin, the longer the flipper.

## Create your own plot

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To create your own plot using code, follow these three steps:

1. Start with the ggplot() function and choose a dataset to work with.

2. Add a geom_ function to display your data.

3. Map the variables you want to plot in the arguments of the aes() function.

Try plotting with different datasets using different geoms and mapping arguments. Coming up in this course, you’ll learn even more about the process of creating a plot. You’ll also get a chance to work with the Penguins dataset to create lots of different plots in ggplot2.

**Pro-Tip:** You can write the same section of code above using a different syntax with the mapping argument inside the ggplot() call: **ggplot(data = penguins, mapping = aes(x = flipper_length_mm, y = body_mass_g)) +  geom_point()**

## The ggplot2 cheat sheet

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

This is just the beginning of what you can do with ggplot2. If you want to find out more about ggplot2, RStudio has a useful reference guide called the “Data Visualization with ggplot2 Cheat Sheet.” You can use the Cheat Sheet as a quick reference while you work to learn about the main functions and features of ggplot2.

Click the link to check it out: [Cheat Sheet](https://ggplot2.tidyverse.org/)

---

# Getting started with ggplot()

[index (77).mp4](Create%20data%20visualizations%20in%20R%20106953f7382d4b87aa80c1b460d6132b/index_(77).mp4)

---

# Common problems when visualizing in R

*You can save this reading for future reference. Feel free to download a PDF version of this reading below:*

[Common-problems-encountered-when-visualizing-in-R.pdf](Create%20data%20visualizations%20in%20R%20106953f7382d4b87aa80c1b460d6132b/pALIn_4vSECCyJ_-L4hAJg_3c83255ab5004b1a99957907331217b0_Common-problems-encountered-when-visualizing-in-R.pdf)

Coding errors are an inevitable part of writing code—especially when you are first beginning to learn a new programming language. In this reading, you will learn how to recognize common coding errors when creating visualizations using **ggplot2**. You will also find links to some resources that you can use to help address any coding problems you might encounter moving forward.

## Common coding errors in ggplot2

When working with R code in ggplot2, a lot of the most common coding errors involve issues with syntax, like misplaced characters. That is why paying attention to details is such an important part of writing code. When there is an error in your code that R is able to detect, it will generate an error message. Error messages can help point you in the right direction, but they won’t always help you figure out the precise problem.

Let’s explore a few of the most common coding errors you might encounter in ggplot2.

### **Case sensitivity**

R code is case sensitive. If you accidentally capitalize the first letter in a certain function, it might affect your code. Here is an example:

**Glimpse(penguins)**

The error message lets you know that R cannot find a function named “Glimpse”:

**Error in Glimpse(penguins) : could not find function "Glimpse"**

But you know that the function glimpse (lowercase “g”) does exist. Notice that the error message doesn’t explain exactly what is wrong but does point you in a general direction.

Based on that, you can figure out that this is the correct code:

**glimpse(penguins)**

### **Balancing parentheses and quotation marks**

Another common R coding error involves parentheses and quotation marks. In R, you need to make sure that every opening parenthesis in your function has a closing parenthesis, and every opening quotation mark has a closing quotation mark. For example, if you run the following code, nothing happens. R does not create the plot. That is because the second line of code is missing two closing parentheses:

**ggplot(data = penguins) +**

**geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g**

RStudio does alert you to the problem. To the left of the line of code in your RStudio source  editor, you might notice a red circle with a white “X” in the center. If you hover over the circle with your cursor, this message appears:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9WGVKuXpRj-hlSrl6TY_tQ_1178b17293114296b0367d6809206f67_Screen-Shot-2021-01-27-at-9.31.44-PM.png?expiry=1717113600000&hmac=7gOLmzNqRO8gXjdguQH1BeUegm8Z-syLc0rno3YAK58)

RStudio lets you know that you have an unmatched opening bracket. So, to correct the code, you know that you need to add a closing bracket to match each opening bracket.

Here is the correct code:

**ggplot(data = penguins) +**

**geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

### **Using the plus sign to add layers**

In ggplot2, you need to add a plus sign (“+”) to your code when you add a new layer to your plot. Putting the plus sign in the wrong place is a common mistake. The plus sign should always be placed at the end of a line of code, and not at the beginning of a line.

Here’s an example of code that includes incorrect placement of the plus sign:

**ggplot(data = penguins)**

**+ geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

In this case, R’s error message identifies the problem, and prompts you to correct it:

**Error: Cannot use `+.gg()` with a single argument. Did you accidentally put + on a new line?**

Here is the correct code:

**ggplot(data = penguins) +**

**geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

You also might accidentally use a pipe instead of a plus sign to add a new layer to your plot, like this:

**ggplot(data = penguins)%>%**

**geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

You then get the following error message:

**Error: `data` must be a data frame, or other object coercible by `fortify()`, not an S3 object with class gg/ggplot**

Here is the correct code:

**ggplot(data = penguins) +**

**geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))**

Keeping these issues in mind and paying attention to details when you write code will help you reduce errors and save time, so you can stay focused on your analysis.

## Help resources

Everyone makes mistakes when writing code–it is just part of the learning process. Fortunately, there are lots of helpful resources available in RStudio and online.

### **R documentation**

R has built-in documentation for all functions and packages. To learn more about any R function, just run the code **?function_name**. For example, if you want to learn more about the geom_bar function, type:

?geom_bar

When you run the code, an entry on “geom_bar” appears in the Help viewer in the lower-right pane of your RStudio workspace. The entry begins with a “Description” section that discusses bar charts:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ZM4mMO-OQZSOJjDvjiGU3A_7e7f14e87d5549a98bb44324a341693e_Screen-Shot-2021-01-27-at-9.52.33-PM.png?expiry=1717113600000&hmac=XeN2kcvjwklGhCo-Syz6LzZISsX4AYsPayTDEciCzEk)

The [RDocumentation website](https://www.rdocumentation.org/) contains much of the same content in a slightly different format, with additional examples and links.

### **ggplot2 documentation**

The [ggplot2 page](https://ggplot2.tidyverse.org/), which is part of the official tidyverse documentation, is a great resource for all things related to ggplot2. It includes entries on key topics, useful examples of code, and links to other helpful resources.

### **Online search**

Doing an online search for the error message you are encountering (and including “R” and the function or package name in your search terms) is another option. There is a good chance someone else has already encountered the same error and posted about it online.

### **The R community**

If the other resources don’t help, you can try reaching out to the R community online. There are lots of useful online forums and websites where people ask for and receive help, including:

- [R for Data Science Online Learning Community](https://www.rfordatasci.com/)
- [RStudio Community](https://community.rstudio.com/)
- [Stackoverflow](http://stackoverflow.com/)
- [Twitter (#rstats)](https://twitter.com/hashtag/rstats?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1229486581620367361%7Ctwgr%5Eshare_3&ref_url=https%3A%2F%2Fwww.t4rstats.com%2F&src=hashtag_click)

---

# Hands On Activity: Using ggplot

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

In the last activity, you got an introduction to visualizing data in ggplot2. In this activity, you’ll dive deeper with ggplot2 to quickly create data visualizations that allow you to explore your data and gain new insights.

By the time you complete this activity, you will have strengthened your understanding of ggplot2 and visualizing data in R. You will be able to use basic ggplot2 syntax and troubleshoot some common errors you might encounter. This will enable you to easily demonstrate and share your insights throughout your career as a data analyst.

## Working in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed,  navigate to the file explorer in the bottom right and click on the following: **Course 7 -> Week 4 -> Lesson2_GGPlot.Rmd**.

The .csv file you will need, hotel_bookings.csv, is also located in this folder.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

[Lesson2_GGPlot.txt](Create%20data%20visualizations%20in%20R%20106953f7382d4b87aa80c1b460d6132b/algvdUHgT7iYL3VB4B-49g_f8ffabe1fac842d6872cca560da7c9f1_Lesson2_GGPlot.txt)

[hotel_bookings (3).csv](Create%20data%20visualizations%20in%20R%20106953f7382d4b87aa80c1b460d6132b/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings_(3).csv)

You can also find the Rmd file with the solutions for this activity here:

[Lesson2_GGPlot_Solutions.txt](Create%20data%20visualizations%20in%20R%20106953f7382d4b87aa80c1b460d6132b/jTmZc7yMSMW5mXO8jJjF6w_f6509abd385345a494a310d8aaea23f1_Lesson2_GGPlot_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.

---