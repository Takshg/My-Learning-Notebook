# Take a closer look at the data

---

# Same data, different outcome

[index (74).mp4](Take%20a%20closer%20look%20at%20the%20data%209f5f116938fa40ac93e70d4f424a96ab/index_(74).mp4)

**Key Points:**

- **Anscombe's quartet:** A set of four datasets that have nearly identical summary statistics but are visually very different. This highlights the importance of data visualization in addition to summary statistics.
- **Data visualization:** The process of creating visual representations of data to help us understand it better.
- **R:** A programming language and software environment for statistical computing and graphics.
- **Summary statistics:** Measures that describe the central tendency and variability of a dataset, such as mean, standard deviation, and correlation.

**Definitions:**

- **Mean:** The average of a set of numbers.
- **Standard deviation:** A measure of how spread out the data is.
- **Correlation:** A measure of how strongly two variables are related.
- **Visualization:** The process of creating visual representations of data.

**Summary:**

The video begins by discussing the importance of data visualization. It then introduces Anscombe's quartet, a set of four datasets that have nearly identical summary statistics but are visually very different. This highlights the fact that summary statistics can be misleading and that data visualization is essential for understanding data.

The video then goes on to show how to use R to create data visualizations. It covers topics such as installing packages, loading data, and creating plots.

The video concludes by emphasizing the importance of exploring data in multiple ways to learn more about its story.

---

# The bias function

[index (75).mp4](Take%20a%20closer%20look%20at%20the%20data%209f5f116938fa40ac93e70d4f424a96ab/index_(75).mp4)

This video lecture focuses on quantifying bias in data analysis using the `bias` function in R. Here's a detailed summary with key points and definitions:

**Key Points:**

- **Bias:** The difference between the actual outcome and the predicted outcome of your data.
- **Bias Function:** A function in R that calculates the average amount that the actual outcome is greater than the predicted outcome.
- **SimDesign Package:** An R package that contains the `bias` function.
- **Unbiased Model:** A model where the bias is close to zero.
- **Biased Model:** A model where the bias is significantly different from zero.

**Definitions:**

- **Actual Outcome:** The real-world result of an event or process.
- **Predicted Outcome:** The outcome predicted by a model or analysis.
- **Data Analysis:** The process of examining and interpreting data to extract meaningful insights.

**Key Takeaways:**

- The `bias` function helps quantify bias in data analysis, providing valuable information about the accuracy of your model.
- A high bias value indicates that your data might be biased and requires further investigation.
- Understanding bias is crucial for making informed decisions based on data analysis.

**Examples:**

- **Weather Channel:** The video uses the example of a weather channel to demonstrate how the `bias` function can identify bias in temperature predictions.
- **Game Store:** The video also uses the example of a game store to show how the `bias` function can help evaluate stock ordering practices.

---

# Working with biased data

Every data analyst will encounter an element of bias at some point in the data analysis process. That’s why it’s so important to understand how to identify and manage biased data whenever possible. You might recall we explored bias in detail in Course 3 of this program. In this reading, you will read a real-life example of an analyst who discovered bias in their data, and learn how they used R to address it.

## Addressing biased data with R

This scenario was shared by a quantitative analyst who collects data from people all over the world. They explain how they discovered bias in their data, and how they used R to address it:

“I work on a team that collects survey-like data. One of the tasks my team does is called a side-by-side comparison. For example, we might show users two ads side-by-side at the same time. In our survey, we ask which of the two ads they prefer. In one case, after many iterations, we were seeing consistent bias in favor of the first item. There was also a measurable decrease in the preference for an item if we swapped its position to second.

So we decided to add randomization to the position of the ads using R. We wanted to make sure that the items appeared in the first and second positions with similar frequencies. We used sample() to inject a randomization element into our R programming. In R, the sample() function allows you to take a random sample of elements from a data set. Adding this piece of code shuffled the rows in our data set randomly. So when we presented the ads to users, the positions of the ads were now random and controlled for bias. This made the survey more effective and the data more reliable.”

## Key takeaways

The sample() function is just one of many functions and methods in R that you can use to address bias in your data. Depending on the kind of analysis you are conducting, you might need to incorporate some advanced processes in your programming. Although this program won’t cover those kinds of processes in detail, you will likely learn more about them as you get more experience in the data analytics field.

To learn more about bias and data ethics, check out these resources:

- [**Bias function:**](https://www.rdocumentation.org/packages/SimDesign/versions/2.2/topics/bias) This web page is a good starting point to learn about how the bias function in R can help you identify and manage bias in your analysis.
- [**Data Science Ethics**](https://datasciencebox.org/02-ethics.html): This online course provides slides, videos, and exercises to help you learn more about ethics in the world of data analytics. It includes information about data privacy, misrepresentation in data, and applying ethics to your visualizations.

---

# Hands On Activity: Changing your data

## Activity overview

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UWFf-U9hTzKhX_lPYX8yBw_8c2e9cd211e3479a89816c7b1816ab07_image4.png?expiry=1717113600000&hmac=Gqe4LwaNIT8ElDkyxG__403kaOWYPbqS1QQg4FxF9VQ)

By now, you have learned many ways to change and work with data in a variety of settings, including spreadsheets and RStudio. In this activity, you’ll follow through a real-world scenario and practice manipulating and changing real data in R.

Upon completing this activity, you will know how to use functions to manipulate your data and use statistical summaries to explore your data. This will enable you to use R for more complex tasks in your career as a data analyst and help you gain initial insights into data that you can share with your stakeholders.

## Working in RStudio Cloud

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/TOqxzuNFR2eqsc7jRVdnKg_a3c6611d874f403a923e10406b4f38a9_image4.png?expiry=1717113600000&hmac=SA5ye_kHuZTlHoboPmvdTdy-HIGyy4bNDQ20XzTGB98)

To start, log into your RStudio (Posit) Cloud account. Open the project you will work on in the activity with [this link](https://posit.cloud/content/6208304), which opens in a new tab. If you haven't gone through this process already, at the top right portion of the screen you will see a "red stamp" indicating this project as a Temporary Copy. Click on the adjacent button, **Save a Permanent Copy**, and the project will be saved in your main dashboard for use with future lessons. Once that is completed, navigate to the file explorer in the bottom right and click on the following: **Course 7 -> Week 3 -> Lesson3_Change.Rmd**.

The .csv file that you will need, hotel_bookings.csv, is also located in this folder.

If you have trouble finding the correct activity, check out this [step-by-step guide](https://scribehow.com/shared/Access_and_Install_Course_Material_for_Lesson_3__JGhlL8PLSxuqtK2KRWZkJw) on how to navigate in RStudio (Posit) Cloud. Make sure to select the correct R markdown (Rmd) file. The other Rmd files will be used in different activities.

[Lesson3_Change.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/osHCTXtSSd2Bwk17Ukndiw_4c290cdedaab4ba0ae55358416b13ef1_Lesson3_Change.txt)

[hotel_bookings (2).csv](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/GL0bk8O2Sja9G5PDtko2uQ_31e445d7ca64417eb45aeaa08ec90bf1_hotel_bookings_(2).csv)

If you are using RStudio Desktop, you can download the Rmd file and the data for this activity directly here:

You can also find the Rmd file with the solutions for this activity here:

[Lesson3_Change_Solutions.txt](../All%20Lessons%20within%20RStudio%20eee207139d0e44b08808f644117b4284/2kdGwErrR6SHRsBK69ek2g_7b1b9b3017c24efab910e4bfa3e402f1_Lesson3_Change_Solutions.txt)

Carefully read the instructions in the comments of the Rmd file and complete each step. Some steps may be as simple as running pre-written code, while others may require you to write your own functions. After you finish the steps in the Rmd file, return here to confirm that your work is complete.