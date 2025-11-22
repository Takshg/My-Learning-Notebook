# Explore aesthetics in analysis

---

# Enhancing visualizations in R

[index (78).mp4](Explore%20aesthetics%20in%20analysis%2033e9de38ccf74a698db57271c0a90f45/index_(78).mp4)

**Introduction:**

- The video begins by highlighting the importance of aesthetics in data visualization.
- Aesthetics are visual properties of objects in a plot that can be used to highlight key points and communicate more effectively.

**Mapping Aesthetics to Variables:**

- The `aes()` function in R is used to map variables to aesthetics.
- Each aesthetic can be mapped to a specific variable by setting the name of the aesthetic equal to the name of the variable inside the parentheses of the `aes()` function.
- For example, to map the variable `flipper_length` to the x-axis and `body_mass` to the y-axis, you would write:

```r
ggplot(data = penguins, aes(x = flipper_length, y = body_mass)) +
  geom_point()

```

**Common Aesthetics:**

- The video covers the following common aesthetics:
    - **x and y:** These map variables to the x and y axes of the plot.
    - **color:** This maps a variable to the color of the data points.
    - **shape:** This maps a variable to the shape of the data points.
    - **size:** This maps a variable to the size of the data points.
    - **alpha:** This maps a variable to the transparency of the data points.

**Examples:**

- The video provides several examples of how to use aesthetics to enhance data visualizations.
- For example, it shows how to use color to distinguish between different species of penguins in a scatter plot.
- It also shows how to use shape and size to highlight different groups of data points.

**Additional Points:**

- The video emphasizes the importance of using aesthetics thoughtfully to avoid cluttering the plot and making it difficult to interpret.
- It also mentions that aesthetics can be used to make data visualizations more accessible to people with visual impairments.

**Key Takeaways:**

- Aesthetics are a powerful tool for enhancing data visualizations.
- The `aes()` function in R is used to map variables to aesthetics.
- Common aesthetics include color, shape, size, and alpha.
- Aesthetics should be used thoughtfully to avoid cluttering the plot.

**Definitions:**

- **Aesthetics:** Visual properties of objects in a plot.
- **Mapping:** Matching up a specific variable in your dataset with a specific aesthetic.
- **Legend:** A key that explains the meaning of different colors, shapes, or sizes in a plot.

---

# Aesthetic attributes

In this reading, you will learn about the three basic aesthetic attributes to consider when creating ggplot2 visualizations in R: **color, size,** and **shape.** These attributes are essential tools for creating data visualizations with ggplot2 and are built directly into its code.

## Aesthetics in ggplot2

**ggplot2** is an R package that allows you to create different types of data visualizations right in your R workspace. In ggplot2, an **aesthetic ****is defined as a visual property of an object in your plot.

There are three aesthetic attributes in ggplot2:

- **Color**: this allows you to change the color of all of the points on your plot, or the color of each data group
- **Size**: this allows you to change the size of the points on your plot by data group
- **Shape**: this allows you to change the shape of the points on your plot by data group

Here’s an example of how aesthetic attributes are displayed in R:

**ggplot(data, aes(x=distance, y= dep_delay, color=carrier, size=air_time, shape = carrier)) 
      geom_point()**

By applying these aesthetic attributes to your work with ggplot2, you can create data visualizations in R that clearly communicate trends in your data.

## Additional resources

For more information about aesthetic attributes, check out these resources:

- [**Data visualization with ggplot2 cheat sheet**](https://ggplot2.tidyverse.org/): RStudio’s cheat sheet is a great reference to use while working with ggplot2. It has tons of helpful information, including explanations of how to use geoms and examples of the different visualizations that you can create.
- [**RDocumentation aes function**](https://www.rdocumentation.org/packages/ggplot2/versions/3.3.3/topics/aes): This guide describes the syntax of the **aes** function and explains what each argument does.

---

# Doing more with ggplot

[index (79).mp4](Explore%20aesthetics%20in%20analysis%2033e9de38ccf74a698db57271c0a90f45/index_(79).mp4)

**Key Points:**

- **Geoms:** Geoms are the geometrical objects used to represent data in ggplot2. They include points, bars, lines, and more.
- **Scatter Plots:**
    - Use the `geom_point` function to create scatter plots.
    - Can use different geoms to represent the data in different ways, such as `geom_smooth` for a smooth line.
    - Can combine multiple geoms in the same plot to show different aspects of the data.
    - Use the `jitter` aesthetic to add random noise to points and avoid overplotting.
- **Bar Charts:**
    - Use the `geom_bar` function to create bar charts.
    - By default, counts the number of times each x-value appears in the data and shows the counts on the y-axis.
    - Can use aesthetics like `color` and `fill` to add color to the bars and make the plot easier to understand.
    - Can create stacked bar charts by mapping the `fill` aesthetic to a new variable.

**Definitions:**

- **ggplot2:** A popular R package for creating statistical graphics.
- **Scatter Plot:** A plot that shows the relationship between two continuous variables.
- **Bar Chart:** A plot that shows the frequency of categorical data.
- **Geom:** A geometrical object used to represent data in ggplot2.
- **Aesthetic:** A visual property of a geom, such as color, size, or shape.
- **Overplotting:** When data points in a plot overlap with each other, making it difficult to see the individual points.
- **Stacked Bar Chart:** A bar chart where bars are stacked on top of each other to show the distribution of a categorical variable across different categories of another variable.

**Additional Notes:**

- The video uses the `penguins` and `diamonds` datasets from the ggplot2 package.
- The video provides code examples for creating scatter plots and bar charts with different geoms and aesthetics.
- The video encourages learners to explore the ggplot2 cheat sheet for more information about geoms.

---

# Smoothing

In this reading, you will learn about smoothing in ggplot2 and how it can be used to make your data visualizations in R clearer and easier to follow. Sometimes it can be hard to understand trends in your data from scatter plots alone. **Smoothing** enables the detection of a data trend even when you can't easily notice a trend from the plotted data points. ggplot2’s smoothing functionality is helpful because it adds a **smoothing line** as another layer to a plot; the smoothing line helps the data to make sense to a casual observer.

**Example code**

---

ggplot(data, aes(x=distance, 
y= dep_delay)) +
    geom_point() +
    geom_smooth()

---

The example code creates a plot with a trend line similar to the blue line below.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XbKKHOhhSEKyihzoYchC-A_368afc47eb8a4edcbb089c2684ce088f_e0a48bb6-bfad-4eda-96bf-c292a3beac48.png?expiry=1717113600000&hmac=J4Em2GQ41rk-rYGUqWoSIg6TkF9W6UyUhZJL88goMAI)

# Two types of smoothing

| **Type of smoothing** | **Description** | **Example code** |
| --- | --- | --- |
| **Loess smoothing** | The loess smoothing process is best for smoothing plots with less than 1000 points. | **ggplot(data, aes(x=, y=))+ 
  geom_point() +       
  geom_smooth(method="loess")** |
| **Gam smoothing** | Gam smoothing, or generalized additive model 
smoothing, is useful for smoothing plots with a large number of points. | **ggplot(data, aes(x=, y=)) + 
  geom_point() +        
  geom_smooth(method="gam", 
formula = y ~s(x))** |

The smoothing functionality in ggplot2 helps make data plots more readable, so you are better able to recognize data trends and make key insights. The first plot below is the data before smoothing, and the second plot below is the same data after smoothing.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/wPPc24hXSWuz3NuIV0lrnQ_912eda8141a1490597aa1f78a57921c5_b6a22f66-9ecc-4452-aa73-79e0673d26f5.png?expiry=1717113600000&hmac=dfm7-pz_F3k9E8U_cVnwZ6WMeY3SabKrNVmmVwmmI8w)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/f1AMePxESHyQDHj8RPh8OQ_100fd672112445729c7b0d534ec2ab82_755509aa-c74b-4eb0-a1ec-ff884e86b97f.png?expiry=1717113600000&hmac=6rwtqDF_lrOQUKMfOc11X6yezTe6PKiekiiQAwtc6SE)

# Key takeaways

Smoothing helps data professionals reveal trends. When scatterplots alone lack clarity, smoothing adds a trend line, making underlying patterns in the data easier to spot for casual observers. ggplot2 offers two smoothing methods: Loess is best for plots with fewer than 1,000 points, it creates a flexible, local smoother. Gam is ideal for larger datasets because it uses a more robust model for general trends. Smoothing enhances data communication, adding a visual cue to highlight trends so data visualizations become clearer and more impactful for audiences.

---

# Aesthetics and facets

[index (80).mp4](Explore%20aesthetics%20in%20analysis%2033e9de38ccf74a698db57271c0a90f45/index_(80).mp4)

This video introduces the concept of faceting in ggplot2, a powerful tool for visualizing data in smaller groups or subsets.

**Key Points:**

- **What is faceting?** Faceting allows you to display different subsets of your data on separate plots, revealing patterns and relationships that might be hidden in a single plot.
- **Types of faceting:**
    - **`facet_wrap`:** Creates separate plots for each level of a single variable.
    - **`facet_grid`:** Creates a grid of plots, with each plot representing a combination of levels from two or more variables.
- **Benefits of faceting:**
    - **Focus on specific relationships:** Faceting helps you focus on specific relationships between variables within different groups of your data.
    - **Identify patterns and trends:** Faceting can reveal patterns and trends that might not be apparent in a single plot, especially when dealing with complex data.
    - **Simplify complex visualizations:** Faceting can make complex visualizations easier to understand by breaking them down into smaller, more manageable chunks.
- **Examples:**
    - **Penguin data:** The video demonstrates how to use `facet_wrap` to create separate plots for each species of penguin, allowing you to compare the relationship between body mass and flipper length across different species.
    - **Diamonds data:** The video shows how to use `facet_wrap` to create separate bar charts for each category of cut in the diamonds dataset.
    - **Combined faceting:** The video demonstrates how to use `facet_grid` to create a grid of plots, with each plot representing a combination of species and sex in the penguin data. This allows you to compare the relationship between body mass and flipper length across different combinations of these variables.
- **Customization:** The video briefly touches on how to customize your faceted plots by focusing on specific variables or removing variables from the faceting grid.

**Definitions:**

- **Facet:** A side or section of an object, like the sides of a gemstone. In ggplot2, facets represent different subsets of your data displayed on separate plots.
- **`facet_wrap`:** A function in ggplot2 that creates separate plots for each level of a single variable.
- **`facet_grid`:** A function in ggplot2 that creates a grid of plots, with each plot representing a combination of levels from two or more variables.

---

# Hands on Activity: Aesthetics and visualizations

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

In previous activities, you learned about and worked with ggplot2, an R package for data visualization. In this activity, you’ll follow through a scenario and continue to apply ggplot2 to tailor aesthetic features of visualizations.

By the end of this activity, you will be able to use R to create bar charts, update chart labels, and customize the aesthetics of a visualization by specific criteria. This will enable you to make more complex visualizations to demonstrate your findings.

## Working in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed, navigate to the file explorer in the bottom right and click on the following: **Course 7 -> Week 4 -> Lesson3_Aesthetics.Rmd**.

The .csv file that you will need, hotel_bookings.csv, is also located in this folder.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

[Lesson3_Aesthetics.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/BcijwTl7RhKIo8E5e2YSeg_3e0f5bb543fa4525a0378a7ba0338bf1_Lesson3_Aesthetics.txt)

[hotel_bookings (4).csv](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings_(4).csv)

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

You can also find the Rmd file with the solutions for this activity here:

[Lesson3_Aesthetics_Solutions.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/Fd1svexhQ82dbL3sYRPNwA_9fece722572248bda9738cdf7f8633f1_Lesson3_Aesthetics.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.

**Note**: In Step #6 of the .RMD exercise attachment, be sure to add the chart variable name **deposit_type** within the facet_wrap function parentheses. Your code lines should look like this in your R editor:

**{r creating a plot}**

**ggplot(data = hotel_bookings) +**

**geom_bar(mapping = aes(x = distribution_channel)) +**

**facet_wrap(~deposit_type)**

---

# Filtering and plots

By this point you have likely downloaded at least a few packages into your R library. The tools in some of these packages can actually be combined and used together to become even more useful. This reading will share a few resources that will teach you how to use the filter function from **dplyr** to make the plots you create with **ggplot2** easier to read.

## Example of filtering data for plotting

Filtering your data before you plot it allows you to focus on specific subsets of your data and gain more targeted insights. To do this, just include the dplyr filter() function in your ggplot syntax.

**Example code**

---

```sql
data %>%
    filter(variable1 == "DS") %>%  
    ggplot(aes(x = weight, y = variable2, colour = variable1)) +  
    geom_point(alpha = 0.3,  position = position_jitter()) + stat_smooth(method = "lm")
```

---

## Additional resources

To learn more details about ggplot2 and filtering with dplyr, check out these resources:

- [**Putting it all together: (dplyr+ggplot)](https://rladiessydney.org/courses/ryouwithme/03-vizwhiz-1/#1-4-putting-it-all-together-dplyr-ggplot):** The RLadies of Sydney’s course on R uses real data to demonstrate R functions. This lesson focuses specifically on combining dplyr and ggplot to filter data before plotting it. The instructional video will guide you through every step in the process while you follow along with the data they have provided.
- [**Data transformation:](https://r4ds.had.co.nz/transform.html)** This resource focuses on how to use the filter() function in R, and demonstrates how to combine filter() with ggplot(). This is a useful resource if you are interested in learning more about how filter() can be used before plotting.
- [**Visualizing data with ggplot2:**](https://datacarpentry.org/dc_zurich/R-ecology/05-visualisation-ggplot2.html) This comprehensive guide includes everything from the most basic uses for ggplot2 to creating complicated visualizations. It includes the filter() function in most of the examples so you can learn how to implement it in R to create data visualizations.

---

# Hands On Activity: Filters and plots

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

So far, you have learned a lot about ggplot2 and how to create data visualizations in R. In this activity, you’ll follow through a scenario and use the filters and facets features of ggplot2.

By the end of this activity, you will be able to customize your visualizations by applying filters and highlighting facets. This will enable you to emphasize certain aspects of your insights to create comparisons and more nuanced insights in your presentations.

## Working in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed, navigate to the file explorer in the bottom right and click on the following: **Course 7 -> Week 4 -> Lesson3_Filters.Rmd**.

The .csv file that you will need, hotel_bookings.csv, is also located in this folder.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

[Lesson3_Filters.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/cgXdEhw9SqmF3RIcPXqpiQ_62e138c702bb4abfba5db60f97e5edf1_Lesson3_Filters.txt)

[hotel_bookings (5).csv](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings_(5).csv)

You can also find the Rmd file with the solutions for this activity here:

[Lesson3_Filters_Solutions.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/w44BXN8tRZ2OAVzfLSWdHg_a8a82a7f1a8c4869818fdd818b333ef1_Lesson3_Filters_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.

---