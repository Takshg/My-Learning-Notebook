# Overcome the challenges of insufficient data

---

# Deal with insufficient data

### **Key Points**

- **Insufficient data is a common challenge for data analysts.** This can occur even though vast amounts of data are generated daily.
- **Insufficient data can lead to inaccurate insights and poor decision-making.** It's crucial to recognize and address this issue before starting your analysis.
- **This video explores common limitations of data and strategies for dealing with them.**

### **Definitions**

- **Insufficient data:** Data that is inadequate for a specific analysis due to limitations in scope, timeliness, relevance, or accuracy.
- **Data scope:** The range of data sources and variables considered in an analysis.
- **Data timeliness:** The recency and completeness of the data.
- **Data relevance:** The extent to which the data is applicable to the specific analysis being conducted.
- **Data accuracy:** The degree to which the data reflects the true values of the variables being measured.

### **Common Limitations of Data**

- **Limited data scope:** Using data from only one source can lead to biased or incomplete insights.
- **Incomplete data:** Data that is still being collected or is missing values can lead to inaccurate conclusions.
- **Outdated data:** Data that is no longer relevant can lead to misleading results.
- **Geographically limited data:** Data that only covers a specific region may not be representative of a broader population.

### **Strategies for Dealing with Insufficient Data**

- **Identify trends with the available data:** Analyze the data you have to identify patterns and insights.
- **Wait for more data if time allows:** If possible, wait for additional data to become available before drawing conclusions.
- **Talk with stakeholders and adjust your objective:** Discuss the limitations of the data with stakeholders and adjust the analysis objective accordingly.
- **Look for a new data set:** Seek out a more comprehensive or relevant data set for your analysis.

### **Additional Notes**

- The video emphasizes the importance of understanding your business objective before starting your analysis. This will help you determine whether you have sufficient data and identify potential limitations.
- The video also highlights the importance of communicating with stakeholders about data limitations and adjusting your analysis accordingly.

**Overall, this video provides valuable insights into the challenges of insufficient data and strategies for overcoming them.** By understanding these limitations and implementing the suggested strategies, you can ensure that your data analysis is accurate and reliable.

---

# When you find an issue with your data

When you are getting ready for data analysis, you might realize you don’t have the data you need or you don’t have enough of it. In some cases, you can use what is known as proxy data in place of the real data. Think of it like substituting oil for butter in a recipe when you don’t have butter. In other cases, there is no reasonable substitute and your only option is to collect more data.

Consider the following data issues and suggestions on how to work around them.

## Data issue 1: no data

| **Possible Solutions** | **Examples of solutions in real life** |
| --- | --- |
| Gather the data on a small scale to perform a preliminary analysis and then request additional time to complete the analysis after you have collected more data. | If you are surveying employees about what they think about a new performance and bonus plan, use a sample for a preliminary analysis. Then, ask for another 3 weeks to collect the data from all employees. |
| If there isn’t time to collect data, perform the analysis using proxy data from other datasets. 
*This is the most common workaround.* | If you are analyzing peak travel times for commuters but don’t have the data for a particular city, use the data from another city with a similar size and demographic. |

## Data issue 2: too little data

| **Possible Solutions** | **Examples of solutions in real life** |
| --- | --- |
| Do the analysis using proxy data along with actual data. | If you are analyzing trends for owners of golden retrievers, make your dataset larger by including the data from owners of labradors. |
| Adjust your analysis to align with the data you already have. | If you are missing data for 18- to 24-year-olds, do the analysis but note the following limitation in your report: *this conclusion applies to adults 25 years and older* *only*. |

## Data issue 3: wrong data, including data with errors*

| **Possible Solutions** | **Examples of solutions in real life** |
| --- | --- |
| If you have the wrong data because requirements were misunderstood, communicate the requirements again. | If you need the data for female voters and received the data for male voters, restate your needs. |
| Identify errors in the data and, if possible, correct them at the source by looking for a pattern in the errors. | If your data is in a spreadsheet and there is a conditional statement or boolean causing calculations to be wrong, change the conditional statement instead of just fixing the calculated values. |
| If you can’t correct data errors yourself, you can ignore the 
wrong data and go ahead with the analysis if your sample size is still large enough and ignoring the data won’t cause systematic bias. | If your dataset was translated from a different language and some of the translations don’t make sense, ignore the data with bad translation and go ahead with the analysis of the other data. |
- ***Important note:** Sometimes data with errors can be a warning sign that the data isn’t reliable. Use your best judgment.*

### Use the following decision tree as a reminder of how to deal with data errors or not enough data:

1. Can you fix or request a corrected dataset?
NO

2. Do you have enough data to omit the wrong data?
NO

3. Can you proxy the data?
NO

4. Can you collect more data?
NO

Modify the business objective (if possible)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nubavN6IS5mm2rzeiFuZgw_1204106238b34cff9a89859772cdfaa1_Screen-Shot-2021-03-05-at-10.36.19-AM.png?expiry=1716854400000&hmac=uZ_Bc-Lb7LebtaPhgNCBZHJHJHV5YN8izuqH5sMtdDo)

---

# The importance of sample size

### **Key Points**

- **Importance of Data Integrity:** Having the right kind and amount of data is crucial for accurate analysis and achieving business objectives.
- **Population vs. Sample:** A population encompasses all possible data values in a dataset, while a sample represents a smaller portion of the population chosen to make predictions about the whole.
- **Sample Size:** Using a sample size is more cost-effective and time-saving than analyzing the entire population, especially when dealing with large datasets.
- **Sampling Bias:** When a sample doesn't accurately represent the population, leading to inaccurate conclusions.
- **Random Sampling:** A method of selecting a sample where every possible type of the sample has an equal chance of being chosen, minimizing sampling bias.

### **Definitions**

- **Population:** All possible data values in a dataset.
- **Sample:** A smaller portion of the population used to make predictions about the whole.
- **Sample Size:** The number of individuals or data points included in a sample.
- **Sampling Bias:** When a sample doesn't accurately represent the population, leading to inaccurate conclusions.
- **Random Sampling:** A method of selecting a sample where every possible type of the sample has an equal chance of being chosen.

### **Additional Points**

- Using a sample size can lead to uncertainty, as it's not a perfect representation of the entire population.
- Random sampling helps address sampling bias by ensuring equal representation of all population types.
- Understanding sample size is important for data analysts, even if they don't directly create the samples.

---

# Calculate sample size

Before you dig deeper into sample size, familiarize yourself with these terms and definitions:

| **Terminology** | **Definitions** |
| --- | --- |
| **Population** | The entire group that you are interested in for your study. For example, if you are surveying people in your company, the population would be all the employees in your company. |
| **Sample** | A subset of your population. Just like a food sample, it is called a sample because it is only a taste. So if your company is too large to survey every individual, you can survey a representative sample of your population. |
| **Margin of error** | Since a sample is used to represent a population, the sample’s results are expected to differ from what the result would have been if you had surveyed the entire population. This difference is called the margin of error. The smaller the margin of error, the closer the results of the sample are to what the result would have been if you had surveyed the entire population. |
| **Confidence level** | How confident you are in the survey results. For example, a 95% confidence level means that if you were to run the same survey 100 times, you would get similar results 95 of those 100 times. Confidence level is targeted before you start your study because it will affect how big your margin of error is at the end of your study. |
| **Confidence interval** | The range of possible values that the population’s result would be at the confidence level of the study. This range is the sample result +/- the margin of error. |
| **Statistical significance** | The determination of whether your result could be due to random chance or not. The greater the significance, the less due to chance. |

## Things to remember when determining the size of your sample

When figuring out a sample size, here are things to keep in mind:

- Don’t use a sample size less than 30. It has been statistically proven that 30 is the smallest sample size where an average result of a sample starts to represent the average result of a population.
- The confidence level most commonly used is 95%, but 90% can work in some cases.

Increase the sample size to meet specific needs of your project:

- For a **higher** confidence level, use a larger sample size
- To **decrease** the margin of error, use a larger sample size
- For **greater** statistical significance, use a larger sample size

**Note:** Sample size calculators use statistical formulas to determine a sample size. More about these are coming up in the course!  Stay tuned.

### **Why a minimum sample of 30?**

This recommendation is based on the **Central Limit Theorem (CLT)** in the field of probability and statistics. As sample size increases, the results more closely resemble the normal (bell-shaped) distribution from a large number of samples. A sample of 30 is the smallest sample size for which the CLT is still valid. Researchers who rely on **regression analysis** – ****statistical methods to determine the relationships between controlled and dependent variables – ****also prefer a minimum sample of 30.

Still curious? Without getting too much into the math, check out these articles:

- [Central Limit Theorem (CLT)](https://www.investopedia.com/terms/c/central_limit_theorem.asp): This article by Investopedia explains the Central Limit Theorem and briefly describes how it can apply to an analysis of a stock index.
- [Sample Size Formula](https://www.statisticssolutions.com/dissertation-resources/sample-size-calculation-and-sample-size-justification/sample-size-formula/): This article by Statistics Solutions provides a little more detail about why some researchers use 30 as a minimum sample size.

## Sample sizes vary by business problem

Sample size will vary based on the type of business problem you are trying to solve.

For example, if you live in a city with a population of 200,000 and get 180,000 people to respond to a survey, that is a large sample size. But without actually doing that, what would an acceptable, smaller sample size look like?

Would 200 be alright if the people surveyed represented every district in the city?

**Answer**: It depends on the stakes.

- A sample size of 200 might be large enough if your business problem is to find out how residents felt about the new library
- A sample size of 200 might not be large enough if your business problem is to determine how residents would vote to fund the library

You could probably accept a larger margin of error surveying how residents feel about the new library versus surveying residents about how they would vote to fund it. For that reason, you would most likely use a larger sample size for the voter survey.

## Larger sample sizes have a higher cost

You also have to weigh the cost against the benefits of more accurate results with a larger sample size. Someone who is trying to understand consumer preferences for a new line of products wouldn’t need as large a sample size as someone who is trying to understand the effects of a new drug. For drug safety, the benefits outweigh the cost of using a larger sample size. But for consumer preferences, a smaller sample size at a lower cost could provide good enough results.

## Knowing the basics is helpful

Knowing the basics will help you make the right choices when it comes to sample size. You can always raise concerns if you come across a sample size that is too small. A sample size calculator is also a great tool for this. Sample size calculators let you enter a desired confidence level and margin of error for a given population size. They then calculate the sample size needed to statistically achieve those results.

Refer to the [Determine the Best Sample Size](https://www.coursera.org/learn/process-data/lecture/mSj5A/determine-the-best-sample-size) video for a demonstration of a sample size calculator, or refer to the [Sample Size Calculator](https://www.coursera.org/learn/process-data/supplement/ZqcDw/sample-size-calculator) reading for additional information.

## Key takeaways

As you continue on your data analytics journey, be sure to familiarize yourself with key terms including population, sample, margin of error, confidence level, and confidence interval before calculating sample size. Remember that a minimum sample size of 30 is recommended and that sample size varies depending on the specific business problem. Also consider the trade-off between accuracy and cost when determining sample size, as larger sample sizes provide more accurate results but at a higher cost. Finally, use sample size calculators to determine the appropriate sample size for your study.

---

# Pre-cleaning activities

Before data analysts can analyze data, they first need to think about and understand the data they're working with. Assessing data integrity is a key step in this process. As you've learned in previous lessons, you should complete the following tasks before analyzing data:

## Step 1: Review data integrity

1. Determine data integrity by assessing the overall accuracy, consistency, and completeness of the data.

2. Connect objectives to data by understanding how your business objectives can be served by an investigation into the data.

3. Know when to stop collecting data.

Data analysts perform pre-cleaning activities to complete these steps. Pre-cleaning activities help you determine and maintain **data integrity,** which is essential to the role of a junior data analyst.

## **Step 2: Identify what makes data insufficient**

One of the objectives of pre-cleaning activities is to address insufficient data. Recall from previous lessons that data can be insufficient for a number of reasons. Insufficient data has one or more of the following problems:

- Comes from only one source
- Continuously updates and is incomplete
- Is outdated
- Is geographically limited

## **Step 3: Deal with insufficient data**

To deal with insufficient data, you can:

- Identify trends within the available data.
- Wait for more data if time allows.
- Discuss with stakeholders and adjust your objective.
- Search for a new dataset.

---