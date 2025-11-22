# Test your data

---

# Using statistical power

This video introduces the concept of **statistical power**, a crucial aspect of data analysis. It explains how statistical power helps you obtain meaningful results from your tests and studies.

### **Key Points**

- **What is statistical power?** It's the probability of getting **meaningful results** from a test or study.
- **Why is it important?** Statistical power helps you avoid drawing **false conclusions** based on random chance.
- **How does it work?** A larger sample size generally leads to **greater statistical power**.
- **What is a statistically significant result?** It means the results are **real and not due to chance**.
- **What is a good statistical power?** Aim for a power of at least **0.8 (80%)**.

### **Example**

- A restaurant chain wants to test a new milkshake ad.
- They need a large enough sample size to ensure the results are not influenced by factors like customer preferences or promotions.
- A higher statistical power increases the confidence in the results.

### **Additional Points**

- Statistical power is essential for data analysts to make **informed decisions**.
- It helps you **avoid misleading conclusions** and **maximize the impact** of your work.

### **Definitions**

- **Hypothesis testing:** A method to determine if a survey or experiment has meaningful results.
- **Sample size:** The number of individuals or items included in a study.
- **Statistically significant:** A result that is unlikely to be due to chance.

**Remember**

- Statistical power is a valuable tool for data analysts.
- Understanding and applying it correctly leads to **better data-driven decisions**.

---

# When data isn’t readily available

Earlier, you learned how you can still do an analysis using proxy data if you have no data. You might have some questions about proxy data, so this reading will give you a few more examples of the types of datasets that can serve as alternate data sources.

## Proxy data examples

Sometimes the data to support a business objective isn’t readily available. This is when proxy data is useful. Take a look at the following scenarios and where proxy data comes in for each example:

| **Business scenario** | **How proxy data can be used** |
| --- | --- |
| A new car model was just launched a few days ago and the auto dealership can’t wait until the end of the month for sales data to come in. They want sales projections now. | The analyst proxies the number of clicks to the car specifications on the dealership’s website as an estimate of potential sales at the dealership. |
| A brand new plant-based meat product was only recently stocked in grocery stores and the supplier needs to estimate the demand over the next four years. | The analyst proxies the sales data for a turkey substitute made out of tofu that has been on the market for several years. |
| The Chamber of Commerce wants to know how a tourism campaign is going to impact travel to their city, but the results from the campaign aren’t publicly available yet. | The analyst proxies the historical data for airline bookings to the city one to three months after a similar campaign was run six months earlier. |

## Open (public) datasets

If you are part of a large organization, you might have access to lots of sources of data. But if you are looking for something specific or a little outside your line of business, you can also make use of open or public datasets. (You can refer to this [Medium article](https://medium.com/thinkdata/is-there-a-difference-between-open-data-and-public-data-2b8d5608b2f1) for a brief explanation of the difference between open and public data.)

Here's an example. A nasal version of a vaccine was recently made available. A clinic wants to know what to expect for contraindications, but just started collecting first-party data from its patients. A **contraindication** is a condition that may cause a patient not to take a vaccine due to the harm it would cause them if taken. To estimate the number of possible contraindications, a data analyst proxies an open dataset from a trial of the injection version of the vaccine. The analyst selects a subset of the data with patient profiles most closely matching the makeup of the patients at the clinic.

There are plenty of ways to share and collaborate on data within a community. Kaggle ([kaggle.com](https://www.kaggle.com/)) which we previously introduced, has datasets in a variety of formats including the most basic type, Comma Separated Values (CSV) files.

### **CSV, JSON, SQLite, and BigQuery datasets**

- CSV: Check out this [Credit card customers](https://www.kaggle.com/sakshigoyal7/credit-card-customers) dataset, which has information from 10,000 customers including age, salary, marital status, credit card limit, credit card category, etc. (CC0: Public Domain, Sakshi Goyal).
- JSON: Check out this JSON dataset for [trending YouTube videos](https://www.kaggle.com/datasnaek/youtube-new) (CC0: Public Domain, Mitchell J).
- SQLite: Check out this SQLite dataset for 24 years worth of [U.S. wildfire data](https://www.kaggle.com/rtatman/188-million-us-wildfires) (CC0: Public Domain, Rachael Tatman).
- BigQuery: Check out this [Google Analytics 360](https://www.kaggle.com/bigquery/google-analytics-sample) sample dataset from the Google Merchandise Store (CC0 Public Domain, Google BigQuery).

Refer to the Kaggle [documentation for datasets](https://www.kaggle.com/docs/datasets) for more information and search for and explore datasets on your own at [kaggle.com/datasets](https://www.kaggle.com/datasets).

As with all other kinds of datasets, be on the lookout for duplicate data and ‘Null’ in open datasets. Null most often means that a data field was unassigned (left empty), but sometimes Null can be interpreted as the value, 0. It is important to understand how Null was used before you start analyzing a dataset with Null data.

## **Key takeaways**

As you work on data analysis projects, proxy data can often be used to estimate or predict outcomes when actual data is not available. Open or public datasets can be used as proxy data sources, and there are many available online repositories for finding relevant datasets. But be cautious when using proxy data and ensure that it is well-suited for the intended purpose. Finally, check for duplicate data and null values in open datasets before using them for analysis.

---

# Determine the best sample size

### **Key Points**

- **Data integrity:** Refers to the accuracy, completeness, and consistency of data. It's crucial for ensuring reliable and trustworthy results from data analysis.
- **Sample size:** Represents a portion of a larger population used to draw conclusions about the entire population. Choosing the right sample size is essential for achieving accurate and representative results.
- **Confidence level:** Indicates the probability that a sample accurately reflects the larger population. A higher confidence level signifies greater certainty in the results.
- **Margin of error:** Represents the potential difference between the sample results and the results obtained from the entire population. A smaller margin of error indicates higher accuracy.

### **Definitions**

- **Population:** The entire group of individuals or objects being studied.
- **Sample:** A subset of the population selected for analysis.
- **Confidence interval:** A range of values within which the true population value is likely to fall, with a certain level of confidence.
- **Statistical significance:** The likelihood that observed results are not due to chance.

### **Real-life Example**

Imagine a company wants to understand customer preferences for a new product. They conduct a survey with a sample size of 200 customers, aiming for a 95% confidence level and a 5% margin of error. The results show that 60% of the sample prefer the new product. With a 95% confidence level, we can be reasonably certain that the true population preference falls within a range of 55% to 65%.

### **Additional Points**

- The video provides a high-level overview of sample size and data integrity.
- It encourages viewers to explore online calculators for determining appropriate sample sizes.
- The video emphasizes the importance of understanding these concepts for effective data analysis.

---

# Sample size calculator

In this reading, you will learn the basics of sample size calculators, how to use them, and how to understand the results. A **sample size calculator** tells you how many people you need to interview (or things you need to test) to get results that represent the target population. Let’s review some terms you will come across when using a sample size calculator:

- **Confidence level**: The probability that your sample size accurately reflects the greater population.
- **Margin of error**: The maximum amount that the sample results are expected to differ from those of the actual population.
- **Population**: This is the total number you hope to pull your sample from.
- **Sample**: A part of a population that is representative of the population.
- **Estimated response rate**: If you are running a survey of individuals, this is the percentage of people you expect will complete your survey out of those who received the survey.

## How to use a sample size calculator

In order to use a sample size calculator, you need to have the population size, confidence level, and the acceptable margin of error already decided so you can input them into the tool. If this information is ready to go, check out these sample size calculators below:

- [Sample size calculator by surveymonkey.com](https://www.surveymonkey.com/mp/sample-size-calculator/)
- [Sample size calculator by raosoft.com](http://www.raosoft.com/samplesize.html)

## What to do with the results

After you have plugged your information into one of these calculators, it will give you a recommended sample size. Keep in mind, the calculated sample size is the **minimum** number to achieve what you input for confidence level and margin of error. If you are working with a survey, you will also need to think about the estimated response rate to figure out how many surveys you will need to send out. For example, if you need a sample size of 100 individuals and your estimated response rate is 10%, you will need to send your survey to 1,000 individuals to get the 100 responses you need for your analysis.

Now that you have the basics, try some calculations using the sample size calculators and refer back to this reading if you need a refresher on the definitions.

---